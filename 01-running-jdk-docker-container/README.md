# Running JDK Docker Container

This guide will walk you through the steps to run a Docker container with JDK installed.

## Step 1: Install Docker

If you haven't installed Docker yet, please follow the Docker setup instructions in the README file of this repository: [Docker With Java](https://github.com/nguyenkhanhquy/docker-with-java).

## Step 2: Pull the JDK Docker Image

Open your terminal and run the following command to pull the JDK image from Docker Hub. You can choose the version you need (e.g. `openjdk:24-jdk` for OpenJDK 24):

```sh
docker pull openjdk:24-jdk
```

## Step 3: Run the JDK Docker Container

Once the image is downloaded, you can run a container with the following command:

```sh
docker run -it --name my-jdk-container openjdk:24-jdk
```

* `-it`: Runs the container in interactive mode with a terminal.
* `--name my-jdk-container`: Assigns a name to the container for easier reference.

## Step 4: Start Using JShell

Once the container is running, you will see the following output:

```sh
INFO: Created user preferences directory.
|  Welcome to JShell -- Version 24-ea
|  For an introduction type: /help intro

jshell>
```

You are now in the JShell environment, ready to execute Java code. You can type Java statements directly into the prompt (e.g. `System.out.println("Hello, World!");`), and JShell will evaluate them interactively.

## Step 5: Exit JShell

To exit the JShell environment, simply type the following command:

```sh
/exit
```

## Reference Commands

Here are some useful Docker commands for managing your container:

* List all containers (including stopped ones):

    ```sh
    docker ps -a
    ```

* Start a stopped container:

    ```sh
    docker start [CONTAINER ID]
    ```

* Execute a command in a running container (e.g. open JShell):

    ```sh
    docker exec -it [CONTAINER ID] jshell
    ```

* Stop a running container:

    ```sh
    docker stop [CONTAINER ID]
    ```

Feel free to modify the [CONTAINER ID] as needed when using these commands.
