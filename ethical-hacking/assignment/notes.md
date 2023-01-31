
identified hosts

```
Open 172.168.0.202:21
Open 172.168.0.203:21
Open 172.168.0.202:23
Open 172.168.0.1:53
Open 172.168.0.1:80
Open 172.168.0.203:80
Open 172.168.0.202:135
Open 172.168.0.201:135
Open 172.168.0.204:135
Open 172.168.0.202:139
Open 172.168.0.201:139
Open 172.168.0.204:139
Open 172.168.0.202:445
Open 172.168.0.201:445
Open 172.168.0.204:445
Open 172.168.0.1:853
Open 172.168.0.204:3389
Open 172.168.0.201:5357
Open 172.168.0.203:5985
```

```
172.168.0.201 - smb with guest enabled
172.168.0.202 - ethernal blue
172.168.0.203 - have a shell ftp
172.168.0.204 - 
```

scan results for 203 

![[attachments/Screenshot 2023-01-28 at 09.23.48.png]]

results for 204

![[attachments/Screenshot 2023-01-28 at 09.25.29.png]]


![[attachments/Screenshot 2023-01-28 at 09.29.25.png]]

---

172.168.0.202

![[attachments/Screenshot 2023-01-28 at 09.32.55.png]]

this vm is likely vulnerable go ethernal blue 

----

201 -> has a smb with guest enabled

![[attachments/Screenshot 2023-01-28 at 13.00.40.png]]


172.168.0.202 - 

this is vulnerable to ethernal blue we can use the ````use exploit/windows/smb/ms17_010_eternalblu```` module and exploit the vulnerability to get a shell on the victim machine

---

172.168.0.203

there is a ftp server and it has anonymous access enabled. the ftp server is actually the webserver root so if we upload a file to the ftp server we can access it from the webserver. 

we can upload a asp shell to the ftp and execute commands this way we can get a command execution

---

172.168.0.201 - smb with guest enabled

there is a smb server with guest enabled. we can access the users home folder which has some images, videos and etc 