# Microservices Kubernetes Banking Project

This project provides a baseline architecture for a microservices-based banking application deployed on Kubernetes.

## Architecture Overview

The system consists of:
- **Banking API**: A Node.js-based RESTful service handling transactions and user accounts.
- **Banking DB**: A PostgreSQL database for persistent storage.

## Project Structure

```text
├── README.md
├── docker/
│   ├── api/Dockerfile
│   └── db/Dockerfile
├── k8s/
│   ├── namespace.yaml
│   ├── api-deployment.yaml
│   ├── api-service.yaml
│   ├── db-deployment.yaml
│   ├── db-service.yaml
│   ├── configmap.yaml
│   └── secrets.yaml
└── docs/
    └── architecture.png
```

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/)
- [Kubernetes (minikube, k3s, or managed service)](https://kubernetes.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

### Deployment

1. **Create the namespace**:
   ```bash
   kubectl apply -f k8s/namespace.yaml
   ```

2. **Deploy the configuration and secrets**:
   ```bash
   kubectl apply -f k8s/configmap.yaml -f k8s/secrets.yaml
   ```

3. **Deploy the Database**:
   ```bash
   kubectl apply -f k8s/db-deployment.yaml -f k8s/db-service.yaml
   ```

4. **Deploy the API**:
   ```bash
   kubectl apply -f k8s/api-deployment.yaml -f k8s/api-service.yaml
   ```
