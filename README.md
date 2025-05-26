## Day 2 – Kubernetes Architecture, Pod Scheduling, Node Affinity

###  Applied Deployment YAML

File: `deployment.yaml` contains:
- Pod spec for Day 1 Node app
- Resource limits and requests
- Node Affinity and Tolerations rules

###  Verification

After applying:

```bash
kubectl apply -f deployment.yaml
kubectl get pods -o wide

 Questions
1. Why do we set requests and limits for CPU/memory in a production-grade product?
    Requests specify the minimum resources a container requires so Kubernetes can schedule it on a suitable node.
    Limits define the maximum resources a container can consume, preventing it from starving other workloads.
    This ensures fair resource allocation, avoids resource contention, and maintains cluster stability and performance.
2. When would a product team apply node affinity in Kubernetes?
    To control pod placement on nodes with specific labels or characteristics (e.g., hardware type, location).
    To optimize performance by scheduling workloads on appropriate nodes.
    For workload isolation or compliance by separating workloads across different nodes.
    To utilize specific resources like GPUs or SSDs.
    Node affinity provides fine-grained scheduling control to improve reliability and efficiency.
