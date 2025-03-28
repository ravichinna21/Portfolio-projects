# Incident Report Analysis: DDoS Attack Response
- **Date:** March 2025
- **Overview:** My multimedia company experienced a DDoS attack that disrupted network services for 2 hours. I analyzed the incident using the NIST CSF framework and suggested improvements.
- **What I Did:**
  - Analyzed the DDoS attack caused by a flood of ICMP packets through an unconfigured firewall.
  - Applied NIST CSF (Identify, Protect, Detect, Respond, Recover) to assess the incident and plan future improvements.
- **Skills Used:**
  - Incident analysis and documentation.
  - Knowledge of NIST CSF and DDoS attack mitigation.
  - Analytical thinking to recommend solutions.
- **Findings:**
  - Identified: A malicious actor used an ICMP flood attack, affecting the entire internal network.
  - Protect: The team implemented firewall rules to limit ICMP packets and an IDS/IPS system to filter suspicious traffic.
  - Detect: Added source IP verification and network monitoring software to detect abnormal traffic.
  - Respond: Planned to isolate affected systems, restore critical services, and report incidents to management.
  - Recover: Restored network services by blocking ICMP packets, stopping non-critical services, and bringing critical services back online.
- **Recommendations:**
  - Identify: Conduct regular audits to find risks like unconfigured firewalls.
  - Protect: Continue using firewall rules and IDS/IPS, add employee training on phishing.
  - Detect: Improve monitoring with tools like Splunk for faster detection.
  - Respond: Create a detailed incident response plan to isolate and analyze future attacks.
  - Recover: Set up regular backups and test them to ensure quick recovery.
- **Result:** Provided a detailed incident report and a plan to prevent future DDoS attacks, improving overall network security.
