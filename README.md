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
- [Write KQL (Kusto Query Language) a query to investigate suspicious activity, enrich logs with geolocation data using a custom watchlist, and visualize attack origins through a dynamic threat map in Microsoft Sentinel Workbooks]()

Go to Microsoft Sentinel -> Threat management -> Workbooks  <br/>
Click Add Workbook  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.1%20sentinel%2C%20threat%20management-workbooks%2C%20add%20workbook.png)
<br />

Click edit and remove pre populated content  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.1.2%20click%20edit%20and%20remove%20pre%20populated%20content.png)
<br />

Click Add <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.1.3%20click%20add%20.png)
<br />

Go to Add query <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.1.3%20click%20add%20query%20.png)
<br />

Click advanced editor <br/>
Enter JSON <br/>
Click Done Editing <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.1.4%20click%20advanced%20editor%2C%20enter%20JSON%2C%20click%20done%20editing.png)
<br />

Save as Windows VM Attack Map <br/>
Make sure resource group and subscription are correct  <br/>
Click Save As <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.2%20save%20as%20Windows%20VM%20Attack%20Map%2C%20set%20resource%20group%2C%20save%20as.png)
<br />

Set KQL query to pull up failed logons and use geolocation data <br/>
Click Run Query <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.3%20set%20KQL%20query%20in%20log%20analytics%20workspace%2C%20run%20query.png)
<br />

Here is the Attack Map after 24 hours <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/5.4%20Windows%20VM%20Attack%20Map%20after%2024hrs..png)
<br />



















