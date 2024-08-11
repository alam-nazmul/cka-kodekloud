### For maintenance, first we have to move all pods from that node. Then un-schedule the node by
```
kubctl drain node-1
```

### After maintenance, we can schedule the node by
```
kubctl uncordon node-1
```

### Best way is un-schedule the node. Means no new pods can deploy this node. But existing PODs will remain same
```
kubctl cordon node-1
```