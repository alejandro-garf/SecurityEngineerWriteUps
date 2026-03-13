# TryHackMe Room Writeup — Exploits & Vulnerability Lifecycle

---

## What is an Exploit?

Basic review — content and question answers are covered in the reading material.

---

## Vulnerability Lifecycle

The five stages of the Lifecycle of a Vulnerability Framework are:

1. **Discovery**
2. **Coordination**
3. **Mitigation**
4. **Management**
5. **Lessons Learned**

**Question Answers:**
- A **0-day** is a vulnerability that has not been discovered yet.
- **Proof of Concept (PoC)** is the second answer.
- **Patch** is the third answer.

---

## Opportunity for Weaponising Vulnerabilities

- Exploiting 0-day vulnerabilities can take anywhere from a few days to several months or even years.
- Adversaries with access to updated software can reverse-engineer the patch to find the underlying vulnerability.

**Question Answers:**
- The answer to the first question is **yes**.
- An **n-day** is an exploit developed once the patch has been applied.

---

## Exploit Chaining

Exploit chaining is a technique where hackers string together multiple exploits for different vulnerabilities in order to gain complete control of a target system.

**Question Answers:**
- **Exploit chaining** is the first answer.
- **Privilege escalation** is the second answer.
- **Persistence** is the third answer.

---

## Chaining Multiple Vulnerabilities — A Case Study

The first and most crucial step in exploiting a target system is finding and using a vulnerability that provides an initial entry point. As demonstrated in this room, a simple vulnerability like an initial SQL injection can be chained into a series of attacks, leading to an arbitrary file upload and ultimately remote code execution.

> Follow through the provided commands using `sqlmap` to complete the exploitation chain.

**Question Answers:**
- We get the response **undefined** when trying the provided credentials.
- We get **NT AUTHORITY\SYSTEM** after privilege escalation.
- Navigating to the directory gives us the flag: `THM{010101_PAWNED}`
- **2** files were available.

---

## Automating Common Tasks

Common ways to automate security tasks include:

- **Scripts** — Custom-written scripts to perform repetitive tasks.
- **Scheduling tools** — Such as cron jobs (Linux) and Windows Task Scheduler, used to run scripts at specific times.
- **SOAR platforms** — Security Orchestration, Automation, and Response tools that combine multiple automation capabilities.

**Question Answers:**
- It is very important that all scripts and automations we run are from **trusted and official sources**.
