---
title: 'Aerohive API Migration Reference Guide Jun 2026'
source: https://documentation.extremenetworks.com/Aerohive_API_Migration_Reference_Guide.pdf
pages: 41
---

# Aerohive API Migration Reference Guide Jun 2026

Source PDF: [Aerohive_API_Migration_Reference_Guide.pdf](../../pdfs/Aerohive_API_Migration_Reference_Guide.pdf)

<!-- page 1 -->

Aerohive API Migration Reference Guide
Migrating Legacy Aerohive API to ExtremeCloud IQ
XAPI and Extreme Platform ONE Networking Common
Services
9041134-00 Rev AA
 June 2026


<!-- page 2 -->

Copyright © 2026 Extreme Networks, Inc. All rights reserved.
Legal Notice
Extreme Networks, Inc. reserves the right to make changes in specifications and other
information contained in this document and its website without prior notice. The reader should
in all cases consult representatives of Extreme Networks to determine whether any such changes
have been made.
The hardware, firmware, software or any specifications described or referred to in this document
are subject to change without notice.
Trademarks
Extreme Networks and the Extreme Networks logo are trademarks or registered trademarks of
Extreme Networks, Inc. in the United States and/or other countries.
All other names (including any product names) mentioned in this document are the property
of their respective owners and may be trademarks or registered trademarks of their respective
companies/owners.
For additional information on Extreme Networks trademarks, see: https://
www.extremenetworks.com/about-extreme-networks/company/legal/trademarks
Open Source Declarations
Some software files have been licensed under certain open source or third-party licenses.
End-user license agreements and open source declarations can be found at: https://
www.extremenetworks.com/support/policies/open-source-declaration/


<!-- page 3 -->

Table of Contents
Abstract................................................................................................................................................................................................................. v
Preface.................................................................................................................................................................................................................. vi
Text Conventions.................................................................................................................................................................................vi
Documentation and Training..................................................................................................................................................vii
Open Source Declarations..............................................................................................................................................viii
Training.......................................................................................................................................................................................... viii
Help and Support............................................................................................................................................................................viii
Subscribe to Product Announcements..................................................................................................................ix
Send Feedback.....................................................................................................................................................................................ix
Legacy Aerohive API Migration Introduction....................................................................10
Which API to Use................................................................................................................................................................................ 11
Authentication Changes...............................................................................................................................................................11
Base URL and Pagination Changes.....................................................................................................................................11
Base URL Changes................................................................................................................................................................. 12
Pagination Changes..............................................................................................................................................................12
Migration Coverage Summary................................................................................................................................................12
Known Gaps and Migration Risks.........................................................................................................................................13
Endpoints with No Replacement............................................................................................................................... 13
Behavioral Differences to Watch.................................................................................................................................14
Access API Documentation and Support............................................................................15
Migrate Authentication from ownerId to OAuth 2.0.......................................................16
Device Onboarding Endpoint Migration............................................................................. 17
Device Inventory and Delete Endpoint Migration........................................................... 18
Device Details and Statistics Endpoint Migration........................................................... 19
Default Device Password Endpoint Migration................................................................. 20
Device Location Endpoint Migration.................................................................................... 21
Network Policy Management Endpoint Migration......................................................... 22
Webhook Subscription Endpoint Migration......................................................................23
SSID Profile Endpoint Migration............................................................................................25
SSID Configuration State Endpoint Migration (CS Only)...............................................27
Identity and Credential Management Endpoint Migration......................................... 28
User Groups Endpoint Migration...........................................................................................30
Client Monitoring Endpoint Migration................................................................................. 31
Device Alarms Endpoint Migration.......................................................................................32
Aerohive API Migration Reference Guide iii


<!-- page 4 -->

Real-Time Client Location Endpoint Migration................................................................ 33
Bluetooth and BLE Endpoint Migration............................................................................. 34
Bluetooth Device Configuration...........................................................................................................................................34
Bluetooth Network Policy Configuration.......................................................................................................................35
BLE Monitoring Data..................................................................................................................................................................... 35
Switch Port Configuration and Port Type Profile Endpoint Migration....................36
Switch Port Configuration......................................................................................................................................................... 36
Port Type Profiles.............................................................................................................................................................................. 37
Presence Analytics Endpoint Migration............................................................................. 38
Legacy Endpoint Quick Reference....................................................................................... 39
Table of Contents
iv Aerohive API Migration Reference Guide


<!-- page 5 -->

Abstract
The Aerohive API Migration Reference Guide provides a complete endpoint-
by-endpoint mapping from the deprecated Aerohive API hosted at
developer.aerohive.com to the replacements in the ExtremeCloud IQ API (XAPI)
and Extreme Platform ONE Networking Common Services APIs. The guide covers
authentication changes from ownerId query parameters to OAuth 2.0 bearer tokens,
base URL and pagination differences, and migration coverage status across 53 legacy
endpoints spanning 14 functional areas. Migration notes identify full, partial, and
unavailable replacements, and document the known gaps including discontinued
Bluetooth and BLE capabilities, retired Aerohive SR series switch hardware, and
presence analytics superseded by Extreme Platform ONE Networking Client Tracking.
The guide includes task-based migration procedures and a quick-reference checklist
for all legacy endpoints. Cutoff Date: July 12, 2026. The legacy Aerohive Developer API
will be permanently shut down on July 12, 2026. After the cutoff date all requests to
legacy Aerohive endpoints will fail. See Field Notice FN-2026-526.
Aerohive API Migration Reference Guide v


<!-- page 6 -->

Preface
Read the following topics to learn about:
• The meanings of text formats used in this document.
• Where you can find additional information and help.
• How to reach us with questions and comments.
Text Conventions
Unless otherwise noted, information in this document applies to all supported
environments for the products in question. Exceptions, like command keywords
associated with a specific software version, are identified in the text.
When a feature, function, or operation pertains to a specific hardware product, the
product name is used. When features, functions, and operations are the same across an
entire product family, such as Extreme Networks switches, the product is referred to as
the switch.
Table 1: Notes and warnings
Icon Notice type Alerts you to...

Tip Helpful tips and notices for using the product

Note Useful information or instructions

Important Important features or instructions

Caution Risk of personal injury, system damage, or loss of data

Warning Risk of severe personal injury
vi Aerohive API Migration Reference Guide


<!-- page 7 -->

Table 2: Text
Convention Description
screen displays This typeface indicates command syntax, or represents
information as it is displayed on the screen.
The words enter and
type
When you see the word enter in this guide, you must type
something, and then press the Return or Enter key. Do not
press the Return or Enter key when an instruction simply
says type.
Key names Key names are written in boldface, for example Ctrl or Esc.
If you must press two or more keys simultaneously, the
key names are linked with a plus sign (+). Example: Press
Ctrl+Alt+Del
Words in italicized type Italics emphasize a point or denote new terms at the place
where they are defined in the text. Italics are also used
when referring to publication titles.
New information. In a PDF, this is searchable text.
Table 3: Command syntax
Convention Description
bold text Bold text indicates command names, keywords, and
command options.
italic text Italic text indicates variable content.
[ ] Syntax components displayed within square brackets are
optional.
Default responses to system prompts are enclosed in
square brackets.
{ x | y | z } A choice of required parameters is enclosed in curly
brackets separated by vertical bars. You must select one of
the options.
x | y A vertical bar separates mutually exclusive elements.
< > Nonprinting characters, such as passwords, are enclosed in
angle brackets.
... Repeat the previous element, for example,
member[member...].
\ In command examples, the backslash indicates a “soft” line
break. When a backslash separates two lines of a command
input, enter the entire command at the prompt without the
backslash.
Documentation and Training
Find Extreme Networks product information at the following locations:
Preface Documentation and Training
Aerohive API Migration Reference Guide vii


<!-- page 8 -->

Current Product Documentation
Release Notes
Hardware and Software Compatibility for Extreme Networks products
Extreme Optics Compatibility
Other Resources such as articles, white papers, and case studies
Open Source Declarations
Some software files have been licensed under certain open source licenses. Information
is available on the Open Source Declaration page.
Training
Extreme Networks offers product training courses, both online and in person, as well as
specialized certifications. For details, visit the Extreme Networks Training page.
Help and Support
If you require assistance, contact Extreme Networks using one of the following
methods:
Extreme Portal
Search the GTAC (Global Technical Assistance Center) knowledge base; manage
support cases and service contracts; download software; and obtain product
licensing, training, and certifications.
The Hub
A forum for Extreme Networks customers to connect with one another, answer
questions, and share ideas and feedback. This community is monitored by Extreme
Networks employees, but is not intended to replace specific guidance from GTAC.
Call GTAC
For immediate support: (800) 998 2408 (toll-free in U.S. and Canada) or
1 (408) 579 2800. For the support phone number in your country, visit
www.extremenetworks.com/support/contact.
Before contacting Extreme Networks for technical support, have the following
information ready:
• Your Extreme Networks service contract number, or serial numbers for all involved
Extreme Networks products
• A description of the failure
• A description of any actions already taken to resolve the problem
• A description of your network environment (such as layout, cable type, other relevant
environmental information)
• Network load at the time of trouble (if known)
• The device history (for example, if you have returned the device before, or if this is a
recurring problem)
• Any related RMA (Return Material Authorization) numbers
Open Source Declarations Preface
viii Aerohive API Migration Reference Guide


<!-- page 9 -->

Subscribe to Product Announcements
You can subscribe to email notifications for product and software release
announcements, Field Notices, and Vulnerability Notices.
1. Go to The Hub.
2. In the list of categories, expand the Product Announcements list.
3. Select a product for which you would like to receive notifications.
4. Select Subscribe.
5. To select additional products, return to the Product Announcements list and repeat
steps 3 and 4.
You can modify your product selections or unsubscribe at any time.
Send Feedback
The User Enablement team at Extreme Networks has made every effort to ensure
that this document is accurate, complete, and easy to use. We strive to improve our
documentation to help you in your work, so we want to hear from you. We welcome all
feedback, but we especially want to know about:
• Content errors, or confusing or conflicting information.
• Improvements that would help you find relevant information.
• Broken links or usability issues.
To send feedback, email us at Product-Documentation@extremenetworks.com.
Provide as much detail as possible including the publication title, topic heading,
and page number (if applicable), along with your comments and suggestions for
improvement.
Preface Subscribe to Product Announcements
Aerohive API Migration Reference Guide ix


<!-- page 10 -->

Legacy Aerohive API Migration
Introduction
Which API to Use on page 11
Authentication Changes on page 11
Base URL and Pagination Changes on page 11
Migration Coverage Summary on page 12
Known Gaps and Migration Risks on page 13
Extreme Networks is deprecating the legacy Aerohive API at developer.aerohive.com.
If you are currently using this API, you must migrate your integrations to Extreme
Networks APIs before the deprecation cutoff date.
Note
IMPORTANT Cutoff date: July 12, 2026. The legacy Aerohive Developer API
(developer.aerohive.com, base URL https://[rdc-id].aerohive.com/xapi/)
will be permanently shut down on July 12, 2026. After this date all requests
to legacy Aerohive endpoints will fail. Private Regional Data Center (RDC)
deployments are affected identically to public-cloud customers — there is no
grace period for private RDC accounts. Reference: Field Notice FN-2026-526.
This guide provides a complete endpoint-by-endpoint mapping from the legacy
Aerohive API to replacements in the Extreme Platform ONE Networking Common
Services (CS) API and ExtremeCloud IQ API (XAPI). For each legacy endpoint, the
replacement is identified highlighting key differences in parameters and behavior, and
notes endpoints that have no direct replacement.
Extreme Networks offers two modern API platforms as migration targets:
• Extreme Platform ONE Networking Common Services (CS) — The preferred platform
for all new integrations. CS provides the latest APIs with the richest feature set,
covering device lifecycle, assets, site and location management, alerts, notifications
and webhooks, performance monitoring, Identity and Access Management (IAM),
and audit logs.
• ExtremeCloud IQ API (XAPI) — Use XAPI when CS does not yet cover the required
capability, for example, network policy management, SSID configuration, credential
and end-user management, and client monitoring. XAPI is full-featured and mature.
The legacy Aerohive API contains 53 endpoints across 20 functional areas. Of these,
21 endpoints have full replacements, 23 have partial replacements, and 9 have no
10 Aerohive API Migration Reference Guide


<!-- page 11 -->

replacement because the underlying hardware features have been discontinued or the
functionality has not yet been exposed in the newer APIs.
Which API to Use
Extreme Networks provides two modern API platforms to replace the legacy Aerohive
API. Use Extreme Platform ONE Networking Common Services (CS) for all new
integrations, and ExtremeCloud IQ API (XAPI) for capabilities not yet available in CS.
Table 4: API platform selection guide
API platform Base URL When to use
Extreme Platform ONE
Networking Common Services
(CS)
https://cloudapi.extremecloudiq.com/
{service}/v1/
Preferred for all new integrations. CS provides the latest
APIs with the richest feature set. CS covers device lifecycle,
assets, site and location management, alerts, notifications
and webhooks, performance monitoring, Identity and
Access Management (IAM), and audit logs.
ExtremeCloud IQ API (XAPI) https://api.extremecloudiq.com/ Use when CS does not cover the required capability,
for example, network policy management, SSID
configuration, credential and end-user management, and
client monitoring. Full-featured and mature.
Authentication Changes
The legacy Aerohive API used an ownerId query parameter on every request to
identify the customer. The new APIs use OAuth 2.0 bearer tokens. All integrations
must switch from ownerId query parameter authentication to OAuth 2.0 bearer token
authentication. The bearer token implicitly identifies your organization, do not include
ownerId on each request.
Use the following task to migrate your authentication:
1. Obtain an API access token from ExtremeCloud IQ or Extreme Platform ONE
Networking.
2. Include the token in every request as: Authorization: Bearer <your-token>
3. Remove all ownerId query parameters from your requests.
Note
For step-by-step instructions on updating your requests, see Migrate
Authentication from ownerId to OAuth 2.0 on page 16.
Base URL and Pagination Changes
Migrating from the legacy Aerohive API requires updating base URLs and pagination
parameters in all existing API calls.
Legacy Aerohive API Migration Introduction Which API to Use
Aerohive API Migration Reference Guide 11


<!-- page 12 -->

Base URL Changes
Replace the legacy base URL with the appropriate new base URL for your target API
platform.
Table 5: Base URL mapping
Legacy base URL New base URL
https://[rdc-id].aerohive.com/xapi/
Note:
rdc-id is the Regional Data Center identifier assigned to the
customer's account.
XAPI: https://api.extremecloudiq.com/
CS: https://cloudapi.extremecloudiq.com/{service}/v1/
Pagination Changes
Pagination parameter names and index bases differ between the legacy API and the
new APIs.
• Legacy API: Uses page (0-based) and pageSize (default varies, up to 1000).
• New APIs: Uses page and limit with varying base indexes. XAPI uses 0-based page
indexing. Some CS APIs use 1-based page indexing. Always check the specific API
documentation for pagination semantics.
Migration Coverage Summary
The legacy Aerohive API contains 53 endpoints across 20 functional areas. The following
table summarizes migration coverage by category.
Table 6: Migration coverage by category
Coverage Functional areas Endpoint count Description
Full 10 21 Complete replacement available in XAPI or Common
Services.
Partial 5 23 Core functionality is covered. Some edge case
features are missing or migration involves a successor
capability (for example Extreme Platform ONE
Networking Client Tracking) rather than a 1:1 API.
No replacement 5 9 No equivalent in newer APIs (for example,
discontinued hardware, BLE, or UI-only
management).
For a complete list of all endpoints and their individual replacement status, see Legacy
Endpoint Quick Reference on page 39. For details on endpoints with no replacement,
see Known Gaps and Migration Risks on page 13.
Base URL Changes Legacy Aerohive API Migration Introduction
12 Aerohive API Migration Reference Guide


<!-- page 13 -->

Known Gaps and Migration Risks
Some legacy Aerohive API endpoints have no equivalent in the current ExtremeCloud
IQ API (XAPI) or Extreme Platform ONE Networking Common Services APIs. Additional
behavioral differences require code changes beyond simple endpoint substitution.
Endpoints with No Replacement
The following legacy capabilities have no equivalent in the current XAPI or Common
Services APIs. These are primarily related to hardware features that have been
discontinued or capabilities not yet exposed in the external API.
Table 7: Legacy endpoints with no replacement
Capability Legacy endpoints Details
Bluetooth and BLE device configuration 3 endpoints BLE and iBeacon configuration for each device. The Aerohive BLE
hardware feature has been discontinued. No replacement is planned.
Bluetooth and BLE network policy
configuration
2 endpoints BLE configuration templates at the policy level. The hardware has
been discontinued. No replacement is planned.
BLE monitoring data 1 endpoint Real-time BLE beacon inventory and monitoring, used for asset
tracking and wayfinding. No replacement is available.
Switch port configuration (write) 1 endpoint Applies only to Aerohive SR series switches, which reach End of
Support Life on January 5, 2027, and are not supported in Extreme
Platform ONE Networking. Read-only port information is available
through XAPI D360. No write replacement is planned because the
hardware platform is being retired.
Port type profiles 2 endpoints Port type profile management is not exposed in any newer API. These
profiles are managed through the ExtremeCloud IQ user interface
only.
Presence analytics 3 endpoints No direct API replacement exists. The underlying Presence Engine
feature is effectively superseded by Extreme Platform ONE
Networking Client Tracking.
Tip:
If your integration depends on foot traffic or engagement analytics,
Client Tracking provides the successor capability.
Credential delivery (email and SMS) 2 endpoints Email and SMS notification is available through the createUserGroup
API at the user group level. PCG key email covers a subset
of workflows. Per-credential delivery calls and credential renewal
(expiration extension) have no direct equivalent.
Legacy Aerohive API Migration Introduction Known Gaps and Migration Risks
Aerohive API Migration Reference Guide 13


<!-- page 14 -->

Behavioral Differences to Watch
The following behavioral differences require code updates beyond simple endpoint
substitution.
• Authentication: The legacy API used the ownerId query parameter. The new APIs
require OAuth 2.0 bearer tokens.
• Pagination: The legacy API used page (0-based) and pageSize. The new APIs require
page and limit with varying base indexes.
• Time parameters: The legacy API accepted natural language values such as 7 days
ago. The new APIs require epoch milliseconds.
• PSK retrieval: The legacy API exposed raw PSK values. XAPI intentionally does not
return raw keys as a security improvement. If your integration reads PSK values, you
must store the PSK values separately.
• Alarms: The legacy API supported cross-device queries. XAPI listAlerts API
supports cross-device alert queries. The CS Alert API is also available for cross-device
use.
• Client location: The legacy API was AP-centric, queried by AP MAC address. XAPI is
client-centric, queried by client MAC address.
• Device delete: The legacy API used DELETE with query parameters. The new APIs use
POST with a filter body.
• Credential model: Legacy credentials map to XAPI endusers. Field names and
object structures differ.
Behavioral Differences to Watch Legacy Aerohive API Migration Introduction
14 Aerohive API Migration Reference Guide


<!-- page 15 -->

Access API Documentation and
Support
Use the the following task for Extreme Networks developer portals and support
resources to begin your migration.
1. Access the API documentation for your target platform.
• Extreme Platform ONE Networking developer portal: https://
developer.extremeplatformone.com
• ExtremeCloud IQ API (XAPI) base URL: https://api.extremecloudiq.com/
2. Contact Extreme Networks support if you need migration assistance.
• Contact your Extreme Networks account team.
• Submit a case through the Global Technical Assistance Center (GTAC): https://
extremeportal.force.com
Aerohive API Migration Reference Guide 15


<!-- page 16 -->

Migrate Authentication from ownerId to
OAuth 2.0
Use the following task to update your API requests to use OAuth 2.0 bearer token
authentication in place of the legacy ownerId query parameter.
1. Obtain an API access token from ExtremeCloud IQ or Extreme Platform ONE
Networking.
For token generation instructions, see the ExtremeCloud IQ API documentation at
https://api.extremecloudiq.com/ or the Extreme Platform ONE Networking developer
portal at https://developer.extremeplatformone.com.
2. Add the bearer token to the Authorization header of every API request.
Authorization: Bearer <your-token>
3. Remove all ownerId query parameters from your API requests.
The bearer token implicitly identifies your organization. Including ownerId is no
longer required or supported.
Your API requests use OAuth 2.0 bearer token authentication and are compatible with
both XAPI and CS endpoints.
16 Aerohive API Migration Reference Guide


<!-- page 17 -->

Device Onboarding Endpoint Migration
Coverage: full. Complete replacements are available in both Extreme Platform
ONE Networking Common Services and ExtremeCloud IQ API (XAPI) for all device
onboarding endpoints.
Table 8: Device onboarding endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
POST /v1/configuration/
device/inventory/
onboarding
Onboard devices by
serial number.
CS
(preferr
ed)
POST /device-lifecycle-
mgmt/v1/devices/onboard/
wireless
POST /device-lifecycle-
mgmt/v1/devices/onboard/
wired
Separate wireless and
wired onboarding
endpoints. CS also
supports bulk import
through XLSX.
Request body changes:
legacy uses {sns: [...],
deviceIds: [...]} . CS uses
device-type-specific request
bodies. The legacy ownerId
parameter is replaced by bearer
token.
POST /v1/configuration/
device/inventory/
onboarding
Onboard devices by
serial number (XAPI
alternative).
XAPI POST /devices/:onboard
POST /devices/:advanced-
onboard
Simple or advanced
onboarding. Advanced
onboarding supports
asynchronous (long-
running operation)
mode.
XAPI :advanced-onboard adds
network policy assignment
during onboarding. This
capability is not available in the
legacy API.
Aerohive API Migration Reference Guide 17


<!-- page 18 -->

Device Inventory and Delete Endpoint
Migration
Coverage: full. Complete replacements are available in XAPI and CS for all device
inventory and delete endpoints.
Table 9: Device inventory and delete endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/monitor/devices List all devices
(paginated, with active
client count).
XAPI
(richer)
GET /devices  (many filter
and view variants)
Far richer device listing
with filters by location,
model, status, and
more.
Legacy pageSize default is
1000. XAPI uses the limit
parameter. Legacy returns
locations as a string array.
XAPI returns structured location
objects.
GET /v1/monitor/devices List all devices (CS
alternative).
CS GET /asset/v1/devices/
filters
Asset API
with attribute-based
filtering.
CS Asset API focuses on
asset-management views (serial
number, model, lifecycle state).
For operational status, use XAPI.
GET /v1/monitor/devices/
{deviceId}
Get device details
including IP, MAC, CPU,
memory, interfaces,
and alarms.
XAPI GET /d360/overview/
devices-summary?
deviceId={id}
GET /d360/device/
metadata?deviceId={id}
GET /d360/device/stats?
deviceId={id}&startTime=
...&endTime=...
GET /d360/device/
interfaces?
deviceModel=...
Device details split
across multiple
D360 endpoints for
modularity.
Legacy returned all device
information in one call. XAPI
separates metadata, stats,
interfaces, and issues into
distinct endpoints. startTime
and endTime require epoch
milliseconds, not natural
language values.
DELETE /v1/configuration/
device?ids=...
Delete onboarded
devices by ID list.
CS
(preferr
ed)
POST /device-lifecycle-
mgmt/v1/devices/:delete
Bulk delete with a
device filter.
Legacy uses DELETE with the
ids query parameter. CS and
XAPI use POST with a filter body.
DELETE /v1/configuration/
device?ids=...
Delete onboarded
devices by ID list (XAPI
alternative).
XAPI POST /devices/:delete Delete with
XiqDeviceFilter
body and
optional force_delete
parameter.
XAPI adds a force_delete
option not available in the
legacy API.
18 Aerohive API Migration Reference Guide


<!-- page 19 -->

Device Details and Statistics Endpoint
Migration
Coverage: full. Complete replacements are available in XAPI and CS for all device details
and statistics endpoints.
Table 10: Device details and statistics endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/monitor/devices/
{deviceId}
Detailed device
information: IP, MAC,
OS, CPU, memory,
uptime, interfaces, and
alarms.
XAPI GET /d360/device/
metadata?deviceId={id}
GET /d360/device/stats?
deviceId={id}&startTime=
...&endTime=...
GET /d360/device/
interfaces?
deviceModel=...
GET /d360/device/issues?
deviceId={id}&startTime=
...&endTime=...
Split into metadata
(static), stats (time-
range), interfaces
(model-based), and
issues.
Legacy time parameters used
natural language such as 1
day ago . XAPI requires epoch
milliseconds.
GET /v1/monitor/devices/
{deviceId}
Device details
(CS alternative for
analytics).
CS POST /performance-
monitor/v1/analytics/
device-health
Time-series device
health analytics
including CPU,
memory, and
throughput.
CS Performance Monitor is
for analytical and time-series
use cases, not real-time status
queries.
GET /v1/monitor/devices/
{deviceId}/clientList
List wired clients
connected to a device.
XAPI POST /d360/client/grid?
deviceId={id}&startTime=
...&endTime=...
Richer client grid with
filtering, sorting, and
connection status.
Legacy returned basic client
MAC, connection status, and
port. XAPI adds health scores,
usage statistics, and SSID
information.
Aerohive API Migration Reference Guide 19


<!-- page 20 -->

Default Device Password Endpoint
Migration
Coverage: full. A complete replacement is available in XAPI for the default device
password endpoint.
Table 11: Default device password endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
PUT /v1/configuration/
devices/devicepassword
Set the default device
password.
XAPI GET /account/viq/
default-device-password
PUT /account/viq/
default-device-password
Get and update
the default device
password.
XAPI exposes both a GET
endpoint to read the current
password and a PUT endpoint to
update. The legacy API provided
only the PUT operation. No CS
equivalent is available.
20 Aerohive API Migration Reference Guide


<!-- page 21 -->

Device Location Endpoint Migration
Coverage: full. Complete replacements are available in CS and XAPI for all device
location (AP location folder) endpoints.
Table 12: Device location endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
apLocationFolders
Get the location folder
hierarchy (tree of
GENERIC, BUILDING,
and FLOOR nodes).
CS
(preferr
ed)
GET /site-location/v1/
tree
Full location tree
with sites, buildings,
and floors. Supports
parentId filter and
expandChildren.
Legacy used a flat
FolderTreeNode with
folderType. CS uses a typed
hierarchy of sites, buildings,
floors, and zones, each with
dedicated endpoints.
GET /v1/configuration/
apLocationFolders/
{folderId}
Get a specific location
folder node.
CS GET /site-location/v1/
sites/{id}
GET /site-location/v1/
buildings/{id}
GET /site-location/v1/
floors/{id}
Type-specific retrieval
by entity type.
You must know the entity type
to call the correct endpoint. Use
GET /tree  first to discover the
hierarchy.
GET /v1/configuration/
apLocationFolders
Get the location
folder hierarchy (XAPI
alternative).
XAPI GET /locations/tree?
expandChildren=true
GET /locations/site
GET /locations/building
GET /locations/floor
GET /locations/site/{id}
GET /locations/building/
{id}
GET /locations/floor/
{id}
Full location create,
read, update, and
delete (CRUD)
operations for sites,
buildings, floors, and
zones.
XAPI provides full lifecycle
management. The legacy
API was read-only. XAPI
also supports device location
assignment through PUT /
devices/{id}/location.
Aerohive API Migration Reference Guide 21


<!-- page 22 -->

Network Policy Management Endpoint
Migration
Coverage: full. Complete replacements are available in XAPI for all network policy
management endpoints.
Table 13: Network policy management endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
networkpolicy/policies
List network policies. XAPI GET /network-policies?
page=...&limit=...&keywo
rd=...
Paginated list with
keyword search and
field selection.
XAPI returns richer policy
objects (XiqNetworkPolicy)
with SSID lists and security
settings. Legacy returned basic
ID, name, and description.
PUT /v1/configuration/
networkpolicy/deploy
Deploy (push) a
network policy to
devices.
XAPI PUT /devices/{id}/
network-policy?
networkPolicyId={policyI
d}
POST /devices/network-
policy/:assign (bulk)
Per-device or bulk
policy assignment.
Legacy deploy included
configurationType (Delta or
Full) and activation scheduling.
XAPI assignment is simpler.
You may need to perform a
separate configuration push. No
CS equivalent is available.
POST /v1/configuration/
networkpolicy/
{policyId}/devices
Assign a policy to
devices by serial
number or device ID.
XAPI POST /devices/network-
policy/:assign
Bulk assignment using
XiqAssignDevicesNet
workPolicyRequest
filter body.
Legacy used an sns[] array.
XAPI uses the device filter
pattern.
22 Aerohive API Migration Reference Guide


<!-- page 23 -->

Webhook Subscription Endpoint
Migration
Coverage: full. Complete replacements are available in CS and XAPI for all webhook
subscription endpoints.
Table 14: Webhook subscription endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
POST /v1/configuration/
webhooks
Create a webhook
subscription with URL,
secret, app name, and
message type.
CS
(preferr
ed)
POST /notification/v1/
webhook
Full webhook CRUD
with bulk enable and
disable capabilities.
Legacy required ownerId,
application name, secret,
and URL. CS uses bearer
token authentication, supports
multiple webhook types, and
adds bulk operations.
POST /v1/configuration/
webhooks
Create a webhook
subscription (XAPI
alternative).
XAPI POST /subscriptions/
webhook
POST /alert-
subscriptions/webhooks
Two webhook systems:
general notifications
and alert-specific.
XAPI separates general event
webhooks from alert webhooks.
Legacy had a single webhook
system.
GET /v1/configuration/
webhooks
List webhook
subscriptions.
CS GET /notification/v1/
webhook
List all webhooks with
filtering.
GET /v1/configuration/
webhooks
List webhook
subscriptions (XAPI
alternative).
XAPI GET /subscriptions/
webhook?
page=...&limit=...&keywo
rd=...
GET /alert-
subscriptions/webhooks
Separate lists for
general and alert
webhooks.
Aerohive API Migration Reference Guide 23


<!-- page 24 -->

Table 14: Webhook subscription endpoint mapping (continued)
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
DELETE /v1/configuration/
webhooks/
{subscriptionId}
Delete a webhook
subscription.
CS DELETE /notification/v1/
webhook/{id}
Delete by ID.
DELETE /v1/configuration/
webhooks/
{subscriptionId}
Delete a webhook
subscription (XAPI
alternative).
XAPI DELETE /subscriptions/
webhook/:delete?
ids=[...] (general-bulk)
POST /alert-
subscriptions/
webhooks/:delete body
{ids:[...]} (alert - bulk)
DELETE /alert-
subscriptions/webhooks/
{id} (alert-single)
General webhooks:
bulk delete by ID list.
Alert webooks: bulk
delete. Alert webhooks:
single delete by ID.
The two XAPI webhook
systems use different bulk-
delete conventions. General
uses DELETE /subscriptions/
webhook/:delete?ids=[...]
(DELETE method, ids as
query array). Alert uses
POST /alert-subscriptions/
webhooks/:delete with {ids:
[...]} in the request body.
The legacy single-ID DELETE /
webhooks/{subscriptionId}
shape exists only on the alert
side.
Webhook Subscription Endpoint Migration
24 Aerohive API Migration Reference Guide


<!-- page 25 -->

SSID Profile Endpoint Migration
Coverage: partial. Core SSID management functionality is available in XAPI, but some
capabilities differ significantly from the legacy API, particularly PSK retrieval and per-
device SSID configuration.
Table 15: SSID profile endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/ssids List all SSID profiles (ID,
name, broadcast name,
radio band, security
mode).
XAPI GET /ssids?
page=...&limit=...
Paginated SSID list. Response schema is similar.
XAPI adds more fields per SSID.
GET /v1/configuration/ssids/
{ssidProfileId}
Get detailed SSID
profile including
access security, CWP,
RADIUS, schedules, and
advanced settings.
XAPI GET /ssids/advanced-
settings/{id}
GET /network-policies/
{id}/ssids
Profile details through
advanced settings.
SSIDs are accessed
through the network
policy context.
Legacy returned the full
profile in one call, including
access security, CWP profile,
RADIUS client profile, schedules,
and advanced settings. XAPI
splits these across multiple
endpoints.
GET /v1/configuration/
devices/{deviceId}/ssids
Get SSID configuration
for a specific device,
including per-interface
configuration and
overrides.
XAPI GET /devices/{id}/ssid/
status
POST /devices/{id}/ssid/
status/:change
POST /devices/{id}/
ssid/:override
Device-level SSID
status, enable and
disable operations, and
override management.
Legacy returned per-WiFi-
interface SSID configuration
with disable flags and overrides.
XAPI provides status and
change operations separately.
PUT /v1/configuration/
devices/{deviceId}/ssids
Update SSID
configuration for a
device.
XAPI POST /devices/{id}/
ssid/:override
POST /devices/{id}/ssid/
status/:change
Override SSID name
and password per
device, or enable and
disable SSIDs.
Legacy used a full PUT of the
SSID configuration array. XAPI
uses targeted operations.
GET /v1/configuration/ssids/
{ssidProfileId}/psk
Get PSK and PPSK
security settings,
including the raw key
value.
XAPI PUT /ssids/{id}/psk/
password (write only)
PUT /ssids/{id}/mode/psk
PUT /ssids/{id}/mode/
ppsk
XAPI provides PSK
password change and
mode switching, but
does not expose raw
PSK retrieval.
Important:
The legacy API exposed the
raw PSK key value through a
GET request. XAPI intentionally
does not return raw keys as a
security improvement. If your
integration reads PSK values,
you must store them separately.
Aerohive API Migration Reference Guide 25


<!-- page 26 -->

Table 15: SSID profile endpoint mapping (continued)
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
PUT /v1/configuration/ssids/
{ssidProfileId}
Update PSK and PPSK
settings for an SSID.
XAPI PUT /ssids/{id}/psk/
password
PUT /ssids/{id}/mode/psk
PUT /ssids/{id}/mode/
ppsk
PUT /ssids/{id}/mode/
open
PUT /ssids/{id}/mode/
dot1x
PUT /ssids/{id}/mode/wep
Granular, mode-specific
update endpoints.
Legacy used a single PUT
with the full PSK and PPSK
object. XAPI provides per-mode
endpoints for more targeted
operations.
GET/PU
T
/beta/configuration/
ssids/{ssidProfileId}/
filters
Get and set MAC
filtering rules for an
SSID (PERMIT or DENY
by MAC address or
OUI).
XAPI GET /ssids/advanced-
settings/{id}
PUT /ssids/advanced-
settings/{id}
Advanced settings
cover similar
functionality, but no
direct MAC filter
rules API has been
confirmed.
Partial: legacy had explicit MAC
filter rules with enable, default
action, and MAC and OUI
rules. XAPI advanced settings
cover overlapping functionality,
but the exact MAC filter rule
structure may differ.
Tip:
Verify MAC filter behavior in
a test environment before
deploying to production.
SSID Profile Endpoint Migration
26 Aerohive API Migration Reference Guide


<!-- page 27 -->

SSID Configuration State Endpoint
Migration (CS Only)
Coverage: full. CS provides read-only SSID configuration and state retrieval through the
Config State API.
Table 16: SSID configuration state endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/ssids
(read context)
Read SSID
configuration state.
CS POST /read-config-
state/v1/retrieve-asset-
ssid-config
POST /read-config-
state/v1/retrieve-asset-
ssid-state
CS Config State API
provides read-only SSID
configuration and state
retrieval.
CS Config State is read-only
and focuses on current device
state rather than profile
management. Use XAPI for SSID
create, read, update, and delete
operations.
Aerohive API Migration Reference Guide 27


<!-- page 28 -->

Identity and Credential Management
Endpoint Migration
Coverage: partial. Core credential (PPSK and RADIUS) create, read, update, and delete
operations are available in XAPI, but bulk delete, credential renewal, and per-credential
delivery have no direct equivalent.
Table 17: Identity and credential management endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
POST /v1/identity/credentials
/v2/identity/credentials
Create a credential
(PPSK or RADIUS)
with delivery method,
MAC binding, and user
group.
XAPI POST /endusers Create an end user
(XiqCreateEndUserReq
uest).
Legacy credentials map to
XAPI endusers. Request body
structure differs: legacy used
groupId, macBindingList, and
policy (PERSONAL or GUEST).
XAPI uses user_group_id,
password, and email fields.
GET /v1/identity/credentials
/v2/identity/credentials
Query credentials by
type, user group, name,
email, and other filters.
XAPI GET /endusers?
page=...&limit=...&user_
group_ids=...&usernames=
...
Paginated list with user
group and username
filters.
Legacy provided richer
query parameters including
credentialType, memberOf,
adUser, first name, last
name, phone, and email.
XAPI filters are simpler.
Use user_group_ids and
usernames.
PUT /v1/identity/
credentials/
{credentialId}
/v2/identity/
credentials/
{credentialId}
Update a credential. XAPI PUT /endusers/{id} Update end user
(XiqUpdateEndUserReq
uest).
DELETE /v1/identity/
credentials?ids=[...]
/v2/identity/
credentials?ids=[...]
Delete credentials by
ID list.
XAPI DELETE /endusers/{id} Delete end user by
single ID.
Legacy supported bulk delete
through an ids array. XAPI
deletes one record at a time.
28 Aerohive API Migration Reference Guide


<!-- page 29 -->

Table 17: Identity and credential management endpoint mapping (continued)
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
PUT /v1/identity/
credentials/
{credentialId}/renew
Extend or renew
credential expiration.
XAPI POST /endusers/
{id}/:regenerate-
password
Regenerate password
— not a direct renewal
equivalent.
Gap: legacy renew extended
the expiration date without
changing the credential. XAPI
regenerate-password creates
a new password. There is
no direct expiration-extension
endpoint in XAPI.
POST /v1/identity/
credentials/deliver
/v2/identity/
credentials/deliver
Deliver a credential
through email or SMS.
XAPI POST /usergroups
(createUserGroup —
includes email and SMS
notification settings)
User group creation
includes notification
delivery configuration.
Email and SMS notification
is available through the
createUserGroup API at
the user group level, not
per-credential delivery. For
Private Client Group (PCG)
key-based workflows, XAPI
also provides POST /pcgs/
key-based/network-policy-
{policyId}/keys/:email.
Identity and Credential Management Endpoint
Migration
Aerohive API Migration Reference Guide 29


<!-- page 30 -->

User Groups Endpoint Migration
Coverage: full. Complete replacements are available in XAPI and CS for all user group
endpoints, with XAPI adding full lifecycle management not available in the legacy API.
Table 18: User groups endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/identity/userGroups
/v2/identity/userGroups
Query user groups.
Returns group ID,
name, and associated
SSIDs.
XAPI
(richer)
GET /usergroups?
page=...&limit=...&passw
ord_db_location=...&pass
word_type=...
POST /usergroups
PUT /usergroups/{id}
DELETE /usergroups/{id}
Full CRUD: list, create,
update, and delete user
groups.
Legacy was read-only
(GET only). XAPI provides
full lifecycle management.
Response includes richer group
detail.
GET /v1/identity/userGroups
/v2/identity/userGroups
Query user groups (CS
alternative).
CS IAM API (endpoints for
user, group, and role
management)
CS Identity and
Access Management
(IAM) provides
comprehensive
identity management
including user groups,
roles, and permissions.
CS IAM is broader than
legacy user groups and
covers the full IAM lifecycle.
Use for Extreme Platform
ONE Networkingnative identity
management.
30 Aerohive API Migration Reference Guide


<!-- page 31 -->

Client Monitoring Endpoint Migration
Coverage: full. Complete replacements are available in XAPI for all client monitoring
endpoints, with significantly richer detail than the legacy API.
Table 19: Client monitoring endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/monitor/clients List historical and
active clients with
client MAC, host name,
IP, OS, SSID, usage, and
health scores.
XAPI GET /clients/active?
locationIds=...&deviceId
s=...&vlans=...&ssids=..
.&page=...&limit=...
Rich client listing with
filters by location,
device, VLAN, SSID,
OS, health status, and
connection type.
Legacy used startTime and
endTime to control active
versus historical results. XAPI /
clients/active is for current
clients. The /client-details/*
endpoints provide historical
views.
GET /v1/monitor/clients/
{clientId}
Get client
details including
MAC, protocol,
authentication
method, radio, receive
and transmit statistics,
and application usage.
XAPI GET /clients/{id}?
views=...&fields=...
GET /clients/
byMac/{clientMac}?
views=...&fields=...
GET /client-details/
overview/info/
{clientId}?
startTime=...&endTime=..
.
GET /client-details/
overview/chart-data/
{clientId}?
startTime=...&endTime=..
.
Multiple detail
endpoints with
customizable views
and fields. Supports
lookup by ID or MAC
address.
XAPI provides significantly
richer client detail including
roaming trail, connectivity
experience, health diagnostics,
and chart data. Legacy returned
a single flat response.
GET /v1/monitor/devices/
{deviceId}/clientList
List clients connected
to a specific device.
XAPI POST /d360/client/grid?
deviceId={id}&startTime=
...&endTime=...
Device-scoped client
grid with filtering,
sorting, and connection
status.
Legacy returned basic client
MAC, connection status, and
port. XAPI provides full client
detail per device.
Aerohive API Migration Reference Guide 31


<!-- page 32 -->

Device Alarms Endpoint Migration
Coverage: partial. Cross-device alarm queries are available in XAPI and CS, but the
legacy Aerohive Alarms system maps differently to the newer Alerts infrastructure.
Table 20: Device alarms endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/monitor/alarms?
deviceMac=...&severity=.
..&startTime=...&endTime
=...
List alarms across
devices with time
range, device MAC, and
severity filters.
XAPI GET /devices/{id}/
alarms?
startTime=...&endTime=..
.&page=...&limit=...
(per-device)
GET /alerts  (listAlerts —
cross-device)
Per-device alarm
listing, or cross-device
queries through
listAlerts.
XAPI listAlerts API supports
cross-device alert queries.
The legacy alarm endpoints
correspond to the older
Aerohive Alarms system, not
Extreme Alerts.
Tip:
If you are already using the
Extreme Alerts system, migrate
directly to the CS Alert API.
GET /v1/monitor/alarms List alarms across
devices (CS alternative).
CS GET /alert/v1/alerts?...
(18 or more filter parameters)
GET /alert/v1/alerts/
stats-by-location
GET /alert/v1/alerts/
stats-by-device
GET /alert/v1/alerts/
{deviceId}/stats
POST /alert/v1/alerts/
reports
CS Alert API provides
comprehensive cross-
device listing, statistics
by location and device,
report generation, and
acknowledgment.
CS Alert API supports rich
filtering and aggregation that
exceeds both legacy and XAPI
capabilities.
Tip:
For cross-device alarm queries,
CS Alert API provides the
most complete replacement for
legacy alarm functionality.
32 Aerohive API Migration Reference Guide


<!-- page 33 -->

Real-Time Client Location Endpoint
Migration
Coverage: partial. XAPI provides client-centric location queries, but the legacy AP-
centric (per AP MAC) streaming model has no direct equivalent.
Table 21: Real-time client location endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/location/clients?
apMacs=...
/v3/location/clients?
apMacs=...
Real-time client
location observations
per AP MAC address,
including latitude and
longitude, x and
y coordinates, RSSI,
manufacturer, OS, and
SSID.
XAPI GET /essentials/eloc/
clients/{clientMac}/
last-known-location?
floorId=...&parentId=...
GET /clients/active?
locationIds=...
(listActiveClients with
location filter)
Last-known location
per client MAC address,
or list active clients
filtered by location.
For location-based client
queries, use the
listActiveClients API with
a location filter. Remaining
gap: legacy returned real-time
RSSI observations grouped by
AP MAC address in an AP-
centric streaming model. XAPI
provides client-centric queries
(per-client last-known location
or per-location active client
list). The per-AP-MAC streaming
model has no equivalent in XAPI
or CS.
Aerohive API Migration Reference Guide 33


<!-- page 34 -->

Bluetooth and BLE Endpoint Migration
Coverage: no replacement. All Bluetooth and BLE endpoints in the legacy Aerohive API
have been discontinued. The Aerohive BLE hardware feature is no longer supported,
and no replacement API exists in XAPI or CS.
Bluetooth Device Configuration
Table 22: Bluetooth device configuration endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
device/{deviceId}/
bluetoothconfig
Get Bluetooth
configuration for a
device including enable
or disable BLE and
iBeacon major, minor,
power, and UUID
settings.
— No replacement No Bluetooth device
configuration API exists
in XAPI or CS.
The Aerohive BLE and
iBeacon feature set has been
discontinued.
Tip:
If your integration uses API-
driven BLE configuration for
asset tracking or wayfinding,
contact your Extreme Networks
account team for information
about alternative solutions.
PUT /v1/configuration/
device/{deviceId}/
bluetoothconfig
Set Bluetooth
configuration for a
device.
— No replacement
GET /v1/configuration/
device/bleenableddevices
List BLE-enabled
devices.
— No replacement
34 Aerohive API Migration Reference Guide


<!-- page 35 -->

Bluetooth Network Policy Configuration
Table 23: Bluetooth network policy configuration endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
networkpolicy/
{policyId}/
bluetoothconfig
Get Bluetooth
configuration template
for a network policy,
including iBeacon
UUID, name, and
monitoring settings.
— No replacement No Bluetooth policy
configuration API exists
in XAPI or CS.
BLE and iBeacon policy
configuration has been
discontinued.
PUT /v1/configuration/
networkpolicy/
{policyId}/
bluetoothconfig
Set Bluetooth
configuration template
for a network policy.
— No replacement
BLE Monitoring Data
Table 24: BLE monitoring data endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/monitor/
blemonitoringdata
Real-time BLE
monitoring data
including beacon
inventory: AP MAC,
BLE MAC, UUID, signal,
location, and device
status.
— No replacement No BLE monitoring
data API exists in XAPI
or CS.
BLE monitoring and asset
tracking has been discontinued.
Tip:
If your integration depends on
BLE monitoring for IoT or asset
tracking, contact your Extreme
Networks account team for
information about alternative
solutions.
Bluetooth and BLE Endpoint Migration Bluetooth Network Policy Configuration
Aerohive API Migration Reference Guide 35


<!-- page 36 -->

Switch Port Configuration and Port
Type Profile Endpoint Migration
Coverage: no replacement. Switch port write operations and port type profile endpoints
have no replacement. These endpoints apply only to Aerohive SR series switches, which
reach End of Support Life on January 5, 2027.
Switch Port Configuration
Table 25: Switch port configuration endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
switch/{deviceId}/
settings
Get switch port settings
including port details,
VLANs, STP, LLDP,
LAG, and transmission
settings.
XAPI
(read-
only)
GET /d360/device/
interfaces?
deviceModel=...
Read-only interface
information per device
model.
Only applies to Aerohive SR
series switches. All SR devices
reach End of Support Life on
January 5, 2027, and are not
supported in Extreme Platform
ONE Networking. XAPI provides
read-only interface information
through D360.
PUT /v1/configuration/
switch/{deviceId}/
settings
Set switch port settings
including VLANs, port
types, LAG, STP, and
speed and duplex
settings.
— No replacement (write) No API is available
to programmatically
configure switch port
settings.
Only applies to Aerohive
SR series switches. All SR
devices reach End of Support
Life by January 5, 2027. No
write replacement is planned
because the hardware platform
is being retired.
36 Aerohive API Migration Reference Guide


<!-- page 37 -->

Port Type Profiles
Table 26: Port type profile endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v1/configuration/
porttypes
List port type profiles
including ID, name,
device series, and port
type.
— No replacement No port type profile API
exists in XAPI or CS.
Port type profiles are managed
through the ExtremeCloud IQ
user interface only.
GET /v1/configuration/
porttypes/{portTypeId}
Get detailed
port type profile
including VLAN, voice
VLAN, authentication
methods, and user
profiles.
— No replacement
Switch Port Configuration and Port Type Profile
Endpoint Migration Port Type Profiles
Aerohive API Migration Reference Guide 37


<!-- page 38 -->

Presence Analytics Endpoint Migration
Coverage: partial. Presence analytics endpoints have no direct API replacement.
Extreme Platform ONE Networking Client Tracking is the recommended successor
capability for foot traffic and engagement analytics.
Table 27: Presence analytics endpoint mapping
Legacy
method
Legacy endpoint Legacy description New
API
New endpoint New description Migration notes
GET /v2/clientlocation/
clientcount
Client count by
location and AP
over time, including
associated, engaged,
new, returning,
passersby, and unique
client counts.
— No direct API replacement Extreme Platform ONE
Networking Client
Tracking is the
successor capability.
Legacy presence analytics
including foot traffic,
engagement metrics, and
time-series breakdowns have
no direct API equivalent.
The underlying Presence
Engine feature is superseded
by Extreme Platform ONE
Networking Client Tracking.
Tip:
If your integration depends
on presence analytics, Client
Tracking provides the successor
capability.
GET /v2/clientlocation/
clientpresence
Distinct client presence
list by time unit
(FiveMinutes, OneHour,
or OneDay).
— See above
GET /v2/clientlocation/
clienttimeseries
Client count time-
series by time unit.
— See above
38 Aerohive API Migration Reference Guide


<!-- page 39 -->

Legacy Endpoint Quick Reference
Use this table as a checklist when migrating your integration. It lists all 53 legacy
Aerohive API endpoints with their replacement status and recommended new
endpoints.
Table 28: All 53 legacy Aerohive API endpoints
Legacy
method
Legacy endpoint Replacement Coverage
POST /v1/configuration/device/inventory/
onboarding
CS: POST /device-lifecycle-mgmt/v1/devices/
onboard/wireless (or /wired); XAPI: POST /
devices/:onboard
Full
GET /v1/monitor/devices XAPI: GET /devices ; CS: GET /asset/v1/devices/
filters
Full
GET /v1/monitor/devices/{deviceId} XAPI: GET /d360/device/metadata  + /stats
+ /interfaces; CS: POST /performance-monitor/v1/
analytics/device-health
Full
GET /v1/monitor/devices/{deviceId}/
clientList
XAPI: POST /d360/client/grid Full
DELETE /v1/configuration/device CS: POST /device-lifecycle-mgmt/v1/devices/:delete ;
XAPI: POST /devices/:delete
Full
PUT /v1/configuration/devices/devicepassword XAPI: PUT /account/viq/default-device-password Full
GET /v1/configuration/apLocationFolders CS: GET /site-location/v1/tree ; XAPI: GET /
locations/tree
Full
GET /v1/configuration/apLocationFolders/
{folderId}
CS: GET /site-location/v1/sites/{id}  or /buildings/
{id} or /floors/{id}
Full
GET /v1/configuration/networkpolicy/policies XAPI: GET /network-policies Full
PUT /v1/configuration/networkpolicy/deploy XAPI: POST /devices/network-policy/:assign Full
POST /v1/configuration/networkpolicy/
{policyId}/devices
XAPI: POST /devices/network-policy/:assign Full
POST /v1/configuration/webhooks CS: POST /notification/v1/webhook ; XAPI: POST /
subscriptions/webhook
Full
GET /v1/configuration/webhooks CS: GET /notification/v1/webhook ; XAPI: GET /
subscriptions/webhook
Full
DELETE /v1/configuration/webhooks/
{subscriptionId}
CS: DELETE /notification/v1/webhook/{id} ; XAPI:
DELETE /subscriptions/webhook/:delete
Full
GET /v1/configuration/ssids XAPI: GET /ssids Full
Aerohive API Migration Reference Guide 39


<!-- page 40 -->

Table 28: All 53 legacy Aerohive API endpoints (continued)
Legacy
method
Legacy endpoint Replacement Coverage
GET /v1/configuration/ssids/{ssidProfileId} XAPI: GET /ssids/advanced-settings/{id} Partial
GET /v1/configuration/devices/{deviceId}/
ssids
XAPI: GET /devices/{id}/ssid/status Partial
PUT /v1/configuration/devices/{deviceId}/
ssids
XAPI: POST /devices/{id}/ssid/:override  + /
status/:change
Partial
GET /v1/configuration/ssids/
{ssidProfileId}/psk
XAPI: No raw PSK read — security improvement Partial
PUT /v1/configuration/ssids/{ssidProfileId} XAPI: PUT /ssids/{id}/psk/password  + /mode/psk + /
mode/ppsk
Full
GET /beta/configuration/ssids/
{ssidProfileId}/filters
XAPI: GET /ssids/advanced-settings/{id} Partial
PUT /beta/configuration/ssids/
{ssidProfileId}/filters
XAPI: PUT /ssids/advanced-settings/{id} Partial
POST /v1/identity/credentials XAPI: POST /endusers Partial
POST /v2/identity/credentials XAPI: POST /endusers Partial
GET /v1/identity/credentials XAPI: GET /endusers Partial
GET /v2/identity/credentials XAPI: GET /endusers Partial
PUT /v1/identity/credentials/{credentialId} XAPI: PUT /endusers/{id} Partial
PUT /v2/identity/credentials/{credentialId} XAPI: PUT /endusers/{id} Partial
DELETE /v1/identity/credentials XAPI: DELETE /endusers/{id} Partial
DELETE /v2/identity/credentials XAPI: DELETE /endusers/{id} Partial
PUT /v1/identity/credentials/{credentialId}/
renew
XAPI: POST /endusers/{id}/:regenerate-password  (not
an exact match)
Partial
POST /v1/identity/credentials/deliver XAPI: POST /usergroups  (createUserGroup — email and
SMS notification at group level)
Partial
POST /v2/identity/credentials/deliver XAPI: POST /usergroups  (createUserGroup — email and
SMS notification at group level)
Partial
GET /v1/identity/userGroups XAPI: GET /usergroups ; CS: IAM API Full
GET /v2/identity/userGroups XAPI: GET /usergroups ; CS: IAM API Full
GET /v1/monitor/clients XAPI: GET /clients/active Full
GET /v1/monitor/clients/{clientId} XAPI: GET /clients/{id}  + /client-details/overview/
info/{id}
Full
GET /v1/monitor/alarms XAPI: GET /alerts  (listAlerts — cross-device); GET /
devices/{id}/alarms (per-device); CS: GET /alert/v1/
alerts
Full
Legacy Endpoint Quick Reference
40 Aerohive API Migration Reference Guide


<!-- page 41 -->

Table 28: All 53 legacy Aerohive API endpoints (continued)
Legacy
method
Legacy endpoint Replacement Coverage
GET /v1/location/clients XAPI: GET /essentials/eloc/clients/{mac}/last-
known-location; GET /clients/active  (with location
filter)
Partial
GET /v3/location/clients XAPI: GET /essentials/eloc/clients/{mac}/last-
known-location; GET /clients/active  (with location
filter)
Partial
GET /v1/configuration/device/{deviceId}/
bluetoothconfig
No replacement None
PUT /v1/configuration/device/{deviceId}/
bluetoothconfig
No replacement None
GET /v1/configuration/device/
bleenableddevices
No replacement None
GET /v1/configuration/networkpolicy/
{policyId}/bluetoothconfig
No replacement None
PUT /v1/configuration/networkpolicy/
{policyId}/bluetoothconfig
No replacement None
GET /v1/monitor/blemonitoringdata No replacement None
GET /v1/configuration/switch/{deviceId}/
settings
XAPI: GET /d360/device/interfaces  (read-only) Partial
PUT /v1/configuration/switch/{deviceId}/
settings
No replacement (write) None
GET /v1/configuration/porttypes No replacement None
GET /v1/configuration/porttypes/{portTypeId} No replacement None
GET /v2/clientlocation/clientcount Extreme Platform ONE Networking Client Tracking
(successor capability)
Partial
GET /v2/clientlocation/clientpresence Extreme Platform ONE Networking Client Tracking
(successor capability)
Partial
GET /v2/clientlocation/clienttimeseries Extreme Platform ONE Networking Client Tracking
(successor capability)
Partial
Legacy Endpoint Quick Reference
Aerohive API Migration Reference Guide 41
