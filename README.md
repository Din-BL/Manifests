# Demo App Helm Chart

## Overview

This Helm chart defines the Kubernetes infrastructure for the Demo Application. It establishes a deployment with rolling updates, autoscaling capabilities, internal service routing, and secure external access.

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

---

*This chart encapsulates deployment patterns for a containerized application with appropriate networking, scaling, and security configurations.*
