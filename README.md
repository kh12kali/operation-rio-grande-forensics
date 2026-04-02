# Operation Rio Grande — Digital Forensic Investigation

**Type:** Digital Forensics · Criminal Case Investigation  
**Tools:** Autopsy · FTK Imager · WinRAR · OpenPuff · HxD · Windows Registry Recovery  
**Report Format:** Court-ready forensic report (PACE guidelines)

---

## Case Overview

A forensic investigation conducted on behalf of a police hi-tech forensics unit.  
The suspect, Joe Sins, was arrested in connection with an armed robbery.  
A laptop was seized from his home and a forensic image was taken for analysis.

My role was to examine the forensic image, recover and analyse all relevant evidence,  
and produce a formal report suitable for court proceedings.

---

## What I Did

### Evidence Preservation
- Verified the integrity of the forensic image using MD5 and SHA1 hashes
- Confirmed hashes matched the original before beginning analysis
- Documented full chain of custody from seizure to investigation completion

### Disk & File System Analysis
- Identified operating system, file system type (NTFS), partition layout
- Extracted user account details, last logon times, and SID information
- Analysed startup programs and recently accessed files (MRU)

### Document & Evidence Recovery
- Located and analysed 20+ files of interest including text files, documents, spreadsheets, and executables
- Recovered hidden address data concealed inside an Excel spreadsheet
- Identified and read encrypted text files by changing file extensions manually

### Password Chain Cracking
- Found password 1 hidden inside JPEG metadata (`f00tb4llm4d`)
- Used it to run `main.exe` which revealed password 2 (`d3l3 A11i`)
- Discovered password 3 via MD5 decryption of `My ID.rtf` (`letsgetrich`)
- Used passwords to access RAR archive and password-protected ZIP folder

### Steganography Detection
- Identified use of OpenPuff and VeraCrypt encryption software on device
- Located OpenPuff password hidden inside a football stats document
- Flagged encrypted files requiring further decryption

### Web & Timeline Analysis
- Reconstructed suspect activity timeline using Autopsy timeline tool
- Identified browser searches related to knives and the victim's watch
- Found British Museum alibi enquiry with no proof of booking

### Image Forensics
- Catalogued and categorised 15+ images of interest
- Identified illegal content (Category A and Category C) with proper documentation
- Cross-referenced images with suspect's known interests

---

## Key Findings

| Evidence | Significance |
|---|---|
| `bazzer.txt` | Chat logs discussing the robbery plan, victim's address, and watch |
| `The Terminator.xlsx` | Contained victim's exact address and date of offence — hidden in white text |
| `Payment Plan.rar` | Password-protected archive containing knife images |
| `my stuff.zip` | Contained illegal images, conversation about selling stolen watch |
| `Kanes watch.PNG` | Image of victim's stolen watch found on suspect's account |
| `main.exe` | Custom application concealing a password — evidence of planning |
| `My New Hat.jpg` | Image of male in green hat matching suspect description |

---

## Tools Used

| Tool | Purpose |
|---|---|
| Autopsy 4.17.0 | Primary forensic analysis — file tree, keyword search, timeline |
| AccessData FTK Imager 4.3.0.18 | Hash verification and disk imaging |
| WinRAR 6.11 | Accessing password-protected archives |
| OpenPuff 3.4 | Steganography analysis |
| Windows Registry Recovery | Registry and user account analysis |
| HxD Hex Editor | Manual file inspection |

---

## Skills Demonstrated

- Chain of custody documentation
- Disk image integrity verification (MD5 / SHA1)
- Timeline reconstruction
- Password cracking and decryption chain
- Steganography detection
- File system and registry analysis
- Court-ready forensic report writing
- Evidence categorisation and legal compliance

---

## Files in This Repository

- `Operation_Rio_Grande_Report.docx` — Full forensic investigation report
- `README.md` — This file

---

*Conducted as part of cybersecurity and digital forensics training.*  
*All case materials are fictional scenarios used for educational purposes.*
# operation-rio-grande-forensics
