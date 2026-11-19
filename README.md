# kubeadm-gitops-lab

Demo manifests for a GitOps exercise: Argo CD watches `apps/dev` and keeps the
`dev` namespace of a kubeadm cluster in sync with this repository.

- `apps/dev/namespace.yaml`: the `dev` namespace
- `apps/dev/webapp.yaml`: an NGINX page (ConfigMap + Deployment + Service)

Change `index.html` or `replicas`, push, and Argo CD applies it. A manual edit
in the cluster is reverted by self-heal.
