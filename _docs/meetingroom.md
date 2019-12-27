---
layout: docs
title: Meeting Room Management
css: ['documents.css']
---

## Main Page

The Meeting Room page is a powerful area of the portal that allows for the administration of individual meeting room devices: 

![Cloud Portal](/assets/images/meeting.1.png){:width="850px"}

The meeting room page allows you to see all devices enabled for Skype for Business.  At the top of each column is the ability to filter rows based on a specific search criteria.  When selecting a meeting room, a fly-out window will appear from the right side of the screen.  This will include the ability to modify properties and see call history.

## Modify Existing Meeting Room

When selecting a meeting room from the table of existing list, you will see the following page appear.

> **Important:** By default, editing is disabled when you open up any account.  You must select the Enable Editing button.  Once you do this, you can modify the settings for the account.  When you make a change, that change takes effect immediately.  **There is no save button required.**

![Cloud Portal](/assets/images/meeting.2.png){:width="850px"}

### Voice

**Enterprise Voice** must be enabled in order for the room to have access to PSTN features. If disabled, the room will not be able to communicate with traditional phone users. 
 
**Line URI** is the assigned phone number and extension for the room. Clicking on this dropdown box will display a list of all available unassigned numbers that can be assigned to the room.  
 
**Private Line URI** is a secondary, private line for the room that will ignore all delegate and team-ring rules otherwise established for the room main line. It is not necessary to assign a private line.  

### Policies

**911 Policy** is extremely important – this determines how outgoing 911 calls from the room are routed. For organizations with one office, there will only be one 911 policy – however, organizations with multiple locations (or even multiple floors within a single building) must ensure that rooms have the proper 911 policy attached.  

**Routing Policy** is for organizations with mulitple routing options.  If your organization only has a single policy the option will be grayed out.

**Dial Plan** is for organizations with mulitple and advanced dial plans.  If your organization only has a single policy the option will be grayed out.

**Conference Policy** is for organizations with mulitple conferencing policies.  If your organization only has a single policy the option will be grayed out.

**Client Policy** is the policy that applies to the room Skype for Business client.

**External Access Policy** controls if the room is able to communicate with federated partners or Skype Consumer clients 

### Room PIN

Room PIN is not a necessary setting for most Skype for Business setups. In fact, it only serves two purposes – and if your organization does not use PIN Authentication for your phones, and you anticipate every conference call containing at least one Skype for Business user present, you do not need to worry about setting a Room PIN for any room. 

### Call History

Call History will bring you to a personalized Call Detail Record page for the meeting room, including some basic info on their account details: 

Under General Information on the left, you will find the room's SIP Address, the License Requirements of their account (dependent upon their active features), and whether PSTN Voice is enabled. (PSTN Voice describes whether the room account can place calls to traditional phone numbers). To the right you will see the rooms last 10 calls (conferences excluded). Double-clicking on any of these calls will bring you to the in-depth Call Detail page for that call, described more thoroughly in a later section.

## Enabling a New Meeting Room

Prerequisites: If you do have an on premise Active Directory environment, ensure that the account has been added to the appropriate sync group. If you do not have an on premise Active Directory environment (or are unsure what that means) see the Create a New Meeting Room below.  If you do not have an on premises Active Directory environment please contact support to assist.

![Cloud Portal](/assets/images/meeting.3.png){:width="850px"}

1. Navigate to the Meeting Room tab by logging into the portal and clicking on "Meeting Rooms" on the left sidebar: 
2. Within the Meeting Room tab, click on "Enable Meeting Room" at the top of the screen:
3. This will open the New Meeting Room dialog.  Select an existing account from the drop down that you wish to enable.
- If the account you wish to add does not appear, please double check that the prerequisite step earlier in this section was completed. 
4. Select the appropriate configurations for the meeting room:
- Select the option for the meeting room based on their location and 911 policy.  Click Create Meeting Room when completed.  If there are additional settings you need to modify, simply edit the meeting Room.

