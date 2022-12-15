<h1><b>Как работают CNI, типы CNI, особенности развертывания и эксплуатации.</b></h1>
CNI or Container Network Interface. And, as it becomes clear from its name, CNI stands for connecting, adding and deleting disconnecting containers to networks.
Mainly CNI is a framework or a plugin that can dynamically configure networking resources (network, IP-addresses, hosts). In other words, this plugin inserts a network interface into the container network namespace and make any necessary changes on the host.

There're different types of plugins of CNI. For example, flannel, calico and others. 
Calico, in its turn, provides a CNI plugin that can be used for integration with Kubernetes. Calico creates a flat layer-3 network and assigns a fully routable IP address to every pod.
To install Calico you can use yaml file which creates calico-node daemonset (pod that runs on all the nodes of the K8s cluster). So it installs just like any other pod:

kubectl apply -f address_to _pod/calico.yaml
        
<h1><b>Что такое виртуализация? Какие виды бывают, чем виртуализация отличается от контейнеризации и отличается ли?
</b></h1>	
Virtualization is a process that allows for more efficient utilization of physical computer hardware and is the foundation of cloud computing.
It uses software to create an abstraction layer over computer hardware that allows the hardware elements of a single computer to be divided into multiple virtual computers - virtual machines.
Each VM runs its own operating system (OS) and behaves like an independent computer.

  Types of virtualization:
  •	Desktop virtualization
  •	Network virtualization
  •	Storage virtualization
  •	Data virtualization
  •	Application virtualization
  •	Data center virtualization
  •	CPU virtualization
  •	GPU virtualization
  •	Linux virtualization
  •	Cloud virtualization
  
Containerization and virtualization have something in common, but some things are different. Server virtualization reproduces an entire computer in hardware, which then runs an entire OS. The OS runs one application. That’s more efficient than no virtualization at all, but it still duplicates unnecessary code and services for each application you want to run.
Containers take an alternative approach. They share an underlying OS kernel, only running the application and the things it depends on, like software libraries and environment variables. This makes containers smaller and faster to deploy.

  
        
    
	
	
