---
layout: docs
title: User Management
css: ['documents.css']
---

## Main Page

The Users page is a powerful area of the portal that allows for the administration of individual user accounts: 

The first 25 users in your organization are displayed automatically upon loading the page; for larger organizations, you may user the search bar to locate individual users. Displayed next to each user are three clickable links: Call History, Call Forwarding and Edit User. 
(TIP: Double-clicking anywhere within a user’s row will also open their Edit User page) 

## Call History

Call History will bring you to a personalized Call Detail Record page for the user, including some basic info on their account details: 

Under General Information on the left, you will find the user’s SIP Address, the License Requirements of their account (dependent upon their active features), and whether PSTN Voice is enabled. (PSTN Voice describes whether the user account can place calls to traditional phone numbers). To the right you will see the user’s last 10 calls (conferences excluded). Double-clicking on any of these calls will bring you to the in-depth Call Detail page for that call, described more thoroughly in a later section.

## Call Forwarding

Call Forwarding allows you to view and edit the Call Forwarding settings for any user in your organization. When you first click the Call Forwarding link in a user’s row, you will be brought to the following setting screen displaying their current settings: 

From this page you can alter the user’s call forwarding settings.

**Incoming Calls** can be set to either forward calls to or simultaneously ring 1) another Skype for Business user or 2) a telephone number. Calls can also be forwarded directly to Voicemail.  

**Unanswered Calls** can be set to go to Voicemail, another Skype for Business user, or a telephone number in anywhere from 5 to 60 seconds (in 5 second increments).  

Once you change a setting, a Save button will appear. Once clicked, these changes will be reflected in the user’s client immediately.  

The **Team Members** and **Delegate Members** tabs allow you to view the user’s team and delegate settings. At this time, technical limitations prevent remotely changing delegate relationships through the portal.  

## Edit User

The Edit User page allows for the management of specific users’ account settings. There are four tabs where user information can be modified: 

### Skype Options

NOTE: Your options may vary depending on your organization and policies available.

**Enterprise Voice** must be checked in order for the user to have access to PSTN features. If unchecked, the user will not be able to communicate with traditional phone users.  
 
**Line UR**I is the assigned phone number and extension for the user. Clicking on this dropdown box will display a list of all available unassigned numbers that can be assigned to the user.  
 
**Private Line URI** is a secondary, private line for the user that will ignore all delegate and team-ring rules otherwise established for the user’s main line. It is not necessary to assign a private line.  
 
**911 Policy** is extremely important – this determines how outgoing 911 calls from the user are routed. For organizations with one office, there will only be one 911 policy – however, organizations with multiple locations (or even multiple floors within a single building) must ensure that users have the proper 911 policy attached.  

**Client Policy** is the policy that applies to the user’s Skype for Business client.

**External Access Policy** controls if the user is able to communicate with federated partners or Skype Consumer clients 

### User PIN

The User PIN tab allows you to set a PIN that serves two purposes, described in the screenshot below (and on the tab itself within the portal): 

User PIN is not a necessary setting for most Skype for Business setups. In fact, it only serves two purposes – and if your organization does not use PIN Authentication for your phones, and you anticipate every conference call containing at least one Skype for Business user present, you do not need to worry about setting a User PIN for any user.  

### Contact Card/Address

These tabs allow you to modify the user’s Contact Card and Address information. This is not required. It is important to note that this information is publicly accessible to the user’s contacts in Skype for Business.  

It is also important to note that users with on premise Active Directory cannot make these changes in the Portal; they must be made within Active Directory instead.  

## Change Password

Changing a user’s password is very straightforward within the portal. Once you have navigated to a user’s Edit User page, simply click Change Password

This will bring you to the Change Password page, where the instructions and password guidelines are notated: 

## Enabling a New User

Prerequisites: If you do have an on premise Active Directory environment, ensure that the user has been added to the appropriate sync group. If you do not have an on premise Active Directory environment (or are unsure what that means), ensure that you have contacted T2M Support to create the user’s cloud account.

1. Navigate to the Users tab by logging into the portal and clicking on “Users” on the left sidebar: 
2. Within the Users tab, click on “Enable Users” at the top right of the screen:
3. This will open the New User dialog. The user you wish to enable should be listed here:(If the user you wish to add does not appear, please double check that the prerequisite step earlier in this section was completed) Check the box next to the user(s) that you wish to enable and click Move to Next Step.  
4. Select the appropriate configurations for the user(s): 

If your user will be using PSTN features, you will need to check the Enterprise Voice box. Select the appropriate Dial Plan, Client Policy, and External Access Policy for your user and then click Enable Users to save.  

Your user is now enabled for Cloud Complete! 

## Delegating Portal Administration Powers

The Cloud Complete Portal offers the ability to delegate administrative powers to different users in your organization in an extremely granular way. Using the Users & Roles menu, you can add users to five different administrative roles with different levels of control: 

If none of the preset roles suit your exact need, you can create your own custom organization roles as well. 
 
To access the Users & Roles menu, hover your mouse over your name in the top-corner of the Portal and click Users & Roles: 

### Users Tab

Once you click Users & Roles, you will be brought to the Users tab. This shows your existing administrative users and the roles they own:  

From here you may Add, Edit and Delete users to the preset roles available. Clicking Edit in a user’s row will allow you to change their access level as well as view their current powers in the portal: 

To Add a user to a preset role, click Add User. You will be brought to this page: 

 
Simply begin typing the name of any user in your organization in the Name Search box – they will populate automatically. Please note that users must already be active with Enterprise Voice in order to be selected as an administrative user. Select the appropriate preset from the Permissions drop-down and click Add User to save.  

### Roles Tab

Click on “Roles” as in the screenshot below to navigate to the Roles tab, where you may set up custom roles for your organization: 

This will bring you to the Roles page, which displays a readout of the permissions granted to each of the preset roles, as well as a listing of your organization’s existing custom roles. Click Add Role to add a new custom role: 

The Add Role page allows you to mix and match Read and Edit capabilities for a variety of Portal functions: 

**Manage Users & Roles** allows the user to add, edit, and delete users and roles – this is the highest level of access, and we recommend that it be reserved for global administrators.  
**Billing Menu** allows the user access to the billing menu for license information.  
**Support Menu** allows the user to submit support requests to the Time2Market Cloud support team.  
 
**Users, Common Area, Meeting Rooms and Call Groups** – if Read is checked, the administrator will be able to view existing information regarding these users / rooms / groups. If Edit is checked, the administrator will be able to reset passwords, change user phone numbers, edit call group membership, etc.  
 
To create a custom role, select the options you would like available, enter a Role Name and click Save Changes & Add Role. Remember to add user to the role group once the role is created.  
