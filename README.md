**GitOps Kubernetes Platform**

GitOps-based deployment platform using ArgoCD and Helm.

---

**Overview**

This project demonstrates automated Kubernetes deployments using GitOps practices.
Application configurations are stored in Git and synchronized to the cluster using ArgoCD.

---

**Technologies**

- Kubernetes
- ArgoCD
- Helm
- GitOps

---

**Architecture**

```
Developer
   │
   ▼
Git Repository
   │
   ▼
ArgoCD
   │
   ▼
Kubernetes Cluster
```
---

**Repository Structure**

```
gitops-argocd-helm
│
├ apps
│   └ nginx
│
├ argocd
│   └ application.yaml
│
├ environments
│   ├ dev
│   └ prod
```

---

**Deployment**

Install Helm chart:

  helm install nginx ./apps/nginx

ArgoCD will automatically synchronize the application with the cluster.

---

**Features**

- GitOps based deployments
- Helm templating for Kubernetes applications
- Automated cluster synchronization
