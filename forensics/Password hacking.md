- passwords need to be secured inorder for not to be stolen
- levels of protection,
         - store password(clear text)
         - store hashed password
         - store hashed salted password
         - store hashed salted password in an encrypted database file

- passwords are the key to acessing encrypted files
---
- encryption modes
        -full disk encryption : protecting information by encrypting all the data on the disk,including temporary files,programs and system files.
        - by doing MBR analysis can identify the number of partitions on the disk
        - MBR loads the OS to the main memory
                - into the RAM
        - some h/w based encryptions can encrypt the whole MBR as well.

-full disk encrytpion
        - bitlocker is an encryption mechanism which encrypts drive and prevents unauthorized access
                - uses AES and CBC (128 and 256 bit)
                - CBC used on each individual sector.
                - three modes of bitlocker(or combined),
                             - Transparent operation mode 
                             - user authentication mode
                             - USB key mode
        - file vault is a disk encryption as same as bitlocker

[bitlocker and efs can be used in conjunction]

-File system encryption
        -the encryptedd file system provides security for the NTFS file system[uses public key system]
                - the EFS system uses user password to keep the private key secret to protect the file.
                - encrypts the file content not the metadata.

-Application-level encryption 
        -FTK(forensic toolkit) 
                -FTK supports in finding deleted emails ,scanning disk for text strings(to crack encryptions)
        -Password recovery toolkit
                -helps in recovering passwords and useful in dealing with encrypted data[ophcrack]

---
- capturing password
        - ask the suspect
        - written down - looking for physical and logical evidence
        - try any used passwords-people tend to reuse passwords
        - searching for stored passwords on the ram
                 - truecryptdisk encrytion held the master key in the ram
                 - password is stored in RAM for the OS for validation purposes
                 - passwrods are stored in clear text



---
- standard attack scenarios 
        -dictionary attacks 
            breaking into  a password protected computer by entering every word in the dictionary as a password
        -rule based attacks
            attacking by knowing the rules in the system
        -brute force attacks
             submitting and guessing many passwords until authenticated.

---
- rainbow tables 

-can reverse hash functions  by using precomputed tables (rainbow tables contains them)

-need to produced for each hashing algorithm
        -salting is an effictive measure to prevent this.
