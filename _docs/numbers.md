---
layout: docs
title: Numbers
css: ['documents.css']
---

The **T2M Numbers App** is the place to manage owned number ranges, check individual number assignments/avaliable numbers, request new numbers, and perform carrier-level forwards across all T2M voice services.

## Number Ranges

![Cloud Portal](/assets/images/numbers.1.png){:width="850px"}

The **Number Ranges** section of the T2M Numbers App displays all the number ranges that an organization owns. On this page, clicking on the description next to a number range will show the location that the DID range is assigned to, but it will also let the customer modify the description next to the number range. By default, T2M enters the description as the location when new numbers are provisioned against the customer's tenant. There is also the ability to export the data provided to an Excel .xlsx file.

![Cloud Portal](/assets/images/numbers.2.png){:width="850px"}

## Phone Numbers

 ![Cloud Portal](/assets/images/numbers.3.png){:width="850px"}

The **Phone Numbers** section of the T2M Numbers App displays all DID's from the number ranges assigned to a customer's tenant. This allows an organization to see who or what service is assigned to each DID and to find what DID's are avaliable for use. Some of the assignments types that are possbile are:
  -User
  -Exchange Contact
  -Dial-In Bridge
  -Trusted App
  -Common Area Phone
  -Meeting Room
  -$null - For Analog SIP Gateways

In order to see what numbers are avaliable for a customer, click on the dropdown under **Avaliable** and select **true**. Once this is selected, all avaliable numbers for assignment will show a circular checkbox next to the DID. 

![Cloud Portal](/assets/images/numbers.4.png){:width="850px"}

## Number Request

![Cloud Portal](/assets/images/numbers.5.png){:width="850px"}

The **Request** section of the T2M Numbers App allows a customer to submit a request to the T2M Help Desk to purchase and provision new DID's for their tenant. Information collected on the form includes:
  -Business Name
  -Service Address
  -Request Type
  -Quantity
  -Area Code
  -Sequential Numbers
  -CNAM

After the **Submit New Request** button is clicked, the request sent to the T2M Help Desk. Once recieved, the new numbers will be purchased and provisioned for the customer's tenant.

## PSTN Forward

![Cloud Portal](/assets/images/numbers.6.png){:width="850px"}

The **PSTN Forward** section of the T2M Numbers App allows a customer to create carrier-Level PSTN Forwards for their DID's. This allows forwards to be set outside of T2M's voice services and is able to forward DID's that are assigned to non-user objects.

## PSTN Forward - Creating a PSTN Forward

In order to create a forward for DID, Navigate to the T2M Numbers App > PSTN Forward > Add PSTN Number Forward. A flyout will open that will request the following information:
  -Source Number (Will only show owned DID's)
  -Destination
  -Note (Note to identify the forward such as "Elon Musk FWD to Cell")

![Cloud Portal](/assets/images/numbers.7.png){:width="850px"}

Once the requested information is entered, click the **Create Forward Request** button. A forward will be created with the assigned carrier within 30 seconds.

## PSTN Forward - Creating a Store Forward

If a customer's tenant provides services to a customer's retail stores, the **Store Forward** will be an avaliable feature. This allows store forwards to be completed by entering the source store Identifier and then the destination store number or other PSTN number. This will create a forward with the carrier that owns the source DID and take effect within 30 seconds.

In order to create a forward for a retail store, Navigate to the T2M Numbers App > PSTN Forward > Store Forward. A flyout will open that will request the following information:
  -Source Store Identifier (Usually 5 digits)
  -Destination (Store Identifier or PSTN Number)
  -The actual destination (5-digit store identifier or PSTN number)

![Cloud Portal](/assets/images/numbers.8.png){:width="850px"}

Once the requested information is entered, click the **Create Forward Request** button. A forward for the store will be created with the assigned carrier within 30 seconds.

## PSTN Forward - Removing a PSTN Forward

Once a PSTN Forward is no longer needed, it can be removed from the T2M Portal. In order to do this, navigate to the T2M Numbers App > PSTN Forward and then select the DID that you want to remove. Once selected, the PSTN Forward flyout will appear. Select the toggle next to **Do you want to remove this PSTN Forward?** and the **Delete PSTN Forward** button will appear. Click this and the forward will be removed from the carrier within 30 seconds.

![Cloud Portal](/assets/images/numbers.9.png){:width="850px"}