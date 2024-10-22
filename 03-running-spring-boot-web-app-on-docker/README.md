# Running Spring Boot Web App On Docker

This project demonstrates how to run a Spring Boot web application using Docker.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/) 20.10.8 or later
- [Apache Maven](https://maven.apache.org/download.cgi) 3.9.9 or later

## Intallation

### Step 1: Clone the Repository

First, clone the project from the repository:

```sh
git clone https://github.com/nguyenkhanhquy/docker-with-java.git
```

### Step 2: Navigate to the Project Directory

Change into the project directory:

```sh
cd docker-with-java/03-running-spring-boot-web-app-on-docker
```

### Step 3: Build the Project

Build the project using Maven:

```sh
.\mvnw clean package
```

**Note**: If you prefer, you can replace `.\mvnw` with `mvn` if Maven is installed globally on your machine.

### Step 4: Build the Docker Image

Create the Docker image using the provided `Dockerfile`:

```sh
docker build -t test/rest-demo:v1 .
```

**Explanation of the Dockerfile:**

The following is a brief explanation of the contents of the `Dockerfile`:

```dockerfile
FROM openjdk:24-jdk
```

- This line specifies the base image to use, which is OpenJDK 24. It provides the necessary environment for running Java applications.

```dockerfile
ARG JAR_FILE=target/*.jar
```

- This line defines a build argument `JAR_FILE`, which points to the location of the JAR file generated by Maven.

```dockerfile
COPY ${JAR_FILE} app.jar
```

- This line copies the JAR file from the specified location into the Docker image and renames it to `app.jar`.

```dockerfile
ENTRYPOINT ["java","-jar","/app.jar"]
```

- This line sets the command to execute when the container starts, which is to run the Java application using the `app.jar` file.

### Step 5: Run the Application

Launch the Docker container:

```sh
docker run -p 8081:8081 test/rest-demo:v1
```

Open your web browser and go to `http://localhost:8081/` to access the application.

### Step 6: Stop the Application

To stop the Spring Boot application, simply press `CTRL + C`.

## Author

- Author Name: `Nguyễn Khánh Quy`
- Email: <nguyenkhanhquy123@gmail.com>