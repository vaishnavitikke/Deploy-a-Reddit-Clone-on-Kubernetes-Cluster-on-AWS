# Deploy-a-Reddit-Clone-on-Kubernetes-Cluster-on-AWS

Deployed a Reddit Clone app using Docker containers, Kubernetes (Minikube), and AWS EC2.

## Tech Stack 
- Docker  
- Kubernetes (Minikube + kubectl)  
- AWS EC2 (Ubuntu)

Installation
Follow these steps to install and run the Reddit clone app on your local machine:

1. Clone this repository to your local machine: git clone 
2. Navigate to the project directory: cd reddit-clone-k8s-ingress
3. Build the Docker image for the Reddit clone app: docker build -t reddit-clone-app .
4. Deploy the app to Kubernetes: kubectl apply -f deployment.yaml
5. Deploy the Service for deployment to Kubernetes: kubectl apply -f service.yaml
6. Enable Ingress by using Command: minikube addons enable ingress
7. Expose the app as a Kubernetes service: kubectl expose deployment reddit-deployment --type=NodePort --port=5000
8. Create an Ingress resource: kubectl apply -f ingress.yaml

## Steps
1. Launch EC2 Instances 
   - CI Server (Docker build & push)  
   - Deployment Server (K8s cluster)

2. Dockerize App
   - Build and push image to Docker Hub

3. Minikube Setup
   - Install Docker, Minikube, and kubectl on Deployment EC2  
   - Start cluster: `minikube start --driver=docker`

4. Kubernetes Deployment
   - Apply `Deployment.yml` and `Service.yml`  
   - Expose service using `NodePort` or `Ingress`

5. Access App
   - Visit `http://<EC2-IP>:3000` or Ingress domain

## ✅ Output
Live Reddit clone running on AWS-hosted Kubernetes cluster.
