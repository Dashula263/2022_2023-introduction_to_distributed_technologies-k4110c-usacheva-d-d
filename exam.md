CNI or Container Network Interface. And as it becomes clear from its name, CNI stands for connecting, adding and deleting disconnecting containers to networks.
Mainly CNI is a framework or a plugin that can dynamically configure networking resources (network, IP-addresses, hosts). In other words, this plugin inserts a network interface into the container network namespace and make any necessary changes on the host.

There're different types of plugins of CNI. For example, flannel, calico and others. 
Calico, in its turn, provides a CNI plugin that can be used for integration with Kubernetes. Calico creates a flat layer-3 network and assigns a fully routable IP address to every pod.
To install Calico you can use yaml file which creates calico-node daemonset (pod that runs on all the nodes of the K8s cluster). So it installs just like any other pod:
kubectl apply -f <address to pod>/calico.yaml
    
	
	
