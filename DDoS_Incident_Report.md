# 🛡️ Incident Report Analysis: DDoS Attack

## Summary
Our company was the victim of a DDoS attack that flooded the system's network and compromised it for 2 hours until the issue was resolved. The organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets, and normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services, and restoring critical ones. Upon analysis, the cybersecurity team found that a malicious actor initiated the ICMP flood due to an unconfigured firewall.

---

## NIST Cybersecurity Framework Application

### 🔍 Identify
The company’s cybersecurity team investigated the situation and found that a malicious actor flooded the company’s network with ICMP pings. This vulnerability allowed the attacker to overwhelm the network through a Distributed Denial of Service (DDoS) attack. The root cause was identified as an unconfigured or misconfigured firewall, which failed to block the ICMP flood.

---

### 🛡️ Protect
To mitigate future attacks, the security team implemented the following measures:
- A new firewall rule to **rate-limit incoming ICMP packets**
- Deployment of an **IDS/IPS** system to filter suspicious ICMP traffic
- **Source IP address verification** to identify and block spoofed traffic
- Installation of **network monitoring software** to flag abnormal traffic patterns in real time

---

### 📡 Detect
With the new firewall and IDS/IPS systems in place, any future ICMP ping floods or DDoS activity will generate real-time alerts in the organization’s SIEM (Security Information and Event Management) tool. This allows for earlier detection and faster escalation of similar threats.

---

### ⚠️ Respond
The incident response team:
- Activated the **DDoS response plan**  
- Blocked all **incoming ICMP traffic** at the firewall  
- Took **non-essential systems offline** to preserve critical resources  
- **Notified stakeholders and leadership**, maintaining communication throughout  
- Initiated **log analysis and forensics** to identify the attack's origin  
- Conducted a **post-incident review** to improve response playbooks  

---

### 🔧 Recover
Post-incident recovery included:
- A **phased restoration** of non-critical systems  
- Ongoing **performance and availability monitoring**  
- Updates to **firewall rules and network architecture**  
- **Security training** on escalation procedures and system hardening  
- Review of **business continuity and DDoS protection strategies**, including potential integration with cloud-based mitigation services  
- Testing of **failover and backup systems** to strengthen resilience
