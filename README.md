Task 3 – Kubernetes Deployment
📌 About This Task

Task 3 focuses on deploying a simple frontend–backend application using Kubernetes.
The objective of this task is to understand how applications are deployed, managed, and exposed inside a Kubernetes cluster using Deployments and Services.

This task demonstrates a basic microservices-style setup where frontend and backend components run independently and communicate through Kubernetes services.

📂 Project Structure
.
├── backend-deployment.yaml
├── backend-service.yaml
├── frontend-deployment.yaml
├── frontend-service.yaml
└── README.md

⚙️ Kubernetes Components Used
Backend Deployment (backend-deployment.yaml)

Defines the backend application pods

Manages replica count and pod lifecycle

Ensures backend availability and scalability

Backend Service (backend-service.yaml)

Exposes the backend internally within the cluster

Allows the frontend to communicate with the backend using a stable service endpoint

Frontend Deployment (frontend-deployment.yaml)

Deploys the frontend application pods

Manages replicas and application availability

Frontend Service (frontend-service.yaml)

Exposes the frontend application

Enables external or internal access depending on service type

🚀 Deployment Steps
kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-service.yaml
kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml


Verify resources:

kubectl get pods
kubectl get services

🛠️ Tools & Technologies Used

Kubernetes – Container orchestration

kubectl – Kubernetes command-line tool

YAML – Configuration files for deployments and services

Docker Images – Containerized frontend and backend applications

🎯 Learning Outcomes

Understood Kubernetes Deployments and Services

Learned how frontend and backend components communicate in a cluster

Gained hands-on experience deploying applications on Kubernetes

Improved understanding of container orchestration basics

✅ Conclusion

This task provided practical exposure to Kubernetes deployment workflows and helped build a foundation for managing containerized applications in real-world environments.
