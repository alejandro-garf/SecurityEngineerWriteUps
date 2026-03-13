# TryHackMe Room Writeup — Preservation of Evidence & Incident Handling

---

## Preservation of Evidence

The biggest mistake made during incidents is **shutting the host down**, as this destroys volatile data that cannot be recovered.

### Order of Volatility

Evidence should be collected in order from most to least volatile:

| Priority | Data Type |
|---|---|
| 1 | Registers and cache |
| 2 | Routing and ARP tables |
| 3 | Temporary files |
| 4 | Disk |
| ... | ... |
| 7 | Archival media |

### Key Collection Considerations

- **Registers and cache** are extremely volatile and constantly changing as the host executes different applications — capture these first.
- Capture network information such as **routing and ARP tables** to understand which subnet the host was connected to. This helps determine the scope of the incident and identify other hosts that should be scrutinised.
- Capture any **temporary files** created by applications on the host.
- Take a **snapshot of the host's drive**.
- Do not trust the programs on the compromised system.
- Do not run programs that modify the access times of files.

**Question Answers:**
- The disk is given a priority of **4**.
- Archival media is last at **7**.
- Registers and cache are **1**.
- **Chain of custody** is important to ensure we can prove evidence has not been tampered with.

---

## Alerting the Relevant Stakeholders

- A **playbook** provides predefined steps and actions to help the team deal with incidents.
- **Call trees** indicate who has to be informed and who is responsible for informing them.

**Question Answers:**
- The answers are **call tree** and **playbook**.

---

## Isolation of the Incident

The biggest pitfall during an incident is moving to eradication and recovery **before** the appropriate containment actions have been performed.

Isolation aims to ensure that the infection cannot spread to other hosts on the network. There are several approaches:

- **Virtual Isolation** — The host is collected and fully isolated from the network and users; the host is restricted from communicating through the use of software.
- **Physical Isolation** — The device is physically disconnected from the network.
- **Network Segmentation** — Instead of full isolation, the team can rate-limit the network speed. Slowing down the connection allows the team to perform a more in-depth analysis of the actions being performed.

**Question Answers:**
- **Virtual isolation** can be performed remotely through EDR.
- **Physical isolation** is the second answer.
- **Network segmentation** is the third answer.

---

## Business Continuity Planning (BCP)

A **BCP (Business Continuity Plan)** is a plan meant to help an organisation recover from an incident. It is more encompassing than a DRP and covers elements such as communication to internal and external stakeholders.

A **DRP (Disaster Recovery Plan)** focuses mainly on the technical recovery of a division.

### Key Recovery Metrics

| Term | Definition |
|---|---|
| **Recovery Point Objective (RPO)** | The amount of data we are willing to accept can be lost. |
| **Recovery Time Objective (RTO)** | The amount of time required to recover the hardware of our system. |
| **Work Recovery Time (WRT)** | The amount of time required to recover the software and data of our system. |
| **Maximum Tolerable Downtime (MTD)** | The maximum amount of downtime that we are willing to accept. |
| **Mean Time Between Failures (MTBF)** | How long our system will operate between incidents on average. |
| **Mean Time To Repair (MTTR)** | How long it will take to recover our system on average. |

**Question Answers:**
- **BCP** stands for Business Continuity Plan.
- **DRP** stands for Disaster Recovery Plan.
- **Recovery Time Objective** deals with the time required for the recovery of hardware.
- **Mean Time To Repair** deals with the average amount of time required to recover a system.

---

## Documentation of Actions

Even when a BCP is invoked, documentation is incredibly important. Best practices include:

- Use a template for documentation.
- After the incident, conduct a **lessons learned** session.

**Question Answers:**
- Time should be noted in **UTC**.

---

## Handing Over

Follow through the site to complete the final task.

> Flag: `THM{I.am.ready.to.become.a.first.responder}`
