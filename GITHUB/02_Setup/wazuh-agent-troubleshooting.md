=> Wazuh Agent Troubleshooting
Problems Encountered
During setup, several configuration issues prevented the agent from connecting successfully.

These included incorrect manager IP configuration, permission errors, service startup failures, and agent key conflicts.

=> Root Causes
Incorrect server address in configuration file.
Improper file permissions.
Old PID files causing service conflicts.
Agent already registered with conflicting keys.
System time mismatch affecting authentication.

=> Resolution Steps
The configuration file was corrected with the proper manager IP address.
Permissions were restored using appropriate chmod commands.
Old PID files were removed to clear service conflicts.
The agent was re-registered after deleting old client keys.
System time was synchronized to ensure proper communication.

Outcome
After applying the fixes, the agent successfully connected to the Wazuh manager and began forwarding logs normally.