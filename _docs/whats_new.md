---
layout: docs
title: What's New 
css: ['documents.css']
---

## July 2019 ##

The July 2019 Update comes with a complete rewrite of the T2M Cloud Complete portal for faster access, easier security options and more flexibility to add the features you want to help control your T2M Cloud Apps.  In addition to a completely new user interface that is easy and faster to use.  Make sure to see the [Accessing the Portal](https://docs.t2mhosted.com/docs/cloud.html#accessing-the-portal) for more details.

1. User Updates
- When creating a new user from a sync'ed account, SIP Address is now based off of the sync'ed SMTP (e-mail) address and not the UPN.  Administrators can click on the Show Advanced Naming option to override.
- When editing a user, administrators can now change both the UPN and SIP address.  Including the ability to support mismatched entries.
- When deleting a user, the underlying Active Directory account will automatically be deleted.  Organizations that use a sync tool will need to clear the required attributes and resync the account.
2. Common Area Devices
- Administrators can now edit the SIP Address for common area phones.
3. Meeting Rooms
- Administrators can now edit the SIP Address for meeting room devices.
- When deleting a meeting room, the underlying Active Directory account will automatically be deleted.  Organizations that use a sync tool will need to clear the required attributes and resync the account.
4. Call Groups
- Administrators can now create a call group without needing to submit a support ticket.
- Administrators can now delete a call group.
5. Reports
- All reports that are in table format now include the ability to export the table to CSV.
- All reports have been updated to respond quickly.  If a report is known to take more than 60 seconds a warning will appear.
6. Portal feedback can now be left directly within the portal and that feedback is routed to our Github repository immediately.
