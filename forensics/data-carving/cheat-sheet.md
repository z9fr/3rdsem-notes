## Header-Footer Carving

- Carving using distinct byte patterns signifying the start and end of a file
- Assumes the file is not fragmented; and fragmented files may be partially extracted

### the process

- scan for the header of file type `0xFFD8`
- scan for file type footer
- bytes between the header and footer is likely to be a file
- copy the bytes to a file

![[attachments/Screenshot 2023-01-13 at 02.12.28.png]]

---

## Header-Maximum File Size Carving

- Carving a fixed number of bytes from the beginning of a possible file
- 