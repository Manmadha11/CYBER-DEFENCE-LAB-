=> Detection Engineering — Custom SSH Brute Force Rule
Purpose
The purpose of this phase is to design and implement a custom detection rule to improve the ability of the SIEM platform to identify brute force attacks.

Detection engineering is a core responsibility of SOC teams, as it enhances monitoring capabilities and reduces the risk of undetected threats.

This phase demonstrates the ability to customize detection logic based on observed attack patterns.

=> Detection Improvement Strategy
The built-in detection rule successfully identified authentication failures, but a custom rule was created to increase visibility by triggering a high-severity alert when multiple failed login attempts occur within a short timeframe.

This approach improves alert prioritization and helps security teams respond faster.

=> Rule Logic
The custom rule is configured to trigger when multiple authentication failure events are detected within a defined timeframe.

The rule references the existing authentication failure rule and escalates the alert severity when repeated attempts are observed.

Rule Configuration File
The custom rule was added to the local rules configuration file on the SIEM manager.

This file allows custom detection logic to be defined without modifying default rules.

=> Custom Rule Added
<rule id="100001" level="12" frequency="5" timeframe="60">
  <if_sid>5716</if_sid>
  <description>Custom SSH brute force detection</description>
</rule>

=> Rule Explanation
The rule identifier uniquely identifies the custom detection logic.
The severity level is set high to indicate potential malicious activity.
The frequency condition triggers the rule after multiple events occur.
The timeframe defines the period in which repeated events must occur to trigger detection.
The rule references the authentication failure rule to build upon existing detection logic.

=> Rule Testing
The SIEM configuration was validated to ensure the rule syntax was correct and no configuration errors were present.

After validation, the manager service was restarted to apply the new rule.

=> Commands Used

"sudo nano /var/ossec/etc/rules/local_rules.xml"
"sudo /var/ossec/bin/wazuh-manager -t"
"sudo systemctl restart wazuh-manager"

=> Validation Result
The custom rule successfully triggered alerts during repeated authentication failures, confirming that the detection logic is functioning as expected.

=> Detection Enhancement Impact
Custom detection improves visibility into attack behavior and allows security teams to prioritize high-risk events.

This reduces response time and strengthens overall security monitoring.

=> MITRE ATT&CK Mapping
Technique: Brute Force

Tactic: Credential Access

This attack technique involves repeated authentication attempts to gain unauthorized access using guessed credentials.

=> Evidence Collection
Screenshots were captured showing the rule configuration and the triggered alert in the SIEM dashboard.

=> Conclusion
Phase 7 demonstrates the ability to design and implement custom detection logic to enhance SIEM capabilities.
This confirms advanced understanding of detection engineering principles used in real SOC environments.

![custum-log_rule](C:\Users\manma\OneDrive\Pictures\GITHUB\Log-rule.png)

