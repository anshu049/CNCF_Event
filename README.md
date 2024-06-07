# Create HPA for app
```
kubectl autoscale deployment nodeapp --cpu-percent=20 --min=1 --max=10
```
