---
layout: docs
title: Phone Setup
order: 2
css: ['documents.css']
category: phones
---

## Common Areas ##


The Common Area tab allows you to add, remove or modify common area phones for your organization. Common area phones are just what they sound like – phones in shared, semi-public areas that maCy be used by anyone who picks up the handset. Click on Common Area on the sidebar to view a listing of your active common area devices:

From here you may create new common area phones or modify the settings of existing ones by double-clicking on the device’s row. This will bring you to an Edit Common Area Device page, almost identical to the Edit User page described earlier in this document. 

To add a new common area phone, click Create Common Area Phone to the right of the search bar. This will bring you to the following page, similar to enabling a new User:

***It is important to note that common area devices REQUIRE PIN Authentication and the corresponding necessary network configuration changes in order to function. They also incur different per-month charges. If you are an existing customer who is interested in setting up common area phones for the first time, please contact your project manager BEFORE enabling any devices on this page. 

## Meeting Rooms ##

Clicking on Meeting Rooms in the sidebar will bring you to the Meeting Rooms page, where you may create, remove or modify meeting room devices:
 
 
Meeting Rooms function almost identically to regular users as far as enabling and modifying account details. For a step-by-step process please see section “Enabling A New User

## VVX Phone Setup ##

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


