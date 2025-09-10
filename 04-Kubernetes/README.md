# Kubernetes Main Components
  # Service:
    - Is responsible for enabling network access to a set of Pods
    - Is assigned an IP address("Cluster IP"), Which the service proxies use.
    - Provides load balancing and good abstaction for loose coupling within and outside the cluster.
    # External: Service is created to allow external users to access the containerized application        in pods.
    # Internal: Service restrict the communication within the cluster.
    - There are three type of Service types are ClusterIP, NodePort & LoadBalancer.

  # ingress:
    - Is an API objects that allows access to your Kubernetes service from outside the cluster.
    - Is completely independent to your service.
    - Helps consolidate routing rules into one place.
    - Is typically used ina production enviroment to expose application to the internet.
    
    
