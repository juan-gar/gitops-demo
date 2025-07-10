
# gitops-demo
=======
# GitOps Demo with ArgoCD, Helm, and Kustomize

This project demonstrates a GitOps workflow using ArgoCD to deploy a simple app to Kubernetes with separate staging and production environments.

## ✨ Tech Stack

- Kubernetes
- ArgoCD
- Helm (templating)
- Kustomize (overlays)
- External Secrets Operator
- cert-manager (optional)
- Prometheus/Grafana (optional)

## 🧩 Environments

- `staging`: Deploys a basic nginx app with v1.25
- `production`: Same app, isolated namespace

## 🚀 Quick Start

```bash
kubectl create ns argocd
kubectl apply -n argocd -f argocd/apps/demo-app-staging.yaml
kubectl apply -n argocd -f argocd/apps/demo-app-production.yaml
```

## 🔐 Secrets

Uses External Secrets Operator to pull from AWS Secrets Manager.

## 🧭 TODO

- [ ] Add Prometheus & Grafana monitoring
- [ ] Add cert-manager TLS support
- [ ] Add CI/CD GitHub Actions pipeline

