*What is a honeypot*
----

- A resource that is designed to be attacked and compromised
- Expected to be attacked , probed and exploited 
- Does not fix or prevent anything
- Honeypots helps to gather information for SA

---

*Types of Honeypots - UseCases* 
---

### Research honeypot

- its a trap used by developers, sysadmins and blueteam managers for research purposers

### Production honeypot

-  used by companies and corparations to investigate the behaviour and techniques of hackers seeking to attack the public facing network

---

*Types of Honeypots - Context* 
---

### Server honeypot

- often associated with production
- placed inside production network with other prod servers

### Client Honeypots

- active security devices in search of servers that attack clients
- the client honeypot poses as a client and interacts with the server to examine whether an attack has occured. 
- often client honeypots focus on web browers. 
- any client interfacts with servers can be part of a client honeypoint - ftp, ssh, email, etc

----

*Types of Honeypots - build*
---

- virtual honeypot
- physical honeypot

( A virtual honeypot can emulated multiple systems, but can be more  
easily detected as a honeypot )

----

*Pros of Honeypots*
---

- protect network though deception
- early detection and prevention
- better prepare for sysadmins
- better understanding of attacker actions & motives
- protect real systems 

*Cons of Honeypots*
---

- modern cyber criminals have more resources 
- no matter what, systems get complecated and errors are common
- misconfigurations are common
- new attacks happen
- honeypots detection are limited. emulated hosts can be detected with fingerprinting

----

*Honeypot examples*
---

- Spam honeypot
	- also known as a spam trap. specially created to catch spammers
- Malware honeypot
	- created to simulate vulnerable apps. APIs and systems for getting malware attacks
	- the collected data is used for malware pattern reconnaissance
- Database honeypot
	- databases are common target of web attackers
	- used to watch and learn different attack techniques such as SQL injection , privilage abuse 
- Spider honeypot
	- works by created false web pages and links that only accesable by web-crawlers


---

*Honeynet*
---

honeynet is a decoy network that contains one or more honeypots. you can inject vulnerabilities into honeynet to make it easy for attacker to access trap.

any system on honeynet may serve as a point of entry for attack

---

*Honeypot hunters*
---

fingerprinting, timing can make honeypots easier to detect. the effort of making all honeypoints high-interactive level is not feasible. This has led to a decrease in use but

- Still interesting pieces to apply else where
- Still has its uses in specific cases

could become more popular in future of IoT. if some of the problem was emulating a complex device. if device gets less complecated it maybe easier to fool attackers

---

*Advantages of honeypots*
---

- Reduced False Positives and Negatives
- Flexibility

*Disadvantages of honeypots*
---

- Limited Field of View
- Getting Fingerprinted
- Risk to the Environment

---

*honeytokens*
==

honey tokens also known as honeypots, fake IT resources used to detect cyber criminal activities.

*Types of honeytokens*
--

**Fake email Addresses**
- phishing, malicious attachments, malicious links 
- since fake addresses should never be used in theory. any mail likely come from someone who got access to internal mail server , email address list or compromised public web server

**Fake Database Data**
- inserting fake records with enticing names or suggested content into an existing database 
- these data entries are the honeytokens. which lure hackers into stealing them. or malicious insiders into giving them away

**Embedded Links That 'Phone Home'**
- honeytokens that exist as real data files (documents, programs ) in the file system. but with embedded likes in them fitted with a “phone home”  switch.

**Web beacon**
- consist of internet link to small object embedded within a file. eg: single-pixel grapic 
- when document is open the web beacon will phone home details on the attackers system 

**Fake Executable Files**
- honeytokens as a application.
- these fake executables files are typically created with a "phone home" switch 
- it activates whenever they're run and it will send the hackers information

**Browser Cookies**
- setting up browser cookies as honeytokens get around blocked ports problem
- it enabels the people setting the trap to use methods similar to google and etc to track people who visit them.

**Canary Traps**
- these traps are constructed on the basis of "canary" begin like a whistle-blower, or snitch
- these honeytokens typically consist of some kind of trace

**Amazon Web Services (AWS) Keys**
- when attackers testing the aws keys, aws has a build-in logging system. so we can use it as honeytoken and security teams can monitor how they are used


---

*Questions & Data*
=

Do common attacks `origins` exist ?
- ip address / ip-prefix
- domain name, urldetails
- location
- attacker userId, email
- attackers os


What is the target of the attacks
- IP
- Port and Transport Protocols
- services
- software and clients, plugins
- cve
- os

Is the attacker human or script/machine?
- keystrokes (errors, mistypes, speed)
- time of delay
- speed and volume of attacks
- complexity of action

What are attack frequencies
- number of attacks per time unit, and their origins
- time between attacks
- number of attack origins and targets
- received packets/data per time unit
- number/duration of time in a honeypot

Are there any new questions we need to answer with IoT etc?
- Tying back to situational awareness
- Self learning honeypots
	- monitor local network and dynamically deploy honeypots
- Honey farm
	- centralized collection of honeypots  and analysis tools
- next generation deception technology / security
- emulation on a larger scale
- market size exceeding $1 billion by 2020
- market Research Media estimates the cumulative deception technology market value at $12 billion