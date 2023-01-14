- wifi authentication modes
    - open system authentication : gaining access to a network with a wired equivalent privacy protocol(WEP)protocol or no encryption
    {refer slide 8}
    - shared key authentication: only those wirless clients with shared key can connect. shared key authentication can only be used with WEP.
    {refer slide 9}
    - cetralized authentication : [single sign on protocol for the web] purpose is to permit a user access multiple web applications while providing their credentials only once.

- wifi encrytpion 
    - IEEE 802.11i :to facilitate secure end-to-end communication for (WLAN). [specify securtiy mechanisms for 802.11 networks]
    
    - Wired equivalent privacy: [oldest,most common and can be easily cracked]provide a wireless local area network (WLAN) with a comparable level of security to a wired local area network (LAN). {so that the outsiders not inside the encrypted network cannot infiltrate}
    
    - extensible authentication protocol: supports  multiple authentication methods.
             ex : kerberos,tokens,certificates,LEAP{CISCO

    - Wifi Protected Access : used temporal key integrity protocol(TKIP) and message integrity check(MIC)

    - WPA-2 upgrade to WPA 2 using AES and CCMP
	   
    - WPA-2 enterprise : integrates EAP
    - WPA 3 - galois/counter mode 256 for encrytion and HMAC SHA-384 for authetication.

- wifi threats - access control 
    - war driving : detect WLANS by listening or probe requests
    - mac spoofing : changing mac address of a network card.``


- tools used for recon. 
    - netstumbler [refer slide 15]
    - kismet [refer slide 16]
    - mapping accesspoints[refer slide 17]

- Wifi threats -integrity
    - WEP injection : constructing and sending forged WEP encrytpion keys
    - extensible AP replay : capturing the 802.1X EAP for later replay
    - intialization vector replay attacks: deriving the keystream by sending plain text message.

- wifi threats - confidentiality
    - traffic analysis : obtaining info. from traffic observation.
    - session hijacking : manipulating the network such that the attacker's host appears to be the desired destination
    - masquerading - pretending to be an authorized user.

- wifi threats -availability 
    - ARP poisoning : MITM attack allowing attackers to intercept comms. between network devices.
    - Denial of service(DOS): shutting down network with zombie requests to a server by flooding with zombie requests, which blocks legitimate users from accessing content.

- wifi attacks aircrack-ng suite
    - aircrack-ng: de facto WEP/WPA/2 PSK cracking tool
    - air drop -ng : targeted rule based de authentication of users.
    - airmon-ng: used to switch from managed to monitor mode on the wireless interface
    - easside-ng : communicate via a WEP encrypted AP without knowing the WEP key.

- detection of hidden SSID's 
        - run airmon-ng in monitor mode
        - start airdump-ng to discover hidden SSID's
        - de-authenticate the client to reveal the hidden SSID using Aireplay-ng
        - switch to airdump to view the SSID
        [refer slide 25]

- for WPS cracking use pixie dust [refer slide 26]

- WPA cracking - Wi-Fi attacks 
        -run airmon-ng in monitor mode
        -collect traffic using airdump
        -deauthenticate the client
        [refer slide 27]
        -execeute file through aircrack-ng

