# Docker
- Docekr is one of the methods used to isolate and run entire applications using any operating system, everything is isolated : programming language, software packages, databases, and more.
- it is used instead of virtual environments.
-  Docker can be shared among team members so everyone is working on the same setup. 

## Containers vs Virtual Environments
Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer.
- virtual environments can only isolate Python packages.

## Images and Containers
Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.
When we ran hello-world we used an official Docker image. We did not have to create the image ourself. But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.

- A Dockerfile is the recipe for a cake
- An image is a snapshot of the recipe at a given time
- A docker-compose.yml says how to make the cake
- And the container is the actual, baked cake

## Images
- First create a local directory on your computer for our code. 
- define the image with a Dockerfile. This is similar to a Pipenv or a requirements.txt file; it is a list of all the requirements needed to build our image. It is simpler to have them all in one place rather than install each manually line-by-line.
- ith your text editor add the following single line of code to the Dockerfile.

```
FROM python:3.7-alpine
```
- . The first instruction must be the FROM command which lets us import a base image to use for our image. This base image could be another Docker image or one we create entirely from scratch.


## Image Builds
```
$ docker image build .
Sending build context to Docker daemon  2.048kB
Step 1/1 : FROM python:3.7-alpine
3.7-alpine: Pulling from library/python
c9b1b535fdd9: Pull complete
2cc5ad85d9ab: Pull complete
53a2fca3c2ea: Pull complete
30fce49de8b1: Pull complete
49bcb9571cc7: Pull complete
Digest: sha256:7655eea15dfd981eeb7d243af21e8561e967709caba938d50b136cdb992f3546
Status: Downloaded newer image for python:3.7-alpine
 ---> b2c276538711
Successfully built b2c276538711
```

We can list all existing Docker images to confirm this new one has been built alongside the initial alpine image.
```
 docker image ls
REPOSITORY      TAG             IMAGE ID            CREATED             SIZE
python          3.7-alpine      b2c276538711        3 days ago          97.7MB
hello-world     latest          fce289e99eb9        12 months ago       1.84kB
```

## Image Layers
Every image is made up of one or more image layers. The base layer is often a flavor of Linux, like alpine. When we built the image for python:3.7-alpine this image had the id b2c276538711. But that image depended on five other images which were visible while building it:
This is called image layering and it exists for two main reasons:
1. each image layer is immutable–unchanged–like a git commit. This helps ensure consistency when two developers build the same image.
2. performance. Docker caches the steps in a Dockerfile to speed up subsequent builds. When a change is made to a step, all steps following it will be executed from scratch.

> For this reason, order matters in a Dockerfile. Typically you want to put code that won’t change often at the top and code that will change at the end.

## Containers
- create a django project

## Dockerized Django
We’ll now create a Dockerfile for our image which will completely replace our local dev environment, so this will have Python 3 and Django. Then we’ll add a docker-compose.yml for the container instructions. Make each file via the command line.

```
touch Dockerfile
touch docker-compose.yml
```

[Continue to use docker in django](https://wsvincent.com/beginners-guide-to-docker/)


