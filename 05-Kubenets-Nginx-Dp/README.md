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
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/90e57540e4ca48853094892a82ae4de6d8516403/05-Kubenets-Nginx-Dp/Create%20Dp.png)

✔️ This creates a deployment named local-nginx.

2️⃣ Check Deployment

- Verify if the deployment is running:
```bash
kubectl get deployment
```
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/2fd42d168237b091dfb1d5594a71c39c02035267/05-Kubenets-Nginx-Dp/Get%20Dp.png)

3️⃣ Get Pods

- Check the pod(s) created by the deployment:
```bash
kubectl get pods
```
![image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/55ec6728ce46da956d9dc9df2d5174bec0f75254/05-Kubenets-Nginx-Dp/Get%20Pods.png)

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
![image Alt](

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

