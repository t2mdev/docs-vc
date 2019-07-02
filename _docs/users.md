---
layout: docs
title: User Management
css: ['documents.css']
---

## Main Page

The Users page is a powerful area of the portal that allows for the administration of individual user accounts: 

![Cloud Portal](/assets/images/user.1.png){:width="750px"}

Here you will see all of the users for your organization.  At the top of each column is the ability to filter rows based on a specific search criteria.  When selecting a user, a fly-out window will appear from the right side of the screen.  This will include the ability to modify properties, see call history and modify call forwarding.

## Modify Existing User

When clicking on a user, you will see the following page appear.

!Important: By default, editing is disabled when you open up any user account.  You must select the Enable Editing button.  Once you do this, you can modify the settings for the user.  When you make a change, that change takes effect immediately.  There is no save button required.

![Cloud Portal](/assets/images/user.2.png)

### Voice

**Enterprise Voice** must be checked in order for the user to have access to PSTN features. If unchecked, the user will not be able to communicate with traditional phone users. 
 
**Line URI** is the assigned phone number and extension for the user. Clicking on this dropdown box will display a list of all available unassigned numbers that can be assigned to the user.  
 
**Private Line URI** is a secondary, private line for the user that will ignore all delegate and team-ring rules otherwise established for the user’s main line. It is not necessary to assign a private line.  

## Policies

**911 Policy** is extremely important – this determines how outgoing 911 calls from the user are routed. For organizations with one office, there will only be one 911 policy – however, organizations with multiple locations (or even multiple floors within a single building) must ensure that users have the proper 911 policy attached.  

**Routing Policy** is for organizations with mulitple routing options.  If your organization only has a single policy the option will be grayed out.

**Dial Plan** is for organizations with mulitple and advanced dial plans.  If your organization only has a single policy the option will be grayed out.

**Conference Policy** is for organizations with mulitple conferencing policies.  If your organization only has a single policy the option will be grayed out.

**Client Policy** is the policy that applies to the user’s Skype for Business client.

**External Access Policy** controls if the user is able to communicate with federated partners or Skype Consumer clients 

### User PIN

The User PIN tab allows you to set a PIN that serves two purposes, described in the screenshot below (and on the tab itself within the portal): 

User PIN is not a necessary setting for most Skype for Business setups. In fact, it only serves two purposes – and if your organization does not use PIN Authentication for your phones, and you anticipate every conference call containing at least one Skype for Business user present, you do not need to worry about setting a User PIN for any user. 

### Call History

Call History will bring you to a personalized Call Detail Record page for the user, including some basic info on their account details: 

Under General Information on the left, you will find the user’s SIP Address, the License Requirements of their account (dependent upon their active features), and whether PSTN Voice is enabled. (PSTN Voice describes whether the user account can place calls to traditional phone numbers). To the right you will see the user’s last 10 calls (conferences excluded). Double-clicking on any of these calls will bring you to the in-depth Call Detail page for that call, described more thoroughly in a later section.

### Forwarding

Call Forwarding allows you to view and edit the Call Forwarding settings for any user in your organization. When you first click the Call Forwarding link in a user’s row, you will be brought to the following setting screen displaying their current settings: 

From this page you can alter the user’s call forwarding settings.

**Incoming Calls** can be set to either forward calls to or simultaneously ring 1) another Skype for Business user or 2) a telephone number. Calls can also be forwarded directly to Voicemail.  

**Unanswered Calls** can be set to go to Voicemail, another Skype for Business user, or a telephone number in anywhere from 5 to 60 seconds (in 5 second increments).  

Once you change a setting, a Save button will appear. Once clicked, these changes will be reflected in the user’s client immediately.  

The **Team Members** and **Delegate Members** tabs allow you to view the user’s team and delegate settings. At this time, technical limitations prevent remotely changing delegate relationships through the portal.  

## Enabling a New User

Prerequisites: If you do have an on premise Active Directory environment, ensure that the user has been added to the appropriate sync group. If you do not have an on premise Active Directory environment (or are unsure what that means) see the Create a New User below.

1. Navigate to the Users tab by logging into the portal and clicking on "Active Users" on the left sidebar: 
2. Within the Users tab, click on "Enable User" at the top right of the screen:
3. This will open the New User dialog. The user you wish to enable should be listed here.  (If the user you wish to add does not appear, please double check that the prerequisite step earlier in this section was completed) Check the box next to the user(s) that you wish to enable and click Move to Next Step.  
4. Select the appropriate configurations for the user(s): 

Select the option for the user based on their location and 911 policy.  Click Create User when completed.  If there are additional settings you need to modify, simply edit the user.

## Creating a New User

Prerequisites: This is for customers who do not have an Active Directory sync option.

1. Navigate to the Users tab by logging into the portal and clicking on "Active Users" on the left sidebar: 
2. Within the Users tab, click on "Add User" at the top right of the screen:
3. This will open the New User dialog.  Enter all of the necessary information for the user. 
4. Select the appropriate configurations for the user(s): 

Select the option for the user based on their location and 911 policy.  Click Create User when completed.  If there are additional settings you need to modify, simply edit the user..
