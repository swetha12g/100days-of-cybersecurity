![linux-commands-diagram](https://github.com/user-attachments/assets/6495370f-6e53-4bba-abf4-77ed66b5f76a)

# Essential Linux Commands for Cybersecurity Beginners

## Basic System Navigation and File Operations

| Command | Syntax | Description | Security Use Case |
|---------|--------|-------------|------------------|
| `ls` | `ls -la` | List directory contents | Identify hidden files and permissions |
| `cd` | `cd directory` | Change directory | Navigate through system directories |
| `pwd` | `pwd` | Print working directory | Verify current location |
| `chmod` | `chmod 755 file` | Change file permissions | Set secure file permissions |
| `chown` | `chown user:group file` | Change file ownership | Manage file ownership |
| `find` | `find / -name filename` | Search for files | Locate suspicious files |
| `grep` | `grep "pattern" file` | Search text patterns | Search for specific strings in logs |

## Network Commands

| Command | Syntax | Description | Security Use Case |
|---------|--------|-------------|------------------|
| `ifconfig`/`ip` | `ifconfig` or `ip a` | Show network interfaces | Network reconnaissance |
| `netstat` | `netstat -tuln` | Show network connections | Identify open ports and connections |
| `nmap` | `nmap -sV target` | Network scanning tool | Port scanning and service detection |
| `tcpdump` | `tcpdump -i eth0` | Packet capture tool | Network traffic analysis |
| `ping` | `ping host` | Test network connectivity | Basic network troubleshooting |
| `traceroute` | `traceroute host` | Show network path | Network path analysis |

## System Information and Monitoring

| Command | Syntax | Description | Security Use Case |
|---------|--------|-------------|------------------|
| `ps` | `ps aux` | Show running processes | Identify suspicious processes |
| `top` | `top` | Show system resources | Monitor system performance |
| `who` | `who` | Show logged-in users | Monitor user sessions |
| `last` | `last` | Show last logged in users | Audit login history |
| `history` | `history` | Show command history | Audit user commands |
| `uname` | `uname -a` | Show system information | System identification |

## File Analysis and Security

| Command | Syntax | Description | Security Use Case |
|---------|--------|-------------|------------------|
| `md5sum` | `md5sum file` | Generate MD5 hash | File integrity verification |
| `sha256sum` | `sha256sum file` | Generate SHA256 hash | Secure file verification |
| `file` | `file filename` | Determine file type | Identify file types |
| `strings` | `strings file` | Show printable strings | Basic malware analysis |
| `xxd` | `xxd file` | Hexadecimal dump | Low-level file analysis |

## Log Analysis

| Command | Syntax | Description | Security Use Case |
|---------|--------|-------------|------------------|
| `tail` | `tail -f /var/log/syslog` | Show end of file | Real-time log monitoring |
| `head` | `head file` | Show start of file | Quick log review |
| `less` | `less file` | View file contents | Log file analysis |
| `cat` | `cat file` | Display file contents | View configuration files |
| `awk` | `awk '{print $1}' file` | Text processing | Log parsing |
| `sed` | `sed 's/old/new/' file` | Stream editor | Log modification |
