Linux Service Management Troubleshooting

Scenario:
User reports web service is not accessible.

Date:
2/18/2026

Initial Hypothesis:
Service may be stopped, failed, or misconfigured.

Diagnostic Steps:

Verified Apache package installation using:
sudo apt update
sudo apt install apache2

Checked service status using:
systemctl status apache2

Observed Status (Before Simulation):
Service state: active (running)

Simulated Issue:
Stopped service using:
sudo systemctl stop apache2

Observed Status After Stop:
Service state: inactive (dead)

Resolution Steps:
Restarted service using:
sudo systemctl start apache2

Verified service returned to active (running) state using:
systemctl status apache2

Final Verification:
Service successfully restarted and operating normally.

What I Learned:
Linux services can be managed using systemctl. Verifying service status before escalation is critical when diagnosing application availability issues.
