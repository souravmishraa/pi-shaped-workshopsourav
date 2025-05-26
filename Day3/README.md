# Kubernetes Networking Setup - Day 3

## Resources created

- Deployment (`my-app`) running Nginx pods
- Services:
  - ClusterIP (`my-app-clusterip`) — Internal-only access
  - NodePort (`my-app-nodeport`) — Access on node IP and port 30036
- Ingress (`my-app-ingress`) — Routes `/app` path on host `myapp.local` to the ClusterIP service

## Testing

- ClusterIP tested with `kubectl port-forward`
- NodePort accessible via `http://<NodeIP>:30036`
- Ingress accessible via `http://myapp.local/app` (requires ingress controller and host entry)

## Core Concept Questions

### 1. How would you expose an internal microservice (e.g., user-auth) differently than a public-facing frontend?

Internal microservices like `user-auth` are exposed via ClusterIP services, which are only accessible inside the cluster. This limits their exposure and improves security. Public-facing frontends are exposed using NodePort, LoadBalancer, or Ingress resources that allow external traffic access with appropriate routing and load balancing.

### 2. Why might a product use Ingress instead of directly exposing each microservice via LoadBalancer?

Ingress allows centralized routing, SSL termination, and path-based or host-based routing, reducing the number of external IPs and LoadBalancers needed. This saves cost and simplifies management. Directly exposing each microservice with LoadBalancer is inefficient and expensive because each service requires its own external IP and load balancer.

