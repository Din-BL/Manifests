# Demo App Helm Chart

## Overview

This Helm chart defines the Kubernetes infrastructure for the Demo Application. It establishes a deployment with rolling updates, autoscaling capabilities, internal service routing, and secure external access.
The chart integrates with ArgoCD for automatic deployment and continuous delivery operations.

## Architecture Components

- **Deployment**: 2 replicas with 25% rolling update strategy
- **Autoscaling**: Scales between 2-3 replicas based on 80% CPU or 75% memory utilization
- **Networking**: ClusterIP service mapping port 80 to container port 3000
- **External Access**: NGINX Ingress for demoapp.com with TLS encryption
- **Container**: Private ECR repository with authentication

## Technical Design Considerations

- **High Availability**: Multiple replicas with controlled rolling updates
- **Security**: Private registry authentication, TLS encryption, and network isolation
- **Resource Efficiency**: Demand-based scaling with defined utilization thresholds
- **Performance**: Horizontal scaling architecture with efficient traffic routing
- **Continuous Delivery**: ArgoCD integration enables GitOps workflows with automatic synchronization between the Git repository and cluster state

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/4d86bbff-5319-4c9d-8c27-99b93b92014a" alt="Image 1" width="400"/>
</p>
