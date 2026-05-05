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
| Day 2 | April 2026 | Text-Fu — stdout, stdin, pipes, tee | ✅ Done |
| Day 3 | May 2026 | env, cut, paste, head, tail | ✅ Done |
| Day 4 | May 2026 | Text Processing + File Analysis (expand, join, split, sort, tr, uniq, wc, nl) | ✅ Done |
| Day 5 | May 2026 | grep (Search & Filtering + Pipes) | ✅ Done |
| Day 6 | Upcoming | Permissions — chmod, chown | ⏳ Planned |

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
| `rm -rf` | Delete folder and contents — USE CAREFULLY | `rm -rf file1.txt` |

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
- `>` → overwrites file
- `>>` → appends to file
- `<` → takes input from file
- `|` (pipe) → connects commands
- tee → output to both screen and file

---

### Commands Practiced:

| Command | What It Does | Example |
|---|---|---|
| `>` | Redirect output (overwrite) | `echo Hello > file.txt` |
| `>>` | Append output | `echo Hi >> file.txt` |
| `<` | Take input from file | `cat < file.txt` |
| `2>` | Redirect error | `ls fake 2> error.txt` |
| `2>&1` | Redirect stderr to stdout | `ls fake > out.txt 2>&1` |
| `&>` | Redirect both outputs | `ls fake &> all.txt` |
| `\|` | Pipe output | `ls \| less` |
| `tee` | Save + display output | `ls \| tee file.txt` |

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
- Understanding I/O streams is fundamental for automation and scripting
- Linux commands become powerful when combined
- Redirection gives control over data flow
- Pipes allow chaining commands efficiently
---

## Day 3 — Environment Variables + Text Processing + File Inspection

### What I Learned:
- Environment variables store system/session information  
- $VARIABLE is used to access variables  
- env shows all environment variables  
- PATH defines where commands are searched  
- cut extracts specific parts of text  
- paste merges lines/files  
- head shows beginning of file  
- tail shows end of file  
- tail -f is used for real-time monitoring  

---

### Commands Practiced:

| Command | What It Does | Example |
|---|---|---|
| env | Show all environment variables | env |
| echo $VAR | Show variable value | echo $HOME |
| export | Set variable (temporary) | export TEST=test |
| cut | Extract text | cut -c 5 file.txt |
| cut -f | Extract field | cut -f 2 file.txt |
| cut -d | Custom delimiter | cut -d ";" -f 1 file.txt |
| paste | Merge lines | paste file.txt |
| paste -s | Combine into one line | paste -s file.txt |
| paste -d | Change delimiter | paste -d ' ' -s file.txt |
| head | Show first 10 lines | head file.txt |
| head -n | Custom lines | head -n 5 file.txt |
| tail | Show last 10 lines | tail file.txt |
| tail -n | Custom lines | tail -n 5 file.txt |
| tail -f | Real-time monitoring | tail -f file.txt |

---

### Hands-On Practice:
- Viewed environment variables using env  
- Created and accessed variables using export  
- Extracted text using cut  
- Merged lines using paste  
- Viewed file start using head  
- Monitored file changes using tail -f  

---

### Key Insight:
- Environment variables control system behavior  
- Text processing commands are powerful for handling data  
- tail -f is used in real-time monitoring and debugging  

---

## Day 4 — Text Processing & File Analysis (Combined Learning)

### What I Learned:
- `expand` and `unexpand` manage tabs and spaces  
- `join` combines files using common fields  
- `split` breaks large files into smaller parts  
- `sort` organizes data alphabetically or numerically  
- `tr` translates or deletes characters  
- `uniq` removes duplicate lines (requires sorting)  
- `wc` counts lines, words, and bytes  
- `nl` adds line numbers to files  

---

### Commands Practiced:

| Command | What It Does | Example |
|---|---|---|
| `expand` | Tabs → spaces | `expand file.txt` |
| `unexpand -a` | Spaces → tabs | `unexpand -a file.txt` |
| `join` | Combine files | `join file1.txt file2.txt` |
| `split -l` | Split by lines | `split -l 100 file.txt` |
| `sort` | Sort lines | `sort file.txt` |
| `sort -n` | Numeric sort | `sort -n file.txt` |
| `tr` | Translate characters | `echo "hi" \| tr a-z A-Z` |
| `tr -d` | Delete characters | `tr -d '0-9'` |
| `uniq` | Remove duplicates | `sort file.txt \| uniq` |
| `uniq -c` | Count duplicates | `sort file.txt \| uniq -c` |
| `wc` | Count lines/words/bytes | `wc file.txt` |
| `nl` | Add line numbers | `nl file.txt` |

---

### Hands-On Practice:
- Converted tabs to spaces and vice versa  
- Joined files using common fields  
- Split large files into smaller chunks  
- Sorted data alphabetically and numerically  
- Transformed and cleaned text using `tr`  
- Removed and counted duplicate entries  
- Counted file contents using `wc`  
- Added line numbers using `nl`  

---

### Key Insight:
- Text processing commands are powerful when combined  
- `sort + uniq` is essential for handling duplicates  
- These tools are widely used in log analysis and automation  

---

## Day 5 — grep (Search & Filter Text)

### What I Learned:
- `grep` is used to search text in files
- Can filter output based on patterns
- Works with pipes for powerful data processing
- Supports case-insensitive search and counting
- Can match patterns using regular expressions

---

### Commands Practiced:

| Command | What It Does | Example |
|---|---|---|
| `grep` | Search text in file | `grep "fox" file.txt` |
| `grep -i` | Case-insensitive search | `grep -i "fox" file.txt` |
| `grep -c` | Count matching lines | `grep -c "fox" file.txt` |
| `grep -o` | Show only matched text | `grep -o "fox" file.txt` |
| `grep -e` | Specify pattern | `grep -e "-v" file.txt` |
| `grep -f` | Use patterns from file | `grep -f patterns.txt file.txt` |
| `grep with pipe` | Filter command output | `env \| grep USER` |

---

### Hands-On Practice:
- Searched for specific words in files
- Performed case-insensitive searches
- Counted number of matches
- Extracted only matching text
- Used grep with pipes for filtering output

---

### Key Insight:
- `grep` is one of the most powerful Linux commands
- Used heavily in log analysis and troubleshooting
- Combining `grep` with pipes enables advanced data filtering

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
