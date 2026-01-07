# CODTECH Internship – Task 3  
## Kubernetes Microservices Deployment

## 📌 Objective
Deploy a simple microservices-based application on a Kubernetes cluster using Minikube.

---

## 🏗️ Architecture Overview
The application consists of two microservices:

- **Frontend**
  - Technology: Nginx
  - Exposure: NodePort Service
- **Backend**
  - Technology: Python HTTP Server
  - Exposure: ClusterIP Service (internal)

---

## ⚙️ Kubernetes Resources Used
- **Deployments**
  - 2 replicas for frontend
  - 2 replicas for backend
- **Services**
  - ClusterIP (backend)
  - NodePort (frontend)

---

## 🚀 Deployment Steps
1. Installed Docker, kubectl, and Minikube
2. Started a local Kubernetes cluster using Minikube
3. Created Kubernetes YAML configuration files
4. Deployed resources using `kubectl apply`
5. Verified pod and service status
6. Accessed the frontend service via NodePort

---


