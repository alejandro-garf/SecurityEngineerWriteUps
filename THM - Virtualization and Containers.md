# Virtualization and Containers — TryHackMe Writeup

---

## What is Virtualization

- Scalability is a primary benefit of virtualization.
- The operating system of a VM is called a Guest OS.

---

## Hypervisors

A hypervisor provides the ability to create the abstraction layer between hardware and software.

**Type 1 Hypervisors** create an abstraction layer directly between hardware and virtual machines without a common operating system between them. Instead, the hypervisor is the operating system.

**Type 2 Hypervisors**, also known as **hosted hypervisors**, run on top of an existing OS. Examples include VMware Workstation, VMware Fusion, VirtualBox, Parallels, and QEMU.

- VirtualBox is known as a Type 2 hypervisor.
- Type 1 hypervisors are known as bare metal hypervisors.

---

## Containers

Containers have their own filesystem, a portion of computing resources (CPU, RAM), a process space, and more.

- Containers are not completely abstracted from the host operating system.

---

## Docker

Docker Hub is a remote repository for Docker images, similar to GitHub. In order to run the container we need to run the provided command, then curl the IP address that was given to get the flag.

---

## Kubernetes

**Kubernetes**, also shortened to **K8s**, is one such solution known as an **orchestration platform**.

- For the first question, run the provided command.
- For the second question, run `kubectl get pods`.
- For the third question, run `kubectl get pods -A`.
- The fourth answer is found from the first `get pods` command.
- For the fifth question, run `kubectl get deployments`.
- For the sixth question, run `kubectl get services`.
- For the seventh question, run `kubectl get rs`.
- The eighth answer is found from the previous command.
- For the ninth question, run `kubectl delete deployment helloo-tryhackme`.
