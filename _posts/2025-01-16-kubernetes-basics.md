---
layout: post
title: "Kubernetes Fundamentals: From Zero to Hero"
date: 2025-01-16
categories: [devops, kubernetes]
tags: [kubernetes, k8s, containers, orchestration, devops]
image:
  path: /assets/img/posts/kubernetes-basics.png
  alt: Kubernetes Architecture
---

## ⚡ What is Kubernetes?

Kubernetes (K8s) is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.

## 🏗️ Architecture Overview

1. **Control Plane Components**
   - API Server
   - etcd
   - Scheduler
   - Controller Manager

2. **Node Components**
   - kubelet
   - kube-proxy
   - Container Runtime

## 🚀 Basic Concepts

### Pods
The smallest deployable units in Kubernetes.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx
    image: nginx:latest
    ports:
    - containerPort: 80
```

### Deployments
Manage the deployment and scaling of Pods.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:latest
```

## 🔧 Getting Started

1. Install kubectl
2. Set up minikube
3. Deploy your first application
4. Scale and manage workloads
