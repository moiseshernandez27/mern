# MERN App Deployment with Kubernetes
## Descripción

Esta aplicación MERN incluye un servidor backend construido con Node.js y Express, una base de datos MongoDB, y un frontend desarrollado con React. El repositorio está preparado para ser desplegado en un entorno Kubernetes, con servicios para MongoDB y webchat.

## Requisitos

- [Node.js](https://nodejs.org/) (v12 o superior)
- [npm](https://www.npmjs.com/)
- [MongoDB](https://www.mongodb.com/) (o una instancia de MongoDB en la nube como MongoDB Atlas)
- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

Despliegue
Usando Kubernetes
Asegúrate de tener un clúster de Kubernetes funcionando y kubectl configurado para interactuar con tu clúster.

Crea los secretos para MongoDB:
bash
Copy code
kubectl create secret generic mongodb-secret --from-literal=mongo-user=bW9uZ291c2Vy --from-literal=mongo-password=bW9uZ29wYXNzd29yZA==
Despliega los servicios y despliegues de Kubernetes:
bash
Copy code
kubectl apply -f k8s/mongodb-deployment.yaml
kubectl apply -f k8s/mongodb-service.yaml
kubectl apply -f k8s/webchat-deployment.yaml
kubectl apply -f k8s/webchat-service.yaml
Los archivos mongodb-deployment.yaml, mongodb-service.yaml, webchat-deployment.yaml y webchat-service.yaml deben estar en el directorio k8s y contener la configuración de Kubernetes para tus servicios.
