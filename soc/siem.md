*Security information and event management*
=

*What is SIEM?*
---

there are 2 basic technologies

- SIM  - security information management
	- log collection, report generation
	- examples : pcapfiles, wireshark
- SEM - security analyses management
	- analyze the event using event correlations and alert mechanisms
	- examples: IDS, IPS

> SEIM combines SIM and SEM capabilities , together it provides network security intelligence in real time

|          | Security Information Management                            | Security Event Management                                      | Security information and event management |
|----------|------------------------------------------------------------|----------------------------------------------------------------|-------------------------------------------|
| Overview | collection and analysis of security related data from logs | Real-time threat analysis, visualization and incident response | Combines SIM and SEM                      |
| Features | easy to deploy, strong log management                      | complex to deploy, good at real-time monitoring                | complex to deploy, complex functionality  |
| Examples | OSSIM                                                      | NetIQ Sentine                                                  | SolarWindsLog & Event Manager             |


### *SIEM system generally provides following collection of services*

- log management
- IT regulatory compliance  
- Event correlation  
- Active response  
- Endpoint security

---

*Why is SIEM needed*
----

- risk of data breaches are increasing
- attackers adaptive and often try to innovative
- mitigate / detect attacks
- manage increasing volumes of attacks , logs and log sources
- meet compliance requirements

----

*How SIEM works ?*
---

![[attachments/Screenshot 2023-01-07 at 04.26.34.png]]

---

*Choosing SIEM Solution*
---

there are some stuff we need to consider when choosing a SIEM solution

- **log collection**
	- there are universal log collection
	- event collection rate (per second EPS) shorter or longer 
- **activity monitoring**
	- can monitor user activity ? (legit or attacker)
	- privilaged user monitoring (PUMA) 
	- SIEM solutions usually have out-the-box user monitoring 
		- In-the-box in cases of tampering
	- example data collects
		- which user performed ...
		- what action 
		- what device / server
		- where was the action triggered
		- when was the action triggered
- **real-time event Correlation**
	- helps to prioritize and remediate threats
		- boost network security by processing millions of events to detect certain behaviours
	- Correlation can be based on log search, rules and alerts
		- Predefined rules and alerts is a good first step , not sufficient
		- customer rules and alert builder (IDS/IPS)
- **log retention**
	- should automatically archive log data from system
	- repositories tend to centralised (log repos)
	- log process should be "tamper proof" , with encryption, time 
	- valid user should be able to retrieving/analyze data
- **IT compliance reports**
	- ensure that SIEM solution has regulatory compliance reports
	- SIEM solutions should be flexible to build compliance records
- **file integrity monitoring**
	- helps to watch files/folders 
	- things to track
		- created
		- accessed
		- viewed
		- deleted
		- modified renamed
- **log forensics**
	- SIEM solutions should allow users to track down intruders
	- log search should be easy and user friendly 
	- should allow admins to search though logs quickly 
- dashboards
	- help admins take timely action and make decisions during network anomalies
	- users find custamizable dashboards useful
	- data should represent intuitive format to reduce stress


---

*SIEM Best Practices*
---

**Defining SIEM requirements:**

- defined requirements for monitoring, reporting and auditing before deploying a SIEM
- determine scope of the SIEM 
	- which part of infra it will cover 
	- necessary credentials
	- log verbosity
- Define audit data
	- accessibility
	- retention
	- data integrity
	- disposal of old data
	- evidentiary rules

**Make sure SIEM to monitor and report following**

- Access monitoring
- Perimeter defences
	- possible attacks
	- risky config changers
- Resource integrity
	- cirtical network resources 
	- example
		- status
		- backups
		- change management 
		- threats and vulnerabilities
- Intrusion detection
	- incidents reported by intrusion detection
	- correlated/inferred using SIEM data
- Malware defence
- Application defences
	- status
	- config changers 
	- violation and a anomalies for webservers, dbs

----

*Next Gen SIEM*
---

next gen SIEM provides more features 

- User Event Behavioural Analysis (IBEA)
	- using AI to look at patterns of human behaviour. this can help to detect insider threats, targeted attacks, and fraud
- Security Orchestration and Automation (SORT)
	- automate incident response.
	- example
		- SIEM might detect alert for ransomeware and take steps automatically on affected system before attacker encrypt data


---

*Networking example: Varonis*
---

- Varonis can capture file event data from multiple data sources (cloud, on-prem)
	- can log who, what, when, and where of each file access on network
- Varonis also collects DNS, VPN, webproxy activity 
- behavior analytic (UBA) to provide alerts based on learned behavior of users

---

*The Job(s)*
---

Computer Security Incident Response Teams (CSIRTs) describe tools , procedures and roles needed to implement the system

- good team has right mix of people 
- balance between workforce talent and right security tools
- services can be provided in-house or outsourced to external proviers 
- CSIRT is a part of SOC. 
	- soc is a group responsible for overall IT security
		- security policies
		- compliance
		- governance
		- security systems and applications


