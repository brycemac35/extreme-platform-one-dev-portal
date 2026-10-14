---
title: 'Extreme Platform ONE Networking and ExtremeCloud IQ v25.14.0 Licensing Guide Sep 2026'
source: https://documentation.extremenetworks.com/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.pdf
pages: 60
---

# Extreme Platform ONE Networking and ExtremeCloud IQ v25.14.0 Licensing Guide Sep 2026

Source PDF: [Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.pdf](../../pdfs/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.pdf)

<!-- page 1 -->

Extreme Platform ONE ™ Networking and
ExtremeCloud IQ v25.14.0
Licensing Guide
Subscription and License Types, Management, and Troubleshooting
9041243-00 Rev AA
September 2026


<!-- page 2 -->

Copyright © 2026 Extreme Networks, Inc. All rights reserved.
Legal Notice
Extreme Networks, Inc. reserves the right to make changes in specifications and other information
contained in this document and its website without prior notice. The reader should in all cases consult
representatives of Extreme Networks to determine whether any such changes have been made.
The hardware, firmware, software or any specifications described or referred to in this document are
subject to change without notice.
Trademarks
Extreme Networks and the Extreme Networks logo are trademarks or registered trademarks of Extreme
Networks, Inc. in the United States and/or other countries.
All other names (including any product names) mentioned in this document are the property of their
respective owners and may be trademarks or registered trademarks of their respective companies/
owners.
For additional information on Extreme Networks trademarks, see: https://www.extremenetworks.com/
about-extreme-networks/company/legal/trademarks
Open Source Declarations
Some software files have been licensed under certain open source or third-party licenses. End-user
license agreements and open source declarations can be found at: https://www.extremenetworks.com/
support/policies/open-source-declaration/


<!-- page 3 -->

Table of Contents
Abstract................................................................................................................................................................................................................................v
Preface................................................................................................................................................................................................................................. vi
Text Conventions............................................................................................................................................................................................... vi
Documentation and Training................................................................................................................................................................... vii
Open Source Declarations............................................................................................................................................................ viii
Training......................................................................................................................................................................................................... viii
Send Feedback.................................................................................................................................................................................................viii
Help and Support............................................................................................................................................................................................viii
Subscribe to Product Announcements..................................................................................................................................ix
Extreme Support Portal......................................................................................................................................................................ix
Extreme Platform ONE Networking™ and ExtremeCloud IQ Subscriptions...................... 12
License Entitlement Management....................................................................................................................................................... 12
Link Your Extreme Portal Account | Extreme Platform ONE Networking or ExtremeCloud IQ
(New)..........................................................................................................................................................................................................................14
Link Your Extreme Portal Account | ExtremeCloud IQ (Classic).................................................................................... 14
Unlink and Relink Your Extreme Portal Account | Extreme Platform ONE Networking and
ExtremeCloud IQ (New)............................................................................................................................................................................... 15
Unlink and Relink Your Extreme Portal Account | ExtremeCloud IQ (Classic)..................................................... 16
Trial Subscriptions............................................................................................................................................................................................16
Trial Subscription Eligibility............................................................................................................................................................. 17
Request a Trial Subscription...........................................................................................................................................................17
Upgrading to Extreme Platform ONE................................................................................................................................................. 18
What to Expect With a Mixed-Subscription Deployment.......................................................................................18
Unlocking Full Features.................................................................................................................................................................... 20
Subscriptions and Licenses............................................................................................................ 23
ExtremeCloud IQ Pilot..................................................................................................................................................................................23
ExtremeCloud IQ CoPilot...........................................................................................................................................................................24
ExtremeCloud IQ Navigator.....................................................................................................................................................................25
ExtremeCloud IQ NAC................................................................................................................................................................................. 25
Third-Party Management Engine.........................................................................................................................................................26
Premier Switch Features............................................................................................................................................................................26
MACsec Switch Features...........................................................................................................................................................................27
Extreme Platform ONE Standard Networking.............................................................................................................................27
ExtremeCloud IQ Pilot Twin Subscription Provides Backwards Compatibility................................................. 29
Subscription Tier Priorities.......................................................................................................................................................................29
Additional Requirements...........................................................................................................................................................................30
ExtremeCloud IQ Controller......................................................................................................................................................................31
ExtremeCloud IQ Site Engine...................................................................................................................................................................31
Automatic Subscription Alignment....................................................................................................................................................32
Subscription Expiration...............................................................................................................................................................................33
ExtremeCloud IQ Legacy Entitlement Keys.................................................................................................................................33
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 iii


<!-- page 4 -->

Subscription Part Numbers.............................................................................................................34
Management | Extreme Platform ONE™ Networking & ExtremeCloud IQ (New) ............37
Subscriptions and Account Linking...................................................................................................................................................37
ExtremeCloud IQ Pilot Twin Subscription Provides Backwards Compatibility.......................................38
Subscription Management.......................................................................................................................................................................38
Subscription Management Example...................................................................................................................................... 39
Subscriptions & Licensing User Interface........................................................................................................................... 41
Purchase a Subscription................................................................................................................................................................. 42
Create a Subscription Request.................................................................................................................................................. 42
Add Subscriptions to an Existing Enterprise Agreement Contract................................................................43
Renew a Subscription........................................................................................................................................................................44
Add a Note to a Subscription......................................................................................................................................................44
View Subscription History..............................................................................................................................................................45
General Subscription Management...................................................................................................................................................45
Activate a Subscription....................................................................................................................................................................45
View the License Pool.......................................................................................................................................................................46
Manage NAC Allocations | Extreme Platform ONE and ExtremeCloud IQ (New)..................................46
View Device State and Subscription Type.........................................................................................................................47
Pre-provisioning and Subscription Assignment............................................................................................................47
Contracts.............................................................................................................................................................................................................. 48
Contract Status Descriptions..................................................................................................................................................... 48
View Contract Information............................................................................................................................................................49
Quick-Filter Contracts by a Pending Expiration Interval........................................................................................ 49
Filter Contracts by Specified Date Range..........................................................................................................................49
Filter Contracts by Type or Status..........................................................................................................................................50
Filter Contracts by Multiple Criteria...................................................................................................................................... 50
Download the Contracts Table....................................................................................................................................................51
Renew a Contract.................................................................................................................................................................................. 51
Contact Sales............................................................................................................................................................................................51
Management | ExtremeCloud IQ (Classic).................................................................................. 52
View the License Pool..................................................................................................................................................................................52
Manage NAC Allocations | ExtremeCloud IQ.............................................................................................................................. 53
Proactive Notifications................................................................................................................................................................................53
Enable or Disable Proactive Email Notifications............................................................................................................54
Entitlement Violations................................................................................................................................................................................. 54
ExtremeCloud IQ Pilot and Extreme Platform ONE Networking........................................................................ 54
ExtremeCloud IQ Navigator.......................................................................................................................................................... 55
ExtremeCloud IQ CoPilot................................................................................................................................................................55
ExtremeCloud IQ NAC.......................................................................................................................................................................56
Activate or Revoke an ExtremeCloud IQ CoPilot Subscription..................................................................................... 57
Affected Devices Table............................................................................................................................................................................... 57
Pre-provisioning and Subscription Assignment.......................................................................................................................57
Troubleshooting................................................................................................................................................................................................58
Table of Contents
iv Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 5 -->

Abstract
This licensing guide for Extreme Platform ONE Networking and ExtremeCloud IQ version 25.14.0
covers subscription types, license entitlement management, and troubleshooting for network
administrators managing device entitlements across cloud and on-premises deployments.
The guide details License Entitlement Management (LEM), an automated system that assigns
subscriptions from a license pool tied to a linked Extreme Portal account, and distinguishes
licenses from entitlements. It documents available subscription types (Tiers A through D
and 3RD)—along with subscription tier priorities, device eligibility rules, and ExtremeCloud
IQ Pilot Twin subscriptions for backward compatibility with older ExtremeCloud IQ Site
Engine and Controller versions. Management procedures are provided for Extreme Platform
ONE Networking, ExtremeCloud IQ (New), and ExtremeCloud IQ (Classic), covering account
linking, NAC allocation, mixed-subscription deployments, unlocking full features, contract
management, and pre-provisioning. The guide also addresses trial subscription eligibility,
automatic subscription alignment and expiration handling, and proactive entitlement violation
notifications. Intended audience: network administrators with intermediate-to-advanced
technical proficiency.
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 v


<!-- page 6 -->

Preface
Read the following topics to learn about:
• The meanings of text formats used in this document.
• Where you can find additional information and help.
• How to reach us with questions and comments.
Text Conventions
Unless otherwise noted, information in this document applies to all supported environments
for the products in question. Exceptions, like command keywords associated with a specific
software version, are identified in the text.
When a feature, function, or operation pertains to a specific hardware product, the product
name is used. When features, functions, and operations are the same across an entire product
family, such as Extreme Networks switches, the product is referred to as the switch.
Table 1: Notes and warnings
Icon Notice type Alerts you to...

Tip Helpful tips and notices for using the product

Note Useful information or instructions

Important Important features or instructions

Caution Risk of personal injury, system damage, or loss of data

Warning Risk of severe personal injury
vi Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 7 -->

Table 2: Text
Convention Description
screen displays This typeface indicates command syntax, or represents
information as it is displayed on the screen.
The words enter and type When you see the word enter in this guide, you must type
something, and then press the Return or Enter key. Do not press
the Return or Enter key when an instruction simply says type.
Key names Key names are written in boldface, for example Ctrl or Esc. If you
must press two or more keys simultaneously, the key names are
linked with a plus sign (+). Example: Press Ctrl+Alt+Del
Words in italicized type Italics emphasize a point or denote new terms at the place
where they are defined in the text. Italics are also used when
referring to publication titles.
New information. In a PDF, this is searchable text.
Table 3: Command syntax
Convention Description
bold text Bold text indicates command names, keywords, and command
options.
italic text Italic text indicates variable content.
[ ] Syntax components displayed within square brackets are
optional.
Default responses to system prompts are enclosed in square
brackets.
{ x | y | z } A choice of required parameters is enclosed in curly brackets
separated by vertical bars. You must select one of the options.
x | y A vertical bar separates mutually exclusive elements.
< > Nonprinting characters, such as passwords, are enclosed in
angle brackets.
... Repeat the previous element, for example, member[member...].
\ In command examples, the backslash indicates a “soft” line
break. When a backslash separates two lines of a command
input, enter the entire command at the prompt without the
backslash.
Documentation and Training
Find Extreme Networks product information at the following locations:
Current Product Documentation
Release Notes
Preface Documentation and Training
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 vii


<!-- page 8 -->

Hardware and Software Compatibility for Extreme Networks products
Extreme Optics Compatibility
Other Resources such as articles, white papers, and case studies
Open Source Declarations
Some software files have been licensed under certain open source licenses. Information is
available on the Open Source Declaration page.
Training
Extreme Networks offers product training courses, both online and in person, as well as
specialized certifications. For details, visit the Extreme Networks Training page.
Send Feedback
The User Enablement team at Extreme Networks has made every effort to ensure that this
document is accurate, complete, and easy to use. We strive to improve our documentation
to help you in your work, so we want to hear from you. We welcome all feedback, but we
especially want to know about:
• Content errors, or confusing or conflicting information.
• Improvements that would help you find relevant information.
• Broken links or usability issues.
To send feedback, email us at Product-Documentation@extremenetworks.com.
Provide as much detail as possible including the publication title, topic heading, and page
number (if applicable), along with your comments and suggestions for improvement.
Help and Support
If you require assistance, contact Extreme Networks using one of the following methods:
Extreme Portal
Search the GTAC (Global Technical Assistance Center) knowledge base; manage support
cases and service contracts; download software; and obtain product licensing, training,
and certifications.
The Hub
A forum for Extreme Networks customers to connect with one another, answer questions,
and share ideas and feedback. This community is monitored by Extreme Networks
employees, but is not intended to replace specific guidance from GTAC.
Call GTAC
For immediate support: (800) 998 2408 (toll-free in U.S. and Canada) or 1 (408) 579 2800.
For the support phone number in your country, visit www.extremenetworks.com/support/
contact.
Open Source Declarations Preface
viii Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 9 -->

Before contacting Extreme Networks for technical support, have the following information
ready:
• Your Extreme Networks service contract number, or serial numbers for all involved Extreme
Networks products
• A description of the failure
• A description of any actions already taken to resolve the problem
• A description of your network environment (such as layout, cable type, other relevant
environmental information)
• Network load at the time of trouble (if known)
• The device history (for example, if you have returned the device before, or if this is a
recurring problem)
• Any related RMA (Return Material Authorization) numbers
Subscribe to Product Announcements
You can subscribe to email notifications for product and software release announcements,
Field Notices, and Vulnerability Notices.
1. Go to The Hub.
2. In the list of categories, expand the Product Announcements list.
3. Select a product for which you would like to receive notifications.
4. Select Subscribe.
5. To select additional products, return to the Product Announcements list and repeat steps
3 and 4.
You can modify your product selections or unsubscribe at any time.
Extreme Support Portal
The Extreme Networks Extreme Support Portal provides access to:
• License management
• Firmware downloads
• Case management
• GTAC Knowledge base
• And more
To access the portal, you must first create an account. The Extreme Support Portal provides
separate registration forms for End Customers and Partners.
Before you begin, gather the following: A valid corporate email address — required to receive
the appropriate level of portal access. Your company details: company name, address, phone
number (include country code if outside the US), job title, and job role. At least one supporting
identifier: Sold-to number, serial number, contract number, or Purchase Order (PO) number.
Preface Subscribe to Product Announcements
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 ix


<!-- page 10 -->

Create an End Customer Extreme Support Portal Account
The Extreme Support Portal provides separate registration forms for End Customers and
Partners. Use this task to create an End Customer account.
Note
If you are adding a new user to an existing account, the new user must complete and
be vetted through the same registration process.
The portal registration page is at https://extreme-networks.my.site.com/.
1. Go to the Extreme Support Portal and select Login or Signup on the login page.
2. On the login page, select Create a new Extreme Customer Portal Account .
3. Complete all required fields (marked *). Use your corporate email address to ensure the
appropriate access level.
Important
Do not register with a personal email address.
4. Read the Support Portal Terms of Use and select the acknowledgment check box to accept.
Important
You must accept the Terms of Use before you can submit the form. You can adjust
or withdraw consent at any time through the Email Preference Center.
5. Select Register.
A confirmation message appears on the page and a password setup email is sent to your
corporate email address.
6. Open the password setup email and follow the instructions to create your portal password.
Tip
If the email does not appear in your inbox within a few minutes, check your spam
or junk mail folder.
7. To log in to the support portal go to: https://extremesaas.my.site.com/.
Create a Partner Extreme Support Portal Account
The Extreme Support Portal provides separate registration forms for End Customers and
Partners. Use this task to create a Partner account.
The portal registration page is at https://extreme-networks.my.site.com/.
1. Go to the Extreme Support Portal and select Login or Signup on the login page.
2. On the login page, select Create a new Extreme Partner Portal Account.
3. Complete all required fields (marked *). Use your corporate email address to ensure the
appropriate access level.
Important
Do not register with a personal email address.
Extreme Support Portal Preface
x Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 11 -->

4. Read the following terms and select the required check boxes:
• Support Portal Terms of Use
• Extreme Networks Standard Reseller Terms and Conditions
• Trade Compliance Terms and Conditions
You can adjust or withdraw consent at any time through the Email Preference Center.
5. Select Register.
A confirmation message appears on the page and a password setup email is sent to your
corporate email address.
6. Open the password setup email and follow the instructions to create your portal password.
Tip
If the email does not appear in your inbox within a few minutes, check your spam
or junk mail folder.
7. To log in to the support portal go to: https://extremesaas.my.site.com/.
Preface Extreme Support Portal
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 xi


<!-- page 12 -->

Extreme Platform ONE Networking™ and
ExtremeCloud IQ Subscriptions
License Entitlement Management on page 12
Link Your Extreme Portal Account | Extreme Platform ONE Networking or ExtremeCloud
IQ (New) on page 14
Link Your Extreme Portal Account | ExtremeCloud IQ (Classic) on page 14
Unlink and Relink Your Extreme Portal Account | Extreme Platform ONE Networking and
ExtremeCloud IQ (New) on page 15
Unlink and Relink Your Extreme Portal Account | ExtremeCloud IQ (Classic) on page 16
Trial Subscriptions on page 16
Upgrading to Extreme Platform ONE on page 18
All managed network devices require subscriptions. This document describes the available
subscription types, the requirements, and how to order and manage subscriptions using the
following management applications:
• Extreme Platform ONE Networking
• ExtremeCloud IQ (New)
• ExtremeCloud IQ (Classic)
Note
All instances of ExtremeCloud IQ in this document refer to both ExtremeCloud IQ
(Classic) and ExtremeCloud IQ (New), unless otherwise noted.
The terms License and Entitlements are not interchangeable. For more information,
see Table 4 on page 13.
License Entitlement Management
License Entitlement Management (LEM) is a system that enables automatic subscription
management. Subscriptions are not tied to specific device serial numbers, but instead stored
in the license pool in your Extreme Portal Account. When your management application and
Extreme Portal Account are linked, subscription assignment occurs automatically when you
onboard new devices or when devices transition from the unmanaged to the managed state.
Automatic subscription assignment requires sufficient subscriptions to cover all devices.
12 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 13 -->

For more information about the terminology used in this guide, see Table 4.
Table 4: Terminology
Term Definition
Contract A record of the number of subscriptions and or support services
in a purchase order, including their start and end dates. Each line
item in a contract includes the quantity of subscriptions for the
application or support service.
Contract Number Each contract has a unique Contract Number—previously known
as the Contract ID.
CUID A customer account ID, assigned by Extreme Networks to manage
subscriptions. Customers typically have a single CUID, while MSPs
can have multiple CUIDs.
Entitlement Entitlement refers to the right to use a feature or function. There
might be multiple entitlements for one subscription. For instance,
a subscription can include a cloud management entitlement and a
TAC/OS entitlement.
Typically, an entitlement has a meter that determines the unit of
measure for the feature it covers. For instance, an entitlement can
be per-device or per-user.
License A license is required for the perpetual use of software and is
typically downloaded or delivered with hardware. It defines the
rights and restrictions of software usage for the user.
Managed Device A managed device that is assigned a subscription and is managed
by the cloud, Site Engine, or a controller. Managed devices can
be monitored by Extreme Networks applications, and can be in
Connected or Disconnected states.
Subscription A subscription gives a customer the right to use an application,
feature, or function for a defined period of time. A subscription
has a start date and an end date. For example, a customer
might purchase 30 subscriptions of Tier A, whereby each Tier
A subscription contains an entitlement for management and
TAC/OS. Premier subscriptions also include an entitlement for
Premier support.
Subscription Group A subscription group is a group of subscriptions that have the
same start and end date, and are of the same subscription type.
Subscription Status A subscription can be Active, Inactive, or Expired:
• Active means the start date is in the past, and the end date is
in the future.
• Inactive means the start date is in the future.
• Expired means the end date is in the past.
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions License Entitlement Management
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 13


<!-- page 14 -->

Table 4: Terminology (continued)
Term Definition
Support Services Support services provide assistance to ensure effective product
operation and maintenance, and the resolution of product-related
issues. These are available for standalone purchase, or as part of
certain subscriptions.
Unmanaged Device An unmanaged device is a device that does not have a
subscription assigned to it. Extreme Networks does not provide
services for unmanaged devices—no management, no monitoring,
no updates, no upgrades. An unmanaged device is treated as
inventory-only. If there are not enough subscriptions, you or
the system can unmanage devices. Unmanaged devices can
be deleted or converted to the Managed state. If enough
subscriptions are available. Unmanaged devices are always in the
Disconnected state.
Link Your Extreme Portal Account | Extreme Platform ONE Networking or
ExtremeCloud IQ (New)
Use this task to link your Extreme Portal account and Extreme Platform ONE Networking or
ExtremeCloud IQ (New).
1. Go to Subscriptions & Services > Subscriptions & Licensing.
2. Select the Global tab.
3. Select Link Extreme Portal Account and type your Extreme Portal credentials.
Related Links
View the License Pool on page 46
Link Your Extreme Portal Account | ExtremeCloud IQ (Classic)
Use this task to link your Extreme Portal account and ExtremeCloud IQ (Classic).
1. Go to Global Settings > Administration > License Management.
Link Your Extreme Portal Account | Extreme Platform ONE
Networking or ExtremeCloud IQ (New)
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
14 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 15 -->

2. Select Link My Extreme Portal Account and enter your Extreme Portal credentials.
Note
If you are a partner or a distributor and are setting up an Extreme Portal account
for a customer, type your Extreme Portal credentials and the Customer Unique
Identifier (CUID). The CUID is included in the customer welcome letter.
Depending on the subscriptions purchased, ExtremeCloud IQ displays subscription
information in the Entitlements and the NAC Entitlements tables.
Figure 1: ExtremeCloud IQ License Information Page
Related Links
View the License Pool on page 52
Unlink and Relink Your Extreme Portal Account | Extreme Platform ONE
Networking and ExtremeCloud IQ (New)
You must have full access to Subscriptions & Licensing—Administrator role.
Note
Perform this procedure only as part of a testing or troubleshooting strategy.
1. Go to Subscriptions & Services > Subscriptions & Licensing.
2. Select Unlink from Extreme Portal.
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
Unlink and Relink Your Extreme Portal Account | Extreme
Platform ONE Networking and ExtremeCloud IQ (New)
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 15


<!-- page 16 -->

3. Select Link Extreme Portal Account and enter your Extreme Portal credentials.
Unlink and Relink Your Extreme Portal Account | ExtremeCloud IQ (Classic)
Note
Perform this procedure only as part of a testing or troubleshooting strategy.
1. Go to Global Settings > Administration > License Management.
2. Select Unlink from Extreme Portal.
3. Select Link My Extreme Portal Account and enter your Extreme Portal credentials.
The subscription information appears in the Entitlements table.
Trial Subscriptions
Note
An administrator can request a 90-day free trial subscription for an Extreme Platform
ONE application only once. Extreme Platform ONE Networking, ExtremeCloud SD-
WAN, and Extreme Platform ONE Security are available for trial.
ExtremeCloud IQ (Classic) is no longer available for trial.
Trial subscription requests are not available for Managed Service Provider (MSP)
tenants.
Users with the following Extreme Platform ONE Networking roles and other product or
application roles can request a trial subscription:
Extreme Platform ONE Networking:
• Administrator
• BizOps
ExtremeCloud IQ (New):
Administrator
ExtremeCloud IQ (Classic)
• Administrator
• Operator
ExtremeCloud SD-WAN
• Administrator
Extreme Intuitive Insights
• Administrator
The request trial must meet the following criteria to be valid:
• The account is linked to Extreme Portal.
• The request is initiated from the Subscriptions & Licensing page.
• An active subscription does not exist for the selected product.
Unlink and Relink Your Extreme Portal Account |
ExtremeCloud IQ (Classic)
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
16 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 17 -->

• A previous trial was not granted.
• An expired subscription does not exist for the selected product.
If your request is rejected, you are notified and the next step is to contact the Sales team.
In addition to not meeting the preceding criteria, a request can be rejected for the following
reasons:
• Sanctioned country
• Sanctioned company
• Sanctioned individual
• Trial already expired
• Production entitlement already present or expired
Related Links
Request a Trial Subscription on page 17
Trial Subscription Eligibility
Request a trial subscription only if you meet the following criteria:
• You are a new Extreme Platform ONE or ExtremeCloud IQ (New) customer.
• You are an existing Extreme Platform ONE, ExtremeCloud IQ (New), or ExtremeCloud IQ
(Classic) customer who has never purchased or requested a trial subscription for the
application you are considering.
Note
If you requested and were granted a trial in the past but never used it, you are
disqualified from a new trial.
Request a Trial Subscription
Use this task to request a 90-day trial subscription.
1. Go to Subscriptions & Services > Subscriptions & Licensing
2. On the Subscriptions & Licensing page, select Start Trial.
Note
On first request, a Request Process diagram opens.
• (Optional) Select Do not show this message again.
• Select OK.
a. Select the checkbox to Accept Terms and Conditions and acknowledge the policy.
b. Select the check box to agree to share contact information.
c. Select Accept and Continue.
3. In Select Request, select Subscriptions, and then select Next.
4. Select the application that you want to trial, and select Add adding each one to the cart.
5. When you finish adding applications to the cart, select Next.
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions Trial Subscription Eligibility
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 17


<!-- page 18 -->

6. Type your phone number and fill out any optional information, then select Next.
7. Review your request, and then select Next to download the request document.
8. Submit the request document to your Extreme Networks partner or contact your account
team to submit the request.
Note
Depending on the application and regulatory requirements, the trial subscription is
available after a few minutes or up to five working days after verification. In addition
to the in-product subscription-request notification, you receive email notification
regarding the status of your request.
If you have not received the licenses after two business days, contact your account
team.
If the trial subscription request is rejected, contact your account team.
Upgrading to Extreme Platform ONE
Upgrading from ExtremeCloud IQ to Extreme Platform ONE Networking does not require
migration. It is subscription-dependent. Your network data remains in the cloud, and the login
URL remains the same.
After purchasing and activating any quantity of Extreme Platform ONE Standard Networking
subscriptions (Tiers A-D), the system detects them at the next login and loads the Extreme
Platform ONE Networking interface. You can use the 9-dot menu to switch between the
Extreme Platform ONE Networking and ExtremeCloud IQ (Classic) interfaces.
Note
Subscription notes defined in ExtremeCloud IQ (Classic) are available in Extreme
Platform ONE Networking and ExtremeCloud IQ (New), and vice versa. Upgrading to
Extreme Platform ONE Networking does not affect your subscription notes. For more
information, see Add a Note to a Subscription on page 44.
You can use AI Expert to help you to learn about Extreme Platform ONE Networking updates to
the menus and landing pages, or see the Extreme Platform ONE User Guide.
Important
If you have not purchased enough Extreme Platform ONE Standard Networking
subscriptions to cover all devices, see Upgrading to Extreme Platform ONE on page
18.
What to Expect With a Mixed-Subscription Deployment
Full-feature access for Extreme Platform ONE Networking requires Extreme Platform ONE
subscriptions. If a building, outdoor site, or fabric uses a ExtremeCloud IQ Pilot subscription,
feature access is limited. To enable full-feature access, the site (indoor or outdoor), building,
or fabric must use only Extreme Platform ONE subscriptions. For more information, see Table 5
on page 19.
Upgrading to Extreme Platform ONE
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
18 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 19 -->

A blue icon in Extreme Platform ONE Networking indicates limited-feature status. You can
unlock full features provided that you have enough available subscriptions.
Note
If your mixed-subscription deployment includes active CoPilot subscriptions, you can
use the 9-dot menu to switch to ExtremeCloud IQ (New), and then select CoPilot
from the ExtremeCloud IQ (New) 9-dot menu.
Table 5: Comparison of available features according to subscription
Feature Only ExtremeCloud
IQ Pilot
subscriptions
Mixed subscriptions Only Extreme
Platform ONE
Standard
subscriptions
Subscriptions All No Yes Yes
Visualize | Physical
layer
No Yes Yes
Visualize | Fabric layer No * Yes
Visualize | Service
layer
No Yes Yes
Visualize | Split view No Yes Yes
Show Endpoint
to Endpoint Service/
VLAN
No ** Yes
Contracts No Yes Yes
Inventory No Yes Yes
Custom Roles No Yes Yes
AI Expert No Yes Yes
Agent workflows No Yes Yes
Fabric Configuration No *** Yes
* For more information, see Unlocking Full Features on page 20.
** The Show Endpoint to Endpoint Service/VLAN feature requires that both selected devices
be located in buildings or sites with full features unlocked.
*** The Configure Fabric option is available only if all buildings, where Fabric Engine devices
are located, have full features unlocked. If a device is using an ExtremeCloud IQ Pilot
subscription and there is an available Extreme Platform ONE subscription, the tooltip is:
Extreme Platform ONE Subscription not Assigned. If the device already has an Extreme
Platform ONE subscription, but the site or building is not compliant, the tooltip is: Limited
Extreme Platform ONE Features.
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions What to Expect With a Mixed-Subscription Deployment
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 19


<!-- page 20 -->

Unlocking Full Features
Full-feature access for Extreme Platform ONE Networking requires Extreme Platform ONE
subscriptions. Extreme Platform ONE Networking supports mixed-subscription deployments
with some feature limitations. If you have enough Extreme Platform ONE subscriptions, you
can unlock Extreme Platform ONE Networking full features for single or multiple sites (including
outdoor sites), site groups, buildings, or fabrics, from the Inventory, Sites, or Visualize menus,
or the Device Inspector panel.
Note
In Visualize, for the Physical and Fabric layers, the Unlock Full Features option is
available at the site and group site levels in Quick Location Navigation, only if all
child buildings have limited feature access. Blue icons indicate limited feature access.
If you do not have enough available subscriptions, Extreme Platform ONE Networking
can automatically swap (reassign) subscriptions with devices in locations for which
full features are not unlocked.
First, ensure that you have enough subscriptions for all devices in the target sites or buildings.
You have the following options:
• Use (manually reassign) existing subscriptions. See Reassign Subscriptions | Inventory on
page 20, Reassign Subscriptions| Visualize on page 21, or Reassign Subscriptions |
Device Inspector Panel on page 22.
• Purchase a new subscription to add more subscriptions. See Purchase a Subscription on
page 42.
Related Links
Subscription Tier Priorities on page 29
Purchase a Subscription on page 42
Reassign Subscriptions | Inventory on page 20
Reassign Subscriptions| Visualize on page 21
Reassign Subscriptions | Device Inspector Panel on page 22
Reassign Subscriptions | Inventory
To reassign subscriptions, you must have write access to Inventory and Subscriptions
& Licensing, and you must have sufficient Extreme Platform ONE Standard Networking
subscriptions.
Important
This process is non-reversible.
Use this procedure to reassign subscriptions to a site, building, or fabric, replacing
ExtremeCloud IQ Pilot subscriptions with Extreme Platform ONE Standard Networking
subscriptions.
1. Go to Subscriptions & Services > Inventory.
Unlocking Full Features
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
20 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 21 -->

2. Select all sites or filter sites.
If one or more associated devices use ExtremeCloud IQ Pilot licenses, Extreme Platform
ONE Networking displays a widget that shows the number of buildings and the number of
devices using Pilot licenses.
3. Use the widget to drill down to the devices for the filtered sites, and then select Unlock Full
Features.
For more information, see What to Expect With a Mixed-Subscription Deployment on page
18.
Note
If one or more devices are Fabric Engine, to allow the reassignment, you must
select all buildings with Fabric Engine.
4. Select the sites or buildings to unlock, and then select Next.
Blue icons indicate limited features.
5. Select Unlock.
If you do not have sufficient subscriptions to unlock the selected sites or buildings, the
dialog lists the total number of required subscriptions by subscription tier. To purchase the
requisite number of subscriptions, select Request Subscription.
Related Links
What to Expect With a Mixed-Subscription Deployment on page 18
Reassign Subscriptions| Visualize
To reassign subscriptions, you must have write access to Inventory and Subscriptions
& Licensing, and you must have sufficient Extreme Platform ONE Standard Networking
subscriptions.
Important
This process is non-reversible.
Use this procedure to reassign Extreme Platform ONE Standard Networking subscriptions to
a site, building, or fabric, replacing ExtremeCloud IQ Pilot subscriptions with Extreme Platform
ONE Standard Networking subscriptions.
1. Go to Monitoring > Visualize.
2. In
  (Quick Location Navigation), select one or more sites or buildings.
Blue icons indicate limited features.
3. Select
 , and then choose Unlock Full Features.
Note
If there are one or more Fabric Engine devices, to enable the reassignment, you
must select all buildings with Fabric Engine.
4. Select the sites or buildings to unlock, and then select Next.
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions Unlocking Full Features
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 21


<!-- page 22 -->

5. Select Unlock.
If you do not have sufficient subscriptions to unlock the selected sites or buildings, the
dialog lists the total number of required subscriptions by subscription tier. To purchase the
requisite number of subscriptions, select Request Subscription.
Reassign Subscriptions | Device Inspector Panel
To reassign subscriptions, you must have write access to Inventory and Subscriptions
& Licensing, and you must have sufficient Extreme Platform ONE Standard Networking
subscriptions.
The selected device must display the status Connected, Limited Features.
Important
This process is non-reversible.
When you hover over Connected, Limited Features, Extreme Platform ONE Networking
displays one of the following tooltips:
• Extreme Platform ONE Subscription not Assigned
This tooltip indicates that the device is using a ExtremeCloud IQ Pilot subscription.
• Limited Platform ONE Features
This tooltip indicates that the device is using an Extreme Platform ONE Standard
Networking subscription, and the device belongs to a site or building with limited features.
Use this procedure to reassign subscriptions to a site, building, or fabric, replacing
ExtremeCloud IQ Pilot licenses with Extreme Platform ONE Standard Networking subscriptions.
1. In the Device Inspector panel, select Limited Features.
2. Select the buildings or sites to unlock, and then select Next.
Blue icons indicate limited features.
3. Select Unlock.
If you do not have sufficient subscriptions to unlock the selected sites or buildings, the
dialog lists the total number of required subscriptions, according to tier. To purchase the
requisite subscriptions, select Request Subscription.
Unlocking Full Features
Extreme Platform ONE Networking™ and ExtremeCloud IQ
Subscriptions
22 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 23 -->

Subscriptions and Licenses
ExtremeCloud IQ Pilot on page 23
ExtremeCloud IQ CoPilot on page 24
ExtremeCloud IQ Navigator on page 25
ExtremeCloud IQ NAC on page 25
Third-Party Management Engine on page 26
Premier Switch Features on page 26
MACsec Switch Features on page 27
Extreme Platform ONE Standard Networking on page 27
ExtremeCloud IQ Pilot Twin Subscription Provides Backwards
Compatibility on page 29
Subscription Tier Priorities on page 29
Additional Requirements on page 30
ExtremeCloud IQ Controller on page 31
ExtremeCloud IQ Site Engine on page 31
Automatic Subscription Alignment on page 32
Subscription Expiration on page 33
ExtremeCloud IQ Legacy Entitlement Keys on page 33
The following sections describe the subscriptions available for ExtremeCloud IQ, and Extreme
Platform ONE™ Networking.
ExtremeCloud IQ Pilot
ExtremeCloud IQ Pilot subscriptions give your managed devices all of the features and
functionality offered by an ExtremeCloud IQ Pilot system. Each Pilot subscription covers a
single device.
The following devices require ExtremeCloud IQ Pilot subscriptions:
• Cloud-native switches managed by ExtremeCloud IQ
• Cloud-native access points managed by ExtremeCloud IQ
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 23


<!-- page 24 -->

• Devices managed by ExtremeCloud IQ Site Engine
• Devices that require an ExtremeCloud IQ Navigator subscription
Note
If there are not enough ExtremeCloud IQ Navigator subscriptions, you can use an
ExtremeCloud IQ Pilot or Extreme Platform ONE Standard Networking subscription
instead. For more information, see Subscription Tier Priorities on page 29.
The following devices do not require an ExtremeCloud IQ Pilot subscription:
• Digital Twin devices
• Simulated devices
• Unmanaged devices
• Ping-only devices onboarded through ExtremeCloud IQ Site Engine
• Devices assigned an ExtremeCloud IQ Navigator subscription
• Locally managed devices that have been onboarded to ExtremeCloud IQ
• Universal Compute Platform appliances and clusters
• Devices assigned an Extreme Platform ONE Standard Networking subscription
For more information about subscription requirements, see Additional Requirements on page
30.
Related Links
ExtremeCloud IQ Pilot and Extreme Platform ONE Networking on page 54
Additional Requirements on page 30
ExtremeCloud IQ CoPilot
Note
CoPilot subscriptions are available to existing CoPilot customers only.
CoPilot subscriptions offer eligible devices additional functionality. You must have an
ExtremeCloud IQ Pilot or an Extreme Platform ONE Standard Networking subscription to
use an ExtremeCloud IQ CoPilot subscription. ExtremeCloud IQ CoPilot is available for all
ExtremeCloud IQ Pilot accounts, but is unavailable for Extreme Connect accounts or for
Navigator accounts. After you link your account to the Extreme Portal, ExtremeCloud IQ
obtains the CoPilot subscriptions from the license pool.
The following devices are NOT eligible for ExtremeCloud IQ CoPilot subscriptions:
• ExtremeCloud IQ Controller
• Extreme Campus Controller
• Devices onboarded through Extreme Campus Controller
• WiNG devices
• Devices onboarded through ExtremeCloud IQ Controller
• Devices onboarded through ExtremeCloud IQ Site Engine
• Digital Twin devices
ExtremeCloud IQ CoPilot Subscriptions and Licenses
24 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 25 -->

• Simulated devices
• SR (legacy switch) devices reporting directly to ExtremeCloud IQ
• Dell N-series devices reporting directly to ExtremeCloud IQ
• Devices onboarded as Managed Locally
• Devices for which the subscription was revoked by using the Actions menu.
Actions > Change CoPilot License Status > Revoke CoPilot License
• Unmanaged devices
Related Links
ExtremeCloud IQ Pilot on page 23
ExtremeCloud IQ CoPilot on page 55
Extreme Platform ONE Standard Networking on page 27
ExtremeCloud IQ Navigator
An ExtremeCloud IQ Navigator subscription provides management functions for third-party
and non-native cloud devices. Features include Application Visibility, SSH Proxy, Web Proxy
to WiNG Controller, and Web Proxy to Extreme Campus Controller and ExtremeCloud IQ
Controller.
Each Navigator subscription covers a single device. The following devices require a Navigator
subscription:
• Some devices managed by ExtremeCloud IQ Site Engine. For more information, see
ExtremeCloud IQ Site Engine Licensing.
• WiNG (VX) controllers that are onboarded to ExtremeCloud IQ require one ExtremeCloud
IQ Navigator subscription per device.
• WiNG APs that are onboarded using the WiNG (VX) controller require one subscription per
device.
Related Links
ExtremeCloud IQ Navigator on page 55
ExtremeCloud IQ NAC
Network Access Control (NAC) uses a set of protocols to secure devices when they access
the network. The 802.1X standard is a basic form of NAC. NAC controls access using policies
such as pre-admission endpoint security checks and post-admission controls over access
levels, and permissions that devices exercise in the network.
ExtremeCloud IQ NAC subscriptions are compatible with ExtremeCloud A3 version 4.0 and
later, and with ExtremeCloud IQ Site Engine version 21.9 and later.
Because the quantity of total NAC subscriptions can change over time, the allocation is stored
as a percentage. However, the management application displays the allocation both as a
percentage and as a calculated absolute number.
Subscriptions and Licenses ExtremeCloud IQ Navigator
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 25


<!-- page 26 -->

Related Links
Manage NAC Allocations | Extreme Platform ONE and ExtremeCloud IQ (New) on page 46
Manage NAC Allocations | ExtremeCloud IQ on page 53
ExtremeCloud IQ NAC on page 56
Third-Party Management Engine
Third-Party Management Engine manages on-premises, non-cloud native devices that
communicate using SNMP, including third-party devices and Extreme Networks legacy
devices.
Third-Party Management Engine requires a Tier A or better subscription. If Third-Party
Management Engine is unmanaged, it does not report statistics to the cloud management
application. All devices managed by Third-Party Management Engine require a Tier 3RD or
better subscription. See Subscription Tier Priorities on page 29.
Related Links
Subscription Tier Priorities on page 29
Premier Switch Features
While the base software included with each switch supports most switch features, certain
features require a Premier license. Feature requirements are platform- and network operating
system-specific. For details and ordering information, see the switch datasheets.
Universal Switches running Switch Engine or Fabric Engine might require a Premier license
to enable advanced features or a higher feature tier. A Premier license is available as either
a perpetual license or included as part of an Extreme Platform ONE Standard Networking
subscription.
You can push a Perpetual Premier License to the switch using the management application
GUI, or install it manually using a license file generated by the Extreme Portal: https://
extremeportal.force.com/ExtrLogin.
For switches managed by ExtremeCloud IQ, Extreme Platform ONE, or ExtremeCloud IQ
Site Engine with a Pilot or Extreme Platform ONE subscription used by the switches, the
management application receives notification of the license and enables the use of Premier
switch features for the duration of the subscription. The switches must be 5xxx or 7xxxx
series. See the switch documentation for the minimum firmware versions.
Note
Although Extreme Platform ONE entitlements include Premier features, the
management application displays Premier perpetual licenses only if an actual Premier
license exists on the switch. If only Pilot or Extreme Platform ONE subscriptions exist,
the management application displays only the subscription entitlement level.
Third-Party Management Engine Subscriptions and Licenses
26 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 27 -->

MACsec Switch Features
While the base software included with each switch supports most switch features, MACsec
features require a MACsec license. For details and ordering information, see the switch
datasheets.
Extreme Platform ONE Standard Networking
Extreme Platform ONE Standard Networking subscriptions provide managed devices all the
features and functionality offered by an ExtremeCloud IQ Pilot system, plus access to Extreme
Platform ONE and device TAC OS Support. Each Extreme Platform ONE Standard Networking
subscription includes subscriptions for a specific number of single devices.
Important
While TAC OS Support is included in Extreme Platform ONE Standard Networking
subscriptions, there are exceptions documented in Products with TAC & OS Excluded
from a Platform ONE Subscription published at https://www.extremenetworks.com/
support/policies.
Platform ONE Standard Networking subscriptions are divided into subscription tiers, as
described in the following table.
Table 6: Extreme Platform ONE Standard Networking Subscription Tiers
Subscription tier Device family
Tier A Universal APs
Non-Universal APs
4000 Series
5100 Series
5300 Series
Summit X435
Summit X440-G2
SR Series
N Series
BR Series
XR Series
XA 1400 Series
Third-Party Management Engine
Tier B 5400 Series
Summit X450-G2
ERS 4800
ERS 4900
Subscriptions and Licenses MACsec Switch Features
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 27


<!-- page 28 -->

Table 6: Extreme Platform ONE Standard Networking Subscription Tiers (continued)
Subscription tier Device family
Tier C 5500 Series
Summit X460-G2
Summit X465
Summit X590
VSP 4450
VSP 4850
VSP 4900
ERS 5900
Tier D 5700 Series
7000 Series
Summit X670-G2
Summit X690
Summit X870
VSP 7200 Series
VSP 7400 Series
VSP 8200 Series
VSP 8400 Series
VSP 8600 Series
Tier 3RD Devices managed by Third-Party Management Engine
The following devices require an Extreme Platform ONE Standard Networking subscription:
• Cloud-native switches managed by Extreme Platform ONE Networking
• Cloud-native access points managed by Extreme Platform ONE Networking
• Devices managed by ExtremeCloud IQ Site Engine
The following devices do not require an Extreme Platform ONE Standard Networking
subscription:
• Digital Twin devices
• Simulated devices
• Unmanaged devices
• Ping-only devices onboarded through ExtremeCloud IQ Site Engine
• Devices assigned an ExtremeCloud IQ Navigator subscription
If there are not enough ExtremeCloud IQ Navigator subscriptions, you can use an
Extreme Platform ONE Standard Networking subscription instead. For more information,
see Subscription Tier Priorities on page 29.
• Locally managed devices that have been onboarded to Extreme Platform ONE Networking
• Universal Compute Platform appliances and clusters
For more information about subscription requirements, see Additional Requirements on page
30.
Extreme Platform ONE Standard Networking Subscriptions and Licenses
28 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 29 -->

Related Links
Additional Requirements on page 30
ExtremeCloud IQ Pilot Twin Subscription Provides Backwards Compatibility
Some versions of ExtremeCloud IQ Site Engine and ExtremeCloud IQ Controller do not
support Extreme Platform ONE Standard Networking subscriptions. To provide you with the
necessary time to upgrade to later versions, every Extreme Platform ONE Standard Networking
subscription includes an ExtremeCloud IQ Pilot Twin subscription with the same start date,
end date, and subscription quantity.
• The Extreme Portal displays both Extreme Platform ONE Standard Networking and
ExtremeCloud IQ Pilot Twin subscriptions.
• ExtremeCloud IQ (Classic) and ExtremeCloud IQ (New) do not display ExtremeCloud IQ
Pilot Twin subscriptions.
• Extreme Platform ONE applications 1 do not display ExtremeCloud IQ Pilot Twin
subscriptions.
• ExtremeCloud IQ Site Engine version 25.2 and earlier supports ExtremeCloud IQ Pilot and
ExtremeCloud IQ Pilot Twin subscriptions.
• ExtremeCloud IQ Site Engine version 25.5 and later supports ExtremeCloud IQ Pilot and
Extreme Platform ONE Standard Networking subscriptions.
• ExtremeCloud IQ Controller versions support ExtremeCloud IQ Pilot and ExtremeCloud IQ
Pilot Twin subscriptions.
1 Extreme Platform ONE Networking or Extreme Platform ONE Security
Note
If you purchased Extreme Platform ONE Standard Networking subscriptions and are
running management application versions that are incompatible with them, you can
use the provided ExtremeCloud IQ Pilot Twin subscriptions.
Contracts that include Extreme Platform ONE Standard Networking subscriptions
identify the Pilot Twin subscriptions as XIQ-CHILD-PIL-S-C-PWP or XIQ-CHILD-PIL-
S-C-EW.
Subscription Tier Priorities
When you add devices, or change the device status from Unmanaged to Managed, Extreme
Platform ONE Networking and ExtremeCloud IQ can use a higher subscription tier if the
appropriate tier is unavailable.
Subscriptions and Licenses
ExtremeCloud IQ Pilot Twin Subscription Provides
Backwards Compatibility
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 29


<!-- page 30 -->

Example: For a device that belongs to Tier A, the management application assigns a Tier A
subscription. If the Tier A subscription is unavailable, the management application assigns a
Tier B subscription. See the following table for more information.
Table 7: Subscription tier priorities
Subscription Navigator
eligible
device
Tier A
device
Tier B
device
Tier C
device
Tier D
device
TPME * TPME *
managed
device
Tier 3RD First
Choice
— — — — — First
Choice
Navigator Priority 2 — — — — — —
Standard Tier
A
Priority 3 First
Choice
— — — First
Choice
Priority 2
Standard Tier
B
Priority 4 Priority 2 First
Choice
— — Priority 2 Priority 3
Standard Tier
C
Priority 5 Priority 3 Priority 2 First
Choice
— Priority 3 Priority 4
Standard Tier
D
Priority 6 Priority 4 Priority 3 Priority 2 First
Choice
Priority 4 Priority 5
Pilot ** Priority 7 Priority 5 Priority 4 Priority 3 Priority 2 — Priority 6
Unmanaged Priority 8 Priority 6 Priority 5 Priority 4 Priority 3 Priority 5 Priority 7
* Third-Party Management Engine (TPME)
** Pilot subscriptions cannot be assigned for devices located in a site or building after you
Unlock Full Features for that site or building.
Additional Requirements
There are additional requirements and considerations for the following applications and
devices.
Device Stacks
Device stacks can use subscriptions of different tiers, subject to the following
requirements:
• The subscriptions must all be of the same level—Standard or Pilot. A combination is
unsupported.
• Each unit in a stack requires a subscription. If there are insufficient subscriptions to
cover all devices in a stack, the entire stack is Unmanaged.
Note
Extreme Platform ONE Networking and ExtremeCloud IQ do not support
onboarding stacks that include devices from different families (heterogenous
stacks). ExtremeCloud IQ Site Engine supports heterogenous stacks, and can be
onboarded to Extreme Platform ONE Networking or ExtremeCloud IQ.
Additional Requirements Subscriptions and Licenses
30 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 31 -->

ExtremeCloud IQ Site Engine
Each instance of ExtremeCloud IQ Site Engine, ExtremeCloud IQ Site Engine Analytics, and
ExtremeCloud IQ Site Engine Control requires a subscription.
If there is no suitable subscription with available subscriptions, ExtremeCloud IQ Site
Engine and all devices managed by the Site Engine are Unmanaged.
ExtremeCloud Tunnel Concentrator
Each instance of Tunnel Concentrator requires a Tier A subscription. If there is no suitable
subscription, Tunnel Concentrator is inoperative.
Additionally, each AP connected to a Tunnel Concentrator requires a Tier A subscription.
ExtremeCloud IQ Controller
ExtremeCloud IQ Controller is a scalable, on-premises network management appliance
(physical or virtual) designed for unified wired and wireless control in campus and high-
density environments. It manages up to 20,000 devices (including 1,000 switches) and
supports up to 100,000 concurrent users.
Note
ExtremeCloud IQ Controller requires a one-time, per appliance activation key (sold
separately) to enable the software on the hardware or virtual appliance.
Each device managed by ExtremeCloud IQ Controller requires one of the following
subscription options:
• ExtremeCloud IQ Pilot, or Pilot Twin (included with Extreme Platform ONE Standard
Networking subscriptions)
• ExtremeCloud IQ Navigator
While it operates independently on-premises, it can optionally connect to the ExtremeCloud
IQ or Extreme Platform ONE Networking cloud platform. While ExtremeCloud IQ Controller
shares information with the cloud platform, it does not rely on the cloud platform for licensing.
Connected Mode
ExtremeCloud IQ Controller connects directly to License Entitlement Management (LEM).
The Controller does not use the cloud platform connection to LEM.
Air-Gap Mode
ExtremeCloud IQ Controller stores subscriptions locally in a file for determining whether
the deployment has sufficient subscriptions of each subscription type. This mode ensures
that ExtremeCloud IQ Controller does not require an Internet connection for LEM.
For more information see ExtremeCloud IQ Controller documentation.
ExtremeCloud IQ Site Engine
ExtremeCloud IQ Site Engine extends and enhances ExtremeCloud IQ management of
Extreme Networks Universal Hardware (switches and access points), and legacy, third-party,
Subscriptions and Licenses ExtremeCloud IQ Controller
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 31


<!-- page 32 -->

and non-cloud native devices. ExtremeCloud IQ Site Engine provides end-to-end network
management, task automation, real-time analytics, and service assurance.
ExtremeCloud IQ Site Engine includes all the features and functionality of Extreme
Management Center. If you are an existing Extreme Management Center customer, contact
your representative to have your Extreme Management Center license migrated to
ExtremeCloud IQ Site Engine.
Note
ExtremeCloud IQ Site Engine requires an ExtremeCloud IQ Pilot or an Extreme
Platform ONE Standard Networking subscription. ExtremeCloud IQ Site Engine is
unsupported with ExtremeCloud IQ Connect accounts.
Each device managed by ExtremeCloud IQ Site Engine requires one of the following
subscription options:
• ExtremeCloud IQ Pilot
• ExtremeCloud IQ Navigator
• Extreme Platform ONE Standard Networking
• No subscription—applies to devices added with a ping-only profile, typically used for
monitoring non-SNMP devices, such as printers, cameras, and IoT sensors, or third-party
devices where full management is not required.
There are two deployment modes for ExtremeCloud IQ Site Engine:
• Connected mode: ExtremeCloud IQ manages subscriptions for ExtremeCloud IQ Site
Engine. As you add devices to ExtremeCloud IQ Site Engine, they onboard to ExtremeCloud
IQ, with a request for an appropriate subscription. ExtremeCloud IQ activates the available
subscription from the license pool and determines whether you meet or exceed the
limits for each subscription type. All ExtremeCloud IQ Site Engines connected to the
same ExtremeCloud IQ account share the same pool. A managed device requires one
subscription, depending on the number of ExtremeCloud IQ Site Engines managing that
device.
• Air gap mode: ExtremeCloud IQ Site Engine stores subscriptions locally in a file for
determining whether you meet or exceed the limits for each subscription type. This mode
ensures that ExtremeCloud IQ Site Engine does not require an Internet connection to verify
the number of available subscriptions.
For more detailed information, visit ExtremeCloud IQ Site Engine Licensing.
Related Links
ExtremeCloud IQ Pilot on page 23
ExtremeCloud IQ Navigator on page 25
Extreme Platform ONE Standard Networking on page 27
Automatic Subscription Alignment
When you onboard new devices or the license pool changes, ExtremeCloud IQ aligns your
subscriptions to avoid license violations. This feature automatically updates subscription
consumption and changes the subscription types as needed.
Automatic Subscription Alignment Subscriptions and Licenses
32 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 33 -->

When you onboard new devices, and there are available entitlements in the pool, the system
automatically assigns the available subscriptions. If you onboard devices and there are no
available subscriptions, an license violation occurs.
If there are insufficient Navigator subscriptions, ExtremeCloud IQ automatically assigns a
higher-tier subscription if one is available.
When the following license pools grow, ExtremeCloud IQ assigns the subscriptions to eligible
devices:
• CoPilot
• Pilot
• Navigator
If a device is part of a stack and there are sufficient subscriptions available, the system
assigns subscriptions to all devices in the stack. If there are insufficient entitlements for all
devices in a stack, ExtremeCloud IQ does not automatically assign entitlements to any of the
devices in the stack.
Related Links
Entitlement Violations on page 54
Subscription Expiration
When a subscription expires, ExtremeCloud IQ automatically assigns available current
subscriptions of the same type. If there are insufficient current subscriptions of the same type
available to cover the expired assignments, subscription reallocation occurs automatically.
If the higher-tier subscriptions do not have sufficient available subscriptions, the system
reallocates subscriptions for the most recently onboarded devices first. Subscription tier
reallocation follows the same logic as subscription assignment. For more information, see
Subscription Tier Priorities on page 29.
ExtremeCloud IQ Legacy Entitlement Keys
Legacy Entitlement Keys are unsupported with the enhanced license and entitlement schema
and new features. The option to add a Legacy Entitlement Key is disabled, and Legacy
Entitlement Keys are no longer available for purchase. Contact GTAC for assistance with
converting Legacy Entitlement Keys to ExtremeCloud IQ Pilot subscriptions.
Related Links
ExtremeCloud IQ Pilot on page 23
Subscriptions and Licenses Subscription Expiration
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 33


<!-- page 34 -->

Subscription Part Numbers
Use the following part numbers to order subscriptions. Contact your Extreme Networks or
Extreme Networks Partner Sales Representative.
Table 8: ExtremeCloud IQ Pilot
Part Number Description
XIQ-PIL-S-C-PWP ExtremeCloud IQ Pilot Right-to-use Subscription and PartnerWorks
Plus SaaS Support for one device for one year
XIQ-PIL-S-C-EW ExtremeCloud IQ Pilot Right-to-use Subscription and ExtremeWorks
SaaS Support for one device for one year
Table 9: ExtremeCloud IQ CoPilot
Part Number Description
XIQ-COPILOT-S-C-PWP ExtremeCloud IQ CoPilot Right-to-use Subscription
PartnerWorks Plus SaaS Support for one device for one year
XIQ-COPILOT-S-C-EW ExtremeCloud IQ CoPilot Right-to-use Subscription
ExtremeWorks SaaS Support for one device for one year
Note
ExtremeCloud IQ CoPilot subscriptions are available only for existing CoPilot
customers.
Table 10: ExtremeCloud IQ Navigator
Part Number Description
XIQ-NAV-S-C-PWP ExtremeCloud IQ Navigator Right-to-use Subscription PartnerWorks
Plus SaaS Support for one device for one year
XIQ-NAV-S-C-EW ExtremeCloud IQ Navigator Right-to-use Subscription ExtremeWorks
SaaS Support for one device for one year
34 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 35 -->

Table 11: ExtremeCloud IQ NAC
Part Number Description
XIQ-NAC-S-1K-PWP ExtremeCloud IQ NAC Right-to-use Subscription and PartnerWorks
Plus SaaS Support for 1K end-systems for one year
XIQ-NAC-S-10K-PWP ExtremeCloud IQ NAC Right-to-use Subscription and PartnerWorks
Plus SaaS Support for 10K end-systems for one year
XIQ-NAC-S-100K-PWP ExtremeCloud IQ NAC Right-to-use Subscription and PartnerWorks
Plus SaaS Support for 100K end-systems for one year
XIQ-NAC-S-1K-EW ExtremeCloud IQ NAC Right-to-use Subscription and
ExtremeWorks SaaS Support for 1K end-systems one year
XIQ-NAC-S-10K-EW ExtremeCloud IQ NAC Right-to-use Subscription and
ExtremeWorks SaaS Support for 10K end-systems for one year
XIQ-NAC-S-100K-EW ExtremeCloud IQ NAC Right-to-use Subscription and
ExtremeWorks SaaS Support for 100K end-systems for one year
Table 12: Extreme Platform ONE Networking™ Networking
Part Number Description
EP1-STD-TA-S-C-
PWP-1YR
Extreme Platform ONE Standard Networking Right-to-use and
PartnerWorks Plus (PWP) TAC OS Support for one device of Tier
A per year
EP1-STD-TB-S-C-
PWP-1YR
Extreme Platform ONE Standard Networking Right-to-use and
PartnerWorks Plus (PWP) TAC OS Support for one device of Tier
B per year
EP1-STD-TC-S-C-
PWP-1YR
Extreme Platform ONE Standard Networking Right-to-use and
PartnerWorks Plus (PWP) TAC OS Support for one device of Tier
C per year
EP1-STD-TD-S-C-
PWP-1YR
Extreme Platform ONE Standard Networking Right-to-use and
PartnerWorks Plus (PWP) TAC OS Support for one device of Tier
D per year
EP1-STD-TA-S-C-
EW-1YR
Extreme Platform ONE Standard Networking Right-to-use
Subscription and ExtremeWorks (EW) SaaS and device TAC OS
Support for one Tier A device, for one year
EP1-STD-TB-S-C-
EW-1YR
Extreme Platform ONE Standard Networking Right-to-use
Subscription and ExtremeWorks (EW) SaaS and device TAC OS
Support for one Tier B device for one year
EP1-STD-TC-S-C-
EW-1YR
Extreme Platform ONE Standard Networking Right-to-use
Subscription and ExtremeWorks (EW) SaaS and device TAC OS
Support for one Tier C device for one year
EP1-STD-TD-S-C-
EW-1YR
Extreme Platform ONE Standard Networking Right-to-use
Subscription and ExtremeWorks (EW) SaaS and device TAC OS
Support for one Tier D device for one year
EP1-STD-T3RD-S-C-
EW-1YR
Extreme Platform ONE Standard Networking Right-to-use
Subscription for one Third-Party Tier device for one year
Subscription Part Numbers
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 35


<!-- page 36 -->

Table 12: Extreme Platform ONE Networking™ Networking (continued)
Part Number Description
XIQ-CHILD-PIL-S-C-
PWP
ExtremeCloud IQ Pilot Twin Right-to-use Subscription and
PartnerWorks Plus SaaS Support for one device for one year
XIQ-CHILD-PIL-S-C-EW. ExtremeCloud IQ Pilot Twin Right-to-use Subscription and
ExtremeWorks Plus SaaS Support for one device for one year
Table 13: Extreme Platform ONE™ Security
Part Number Description
EP1-SEC-S-C-250-EW Extreme Platform ONE Secure Subscription with EW Support for
250 endpoints per year
EP1-SEC-S-C-250-EWP Extreme Platform ONE Secure Subscription with EW Premier
Support for 250 endpoints per year
EP1-SEC-S-C-250-PSS Extreme Platform ONE Secure Subscription with PSS Support for
250 endpoints per year
EP1-SEC-S-C-1K-EW Extreme Platform ONE Secure Subscription with EW Support for
1,000 endpoints per year
EP1-SEC-S-C-1K-EWP Extreme Platform ONE Secure Subscription with EW Premier
Support for 1,000 endpoints per year
EP1-SEC-S-C-1K-PSS Extreme Platform ONE Secure Subscription with PSS Support for
1,000 endpoints per year
EP1-SEC-S-C-10K-EW Extreme Platform ONE Secure Subscription with EW Support for
10,000 endpoints per year
EP1-SEC-S-C-10K-EWP Extreme Platform ONE Secure Subscription with EW Premier
Support for 10,000 endpoints per year
EP1-SEC-S-C-10K-PSS Extreme Platform ONE Secure Subscription with PSS Support for
10,000 endpoints per year
EP1-SEC-S-C-100K-EW Extreme Platform ONE Secure Subscription with EW Support for
100,000 endpoints per year
EP1-SEC-S-C-100K-
EWP
Extreme Platform ONE Secure Subscription with EW Premier
Support for 100,000 endpoints per year
EP1-SEC-S-C-100K-PSS Extreme Platform ONE Secure Subscription with PSS Support for
100,000 endpoints per year
EP1-SECPLUS-S-C-50-
EW
Extreme Platform ONE Secure Plus Subscription with EW Support
for 50 endpoints and 50 remote users per year
EP1-SECPLUS-S-C-50-
EWP
Extreme Platform ONE Secure Plus Subscription with EW Premier
Support for 50 endpoints and 50 remote users per year
EP1-SECPLUS-S-C-50-
PSS
Extreme Platform ONE Secure Plus Subscription with PSS Support
for 50 endpoints and 50 remote users per year
Subscription Part Numbers
36 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 37 -->

Management | Extreme Platform ONE™
Networking & ExtremeCloud IQ (New)
Subscriptions and Account Linking on page 37
Subscription Management on page 38
General Subscription Management on page 45
Contracts on page 48
Note
All content in this chapter applies to both management applications, Extreme
Platform ONE Networking and ExtremeCloud IQ (New), unless otherwise noted.
Manage subscriptions and trials on the Subscriptions & Licensing page. You can search for
subscriptions, verify the subscription status, and filter results to view specific details.
It is helpful to understand the interrelationship between contracts, subscriptions, and
entitlements. See License Entitlement Management on page 12.
Subscriptions and Account Linking
You can use Extreme Platform ONE Standard Networking subscriptions for the following
products:
• Extreme Platform ONE Networking
• ExtremeCloud IQ (New)
• ExtremeCloud IQ (Classic)
• ExtremeCloud IQ Controller
• ExtremeCloud IQ Site Engine
To activate the Extreme Platform ONE Standard Networking subscriptions that you purchased,
you must link your Extreme Portal account. For detailed instructions, see:
• Link Your Extreme Portal Account | Extreme Platform ONE Networking or ExtremeCloud IQ
(New) on page 14
• Link Your Extreme Portal Account | ExtremeCloud IQ (Classic) on page 14
Note
You can link your Extreme Portal account either in Extreme Platform ONE Networking
or ExtremeCloud IQ. If either is already linked, new subscriptions are automatically
available for both applications.
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 37


<!-- page 38 -->

Related Links
Link Your Extreme Portal Account | Extreme Platform ONE Networking or ExtremeCloud IQ
(New) on page 14
ExtremeCloud IQ Pilot Twin Subscription Provides Backwards Compatibility
Some versions of ExtremeCloud IQ Site Engine and ExtremeCloud IQ Controller do not
support Extreme Platform ONE Standard Networking subscriptions. To provide you with the
necessary time to upgrade to later versions, every Extreme Platform ONE Standard Networking
subscription includes an ExtremeCloud IQ Pilot Twin subscription with the same start date,
end date, and subscription quantity.
• The Extreme Portal displays both Extreme Platform ONE Standard Networking and
ExtremeCloud IQ Pilot Twin subscriptions.
• ExtremeCloud IQ (Classic) and ExtremeCloud IQ (New) do not display ExtremeCloud IQ
Pilot Twin subscriptions.
• Extreme Platform ONE applications 1 do not display ExtremeCloud IQ Pilot Twin
subscriptions.
• ExtremeCloud IQ Site Engine version 25.2 and earlier supports ExtremeCloud IQ Pilot and
ExtremeCloud IQ Pilot Twin subscriptions.
• ExtremeCloud IQ Site Engine version 25.5 and later supports ExtremeCloud IQ Pilot and
Extreme Platform ONE Standard Networking subscriptions.
• ExtremeCloud IQ Controller versions support ExtremeCloud IQ Pilot and ExtremeCloud IQ
Pilot Twin subscriptions.
1 Extreme Platform ONE Networking or Extreme Platform ONE Security
Note
If you purchased Extreme Platform ONE Standard Networking subscriptions and are
running management application versions that are incompatible with them, you can
use the provided ExtremeCloud IQ Pilot Twin subscriptions.
Contracts that include Extreme Platform ONE Standard Networking subscriptions
identify the Pilot Twin subscriptions as XIQ-CHILD-PIL-S-C-PWP or XIQ-CHILD-PIL-
S-C-EW.
Subscription Management
View and manage subscriptions on the Subscriptions & Licensing page. You can view all
subscriptions and licenses on the Global tab, or select one of the following tabs:
• Wired & Wireless
• Credits
• Security
• SD-WAN
ExtremeCloud IQ Pilot Twin Subscription Provides
Backwards Compatibility
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
38 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 39 -->

Available options depend on your subscriptions, and user role. If you have not already
purchased a subscription, you can request a free trial from the application or service tab.
Note
Subscriptions were previously referred to as licenses. The terms are not
interchangeable. For information about the difference, see License Entitlement
Management on page 12.
The following table describes terms related to contracts, subscriptions, and entitlements.
Table 14: Subscription management terminology
Term Description
Activate To use a subscription. When you manually
assign a subscription to a device, or when
the system automatically assigns an available
subscription.
Contract All-encompassing, a contract can include
multiple subscriptions and includes pricing
and terms.
Entitlement Entitlement refers to the right to use
a feature or function. There can be
multiple entitlements for one subscription.
For example, a subscription can include a
cloud management entitlement and a TAC/OS
entitlement.
Typically, an entitlement has a meter that
determines the unit of measure for the
feature it covers. For example, an entitlement
can be per-device or per-user.
Purchase Buy the product or service. For more
information about purchasing products or
services, contact an official Extreme Networks
Partner.
Renew Extend an existing contract or subscription.
Revoke Return an activated subscription to the
license pool.
Subscription Includes a start and end date and provides
access to the management application
products. A subscription provides explicit
Extreme Networks entitlements.
Subscription Management Example
In this example, the customer has two contracts:
• Contract 123, which includes the following:
◦ 30 Tier A subscriptions
◦ 20 Tier B subscriptions
◦ 15 MACsec licenses
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) Subscription Management Example
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 39


<!-- page 40 -->

• Contract 456, which includes 50 Tier A subscriptions.
Tier A and Tier B subscriptions are per device, and include the following entitlements:
• Management
• TAC / OS for eligible devices
• Premier Features for eligible devices
MACsec licenses are per device, and include the MACsec entitlement.
Therefore, the customer can make the following assignments:
• Tier A subscriptions to 80 devices (3 entitlements)
• Tier B subscriptions to 20 devices (3 entitlements)
• MACsec licenses to 15 devices (1 entitlement)
Related Links
Subscriptions & Licensing User Interface on page 41
Subscription Management Example
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
40 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 41 -->

Subscriptions & Licensing User Interface
Figure 2 identifies elements and features available on the Subscriptions & Licensing page.
See Table 15 for descriptions of the numbered elements.
Figure 2: Subscriptions & Licensing interface
Table 15: Subscriptions & Licensing interface descriptions
Callout Interface Area Description
1 Global tab Displays all subscriptions for all applications and
services when unfiltered. The following columns
display the total number of subscriptions, the
number of active subscriptions, and the number
still available.
• Total = sum of all subscriptions available to use
= sum all of the same subscription type with
start date in the past and end date in the future
= exclude expired and not yet valid
• Active = sum of all subscriptions currently in
use
• Available = Total minus Active
These numbers fluctuate as subscriptions are
applied or removed from a device or devices.
To display details for a specific application or
service, select the corresponding tab.
2 CUID The unique ID associated with the license pool. The
CUID is very important when communicating with
support personnel.
3 Extreme Portal link status Indicates whether ExtremeCloud IQ is linked to
your Portal account. The account must be linked
to see content of the license pool.
4 Link / Unlink Toggle the link status between ExtremeCloud IQ
and your Extreme Portal account.
Caution: Use Unlink only for troubleshooting when
directed by Support personnel.
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) Subscriptions & Licensing User Interface
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 41


<!-- page 42 -->

Table 15: Subscriptions & Licensing interface descriptions (continued)
Callout Interface Area Description
5 Synchronize Subscriptions Synchronize the display of your Extreme Platform
ONE Networking subscriptions with the license
pool.
6 Request Create a purchase request that you can submit to
your partner for review and to get a quote.
7 3-dot menu Displays action options:
• Request History
• Manage NAC Allocations
• Contact Support
• Contact Sales
8 View Select Simple, or group subscriptions according to
the Description or by Product.
9 Columns Customize the columns that you see on the page.
(Unavailable when you sort by Product.)
10 Filter Filter the table by Entitlement, Product, or Status.
Purchase a Subscription
As you expand your system, you can purchase new subscriptions of the appropriate
subscription types to cover additional devices, according to your needs.
For more information, you can contact sales or complete the workflow to create a subscription
request and print the form to submit to your Extreme Networks partner.
Create a Subscription Request
Use this task to create a subscription request to send to your Extreme Networks Preferred
Partner.
You can initiate a subscription request from multiple Extreme Platform ONE Networking entry
points.
Note
Subscription Request is not available for Managed Service Provider (MSP) accounts.
1. Go to Subscriptions & Services > Subscriptions & Licensing, and then select Request.
Alternatively, in Extreme Platform ONE you can go to Subscriptions & Services >
Contracts, and then select Request.
2. Select Request Quote.
3. In the Request Process dialog, read the information and then select OK.
Tip
If you prefer not to see this information for future requests, select Don't show this
message again.
Purchase a Subscription
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
42 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 43 -->

4. To specify the request type, select either Subscription or Contract, and then select Next.
5. In the Select Subscriptions area, select one or more applications and then select Add.
Note
If your current deployment includes ExtremeCloud IQ Pilot subscriptions, the
Wired and Wireless category displays the following message: To unlock full
features for all devices in your network, you need additional subscriptions. To
add enough Extreme Platform ONE Standard Networking subscriptions to replace
the Pilot subscriptions, select Select & Add and follow the on-screen prompts.
6. Use the Selected Subscriptions pane to select and make changes to Duration and
Quantity in the respective fields for each requested subscription.
7. Select Next and provide additional information.
a. In General information, type your phone number.
b. (Optional) Type the name of your Preferred Partner.
c. (Optional) Type Additional Comments.
d. Select Next.
8. Review the request details in Review Request, and then select Next.
9. Save the subscription request summary document, then print or digitize it, and submit the
request to your Extreme Networks Preferred Partner.
Use the Partner Locator to find and connect with a Preferred Partner.
Add Subscriptions to an Existing Enterprise Agreement Contract
Use this task to add subscriptions to an existing Enterprise Agreement contract.
Note
This feature applies only to Extreme Platform ONE contracts that are part of an
Enterprise Agreement.
1. Go to Subscriptions & Services > Subscriptions & Licensing, and then select Request.
Alternatively, you can go to Subscriptions & Services > Contracts, and then select
Request.
2. Select Add to Enterprise Agreement.
3. On the 1 Select Contract page, select the contract to which you want to add more
subscriptions, and then select Next.
4. On the 2 Add Subscriptions page, select one or more applications and then select Add.
5. After you add subscriptions, change the Quantity for each subscription, according to your
needs.
6. Select Next.
7. (Optional) On the Contact Details page, provide additional information:
a. Type your Phone Number.
b. Type an email address to Send a copy to.
c. To add an additional email address to copy on the request, select Add recipient and
type the address.
8. Select Next.
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
Add Subscriptions to an Existing Enterprise Agreement
Contract
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 43


<!-- page 44 -->

9. Review the request details on the Review page, and then select Next.
10. In the Confirm Added Subscriptions dialog, read the conditions, and then select I agree to
confirm.
11. Select Submit.
In a few minutes, the system creates a new contract for the requested subscriptions. At the
next anniversary for the selected contract, the system updates the contract to include the
subscriptions that you added.
Renew a Subscription
Before a subscription expires, your Extreme Networks Preferred Partner will send you a renewal
quote. If you prefer, you can contact your partner proactively. To find a new partner, use the
Partner Locator.
To renew a subscription, send a subscription request to your Extreme Networks Preferred
Partner. After a subscription request is processed, Extreme Networks adds subscriptions to
the license pool for your CUID.
Related Links
Create a Subscription Request on page 42
NEW!Add a Note to a Subscription
Notes for subscriptions provide additional context that is useful when multiple admins share
the same console. In a single-admin environment, notes provide historical context. Use notes
to do the following:
• Record why you purchased a subscription.
• Leave information for whoever handles the next renewal cycle, especially if the
circumstances were unusual or involved a special agreement.
Subscription notes are synchronized and appear in the following locations:
• Extreme Platform ONE Networking, Subscriptions & Licensing
• ExtremeCloud IQ (New), Subscriptions & Licensing
• ExtremeCloud IQ Site Engine, Licensing
• ExtremeCloud IQ (Classic), License Information
Use this task to add a note to a subscription.
1. Go to Subscriptions & Services > Subscriptions & Licensing.
2. Select the subscription for which you want to add the note.
The Global tab lists all subscriptions that you have purchased, for all products. Select
Wired & Wireless or another tab to filter the table by product.
3. In the Subscription Details dialog, double-click the corresponding cell in the Notes
(Optional) column.
4. Enter the note, and then select Save.
Renew a Subscription
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
44 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 45 -->

View Subscription History
Use this task to view the history of subscription purchases, or trials and trial requests.
1. Go to Subscriptions & Services > Subscriptions & Licensing, select
 , and then select
Request History.
The Subscriptions & Licensing / Request History page organizes all subscription requests
under the Requests and Enterprise Agreements tabs. You can order more subscriptions
from either tab.
• Requests tab: Select Request and see Create a Subscription Request on page 42.
• Enterprise Agreements tab: Select Add to Agreement and see Add Subscriptions to an
Existing Enterprise Agreement Contract on page 43.
2. To see the history of subscriptions added to existing contracts that are subject to an
Enterprise Agreement, select Enterprise Agreements.
3. (Optional) Use the Search feature to refine the result set and view for a specific subset of
subscriptions.
You can view details in the columns.
4. (Optional) To download summary information for a subscription or a subscription request,
select
  for the corresponding entry, and then select Download.
To complete the download, save the file when prompted.
Related Links
Create a Subscription Request on page 42
Add Subscriptions to an Existing Enterprise Agreement Contract on page 43
General Subscription Management
Use the Subscriptions & Licensing interface to perform general subscription management
tasks, such as viewing and activating subscriptions, and managing NAC allocations.
Note
Subscription counts in the license pool fluctuate when usage changes for a product,
when a contract or a subscription expires, or after a new subscription order is
processed.
Activate a Subscription
The following actions activate (use) a subscription:
• Add a device as Managed.
• Enable an entitled application. You may need to apply entitlements in some cases (for
example, MACsec).
The following actions revoke a subscription.
• Unmanage or delete a device.
• Disable an entitled feature. You may need to revoke an entitlement manually in some cases
(for example, MACsec) before you delete the device.
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) View Subscription History
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 45


<!-- page 46 -->

View the License Pool
An license pool is a set of entitlements that are available to you, including subscriptions and
licenses. Subscriptions can have different start dates, and end dates. You can activate (assign)
subscriptions in the pool when needed and return subscriptions to the pool when you remove
them and they are no longer assigned (Active). You can view subscription expiration status;
subscription type, term start and end date; and the number of total, active, and available
subscriptions.
Subscription synchronization is automated and scheduled by the system. If you do not see
your new subscriptions and licenses on the Subscriptions & Licensing page, you can initiate
on-demand synchronization. You can synchronize subscriptions only once every 5 minutes.
Important
Do not use Synchronize Subscriptions just to refresh the information in the
management application.
1. Go to Subscriptions & Services > Global.
To view application-specific subscriptions, select the corresponding tab.
2. To search for records, start typing a search attribute such as product, subscription or
subscription type, status, or a complete or phrase or words from a description in the
Search field.
Note
Search terms are not case-sensitive.
To clear the search, select X in the Search field.
3. To group the records according to product, select View and choose Product.
The default view displays all records in alphabetical order according to the Description.
4. To filter records in a page, select Filter (
 ) and choose the filter attribute.
To clear an individual filter, click X for the appropriate filter. To clear all the filters, select
Clear All Filters.
Manage NAC Allocations | Extreme Platform ONE and ExtremeCloud IQ (New)
Use this task to allocate NAC subscriptions to devices according to your needs.
Note
ExtremeCloud IQ Site Engine must be onboarded before you can manage NAC
allocations.
1. Go to Subscriptions & Licensing and select Global.
2. At the top right corner of the page, select
 , and then select Manage NAC Allocations.
Note
The menu selection in this procedure does not appear unless you have one or
more NAC subscriptions.
3. In the NAC Entitlements Allocation window, specify the allocation percentage of the
license pool to assign to the corresponding entity.
View the License Pool
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
46 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 47 -->

4. Select Save Allocations.
View Device State and Subscription Type
Note
When the management application detects an entitlement violation state, the
application automatically unmanages devices, and the Subscription column value
for the devices changes to Not Licensed.
Table 16: State and Subscription Types
State Subscription Type Explanation
Managed Standard Tier A Standard Tier A subscription in use
Managed Standard Tier B Standard Tier B subscription in use
Managed Standard Tier C Standard Tier C subscription in use
Managed Standard Tier D Standard Tier D subscription in use
Managed Standard Tier 3RD Standard Tier Third-Party Management
Engine subscription in use
(by a third party, legacy, or
ExtremeCloud IQ Site Engine device)
Managed Pilot Pilot subscription in use
Managed Navigator Navigator subscription in use
Managed Not Applicable Ping Only device reported by
ExtremeCloud IQ Site Engine
Universal AP device reported by
ExtremeCloud IQ Controller
Digital Twin Simulated device
Unmanaged Not Applicable Device unmanaged by admin
Unmanaged Not Licensed Device subscription (entitlement)
expired
—empty— —empty— Connect level
—empty— Not Applicable Device onboarded as managed locally
Use this task to view device details, including state and subscription type.
1. To view device and state subscription details, go to Subscriptions & Services and select
Inventory.
2. (Optional) To increase the table visibility, select Show Summary to hide the Firmware
Status and Hardware Lifecycle summaries.
3. To choose which columns to display, or to reorder the columns, select
 .
Pre-provisioning and Subscription Assignment
The management application does not assign a subscription to a device until the device
connects to the cloud for the first time. Therefore, you can pre-provision new devices before
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) View Device State and Subscription Type
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 47


<!-- page 48 -->

decommissioning the old ones, even if you do not have enough subscriptions to cover all the
devices. The following example explains how the process works.
Example
AP-A represents the old devices, and AP-B represents the new devices.
AP-A is operational, the State is Managed, and the device uses a subscription.
AP-B is not connected to the Internet.
1. Add the serial number for AP-B to the management application.
2. Assign policy and configure AP-B.
AP-B does not use a subscription, and the State is New.
3. In the management application, Unmanage AP-A.
AP-A is operational and provides service. Because the State is Unmanaged, the
management application reports the device as Disconnected. The system does not collect
statistics for the device, and you cannot change the configuration.
AP-A no longer uses a subscription.
4. Connect AP-B to the Internet.
The AP-B State changes from New to Managed, and AP-B uses a subscription.
Contracts
This section applies to Extreme Platform ONE Networking only.
You can view details for each contract in the Contracts page, and you can renew a contract to
avoid service disruption. Information for each contract includes the following details:
• Contract number
The following icon indicates a contract that is part of an Enterprise Agreement:
 .
• Start and end dates
• Partner
• Contract status
• Number of line items for the contract
• Location of the site where the contract is in use.
Related Links
License Entitlement Management on page 12
Subscription Management on page 38
Contract Status Descriptions
The Contracts page displays your contract details. Colored dots indicate the contract status:
• Green—subscriptions in good standing
Contracts
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
48 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 49 -->

• Amber—needs attention
• Red—canceled
View Contract Information
The Contracts page provides information about each Extreme Platform ONE Networking
contract, including details such as start and end date and contract status.
Use this task to view contract information.
1. Go to Subscriptions & Services > Contracts.
2. To choose which columns to show, select
 , and select or clear the corresponding check
boxes.
3. To rearrange the order of the columns, select and drag a column heading in the table.
Quick-Filter Contracts by a Pending Expiration Interval
Use this task to filter contracts by a pending expiration interval.
1. Go to Subscriptions & Services > Contracts.
2. For Filters Applied, select one of the filter options:
• None
• Expires in 30 days
• Expires in 60 days
• Expires in 90 days
Related Links
Filter Contracts by Specified Date Range on page 49
Filter Contracts by Multiple Criteria on page 50
Filter Contracts by Specified Date Range
Filter contracts according to the following filter criteria:
• Before or After (Choice 1 for the specified date or dates)
• Date in mm/dd/yyyy format
• AND/OR (Boolean choices)
• Before or After ( Choice 2 for the specified date or dates)
Use this task to filter contracts by a range of dates.
1. Go to Subscriptions & Services > Contracts.
2. On the Start Date column heading, select
 .
a. In the dialog, specify your filter criteria.
b. Type the date in the correct format.
c. Select Apply.
3. To redefine your criteria, select Reset.
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) View Contract Information
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 49


<!-- page 50 -->

Related Links
Quick-Filter Contracts by a Pending Expiration Interval on page 49
Filter Contracts by Multiple Criteria on page 50
Filter Contracts by Type or Status
Use this task to filter the table according to the type of contract, or the status of the contract.
1. Go to Subscriptions & Services > Contracts.
2. On the header row, select the corresponding
  icon, and configure the settings.
Table 17: Filter settings
Filter by Settings
Type Choose Standard or Enterprise Agreement.
Status Choose from the following options:
• All
• Active
• Expired
Filter Contracts by Multiple Criteria
Filter contracts using the following criteria:
• Search box
• End Date
◦ None
◦ Expires in 30 days
◦ Expires in 60 days
◦ Expires in 90 days
• Partner
• Status
• Site
Use this task to filter contracts using multiple criteria options and the Filters sidebar.
1. Go to Subscriptions & Services > Contracts.
2. Select the Filters sidebar.
3. Select the filter criteria, and then select Apply.
4. To redefine your criteria, select Reset.
Related Links
Quick-Filter Contracts by a Pending Expiration Interval on page 49
Filter Contracts by Specified Date Range on page 49
Filter Contracts by Type or Status
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New)
50 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 51 -->

Download the Contracts Table
Use this task to download the information in the Contracts table as a CSV file. If you filter the
table, the downloaded file includes only the filtered information.
1. Go to Subscriptions & Services > Contracts.
2. (Optional) Select the filter criteria.
3. Select
 .
Renew a Contract
Renew existing contracts from within Extreme Platform ONE Networking to ensure access to
services without interruption.
Use this task to renew a contract.
1. Go to Subscriptions & Services > Subscriptions & Licensing, and then select Request.
Alternatively, in Extreme Platform ONE you can go to Subscriptions & Services >
Contracts, and then select Request.
2. Select Request Quote.
3. In the Request Process dialog, read the information and then select OK.
Tip
If you prefer not to see this information for future requests, select Don't show this
message again.
4. Select Contracts, and then select Next.
5. Select the contracts to renew, and then select Add.
6. When you finish adding contracts to the cart, select Next.
7. Provide your phone number and optional information, and then select Next.
8. Review the request details in Review Request, and then select Next.
9. Save the subscription request summary document, then print or digitize it, and submit the
request to your Extreme Networks Preferred Partner.
Use the Partner Locator to find and connect with a Preferred Partner.
Contact Sales
Contact Extreme Networks Sales for information about contracts, subscriptions, and licenses,
and for other needs you might have.
1. Go to Subscriptions & Services > Contracts and select Contact Sales.
The Contact the Extreme Networks Sales Team web page opens.
2. Complete and submit the form.
Alternatively, see Other Ways to Get in Touch, and select another contact option.
A sales representative will contact you.
Management | Extreme Platform ONE™ Networking &
ExtremeCloud IQ (New) Download the Contracts Table
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 51


<!-- page 52 -->

Management | ExtremeCloud IQ (Classic)
View the License Pool on page 52
Manage NAC Allocations | ExtremeCloud IQ on page 53
Proactive Notifications on page 53
Entitlement Violations on page 54
Activate or Revoke an ExtremeCloud IQ CoPilot Subscription on page 57
Affected Devices Table on page 57
Pre-provisioning and Subscription Assignment on page 57
Troubleshooting on page 58
The following sections provide information about entitlement management for ExtremeCloud
IQ (Classic).
Note
All references to ExtremeCloud IQ in this chapter refer to ExtremeCloud IQ (Classic).
View the License Pool
A license pool is the set of licenses and subscriptions that are available to you. Entitlements
can have different start dates, and end dates as specified in the license or subscription. You
can activate subscriptions as needed and return them to the pool when you revoke them and
they are no longer assigned (Active). You can view the expiration status; entitlement type, term
start and end date; and the number of total, active, and available licenses and subscriptions.
Note
The subscription and license information is cached. The refresh interval depends on
the location of your ExtremeCloud IQ account. To update the cached information
from the license pool on the License Information page, select Synchronize.
Go to Global Settings > Administration > License Management.
52 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 53 -->

Manage NAC Allocations | ExtremeCloud IQ
After you onboard compatible NAC engines (ExtremeCloud A3 and/or ExtremeCloud IQ Site
Engine), ExtremeCloud IQ adds the serial numbers to the NAC Entitlements table using the
following logic:
• ExtremeCloud IQ automatically allocates up to 100% of the total NAC entitlements from
the entitlement pool to the first NAC engine (no user action is required). If the allocation is
successful, the value in the Allocated % column updates. If the allocation is not successful,
the value is 0%.
• ExtremeCloud IQ automatically allocates from the remaining percentage (if any) to the next
NAC engine. For example, if the allocation for the first NAC engine is 20%, ExtremeCloud
IQautomatically allocates from the remaining 80% to the second NAC engine.
Use this procedure to modify the number of allocated ExtremeCloud IQ NAC entitlements for
an NAC engine.
1. Go to Global Settings > Administration > License Management.
2. In the NAC Entitlements table, select the serial number for the NAC engine, and then type
a new number in the Allocated % column.
The range is 0–100, with increments of 0.1. ExtremeCloud IQ sends the allocated values to
NAC engines.
3. Select SAVE.
Proactive Notifications
To help you manage subscriptions proactively, ExtremeCloud IQ provides advanced
notification of impending entitlement violations. When a subscription reaches each of the
following thresholds, Administrators see a warning banner message and, optionally, receive
email messages: 90, 60, 30, 7, 6, 5, 4, 3, 2, and 1 days before term expiration.
The banner displays the following message:
LICENSE EXPIRATION – At least one of your ExtremeCloud IQ subscriptions will expire within
XX days. Check affected devices here.
Where XX is the number of days before the subscription term expires.
The banner appears only once for each user, after the day the subscription reaches a
threshold of 90, 60, or 30 days. The system displays the banner daily, from the 7-day
threshold.
The system can also send an email notification to each user on the day the subscription
reaches a threshold of 90, 60, or 30 days. From the 7-day threshold, the system sends email
notifications daily. If multiple subscriptions reach the same threshold, the system combines
the notifications into one email. You can choose whether to opt-in to receiving the emails by
going to Global Settings > Account Details. Subscription is not automatic.
The email notifications identify the type of subscriptions nearing term expiration, and include
a CSV file attachment that lists affected devices. Each email provides additional information
about the impending entitlement violations and the next steps to take.
Management | ExtremeCloud IQ (Classic) Manage NAC Allocations | ExtremeCloud IQ
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 53


<!-- page 54 -->

Related Links
Enable or Disable Proactive Email Notifications on page 54
Enable or Disable Proactive Email Notifications
A banner introducing this feature appears once for each administrator, at login:
Email notifications about upcoming license expiration dates can be enabled/disabled here.
Select the link to open the Global Settings > Account Details page. If you select X to close the
banner, it does not appear again. Use the following procedure to enable or disable notification
emails.
1. Go to Global Settings > Account Details.
2. To receive notification emails, set the Proactive license warning email messages toggles
to ON.
If you want to opt out of receiving notification emails, set the toggles to OFF.
There is a toggle for your primary Email, and one for your Alternate Email. You can set one
or both toggles to ON or OFF.
Entitlement Violations
For devices that are approaching the subscription term expiration, the user interface displays
a banner. The banner identifies the issue and provides a link to the Device list, where you can
see which devices are affected.
LICENSE EXPIRATION - At least one of your ExtremeCloud IQ subscriptions will expire within
XX days. Check affected devices here.
The following notification banner appears when you have devices not covered by a
subscription (entitlement):
LICENSE VIOLATION - Unlicensed devices. Check affected devices here.
ExtremeCloud IQ Pilot and Extreme Platform ONE Networking
If there are not enough ExtremeCloud IQ Pilot or Extreme Platform ONE Networking
subscriptions in the license pool, the system automatically changes the managed state to
Unmanaged and the state to Not Licensed. The system unmanages enough devices to
bring the system back into compliance, starting with the most recently onboarded devices.
Unmanaged devices stop connecting to the CAPWAP server and therefore do not send the
following information:
• Traps to the cloud
• CAPWAP-borne data updates
• Statistical information, including AVC hourly data reports
Enable or Disable Proactive Email Notifications Management | ExtremeCloud IQ (Classic)
54 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 55 -->

An unmanaged device looks for another CAPWAP server, and the AP LED alternates between
amber and white as it periodically connects to Redirector. As a best practice, resolve
entitlement violations as soon as possible.
You can perform the following tasks in ExtremeCloud IQ:
• On the License Information page, synchronize the cached information from the license
pool. Alternatively, you can unlink from and relink to the Extreme Portal using your Extreme
Portal credentials.
• Contact your Extreme Networks or Extreme Networks Partner Sales Representative to
purchase or renew subscriptions.
Note
The number of Pilot licenses can be limited by a Managed Service Provider (MSP).
If an MSP partner manages your account, contact them to increase the limit.
Related Links
Affected Devices Table on page 57
ExtremeCloud IQ Pilot on page 23
ExtremeCloud IQ Legacy Entitlement Keys on page 33
ExtremeCloud IQ Navigator
If there are not enough Navigator subscriptions in the pool, ExtremeCloud IQ automatically
assigns a higher-tier subscription if one is available. View the number of available and
activated subscriptions in Global Settings > Administration > License Management.
Related Links
Affected Devices Table on page 57
ExtremeCloud IQ Navigator on page 25
ExtremeCloud IQ Pilot and Extreme Platform ONE Networking on page 54
ExtremeCloud IQ CoPilot
When a CoPilot subscription expires, the covered device is not CoPilot-entitled. The CoPilot
feature excludes devices not CoPilot-entitled and does not process data from those devices.
Anomalies and statistical reports are not reported in CoPilot. If you have devices for which the
CoPilot subscription has expired, a banner displays the following information:
Some CoPilot eligible devices do not have a CoPilot license allocated. To benefit from the
full value of CoPilot, consider adding CoPilot licenses for all devices that are eligible. Contact
your Extreme or partner representative for assistance. Check affected devices here.
The banner appears only on the CoPilot dashboard. After you dismiss the banner, it does not
reappear for a week.
While the CoPilot entitlement violation is active, standard CoPilot features are not affected
unless there is an active Pilot entitlement violation. CoPilot entitlement violations and Pilot
entitlement violations can be active at the same time.
Management | ExtremeCloud IQ (Classic) ExtremeCloud IQ Navigator
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 55


<!-- page 56 -->

To resolve a CoPilot entitlement violation:
• Contact your Extreme Networks or Extreme Networks Partner Sales Representative to
purchase the required number of subscriptions, or renew expired subscriptions.
• Revoke CoPilot entitlements. Go to Manage > Devices and select the devices to exclude
from CoPilot monitoring. From the Actions menu, select Change CoPilot License Status >
Revoke CoPilot Licenses.
• Change managed CoPilot-eligible devices to unmanaged.
• Update the cached information from the entitlement pool. Go to Global Settings >
Administration > License Management and select Synchronize.
Alternatively, you can unlink from and relink to the Extreme Portal using your Extreme Portal
credentials.
• Disable CoPilot functions in Global Settings > Administration > VIQ Management >
Disable CoPilot feature for this VIQ.
Multiple accounts
To help prevent subscription shortages, you can select which VIQs (accounts) use
CoPilot. Enable or disable CoPilot for each ExtremeCloud IQ account in Global Settings >
Administration > VIQ Management > Enable/Disable CoPilot feature for this VIQ.
Note
If you have multiple ExtremeCloud IQ accounts with CoPilot linked to the same
entitlement pool, there might not be enough licenses to satisfy your requirements.
For example, if two branches in different geolocations share the same pool, the first
come, first served rule applies. To resolve this situation, do one of the following:
• Disable ExtremeCloud IQ CoPilot for the ExtremeCloud IQ account that is in
violation.
• Add the required number of ExtremeCloud IQ CoPilot licenses.
Related Links
Affected Devices Table on page 57
Unlink and Relink Your Extreme Portal Account | ExtremeCloud IQ (Classic) on page 16
ExtremeCloud IQ CoPilot on page 24
ExtremeCloud IQ NAC
Network access control (NAC) entitlement violations are product-specific. Each NAC engine
handles an NAC entitlement violation in a different way.
To resolve an ExtremeCloud IQ NAC entitlement violation:
• Contact your Extreme or Extreme Partner Sales Representative to purchase or renew
subscriptions.
• Increase the allocated NAC quantity for your NAC engine.
• On the License Information page, synchronize the cached information from the license
pool. Alternatively, you can unlink from and relink to the Extreme Portal using your Extreme
Portal credentials.
ExtremeCloud IQ NAC Management | ExtremeCloud IQ (Classic)
56 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 57 -->

Related Links
ExtremeCloud IQ NAC on page 25
Activate or Revoke an ExtremeCloud IQ CoPilot Subscription
ExtremeCloud IQ CoPilot must be enabled and the device must be CoPilot-eligible.
Use the following procedure to choose whether a CoPilot-eligible device gets a subscription.
This procedure is useful if you have fewer CoPilot subscription than eligible devices.
1. Go to Manage > Devices.
2. Select the device for which you want to activate or revoke the CoPilot subscription.
3. From the Actions menu, select Change CoPilot License Status > Activate CoPilot License
or Revoke CoPilot License.
Affected Devices Table
Entitlement notifications and violation banners include a link to the Affected Devices table.
The table shows devices with subscriptions approaching the expiration date. Some table
columns are specific to the subscription notification or violation banner.
• The License column shows the type of subscription.
• The Subscription End Date column shows the date when the subscription will expire.
Pre-provisioning and Subscription Assignment
ExtremeCloud IQ does not assign a subscription to a device until the device connects to the
cloud for the first time. Therefore, you can pre-provision new devices before decommissioning
the old ones, even if you do not have enough subscriptions to cover all the devices. The
following example explains how the process works.
Example
AP-A represents the old devices, and AP-B represents the new devices.
AP-A is operational, the State is Managed, and the device uses a subscription.
AP-B is not connected to the Internet.
1. Add the serial number for AP-B to ExtremeCloud IQ.
2. Assign policy and configure AP-B.
AP-B does not use a subscription, and the State is New.
3. In ExtremeCloud IQ, Unmanage AP-A.
AP-A is operational and provides service. Because the State is Unmanaged, ExtremeCloud
IQ reports the device as Disconnected. The system does not collect statistics for the
device, and you cannot change the configuration.
AP-A no longer uses a subscription.
4. Connect AP-B to the Internet.
Management | ExtremeCloud IQ (Classic) Activate or Revoke an ExtremeCloud IQ CoPilot Subscription
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 57


<!-- page 58 -->

The AP-B State changes from New to Managed, and AP-B uses a subscription.
Troubleshooting
• How do I know whether a device uses a Pilot subscription, a Navigator subscription, a
Legacy Entitlement Key, or has no entitlement?
• How do I determine which devices have CoPilot subscription?
• How do I check which devices use MACsec or Premier switch licenses?
• How do I know which licenses and subscriptions are in the licenses pool?
• How do I know how many licenses and subscriptions are available to use, and how many are
activated?
• The license and subscription information I see in ExtremeCloud IQ does not reflect reality.
How do I refresh cached information?
• How do I realign an ExtremeCloud IQ Navigator subscription?
• What do I need to know about unmanaged devices?
Q: How do I know whether a device has an Extreme Platform ONE™ Networking subscription,
Pilot subscription, Navigator subscription, a Legacy Entitlement Key, or no entitlement?
A: In ExtremeCloud IQ, go to Manage > Devices. The Device License table column indicates
that a device uses a license or subscription, or neither. If this column does not appear in your
table, use the column picker to add it to the displayed columns. Column values are:
• Pilot: An ExtremeCloud IQ Pilot subscription
• Navigator: An ExtremeCloud IQ Navigator subscription
• Legacy: An ExtremeCloud IQ Legacy Entitlement Key
• Standard Tier A: Extreme Platform ONE Standard Networking Subscription Tier A
• Standard Tier B: Extreme Platform ONE Standard Networking Subscription Tier B
• Standard Tier C: Extreme Platform ONE Standard Networking Subscription Tier C
• Standard Tier D: Extreme Platform ONE Standard Networking Subscription Tier D
• Not Applicable: No entitlement is required
Use Filter > License > Device License to determine the quantities of each value.
Q: How do I determine which devices have CoPilot subscription?
A: In ExtremeCloud IQ, navigate to Manage > Devices. The CoPilot column indicates devices
that have CoPilot entitlements as either Active, or None.
The following entitlement status values can apply to CoPilot-eligible devices:
None
This status appears for the following reasons:
• CoPilot is not enabled for the VIQ.
• The device is not CoPilot compatible.
• The device is unmanaged.
• An administrator revoked the subscription.
Troubleshooting Management | ExtremeCloud IQ (Classic)
58 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0


<!-- page 59 -->

Active
The CoPilot subscription is in use (consumed).
Unlicensed
The CoPilot subscription is expired.
If the CoPilot column does not appear in the table, use the column picker to add it. Use the
Filter > License > CoPilot option to determine the quantity.
Q: How do I check which devices use MACsec or Premier switch entitlements?
A: In ExtremeCloud IQ, navigate to Manage > Devices. The Feature License column value
indicates whether the switch uses a MACsec, Premier, or both licenses. If this column does not
appear in your table, use the column picker to add it to the displayed columns. Values are:
• MACsec: A MACsec switch license
• Premier: A Premier switch license
• None: No license
Q: How do I know which entitlements are in the license pool?
A: Log in to the Extreme Portal and navigate to Assets > Cloud Licenses Home.
The table contains all subscriptions and licenses in the license pool. The identifier of
the license pool is the CUID (Customer Unique Identifier). Ensure that your ExtremeCloud
IQ account is linked to the same license pool at ExtremeCloud IQ > Global Settings >
Administration > VIQ Management. If the CUID in the Extreme Portal matches the CUID in
ExtremeCloud IQ, your ExtremeCloud IQ account is linked to the same license pool.
To view entitlements compatible with ExtremeCloud IQ, go to ExtremeCloud IQ > Global
Settings > Administration > License Management > Entitlements.
Q: How do I know how many licenses or subscriptions are available to use, and how many are
activated?
A: There are three ways to do this:
• Log in to the Extreme Portal and navigate to Assets > Cloud Licenses Home >
Entitlements Summary Report. This report updates every 24 hours. Active Quantity
indicates the number of subscriptions in use. Inactive Quantity indicates the number of
subscriptions available for use. Total Quantity is the total number of used and available
subscriptions.
• The Global Settings > Administration > License Management > Entitlements table shows,
by type, the number of subscriptions that are in use, available, and a total of both. How
often this data refreshes depends on the location of your ExtremeCloud IQ account. See
the ExtremeCloud IQ Release Notes.
• The ExtremeCloud IQ > CoPilot > Licenses widget displays information about Pilot and
CoPilot used and available subscriptions.
Q: The license pool (entitlement) information that I see in ExtremeCloud IQ does not reflect
reality. How do I refresh cached license and subscription information?
Management | ExtremeCloud IQ (Classic) Troubleshooting
Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0 59


<!-- page 60 -->

A: The license and subscription information in Global Settings > Administration > License
Management > Entitlements table is cached. The refresh interval depends on the location of
your ExtremeCloud IQ account. To update the cached information from the license pool on the
License Information page, select Synchronize.
Alternatively, you can unlink from and relink to the Extreme Portal using your Extreme Portal
credentials.
Q: How do I realign an ExtremeCloud IQ Navigator entitlement?
A: If there are not enough ExtremeCloud IQ Navigator entitlements in the entitlement pool, an
ExtremeCloud IQ Pilot or an Extreme Platform ONE Standard Networking entitlement can be
used instead. For example, when ExtremeCloud IQ Navigator entitlements become available, if
more entitlements are purchased, or a device that was using an ExtremeCloud IQ Navigator
entitlement is deleted, the realignment is not automatic. To release the device entitlement and
acquire another available entitlement, use the following procedure:
1. Go to Manage > Devices.
2. Select the check boxes for devices to which you want to reassign entitlements.
3. Select Actions > Change Management Status > Unmanage Devices.
4. Select Actions > Change Management Status > Manage Devices
Q: What do I need to know about unmanaged devices?
A: Remember the following points about unmanaged devices:
• Cannot receive configuration updates, which might result in unexpected behavior or
network issues.
• Cannot participate in the ExtremeCloud IQ CoPilot anomaly detection and statistics
gathering.
• Do not require an entitlement (ExtremeCloud IQ Pilot, ExtremeCloud IQ Navigator,
ExtremeCloud IQ CoPilot, Extreme Platform ONE Standard Networking, or ExtremeCloud IQ
Legacy Entitlement Key).
Related Links
Unlink and Relink Your Extreme Portal Account | ExtremeCloud IQ (Classic) on page 16
Troubleshooting Management | ExtremeCloud IQ (Classic)
60 Extreme Platform ONE ™ Networking and ExtremeCloud IQ v25.14.0
