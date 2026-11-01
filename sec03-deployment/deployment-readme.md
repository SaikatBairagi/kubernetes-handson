watch command-
```bash
watch -t -x kubectl get all```

If you change the Deployment spec it will create new replica set as
the specification change means there is some change in the container runtime.
If you change other thing lets say-
replicas: 4 and you change it to 2 it will not create a new replica set.

Rollout-
```bash
kubectl rollout history deploy```
