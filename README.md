# Deploy metrics
```
kubectl apply -f metric.yaml
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

# Deploy Locust
```
kubens locust
```
```
kubectl apply -f locust.yaml
```
