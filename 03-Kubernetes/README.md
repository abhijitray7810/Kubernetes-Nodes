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
