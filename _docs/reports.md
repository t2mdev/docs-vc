---
layout: docs
title: Run Reports
css: ['documents.css']
category: reports
---


## Summary Report ##

The Summary Report gives an at-a-glance overview of your organization’s activity on a weekly basis: 

The report includes # of Unique Logins, # of IM sessions and IM messages, # of Audio Calls and Audio Minutes, # of Video Calls and Video Minutes, and the # of Application Sharing and File Transfers. Useful for an overall view of the organization as a whole, this report is exportable to PDF.  
 	 
## Currently Logged in Users ##

This report shows all logged in users, including detailed information on their devices and software client version: 

This report is updated live and can be exported to Excel. This report can also be accessed by clicking on the Person icon in the blue header bar spanning the portal.  

## IP Device Report ##

The IP Device report generates a full readout of all IP devices in use at your organization, past and present:  

Each of these columns provides useful information on these devices. 

* Manufacturer displays the manufacturer of the device. 
* Version displays the model number of the device. 
* MAC displays the MAC address. 
* User displays the SIP address of the user logged into (or who had been logged into) the device.  
* Last Logon Time and Last Logout Time are self-explanatory. 

## Login Report ##
The Login Report will give you a recent history of your organization’s logins, including the total number of logins and the # of unique users per day:
This report is also exportable to Excel. 
 	 
## Enabled Users ##
The Enabled Users report allows you to generate custom lists of your enabled users. You can add or remove a variety of columns to the reported table depending on your needs:  

After checking the boxes for columns you would like included, click “Update Table” to generate a new report. This report is exportable to Excel.  
 	 
## Locked Accounts ##
For security purposes, users accounts are locked after five consecutive incorrect password attempts. Using the Locked Accounts report, you can view which of your organization’s users are locked out. You will also see the time the account was locked out, as well as the option to Unlock the user instantly. If not unlocked manually, accounts will unlock after 30 minutes.

## User Ratings Report ##
The User Ratings Report displays the lowest ratings that each user in your organization has reported: 


The table’s first column displays the lowest rating the user has given for a call. The second column displays the total # of sessions the user has given a rating for when prompted. The pie chart displays the total breakdown of reported ratings, while the graph at the bottom displays the monthly average for the organization as a whole.  
Double-clicking on a row in the table will give you a detailed list of the user’s call quality reports, along with any feedback they entered when prompted by the client: 

## Call Quality Report ##
The Call Quality Report displays a bar graph of your organization’s aggregate call quality over the selected month:
 
This report takes every single call into account. The grading score is determined by a Microsoft formula that calculates the packet loss, jitter, round trip time and other call quality factors. A score of 91% is considered Good quality, 90% to 86% considered marginal, and anything below 86% is considered a poor call.  

This report displays an extremely detailed breakdown of any call determined by the system to have been of poor quality. It provides additional information and metrics that are useful in determining the cause of poor call quality for each case: 
The report can be modified by raising or lowering the acceptable level of packet loss / jitter / round trip to create a custom readout that fits your needs.   It is important to remember that the Skype for Business client uses a dynamic codec which will account for many of the issues on this report. Although the system will flag it as a poor call, it is possible that the end user did not experience any issues. 


The report is exportable to Excel.

## Conference Summary ##
The Conference Summary report displays metrics for the last 90 days of conference activity in your organization: 

It displays both the total number of conference participants, as well as the number of PSTN conference participants per days.  

## PSTN Conference Minutes ##
The PSTN Conference Minutes report displays the total number of PSTN call-second per conference, along with the organizer and number of participants: 

 
 	 
## PSTN Summary Report ## 
The PSTN Summary Report displays a table and graph of the total number and total minutes of PSTN calls per day within the chosen month: 

There are three phone number reports that display information regarding the allocation of phone numbers to your organization and users within your organization.  

The Number Range report displays the location, number range beginning, number range end, and the proportion of numbers that have already been allocated.  

The All Phone Numbers report displays all numbers assigned to your organization, as well as the Name the number is assigned to, what type of number it is (User, Meeting Room, Call Group, etc.) and whether it is available.

The Phone Numbers in Use report displays all numbers in use, along with the name, SIP address and type of user.  

## Call Details ## 
Possibly the most in-depth report of them all, the Call Details Report displays extremely specific information about an individual call involving one of your organization’s users. This report is accessible from several places in the portal: 

* From the Dashboard, by clicking “Call Info” next to any call in the Recent Activity list 
* From an individual user’s CDR Information page, by double-clicking on any of the user’s last 10 calls.  
* From the Active Calls report, first by clicking on the Phone icon in the blue header bar on every page of the Portal, then by double-clicking on the desired call (yes – this report updates LIVE, even during active calls!) 
Here is an example of the data included in this report: 
 
Call Details on the lefthand side displays some basic information such as the caller and callee user information, the platform they were calling on, the device used, and their network connection.  
Mid-Call Updates below shows any changes in network quality that occurred throughout the call. This is not present on every call report as some calls are completed without any substantive change in network quality.  
Call Overview on the righthand side displays detailed metrics of the call quality for the duration of the call. This is also where warning flags are displayed which could indicate possible (though not guaranteed) call quality issues.  
Call Status will display either In-Progress or Complete. 
Invite Time and End Time display the timestamps of the call’s beginning and end.  
Length is self-explanatory.  

Call Quality is a percentage figure based on a Microsoft formula that includes several call metrics such as packet loss, jitter, round trip time, and more. A score of 91% is considered Good quality, 90% to 86% considered marginal, and anything below 86% is considered a poor call. 

Lowest Stream Quality displays the worst point of call quality reached throughout the call. The possible values are Good, Poor and Bad. It’s important to note that this is not a metric of the call as a whole; it simply registers the lowest point. A 60minute call may experience 30 seconds of terrible packet loss and receive a Bad rating in this line despite overall high call quality.  

Packet Loss Avg (Max) displays the average packet loss for the duration of the call, as well as the maximum packet loss experienced at any point during the call (in parentheses).  
Jitter Avg (Max) displays the average jitter for the duration of the call, as well as the maximum jitter experienced at any point during the call (in parentheses).  

Round Trip Avg (Max) displays the average round trip in milliseconds for the duration of the call, as well as the maximum round trip experienced at any point during the call (in parentheses).  

Protocol displays whether the call occurred over UDP or TCP.  

Connectivity displays whether the call was DIRECT (peer-to-peer media connection) or RELAY (the media was transmitted over an intermediary such as an Edge / Mediation server) 

Network MOS Avg (Min) displays the MOS (Mean Opinion Score) calculated for the call, which is a traditional telephony metric for measuring call quality. A peer-to-peer VoIP call has a maximum score of 4.3, whereas a PSTN call has a maximum score of 3.71. Lower than 3.0 indicates poor call quality.  

Degradation Avg displays the average amount of degradation events that occurred during the call.  The degradation directly impacts the overall call quality score. 