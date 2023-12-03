# 1-Crossplane

The applications in this folder deploy:

- The official Karmada chart, as a control-plane
- The official Crossplane chart
- The crossplane-providers chart within this repository
  - The GCP provider family
  - GKE container provider
  - GCP ProviderConfig with authentication details
  - The AWS provider family
  - EKS cluster provider
  - AWS ProviderConfig with authentication details

## Requirements

- Your argoProject allows access to the Helm repositories deployed from this folder
- A secret called "" with a key called "" in the crossplane-system namespace for the GCP ProviderConfig
- A secret called "" with a key called "" in the crossplane-system namespace for the AWS ProviderConfig
