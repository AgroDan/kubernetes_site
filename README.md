# Kubernetes Manifests for Production

These are all the manifests I've created to allow my site to run within a kubernetes cluster on Linode. The flow of requests goes like so:

```
Internet --> LB with Traefik Ingress --> Site SVC --> Site Deployment
```

Certificates are auto-generated using [Cert-Manager](https://cert-manager.io) and [LetsEncrypt](https://letsencrypt.org). DNS Manipulation is automatically performed with [External-DNS](https://github.com/kubernetes-sigs/external-dns).
