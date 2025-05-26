# 🔍 Local Network Port Scanning with Nmap

## 📌 Objective
To identify open ports in a local network using Nmap, understand services running on them, and analyze security risks.

## 🛠️ Tools Used
- Kali Linux (VirtualBox)
- Nmap
- Wireshark (Optional)
- Git & GitHub

## 🧪 Steps Performed
1. Identified local IP range using `ip a`
2. Scanned network: `sudo nmap -sS 10.0.2.2/24`
3. Saved results in TXT and XML `nmap -sS 10.0.2.2/24 -oN scan_result.txt`
 -oN stands for "output in normal form"
4. Analyzed packets in Wireshark
5. Researched ports and services
6. Noted down potential vulnerabilities

## 📄 Sample Output
Nmap scan report for 10.0.2.2
Host is up (0.013s latency).
Not shown: 994 filtered tcp ports (no-response)
PORT     STATE SERVICE
135/tcp  open  msrpc
445/tcp  open  microsoft-ds
1001/tcp open  webpush
1024/tcp open  kdm
5357/tcp open  wsdapi
8090/tcp open  opsmessaging
MAC Address: 52:54:00:12:35:02 (QEMU virtual NIC)

Nmap scan report for 10.0.2.3
Host is up (0.011s latency).
Not shown: 994 filtered tcp ports (no-response)
PORT     STATE SERVICE
135/tcp  open  msrpc
445/tcp  open  microsoft-ds
1001/tcp open  webpush
1024/tcp open  kdm
5357/tcp open  wsdapi
8090/tcp open  opsmessaging
MAC Address: 52:54:00:12:35:03 (QEMU virtual NIC)


## 🔐 Risks of Open Ports
- Unpatched services
- Misconfigurations
- Unauthorized access

## 🛡️ How to Secure
- Use firewalls
- Disable unused ports
- Enable service authentication
- Regularly scan and update

## 📚 Interview Questions
What is an open port?
An open port is a network port that accepts incoming connections, indicating a service is listening.

How does Nmap perform a TCP SYN scan?
Nmap sends SYN packets to ports. If it receives SYN-ACK, the port is open; if RST, it's closed.

Risks of Open Ports?
Unauthorized access, exploitation of vulnerabilities, data breaches.

TCP vs UDP Scanning?

TCP: Reliable, connection-based, easier to detect.

UDP: Connectionless, harder to detect, but less reliable.

How to Secure Open Ports?
Use firewalls, close unused ports, update services, use authentication.

What does a Firewall do?
Filters incoming/outgoing traffic based on rules; blocks unwanted ports/services.

Why do attackers scan ports?
To find open services they can exploit.

How does Wireshark help?
Shows raw packet data, allowing deeper inspection of traffic during port scans.


## What I Learn from This Task
Network enumeration
Using Kali Linux for recon
Understanding services behind ports
Basics of firewalls and service hardening
Documentation + GitHub workflow
