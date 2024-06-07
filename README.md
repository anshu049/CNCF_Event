# Deploy metrics
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```
# Create namespace for App and Locust
```
kubectl create ns app
```
```
kubectl create ns locust
```

# Deploy App and create HPA
```
kubens app
```
```
kubectl apply -f app.yaml
```
```
kubectl autoscale deployment nodeapp --cpu-percent=30 --min=1 --max=10
```

# Deploy Locust and create HPA
```
kubens locust
```
```
kubect apply -f locust.yaml
```
kubectl autoscale deployment locust-worker --cpu-percent=70 --min=1 --max=10
```
