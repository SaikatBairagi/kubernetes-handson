Some commands of POD-

### to create a POD-

```bash
kubectl apply -f <<file_name>>```

### to delete pod - 

```bash 
kubectl delete -f <<file_name>>```

### to check the pod details-

```bash
kubectl describe pod```


Pod and Container status:

Pod
│
├── Pod Phase
│   ├── Pending
│   ├── Running
│   ├── Succeeded
│   ├── Failed
│   └── Unknown
│
└── Container State
    ├── Waiting
    │    └── Reason
    │         ├── ContainerCreating
    │         ├── ErrImagePull
    │         ├── ImagePullBackOff
    │         ├── CrashLoopBackOff
    │         └── CreateContainerConfigError
    │
    ├── Running
    │
    └── Terminated
         └── Reason
              ├── Completed
              ├── Error
              └── OOMKilled

Labels:
we add labels to the pod to identify the POD of select a particilar pod with the Label name.
```bash
kubectl get pods --show-labels```

```bash
kubectl get pods -l dept=finance```

## Port Forwarding
see the file 03-port-forwarding-pod.yaml for port exposing
This is not the proper way but this way we can create a tunnel
```bash
kubectl port-forward myapp 8080:80```
this will create the tunnel