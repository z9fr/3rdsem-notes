architecture of web server

```
|user|  <-> |webserver| <-> |application-server| <-> |database|
```

<u>example oss web server architecture</u>
- LAMP - linux, apache, mysql, php
- ISS -> internet information service (micorosft)
	- webserver, ftp, ftps , smtp, ntp


### components of a webserver

- document root - root folder which stores html files
- server root - server root which store cofig files
- virtual document tree - alternative storage if original storage is full
- virtual hosting - hosting multiple domains in one server
- web proxy - proxy between server / client


---

### Attacking rationale and impact

- get credentials
- obtain closed source application
- db compromise 
- escalating privilages 
- damage reputation

### why attack ?

- curiosity
- damage reputation

### who (targets) ?

- webmaster
	- more access to infra
- network admin
	- more risk to LAN security

---


## Attack options

- [unpatched] security vulnerabilities
- poor config
- poor security restrictions
- DOS
- DNS attacks
- Directory transversal
- MITM
- Phishing
- web cache poisoning
- ssh bruteforce
- password cracking
- ssrf


## web appliation attacks

- sql injection
- ssrf
- cookie tampering
- xss
- dos
- csrf
- session hijacking


