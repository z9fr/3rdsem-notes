#ids

*What is IDS ?*
---

An **Intrusion Detection System (IDS)** is a system that monitors **network traffic** for suspicious activity and issues alerts when such activity is discovered.

### *Roles of a IDS*

- Access control 
- identification and authorization
- encryption
- firewall

### *IDS Classification*

IDS can be classified accoding to three factors
- source -> place where data is collected
- detection mechanism ->  anaylze the collected data to detect potential intrusions
- response mechanisms -> triggers as a result of generated alerts

----

## *Types of IDSs*

**Network-based IDS (NIDS)**
- Examins the network traffic. 

**Host-based IDS (HIDS)**
- users os audit trails and system logs as information sources

**Protocol-based IDS (PIDS)**
- lives infront of the webserver, it controlles and intercepts the protocol between user and server
- it tries to secure the webserver by monitoring HTTPS protocol 

**Application Protocol-based IDS (APIDS)**
- lives within a group of servers. it identifies intrusions by monitoring and interpreting communication on application specific protocls. 
- example: this can monitor SQL protocol

**Hybrid IDS**
- combine two or more sources mentioned above 

---

## *Detection Method of IDS*

#### **<u>Signature-based (Misuse)</u>

- detects the attacks on the basis of the specific patterns
- detects on the basis of already known malicious instruction sequence

can easily detect the attacks whose signature is already exist, but its quite difficult to detect new malwhere where signature is unknown

#### <u>Anomaly-based Method</u>

- used to detect unknown malware
- it usually compairs the baseline and the current behavious and detects if its bad or not
- high rates of false positives 

baseline - how the system normally behaves

| Anomaly Detection                                            | Signature Detection                                    |
|--------------------------------------------------------------|--------------------------------------------------------|
| false positives                                              | better at detection                                    |
| takes lot of time to train                                   | do not require training                                |
| can detect new attacks                                       | needs to update the signatures to detect new attacks   |
| can serve as a source of information for signature detection | can fail to detect variants of already defined attacks |

----

*Responsve Mechanisms*
--

- Active
	- counters the incident itself ( blocks the attack )
- Passive 
	- notifies other parties ( admins, sms , notification , email )
	- rely on other parties to take a action 
	- IDS are passive 

[[improving detection]]

