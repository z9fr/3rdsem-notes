
## Hacking Methodology

![image](https://media.geeksforgeeks.org/wp-content/uploads/20210701141720/UntitledDiagram.png)


---

# Gaining Access

## Microsoft User Passwords

- windows store passwords in the SAM registory file
- NTLM Authentication Process
- Kerberos Authentication
	- Microsoft has upgraded to Kerberos which provides strong mutual authentication

## Types of Password Attack

- Non-Electronic/non-technical Attacks 
	- dumpster diving, Shoulder-surfing
- Active Online Attacks
	- password guessing
- Passive Online Attacks
	- sniffing, mim
- Offline Attacks
	- recover hashdump

## Password Cracking

- Dictionary Attacks
- rule based
- rainbow table
- guessing
- default passwords
- bruteforce


---

# Buffer Overflow

## stack based Buffer Overflow

> Exploit the ability to overwrite the memory to inject  malicious code


## Heap-Based Buffer Overflow

> Vulnerability leads to overwriting links to dynamic memory allocation

- dynamic memory alocation

---

# Escalating Privileges

-  Horizontal Privilege Escalation – use of resources of  another user with similar access permissions  
- Vertical Privilege Escalation - obtaining access to  resources of a user wit higher privileges

<u>Techniques include</u>
- DLL Hijacking
- exploiting vulns
- Misconfigured Service

---

# Maintaining Access

> Execution of malicious applications to enabled continued access and capturing of information, additional accounts, access to system resources


- Backdoors
- crackers
- keyloggers
- spyware


## Remote Code Techniques

- schedule task
- service execution - new services
- exploiting vulns

---

## Types of Rootkt

- Hypervisor-Level Rootkit – exploiting hardware features  such as Intel VT and AMD-V  
- Hardware/Firmware Rootkit – create a persistent malware  image in firmware  
- Kernel-Level Rootkit – modifying kernel or device drivers  
- Boot-Loader-Level Rootkit – modifying the boot loader  
- Application-Level/User-Mode Rootkit – exploiting APIs  
- Library-Level Rootkit – patch, hook or supplant system calls


### exmple rootkis

- LoJax – UEFI rootkit  
- Scranos – a trojanised rootkit masquerades as cracked software  
- Horse Pill – ramdisk-based containerised rookit  
- Necurs – a kernel-mode driver rootkit

### Detection of rootkits – Host-Based IDS/Anti-Rookits  

- Integrity-Based Detection  
- Signature-Based Detection  
- Heuristic/Behaviour-Based Detection  
- Runtime Execution Path Profiling  
- Cross-View-Based Detection 
- Alternative Trusted Medium – most reliable  
- Analysing memory dumps


----

> Steganography is another Additional Techniques for Hiding Files


---

# Covering Tracks

> Essential step if an attacker wishes to remain obscure


### techniques

- disable logs
- clear logs
- manipulating logs
- delete files
- dissable windows functionalty

