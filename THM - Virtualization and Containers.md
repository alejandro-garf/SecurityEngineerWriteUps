# Virtualization and Containers — TryHackMe Writeup

---

## Task 1: What is Virtualization

Virtualization allows multiple virtual machines to run on a single physical host, with scalability being one of its primary benefits. Each VM runs its own operating system, referred to as the **Guest OS**.

**Q: Scalability is a primary benefit of virtualization?**
A: True

**Q: What is the operating system of a VM called?**
A: Guest OS

---

## Task 2: Hypervisors

A hypervisor provides the ability to create the abstraction layer between hardware and software. There are two types:

- **Type 1 (Bare Metal):** Creates an abstraction layer directly between the hardware and virtual machines with no common OS in between — the hypervisor itself is the operating system.
- **Type 2 (Hosted):** Runs on top of an existing OS. Examples include VMware Workstation, VMware Fusion, VirtualBox, Parallels, and QEMU.

**Q: VirtualBox is known as what type of hypervisor?**
A: Type 2

**Q: Type 1 hypervisors are also known as what?**
A: Bare metal hypervisors

---

## Task 3: Containers

Containers have their own filesystem, a portion of computing resources (CPU, RAM), a process space, and more. However, unlike full VMs, containers are **not** completely abstracted from the host operating system — they share the host kernel.

**Q: Containers are not completely abstracting from the host operating system?**
A: True

---

## Task 4: Docker

Docker Hub is a remote repository for Docker images, similar to how GitHub hosts code. To get the flag, we run the provided command to spin up the container, then curl the given IP address to retrieve it.
```bash
docker run -p 5000:5000 -d cryillic/thm_example_app
curl http://10.65.177.112:5000
```

---

## Task 5: Kubernetes

Kubernetes (K8s) is an orchestration platform used to manage and scale containerized workloads. The questions in this task walk through basic kubectl commands to explore a live cluster.

**Q1:** Run the provided command to deploy the application.

**Q2:** To list all running pods in the default namespace:
```bash
kubectl get pods
```

**Q3:** To list pods across all namespaces:
```bash
kubectl get pods -A
```

**Q4:** The pod name is pulled directly from the output of Q2.

**Q5:** To list all deployments:
```bash
kubectl get deployments
```

**Q6:** To list all services:
```bash
kubectl get services
```

**Q7:** To list all replica sets:
```bash
kubectl get rs
```

**Q8:** The replica set name is pulled from the output of Q7.

**Q9:** To delete the deployment:
```bash
kubectl delete deployment helloo-tryhackme
```
