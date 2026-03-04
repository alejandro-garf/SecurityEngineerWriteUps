# General Active Directory Concepts

## Notes
- The Domain Controller is the brain of the Windows domain server.
  - Acts as an authenticator
- Trees are sets of domains
- Forests are sets of Trees
- There are trusts based on characteristics, which are transitive, and directional trusts, which are not.

## Questions
- Had to go to Active Directory's Domains and Trusts to find the answer

---

# Securing Authentication Methods

## Notes
- We don't want Windows to store the LAN hash.
- We want to make sure Server Message Block signing is enabled.

## Questions
- The answers are found in the Group Policy Management Editor if you follow the steps.

---

# Implementing Least Privilege Model

## Questions
- Computers and printers must be added to the domain tier.
- You should not grant a contractor a high privilege account.

---

# Microsoft Security Compliance Toolkit

## Notes
- Can install and execute security baselines very easily.
- Policy Analyzer also helps you find inconsistencies and misconfigurations.

## Questions
- For the first flag:
  - Go to the scripts folder
  - Click on File, then Run with PowerShell
  - After it ran, nothing happened, so I looked inside the file and found the flag
- For the second flag:
  - Find the file, open it, and the flag is there

---

# Protecting Against Known Attacks

## Notes
- MFA can prevent Kerberoasting attacks.

## Questions
- Kerberos does use offline password cracking.
- If you open the file, you get the answer for the second one.
