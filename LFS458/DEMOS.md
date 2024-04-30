LFS458 - https://training.linuxfoundation.org/training/kubernetes-administration/

# BEFORE

### INTERACTION
- update dashboard, interactive idea notes - gotchas on labs
- dropbox sharelink ~/Dropbox/Shares/Public/2024-May-07_QA_Oracle_FS458/
  https://www.dropbox.com/scl/fo/w1ykd9812xtkbdf6ew0oe/AGDH28-JzrQS32MFLxdj2AI?rlkey=464dv4r8wosvg8y4iwxgp8i19&dl=0
- Look at nolej.io, Kahoot!
- create k8scenario scenarios / INSERT scenarios into peoples machines after labs complete

### SLIDES
- go through my SLIDES_LFS458 to add features into demos here
- prune slides - or grey them out ...
- Check official slides
- Check APPENDICES-WM pdf

### DEMOS
- create a dumbed-down Google micro-services demo
- few deploy/services initially
- remove less basic features (probes, securityContext, serviceAccount)

### LABS
- rerun scripts/DIFF_LFS458.sh => differences

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
- STRETCH: when finished lab, tell them to run scenario "lfs458-3"

# Kubernetes Architecture - Kubernetes Architecture
=> demo etdctl + upgrade
- etcdctl functions + backup ( create resource, then demo restore?)
- scripted upgrade with pauses
- STRETCH: when finished lab, tell them to run scenario "lfs458-4"

# APIs and Access - API Access
=> demo API access (curl, hierarchy)
- show API hierarchy, api-resources
- show curl example (!), kubectl proxy
- show kubectl --raw ... (kubectl get -v 10 |& grep curl)
- STRETCH: when finished lab, tell them to run scenario "lfs458-5"

# API Objects - API Objects
=> demo resource types
- demo deployment/rs, daemonset, sts, job/cronjob
  => integrate into Google Microservices demo ?
    - daemonset to do what ? collect logs ? 
    - sts: is there a DB ? (or add a DB)
    - job: analyse transactions
    - cronjob: check consistency
- STRETCH: when finished lab, tell them to run scenario "lfs458-6"

# Managing State With Deployments - Deployment Overview
=> demonstrate rolling update
  - demo within Google micro-services ??
  - or existing demo ...
    show with/without probes
- STRETCH: when finished lab, tell them to run scenario "lfs458-7"

# Volumes and Data - Volumes Overview
=> demonstrate volumes, cm, secrets
  - demo within Google micro-services ??
      - demo emptyDir with existing ?? : container restart, multiple containers/shared vol, ro-filesystem
      - demo nfs-ext-subdir dynamic ?? (in G-mservices or not)
      - configmaps (+ upgrades + stakater?)
      - secrets for transaction info (+ etcd non encrypted)
  - python etcdctl script ?
- STRETCH: when finished lab, tell them to run scenario "lfs458-8"

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
- STRETCH: when finished lab, tell them to run scenario "lfs458-9"

# Helm - Overview
=> demonstrate helm
  - package installation
  - package creation for Google micro-services demo
- STRETCH: when finished lab, tell them to run scenario "lfs458-10"

# Ingress - Overview
=> demonstrate ingress
  - provide host-base, path-based routes to Google micro-services demo to different backend services
  - add some service-less rules => error
  - add some endpoint-less rules => error
=> demonstrate servicemesh
  - linkerd-viz
  - features?
  - multi-cluster?
- STRETCH: when finished lab, tell them to run scenario "lfs458-11"

# Scheduling - Overview
=> demonstrate scheduling
  - nodeSelector
  - nodeAffinity
  - podAffinity/AntiAffinity
- STRETCH: when finished lab, tell them to run scenario "lfs458-12"

# Logging and Troubleshooting - Overview
=> demonstrate failing scenarios
  - use k8scenario
  - use my examples => develop
  - use Google micro-services ...
- STRETCH: when finished lab, tell them to run scenario "lfs458-13"

# Custom Resource Definition - Overview
=> demonstrate CRD for Google micro-services
  - extend the model ...
- STRETCH: when finished lab, tell them to run scenario "lfs458-14"

# Security - Overview
=> demonstrate security for Google micro-services ...
  - look at security context: add capabilities? roFS, user?
  - add RBAC
  - add policies (VAP/CEL)
  - add network policies ==> update slides for Google micro-services ?
- STRETCH: when finished lab, tell them to run scenario "lfs458-15"

# High Availability - Overview
=> demonstrate HA & etcdctl leader
  - but how to know who is scheduler leader?
- STRETCH: when finished lab, tell them to run scenario "lfs458-16"

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

