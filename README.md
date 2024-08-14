# Microservices Architecture with Python, Kubernetes, RabbitMQ, MongoDB, and MySQL

## Overview

This repository showcases a microservices architecture demonstrating the integration of various technologies including Python, Kubernetes, RabbitMQ, MongoDB, and MySQL. The system is designed to be scalable, reliable, and maintainable with each component handling specific functionalities.

### Technologies Used

- **Python**: Core programming language for developing microservices.
- **Flask**: Lightweight web framework for building RESTful APIs.
- **Kubernetes**: Orchestrates containerized applications for deployment, scaling, and management.
- **RabbitMQ**: Message broker for managing asynchronous communication between services.
- **MongoDB**: NoSQL database for schema-less data storage.
- **MySQL**: Relational database for structured data storage.

## Features

- **Microservices**: Modular services each handling a specific part of the system.
- **Asynchronous Communication**: Utilizes RabbitMQ for efficient message queuing.
- **Scalability**: Managed by Kubernetes for scaling and orchestration.
- **Flexible Data Storage**: Combines MongoDB for unstructured data and MySQL for structured data.

## Getting Started

### Prerequisites

1. **Docker**: Install Docker from [Docker's official website](https://www.docker.com/get-started).
2. **Kubernetes**: Set up Kubernetes and install `kubectl`. Instructions can be found [here](https://kubernetes.io/docs/tasks/tools/).
3. **Python 3.x**: Ensure Python is installed for local development and testing.

### Setting Up the Environment

1. **Clone the Repository**

    ```bash
    git clone https://github.com/yourusername/microservices-architecture.git
    ```

2. **Build Docker Images**

    Build Docker images for each microservice:

    ```bash
    docker-compose build
    ```

3. **Run Services Locally**

    To run the microservices locally using Docker Compose:

    ```bash
    docker-compose up
    ```

4. **Deploy to Kubernetes**

    Apply Kubernetes configurations to deploy the services:

    ```bash
    kubectl apply -f k8s/
    ```

    Ensure your Kubernetes cluster is properly configured and running.

5. **Configure Databases**

    - **MongoDB**: Configure MongoDB settings in the `.env` files of your services.
    - **MySQL**: Set up MySQL and configure connection strings in the relevant services.

6. **Access the Services**

    Once deployed, you can access the services through the exposed endpoints. Refer to the Kubernetes service configuration for specific URLs.

## API Endpoints

Each microservice has its own set of API endpoints. Check the documentation in each service's directory for detailed information.

## Configuration

Configuration files are located in the `config` directory. Update these files with your environment-specific settings, including database connections, RabbitMQ settings, and other service configurations.

## Testing

To run tests locally for each microservice:

```bash
pytest
