# Linux Learning Journey 🐧

Daily progress while learning Linux from zero for a 
career switch to Cloud / IAM Engineering.

**Start Date:** April 2026  
**Target Role:** Azure Cloud Support Engineer / IAM Analyst  
**Target:** Rs.10-14 LPA  
**Certifications Planned:** AZ-900 → AZ-104 → SC-300  

---

## Progress Tracker

| Day | Date | Topics Covered | Status |
|---|---|---|---|
| Day 1 | April 2026 | Linux Basics + Navigation + File Commands | ✅ Done |
| Day 2 | Upcoming | Text-Fu — stdout, stdin, pipes, tee | ✅ Done |
| Day 3 | Upcoming | Permissions — chmod, chown | ⏳ Planned |

---

## Day 1 — Linux Basics + Navigation + File Handling

### 1. GNU
- GNU stands for **GNU's Not Unix**
- Free and open-source project
- Provides essential tools — compilers, editors, utilities
- GNU tools + Linux Kernel = Complete Operating System

### 2. Kernel & Linux Kernel
- Kernel = Core of the operating system
- Responsibilities: manages hardware, memory, processes, devices
- Linux Kernel created by **Linus Torvalds**
- Acts as bridge between software and hardware

### 3. Shell & Bash
- Shell = Command-line interface to interact with system
- **Bash** (Bourne Again Shell) = default shell in most Linux systems
- Shell interprets commands → sends to kernel → executes

### 4. Filesystem & Paths
- Linux uses hierarchical filesystem starting from **/** (root)
- All files and directories live under this structure
- **Absolute path** — starts from / → example: /home/saksham
- **Relative path** — based on current directory → example: ../folder

---

### 5. Navigation Commands

| Command | What It Does | Example |
|---|---|---|
| `pwd` | Print current working directory | `pwd` → /home/saksham |
| `cd` | Change directory | `cd /mayank` |
| `cd ..` | Go to parent directory | `cd ..` |
| `cd ~` | Go to home directory | `cd ~` |
| `cd -` | Go to previous directory | `cd -` |
| `ls` | List files and directories | `ls` |
| `ls -l` | Detailed list with permissions | `ls -l` |
| `ls -a` | Show hidden files too | `ls -a` |
| `ls -r` | Reverse order listing | `ls -r` |

---

### 6. File Handling Commands

| Command | What It Does | Example |
|---|---|---|
| `touch` | Create empty file or update timestamp | `touch myfile.txt` |
| `file` | Identify actual file type | `file myfile.txt` |
| `cat` | View file content / create file | `cat file.txt` |
| `less` | View large files page by page | `less bigfile.txt` |

---

### 7. File Operations

| Command | What It Does | Example |
|---|---|---|
| `cp` | Copy files | `cp file.txt backup.txt` |
| `cp -r` | Copy directories recursively | `cp -r folder/ backup/` |
| `cp -i` | Ask before overwriting | `cp -i file.txt dest/` |
| `cp -p` | Preserve file attributes | `cp -p file.txt dest/` |
| `mv` | Move or rename files | `mv old.txt new.txt` |
| `mkdir` | Create directory | `mkdir saksham` |
| `mkdir -p` | Create nested directories | `mkdir -p saksham/dileep/veena` |
| `rm` | Delete file permanently | `rm file.txt` |
| `rm -rf` | Delete folder and contents — USE CAREFULLY | `rm -rf file1.txt/` |

---

### 8. Search

| Command | What It Does | Example |
|---|---|---|
| `find` | Search files and directories | `find / -name "*.txt"` |
| `find -type f` | Search only files | `find . -type f` |
| `find -type d` | Search only directories | `find . -type d` |

---

### 9. Productivity Commands

| Command | What It Does | Example |
|---|---|---|
| `history` | Show all previously run commands | `history` |
| `help` | Info for built-in commands | `help cd` |
| `man` | Detailed manual for any command | `man ls` |
| `whatis` | One-line description of command | `whatis pwd` |

---

### 10. Session Management

| Command | What It Does |
|---|---|
| `exit` | Close current shell session |
| `logout` | Used for login shells specifically |

---

## 💡 Key Insights From Day 1

> ⚠️ **Linux has NO recycle bin** — `rm` is permanent and irreversible  
> 📄 **File extensions do NOT define file type** — use `file` command to check  
> 🔗 **Commands can be combined with flags** — example: `ls -la`  
> 💪 **Practical usage is essential** — reading alone is not enough  

---

## Day 2 — I/O Streams + Redirection + Pipes

### What I Learned:
- stdout → normal output (screen)
- stdin → input to command
- stderr → error output
- > overwrites file
- >> appends to file
- < takes input from file
- | (pipe) connects commands
- tee → output to both screen and file

---

### Commands Practiced:

| Command | What It Does | Example |
|---|---|---|
| > | Redirect output (overwrite) | echo Hello > file.txt |
| >> | Append output | echo Hi >> file.txt |
| < | Take input from file | cat < file.txt |
| 2> | Redirect error | ls fake 2> error.txt |
| 2>&1 | Combine stdout + stderr | ls fake > out.txt 2>&1 |
| &> | Redirect both outputs | ls fake &> all.txt |
| \| | Pipe output | ls \| less |
| tee | Save + display output | ls \| tee file.txt |

---

### Hands-On Practice:
- Created files using echo and >
- Overwrote and appended content
- Used < to copy content between files
- Captured errors using 2>
- Combined stdout and stderr
- Used pipe with less
- Used tee to store output

---

### Key Insight:
- Linux commands become powerful when combined
- Redirection gives control over data flow
- Pipes allow chaining commands efficiently
---

## 📚 Resources I Am Using

| Resource | Link |
|---|---|
| Linux Journey | linuxjourney.com |
| OverTheWire Bandit | overthewire.org/wargames/bandit |
| JSLinux Browser Terminal | bellard.org/jslinux |
| NetworkChuck YouTube | youtube.com/@NetworkChuck |
| Microsoft Learn | learn.microsoft.com |

---
