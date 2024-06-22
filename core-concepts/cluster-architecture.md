High Level
----------
    
    Master Node - management of cluster
        - ETCD - key,value store. data[]
        - Schedulers - identifies right node to place a container(s).
        - Node controller - takes care of nodes
        - replication controller - ensures reqd. no of containers are running all time
        - kubeapi server - primary management component, orchestrates all ops within cluster
    container runtime(eg docker) - to be installed in all nodes
    Worker nodes - hosts apps as containers
        - kubelet - agent runs on all nodes and listens to kubeapi server
                    [kubeapi periodically fetches status from kubelet]
        - kube-proxy - communication bw worker nodes by this


        ![Architecture diagram](architrcture.svg)
