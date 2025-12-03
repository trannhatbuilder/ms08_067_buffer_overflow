# 📘 Researching Metasploit Framework & Developing a Buffer Overflow Exploit Module

## 🚀 Overview
This project focuses on researching the **Metasploit Framework** and developing a custom **exploit module** targeting a buffer overflow vulnerability. The module provided demonstrates an exploit for **MS08-067**, specifically tailored for **Windows Server 2003 SP2 English (NX enabled)**.

The project showcases:
- Understanding of Metasploit module structure
- Crafting payloads and ROP chains
- Implementing SMB and DCERPC communication
- Bypassing NX (No-eXecute) protections
- Triggering a real-world stack corruption vulnerability

---

## 🧩 Features
- 🔧 **Custom Metasploit exploit module** written in Ruby
- 🧱 **NX bypass chain** using carefully selected ROP gadgets
- 📡 **SMB authentication & DCERPC interaction**
- 🎯 Tested against **Windows Server 2003 SP2 (NX)** in lab environment
- 🛠 Includes path canonicalization exploitation logic found in `NetAPI32.dll`

---

## 📂 Module Structure
- `initialize`: Defines metadata, payload options, references, and targets
- `check`: Determines if the remote host is running a vulnerable service
- `exploit`: Performs SMB login, constructs the malicious path, triggers the overflow, and runs the payload

---

## 📝 Requirements
- Metasploit Framework installed
- Windows Server 2003 SP2 English (NX) as the target
- SMB access credentials
- Lab or isolated environment (⚠️ critical for safety)

---

## 🕹️ Usage
Place the exploit module in:
```
~/.msf4/modules/exploits/windows/smb/
```
Then run:
```
msfconsole
use exploit/windows/smb/ms08_067_custom
set RHOST <target_ip>
set SMBUser <username>
set SMBPass <password>
run
```

---

## 📚 References
- CVE-2008-4250
- Microsoft Security Bulletin MS08-067
- Research documentation from Rapid7

---

## ⚠️ Disclaimer
This exploit is intended **strictly for educational and research purposes**.  
Do **NOT** use it on systems you do not own or without explicit permission.

---

## 👨‍💻 Authors
- 🧑‍💻 NHAT

---

## ⭐ Goal of the Project
To provide a practical study of:
- Metasploit internals
- Exploit development methodology
- Real-world vulnerability exploitation
- Modern defense bypassing (NX/DEP)

This project helps students and security researchers gain hands-on experience in low-level exploit development.
