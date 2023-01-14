- An APT can be known as a stealthy threat actor which has unauthorized access to a network or a system

- Goals of an attacker
	-Disrupt business activities.
	-Create financial loss.
	-Create reputational damage.
	-for black mailing purposes.
	
     - the importance to consider this is to strengthen the digital infrastructure of an organization.
	

- classification of attacks
    -passive attacks : monitoring the network without tampering the data.
    
        examples : sniffing,network traffic analysis
    -active attacks : tampering data in transit.
    
        examples : Denial of service,malware
    -insider atttacks: trusted individuals with physical/logical access.
    
        examples :Social enginnering,theft
    -close in attacks: close physical proximity to the attacker
    
        examples: social enginnering,dumpster diving
    -distribution attacks: attacks done with tampering with hardware and software before distribution.
    
        examples :modifying during production,modifying during distribution

- cyber kill chain - made to aid security proffesionals to identify steps adversaries will follow.
    1.reconnaisance : harvesting information.
    2.weaponization : coupling exploit with backdoor and payload.
    3.deleivery : sending the attack to the victim.
    4.exploitation: executing malicious code on victim.
    5.installation : installing malware.
    6.command to control : remote access for the victim
    7.action on  objectives: accomplishing intruder goals.

- information warfare : using information as a competitive advantage.
    -cyber warfare 
    -economic warfare
    -electronic warfare
    -hacker warfare

- TTP refers to the pattern of activities and methods used by threat actors.
    -tactics : how a threat actor operates.
    -techniques : tools and texhniques used.
    -procedures: actions performed.

- identifcation of adversary behaviour identification 
    -usage of powershell
    -usage of HTTPS user agent
    -usage of DNS tunneling
    -usage of web shell

-  an IOC can be known as the evidence left by an attacker.
    -Unusual no.of DNS requests.
    -Large HTML response size
    -Multiple login failures
    -unusual outbound traffic

- types of ethical hackers,
    -Black hat: use of skills for illegal purposes
    -White hat: use of skills for defensive purposes
    -gray hat: use of skills for offensive and defensive purposes
    -cyber terrorist: attackers motivated by religious and political beleif
    -script kiddies: unskilled hackes using automated tools and scripts.

- common hacking phases 
    -reconnaisance:  gather information
        - (OSINT [ passive approach-open source intelligence]) 
         - (social enginnering,dumpster diving [active approach])
    
        example: whois,nslookup

    -scanning : using information from reconanaisance.
        purpose:
            - identify live machines.
            - open ports
            - active services
            - vulnerabilities

     -gaining access : exploiting the network/system.
        -password cracking
        -buffer overflow
        -session hijacking

     -maintaining access: usage of backdoors,rootkits and trojans
     [pivoting; ustilizing an attack platform to scan and exploit other systems]

    -clearing tracks: removing evidence of the attack (using stegonography and tunneling)


- gathering knowledge of various threats is cyber threat intelligence.
    -identidy objectives
    -application overview
    -application decompose
    -identify threats
    -identify vulnearbilties