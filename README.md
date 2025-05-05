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

Pull up Microsoft Sentinel, go to Configuration -> Watchlist  <br/>
Click New to create a new Watchlist <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/4.1%20sentinel%2C%20configuration-%20watchlist%2C%20create%20new.png)
<br />

Enter geoip for Name and geoip for Alias<br/>
Click Next: Source <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/4.2%20name%20geoip%2C%20alias%20geoip.png)
<br />

Set source type to local file<br/>
Upload the geo-ip summazied.csv file (provided by Josh Madakor) <br/>
Set searchkey to network<br/>
Click review and create  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/4.3%20source%20type-local%20file%2C%20upload%20file%2C%20searchkey-network%2C%20review%20and%20create.png)
<br />

Click Create under Review and create  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/4.4%20create%20watchlist.png)
<br />

Our watchlist created <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/4.5%20watchlist%20created%20.png)
<br />

Lorem ipsum  <br/>

![]()
<br />

Lorem ipsum  <br/>

![]()
<br />

Lorem ipsum  <br/>

![]()
<br />

















