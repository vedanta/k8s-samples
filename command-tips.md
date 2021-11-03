- label the worker nodes:   
`kubectl label node k8s-worker2 node-role.kubernetes.io/worker=worker`
- use JSONPath to query nodes - example - find OS in each node -  
`kubectl get nodes -o jsonpath='{.items[*].status.nodeInfo.osImage}'`
