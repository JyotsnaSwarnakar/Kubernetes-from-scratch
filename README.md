!!!! KUBERNETES ARCHITECTURE !!!

### Worker Node/Data Plane

1. The k8s architecture is divided into two major parts that is **Master node/Control Plane & Worker Node/Data Plane**
2. The **Worker node** consists of 3 components that is (**Kubelet,Kubeproxy and container runtime)**
3. **Kubelet** ensures the pod is always running and if in case the pod is not running it informs to **API server** present in master node. **Kubelet** is responsible for creating the pods.
4. **Kubeproxy** ensures of managing the network , assigning IP address and providing load balancing capacity to the pod
5. The **container runtime** provides a container interface to k8s
6. Data Plane is responsible for running the application

### Master Node/Control Plane

1. The **master node/control plane** consists of **5 components** that is **(API server, Scheduler, etcd, Controller manager, Cloud controller manager)**
2. The **API server** is the heart of Kubernetes, it exposes the Kubernetes API server and every request is received by this API server
3. **Scheduler** selects the node for the pod and schedules it on basis of  different factors
4. **etcd** is a key value store that stores the cluster data
5. **Controller manager** manages the Kubernetes inbuilt controllers like replica set
6. The **Cloud Controller manager** let us link the k8s cluster to the specific cloud API. It only runs the controllers specific to the cloud provider. If Kubernetes is running on-premise cluster or for learning purpose in PC then it will not have cloud controller manager
