## What is virtualization
### Notes
- None
### Questions
- Scalability is a primary benefit of virtualization?
- Operating system of a vm is called a Guest OS

## Hypervisors
### Notes
- A hypervisor provides the ability to create the abstraction layer between hardware and software.
- Type One hypervisors
	- Create an abstraction layer directly between hardware and virtual machines without a common operating system between them. Instead, the hypervisor is the operating system
- **Type 2 hypervisors**, also known as **hosted hypervisors**
	- Examples of type 2 hypervisors include VMware Workstation, VMware Fusion, VirtualBox, Parallels, and QEMU.
### Questions
- VirtualBox is known as a type 2
- Type ones are known as bare metal hypervisors

## Containers
### Notes
- Containers have their own filesystem, a portion of computing resources (CPU, RAM), a process space, and more
### Questions
- Containers are not completely abstracting from the host operating system

## Docker
### Notes 
- Docker Hub is a remote repository for Docker images, similar to GitHub
### Questions
- In order to run the container we need to:
	- Run the provided command
	- and then curl the ip address that was given to get the flag

## Kubernetes
### Notes
- **Kubernetes**, also shortened to "**K8s**," is one such solution known as an **orchestration platform**.
### Questions
- For the first one we just run the provided command
- For the second one we run `kubectl get pods`
- Third one we run `kubectl get pods -A`
- Fourth one we find from the first get pods command
- For the fifth one you run `kubectl get deployments`
- 6th one we run `kubectl get services`
- 7th one we run `kubectl get rs`
- 8th one we get from the previous command
- 9th one is `kubectl delete deployment helloo-tryhackme`
