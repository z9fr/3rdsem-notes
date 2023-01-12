*Header Options*
--

- Action (e.g. alert, pass, log, activate)
- Protocol (e.g. tcp, ip, icmp, udp)
- Source-destination IPs
	- any
	- multiple ips - `192.168.1.10/32, 192.168.1.0/24`
	- multiple ip list - [192.168.1.0/24,10.1.1.0/24]
- source port
	- any
	- port number - 80
	- port range - 1024:2048
	- port exclusion - !80


---

*Rule Options*
--

- `msg` -> title of the alert
- `content` -> text within packet payload

#### *Content matching*

- `offset` - Specifies offset from the beginning of the payload.
- `depth` - Specifies data from initial offset to be searched in the packet
- `distance` - distance from the end of last match 
- `within` - amount of data from the end of the last match, that the next match should use 

---

*Examples*
---

the pattern matcher will search for the string `USER` in packet payload. Then, it will start searching for the string `anonymous`, at 1 byte distance from the end of last content match

```php
alert tcp any any -> any 21 \ (content: 'USER'; content: 'anonymous'; distance: 1;  msg: 'Got anonymous FTP login';)
```

the pattern matcher will search for the string `USER` in packet payload. Then, it will start searching for the string `anonymous`, at 1 byte distance from the end of last content match

```php
alert tcp any any -> any 110 \ (content: 'USER'; nocase; content: !'|0A|'; within: 256; msg: 'POP Username too long, possible overflow';)
```

----

http uri content

if we want to search for something in a url we can use `uricontent`. if we want to alert if someone access `/admin.php` file we can create a rule 


```php
alert tcp any any -> any 80 (flow:to_server,established; uricontent:'/admin.php'; nocase; msg: 'admin.php file accessed';)
```