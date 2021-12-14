# Cluster Setup Using kubeadm
* 3 Nodes Cluster - Ubuntu 18.04 (Bionic Beaver LTS) - Size: Medium
* kubeadm based install
## Steps
* Step 1 - Server Configurations - for controlplane and worker nodes setup hostname and /etc/hosts 
* Step 2 - Install CRI on every node of the cluster
* Step 3 - Install kubernetes packages on every node - kubelet, kubeadm, kubectl (using apt)
* Step 4 - Initiate the controlplane using kubeadm
* Step 5 - Setup kubeconfig - Acquire kubeconfig to interect with cluster
* Step 6 - Install network 
* Step 7 - Join nodes to the cluster, create token in controlplane and then run on each node
* Step 8 - Setup complete

# Cluster Upgrade Using kubeadm
* Start by upgrading the control plane node
* Once the control plane node is upgraded - upgrade the worker nodes one after another

## Steps 
### Controlplane Node
* Step 1 - drain the controlplane nodes ignore daemonsets 
* Step 2 - upgrade kubeadm - apt, --allow-change-held-packages , check for updated kubeadm package
* Step 3 - upgrade controlplane components - plan and then upgrade
* Step 4 - upgrade kubelet and kubectl 
* Step 5 - reload daemons - restart services (kubelet)
* Step 6 - uncordon controlplane node
### worker nodes
* Step 1 - drain the node
* Step 2 - upgrade kubeadm
* Step 3 - update the kubeadm files (kubeadm upgrade node)
* Step 4 - update kubelet and kubectl
* Step 5 - reload daemons - restart services (kubelet)
* Step 6 - uncordon node


