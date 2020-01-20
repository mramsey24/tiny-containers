# Blinkt LED setup
Based on https://github.com/apprenda/blinkt-k8s-controller

1. Clone the blinkt-k8s-controller project to your local machine

2. Create the the DaemonSet with proper permissions
```bash 
kubectl create -f kubernetes/blinkt-k8s-controller-rbac.yaml
```

3. Create the DaemonSet using the included Resource Descriptor:
```bash
kubectl create -f kubernetes/blinkt-k8s-controller-ds.yaml
```

4. Label pods with ```blinkt: show```that you want to show up in the Blinkt LED strip

