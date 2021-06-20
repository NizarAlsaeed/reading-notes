# A Beginner's Guide to Docker
With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated.

This, fundamentally, is what Docker is. A way to implement Linux containers!

## Containers vs Virtual Environments
Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 
and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version.
Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.


## After installing Docker

A good command to inspect Docker is `docker info` which we can run now.

 to inspect just the current image?

`$ docker image ls`

## Images and Containers
An image is a snapshot in time of what a project contains. A container is a running instance of the image.

typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.
There are a large number of official images available on Docker Hub for common software like different flavors of Linux, programming languages, and so on.

## Image Layers
Every image is made up of one or more image layers.
 it exists for two main reasons. First, each image layer is immutable–unchanged–like a git commit. This helps ensure consistency
 when two developers build the same image. The second reason is performance. 
