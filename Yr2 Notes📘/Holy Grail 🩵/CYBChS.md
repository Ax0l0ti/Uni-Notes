# CyberSexy Key Terms
---
> [!info]+ File Details
> Includes information about this (genus:: Cheat Sheet) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  14-04-2025  
> > *Module :* [[Yr2 Notes📘/Semester 2/Cybersecurity/Cybersecurity]]  
> > *Teacher*: #Chatted  
> > *Resources :*  

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#🚨 Speed run]]
> > [[#Exam Breakdown]]
> > [[#🧮 Definitions by Topic]]
> > [[#]]
> > [[#]]

---
> [!danger]+ 🚨 *Speed run*
> - **Cryptography**: AES, RSA, SHA-2, SHA-3, MD5, SHA-1, CSPRNG, Diffie-Hellman, Elliptic Curves, Digital Signatures, Preimage Problem, Hashing, Symmetric vs Asymmetric Encryption, Forward Secrecy  
> - **Network Security**: DNS, BGP, HTTPS, SSL/TLS, IPv4 vs IPv6, Man-in-the-Middle, Protocol Downgrade, Same-Origin Policy, Secure Headers, Secure Transmission  
> - **Application Security**: SQL Injection, XSS, CSRF, Prepared Statements, Input Validation, Sanitization, Vulnerable Plugins, OWASP Top Ten  
> - **Mobile & IoT Security**: Android App Security, IoT Device Risk, Insufficient Binary Protection, Supply Chain Security, Insecure Data Storage, Credential Misuse  
> - **Authentication & Access Control**: MFA, Password Hashing, Salt, Rate Limiting, Account Lockout, Biometrics, Tokenization, Principle of Least Privilege  
> - **Digital Forensics**: Evidence Collection, Chain of Custody, End-User Devices, Cloud Recovery, Prosecution Readiness, Forensic Ethics  
> - **Security Models & Threats**: CIA Triad, Bell-LaPadula, Biba, Threat Models, Attacker Profiles, Malware (Sunburst, Ransomware), Insider Threats, Red/Blue Teams  
> - **Case Studies**: SolarWinds, Colonial Pipeline, Sony Breach, Capital One Cloud Leak, British Airways Hack  
> - **Web Technologies**: JavaScript Security, JSON Logs, DevTools, HTTP Codes, Cross-frame Communication  
> - **Security Engineering**: HSMs, TPMs, Secure Enclaves, Hardware Attacks (Row Hammer), Secure Update Chains

---
## Exam Breakdown

> [!sigma]+ Exam
> 10 multiple choice questions
> One long question (in several parts)
> 
> In terms of "what content is examined", in principle all that has been lectured is examinable. But I am interested in high-level facts rather than details. I realise this isn't a very helpful statement, so here's an example (and I hope the MCQ part of the mock examination helps more).
> - I **DO** expect you to know that MD5 is a thoroughly discredited hash function (for a long time), and its use for any purpose is a major alarm bell.
> - I DO **NOT** expect you to know exactly how or when it was discredited.
> - For cryptography, again I expect a high-level understanding, rather than details (and note that I haven't even given details of AES, SHA-x etc.). So for Diffie-Hellman key agreement
> - I DO **NOT** expect you to know the details (and people use Elliptic Curve Diffie-Hellman, and I haven't explained elliptic curves at all)
> - I **DO** expect you to know that the message key has contributions from both A and B, so that breaking B's random number will not break any other communication.
> **Examination Information Update**

> [!danger] **EXAM NOTEEE**
> Some of you have noticed that the examination is marked as "Open Book", but the interpretation of "open book" in this course is as follows.  
> I will give you (via Moodle) the story a week in advance of the examination, for you to read, digest and, should you wish, research. This is the extent to which the examination is "open".  
> However, YOU MAY NOT BRING anything into the examination, and I do not expect you have done any further research on the story, but I DO expect you to have understood it.

---
## 🧮 Definitions by Topic

> [!abstract]+ Cryptography
> - **AES**: Symmetric encryption standard using block cipher mode.
> - **RSA**: Public-key cryptosystem for secure data transmission.
> - **SHA-2 / SHA-3**: Cryptographic hash functions with higher security than MD5/SHA-1.
> - **CSPRNG**: Cryptographically secure random number generator.
> - **Diffie-Hellman**: Key exchange protocol over insecure channels.
> 	- Alice computes and sends pubic key $A = g^a \mod p$
> 	- Alice receives $B$ and computes secret key $s = B^a \mod p \ \ \ (= g^{ba} \mod p)$
> 	- Alice and Bob can now communicate over an insecure channel
> - **Elliptic Curves**: Efficient structures for public-key cryptography.
> - **Digital Signature**: Verifies authenticity of digital messages.
> - **Preimage Problem**: One-way function property in hashing.
> - **Forward Secrecy**: Ensures session keys are not compromised retrospectively.

> [!tip]+ Network Security
> - **DNS**: Resolves domain names to IP addresses.
> - **BGP**: Routing protocol between autonomous systems.
> - **HTTPS**: Encrypted HTTP using SSL/TLS.
> - **SSL/TLS**: Protocols for secure internet communication.
> - **MITM Attack**: Intercepts communications between parties.
> - **Protocol Downgrade Attack**: Forces use of insecure protocol.
> - **Same-Origin Policy**: Restricts resource access between domains.
> - **Secure Headers**: HTTP response headers to enforce security.
> - **IPv4/IPv6**: Internet address formats.

> [!info]+ Application Security
> - **SQL Injection**: Exploits unsanitized inputs to run SQL code.
> - **XSS**: Injects malicious scripts into websites.
> - **CSRF**: Triggers unwanted actions via authenticated users.
> - **Prepared Statements**: Prevent injection through parameter binding.
> - **Input Validation**: Ensures user data is safe.
> - **OWASP Top Ten**: Key security risks for web apps.

> [!success]+ Authentication & Access Control
> - **MFA**: Multi-Factor Authentication using multiple identity proofs.
> - **Hashing**: One-way transformation of passwords.
> - **Salting**: Adds randomness to hashed passwords.
> - **Rate Limiting**: Prevents brute force by slowing access.
> - **Biometrics**: Fingerprints, facial recognition, etc.
> - **Least Privilege**: Only give access needed to perform role.

> [!heart]+ Digital Forensics
> - **Evidence Collection**: Gathering and preserving digital evidence.
> - **Chain of Custody**: Ensures evidence integrity over time.
> - **Forensic Ethics**: Guidelines on handling sensitive data.
> - **Remote Evidence**: Collecting from cloud, remote servers, etc.

> [!bug]+ Security Models & Threats
> - **CIA Triad**: Confidentiality, Integrity, Availability.
> - **Bell-LaPadula**: No read up, no write down.
> - **Biba Model**: Ensures data integrity (no write up, no read down).
> - **Threat Models**: Analysis of potential attacker strategies.
> - **Sunburst**: Malware in SolarWinds update.
> - **Insider Threats**: Security risks from within the org.
> - **Red/Blue Teams**: Simulated attackers (red) vs defenders (blue).

> [!warning]+ Case Studies
> - **SolarWinds**: Nation-state level supply chain breach.
> - **Colonial Pipeline**: Ransomware attack shutting down oil supply.
> - **Sony Breach**: Leak of confidential media and IP.
> - **Capital One**: Cloud misconfiguration leading to data theft.

> [!omega]+ Web & Engineering
> - **DevTools**: Browser tools for inspecting and debugging.
> - **HTTP Codes**: Responses like 200 (OK), 404 (Not Found), etc.
> - **Secure Enclave**: Hardware area for secure computation (e.g., Intel SGX).
> - **TPM**: Trusted Platform Module, stores cryptographic keys.
> - **HSM**: Hardware Security Module, for crypto operations.

> [!leaf]+ Additional Topics from Learning Outcomes and Unit Description
> - **Security Models**: Abstract frameworks for designing secure systems (e.g., Bell-LaPadula, Biba, Multics).
> - **System Security**: The extent to which a system is protected against unauthorized access or modifications.
> - **Security Weaknesses**: Vulnerabilities or misconfigurations exploitable by attackers.
> - **Biometrics**: Authentication using physiological traits (e.g., fingerprints, facial recognition).
> - **User IDs**: Unique identifiers for users to track access and permissions.
> - **Data Protection Act**: UK legislation protecting personal data from misuse.
> - **Freedom of Information Act**: Grants public access to data held by public authorities.
> - **Regulation of Investigatory Powers Act (RIPA)**: UK law governing surveillance and data interception.
> - **Memory Protection**: Prevents one process from accessing memory allocated to another.
> - **Memory Mapping**: Associates files or devices with regions of memory.
> - **Virtual Memory**: Abstracts physical memory to improve security and multitasking.
> - **chown**: Unix command to change file ownership.
> - **chgrp**: Changes group ownership of files/directories.
> - **setuid**: Unix permission that runs a file with the privileges of the file's owner.
> - **chroot**: Restricts a process to a subset of the filesystem.
> - **Multics Security Model**: Early influential model emphasizing layered security and rings of protection.
> - **Capabilities**: Access control model where references include associated permissions.
> - **Man-in-the-Middle (MITM)**: Attack where the adversary secretly intercepts or alters communications.
> - **OWASP Top Ten**: A list of the ten most critical web application security risks published by OWASP.
