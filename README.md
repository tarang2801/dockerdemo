# Docker Demo

A Spring Boot application designed to demonstrate containerization with Docker, Docker Compose, and Kubernetes deployment manifests.

## Overview

This project is a Java 17 Spring Boot application using Spring MVC and OpenAPI support. It includes:

- Docker support via a Dockerfile
- Compose configuration for local container orchestration
- Kubernetes manifests for deployment and service exposure
- Maven wrapper for easy local builds

## Tech Stack

- Java 17
- Spring Boot 4
- Spring MVC
- Springdoc OpenAPI
- Docker
- Kubernetes
- Maven

## Project Structure

```text
dockerdemo/
├── Dockerfile
├── compose.yaml
├── deployment.yaml
├── service.yaml
├── pom.xml
├── mvnw
├── mvnw.cmd
├── .mvn/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/docker/dockerdemo/
│   │   └── resources/
│   │       └── application.properties
│   └── test/
└── README.md
```

## Prerequisites

Before running this project, make sure you have:

- Java 17 or later
- Maven or the included Maven wrapper
- Docker installed
- Docker Compose installed
- (Optional) Kubernetes CLI for deployment manifests

## Run Locally

Clone the repository:

```bash
git clone https://github.com/tarang2801/dockerdemo.git
cd dockerdemo
```

Start the application with Maven:

```bash
./mvnw clean package
./mvnw spring-boot:run
```

The application will run on the default Spring Boot port:

```text
http://localhost:8080
```

## Run with Docker

Build the Docker image:

```bash
docker build -t dockerdemo .
```

Run the container:

```bash
docker run -p 8080:8080 dockerdemo
```

## Run with Docker Compose

```bash
docker compose up --build
```

This uses the project’s `compose.yaml` configuration to run the app in a containerized environment.

## Kubernetes Deployment

The repository includes Kubernetes deployment files:

- `deployment.yaml`
- `service.yaml`

Apply them using:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

## API Documentation

This project includes Springdoc OpenAPI support, which provides Swagger UI for API exploration.

Once the app is running, open:

```text
http://localhost:8080/swagger-ui/index.html
```

## Notes

This is a simple containerized Spring Boot demo intended to showcase:

- Java application packaging
- Docker image creation
- Local container execution
- Kubernetes deployment setup

## License

This project does not currently specify a license in the repository metadata.

## Author

Tarang
