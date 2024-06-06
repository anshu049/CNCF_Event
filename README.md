```
kubectl autoscale deployment nodeapp --cpu-percent=20 --min=1 --max=10
```

```
kubectl autoscale deployment locust-worker --cpu-percent=80 --min=1 --max=2
```
