=> Attack Surface Discovery
Purpose
The purpose of this phase is to identify exposed services, open ports, and potential vulnerabilities on the target system.

Understanding the attack surface is a critical step in any penetration testing engagement, as it helps determine possible entry points that an attacker could exploit.

This phase simulates the reconnaissance stage of a real-world security assessment.

=> Target Scope
The Ubuntu machine was selected as the target system because it represents a monitored endpoint within the lab environment.

The objective is to enumerate all accessible services and identify potential risks associated with exposed ports.

=> Scanning Methodology
A full TCP SYN scan was performed using Nmap to detect open ports, running services, and operating system details.

The scan also attempted service version detection to identify possible vulnerabilities related to outdated software.

Aggressive timing was used to speed up scanning while maintaining accuracy within the isolated lab environment.

=> Scan Command Used

"nmap -sS -sV -O -T4 192.168.56.X"

Command Explanation
nmap is a network scanning tool used for discovery and security auditing.
The SYN scan technique performs a stealthy scan by sending partial TCP connections.
Service version detection attempts to identify the exact software running on each port.
Operating system detection attempts to identify the target OS based on network responses.
Aggressive timing speeds up the scan while maintaining reliability in a controlled environment.

=> Scan Results Summary
The scan identified multiple open ports and running services on the target machine.
These services represent potential entry points that could be targeted during an attack simulation.

=> Risk Analysis
Open services increase the attack surface and may be vulnerable to misconfiguration, weak authentication, or known exploits.

Identifying these services helps prioritize testing efforts and determine which attack techniques may be applicable in later phases.

=> Key Findings
The system exposes network services that can be targeted for authentication attacks and service enumeration.

These findings will be used in the next phase to simulate attacks and observe detection behavior in the SIEM platform.

=> Evidence Collection
Screenshots of the full Nmap scan output were captured to provide proof of reconnaissance activity and findings.

=> Conclusion
Phase 3 successfully identified the attack surface of the target system and documented exposed services.

This provides the foundation for controlled attack simulation in the next phase.


![Nmap-scan](C:\Users\manma\OneDrive\Pictures\GITHUB\nmap-scan.png)

![ssh-status](C:\Users\manma\OneDrive\Pictures\GITHUB\ssh-status.png)
