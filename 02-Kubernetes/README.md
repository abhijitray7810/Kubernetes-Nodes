# What is a Cluster?
A Kubernetes Cluster is a set of machines (nodes) that work together to run your containerized applications.
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Nodes/blob/ccccccfaf7a89dd417eb12c234c1412100d34b49/02-Kubernetes/Cluster.png)
- A Kubernetes Cluster is the whole system.
It is made up of:
- Control Plane (Master Node) → the brain.
- Worker Nodes → the machines that run apps.
Purpose: Provides a unified platform to run, scale, and manage containerized applications.
👉 Analogy: A cluster is like a company.
When you deploy Kubernetes, you get a Cluster.
# what is a Node(Minions/Server)?
A Node in Kubernetes is a worker machine (physical server or virtual machine) where your application workloads (Pods) run.
Each node is part of a cluster.
- Nodes are managed by the Control Plane.
- A cluster can have many nodes to handle scaling and resilience.
- Is the smallest unit of computing hardware in Kubernetes.
- Encapsulates One or more application as containers.
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/f34c657a43af825148e3391d9b4e7b7e80309637/02-Kubernetes/Pods.png)
👉 Think of a Kubernetes cluster as a factory, and each Node is a worker in that factory.
# What is a Pods in Kubernetes?
A Pod is the smallest deployable unit in Kubernetes.
- It runs one or more containers together with shared network and storage.
- Kubernetes creates, scales, and heals Pods automatically.
- Are assigned a unique IP address(Private)
- Are ephemeral by nature
- Are assigned a new ip on recreation.
# The differences between Cluster, Node, and Pod in Kubernetes (K8s).
| Concept     | What it is                      | Contains                    | Purpose                     | Analogy   |
| ----------- | ------------------------------- | --------------------------- | --------------------------- | --------- |
| **Cluster** | Whole Kubernetes system         | Control plane + many nodes  | Manage and orchestrate apps | City      |
| **Node**    | A single machine in the cluster | Pods (via Kubelet, runtime) | Provides resources for apps | Building  |
| **Pod**     | Smallest deployable unit        | One or more containers      | Runs the actual app         | Apartment |
# Component Architecture Diagram / Kubernetes Architecture Diagram
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/3438d52eb840d4268dd51040a79bb9e40cfc3ca8/02-Kubernetes/Components%20k8s.png)
Here’s a diagram of the Kubernetes architecture showing:
- Control Plane (API Server, etcd, Scheduler, Controller Manager).
- Worker Nodes (Kubelet, Kube-Proxy, Container Runtime).
- Pods (running apps).
