---
layout: docs
title: Windows DHCP Configuration Steps
depth: 1
css: ['documents.css']
---

<p>The following steps are needed to configure Pin Authentication for DHCP/Common Area Phones.  These steps must be completed for each location. </p>

<p>If your site uses a Cisco Router for DHCP, download the Cisco DHCP Settings file and apply to your configuration. </p>

1.	Download the following two files from the portal. 
a.	Windows_DHCP.bat 
b.	DHCPConfigScript.bat 
2.	Copy each file to your DHCP Server to C:\DHCP\ 
3.	Open Command Prompt as Administrator and navigate to the C:\DHCP folder 
4. Run: Windows_DHCP.bat 
5. The batch file will remove any existing scope options specific to Lync/Skype for Business and replace them with the correct values. 

<p>To confirm your settings: </p>

1. Open up DHCP and navigate to your IPv4 | Server Options.  You should now see the updated MSUCClient strings. 

<p>NOTE: If your CX Series phones were previously logged into another server via Pin Auth, you must do a reset of the phone to clear these settings. </p>
