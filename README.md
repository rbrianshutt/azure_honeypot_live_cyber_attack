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

Delete Network Security Group rule for RDP <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.3%20delete%20nsg%20rule.png)
<br />

Create inbound port rule <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.3.2%20create%20inbound%20port%20rule.png)
<br />

Set inbound security rule allowing any source and any destination port<br/>
Click Add <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.3.3%20add%20inbound%20security%20rule.png)
<br />

Any port, source, destination is allowed purposefully to allow brute force attacks <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.3.4%20rule%20added.png)
<br />

Look up the public IP address  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.4%20get%20public%20ip%20address.png)
<br />

Remote into the Windows virtual machines <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.4.2%20remote%20into%20vm.png)
<br />

Enter username and password <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.4.3%20username%20and%20password.png)
<br />

Go to the VM Windows Defender  <br/>
Click Windows Defender Firewall Properties<br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.5.1%20vm%20windows%20defender%2C%20click%20windows%20defender%20firewall%20properties.png)
<br />

Turn off the firewall on: <br/>
- <b>Domain Profile</b> 
- <b>Private Profile</b>
- <b>Public Profile/b>

Click Apply and OK <br/>


![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.5.2%20turn%20off%20domain%2C%20private%2C%20public.png)
<br />

Firewalls are off  <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.5.3%20firewalls%20are%20off.png)
<br />

Use your personal computer to test connectivity to the VM. <br/>
Ping the IP address of the VM <br/>
It pings <br/>

![](https://github.com/rbrianshutt/azure_honeypot_live_cyber_attack/blob/main/SOC%20Lab/1.5.4%20use%20ping%20to%20test%20ability%20to%20connect%20to%20vm%20from%20own%20computer.png)
<br />








