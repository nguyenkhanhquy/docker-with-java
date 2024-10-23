# Packing The Spring Boot Web App

This project demonstrates how to package and run a Spring Boot web application.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) 17 or later
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
cd docker-with-java/02-packing-the-spring-boot-web-app
```

### Step 3: Build the Project

Build the project using Maven:

```sh
.\mvnw clean package
```

### Step 4: Run the Application

After building the project, navigate to the target directory and run the application:

```sh
cd target
java -jar rest-demo.jar
```

Open your web browser and go to `http://localhost:8081/` to access the application.

### Step 5: Stop the Application

To stop the Spring Boot application, simply press `CTRL + C`.

### Alternatively, you can run the application directly with

```sh
.\mvnw spring-boot:run
```

**Note**: If you prefer, you can replace `.\mvnw` with `mvn` if Maven is installed globally on your machine.

## Author

- Author Name: `Nguyễn Khánh Quy`
- Email: <nguyenkhanhquy123@gmail.com>
