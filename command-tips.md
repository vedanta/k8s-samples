<<<<<<< HEAD
- label the worker nodes  
=======
- label the worker nodes:   
>>>>>>> e99d94bb522389eefe2f67702f1c68002f7eff8c
`kubectl label node k8s-worker2 node-role.kubernetes.io/worker=worker`
- use JSONPath to query nodes - example - find OS in each node -  
`kubectl get nodes -o jsonpath='{.items[*].status.nodeInfo.osImage}'`
