---
layout: docs
title: Teams Migration Wiki
css: ['documents.css']
---

Many customers are beginning to take a closer look into T2M Teams Direct Routing as they begin to consider migrating their business telephony to Microsoft Teams and other solutions.
 
When considering a move of the PSTN voice service to Teams, a small pilot deployment involving a select limited group of users is recommended to evaluate the experience prior to the greater company-wide deployment.  It is important to convey and understand the interop and functional differences between Skype for Business (SfB) and Teams to these pilot users because once they have begun to use Teams, they will still be interacting with the majority SfB user base who have not yet migrated to Teams.  This is where understanding the interop experience is important, so that certain aspects of interoperability that are expected are not mistaken for "problems" during the evaluation process.
 
The primary interoperability or functionality characteristics to be aware of when using Teams are as follows:
  -Interop with Messaging, Audio/Video Calling, and presense will work between Voice+ & Teams Users at an organization. This allows for a staggered rollout
  -Desktop sharing between Teams and SfB users is not supported
  -A Teams user and a SfB user cannot do a file transfer between the differing clients
  -A chat between Teams and SfB user cannot be escalated to a meeting from the chat
  -The user’s pre-existing meetings scheduled for the future will be migrated from on-premises to Teams
  -If a meeting is created for Teams, then a SfB user must use Teams to join the meeting, and if a meeting is created in SfB, then the Teams user must join the SfB meeting using SfB. (Web clients will be used in absence of the desktop client)
  -Once in Teams Only mode, users cannot initiate calls or chats from Skype for Business, nor can they schedule new meetings in Skype for Business
  -Contacts that existed on premises are available in Teams shortly after the user logs on for the first time (Takes roughly 24 hours to appear)
  -3PIP phones provide only basic call controls for a Teams user - SLAs will not work on 3PIP phones only Teams certified phones
  -SLAs in the Voice+ service cannot ring users that have been moved to Teams. A new SLA would need to be created on the customer's M365 tenant
  -Legacy phones such as a CX600, CX700, HP 4120, etc will no longer work with Microsoft Teams
  -The user will be able to communicate with users in federated organizations
  -Once in Teams Only mode, users cannot initiate calls or chats from Skype for Business, nor can they schedule new meetings in Skype for Business
 
As a T2M Voice+ customer, it is important to understand that once a user has moved to Teams with T2M Direct Routing, the user management in the T2M Portal will be solely for number assigned and route assignment under the Teams App (https://my.t2mhosted.com/apps/teams/). Policies and other configurations for Teams must be managed within the Microsoft Teams Admin Center (https://admin.teams.microsoft.com/). Call details/related reporting, MACD activities, and any policy related configurations for Teams with T2M Direct Routing users are not available in the T2M portal at this time.
 
## Phase 1: User Migration Process
### Step 1: Set AD Attributes for All Users

In order to ensure a T2M Voice+ user can successfully move to Teams as well as ensure the conveyance of presence between Teams and SfB users, it is important to have the correct AD attributes set for the users who are using Teams with T2M Direct Routing. If the attributes described below are not correct, this could impact presence from working properly between Teams and SfB users. The following AD attributes must be set to the values shown in the customer on-premises AD and synced to Azure for any user homed on Skype for Business Server:
**AD Attribute** | **Value**
**msRTCSIP-DeploymentLocator** | SRV:
**msRTCSIP-OptionFlags** | 385
**msRTCSIP-UserEnabled** | TRUE
**msRTCSIP-PrimaryUserAddress** | sip:user@domain.com (User's SIP Address with sip:)

**Notes:**
  -If these attributes do not exist in your AD today, you will need to obtain a Skype for Business Server installation ISO from T2M to extend your AD schema and then refresh Azure AD Connect's AD Schema. 
  -T2M can also provide a script that can take exported SIP addresses from the T2M Voice+ service and allow you to import these values into your AD.
  -These attributes will need to stay in your AD for existing users, but new users will not need these set

Once these values are set, Skype for Business Online will report the following attributes after Azure AD Connect has synced the newly added AD attributes and Skype for Business Online has reprovisioned the users:
**Online Attribute** | **Value**
**InterpretedUserType**	| HybridOnpremSfBUser
**OnPremHostingProvider**	| SRV:
**OnPremOptionFlags**	| 385
**OnPremEnterpriseVoiceEnabled** | True
**OnPremSIPEnabled** | True
**OnPremSipAddress** | Null
**OnPremLineURI** | Null
**SipProxyAddress**	| sip:user@domain.com (User's SIP Address with sip:)
**EnterpriseVoiceEnabled** | False
**OnPremLineURIManuallySet** | False
**LineURI** | Null
**SipAddress** | sip:user@domain.com (User's SIP Address with sip:)
**Enabled** | True
**VoicePolicy**	| HybridVoice
**TeamsUpgradeEffectiveMode** | Islands or TeamsOnly
**RegistrarPool** |	Null
**HostingProvider**	| SRV:

### Step 2: Plan to Migrate a Group of Users

A group of users needs to be selected to be migrated to Teams. This can be a department, a random list of users, or the entire organization itself. Once these users have been selected, the numbers that are assigned to those users/services (Auto Attendants, Response Groups, etc.) need to be provided to T2M. Once T2M has this information, a date will be provided as to when the users will make the transition to Microsoft Teams/T2M Direct Routing. T2M will also confirm that the interpreted user type for the identified users in the customers tenant is set to **HybridOnPremisesSFBUser**

Note: If a customer is moving away from T2M and moving to Calling Plans from Microsoft, this date will reside on the port date of the phone numbers away from T2M

### Step 3: User Licensing

Users that were identified previously must have the following license(s) assigned for their migration to be successful:
  -Microsoft E1 & Microsoft Phone System (Dial-In Audio Conferencing Add-On is optional)
  -Microsoft E3 & Microsoft Phone System (Dial-In Audio Conferencing Add-On is optional)
  -Microsoft E5 (Dial-In Audio Conferencing and Microsoft Phone System Add-Ons are included)

With each of these license groups, the following apps will need to be enabled per user (These are on by default, but some organizations may have this set differently):
  -Exchange Online
  -Microsoft Teams
  -Skype for Business Online Plan 2 (P2)

Note: the customer is responsible for making sure that their user objects have the above licenses and apps assigned to each user that is part of the migration.

### Step 4: Migration Day

On the day of the user migration, T2M will confirm with the customer beforehand that the move process is still a go. Once this has been verified, T2M will begin the migration of the user objects from Skype for Business Server to Microsoft Teams at the selected time. A report will be given to the customer stating that the users are no longer homed on-premises and are now homed in the cloud.

The customer will need to modify the following AD attribute for each user in the batch in order to complete the user migration to Microsoft Teams:
**AD Attribute** | **Value**
**msRTCSIP-DeploymentLocator** | sipfed.online.lync.com

Note: These attributes will need to stay in your AD for existing users, but new users will not need these set. T2M Can also provide a script to assist with setting these attributes.

**Repeat Steps 2-4 for all remaining users before continuing to the next Phase**


## Phase 2: Migration away from T2M's Voice+ Service

Now that **ALL** user objects have been migrated to Microsoft Teams, the T2M Voice+ Service is still homing user objects and will cause issues for any new user being added to your organization with regards to external federation. These processes below will need to be completed to fully separate your organization away from the T2M Voice+ Service:

### Step 1: Remove Old DNS Records

The following DNS records need to be **removed** from your external DNS records (If using a split domain DNS setup, these will need to be fully removed from your internal DNS):

**A Records**
Hostname | Points to | TTL
sip | 54.69.103.113 | 3600 sec
sip | 54.191.68.13 | 3600 sec

**CNAME Records**
Hostname | Points to | TTL
lyncdiscover | lyncdiscover.t2mhosted.com | 3600 sec

**SRV Records**
Service | Protocol | Port | Weight | Priority | TTL | Name | Target
_sip | _tls | 5061 | 1 | 100 | 3600 sec | @ | edgeaccess.t2mdev.com
_sipfederationtls | _tcp | 5061 | 1 | 100 | 3600 sec | @ | edgeaccess.t2mdev.com

### Step 2: Add New DNS Records
After these records have been removed from your internal and/or external DNS, the following records need added back to ONLY your external DNS. Internal DNS does not need these as you are not signing into Skype for Business anymore and federation is handled only for external messages:

**CNAME Records**
Hostname | Points to | TTL
lyncdiscover | webdir.online.lync.com | 3600 sec
sip | sipdir.online.lync.com | 3600 sec

**SRV Records**
Service | Protocol | Port | Weight | Priority | TTL | Name | Target
_sip | _tls | 443 | 1 | 100 | 3600 sec | @ | sipdir.online.lync.com
_sipfederationtls | _tcp | 5061 | 1 | 100 | 3600 sec | @ | sipfed.online.lync.com.

### Step 3: Disable & Remove Hosting Controller's HC DirSync

Hosting Controller's HC DirSync that was used to sync AD objects to T2M will no longer be needed. To disable & remove the application, the following process must be completed:
  1. From the start menu navigate to **All Programs > HC Directory Sync** and then run **Uninstall HCDirSync** AS AN ADMINISTRATOR.
  2. Remove any sync groups from Active Directory. These are usually titled **(OUName_Sync)
  3. Inform T2M that the app has been removed along with the server's external IP so that licensing for it can be disabled and so that T2M can remove the IP from our firewall

### Step 4: Remove Skype for Business Online Hybrid Configuration

The shared sip address space attribute needs to be set to false since your tenant will no longer be communicating with T2M's Voice+ Platform. To do this you will need to connect to Skype for Business Online via PowerShell, however some prerequisites need to be put in place first:
  1. Install the Microsoft Online Services Sign-In Assistant: https://www.microsoft.com/en-us/download/details.aspx?id=41950
  2. Install the Skype for Business Online PowerShell Module: https://www.microsoft.com/en-us/download/details.aspx?id=39366

After this is installed, connect to Skype for Business Online via PowerShell with the following cmdlets: (Note: You will need to know your .onmicrosoft vanity domain)
*Import-Module SkypeOnlineConnector*
*$sfbSession = New-CsOnlineSession -OverrideAdminDomain t2m.onmicrosoft.com*
*Import-PSSession $sfbSession*

Once connected to Skype for Business Online via PowerShell, run the following cmdlet:
*Set-CsTenantFederationConfiguration -SharedSipAddressSpace $false*

Verify that the cmdlet took effect with the following cmdlet:
*Get-CsTenantFederationConfiguration*

### Step 5: Change Microsoft Teams Tenant Coexistence Mode

Now that all user objects are fully online, the tenant Coexistence Mode must be set to **Teams Only**. To do this navigate to the Microsoft Teams Admin Center (https://admin.teams.microsoft.com/) and select **Org-Wide Settings > Teams Upgrade** then change the **Coexistence Mode** to **Teams Only**. Click **Save** and a warning will appear confirming that you want to make this change. Click **Save** on this prompt to confirm the change.

![Cloud Portal](/assets/images/teamsmigration.1.png){:width="850px"}

## Migration Complete

Your organization has been removed from the T2M Voice+ platform and is now fully hosted on Microsoft Teams with or without T2M Direct Routing.