
- scanning is gathering detailed information by using highly complex reconnaisance techniques.
         - network scanning refers to identifying hosts,ports and services in a network.
          [also for identifying active machines and identify OS running on targets]
              purpose is to identify;
                  - discover exploitable communiation channels
                  - probe listeners.
                  - track users

- types of scanning 
    port scanning - identify open ports and services
    network scanning - identifying active hosts and ip addresses.
    vulnerability scanning - identifying vulnerabilities.

- tcp flags are used to indicate a particular state of connection,
     -FIN
     -RST
     -URG
     -PSH
     -SYN

- scanning tools,
    -Nmap: network exploration and hacking
        can be used as command line or GUI[nmap]
    -Hping2/3: scanner and packet crafting tool   
    
    
     - metasploit : 
         -automate pen tests
         -security auditing
         -command line tool
    - netscan tools pro:
        -GUI tool for troubleshooting,monitoring etc...
        

- Nmap opitimization techniques,
    - reduce scope to scan faster.
    - choose favourable location

- OS discovery is of two types, [banner grabbing is gaining information about a computer system on a network]
        -active banner grabbing : send packets to remote data and analyze response
        -passive banner grabbing: capture packets from target host via sniffin.

             - counter measures for banner grabbing,
                -disable or change banner
                -hide file extensions from web pages

- evasion techniques for IDS and firewall (evading the IDS and firewall)
    -proxy servers [intermediary server that retrieves data from an Internet source]
            - used for anonymity
            - use proxy chaining for evasion
    -custom packets [crafting packets for attacking and exploitation purposes.]
    -spoofing [sendfing packets as to appearing coming from a different IP address] 
              - cannot complete successful TCP 3 way handshake and open a connection.


<refer slide 10>
