## Header-Footer Carving

- Carving using distinct byte patterns signifying the start and end of a file
- Assumes the file is not fragmented; and fragmented files may be partially extracted

### the process

- scan for the header of file type `0xFFD8`
- scan for file type footer
- bytes between the header and footer is likely to be a file
- copy the bytes to a file

---
