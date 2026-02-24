=> Security Incident Report — SSH Brute Force Attack
Executive Summary
A simulated brute force attack targeting the SSH service on the Ubuntu endpoint was conducted within a controlled lab environment.
The attack originated from the Kali Linux attacker machine and generated multiple authentication failures.
The Wazuh SIEM platform successfully detected the attack through built-in and custom detection rules, confirming that monitoring and alerting mechanisms are functioning effectively.
No unauthorized access was achieved during the simulation.

=> Incident Overview
This incident involved repeated login attempts against an SSH service using a password dictionary attack technique.
The activity was identified as malicious due to the high frequency of failed authentication attempts within a short period.

The event was classified as a brute force attack attempt targeting user credentials.

=> Incident Timeline
Attack initiated from attacker machine.
Multiple failed authentication attempts generated on target system.
Logs collected by Wazuh agent.
Detection alert triggered in SIEM dashboard.
Custom detection rule escalated severity.
Incident analysis performed.

=> Affected Systems
Ubuntu Server (monitored endpoint)
Wazuh SIEM Manager

=> Attack Vector
Credential-based attack targeting SSH authentication service.
The attacker used automated password attempts to try to gain unauthorized access.

=> Detection Details
The attack was detected through authentication failure logs collected by the endpoint agent.
Built-in detection rules identified repeated failed login attempts.
A custom rule triggered a high-severity alert when multiple failures occurred within the configured timeframe.

=> Evidence
Security alerts in the SIEM dashboard confirmed detection of brute force behavior.
Authentication logs showed repeated failed login attempts from the attacker IP address.
Screenshots were collected as proof of detection and log activity.

=> Root Cause
The SSH service was exposed within the network, allowing authentication attempts from another host.
Weak authentication controls can allow brute force attempts if not monitored.

=> Impact Assessment
No system compromise occurred during the simulation.
The activity demonstrates how attackers may attempt to gain unauthorized access using credential attacks.
Successful detection prevented potential risk escalation.

=> Response Actions
Security alerts were reviewed and analyzed.
Detection rules validated.
Custom detection logic implemented to improve monitoring.
Logs reviewed to confirm attack behavior.

=> Mitigation Recommendations
Implement account lockout policies after repeated failed login attempts.
Use strong password policies and multi-factor authentication.
Restrict SSH access using network controls or firewall rules.
Continuously monitor authentication logs for suspicious activity.

=> Lessons Learned
Early detection significantly reduces risk of credential compromise.
Custom detection rules improve visibility into attack behavior.
Continuous monitoring is essential for identifying malicious activity.
Security controls should be layered to prevent unauthorized access.

=> MITRE ATT&CK Classification
Tactic: Credential Access
Technique: Brute Force
This technique involves repeated attempts to guess passwords in order to gain unauthorized access.

=> Conclusion
The incident demonstrates successful detection and analysis of a simulated brute force attack within a controlled environment.
The SIEM platform effectively identified malicious behavior and provided visibility into attack activity.
This confirms the effectiveness of monitoring, detection, and response processes implemented in the lab.

                                                                                  Thank you.