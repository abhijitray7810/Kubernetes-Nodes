# Kubernetes-Nodes(k8s)
# What is Kubernetes? 
Kubernetes (often abbreviated as K8s) is an open-source container orchestration platform. It’s used to automate the deployment, scaling, and management of containerized applications.
# Why do we need Kubernetes? / Why Use Kubernetes?
Kubernetes is needed because it solves the challenges of managing containerized applications at scale, automating complex tasks that would otherwise require significant manual effort or custom solutions. Containers (e.g., built with Docker) package applications for portability, but orchestrating them across multiple machines, ensuring reliability, scaling, and updates is where Kubernetes shines.
- Manual container management → Which container runs on which server.
- Scaling → How to handle traffic spikes (e.g., Black Friday).
- Resilience → What if a server crashes? Who restarts the containers.
- Load balancing → How to split traffic across multiple app instances.
- Deployment safety → How to roll out new versions without downtime.
- Portability: Run the same app consistently across different environments.
- Extensibility: Large ecosystem with tools for monitoring, security, and CI/CD integration.
# How Does Kubernetes Work? / How Kubernetes actually works.
- Kubernetes manages a cluster of machines (servers, physical or virtual).
- Some machines act as the Control Plane (the “brain”).
- Others are Worker Nodes (where your apps actually run).
- Master (Control Plane)
- Worker Nodes (Minions,server)
