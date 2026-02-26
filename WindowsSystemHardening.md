# Windows Security Writeup

---

## Understanding General Concepts

### Notes
- To check the running services on a windows machine, you start the run app and type in `services.msc`
- `regedit` = windows registry
- Event Viewer = `eventvwr`

### Questions
1. The first question stumped me as I was not sure what it was asking, had to look it up.
2. Ran `regedit` and then used the find option to find the flag
3. Navigated to the proper directory to get the flag.

---

## Identity and Access Management

### Notes
- No notes on this one

### Questions
- To find the administrator account I would go to Control Panel and then to user accounts = Harden
- For the next answer I have to to the change user account control setting
- There were no other accounts in the vm.

---

## Network Management

### Notes
- There are three profiles, private, public and domain
- Disable SMB protocol if not in use.
- Hosts file acts like a local DNS
- `arp -d` clears the arp cahce
- Disable remote desktop if not in use

### Questions
- Went to firewall -> Monitoring -> Public Profile is active
- Went to the file throught the file explorer and got the answer
- ran the command in the command prompt and got the answer

---

## Application Management

### Notes
- No notes

### Questions
- For the first one I have to go through windows security, go to the virus and threat protection settings, scroll to exclusions to view which exlusions there are.
- Second question is self explaneatory ( I hope lol)
- Third question just follow the directions in the notes porion of it.

---

## Storage Management

### Notes
- No notes, just general info about different security/hardening settings on Windows machines

### Questions
- For the first question I will take an exploratrion of the directory to see if it is stored in random folders - its in the documents folder
- Other two questions are found just by using the file explorer
