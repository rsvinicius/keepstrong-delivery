# Keepstrong-Delivery

# Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Usage](#usage)
4. [License](#license)

## Overview

Keepstrong-Delivery is a sample project inspired by a delivery service like iFood. It showcases various technologies commonly used in microservice architectures. The project includes three microservices for payment, orders, and review/rating. ***Please note that these microservices are implemented as placeholders and do not contain any business logic. They serve as a starting point for integrating your own business logic into the project.*** The project also includes a Spring Batch application for Flyway migrations of MySQL tables. It utilizes Spring Cloud Eureka for service registry and discovery, with a Eureka Gateway service and Eureka Server service. Docker Compose is used to set up the required infrastructure components, including MySQL and RabbitMQ. The project is licensed under the MIT License.

## Requirements

To successfully set up and run the Delivery Project, the following requirements must be met:
- Java 17+
- Docker Compose for MySQL and RabbitMQ Setup
- IntelliJ IDEA / Netbeans / Eclipse

## Usage

To start the platform, follow the steps below. Please note that it is necessary to execute the Docker Compose file to set up the required infrastructure components, and also run the Spring Batch application for MySQL migrations.

### Setting up Infrastructure with Docker Compose
1. Ensure that you have Docker installed on your system.

2. Open a terminal or command prompt.

3. Navigate to the directory where the Docker Compose file is located.

4. Run the following command to start the infrastructure components:
    ```
    docker-compose up
    ```
    This command will download the required Docker images and start the MySQL database and RabbitMQ messaging broker.
    **Note: Keep the terminal or command prompt running while the infrastructure components are active.**

### Running Spring Batch Application for MySQL Migrations
1. Open a new terminal or command prompt.

2. Navigate to the directory where the Spring Batch application code is located.

3. Run the following command to execute the Spring Batch application for MySQL migrations:
    ```
    ./gradlew bootRun
    ```
   This command will run the Spring Batch application and execute the necessary database migrations using Flyway. 
**Note: Ensure that the Docker Compose setup is completed and the infrastructure components are running before running the Spring Batch application for migrations.**

### Starting Eureka Server

1. Open a new terminal or command prompt.

2. Navigate to the directory where the Eureka Server service code is located.

3. Run the following command to start the Eureka Server:
    ```
    ./gradlew bootRun
    ```
   This command will compile and start the Eureka Server service.

### Starting Eureka Gateway
1. Open a new terminal or command prompt.

2. Navigate to the directory where the Eureka Gateway service code is located.

3. Run the following command to start the Eureka Gateway:
    ```
    ./gradlew bootRun
    ```
   This command will compile and start the Eureka Gateway service.

### Starting Microservices
1. Open separate terminals or command prompts for each microservice you want to start.

2. Navigate to the directory where each microservice code is located.

3. Run the following command for each microservice:
    ```
    ./gradlew bootRun
    ```
   This command will compile and start the respective microservice.
    **Note: Ensure that the Docker Compose setup is completed and the infrastructure components (MySQL and RabbitMQ) are running before starting the microservices. Also, ensure that the Eureka Server and Eureka Gateway services are running and accessible before starting the microservices. The microservices rely on the Eureka Server and Gateway for service discovery and routing.**


Once all the required services are started, you can access the application through the configured URLs or endpoints. Refer to the specific documentation of each microservice for more details on the available endpoints and functionalities.

## License

The Project is licensed under the MIT License, promoting open-source collaboration and allowing users to utilize, modify, and distribute the project with minimal restrictions. This license fosters transparency and encourages the growth of open-source software.