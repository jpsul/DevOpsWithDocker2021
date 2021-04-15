# Java 8 base image
FROM openjdk:8

EXPOSE 8080

WORKDIR /usr/src/app

# Copy project files to image
COPY . .

# Build the project in image
RUN ./mvnw package

# Run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
