
# Microsoft Sentinel SOC Lab

## Objective
Build a Microsoft Sentinel SIEM lab to collect logs, detect suspicious activity, and create alerting rules using KQL.

---

## Environment Setup

### Create Log Analytics Workspace
This step creates a central workspace for collecting and analyzing logs.

click link to view screenhot https://github.com/Mojalefa48/azure-security-portfolio/blob/826f34bd661dc933fa9ccdfead927c8ef9f4e3b8/screenshots/create-log-analytics-workspace.png

### Enable Microsoft Sentinel
This step enables Microsoft Sentinel on the Log Analytics workspace to start collecting and analyzing security events.

screenshots/enable-sentinel.png

### Connect Sentinel to Workspace
Microsoft Sentinel is connected to the Log Analytics workspace for centralized monitoring.

screenshots/connect-sentinel.png

---

## Data Collection

### Add Entra ID Data Connector
Configured Microsoft Entra ID to send logs into Sentinel.

screenshots/adding-data-connectors-entra-id.png

### Enable Logs
Enabled diagnostic logs to ensure security events are captured.

screenshots/enabling-log.png

### Verify Sign-in Logs
Validated that user sign-in logs are being ingested into the workspace.

screenshots/entra-id-signin-logs.png

---

## Detection & Monitoring

### Run Sign-in Logs Query (KQL)
Executed KQL queries to analyze authentication activity.

screenshots/running-signin-logs-query.png

### Create Analytics Rule (Failed Logins)
Configured an alert rule to detect repeated failed login attempts.

screenshots/analytics-rule-failed-logins.png

### Scheduled Detection Rule
Set up scheduled detection to continuously monitor suspicious behavior.

screenshots/scheduled-detection-rule.png

---

## Results

- Successfully ingested Entra ID logs into Microsoft Sentinel  
- Created detection rules for failed login attempts  
- Queried logs using KQL  
- Simulated suspicious login activity and detected it  

---

## Skills Demonstrated

- Microsoft Sentinel (SIEM)  
- KQL (Kusto Query Language)  
- Microsoft Entra ID  
- Threat Detection & Monitoring  
- Incident Investigation Basics 
