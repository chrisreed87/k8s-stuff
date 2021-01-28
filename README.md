# k8s-stuff

Helpful tools and software I've used with K8s

# Distros and Management

- [K3s](https://k3s.io)
- [kops](https://kops.sigs.k8s.io)
- [Rancher](https://github.com/rancher/rancher)
  - [Rancher Terraform Provider](https://registry.terraform.io/providers/rancher/rancher2/latest/docs)

# Command Line

- [K9s](https://k9scli.io)
- [Kubectx](https://ahmet.im/blog/kubectx/) & Kubens (included with kubectx install)
- Aliases

```
alias kgn="kubectl get node"
alias kgs="kubectl get svc"
alias kgd="kubectl get deploy"
alias kgp="kubectl get pod"
alias kgi="kubectl get ingress"
alias kns="kubens"
alias ktx="kubectx"
```

# Ingress

- [nginx-ingress](https://kubernetes.github.io/ingress-nginx/) - used in most K8s clusters
  - [app-root](https://kubernetes.github.io/ingress-nginx/examples/rewrite/#app-root) - if your applications root path is different than `/`
- [alb-ingress-controller](https://github.com/kubernetes-sigs/aws-load-balancer-controller) - use ALB's as ingress endpoints, super convenient

# Storage

- [longhorn](https://longhorn.io) - really easy to use persitent storage, replicates across nodes for backup
- [ebs csi driver](https://github.com/kubernetes-sigs/aws-ebs-csi-driver) - use ebs volumes for persistent storage

# Secrets

- [external-secrets](https://github.com/external-secrets/kubernetes-external-secrets) - uses aws ssm/secrets manager for generating kubernetes secrets

# Misc

- [cluster-autoscaler](https://github.com/kubernetes/autoscaler/tree/master/cluster-autoscaler)
- [dnsutils test](https://kubernetes.io/docs/tasks/administer-cluster/dns-debugging-resolution/)
- [rancher overlay test](https://rancher.com/docs/rancher/v2.x/en/troubleshooting/networking/#check-if-overlay-network-is-functioning-correctly)
- [service internal loadbalancer](https://kubernetes.io/docs/concepts/services-networking/service/#internal-load-balancer) - turn a service into a basic NLB
