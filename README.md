Network Security Assessment Report
Prepared by: Kenneth Stephen Ali
Date: 04 November 2024
________________________________________
1. Project Overview
This report details the network security assessment conducted using a Linux virtual machine (VM) configured to scan the host network. The assessment used Nmap for network scanning and Elastic SIEM for real-time monitoring, logging, and alerting. The objective was to identify potential vulnerabilities, monitor network events, and set up an automated alerting mechanism to ensure proactive threat analysis.
________________________________________
2. Methodology
•	Environment Setup:
o	A Linux VM was created to serve as the primary environment for the scanning operations.
o	Elastic SIEM was set up to capture, log, and process the scan data.
•	Network Scanning with Nmap:
o	Nmap was employed for port scanning and to identify live hosts, open ports, and available services on the host network.
o	Scans targeted critical IP addresses within the network to map the attack surface and identify security risks.
•	Log Capture and Analysis:
o	Elastic SIEM was configured to capture and analyse logs generated from the Nmap scans.
o	The SIEM tool processed these logs to generate actionable queries, log events, and alerts for any anomalies or unauthorized access attempts.
•	Email Alert Configuration:
o	Alerts were configured in Elastic to automatically send results to my email for further analysis.
o	This approach ensures timely notification and allows for a rapid response to potential security threats.
________________________________________
3. Findings
1.	Open Ports and Services:
o	The Nmap scan identified several open ports across multiple IPs within the host network.
o	Services associated with these ports were also listed, providing insights into which applications were exposed.
2.	Potential Vulnerabilities:
o	Some ports were unexpectedly open, which could be exploited if left unaddressed.
o	Services running outdated versions were flagged as potential security risks, as they may be vulnerable to known exploits.
3.	Anomalous Activity:
o	Elastic SIEM logged several unusual access attempts during the scanning period, including repeated connection attempts to specific ports.
o	These attempts triggered alerts, suggesting possible probing or reconnaissance activity on the network.
________________________________________
4. Alerts and Notifications
•	SIEM Alert Summary:
o	Total Alerts Generated: [56]
o	High-Priority Alerts: [26]
o	Medium and Low-Priority Alerts: [30]
o	Each alert included a timestamp, source IP, destination IP, and nature of the activity (e.g., unauthorized access, port scan detection).
•	Email Notification:
o	All high-priority alerts were automatically sent to my email. This enabled rapid review and escalation as needed.
________________________________________
5. Recommendations
1.	Port Hardening:
o	Close unused ports and restrict access to necessary services to limit exposure.
o	Implement network segmentation to minimize the risk to sensitive areas of the network.
2.	Software Updates:
o	Update software versions for identified services to the latest stable releases.
o	Regular patching should be scheduled to mitigate vulnerabilities associated with outdated versions.
3.	Monitoring and Alerting:
o	Continue monitoring network activity using Elastic SIEM and periodically refine alert rules to reduce false positives.
o	Review alerts regularly and adjust alert thresholds as necessary to improve accuracy.
4.	Incident Response:
o	Establish an incident response protocol to address any high-priority alerts.
o	Conduct periodic training for the response team to ensure readiness in the event of a security incident.
________________________________________
6. Conclusion
The network security assessment revealed valuable insights into the current state of the host network's security. By leveraging Nmap and Elastic SIEM, it was possible to identify and log potential vulnerabilities, providing a foundation for future security enhancements. The email alerting system ensures that security events are promptly flagged and reviewed, contributing to a more proactive cybersecurity posture.

