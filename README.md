
# 🔐 Cybersecurity Task 1 – Port Scanning using Nmap (Windows)

## 🎯 Objective
To perform local network port scanning using Nmap and analyze open ports to understand possible security exposures.

---

## 🛠 Tools Used
- **Operating System:** Windows
- **Scanner Tool:** Nmap

---

## 📝 Steps Performed

### 🔹 1. Found My IP Address
Ran the following command in Command Prompt:
```
ipconfig
```
From this, identified the local IP (e.g., `192.168.1.5`) and calculated the IP range:  
**`192.168.1.0/24`**

---

### 🔹 2. Performed a TCP SYN Scan
Command used:
```
nmap -sS 192.168.131.175 -oN scan_result.txt
```
This scanned all hosts on the network for open TCP ports using a SYN scan.

---

### 🔹 3. Scanned a Specific Port Range (22–8080)
Command used:
```
nmap -sS -p 22-8080 192.168.131.175 -oN scan_port_range.txt
```
Focused on commonly used ports like SSH (22), HTTP (80), HTTPS (443), etc.

---

### 🔹 4. Disabled Ping with -Pn
Command used:
```
nmap -sS -Pn 192.168.131.175 -oN scan_no_ping.txt
```
Skipped host discovery (ICMP ping), useful for detecting devices that block ping requests.

---

## 📁 Files Included
- scan_result.txt – Full TCP SYN scan result
- scan_port_range.txt – Scan limited to ports 22–8080
- scan_no_ping.txt – Scan with host discovery disabled

---

## 🔍 Observations
- Found multiple devices on the network.
- Open ports detected included:
  - Port 22 (SSH)
  - Port 80 (HTTP)
  - Port 443 (HTTPS)
- These ports can be entry points for attacks if services behind them are misconfigured.

---

## 🔐 Security Notes
- Close unused ports.
- Use firewalls to filter unwanted traffic.
- Regularly audit open ports on devices.
- Keep systems and services updated.

---

## ✅ Submission Info
- **Task:** Cybersecurity Internship – Task 1
- **GitHub Repository:** []
- **Date:** 23-06-2025

---

## 📖 Key Concepts
`nmap`, `TCP SYN scan`, `open ports`, `-sS`, `-Pn`, `-p`, `network reconnaissance`
