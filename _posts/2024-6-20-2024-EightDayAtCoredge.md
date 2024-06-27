---
 layout: post
 title: DAY EIGHT AT COREDGE
 date: 2024-6-20
---
**2024-6-20- AS A LINUX ADMIN**

On day eight feeling was good as always i have learned about Docker what is docker and 
how it works what is the use case of docker and also learned some basic commands of docker...

**1. What is Docker?**


Docker is a containerization platform which packages your application and all its dependencies together in the form of containers so as to ensure that your application works seamlessly in any environment, be it development, test or production. Docker 
containers, wrap a piece of software in a complete filesystem that contains everything needed to run: code, runtime, system tools,system libraries, etc. It wraps basically anything that can be installed on a server. This guarantees that the software will 
always run the same, regardless of its environment.

**2. What is a Docker Container?**

Docker containers include the application and all of its dependencies. It shares the kernel with other containers, running as
isolated processes in user space on the host operating system. Docker containers are not tied to any specific infrastructure: 
they run on any computer, on any infrastructure, and in any cloud. Docker containers are basically runtime instances of Docker 
images.

**3. What are Docker Images?**

Docker image is the source of Docker container. In other words, Docker images are used to create containers. When a user runs a 
Docker image, an instance of a container is created. These docker images can be deployed to any Docker environment.

**4. What is Docker Hub?**

Docker images create docker containers. There has to be a registry where these docker images live. This registry is Docker Hub. 
Users can pick up images from Docker Hub and use them to create customized images and containers. Currently, the Docker Hub is theworld’s largest public repository of image containers.

**5. Explain Docker Architecture?**

Docker Architecture consists of a Docker Engine which is a client-server application with three major components:

A server which is a type of long-running program called a daemon process (the docker command).

A REST API which specifies interfaces that programs can use to talk to the daemon and instruct it what to do.

A command line interface (CLI) client (the docker command).

The CLI uses the Docker REST API to control or interact with the Docker daemon through scripting or direct CLI commands. Many 
other Docker applications use the underlying API and CLI.
Refer to this blog, to read more about Docker Architecture.

**6. What is a Dockerfile?**

Docker can build images automatically by reading the instructions from a file called Dockerfile. A Dockerfile is a text 
document that contains all the commands a user could call on the command line to assemble an image. Using docker build, users can create an automated build that executes several command-line instructions in succession.

The interviewer does not just expect definitions, hence explain how to use a Dockerfile which comes with experience. Have a look at this tutorial to understand how Dockerfile works.

**7. Tell us something about Docker Compose.**

Docker Compose is a YAML file which contains details about the services, networks, and volumes for setting up the Docker 
application. So, you can use Docker Compose to create separate containers, host them and get them to communicate with each other. Each container will expose a port for communicating with other containers.

**What is docker swarm?**

Docker Swarm is native clustering for Docker. It turns a pool of Docker hosts into a single, virtual Docker host. Docker Swarm serves the standard Docker API, any tool that already communicates with a Docker daemon can use Swarm to transparently scale to multiple hosts.


**8. What is the lifecycle of a Docker Container?**


Create a container
Run the container
Pause the container(optional)
Un-pause the container(optional)
Start the container
Stop the container
Restart the container
Kill the container
Destroy the container


**HERE ARE SOME DOCKER USEFUL COMMANDS**

**9. How to check for Docker Client and Docker Server version?**

The following command gives you information about Docker Client and Server versions:

$ docker version

**10. How do you get the number of containers running, paused and stopped?**

You can use the following command to get detailed information about the docker installed on your system.

$ docker info

Course Curriculum
Docker Certification Training Course
You can get the number of containers running, paused, stopped, the number of images and a lot more.

**11. If you vaguely remember the command and you’d like to confirm it, how will you get help on that particular command?**

The following command is very useful as it gives you help on how to use a command, the syntax, etc.

$ docker --help

The above command lists all Docker commands. If you need help with one specific command, you can use the following syntax:

$ docker <command> --help

**12. How to login into docker repository?**

You can use the following command to login into hub.docker.com:

$ docker login

You’ll be prompted for your username and password, insert those and congratulations, you’re logged in.

**13. If you wish to use a base image and make modifications or personalize it, how do you do that?**

You pull an image from docker hub onto your local system

It’s one simple command to pull an image from docker hub:

$ docker pull <image_name>

**14. How do you create a docker container from an image?**

Pull an image from docker repository with the above command and run it to create a container. Use the following command:

$ docker run -it -d <image_name>


**15. How do you list all the running containers?**

The following command lists down all the running containers:

$ docker ps

**16. Suppose you have 3 containers running and out of these, you wish to access one of them. How do you access a running container?**

The following command lets us access a running container:

$ docker exec -it <container id> bash

The exec command lets you get inside a container and work with it.

**17. How to start, stop and kill a container?**

The following command is used to start a docker container:

$ docker start <container_id>

and the following for stopping a running container:

$ docker stop <container_id>

kill a container with the following command:

$ docker kill <container_id>

**18. Can you use a container, edit it, and update it? Also, how do you make it a new and store it on the local system?**

Of course, you can use a container, edit it and update it. This sounds complicated but its actually just one command.

$ docker commit <conatainer id> <username/imagename>

**19. Once you’ve worked with an image, how do you push it to docker hub?

$ docker push <username/image name>

**20. How to delete a stopped container?**

Use the following command to delete a stopped container:

$ docker rm <container id>

**21. How to delete an image from the local storage system?**

The following command lets you delete an image from the local system:

$ docker rmi <image-id>

**22. How to build a Dockerfile?** 

Once you’ve written a Dockerfile, you need to build it to create an image with those specifications. Use the following command to build a Dockerfile:

$ docker build <path to docker file>

