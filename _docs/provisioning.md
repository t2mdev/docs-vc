---
layout: docs
title: Phone Provisioning
css: ['documents.css']
---

## Main Page

The Phone Provisioning Management Application allows you to manage your Poly VVX phones for Teams, Skype for Business or Standard SIP Services.  No on-premises servers or proxies are needed; as long as your phones can connect to our Cloud Servers your phones can receive your configuration. Phones can be provisioned by single configuration, logical locations or via small groups.

![Cloud Portal](/assets/images/provisioning.1.png){:width="750px"}

## Configurations

The T2M Works Provisioning Tools allows you are create one or many different configurations.  Each configure could represent a single company set of phones or you could use each configuration as a physical building location.  Within each Configuration, you can segment your phones into logical groups.

![Cloud Portal](/assets/images/provisioning.2.png){:width="750px"}

When you click on an individual configuration, you will see all of the options exposed for that device.  By default, your configuration will contain no configuration settings and you must choose which values you want to enable for that configuration.

For example, if you wanted to set the *Line Appearance* to display as *Name* you would check the box next to Line Appearance and select the cooresponding value from the drop down list.

![Cloud Portal](/assets/images/provisioning.3.png)

When you have finished making your changes, click the Generate VVX Files button from the bottom of the screen.  This will generate the necessary files for your phones based on the configuration you created.

**Important:** You do not need to click Generate VVX files as you navigate from tab to tab.  Simply click the box at the end of the configuration.

## Configuration Settings

After you have generated your first set of configuration files the options within the Settings Tab.

![Cloud Portal](/assets/images/provisioning.4.png){:width="750px"}

### DHCP Configuration

If your organization wants to push the configuration to all phones you should use the DHCP String supplied and configure it within your DHCP Servers.  Note that this will impact ALL devices that your DHCP Server has access to.

### Manual Configuration

Perfect for testing and smaller deployments, you can manually set the configuration Location information directly in the phone.  By navigating to Settings | Provisioning Server on an individual VVX device you can manually enter the supplied provisioning server information.

### Configuration Files

If you would rather use your own FTPS server, you can download the provisioning files or simply review what settings were set.

## Groups

Groups are a subset of a configuration.  Each configuration can have an unlimited number of Groups.  The groups are helpful to organize phones into a smaller subset of devices.  For example, you could create a group of phones for testing of configuration on a smaller population of devices.  Groups can also be helpful for devices that serve a different purpose, such as Common Area or Meeting Room Devices.

![Cloud Portal](/assets/images/provisioning.5.png){:width="750px"}

The configuration of a group is no different than the configuration settings of a parent configuration.  When create a new group, it will inherent the settings of the parent configuration but once you make changes those changes are now unique to the group.

## Devices

Devices allow you to see all devices that have checked into each configuration.  Additionally, you can see if a device is assigned to particular group within a configuration.

![Cloud Portal](/assets/images/provisioning.6.png){:width="750px"}

When you click on the device, you will see additional settings including the firmware version that is currently running, IP Address (if known) and the ability to download individual configuration files and App and Boot Log files.

![Cloud Portal](/assets/images/provisioning.7.png){:width="750px"}
