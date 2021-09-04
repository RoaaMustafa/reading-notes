# Django REST Framework & Docker

## Docker 

Docker is an open platform for developing, shipping, and running applications. 

 Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. 
 
 Docker provides the ability to package and run an application in a loosely isolated environment called a container. 
 The isolation and security allow you to run many containers simultaneously on a given host.
 Containers are lightweight and contain everything needed to run the application, so you do not need to rely on what is currently installed on the host. 
 You can easily share containers while you work, and be sure that everyone you share with gets the same container that works in the same way.
 
 ![docker-architecture](https://docs.docker.com/engine/images/architecture.svg)
 
 ## Linux Containers
 
 Docker is really just Linux containers which are a type of virtualization.

 Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm.
 How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

 If you rent space on a cloud provider like AWS they are typically not providing you with a dedicated piece of hardware. 
 Instead you are probably sharing a physical server with hundreds or even thousands of other clients.

  What’s the downside to a virtual machine? Size and speed. A typical guest operating system can easily take up 700MB of size.
  So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.


 
## Containers vs Virtual Environments


Virtual environments are used to isolate Python software packages locally.

We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

## Install Docker

Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. 
However if you are on Linux, you will need to add it manually. You can do this by running the command sudo pip install docker-compose after your Docker installation is complete.

To confirm Docker installed correctly we can run our first command docker run hello-world


## Images and Containers

Images and containers are the two fundamental concepts to grasp when you start with Docker. 
An image is a snapshot in time of what a project contains. A container is a running instance of the image.

When we ran hello-world we used an official Docker image. We did not have to create the image ourself. 
But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.

##  Library Website and API

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework;
it always must be added to a project after Django itself has been installed and configured.

## Django REST Framework


Django REST Framework is added just like any other third-party app.
Make sure to quit the local server `Control + c` if it is still running.
Then on the command line type the below.

`(library) $ pipenv install djangorestframework~=3.11.0`


### URLs

Adding an API endpoint is just like configuring a traditional Django app’s routes.
First at the project-level we need to `include` the `api `app and configure its URL route, which will be `api/`

### Views

`views.py` file which relies on Django REST Framework’s built-in generic class views. 
These deliberately mimic traditional Django’s generic class-based views in format, but they are not the same thing.


### Serializers

A serializer translates data into a format that is easy to consume over the internet, typically JSON, and is displayed at an API endpoint. 
We will also cover serializers and JSON in more depth in following chapters. 
For now I want to demonstrate how easy it is to create a serializer with Django REST Framework to convert Django models to JSON.

### cURL
We want to see what our API endpoint looks like. We know it should return JSON at the URL `http://127.0.0.1:8000/api/`

### Browsable API

With the local server still running in the first command line console, navigate to our API endpoint in the web browser at` http://127.0.0.1:8000/api/`.
