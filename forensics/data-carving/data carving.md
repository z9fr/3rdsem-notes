```toc
```

## *Disk File Systems*

- Macintosh File System (MFS)
- File Allocation Table (FAT)
- Encrypting File System (EFS)
- New Technology File System (NTFS)

## *Network File Systems*

- AppleShare
- Network File System (NFS)
- Global File System (GFS)
- Server Message Block (SMB)

---

### *Windows and DOS File Systems*

- Main windows and DOS systems
	- FAT32
	- NTFS
- FAT file system
	- file system used with DOS
	- first file system used with windows (FAT12)
- Boot sector in FAT
	- First sector (512 bytes)
	- In UNIX, called the superblock
- its possible to recover files using forensic tools

---

## *New Technology File System (NTFS)*

- high performance and repairs itself
- supports file-level security, compression, and auditing
- supports large and powerful storage solutions

### Features

- NTFS provides data security
- Fault-tolerant file system
- uses 16-bit unicode character set to name files and folders

----

## *NTFS Structure*

### NTFS Master File Table (MFT)

- store info about file attributes 
- when NTFS volume increase, size of MFT increases
- NTFS reserves space for the MFT to maintain it as it expands

### NTFS Metadata File Table (MFT)

- database consists of information about file attributes
- create record if new file/folder is created on volume
- MFT store information related to files in the form of attributes
- rows consist of file records, and columns has file attributes


Structure of a master file table on an NTFS volume

![Alt Text](http://ntfs.com/images/screenshots/NTFS-MFT-structure.gif)


## *NTFS Security*

### NTFS Encrypting File System (EFS)

- users symmetric encryption with public key technology
- user is supplied with digital certificate with a public key pair
- encryption is done by gui
- file encryption certificate is used when encryption

---

## *Magic numbers*

> file signature is a const used to identify file format

- usually present in the ehader
	- JPEG – Starts with `0xFFD8`
	- PDF – Starts with `0x25 00 50 00 44 00 46` ``%PDF`
- maybe ends as a footer or tail
	- PEG – ends with `0xFFD9`
	- PDF – ends with `0x0A 25 25 45 4F 46` `.%%EOF`

---

## *Data Carving*

> process of reassembling files from fragments in the absence of file systems metadata, can be useful in storage media recovery


### Data carving types

- simple
	- the beginning of the file is not overwritten
	- the file is not fragmented
	- file is not compressed
	- file signatures are not common contents
- advance
	- the file is fragmented
	- file is out of order
	- parts of the file is missing 

![[attachments/Screenshot 2023-01-13 at 01.58.48.png]]

