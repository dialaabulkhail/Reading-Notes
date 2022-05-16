# Django Custom User
## Custom User Model
> always use a custom user model for all new Django projects.
- This provides far more flexibility down the line

## AbstractUser vs AbstractBaseUser
There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. 

- create a new CustomUser model
- create new UserCreation and UserChangeForm
- add the AUTH_USER_MODEL config.

```
AUTH_USER_MODEL = "accounts.CustomUser"
```

- Now update accounts/models.py with a new User model which we'll call CustomUser.

```
# accounts/models.py
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```

- We need new versions of two form methods that receive heavy use working with users. Stop the local server with Control+c and create a new file in the accounts app called forms.py.

```(accounts) $ touch accounts/forms.py```

- We'll update it with the following code to largely subclass the existing forms.

```
# accounts/forms.py
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm

from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")
```

- Finally we update admin.py since the Admin is highly coupled to the default User model.

```
# accounts/admin.py
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ["email", "username",]

admin.site.register(CustomUser, CustomUserAdmin)
```

- In the html templates you can add the following

![base](https://user-images.githubusercontent.com/97671741/168607050-c8eba236-1d06-4011-8dd1-8582832320cd.PNG)
![home](https://user-images.githubusercontent.com/97671741/168607098-4a794328-7bc0-496e-8f18-a67a33c028d0.PNG)
![reg](https://user-images.githubusercontent.com/97671741/168607123-afdbac0e-246d-4f05-8898-e5a5a197eebd.PNG)





[More](https://learndjango.com/tutorials/django-custom-user-model)
_____________
## DjangoX
[DjangoX github repo](https://github.com/wsvincent/djangox)



