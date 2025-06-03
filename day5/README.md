#Kubernetes Assignment - Real-world Use Case

# Setup
 Deployed a 2-tier application (frontend + backend) using raw YAML manifests.
 Applied resource limits and requests to control usage and ensure efficient scheduling.
 Configured liveness and readiness probes for both services to ensure reliability.
 Integrated HPA to auto-scale backend based on CPU utilization.

# Performance & Cost Considerations
 Used resource limits to avoid over-provisioning.
 Set up HPA to optimize pod count based on real usage – helps during peak traffic.
 Probes prevent routing to unhealthy pods, improving reliability.

# Core Questions:

**1. Why are liveness and readiness probes critical?**  
Liveness probes restart unhealthy containers, while readiness probes ensure only healthy pods receive traffic – both crucial for uptime and user experience.

**2. How does HPA help during spikes like flash sales?**  
HPA automatically increases pod count under load, maintaining performance without manual intervention – essential for unpredictable traffic in real-world apps.