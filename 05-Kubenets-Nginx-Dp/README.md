# 🚀 Kubernetes NGINX Deployment with Minikube

This repository demonstrates how to deploy and expose an **NGINX web server** on **Minikube** using `kubectl`.



## 🔹 Prerequisites
- [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed
- [kubectl](https://kubernetes.io/docs/tasks/tools/) installed
- Docker or Hyper-V driver set up

Start Minikube:
```bash
minikube start 
```
## 🛠 Steps to Deploy NGINX
1️⃣ Create Deployment

- Create a deployment that runs the latest NGINX image:
```bash
kubectl create deployment local-nginx --image=nginx:latest
```
![Image Alt](
✔️ This creates a deployment named local-nginx.

2️⃣ Check Deployment

- Verify if the deployment is running:
```bash
kubectl get deployment
```

3️⃣ Get Pods

- Check the pod(s) created by the deployment:
```bash
kubectl get pods
```
✔️ Pods are the smallest deployable units in Kubernetes.

4️⃣ Open Minikube Dashboard

- Launch the Kubernetes web UI:
```bash
minikube dashboard
```
✔️ A browser window will open with a graphical interface.

5️⃣ Expose Deployment as a Service

- Expose the deployment so it can be accessed externally:
```bash
kubectl expose deployment local-nginx --port=80 --type=LoadBalancer
```
- --port=80 → the service will listen on port 80
- --type=LoadBalancer → makes the app accessible outside the cluster

6️⃣ Check Services

- List all services running in the cluster:
```bash
kubectl get service
```

7️⃣ Access NGINX in Browser

- Open the service in your default browser:
```bash
minikube service local-nginx
```
✔️ You should see the NGINX welcome page 🎉

# 🧹 Cleanup (Optional)

 - Delete the resources when you’re done:
```bash
kubectl delete service local-nginx
kubectl delete deployment local-nginx
```
✅ Summary

- Created an NGINX deployment

- Verified pods and deployment

- Exposed it as a LoadBalancer service

- Accessed it via Minikube service

🎯 You have successfully deployed NGINX on Kubernetes with Minikube!

