SSH Connectivity Troubleshooting

Scenario:
User reports inability to SSH to server (10.0.0.50).

Date:
3/3/2026

Initial Hypothesis:
Possible network reachability issue, port 22 blocked, SSH service down, or authentication failure.

Troubleshooting Flow:

Reachability (Layer 3): Verify host is reachable (e.g., ping server IP).

Port Availability (Layer 4): Attempt SSH connection and interpret error behavior.

Timeout suggests port filtering (firewall/ACL/security group).

Connection refused suggests service not listening (sshd down).

Service Status (Layer 7 service state): If access available, verify sshd is running on server (systemctl status ssh/sshd).

Authentication (Layer 7 auth): If connection succeeds but login fails, validate username/password or SSH key configuration.

Key Error Interpretation:

Ping fails: network issue.

Ping works + SSH timeout: port 22 blocked by firewall/ACL.

Ping works + connection refused: SSH service not running/listening.

Prompt appears but login fails: credentials/keys/account issue.

What I Learned:
SSH troubleshooting requires isolating connectivity vs port access vs service availability vs authentication. Error messages guide which layer to investigate next.
