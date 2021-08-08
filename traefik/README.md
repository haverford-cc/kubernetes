# Traefik
This directory contains the Traefik manifests.

```
helm repo add traefik https://helm.traefik.io/traefik
helm repo update

helm install traefik traefik/traefik -f values.yaml -n kube-system
```

## Dashboard
The Traefik Dashboard can be port forwarded locally via:
```
kubectl port-forward -n kube-system $(kubectl get pods -n kube-system --selector "app.kubernetes.io/name=traefik" --output=name) 9000:9000
```
Visit http://127.0.0.1:9000/dashboard/.
