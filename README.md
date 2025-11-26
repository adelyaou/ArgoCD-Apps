# ArgoCD-Apps
Repository for ArgoCD-managed Kubernetes deployments, including Application and AppProject manifests supporting automated GitOps workflows.

This repository contains ArgoCD Application and AppProject simple manifests used to
deploy the Employee App into Kubernetes environments following the GitOps model.

ArgoCD continuously watches this repository and synchronizes the desired state to
the cluster when updates are committed.

---

## Repository Structure

ARGO-INSTALL/
│
├── applications-dev.yaml # ArgoCD Application for Development environment
├── applications-stag.yaml # ArgoCD Application for Staging environment
├── applications-prod.yaml # ArgoCD Application for Production environment
└── project.yaml # ArgoCD AppProject defining access control rules

## How to Apply the Manifests Manually

> Make sure you are connected to the correct Kubernetes context.

### Create AppProject:
```bash
kubectl apply -f project.yaml -n argocd
