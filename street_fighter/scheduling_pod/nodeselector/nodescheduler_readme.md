### How to create the labels on a node
```Actionscript
kubectl label node <node_name> <label_name>=<label_value>
```

### If you want to labeling the nodes by a YAML file then cmd will be
```Actionscript
kubectl apply -f node-label.yaml --force --grace-period 0
```

### How to remove a label from a node
```Actionscript
kubectl label node <node_name> <label_name>=<label_value>-
```

