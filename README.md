# Multi-Cloud Demo

The repository contains demo setup for deploying:

- Minimal EKS and GKE clusters
- Karmada for application deployment
- Bootstrapping the clusters using Karmada, including:
  - Nginx ingress controller
  - ExternalDNS and updating Cloudflare entries
- Harbour on both clusters for an image registry
- CockroachDB with Multi-region replication
- Percona MongoDB with Multi-region replication

## Requirements

- A Kubernetes cluster (Of any kind)
- ArgoCD
  - Each individual step is provided as a helm chart and ArgoCD application to deploy that helm chart
  - You can deploy each stage as an app-of-apps
  - The steps can be applied manually using kubectl, there isn't much templating
- An AWS account, with either:
  - An IAM user with credentials exported as a secret
  - Correct IAM setup for service accounts to be assigned to pods with the correct permissions
- A GCP account with either:
  - A Service Account with credentials exported as a secret
  - Correct IAM setup for service accounts to be assigned to pods with the correct permissions
