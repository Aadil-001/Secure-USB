# Secure-USB Notepad

A portable USB-based logging application thats written in Python, which allows you to create, view, and search timestamped notes directly on a USB drive. Includes **integrity verification** with SHA-256 and **tamper detection with forensic logging**.

---

## Features
- Add and view notes (`notes.txt`) directly on the USB
- Search notes by keyword or date (`YYYY-MM-DD`)
- SHA-256 (cryptographic hash function) file integrity verification
- Tamper detection with forensic logging (`tamper.log`)
- Friendly menu interface:
  - [1] Add note  
  - [2] View notes  
  - [3] Search notes  
  - [4] Verify integrity  
  - [5] View tamper log  
  - [6] Quit  

---

## 📂 Project Structure

Repository contents:

```text
Secure-USB/                 # Repository root
├── Project1.py             # Main Python script (USB Secure Notepad with tamper log)
├── README.md               # Project documentation
├── LICENSE                 # MIT license
├── .gitignore              # Git ignore rules

```
Files created on the USB drive (e.g., USB-1) at runtime:
```
USB-1/                      # USB root
├── notes.txt               # Stores all notes (timestamped entries)
├── notes.sha256            # Baseline hash of notes.txt for integrity verification
├── tamper.log              # Records tamper events (hash mismatches, user, system info)
```

---

##  Usage
1. Plug in your USB (e.g., `USB-1`).
2. Run the program:
   ```bash
   python3 Project1.py
