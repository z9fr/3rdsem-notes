*Ruleset categories of snort*
----

- Attack-Response Rules
	- designed to catch the results of successful attack
	- things like `id=root` , or errors that indicates compromise.
- BotCC Rules
	- auto-generated from several sources confirmed by active botnet and other command control hosts
- Compromised Rules
	- its a list of known compromised hosts
- Current_Events Rules
	- most often these will be simple sigs for binary urls, sigs to catch CLSID of new found vulnerable apps where we dont have exploits 
	- most likely n'day attacks
- DOS Rules
	- catch inbound DOS activity, and outbound indications
- DROP Rules
	- daily updated list of spam haus DROP (dont router or peer) list. primary known for professional spammers
- DShield Rules
	- daily updated list of Dshield top attackers list
- Exploit Rules
	- Rules to detect direct exploits. thinigs like SQL injection etc
- Game Rules
	- online games sig
- Inappropriate Rules
	- Porn, Kiddy porn, sites you shouldn't visit at work
- Malware Rules
- P2P Rules
	- Peer to Peer Bittorrent etc 
- Policy Rules
	- rules for company or organization polic
- Scan Rules
	- detect reconnaissance (port-scanning , niko, nessus)
- VOIP Rules
	- A new/emerging ruleset.
- Web Rules
	- SQL injection
	- webserver overflow
	- vulnerable web apps
- Web-SQL-Injection Rules
	- Rules to prevent/detection SQL injections

----

*Snort Response*
---

> Depends on setup and equipment

- Snort IDS can be set up to become IPS 
- Observe to build new rules
- Data collection (additional option) 
- Automated active response tied to alert

---

*Snort Plug-ins*
----
Plug-ins are modular pieces of code that extend the basic  
functionality of snort

**Preprocessors**
- Examine packets before they are passed to the detection  engine

**Detection**
- Perform tests on a single packet, based on rules

**Output**
- Report results from preprocessors and detection engine


