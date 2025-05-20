# Day 1 – Introduction to Docker & Kubernetes: Containerization Basics

##  Workshop Track
Pi-shaped Workshop – Docker & Kubernetes


## Objectives

- Create a simple Node.js REST API (`Hello, World!`) 
- Write a Dockerfile to containerize the app
- Build and tag a Docker image
- Run the container locally on port `8080`  
- Push the image to Docker Hub

## Core Concept Questions

### Why is Docker useful in building and deploying microservices?

Docker helps package each microservice with everything it needs to run, making it portable and consistent across environments. It speeds up development, testing, and deployment, and makes it easy to scale and manage services independently.

---

### What is the difference between a Docker image and a container?

A Docker image is like a template or snapshot of your app, including its code and dependencies.

A container is the actual running instance created from that image.

---

### How does Kubernetes complement Docker at scale?

KKubernetes is a powerful tool that automates how Docker containers are run and managed. It can:

Automatically start or stop containers as needed

Distribute traffic across containers

Recover failed containers

Perform updates without downtime
---

