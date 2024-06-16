# MERN App Deployment with Kubernetes

## Description
This MERN application includes a backend server built with Node.js and Express, a MongoDB database, and a frontend developed with React. The repository is prepared to be deployed in a Kubernetes environment, with services for MongoDB and webchat.

## Requirements
- Node.js (v12 or higher)
- npm
- MongoDB (or a cloud MongoDB instance like MongoDB Atlas)
- Docker
- Kubernetes
- kubectl

## Deployment Using Kubernetes
Make sure you have a Kubernetes cluster running and kubectl configured to interact with your cluster.

### 1. Create the secrets for MongoDB:
```bash
kubectl create secret generic mongodb-secret --from-literal=mongo-user=pass --from-literal=mongo-password==pass=

### 2. Deploy services and deployments
kubectl apply -f k8s/mongodb-deployment.yaml
kubectl apply -f k8s/mongodb-service.yaml
kubectl apply -f k8s/webchat-deployment.yaml
kubectl apply -f k8s/webchat-service.yaml
