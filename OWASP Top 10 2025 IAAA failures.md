
\# TryHackMe Room Writeup — IAAA, Access Control & Authentication Failures

---

## What is IAAA?

IAAA is a simple framework for thinking about how users and their actions are verified on applications. Each step depends on the previous one — if a prior item is not being performed, the later ones cannot be carried out.

The four components are:

1. **Identification** — Who are you?
2. **Authentication** — Prove who you are.
3. **Authorisation** — What are you allowed to do?
4. **Accountability** — What did you do?

**Question Answers:**
- IAAA stands for **Identity, Authentication, Authorisation, Accountability**.

---

## Broken Access Control

Broken Access Control occurs when the server does not properly enforce who can access what on every request. This allows users to act outside of their intended permissions.

**Question Answers:**
- **Horizontal privilege escalation** fits this description.
- Flag: `THM{Found.the.Millionare!}`

---

## Authentication Failures

Authentication Failures happen when an application cannot reliably verify or bind a user's identity. This can allow attackers to impersonate legitimate users or access accounts that do not belong to them.

**Question Answers:**
- Flag: `THM{Account.confusion.FTW!}`

---

## Logging & Alerting Failures

Follow through the site to identify the attacker's activity in the logs.

**Question Answers:**
- Attacker IP address: **203.0.113.45**
- The account targeted: **admin**
- The attacker attempted to access: **super secret admin stuff**
