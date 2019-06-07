---
layout: docs
title: Device Setup
css: ['documents.css']
---
## Polycom CX 600 Phone

### Physically Connecting the Phone

The first step in settin up and installing a VoIP phone is connecting all the necessary cables. You will need to:

1. Connect the phone to your network via Ethernet cable. This is typically done by disconnecting the Ethernet cable from your computer and plugging it into the phone's LAN port. There are multiple Ehternet ports on the phone- make sure that this cable is plugged into the LAN port and **not** the PC port.
2. Using a second Ethernet cable, connect the phone to the computer by plugging one end into the phone's PC port and other into the Ethernet port on your computer.
3. (OPTIONAL) Plug the power adapter into the back of the phone. This hsould start the initialization process for your phone.
4. Plug the USB Cable into the back of the phone and then connect to your computer. Make sure to fuly push the cable into the back of the phone. Your computer will download the drivers needed for the phone, this may take a few minutes.
5. At this time, your phone should be starting up. Allow the phone to complete the initialization process.
6. While the phone boots up, make sure to connect the handset with the cable provided. The plastic guide slides into the back of the phone to determine the angle it stands at.

### Configuring the Phone

1. Press the Select button to begin
2. Select Yes and choose English
3. Your computer will now prompt you to login again. The account and username should be the same as you use to log in to your Skype for Business Client.
4. The phone will start the login process. This might take a few minutes.
5. After login, enter your new 4 digit unlock pin. This pin exists to prevent people from checking your voicemail when you are away from your desk. By default, your phone logs into voicemail automatically when you are in the office. You will need to enteer it twice.
6. The phone will walk you through a wizard by selecting next. This will include choosing your time zone, date format, and more. Once completed, your phone is ready to be used.

### Using the Phone

### Transferring Calls

1. While on the call, click the menu button
2. Use the arrow key and select **Transfer Directly to...**
3. Use the arrow keys to select the name of the person you want to transfer to, or enter the phone number of who you want to transfer to.
4. Click the Right Select button to transfer the call.

## Polycom VVX Phone ##

The purpose of this guide is to walk you through the successful installation of a VVX Phone for use with Skype for Business in conjunction with Time2Market Cloud Services. Please note that the screenshots used throughout this guide may not match your phone exactly, as there are minor differences between VVX models. However, the fundamental menus involved are similar across all devices.  

### Connecting the Phone ###
The first step, of course, is connecting all the necessary cables. Luckily, there aren’t very many. You will need to: 
1.	Power the phone. This can be done either through a direct power adapter plugged into an AC outlet or through a Power over Ethernet (PoE) adapter.  
2.	Connect the phone to your network via Ethernet cable. This is typically done by disconnecting the Ethernet cable from your computer and plugging it into the phone’s LAN port. There are multiple Ethernet ports on the phone – make sure that this cable is plugged into the LAN port and not the Computer port.  
3.	Using a second Ethernet cable, connect the phone to the computer by plugging one end into the phone’s PC port and the other into the Ethernet port on your computer. This step is technically not required, but it will insure the best connectivity for configuration (and is necessary for BToE sign-in functionality).  

### Enable Web Server ###
In order to access the web-based confiuration menu, it is necessary that the Web Server option is enabled on the phone.
1. Press the Home key and then browse to the follwing menu: Settings>Advanced>(Enter default Admind code 456 on the keypad)>Administration Settings>Web Server Configuration
2.	Select Web Server and choose the Enabled option.  
3.	Select Web Config Mode and choose HTTP/HTTPS (barring a specific reason your organization has to choose another option) 
4.	Select Back and then Save Config to save the changes. The phone will now restart.  

### Verify & Update Software Version ###
Once the phone has restarted, you will next connect to the phone’s web server in order to verify and possibly update the software version.  
1.	On the phone go to Settings > Status > Network > TCP/IP Parameters and note the IP Address assigned to the phone.  If the phone does not have an IP Address, you need to troubleshoot why that is the case. A good place to start would be to double-check the physical connections to and from the phone.  
2.	Open a browser and connect to the IP Address.    
3.	Login to the phone with the default admin credentials of ‘456’ 
4.	On the resulting page, go to Utilities | Software Upgrade 
5.	Ensure that the version of software assigned to the phone is 5.2.x or later.  If the current software version is anything but this, click the “Check for Updates” button (leave Polycom Hosted Server selected). 
6.	The drop-down menu will now display a list of software versions you can install. Select the latest version and choose Install.  Your phone will reboot several times during this process, which can take up to 10 minutes.  

### Enable Lync Mode ###
After the phone has been upgraded, you must enable Lync Mode on the phone.
1. Hold down the key combo of 1, 4, & 9 for three seconds. It will display the Base Profile page. The default password is '456'
2. Selec Lync as the Base Profile. The phone will reboot after the selection.

### Sign in ###
There are two solutions for signing the phones in- Better Together over Ethernet (BToE) and Stand Alond Phone.

**BToE Sign-in**

First, we must enable BToE on the phone itself.
1. Click Home Button> Settings> Features> BTOE
2. Enable BTOE

Second, we must configure the workstation to pair with the phone.
1. Ensure your POlycom VVX Phone is tethered via Ethernet to your computer. The computer must be plugged in via wired/Ethernet connection that comes from the phone.
2. Ensure that the computer is not connected to Wi-Fi in addition to the wired Ethernet connection.
3. Download and install the latest version of Polycom BToE based on the firmware you have installed on your phone 
4. Launch the Polycom BToE application. You should see a message declaring a successful pairing with the phone within a minute. Once all drivers are installed, the computer will prompt for a restart.
5. Log out of Skype for Business/Lync client and log back in.
6. Your client will prompt you to log in to the phone. This can be delayed up to a minute after signing into the software itself. Input the same credentials you use to lof into Skype for Business/Lync.
7. Once your phone is logged in, you will see BToE as an option on the home screen.

**Stand Alone Phone Sign-in**

Depending on your phone, you may be immediately prompted on the phone itself for log-in credentials when the phone boots up. If this is the case, you may enter your sign-in information directly. Enter your entire Skype for Business / Lync user address into both the Sign-in Address and User Name fields. Enter your Skype for Business / Lync password into the Password field. You may leave the Domain and other fields blank.

You may also establish your credentials through the web configuration server.  

1. Navigate to the phone’s IP address and sign in as admin (456). 
2. Go to Utilities > Lync SignIn
3.	Enter your sign-in name, username and password.  You can leave domain, extension and pin blank.  
4.	Your phone will now be signed into Lync

### Enabling Audible Ringtone

By default, Polycom VVX phones are set to disable Shared Line Appearance (SLA) ring tones.  This means that the calls will “ring” the device, but the phone will be silent with no audible sound coming from the device.  Instead, the Skype for Business client will ring and use the default computer ring sound. Many end users prefer the phone itself to ring – the purpose of this guide is thus to provide the steps necessary in order to enable audible ringtones for shared line phones.  

1.	Press the Home button 
2.	Navigate to Settings -> Basic -> Ring Type and select your desired ringtone.  
3.	Hit back until prompted to save your configuration.

## SprectraLink 8440

The SpectraLink 8440 is a wireless phone offering certified for use with Skype for Business and Lync. The purpose of this document is to detail the first-time configuration of these devices, as they ship with several critical features disabled by default. By following this provisioning guide, the SpectraLink 8440 device is a viable wireless option for use with the Time2Market Cloud platform.  

In order to use the SpectraLink 8440, your device must be a SpectraLink with Lync and running firmware 4.13.0.1067 or later. Additionally, it is highly recommended to use a certified Access Point for most optimal voice experience.  The full list of certified Access Points can be found <a href="docs/products.html">here</a>

### Initial Configuration

The initial configuration begins with enabling the following features: 

* Enable Lync Mode 
* Enable WiFi 
* Enable Radio for WiFi 
* Enter SSID and Password for network connectivity 

This can be done with the following steps: 

1.	Click the Home Button on the phone. 
2.	Using the left and right buttons to navigate between menus, select Settings and press the OK button. 
3.	Choose Advanced Settings and enter the default Administrator password of 456. Then select Administrative Settings followed by Network Configuration: 
4.	Select Base Profile at the bottom of the list. 
5.	Press back to see full list of option under Network Configuration. 
6.	Choose Network Interfaces, the second option in the Network Configuration menu. 
7.	Choose Wi-Fi Menu. 
8.	Change Enabled from No to Yes. 
9.	Change SSID from “SSID1” to the SSID you wish to connect to (your Wi-Fi network name) 
10.	Change Security from None to the security type of your wireless access point (for example WPA2-PSK) 
11.	Change type of security to correct password.  For example, if WPA2-PSK was selected, choose the WPA2-PSK menu and enter the password for the SSID entered in step 12. 
12.	Choose Radio. 
13.	Change Regulatory Domain from None to 01. 
14.	Enable 5GHz and/or 2.4 GHz, depending on the access point you are using. 
15.	Press the left (back) button until the option to Save Config is presented.  Save the configuration and the phone will reboot. 

After the phone is rebooted, obtain the IP Address by going to Settings -> Status -> Network -> TCP/IP Parameters. 

### Provisioning the User and Logging In

You can either use a provisioning server to automatically log the device in, or you can manually configure the device using a username and password. 

**MANUAL LOGIN METHOD**

Open your web browser (Google Chrome is recommended; Internet Explorer may experience issues loading the web GUI). Navigate to the phone’s IP Address found in the section above (Settings -> Status -> Network -> TCP/IP Parameters) 
1.	Enter the default password of 456 to log in as administrator. 
2.	Choose Simple Setup. 
3.	Expand Time Synchronization and select the necessary information. 
4.	Choose Settings -> Lines 
5.	Under Identification, enter the SIP Address of the user. Display Name and Label may be left blank. 
6.	Under Authentication, choose Disable and enter the SIP Address under User ID and the password under Password. Domain may be left blank. 
7.	Click Save.  The phone should reboot. 
 
**PROVISIONING SERVER METHOD**

Open your web browser and navigate to the phone’s IP address. 
1.	Enter the default password of 456 to log in as administrator. 
2.	Choose Settings -> Provisioning Server 
3.	Enter the URL of your provisioning server 
4.	Choose Save.  Your phone should reboot and apply the settings as configured

## Windows DHCP Settings ##
The following steps are needed to configure Pin Authentication for DHCP/Common Area Phones.  These steps must be completed for each location.

If your site uses a Cisco Router for DHCP, download the Cisco DHCP Settings file and apply to your configuration.

1.	Download the following two files from the portal. 
    a.	Windows_DHCP.bat 
    b.	DHCPConfigScript.bat 
2.	Copy each file to your DHCP Server to C:\DHCP\ 
3.	Open Command Prompt as Administrator and navigate to the C:\DHCP folder 
4. Run: Windows_DHCP.bat 
5. The batch file will remove any existing scope options specific to Lync/Skype for Business and replace them with the correct values. 

To confirm your settings:

1. Open up DHCP and navigate to your IPv4 | Server Options.  You should now see the updated MSUCClient strings. 

NOTE: If your CX Series phones were previously logged into another server via Pin Auth, you must do a reset of the phone to clear these settings.
