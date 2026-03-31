# oss-audit-24BSA10228

**Topic:** The Open Source Audit: VLC Media Player 🎥🐧  
**Course:** Open Source Software (OSS NGMC) - Capstone Project  
**Student Name:** Arrnav Gupta  
**Registration Number:** 24BSA10228  
**Chosen Software:** VLC Media Player  

---

## 📖 Project Overview
This repository contains the practical technical component of "The Open Source Audit" capstone project. It includes a suite of five Bash shell scripts designed to demonstrate practical Linux system administration, automation skills, and an understanding of how open-source tools operate at the command line.

The accompanying written report (submitted via the VITyarthi portal) explores the origins, licensing (GPL/LGPL), FOSS ecosystem, and ethical philosophy behind **VLC Media Player**.

---

## 🛠️ The Scripts

Here is a breakdown of the 5 scripts included in this repository:

1. **`script1.sh` (System Identity Report)**  
   Acts as a welcome screen. It uses command substitution to display the Linux distribution, kernel version, currently logged-in user, system uptime, and a message regarding the OS's open-source license.
   
2. **`script2.sh` (FOSS Package Inspector)**  
   Checks whether **VLC Media Player** (and other key packages) is installed on the system. It uses `dpkg`/`rpm` to fetch the package version and utilizes a `case` statement to print a short philosophical note about the software's purpose.
   
3. **`script3.sh` (Disk and Permission Auditor)**  
   Loops through critical system directories (e.g., `/etc`, `/var/log`, `/usr/bin`). It reports how much disk space each directory uses alongside its owner and read/write/execute permissions.
   
4. **`script4.sh` (Log File Analyzer)**  
   Reads a specified log file line-by-line using a `while-read` loop. It counts how many lines contain a specific keyword (like `ERROR` or `WARNING`) passed via command-line arguments and prints a summary.
   
5. **`script5.sh` (The Open Source Manifesto Generator)**  
   An interactive script that prompts the user with three questions about their open-source usage and philosophy. It concatenates the answers to generate a personalized open-source manifesto and saves it to a `.txt` file.

---

## ⚙️ Dependencies & Prerequisites

To run these scripts successfully, your system should meet the following requirements:
* **Operating System:** A Linux environment (Ubuntu/Debian, CentOS/RHEL, or a compatible VM/WSL setup).
* **Target Software:** `vlc` should be installed to fully test Script 2.
* **Package Manager:** `dpkg` (Debian/Ubuntu) or `rpm` (RedHat/CentOS) available in the system path.
* **Standard GNU Utilities:** `awk`, `grep`, `du`, `uname`, `uptime` (these are pre-installed on almost all Linux distributions).

---

## 🚀 Step-by-Step Instructions to Run

### Step 1: Clone the Repository
Open your Linux terminal and clone this repository:
```bash
git clone https://github.com/luthentic484/oss-audit-24BSA10228/
```

### Step 2: Navigate to the Directory
```bash
cd oss-audit-24BSA10228
```

### Step 3: Grant Execution Permissions
Before running the scripts, you must make them executable:
```bash
chmod +x *.sh
```

### Step 4: Execute the Scripts
Run each script using the following commands:

**Run Script 1: System Identity Report**
```bash
./script1.sh
```

**Run Script 2: Package Inspector**
```bash
./script2.sh
```

**Run Script 3: Disk and Permission Auditor**
```bash
./script3.sh
```

**Run Script 4: Log File Analyzer**  
*Note: This script requires command-line arguments (the log file path and an optional keyword). You may need `sudo` to read system logs.*
```bash
# Syntax: ./script4.sh [path_to_log] [keyword]
sudo ./script4.sh /var/log/syslog ERROR
```
*(If you are on CentOS/RHEL, use `/var/log/messages` instead).*

**Run Script 5: Manifesto Generator**
```bash
./script5.sh
```
*Follow the interactive on-screen prompts. Once finished, check your directory for the newly generated `.txt` file!*
```
