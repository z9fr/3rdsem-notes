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
- Procedures
	- scan the header for a file type
	- extract the fixed number of bytes from a point 
- Useful for files with fixed length

---

## Header-Embedded File Length Carving

> based on the size of file embedded in the first few bytes of the file

procedures
- scan for the file header
- once found , determine the file size
- extract bytes

this will not work on fragmented files

---

## File Structure based Carving

> using the knowladge of file internal strucutre, as a example header footer and size

Procedures  
• Look for header  
• Find first start of section  
• Look for section size  
• Next section, next, next ...  
• Look for footer if no section

### example

- JPG has signature `OxFFD8`
- FF DA is the section marker for the
- ends with `FF D9` 

(dont think very important it just says look for the head and tail of the file)

----

## Bi-fragment Gap Carving

- Users object validation

procedure 

- identify header and footer blocks
- assume one external block exists
- construct files and use object validation
- assume two external blocks exist and repeat

----


