# 3-Cluster

This application will deploy Karmada propagation policies on our main cluster, which will install everything we need to bootstrap our cluster. For the purposes of this demo, those things are:

- ExternalDNS
- A secret for ExternalDNS so the deployment can access our Cloudflare account
- NGINX Ingress controller for routing
