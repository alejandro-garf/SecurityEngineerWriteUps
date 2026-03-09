# Virtualization & Containerization

## What is Virtualization

Scalability is a primary benefit of virtualization. The operating system of a VM is referred to as the **Guest OS**.

---

## Hypervisors

A hypervisor provides the ability to create the abstraction layer between hardware and software.

**Type 1 Hypervisors** (also known as **bare metal hypervisors**) create an abstraction layer directly between hardware and virtual machines without a common operating system between them — the hypervisor itself acts as the operating system.

**Type 2 Hypervisors** (also known as **hosted hypervisors**) run on top of an existing OS. Examples include VMware Workstation, VMware Fusion, VirtualBox, Parallels, and QEMU.

---

## Containers

Containers have their own filesystem, a portion of computing resources (CPU, RAM), a process space, and more. Unlike VMs, containers are **not** completely abstracted from the host operating system.

---

## Docker

Docker Hub is a remote repository for Docker images, similar to GitHub. To run a container, execute the provided command, then curl the given IP address to retrieve the flag.

---

## Kubernetes

**Kubernetes** (shortened to **K8s**) is an orchestration platform used to manage containerized workloads at scale.

| # | Task | Command |
|---|------|---------|
| 1 | Deploy the application | *(run the provided command)* |
| 2 | List pods | `kubectl get pods` |
| 3 | List pods across all namespaces | `kubectl get pods -A` |
| 4 | Find pod name | *(from output of command #2)* |
| 5 | List deployments | `kubectl get deployments` |
| 6 | List services | `kubectl get services` |
| 7 | List replica sets | `kubectl get rs` |
| 8 | Find replica set name | *(from output of command #7)* |
| 9 | Delete a deployment | `kubectl delete deployment helloo-tryhackme` |
