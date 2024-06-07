# Deploy metrics
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

# Create HPA for app
```
kubectl autoscale deployment nodeapp --cpu-percent=30 --min=1 --max=10
```

# Create HPA for Locust
```
kubectl autoscale deployment locust-worker --cpu-percent=70 --min=1 --max=10
```
