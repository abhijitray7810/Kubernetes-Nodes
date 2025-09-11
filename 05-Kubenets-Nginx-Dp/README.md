# 🚀 Kubernetes NGINX Deployment with Minikube

This repository demonstrates how to deploy and expose an **NGINX web server** on **Minikube** using `kubectl`.



## 🔹 Prerequisites
- [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed
- [kubectl](https://kubernetes.io/docs/tasks/tools/) installed
- Docker or Hyper-V driver set up

Start Minikube:
```bash
minikube start```

🛠 Steps to Deploy NGINX
1️⃣ Create Deployment

Create a deployment that runs the latest NGINX image:
```bash
kubectl create deployment local-nginx --image=nginx:latest


✔️ This creates a deployment named local-nginx.
