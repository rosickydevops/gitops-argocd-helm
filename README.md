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
├ argocd
│  ├ app-main
│  │  ├ dev
│  │  │  └ dev-main.yaml
│  │  └ prod
│  │     └ prod-main.yaml
│  │
│  └ chart-app
│     ├ dev
│     │  ├ Chart.yaml
│     │  ├ values.yaml
│     │  └ templates
│     │     └ values.yaml
│     │
│     └ prod
│        ├ Chart.yaml
│        ├ values.yaml
│        └ templates
│           └ values.yaml
│
├ chart
│  ├ templates
│  │  ├ deployment.yaml
│  │  ├ service.yaml
│  │  └ ingress.yaml
│  │
│  ├ values
│  │  ├ dev
│  │  │  └ values.yaml
│  │  └ prod
│  │     └ values.yaml
│  │
│  ├ Chart.yaml
│  └ values.yaml
│
└ README.md

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
