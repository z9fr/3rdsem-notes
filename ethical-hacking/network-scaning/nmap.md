
*Host discovery*
=

> when discovering hosts on local network, nmap will try ARP first

---

ICMP ECHO ping scan
----
Variant – ping sweep

```bash
nmap –sn –PE 10.0.0.100-10.0.0.200
```


TCP SYN Scan
----
Basic TCP SYN packet

```bash
nmap –sn –PS
```

TCP ACK scan
----
Send an empty TCP ACK packet

```bash
nmap –sn –PA
```

---

Port/service discovery
=

TCP
----

- Open – TCP connect  
- Stealth – half-open  (SYN Scan)

```bash
# full-scan
nmap -sT <ip addr>

# half-scan
nmap -sS  <ip addr>
```

- ACK flag 

```bash
nmap -sA
```

- IDLE/IPID scan
	- Attacker sends packet with spoofed address from a [“zombie”] computer to a target  
	- If target replies (port open), zombie sends a RST packet as the reply was  unsolicited

```bash
nmap –sI
```

---

UDP/SCTP/SSDP scanning
---

##### UDP - Raw ICMP port unreachable

```
nmap –sU
```

- Sending packet to a specific UDP por
- Port open – no response; port closed – ICMP port unreachable

##### SSDP 

```
nmap –sL
```

- discover local service

---

*Nmap optimisation techniques*
==

- Scan faster - reduce the scope of the scan `-sn`
- Control aggressiveness -  (`–T`) profiles 0-5 , higher the faster

---

OS Discovery
=

Nmap and unicornscan

```
nmap –O
```

- nmap also has a programmable engine for OS discovery

### Passive banner grabbing

capture packets from target host via sniffing to determine particular behaviour
- Error messages
- Network traffic
- Page extensions

### Specific behaviour, as set by the OS

- TTL - each OS sets its default value  
- Window size – vary between OSes  
- DF bit – set or not  
- ToS – set or not

### Banner grabbing countermeasures

- dissable or change the banner
- hide file extensions from web pages

---

Evasion Techniques
=

