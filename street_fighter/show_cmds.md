### To show the node status
```Actionscript
kubectl get nodes -o wide
```
  
  ### To show the pod status in default namespace
```
kubectl get pods -o wide
```
  
  ### To show the pod status in default namespace
```
kubectl get pods -o wide -n <namespace_name>
```
  
  ### To show the pod status in all namespace
```
kubectl get pods -o wide -A
```
  #### _All modules will be running stage if we put the module configuration on "/etc/modules-load.d"_
  
  ### How to get output by YAML file
```Actionscript
kubectl get pods -o yaml
```
  
  ### How to get output by JSON file
```Actionscript
kubectl get pods -o json
```
  
  ### How to get namespace information from the cluster
```Actionscript
kubectl get namespaces
```
  

  ### To delete all Pods
```Actionscript
kubectl delete pods --all
```
  
  ### To show the details information of nodes
```Actionscript
kubectl describe node <node_name>
```
  
  ### To show the k8s objects
```Actionscript
kubectl api-resources
```

