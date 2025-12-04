🐧 Linux & SOC Analyst Portfolio

This repository demonstrates practical Linux skills applied to SOC operations, incident response, and Security+ (SY0-701) preparation.
It includes real investigation examples, threat-hunting techniques, log analysis, and core command-line fundamentals.

🚀 Skills Demonstrated
🔹 Linux Fundamentals

File system navigation (ls, cd, pwd)

File operations (cat, nano, cp, mv, rm)

Permissions & ownership (chmod, chown)

User & group management (id, sudo, /etc/passwd)

🔹 SOC / Blue Team Linux Skills

Log analysis (tail -f, grep, journalctl)

Process investigation (ps aux, top, lsof)

Network inspection (ss -tulnp, ip a, curl, ping)

Threat hunting (IOCs, hashing files, persistence checks)

🔹 Security Hardening

Least privilege validation

Identifying misconfigurations

Reviewing open ports & services

Detection of unauthorized changes

📂 Repository Structure
01-Linux-Basics/
02-SOC-Linux-Analysis/
03-Incident-Response-Labs/
04-Tools-&-Cheatsheets/


Each folder contains practical examples, notes, and reference materials used during hands-on investigations.

🧪 Example: SOC Linux Investigation

(04-SOC-Linux-Analysis/process-investigation.md)

🔍 Suspicious Process Detected
ps aux | grep crypto

Findings

Unknown binary executed from /tmp/crypto-miner

Open port 3333 communicating with an external IP

CPU usage consistently above 90% (possible crypto-miner)

Actions Taken

Terminated process (kill -9 <PID>)

Verified system binary integrity (sha256sum)

Checked persistence mechanisms (crontab -l, systemd services`)

Collected logs for escalation and forensic review

📘 Example: Log Analysis (auth.log)
Command Used
grep "Failed password" /var/log/auth.log

Findings

Repeated failed SSH login attempts

Activity from foreign IP ranges

No successful compromise detected

Response

Disabled password authentication

Enforced key-based SSH login

Updated firewall rules to restrict remote access

🔐 Key Linux Commands (Quick Reference)
Category	Commands
Navigation	cd, ls, pwd
File Operations	cat, nano, cp, rm, mv
Permissions	chmod, chown
Processes	ps aux, top, kill, lsof
Networking	ip a, ping, ss -tulnp, curl
Logs	tail -f, grep, journalctl
Security	history, stat, sha256sum
🏆 Why This Matters

Linux is the backbone of modern cybersecurity:

Most production servers run Linux

SOC analysts rely on Linux for logs, forensics, and threat detection

Security+ Domain 2 & 4 require Linux proficiency

Real cyber incidents require command-line investigation

This portfolio highlights hands-on capabilities, not just theoretical understanding.
