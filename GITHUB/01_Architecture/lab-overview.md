=> PROJECT NAME
Cyber Defense Lab – Attack Simulation, Detection & Incident Response using Wazuh

=> Objective
The objective of this lab is to simulate real-world cyber attacks in a controlled environment and validate detection capabilities using a SIEM platform.

This environment is designed to demonstrate practical skills in:

=> Lab architecture design
->Network configuration
->Attack simulation
->Log monitoring
->Detection engineering
->Incident response workflow

The lab is fully isolated to ensure safe testing without impacting external networks.

=> Lab Environment Description
The lab consists of three virtual machines configured in an isolated host-only network to simulate an attacker, a victim system, and a SIEM monitoring server.

The attacker machine is used to simulate offensive security techniques.
The victim machine acts as a monitored endpoint with the Wazuh agent installed.
The Wazuh server functions as the centralized logging and detection engine.

=> Machines in Scope
Kali Linux is configured as the attacker machine used for reconnaissance and attack simulation.

Ubuntu Server is configured as the victim machine running monitored services and the Wazuh agent.

Wazuh Server is configured as the SIEM manager responsible for log collection, analysis, and alert generation.

=>Network Architecture
The lab uses a Host-Only network to create a fully isolated environment.

=> This ensures:
Safe attack simulation
No internet exposure
Controlled traffic flow
Reliable testing conditions

All machines are configured within the same subnet to allow communication between attacker, victim, and SIEM.

=> Architecture Validation
The lab setup was validated by confirming that all virtual machines were powered on and properly connected to the host-only adapter.

Network interfaces were verified on each machine to confirm correct IP assignment and subnet alignment.

Connectivity tests were performed to ensure that all machines could successfully communicate with each other.

=> Network Verification
All systems were confirmed to be operating within the same subnet range and able to communicate successfully using ICMP echo requests.

This confirms proper routing and network configuration required for attack simulation and monitoring.

=> Lab Validation Summary
The infrastructure is fully operational and ready for attack simulation.

All machines are reachable, network configuration is correct, and the environment is stable for proceeding to SIEM validation.

=> Evidence Collection
Screenshots are stored to provide proof of lab configuration and validation.

=> These include:
All virtual machines running
Network adapter configuration
IP address verification
Connectivity tests

=> Conclusion
Phase 1 successfully establishes a controlled cyber defense lab environment with verified connectivity and infrastructure readiness.

The lab is now prepared for SIEM service validation and subsequent attack simulation phases.

![VM Overview](GITHUB / vm-overview.png)

![IP Verification](GITHUB/wazuh-ip.png)
![IP Verification](GITHUBkali_ip.png)
![IP Verification](GITHUBvm-overview.png)

![Connectivity Test](GITHUB/ping-test_bwt-vms.png)





