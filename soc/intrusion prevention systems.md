
IPS record information related to events and notifiy admins. IPS also respond to detected threat by attempting to prevent it from succeeding. as a example by droping connection

## *Network-based IPS*

> Monitors the entire network for suspicious trraffic by analyzing protocl activity

 <u>2 types of NIPS</u>

- network based IPS
	- its like a intersection of firewall with IDS capabilities
	- it uses 2 network interfaces (internal, external)
		- packets appearing in interfaces are passed to detection engine
		- accepted packets forwared to the second interface
		- bad packets are discarded
- Rate-based IPS
	- known as attack mitigators
	- monitor traffic flows
	- look for dos attempts , scan attempts 


#### *Advantage and Disadvantages of NIPS*

| Advantages                                        | Disadvantages                                                             |
|---------------------------------------------------|---------------------------------------------------------------------------|
| Can prevent attacks before they reach destination | Require careful planing because it has a high impact on the network infra |
| Easier to manage                                  | Can be targeted as a part of the attack                                   |

---

## *Host-based IPS*

- Runs inside the OS kernal and services
- Intercepts requests to the system
- Monitor syscalls, and blocks ones that cause malecious behaviour 
- Application level protected by inspecting data streams and env specific config


#### *Advantage and Disadvantages of HIPS*

| Advantages                                    | Disadvantages                                            |
|-----------------------------------------------|----------------------------------------------------------|
| Usually performs misuse and anomaly detection | OS updates might break the IPS                           |
|                                               | Since it intercepts request can cause performance issues |


---

*IPS pros and cons*
--
| Advantages               | Disadvantages                           |
|--------------------------|-----------------------------------------|
| Can respond in real time | Can introduce overhead                  |
|                          | Can represent a single point of failure |
|                          | Can deny legit requests                 |


*Addressing IPS challenges*
----

#### *Single point of failure*

- use backup IPS 
	- can be expensive
- redirect traffic around IPS 
	- does not provide protection against attacks
- Pre-configure IPS with minimum capabilites allowing traffic to pass (fail-open)
	- does not provide protection against attacks

#### *False alams*

- Respond only to alarms with high certainty
	- can be applicable to only small set of alams
