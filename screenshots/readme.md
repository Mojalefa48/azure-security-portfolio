## Environment Setup

### Create Log Analytics Workspace
(screenshots/create-log-analytics-workspace.png)

### Enable Microsoft Sentinel
This step enables Microsoft Sentinel on the Log Analytics workspace to start collecting and analyzing security events.

![Enable Sentinel](screenshots/enable-sentinel.png)

### Connect Sentinel to Workspace
![Connect Sentinel](screenshots/connect-sentinel.png)


## Data Collection

### Add Entra ID Data Connector
![Add Data Connector](screenshots/adding-data-connectors-entra-id.png)

### Enable Logs
![Enable Logs](screenshots/enabling-log.png)

### Verify Sign-in Logs
![Sign-in Logs](screenshots/entra-id-signin-logs.png)


## Detection & Monitoring

### Run Sign-in Logs Query (KQL)
![KQL Query](screenshots/running-signin-logs-query.png)

### Create Analytics Rule (Failed Logins)
![Analytics Rule](screenshots/analytics-rule-failed-logins.png)

### Scheduled Detection Rule
![Scheduled Rule](screenshots/scheduled-detection-rule.png)


## Results

- Successfully connected Entra ID logs to Sentinel  
- Created detection rules for failed login attempts  
- Queried logs using KQL  
- Simulated suspicious activity and detected it  
``
