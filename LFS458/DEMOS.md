LFS458 - https://training.linuxfoundation.org/training/kubernetes-administration/

# TODO
- Look at nolej.io
- go through my SLIDES_LFS458 to add features into demos here
- prune slides - or grey them out ...

# BEFORE
- create a dumbed-down Google micro-services demo
- few deploy/services initially
- remove less basic features (probes, securityContext, serviceAccount)

# Introduction - Linux Foundation
# MYMODULE: Containers (in case)
=> reduce/minimize slides

# MYMODULE: Kubernetes Introduction
=> reduce/minimize slides

# MYMODULE: Kubernetes 101
=> demo basics
- demo Pods, Deployments, Services, YAML (dry-run, create/apply, get -o yaml)
- Google Microservices demo as is
  
# Installation and Configuration - Getting Started With Kubernetes
=> demo install ?
- scripted install with pauses
- manual steps: kubeadm init, kubeadm join (lazy way)

# Kubernetes Architecture - Kubernetes Architecture
=> demo etdctl + upgrade
- etcdctl functions + backup ( create resource, then demo restore?)
- scripted upgrade with pauses

# APIs and Access - API Access
=> demo API access (curl, hierarchy)
- show API hierarchy, api-resources
- show curl example (!), kubectl proxy
- show kubectl --raw ... (kubectl get -v 10 |& grep curl)

# API Objects - API Objects
=> demo resource types
- demo deployment/rs, daemonset, sts, job/cronjob
  => integrate into Google Microservices demo ?
    - daemonset to do what ? collect logs ? 
    - sts: is there a DB ? (or add a DB)
    - job: analyse transactions
    - cronjob: check consistency

# Managing State With Deployments - Deployment Overview
=> demonstrate rolling update
  - demo within Google micro-services ??
  - or existing demo ...
    show with/without probes

# Volumes and Data - Volumes Overview
=> demonstrate volumes, cm, secrets
  - demo within Google micro-services ??
      - demo emptyDir with existing ?? : container restart, multiple containers/shared vol, ro-filesystem
      - demo nfs-ext-subdir dynamic ?? (in G-mservices or not)
      - configmaps (+ upgrades + stakater?)
      - secrets for transaction info (+ etcd non encrypted)
  - python etcdctl script ?

# Services - Overview
=> demonstrate services
  - Google micro-services
    - clusterIP intern => iptables
      demo DNS
      could demo without selector
    - NodePort   => accessible on Node IP
      could demo internal/externalTrafficPolicy
      could demo headless (for STS)
    - LoadBalancer => could demo with MetalLB or kube-vip
    - ExternalName
      ??

# Helm - Overview
=> demonstrate helm
  - package installation
  - package creation for Google micro-services demo

# Ingress - Overview
=> demonstrate ingress
  - provide host-base, path-based routes to Google micro-services demo to different backend services
  - add some service-less rules => error
  - add some endpoint-less rules => error
=> demonstrate servicemesh
  - linkerd-viz
  - features?
  - multi-cluster?

# Scheduling - Overview
=> demonstrate scheduling
  - nodeSelector
  - nodeAffinity
  - podAffinity/AntiAffinity

# Logging and Troubleshooting - Overview
=> demonstrate failing scenarios
  - use k8scenario
  - use my examples => develop
  - use Google micro-services ...

# Custom Resource Definition - Overview
=> demonstrate CRD for Google micro-services
  - extend the model ...

# Security - Overview
=> demonstrate security for Google micro-services ...
  - look at security context: add capabilities? roFS, user?
  - add RBAC
  - add policies (VAP/CEL)
  - add network policies ==> update slides for Google micro-services ?

# High Availability - Overview
=> demonstrate HA & etcdctl leader
  - but how to know who is scheduler leader?

____ TODO ______________________________________________________________

# Introduction - Linux Foundation
- Linux Foundation Training
- Linux Foundation Certifications
- Linux Foundation Digital Badges
- Laboratory Exercises, Solutions and Resources
- Things Change in Linux and Open Source Projects
- E-Learning Course: LFS258
- Platform Details Basics of Kubernetes - Define Kubernetes
- Cluster Structure
- Adoption
- Project Governance and CNCF
- Labs

# Installation and Configuration - Getting Started With Kubernetes
- Minikube
- kubeadm
- More Installation Tools
- Labs

# Kubernetes Architecture - Kubernetes Architecture
- Networking
- Other Cluster Systems
- Labs

# APIs and Access - API Access
- Annotations
- Working with A Simple Pod
- kubectl and API
- Swagger and OpenAPI
- Labs

# API Objects - API Objects
- The v1 Group
- API Resources
- RBAC APIs
- Labs

# Managing State With Deployments - Deployment Overview
- Managing Deployment States
- Deployments and Replica Sets
- DaemonSets
- Labels
- Labs

# Volumes and Data - Volumes Overview
- Volumes
- Persistent Volumes
- Rook
- Passing Data To Pods
- ConfigMaps
- Labs

# Services - Overview
- Accessing Services
- DNS
- Labs

# Helm - Overview
- Helm
- Using Helm
- Labs

# Ingress - Overview
- Ingress Controller
- Ingress Rules
- Service Mesh
- Labs

# Scheduling - Overview
- Scheduler Settings
- Pod Specification
- Affinity Rules
- Taints and Tolerations
- Labs

# Logging and Troubleshooting - Overview
- Troubleshooting Flow
- Basic Start Sequence
- Monitoring
- Plugins
- Logging
- Troubleshooting Resources
- Labs

# Custom Resource Definition - Overview
- Custom Resource Definitions
- Aggregated APIs
- Labs

# Security - Overview
- Accessing the API
- Authentication and Authorization
- Admission Controller
- Pod Policies
- Network Policies
- Labs

# High Availability - Overview
- Stacked Database
- External Database
- Labs

