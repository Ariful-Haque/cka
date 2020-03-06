
# Master node 
1. Kube-apiserver
2. Controller manager 
    1. Node controller: node monitor period 5 seconds, node monitor grace period 40 seconds, 
    pod eviction timeout 5m 
    2. Replication controller 
    3. Deployment controller
    4. Service-account controller
    5. Replicaset controller 
    
    and many more. How do you see and where are they located? They are all packaged into a single process called **'Kube-controller-manager'** 
3. Etcd 
4. Kube-scheduler


# Worker Nodes
1. kubelet
2. kube-proxy : *helps enabling communication between services* 
3. container runtime


