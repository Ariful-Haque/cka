
# Master node 
1. Kube-apiserver
2. Controller manager 
    1. Node controller: node monitor period 5 seconds, node monitor grace period 40 seconds, 
    pod eviction timeout 5m 
    2. Replication controller 
    3. Deployment controller
    4. Service-account controller
    5. Replicaset controller 
    
    and many more. How do you see them and where are they located? They are all packaged into a single process called **'Kube-controller-manager'**.
    
    Where can you see the 'kube-controller-manager' pod defination file? /etc/kubernetes/manifests/
3. Etcd 
4. Kube-scheduler

    Scheduler only responsible for deciding which pod goes to which node. It actually does not place the pod on the nodes. That is the job of the kubelet. 


# Worker Nodes

1. kubelet

    **kubeadm does not deploy kubelet**. You have to install it manually on your worker nodes. 
2. kube-proxy : *helps enabling communication between services* 

    kube-proxy is a process that runs on each node in the kubernetes cluster. Its job is to look for new services and everytime a new service is created, it creates the appropriate rules on each node to forward traffic to those services to the backend pods.  
    
3. container runtime


