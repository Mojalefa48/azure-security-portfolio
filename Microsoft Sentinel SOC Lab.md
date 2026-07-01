
# Microsoft Sentinel SOC Lab

## Objective
Build a Microsoft Sentinel SIEM lab to collect logs, detect suspicious activity, and create alerting rules using KQL.

---

## Environment Setup

### Create Log Analytics Workspace
This step creates a central workspace for collecting and analyzing logs.

https://github.com/Mojalefa48/azure-security-portfolio/blob/826f34bd661dc933fa9ccdfead927c8ef9f4e3b8/screenshots/create-log-analytics-workspace.png

### Enable Microsoft Sentinel
This step enables Microsoft Sentinel on the Log Analytics workspace to start collecting and analyzing security events.

https://github.com/Mojalefa48/azure-security-portfolio/blob/083c7156bc371b9c457bcd6ae5ca5a6e29f292f4/screenshots/enable-sentinel.png

### Connect Sentinel to Workspace
Microsoft Sentinel is connected to the Log Analytics workspace for centralized monitoring.

https://github.com/Mojalefa48/azure-security-portfolio/blob/083c7156bc371b9c457bcd6ae5ca5a6e29f292f4/screenshots/entra-id-log-export-setup.png

---

## Data Collection

### Add Entra ID Data Connector
Configured Microsoft Entra ID to send logs into Sentinel.

https://github.com/Mojalefa48/azure-security-portfolio/blob/083c7156bc371b9c457bcd6ae5ca5a6e29f292f4/screenshots/adding-data-connectors-entra-id.png.png

### Enable Logs
Enabled diagnostic logs to ensure security events are captured.

click link to view screenshot https://github.com/Mojalefa48/azure-security-portfolio/blob/083c7156bc371b9c457bcd6ae5ca5a6e29f292f4/screenshots/entra-id-log-export-setup.png

### Verify Sign-in Logs
Validated that user sign-in logs are being ingested into the workspace.

https://github.com/Mojalefa48/azure-security-portfolio/blob/44884fac84f1abd6e4744839ed221b884e550f65/screenshots/Sign%20in%20logs%20.png

---

## Detection & Monitoring

### Run Sign-in Logs Query (KQL)
Executed KQL queries to analyze authentication activity.

https://github.com/Mojalefa48/azure-security-portfolio/blob/f527ae766db10ee9d501f32922cc248363f35bce/screenshots/running-signin-logs-query.png

## Advanced Threat Detection

Impossible Travel Detection
Developed a geo-velocity detection rule using Microsoft Sentinel and KQL to identify potential account compromise based on abnormal login locations and travel speed.

https://github.com/Mojalefa48/azure-security-portfolio/blob/1f3a95841c36d8457f0bf57af149f91ca78bb7f7/screenshots/Impossible%20Travel%20Detection.png

### Create Analytics Rule (Failed Logins)
Configured an alert rule to detect repeated failed login attempts.

https://github.com/Mojalefa48/azure-security-portfolio/blob/df1672f0a83aa0d799a66f3f38074b860ad1bad9/screenshots/analytics-rule-failed-logins.png.png

### Scheduled Detection Rule
Set up scheduled detection to continuously monitor suspicious behavior.

https://github.com/Mojalefa48/azure-security-portfolio/blob/f527ae766db10ee9d501f32922cc248363f35bce/screenshots/Scheduled%20Detection%20Rule.png


## AI Integration

A Logic App playbook (AI-SOC-SuspiciousIP) was created and integrated with Microsoft Sentinel.

Workflow:
Suspicious IP Detection
- Incident Creation
- Logic App Playbook
-Automated Email Notification

Validation:
- Playbook successfully deployed
- Microsoft Sentinel connector configured
- Outlook connector configured
- Playbook execution validated through successful run history

Troubleshooting:
While configuring Sentinel Automation Rules, an HTTP 400 error was encountered:

"Missing required permissions for Microsoft Sentinel on the playbook resource"

Troubleshooting steps performed:
- Reviewed Azure Activity Logs
- Validated Logic App permissions
- Verified Microsoft Sentinel Contributor roles
- Verified managed identity configuration
- Confirmed successful playbook execution

https://github.com/Mojalefa48/azure-security-portfolio/blob/6fdb5842a6e12ffd957520e4b61d15bb6fd39e73/screenshots/Logic%20App%20Playbook.png

Lessons Learned:
- Sentinel Automation Rules require additional playbook permissions
- Azure Activity Logs are critical for troubleshooting automation failures
- Logic Apps can be validated independently of Sentinel automation rules

# Threat Hunting Lab

## Objective
Perform proactive threat hunting using Microsoft Sentinel.

## Data Source
Microsoft Entra ID SigninLogs

## Hunting Queries
- Failed Login Hunt
- Multiple Country Hunt
- Suspicious IP Hunt
- After-Hours Login Hunt
- MFA Failure Hunt

https://github.com/Mojalefa48/azure-security-portfolio/blob/f780db75a2cb0a67ecb106a07451b5416b6195c8/screenshots/Hunt%20for%20Multiple%20Countries.png

## Lessons Learned
- Threat hunting differs from detection engineering
- KQL can identify suspicious behavior without alerts
- Proactive analysis improves visibility

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
- Suspicious IP Detection
- Threat Detection & Monitoring
- Threat Hunting
- Logic Apps
- AI-style SOC Automation
- Incident Investigation Basics
- Impossible Travel Detection


