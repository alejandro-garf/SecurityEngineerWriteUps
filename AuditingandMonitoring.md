# TryHackMe Room Writeup — IT Auditing & Log Management

---

## Introduction

- **Auditing** is the systematic review of an organisation's technological infrastructure, policies, and operations.
- **Monitoring** is the continuous observation of an organisation's computer technologies and related resources.

---

## Audit Objectives and Types

Auditing of information systems involves the systematic, independent, and objective examination of an organisation's IT infrastructure, processes, and controls.

There are two major audit types:

- **Internal Audits** — Performed by an organisation's own personnel or staff members assigned to the internal audit function.
- **External Audits** — Conducted by independent auditors not employed by the organisation being audited. These auditors are typically from external accounting or auditing firms, and the primary purpose is to provide an impartial and objective review.

> **Note:** If we don't start with an internal audit, we will most likely need multiple external audits, which can get quite expensive.

**Question Answers:**
- External audits are conducted by independent auditors.
- Internal audits are conducted by an organisation's own personnel.

---

## Audit Frameworks

**Question Answers:**
- **PCI DSS** is a framework for the payment card industry.
- **CCTA** developed ITIL.
- **ISACA** developed COBIT.

---

## Auditing IT Infrastructure and Operations

The audit process follows these steps in order:

1. **Planning** — Identify the audit scope.
2. **Information Gathering**
3. **Risk Assessment and Control Evaluation**
4. **Testing**
5. **Analysis and Findings**
6. **Reporting** — Present our findings.
7. **Follow-Up** — The organisation reviews the findings.

**Question Answers:**
- We present our findings during the **reporting** phase.
- Organisations review the findings during the **follow-up** phase.
- The audit scope is identified during the first step: **planning**.

---

## Log Management on Linux

Many Linux distributions use system logging daemons such as `rsyslog`, `syslog-ng`, and `journald` to manage, process, and store log events.

### Types of Logs

- **System logs** — Contain information about the general health and operation of the system.
- **Application logs** — Contain information about the specific applications running on the system.
- **Security logs** — Contain information about security-related events, such as logins and failed authentication attempts.

### Useful Commands

Get a summary of events:
```bash
aureport --summary
```

View failed login events:
```bash
aureport --failed
```

Search for failed login attempts by a specific user:
```bash
ausearch --message USER_LOGIN --success no --interpret | grep ct=<username> | wc -l
```

**Question Answers:**
- Running `aureport --failed` showed **263** failed logins.
- Running the search command filtered for user `mike` returned **4** failed login attempts.
- Running the search command filtered for user `root`:
  ```bash
  ausearch --message USER_LOGIN --success no --interpret | grep ct=root | wc -l
  ```
  Returned a count of **227**.

---

## Log Management on Windows

**Question Answers:**
- The Event ID for a failed login event is **4625**.
- Under the Security event log, there were **2** relevant events.
- **1** failed login attempt occurred in 2021.
