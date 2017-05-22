# On HPC cloud

Created vm from ubuntu16 app + 40Gb disk for docker.
Formatted /dev/vdb/ with single ext4 partition
Mounted /dev/db1 as /var/lib/docker
Started docker server

# Setup a single node kubernetes with

https://kubernetes.io/docs/getting-started-guides/kubeadm/
```
kubeadm init
kubectl --kubeconfig /etc/kubernetes/admin.conf proxy
```
# Mybinder

Followed http://docs.mybinder.org/custom-deployments
Changes:
```
sudo npm install -g binder-control
binder-control start-all

prompt: Would you like to stop the Kubernetes cluster?:  (yes) no
prompt: Would you like to stop the local Kubernetes deployment (local testing only)?:  (no) yes
prompt: Would you like to stop the database service?:  (yes) 
prompt: Would you like to stop the logging service?:  (yes) 
```

Build fails, might need a pod.


