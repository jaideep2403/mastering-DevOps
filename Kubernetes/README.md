# Kubernetes

Basically, why Kubernetes?
The Docker had many problems in day-to-day life in the industry,
Four main problems of the docker that are,

•	Single host

•	Auto scaling

•	Auto Healing

•	Docker is not for Enterprise Nature

So, if we wonder how all these problems are solved, here comes the Kubernetes.
Kubernetes is an Open-source platform for managing containerized applications. It automates the deployment, scaling and management of these applications. It is portable, extensible and declarative, and has a large and growing ecosystem of services and tools. 
So, Kubernetes came up with a solution for all those docker problems.

**How did it solve the problem of single host?**

By default, Kubernetes is a cluster, cluster is group of nodes. 

So, Kubernetes on production is installed in terms of Master node architecture just like Jenkins. 
If there are 100s of containers running and if one of the container lifecycles is affecting any of the containers, what Kubernetes does is, it just picks up the affected container and puts into the other node to resume its capability without any intervention.

**How does it solve Auto scaling?**

Kubernetes has something called replica set.

So, if a container is experiencing a huge load on a certain time (the no of users hitting the application n increases). We have replicaset.yaml file and increase the replicas and bring up the new containers manually. Kubernetes also supports HPA (Horizontal pod Auto scaler) using which we can increase the no of containers whenever we experience the load.

**How does it solve Auto healing?**

Kubernetes controls and fix the damage.

If one of the containers goes down, using the Auto healing feature Kubernetes will spin up a new container before the old one dies.
We have something called API server in k8s, this API servers receives the signal of container going down, immediately the k8s rolls out a new container before the old one goes down. The user doesn’t even experience of any shutdown of the application.

**How will it support Enterprise Nature?**

People at Google Built Enterprise level container orchestration platform called Kubernetes.

Since Docker is not of enterprise nature (Load balancer support, firewall support, auto healing, auto scaling, Api gateways, blacklisting ips etc.). so, it is never used in Production platform. Kubernetes is aiming to solve these problems.