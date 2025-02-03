# swip-deployment
ArgoCD configurations, Helm values, Kubernetes manifests

swip-deployment/
│── manifests/                   # Contains all ArgoCD applications & K8s manifests
│   │── argo-cd.yaml              # ArgoCD bootstrap application
│   │── middleware.yaml           # Deploys Kafka, PostgreSQL, MongoDB, Keycloak
│   │── backend.yaml              # Deploys SWIP backend
│   │── frontend.yaml             # Deploys SWIP frontend
│   │── keycloak.yaml             # Deploys Keycloak realm
│   │── secrets.yaml              # Kubernetes secrets (GitHub Token, Database credentials)
│── helm/                         # Helm values for different environments
│   │── middleware-values.yaml    # Helm values for Kafka, PostgreSQL, MongoDB
│   │── backend-values.yaml       # Helm values for backend
│   │── frontend-values.yaml      # Helm values for frontend
│── ci-cd/                        # CI/CD Configuration
│   │── github-webhook.yaml       # Configures GitHub webhook for auto-sync
│   │── argocd-autosync.yaml      # Configures ArgoCD to auto-sync on changes
│── README.md                     # Documentation
