# network_portscan_task1
# Network Port Scanning with Nmap

🎯 Objective
Learn to discover open ports on devices in the local network to understand network exposure.

🧰 Tools Used
- Nmap:For network discovery and port scanning.  
- Wireshark:For observing live packets during the scan

🧪 Steps Performed
1. Verified the system’s local IP using `ipconfig` — IPv4: `192.168.2.20`.  
2. Identified the network range: `192.168.2.0/24`.  
3. Ran a ping scan to discover active devices:
   nmap -Pn -sn 192.168.2.0
4. Found that the active host was **192.168.2.20**.
5. Conducted a TCP SYN scan to identify open ports:
   nmap -sS 192.168.2.20
   
6. Observed open ports and services on that host.

Results

| Port    | State | Service        |
| ------- | ----- | -------------- |
| 135/tcp | open  | msrpc          |
| 139/tcp | open  | netbios-ssn    |
| 445/tcp | open  | microsoft-ds   |
| 902/tcp | open  | iss-realsecure |
| 912/tcp | open  | apex-mesh      |

Interpretation

* Ports 135, 139, 445 indicate file sharing and RPC services.
* Ports 902, 912 are related to VMware services, indicating virtualization software is active.
* Open ports reveal potential network exposure points — attackers could exploit them if not s configured to limit access.

 
