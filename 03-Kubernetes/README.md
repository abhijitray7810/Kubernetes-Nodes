# Master Components
The Master Components (Control Plane) in Kubernetes are:
- API Server 🛠
Entry point for all requests (kubectl, API calls).
Exposes Kubernetes API.

- etcd 📒
Distributed key-value store.
Holds the cluster state (nodes, pods, configs).

- Scheduler 📅
Assigns Pods to Nodes based on resources and rules.

- Controller Manager ⚙️
Runs controllers that ensure the desired state = actual state.
Examples: Node Controller, ReplicaSet Controller.

- Cloud Controller Manager ☁️ (optional)
Connects Kubernetes with cloud provider APIs (AWS, GCP, Azure).
![Image Alt](https://github.com/abhijitray7810/Kubernetes-Notes/blob/0cef167ccd1a7f700aea16ae310920beea7320f3/03-Kubernetes/Master-Com.png)
# Worker Node Components in Kubernetes
🏢 A Worker Node is where applications (Pods) actually run. Each node has these key components:
1. Kubelet
  - What it does:
       - An agent running on each node.
       - Talks to the Control Plane (API Server).
       - Ensures containers inside Pods are running as expected.

  - Analogy: The Team Leader on the ground.
       - Takes instructions from management (Control Plane).
       - Makes sure employees (containers) are doing their jobs.
2. Kube-Proxy
- What it does:

   - Manages network traffic inside the node.
   - Forwards requests to the right Pod.
   - Provides load balancing between Pods.

-Analogy:
   - The Office Receptionist / Switchboard Operator.
   - Directs phone calls (network requests) to the correct employee (Pod).
3. Container Runtime
- What it does:
  - The actual software that runs containers (Docker, containerd, CRI-O, etc.).
- Analogy:
  - The Work Desk & Tools employees use.
  - Without a desk/tools (runtime), employees (containers) can’t work.
4. Pods
- What it does:
    - The smallest deployable unit in Kubernetes.
    - Wraps one or more containers that work together.

- Analogy:
    - The Employees themselves.
    - Each Pod = one worker (or a small team of workers) doing the actual job.
