# Deploy metrics
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

# Create HPA for app
```
kubectl autoscale deployment nodeapp --cpu-percent=20 --min=1 --max=10
```
