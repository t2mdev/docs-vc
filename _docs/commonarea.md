---
layout: docs
title: Common Area Management
css: ['documents.css']
---

## Main Page

The Common Area page is a powerful area of the portal that allows for the administration of all common area devices: 

![Cloud Portal](/assets/images/common.1.png){:width="750px"}

The common area page allows you to see all common area devices that are enabled for Skype for Business.  At the top of each column is the ability to filter rows based on a specific search criteria.  When selecting a common area device, a fly-out window will appear from the right side of the screen.  This will include the ability to modify properties and see call history.

## Modify Existing Common Area Device

When selecting a device from the table of existing common area devices, you will see the following page appear.

> **Important:** By default, editing is disabled when you open up any account.  You must select the Enable Editing button.  Once you do this, you can modify the settings for the account.  When you make a change, that change takes effect immediately.  **There is no save button required.**

![Cloud Portal](/assets/images/common.2.png){:width="750px"}

### Voice

**Phone Number** is the assigned phone number and extension for the common area device. Clicking on this dropdown box will display a list of all available unassigned numbers that can be assigned to the common area device.  

### Policies

**911 Policy** is extremely important – this determines how outgoing 911 calls from the common area device are routed. For organizations with one office, there will only be one 911 policy – however, organizations with multiple locations (or even multiple floors within a single building) must ensure that users have the proper 911 policy attached.  

**Routing Policy** is for organizations with mulitple routing options.  If your organization only has a single policy the option will be grayed out.

**Dial Plan** is for organizations with mulitple and advanced dial plans.  If your organization only has a single policy the option will be grayed out.

**Conference Policy** is for organizations with mulitple conferencing policies.  If your organization only has a single policy the option will be grayed out.

### Device PIN

The device pin is used to log in a common area device.  You must configure a pin and configure your network to use the necessary DHCP scopes for the device to login.

### Call History

Call History will bring you to a personalized Call Detail Record page for the common area device, including some basic info on their account details: 

Under General Information on the left, you will find the device SIP Address, the License Requirements of their account (dependent upon their active features), and whether PSTN Voice is enabled. (PSTN Voice describes whether the common area device account can place calls to traditional phone numbers). To the right you will see the common area device last 10 calls (conferences excluded). Double-clicking on any of these calls will bring you to the in-depth Call Detail page for that call, described more thoroughly in a later section.

## Creating a New Device

![Cloud Portal](/assets/images/common.3.png){:width="750px"}

1. Navigate to the Common Area tab by logging into the portal and clicking on "Common Area" on the left sidebar: 
2. Within the Common Area tab, click on "Add Common Area Device" at the top of the screen:
3. This will open the New Common Area dialog.  Enter all of the necessary information. 
4. Select the appropriate configurations for the new device: 
- Select the option for the common area device based on their location, 911 policy and phone number.  Click Create Common Area when completed.  If there are additional settings you need to modify, simply edit the common area device.
