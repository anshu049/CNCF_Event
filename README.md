# Deploy metrics
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```
# Create namespace for App and Locust
```
kubectl create ns App
```
```
kubectl create ns Locust
```

# Deploy App and create HPA
```
kubectl apply -f app.yaml
```
```
kubectl autoscale deployment nodeapp --cpu-percent=30 --min=1 --max=10
```

# Deploy Locust and create HPA
```
kubect apply -f locust.yaml
```
```
kubectl autoscale deployment locust-worker --cpu-percent=70 --min=1 --max=10
```
