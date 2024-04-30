
LFD459 - https://training.linuxfoundation.org/training/kubernetes-for-app-developers/

# BEFORE:
- Look at nolej.io
- Post LFS458, put demo ideas here
- Review my SLIDES_LFD459, update demo ideas
- Prune slides

# Introduction - Objectives

# Build - Container Options

# Design - Traditional Applications: Considerations

# Deployment Configuration - Volumes Overview

# Understanding Security - Security Overview

# Exposing Applications - Service Types

# Application Troubleshooting

____ TODO ______________________________________________________________

# Introduction - Objectives
- Who You Are
- The Linux Foundation
- Linux Foundation Training
- Certification Programs and Digital Badging
- Platform Details Kubernetes Architecture - What Is Kubernetes?
- Components of Kubernetes
- Challenges
- The Borg Heritage
- Kubernetes Architecture
- Terminology
- Control Plane Node
- Worker Nodes
- Pods
- Services
- Operators
- Single IP per Pod
- Networking Setup
- CNI Network Configuration File
- Pod-to-Pod Communication
- Cloud Native Computing Foundation
- Resource Recommendations
- Labs

# Build - Container Options
- Containerizing an Application
- Creating the Dockerfile
- Hosting a Local Repository
- Creating a Deployment
- Running Commands in a Container
- Multi-Container Pod
- readinessProbe
- livenessProbe
- startupProbe
- Testing
- Helm
- Labs

# Design - Traditional Applications: Considerations
- Decoupled Resources
- Transience
- Flexible Framework
- Managing Resource Usage
- Using Label Selectors
- Multi-Container Pods
- Sidecar Container
- Adapter Container
- Ambassador
- initContainer
- Custom Resource Definitions
- Points to Ponder
- Jobs
- Labs

# Deployment Configuration - Volumes Overview
- Introducing Volumes
- Volume Spec
- Volume Types
- Shared Volume Example
- Persistent Volumes and Claims
- Persistent Volume
- Persistent Volume Claim
- Dynamic Provisioning
- Secrets
- Using Secrets via Environment Variables
- Mounting Secrets as Volumes
- Portable Data with ConfigMaps
- Using ConfigMaps
- Deployment Configuration Status
- Scaling and Rolling Updates
- Deployment Rollbacks
- Labs

# Understanding Security - Security Overview
- Accessing the API
- Authentication
- Authorization
- RBAC
- RBAC Process Overview
- Admission Controller
- Security Contexts
- Pod Security Policies
- Pod Security Standards
- Network Security Policies
- Network Security Policy Example
- Default Policy Example
- Labs

# Exposing Applications - Service Types
- Services Diagram
- Service Update Pattern
- Accessing an Application with a Service
- Service without a Selector
- ClusterIP
- NodePort
- LoadBalancer
- ExternalName
- Ingress Resource
- Ingress Controller
- Service Mesh
- Labs

# Application Troubleshooting
- Troubleshooting Overview
- Basic Troubleshooting Steps
- Ongoing (Constant) Change
- Basic Troubleshooting Flow: Pods
- Basic Troubleshooting Flow: Node and Security
- Basic Troubleshooting Flow: Agents
- Monitoring
- Logging Tools
- Monitoring Applications
- System and Agent Logs
- Conformance Testing
- More Resource
- Labs

