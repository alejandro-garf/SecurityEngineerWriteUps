# TryHackMe Room Writeup — Secure Software Development Lifecycle (SSDLC)

---

## What is SSDLC?

Secure SDLC models aim to introduce security at every stage of the SDLC. Security is a constant concern, improving software quality continuously. Key benefits include:

- **Boosted security education and awareness** — All stakeholders are aware of each phase's security recommendations and requirements.
- **Early flaw detection** — Vulnerabilities are identified before deployment, reducing the risk of being hacked or disrupted.
- **Cost and time savings** — Early detection and resolution of vulnerabilities reduces business risk, brand reputation damage, and fines that could otherwise lead to economic disaster.

**Question Answers:**
- It costs **15 times more** to identify vulnerabilities in the testing phase.

---

## Implementing SSDLC

To implement a Secure SDLC, the following steps should be taken:

1. Perform a **gap analysis**.
2. Create **Software Security Initiatives (SSI)**.
3. Formalise processes.

Key security activities mapped to SDLC stages:

| SDLC Stage | Security Activity |
|---|---|
| Planning & Requirements | Risk Assessment |
| Design | Threat Modelling |
| Development | Code Scanning / Review |
| Testing | Penetration Testing & Vulnerability Scanning |

**Question Answers:**
- You need to understand the security posture before implementing a Secure SDLC process.
- A **risk assessment** is performed during the planning and requirements stage.
- **Threat modelling** is carried out during the design phase.

---

## Risk Assessment

Risk assessment involves listing factors such as:

- The data value of the program.
- The security level of companies providing resources the code depends on.
- The clients purchasing the software.
- The distribution scale of the software (single user, small workgroup, or worldwide release).

Risk evaluation should also include worst-case scenario analysis in the event of a successful attack.

> **Formula:** `Risk = Severity × Likelihood`

**Question Answers:**
- The risk formula is **Severity × Likelihood**.
- The second question refers to a **quantitative risk assessment**.

---

## Threat Modelling

Threat modelling is a structured process of identifying potential security threats and prioritising mitigation techniques so that assets classified as valuable or high-risk during the risk assessment — such as confidential data — are protected.

Common threat modelling methodologies include **STRIDE**, **DREAD**, and **PASTA**.

### STRIDE

STRIDE stands for:

- **S**poofing
- **T**ampering
- **R**epudiation
- **I**nformation Disclosure
- **D**enial of Service
- **E**levation/Escalation of Privilege

### DREAD

DREAD ranks threats by assigning scores based on severity and risk probability. Each component is scored on a scale of 0–10:

| Component | Description |
|---|---|
| **Damage** | The potential impact of a threat. |
| **Reproducibility** | The complexity of reproducing the threat. |
| **Exploitability** | How easily the threat can be exploited. |
| **Affected Users** | The number of users impacted. |
| **Discoverability** | The ease of discovering the threat. |

**Question Answers:**
- **DREAD** is the modelling methodology based on risk probability.
- **STRIDE** is built upon the CIA Triad.
- **PASTA** aligns technical requirements with business objectives.

---

## Secure Coding

Secure code review is a measure where the code itself is verified and validated to ensure that found vulnerabilities can be mitigated and removed.

### Testing Methodologies

| Method | Full Name | Description |
|---|---|---|
| **SAST** | Static Application Security Testing | A white-box testing method that directly analyses the source code. |
| **DAST** | Dynamic Application Security Testing | A black-box testing method that finds vulnerabilities at runtime. |
| **IAST** | Interactive Application Security Testing | Analyses code for security vulnerabilities while the app is running; checks source code similar to SAST, but at the post-build stage. |
| **RASP** | Runtime Application Self-Protection | Protects the application at runtime by detecting and blocking attacks in real time. |

**Question Answers:**
- **SAST** is recommended at the beginning of the SDLC.
- **DAST** analyses applications using the black-box method.
- **SAST** uses the white-box method.

---

## Security Assessment

Security assessments consist of two primary activities: **Penetration Testing** and **Vulnerability Assessments**.

**Question Answers:**
- **Vulnerability assessments** are more budget-friendly.
- **Penetration testing** is the second answer.
- Both vulnerability assessments and penetration tests are carried out during the **operations and maintenance** phase.

---

## SSDLC Methodologies

### Microsoft's SDL

Microsoft's Security Development Lifecycle is built on four core principles:

- **Secure by Design** — Security is a built-in quality attribute affecting the whole software lifecycle.
- **Security by Default** — Software systems are constructed to minimise potential harm caused by attackers; for example, software is deployed with the least necessary privilege.
- **Secure in Deployment** — Software deployment is accompanied by tools and guidance supporting users and administrators.
- **Communications** — Software developers are prepared for occurring threats by communicating openly and in a timely manner with users and administrators.

### Other Methodologies

- **SAMM (Software Assurance Maturity Model)** — Allows you to measure tailored risks facing your organisation.
- **BSIMM (Building Security In Maturity Model)** — Acts as a measuring stick to determine your security posture.

**Question Answers:**
- Microsoft's SDL follows a set of mandatory procedures embedded in the SDLC.
- **SAMM** allows you to measure tailored risks facing your organisation.
- **BSIMM** acts as a measuring stick to determine your security posture.
- Follow through the final task to get the flag.
