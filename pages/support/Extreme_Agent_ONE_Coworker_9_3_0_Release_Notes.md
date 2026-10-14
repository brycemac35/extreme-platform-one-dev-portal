---
title: 'Extreme Agent ONE Coworker v9.3.0 Release Notes Oct 2026'
source: https://documentation.extremenetworks.com/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.pdf
pages: 9
---

# Extreme Agent ONE Coworker v9.3.0 Release Notes Oct 2026

Source PDF: [Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.pdf](../../pdfs/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.pdf)

<!-- page 1 -->

Extreme Agent ONE™
Coworker v9.3.0
Release Notes
New Features, Limitations, and Known
Issues
9041299-00 Rev. AA
October 2026


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
Abstract.................................................................................................................................................. 4
Help and Support..................................................................................................................................5
Subscribe to Product Announcements.............................................................................................................................................5
General Release Information............................................................................................................. 7
Features and Updates.....................................................................................................................................................................................7
Resolved Issues....................................................................................................................................................................................................7
Known Issues......................................................................................................................................................................................................... 8
Limitations.....................................................................................................................................................................................................8
Related Documentation.................................................................................................................................................................................9
Extreme Agent ONE™ Coworker v9.3.0 iii


<!-- page 4 -->

Abstract
These release notes for Extreme Agent ONE™ Coworker version 9.3.0 describe new features,
resolved issues, known issues, and limitations for the AI assistant that operates within
Extreme Platform ONE™. The default skills are Nudge, Talk to Data, Talk to Knowledge,
and Talk to Support. New features include redesigned exported chat PDFs, citation hover
tooltips, improved copy formatting, better conversational memory, reasoning updates every
4–5 seconds, localized nudges, and Talk to Knowledge preference for Extreme Platform ONE
documentation. The Release Notes also cover Resolved Issues, Known Issues, and Limitations.
Limitations note that Talk to Support incidents create no Extreme Exchange™ audit log and
that change logs omit the originating skill; users must verify tickets in the support portal and
correlate changes by timestamp, user, and action.
4 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 5 -->

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
Extreme Agent ONE™ Coworker v9.3.0 5


<!-- page 6 -->

4. Select Subscribe.
5. To select additional products, return to the Product Announcements list and repeat steps
3 and 4.
You can modify your product selections or unsubscribe at any time.
Subscribe to Product Announcements Help and Support
6 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 7 -->

General Release Information
Features and Updates on page 7
Resolved Issues on page 7
Known Issues on page 8
Related Documentation on page 9
Features and Updates
Release 9.3.0 features the following updates:
• PDF downloads—Overhauled exported chat PDFs to improve the usability of downloaded
PDFs. The new format provides visualizations that make it easier to distinguish admin
messages from those of Extreme Agent ONE™ Coworker.
• User Interface updates—Enhanced the user interface by adding tooltips for chat icons,
hover tooltips that display the citation when you hover your cursor over a link, and
consolidated links when there are multiple links that go to the same source.
• Copy Improvements—Improved text formatting output when you copy text from an
existing chat and paste in a text editor.
• Conversational memory enhancements—Memory improvements ensure that Extreme
Agent ONE Coworker retains the context of existing conversations. In addition, reasoning
improvements ensure that Extreme Agent ONE Coworker provides reasoning updates every
4–5 seconds while preparing a response.
• Localization—Localization improvements ensure that nudges appear in the admin's
preferred language.
• Talk to Knowledge improvements—To ensure that Extreme Platform ONE documentation
is emphasized over legacy documentation.
Resolved Issues
Issue Description
DT4N-8825 Resolved issue with troubleshooting flow where Extreme Agent ONE Coworker
suggested next steps but did not indicate who should complete those steps: the
user or Extreme Agent ONE Coworker.
DT4N-8826 Resolved issue with troubleshooting flow where Extreme Agent ONE Coworker did
not return data for a query and did not provide a clear message of the reason.
Updated messaging to provide more information on the reason that no data was
returned (for example, an incorrect identifier).
Extreme Agent ONE™ Coworker v9.3.0 7


<!-- page 8 -->

Issue Description
DT4N-8695 Resolved issue where option to upload attachments such as logs or other files
was given to the user after generating an evidence though case creation was not
requested yet.
DT4N-9064 Resolved issue where no option to upload attachments such as logs or other files
was given after user has generated a an evidence report.
DT4N-9314 Addressed issue where the timestamps of charts generated by Extreme Agent
ONE Coworker reponses did not match the system time of Extreme Platform ONE™
Networking.
DT4N-9624 Addressed issue where the widget action buttons remain disabled after another
interaction with a widget is completed.
DT4N-9699 Addressed issue where the Intro Nudge language was not updating after changing
the preferred language.
DT4N-9729 Resolved issue with troubleshooting flow where Extreme Agent ONE Coworker
stops helping when you switch context by asking for clarifications on existing
information or recommendations based on information provided. The update gives
you more control over the troubleshooting flow.
DT4N-9738 Resolved issue that occurred when you asked Extreme Agent ONE Coworker about
a device or client, but provided an incorrect identifier (for example, an incorrect
MAC address). In this situation, Extreme Agent ONE Coworker tried to answer your
question instead of first asking you to clarify the specific device or client.
Known Issues
Issue Description
CFD-18480 An issue exists where case descriptions that the Talk to Support skill generates
use inconsistent formatting.
CFD-18478 An issue exists where Extreme Agent ONE does not distinguish between public
and internal only cases. If an admin requests a list of open cases, Extreme Agent
ONE Coworker may return all open cases.
DT4N-9629 An issue has been observed with wired client metrics where data returned by
Extreme Agent ONE may differ from that of Extreme Platform ONE.
Limitations
Talk to Support Incidents Not Reflected in Chat Logs
Incident creation through the Talk to Support skill succeeds in the support system but does
not currently create a dedicated audit log in Extreme Exchange™. Capture the ticket number
returned in the conversation and verify it directly in the support portal or ticketing system. For
this release, do not use Chat Logs as the sole evidence of incident creation.
Change Logs Do Not Identify the Originating Skill
Configuration changes executed through Extreme Agent ONE Coworker are logged in Extreme
Exchange, but the logs do not explicitly show the exact originating skill name. For now,
correlate activities using timestamp, user, object changed, and action detail. If stricter
Known Issues General Release Information
8 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 9 -->

traceability is needed, maintain supplemental operational notes for high-impact changes
performed through Extreme Agent ONE Coworker.
Related Documentation
The following documentation is available for Extreme Agent ONE™ Coworker:
• Extreme Agent ONE Coworker User Guide
The following documentation is available for Extreme Exchange™:
• Extreme Exchange User Guide
General Release Information Related Documentation
Extreme Agent ONE™ Coworker v9.3.0 9
