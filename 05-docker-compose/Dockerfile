# The base image on which we would build our image
FROM openjdk:17-jdk-alpine

# Install curl and maven
RUN apk --no-cache add curl maven

# Set environment variables
ENV PORT=${PORT}
ENV DB_HOST=${DB_HOST}
ENV DB_NAME=${DB_NAME}
ENV DB_USER=${DB_USER}
ENV DB_PASS=${DB_PASS}

# Expose port 8081
EXPOSE 8081

# Set the working directory
WORKDIR /app

# Copy the pom.xml file to the working directory
COPY pom.xml .

# Resolve the dependencies in the pom.xml file
RUN mvn dependency:resolve

# Copy the source code to the working directory
COPY src src

# Build the project
RUN mvn package -DskipTests

# Run the application
ENTRYPOINT ["java", "-jar", "target/rest-demo.jar"]
