# DRF Permissions
Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.

The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the IsAuthenticated class in REST framework.

A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.

## How permissions are determined
Permissions in REST framework are always defined as a list of permission classes.

Before running the main body of the view each permission in the list is checked. If any permission check fails, an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.

When the permission checks fail, either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

- The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.

## Object level permissions
REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.

This will either raise a PermissionDenied or NotAuthenticated exception, or simply return if the view has the appropriate permissions.
```
def get_object(self):
    obj = get_object_or_404(self.get_queryset(), pk=self.kwargs["pk"])
    self.check_object_permissions(self.request, obj)
    return obj
```

## Limitations of object level permissions
For performance reasons the generic views will not automatically apply object level permissions to each instance in a queryset when returning a list of objects.

Often when you're using object level permissions you'll also want to filter the queryset appropriately, to ensure that users only have visibility onto instances that they are permitted to view.

Because the get_object() method is not called, object level permissions from the has_object_permission() method are not applied when creating objects. In order to restrict object creation you need to implement the permission check either in your Serializer class or override the perform_create() method of your ViewSet class.

## Setting the permission policy
- The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting.

```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

- If not specified, this setting defaults to allowing unrestricted access:
```
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

- You can also set the authentication policy on a per-view, or per-viewset basis, using the APIView class-based views.

```
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```

# API Reference
[Review permission classes here](https://www.django-rest-framework.org/api-guide/permissions/)

# Overview of access restriction methods
REST framework offers three different methods to customize access restrictions on a case-by-case basis. These apply in different scenarios and have different effects and limitations.

1. queryset/get_queryset(): Limits the general visibility of existing objects from the database. The queryset limits which objects will be listed and which objects can be modified or deleted. The get_queryset() method can apply different querysets based on the current action.
2. permission_classes/get_permissions(): General permission checks based on the current action, request and targeted object. Object level permissions can only be applied to retrieve, modify and deletion actions. Permission checks for list and create will be applied to the entire object type. (In case of list: subject to restrictions in the queryset.)
3. serializer_class/get_serializer(): Instance level restrictions that apply to all objects on input and output. The serializer may have access to the request context. The get_serializer() method can apply different serializers based on the current action.

