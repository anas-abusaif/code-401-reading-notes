# Django REST Framework & Docker

Docker is really just Linux containers which are a type of virtualization.

Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

## Install Docker

To install Docker we need to download the desktop app on our computer and create a free account. The initial download of Docker might take some time to download. It’s a big file. Feel free to stretch your legs at this point!

Once Docker is done installing we can confirm the correct version is running. It should be at least version 19.

```
docker --version
```

Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command 

```
sudo pip install docker-compose 
```

after your Docker installation is complete.

Now run the command below to confirm you have a working version of it, too. The version should be at least 1.24.x.

$ docker-compose --version
docker-compose version 1.24.1, build 4667896b

## Library Website and API

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

First we need a dedicated directory on our computer to store the code. This can live anywhere but for convenience, if you are on a Mac, we can place it in the Desktop folder. The location really does not matter; it just needs to be easily accessible.

A traditional Django website consists of a single project and one (or more) apps representing discrete functionality. Let’s create a new project with the startproject command. Don’t forget to include the period . at the end which installs the code in our current directory. If you do not include the period, Django will create an additional directory by default.