<h1>Azure Honeypot & SIEM: Real-Time Cyber Attack Detection</h1>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.4%20Windows%20VM%20Attack%20Map%20after%2024hrs..png)

<h2>Description</h2>
In this lab, I deployed a Windows 10 virtual machine in Microsoft Azure to simulate a honeypot environment for brute-force attack detection. I configured log collection using Log Analytics Workspace and Microsoft Sentinel, then analyzed failed login attempts with KQL (Kusto Query Language). To enrich the data, I imported a GeoIP watchlist for identifying attacker locations and visualized the results using a custom-built attack map in Sentinel Workbooks. This project demonstrates core skills in cloud security, SIEM deployment, log analysis, and threat visualization.
<br />

<h2>Techonologies Used</h2>

- <b>Microsoft Azure Virtual Machines</b>
- <b>Network Security Group</b>
- <b>Log Analytics Workspace</b>
- <b>Microsoft Sentinel, KQL, Workbook</b>
- <b>Remote Desktop</b>

<h2>Operating Systems</h2>

- <b>Windows 10</b>

<h2>Overview:</h2>

- <b>Setting up an Azure environment</b> 
- <b>Creating and exposing a Windows 10 virtual machine to simulate attack surface</b>
- <b>Capturing failed login attempts and analyzing them via Event Viewer</b>
- <b>Forwarding logs to a centralized Log Analytics Workspace (LAW)</b>
- <b>Deploying Microsoft Sentinel and configuring security connectors</b>
- <b>Writing KQL (Kusto Query Language) queries to investigate suspicious activity</b>
- <b>Enriching logs with geolocation data using a custom watchlist</b>
- <b>Visualizing attack origins with a dynamic threat map in Sentinel Workbooks</b>

<h2>Program Walk-Through:</h2>

- [Setting up an Azure environment](https://github.com/rbrianshutt/setting_up_azure_environment/blob/main/README.md)
- [Creating and exposing a Windows 10 virtual machine to simulate attack surface](https://github.com/rbrianshutt/attack_surface/blob/main/README.md)
- [Capturing failed login attempts and analyzing them via Event Viewer](https://github.com/rbrianshutt/event_viewer/blob/main/README.md)
- [Forwarding logs to a centralized Log Analytics Workspace (LAW)](https://github.com/rbrianshutt/law/blob/main/README.md)
- [Deploying Microsoft Sentinel and configuring security connectors](https://github.com/rbrianshutt/sentinel/blob/main/README.md)
- [Write KQL (Kusto Query Language) a query to investigate suspicious activity, enrich logs with geolocation data using a custom watchlist, and visualize attack origins through a dynamic threat map in Microsoft Sentinel Workbooks](https://github.com/rbrianshutt/sentinel_workbook/blob/main/README.md)




















