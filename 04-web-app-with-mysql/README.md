# Web App With MySQL

This is a simple Spring Boot web app that uses MySQL as a database.

## Requirements

Before you begin, ensure you have the following installed:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) 17 or later
- [MySQL](https://dev.mysql.com/downloads/mysql/) 8.0 or later
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
cd docker-with-java/04-web-app-with-mysql
```

### Step 3: Create a MySQL Database

Create a MySQL database named `student_db`:

```sql
CREATE DATABASE student_db;
```

### Step 4: Configure application.properties

Open the `src/main/resources/application.properties` file and update it with your MySQL connection details:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_db
spring.datasource.username=[your_mysql_username]
spring.datasource.password=[your_mysql_password]
```

Make sure to replace `[your_mysql_username]` and `[your_mysql_password]` with your actual MySQL credentials.

### Step 5: Build the Project

Build the project using Maven:

```sh
.\mvnw clean package
```

### Step 6: Run the Application

After building the project, navigate to the target directory and run the application:

```sh
cd target
java -jar rest-demo.jar
```

Open your web browser and go to `http://localhost:8081/students` to access the application.

### Step 7: Stop the Application

To stop the Spring Boot application, simply press `CTRL + C`.

### Alternatively, you can run the application directly with

```sh
.\mvnw spring-boot:run
```

**Note**: If you prefer, you can replace `.\mvnw` with `mvn` if Maven is installed globally on your machine.

## Author

- Author Name: `Nguyễn Khánh Quy`
- Email: <nguyenkhanhquy123@gmail.com>
