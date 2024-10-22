# Docker With Java

Learn Docker, Containerization, Containers, Running App in Docker, Docker Compose.

## What is Docker?

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker's methodologies for shipping, testing, and deploying code, you can significantly reduce the delay between writing code and running it in production.

## Docker Setup

### Step 1: Access the Docker Website

Go to the official Docker website at [https://www.docker.com/](https://www.docker.com/).

### Step 2: Download Docker Desktop

1. Click on the **Get Started** or **Download Docker Desktop** button on the homepage.

1. Choose the version suitable for your Windows operating system.

### Step 3: Install Docker Desktop

1. Open the installer file that you just downloaded (it usually has a `.exe` extension).

1. Follow the installation instructions. You can select the default installation options.

1. Once the installation is complete, restart your computer if prompted.

### Step 4: Log in or Create a Docker Account

1. Open Docker Desktop.

1. If you already have a Docker account, log in. If not, you can create a new account directly from the application.

### Step 5: Verify the Installation

1. Open Command Prompt (CMD) or PowerShell.

1. Enter the following command to check the installed Docker version:

```sh
docker --version
```

### Step 6: Running First Container

```sh
docker run hello-world
```

**Hello from Docker!**

This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:

1. The Docker client contacted the Docker daemon.

1. The Docker daemon pulled the "hello-world" image from the Docker Hub.

1. The Docker daemon created a new container from that image which runs the executable that produces the output you are currently reading.

1. The Docker daemon streamed that output to the Docker client, which sent it to your terminal.

## Docker Commands

```sh
docker --help
```

Usage:  `docker [OPTIONS] COMMAND`

A self-sufficient runtime for containers

### Common Commands

`run` : Create and run a new container from an image

`exec` : Execute a command in a running container

`ps` : List containers

`build`: Build an image from a Dockerfile

`pull`: Download an image from a registry

`push`: Upload an image to a registry

`images` : List images

`login` : Log in to a registry

`logout` : Log out from a registry

`search` : Search Docker Hub for images

`version` : Show the Docker version information

`info` : Display system-wide information

### Commands

`rm` : Remove one or more containers

`rmi` : Remove one or more images

`start` : Start one or more stopped containers

`stats` : Display a live stream of container(s) resource usage statistics

`stop` : Stop one or more running containers

## Docker Architecture

![Docker Architecture](https://docs.docker.com/get-started/images/docker-architecture.webp)

## Author

- Author Name: `Nguyễn Khánh Quy`
- Email: <nguyenkhanhquy123@gmail.com>
