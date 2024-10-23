# Docker Compose

This project demonstrates how to use Docker Compose to run a Spring Boot application alongside a MySQL database.

## Requirements

Before you begin, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/) 20.10.8 or later

## Intallation

### Step 1: Clone the Repository

First, clone the project from the repository:

```sh
git clone https://github.com/nguyenkhanhquy/docker-with-java.git
```

### Step 2: Navigate to the Project Directory

Change into the project directory:

```sh
cd docker-with-java/05-docker-compose
```

### Step 3: Build and Run the Application

To build and run the application, use the following command:

```sh
docker-compose up --build
```

After the application starts, open your web browser and navigate to `http://localhost:8081/students` to access it.

### Step 4: Stop the Application

To stop the Spring Boot application, simply press `CTRL + C`.

### Step 5: Shut Down the Application

To shut down all services, use the following command:

```sh
docker-compose down
```

## Author

- Author Name: `Nguyễn Khánh Quy`
- Email: <nguyenkhanhquy123@gmail.com>
