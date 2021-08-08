# Kubernetes
Haverford Coding Club's Kubernetes manifests!

## Secrets
Create secrets via `kubectl create secret`.
```
kubectl create secret generic example-secret-env -n example \
    --from-literal=BEST_ANIMAL=axolotl \
    --from-literal=DATABASE_URL=postgres.example.svc.cluster.local:5432/example
```
