# What is Kubernetes
Kubernetes, often abbreviated as K8s, is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications
**Features**
* Container management
* Automated Scaling
* Self-Healing
* Declarative Configuration
* Service Discovery and Load balancing
  
**Master Node components**
* API server -
* Scheduler -
* Controller Manager -
* etcd Database -

  
**Pods** are the basic building blocks of any application running in Kubernetes
A Pod consists of one or more containers and a set of resources shared by those containers.


**Namespaces** provide a way to keep your objects organized within the cluster.

**configMap** is a kuberneters Object that stores configuration data in a key-value format.

**Multi-container pods** are simply pods with more than once container that all work together as single unit.

**Probes**- Allow you to customize how kubernetes determines the status of the your Containers

**Liveness probe** Indicates whether the container is running properly and governs when the cluster will automatically stop or restart the container

**Readiness probe**  The container is ready to service requests and governs whether requests will be forward to the pod

