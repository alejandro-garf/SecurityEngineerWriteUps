 THM — Networking Fundamentals Walkthrough

## Application Layer

Starting off with the application layer. The big takeaway here is that TCP and UDP
protocols each bind to specific ports — this comes up constantly in CTFs and recon,
so worth drilling in.

### FTP

FTP runs over TCP and has two modes you need to know:

- **Active** — the server reaches back out to the client to establish the data connection.
- **Passive** — the client sends a `PASV` command and the server opens a port for the
  client to connect to. This is the more firewall-friendly option and shows up more
  in the real world.

### Email Protocols

- **SMTP** is the push protocol — it's what sends and routes email between servers.
- **POP3** pulls messages down from the server to your local client.
- SMTPS uses **port 465** (implicit TLS) or **port 587** (STARTTLS). Both are fair
  game on exams and CTFs.

### Question Answers

- HTTPS port → **443**
- FTP passive command → **PASV**

---

## DNSSEC

DNSSEC is essentially DNS with a trust layer bolted on. The core idea is that DNS
responses get signed with the domain owner's private key, so you can actually verify
the response you're getting is legit and not spoofed. Without it, you're just trusting
whatever answer the resolver gives you — which opens the door to cache poisoning.

> For the questions here, just do the reading — they test comprehension of the above.

---

## Presentation & Session Layers

### SOCKS5

SOCKS5 is a proxy protocol that routes your traffic through a delegate server. Useful
for firewall traversal and anonymizing connections. You'll see this come up in red team
tooling a lot.

### TLS Handshake

This is the important one. The handshake goes like this:

1. **Client Hello** — client sends supported TLS versions and cipher suites.
2. **Server Hello** — server picks a cipher suite and sends its certificate.
3. **Authentication** — client verifies the certificate.
4. **Premaster Secret** — client generates one and encrypts it with the server's public key.
5. **Decryption** — server decrypts it with its private key.
6. **Key Derivation** — both sides independently derive the same session keys.
   Keys are **never transmitted** directly — this is the key point.
7. **Encrypted Session** — everything from here on is encrypted.

> The flag for this section comes from following the steps above in the task.
> The rest of the questions are reading comprehension.

---

## Network Layer

### IPsec

IPsec operates at the network layer and secures traffic through three mechanisms:

- **Authentication Header (AH)** — handles integrity. Confirms packets weren't tampered with.
- **Encapsulating Security Payload (ESP)** — handles confidentiality. Actually encrypts the payload.
- **Security Association (SA)** — manages the key exchange and negotiation between peers.

### Question Answers

- ESP stands for → **Encapsulating Security Payload**
- Vendor commonly used with IPsec VPNs → **Cisco**
- Secure web protocol pairing → **TLS/SSL**
```
