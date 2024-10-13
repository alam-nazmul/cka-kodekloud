### How to create namespace on your cluster
```Actionscript
kubectl create namespace <namespace_name>
```

### How to delete namespace on your cluster
```Actionscript
kubectl delete namespace <namespace_name>
```

### How to show details of a namespace on your cluster
```Actionscript
kubectl describe namespace <namespace_name>
```

### To create a namespace by a YAML file
```Actionscript
kubectl create -f namespace.yaml
```

### To delete a namespace by a YAML file
```Actionscript
kubectl delete -f namespace.yaml
```

### To update a namespace by a YAML file
```Actionscript
kubectl apply -f namespace.yaml
```