
# DockerLab


**Author:** Mohamed Mohamed  
**Email:** mohamed0395@gmail.com

---

![Image](https://i.imgur.com/HnoDik4.png)

---

## Introducing My Docker Project!

### What is Docker?

Docker is a platform that automates app deployment using containers. One thing I didn't expect to run into was port conflicts. If multiple containers try to bind to the same host port, one will fail. This project took me 2.5 hours to complete.

---

## Understanding Containers and Docker

### Containers

Containers are isolated, lightweight environments that package everything needed to run an application. They are useful because they ensure software runs consistently and reliably across different computing environments.

A container image is a template for containers. In Docker, it serves as a blueprint for containers, enabling consistent, portable deployment across different environments by packaging all dependencies together.

### Docker

Docker is an open-source platform that automates app development using containers. Docker Desktop is a GUI-based tool for managing Docker containers on Windows or Mac OS.

The Docker daemon is a persistent background process that manages and coordinates all Docker objects like containers, images, and networks. It listens for Docker API requests and handles container lifecycle operations.

---

## Running an Nginx Image

Nginx is an open-source web server that also functions as a reverse proxy, load balancer, and HTTP cache. It's known for high performance, stability, and scalability, and is widely used to serve web content and manage network traffic efficiently.

The command I ran to start a new container was `docker run -d -p 80:80 nginx`. I used an Nginx container image, ran it in detached mode, and mapped port 80, allowing me to access the webpage locally.

![Image](https://i.imgur.com/hfEzLRU.png)

---

## Creating a Custom Image

The Dockerfile is a document with all the instructions for building your Docker image. Docker would read a Dockerfile to understand how to set up my application's environment and which software packages it should install.

My docker file tells Docker three things, which base image to use, what commands to run during image creation, and how to start the application when a container launches.

The command I used to build a custom image with my Dockerfile was `docker build -t my-web-app .` The `.` at the end of the command means it tells Docker to find the Dockerfile in the current directory.

![Image](https://i.imgur.com/P3Ldh6d.png)

---

## Running My Custom Image

There was an error when I ran my custom image because there was already a container using port 80, so the new container I was creating couldn't access it. I resolved it by heading over to the Docker software and stopping the "nginx" container.

In this example, the container image is the blueprint that tells Docker application code, libraries etc that should be in the container. The container works as software that's created from this image and running web server displaying my index.html.  

![Image](https://i.imgur.com/GC2SXG3.png)

---

## Elastic Beanstalk

AWS Elastic Beanstalk is a service that simplifies deploying, managing, and scaling applications. It handles infrastructure, load balancing, capacity provision, auto scaling and application health monitoring.

Deploying my custom image with Elastic Beanstalk took me about 10 mins

![Image](https://i.imgur.com/KFPKAgz.png)

---

## Deploying App Updates

To learn how to deploy app updates with Elastic Beanstalk, I updated my app by changing a few things in my index.html, i verified those changes by opening the file locally on my computer.

![Image](https://i.imgur.com/qGbpWBP.png)

---

---
