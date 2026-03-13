# TryHackMe Room Writeup — Incident Response and Management

---

## What is Incident Response and Management?

Key concepts in incident response:

- If there is sufficient severity, an alert can be raised to an **incident**.
- Sometimes the alert information is not sufficient and we have to gather more information than what is currently provided. This process is usually referred to as **Digital Forensics**.
- A **CERT Incident** is one where we don't yet have enough to raise the alarm bells, but we are concerned and therefore performing additional investigation to determine the scope of the incident.
- At **level four**, it is all hands on deck and officially a full-scale cyber crisis.

**Question Answers:**
- **Level 3** is when SOCs are placed on high alert.
- **Level 4** is when it is a cyber crisis.
- **IM (Incident Management)** is how we respond.
- **IR (Incident Response)** is when we are trying to figure out what happened.

---

## Different Roles During an Incident

| Role | Responsibility |
|---|---|
| **SOC Analyst** | Deals with the various events and alerts that occur in the SOC. |
| **SOC Manager** | Understands the technical information required for an investigation and divides tasks during an incident. |
| **Forensic Analyst** | Performs an investigation to better understand what happened during an incident. |
| **Malware Analyst** | A forensic analyst who focuses on understanding how malware works. |
| **Threat Hunter** | Actively tries to uncover new threats in the environment. |
| **Security Engineer** | Responsible for the security of their division, application, or system. |
| **ISO (Information Security Officer)** | Acts as the bridge between the Incident Response team and their division team that will implement the actions provided by the Incident Manager. |
| **Incident Manager** | Trained to perform management duties for Incident Response and Management. |
| **Product Owner** | Called in as a subject matter expert to assist with the investigation. |
| **Executive (CIO/COO)** | Responsible for ensuring the Crisis Management Team (CMT) functions as it should and can deal with the crisis. |

**Question Answers:**
- Flag: `THM{Roles.and.Responsibilities.of.IR.and.IM}`

---

## The Process of Incident Management

Key preparation activities include:

- Identify and document key stakeholders and call trees that will be used during an incident.
- Create and update playbooks that aid the team in following a set process for incidents with a known nature.
- Exercise the team's ability to deal with an incident through tabletop exercises and cyber war games.
- Continuously perform threat hunting to help create new alert rules based on modern attacker techniques.
- Once the scope of the incident is better understood, the team begins with **containment**, **eradication**, and **recovery**.

**Question Answers:**
- Flag: `THM{Preparation.is.Key.for.Incident.Management}`

---

## Common Pitfalls During an Incident

- Once a solution is deployed, there may still be configurations that did not adhere to security best practices but were implemented to get the solution up and running faster.
- The **hardening process** reverses these configurations to bring them back in line with security best practices.

**Question Answers:**
- Flag: `THM{Avoiding.the.Common.IM.Mistakes}`
