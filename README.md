# argocd-cmp-trigger

Placeholder git trigger repo for ArgoCD v3.2.0 Config Management Plugin sidecar.

ArgoCD v3.2.0 plugin sources still perform `git clone` even when the actual
manifests come from the in-cluster `argocd/alephant-infra` ConfigMap. This
repo provides the required cloneable `source.repoURL`; its content is NOT
applied — only the commit SHA drives manifest cache versioning.

Bump: `echo "$(date -u +%s)" > trigger.txt && git commit -am bump`
