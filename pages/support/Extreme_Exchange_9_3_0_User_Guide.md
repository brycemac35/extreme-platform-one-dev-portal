---
title: 'Extreme Exchange v9.3.0 User Guide Oct 2026'
source: https://documentation.extremenetworks.com/Extreme_Exchange_9_3_0_User_Guide.pdf
pages: 17
---

# Extreme Exchange v9.3.0 User Guide Oct 2026

Source PDF: [Extreme_Exchange_9_3_0_User_Guide.pdf](../../pdfs/Extreme_Exchange_9_3_0_User_Guide.pdf)

<!-- page 1 -->

Extreme Exchange™
v9.3.0
User Guide
Monitor, Manage, and Engage with Extreme
Agent ONE™ Skills
9041300-00 Rev. AA
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
Abstract...............................................................................................................................................................................................................................iv
Preface.....................................................................................................................................................5
Text Conventions................................................................................................................................................................................................5
Documentation and Training..................................................................................................................................................................... 6
Open Source Declarations................................................................................................................................................................7
Training.............................................................................................................................................................................................................7
Help and Support............................................................................................................................................................................................... 7
Subscribe to Product Announcements.................................................................................................................................. 8
Extreme Support Portal.......................................................................................................................................................................8
Send Feedback.................................................................................................................................................................................................. 10
Extreme Exchange™ Overview.........................................................................................................11
The User Interface..............................................................................................................................................................................................11
Launch Extreme Exchange.........................................................................................................................................................................13
Extreme Exchange Site Options..................................................................................................... 14
Home..........................................................................................................................................................................................................................14
Catalog......................................................................................................................................................................................................................14
Dashboard..............................................................................................................................................................................................................15
View Audit Logs.......................................................................................................................................................................................15
Enter Custom Date Range...............................................................................................................................................................16
Community............................................................................................................................................................................................................16
Launch Documentation..................................................................................................................................................................... 17
Extreme Exchange™ v9.3.0 iii


<!-- page 4 -->

Abstract
The Extreme Exchange™ User Guide documents the management and monitoring platform for
Extreme Agent ONE™ AI deployment. Extreme Exchange gives administrators a single interface
to monitor Extreme Agent ONE performance and usage—including which skills are being used
and the assistant's success rate—and to review change requests through an audit log for
troubleshooting and governance. The guide describes the user interface and its common
action icons, and explains how to launch Extreme Exchange from the Extreme Agent ONE
Command Bar within Extreme Platform ONE™ Networking. It then walks through the four site
sections: Home, Catalog, Dashboard, and Community—a set of videos, demos, articles, and
FAQs. It also covers procedures for viewing audit logs, entering custom date ranges, and
launching the latest documentation. The intended audience is Admin and NetSecOps users
managing an Extreme Agent ONE deployment.
iv Extreme Exchange™ v9.3.0


<!-- page 5 -->

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
Extreme Exchange™ v9.3.0 5


<!-- page 6 -->

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
Documentation and Training Preface
6 Extreme Exchange™ v9.3.0


<!-- page 7 -->

Hardware and Software Compatibility for Extreme Networks products
Extreme Optics Compatibility
Other Resources such as articles, white papers, and case studies
Open Source Declarations
Some software files have been licensed under certain open source licenses. Information is
available on the Open Source Declaration page.
Training
Extreme Networks offers product training courses, both online and in person, as well as
specialized certifications. For details, visit the Extreme Networks Training page.
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
Preface Open Source Declarations
Extreme Exchange™ v9.3.0 7


<!-- page 8 -->

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
Learning about Extreme Support Portal accounts.
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
Create an End Customer Extreme Support Portal Account
How to create an End Customer Extreme Portal account.
The Extreme Support Portal provides separate registration forms for End Customers and
Partners. Use this task to create an End Customer account.
Note
If you are adding a new user to an existing account, the new user must complete and
be vetted through the same registration process.
The portal registration page is at https://extreme-networks.my.site.com/.
1. Go to the Extreme Support Portal and select Login or Signup on the login page.
2. On the login page, select Create a new Extreme Customer Portal Account .
Subscribe to Product Announcements Preface
8 Extreme Exchange™ v9.3.0


<!-- page 9 -->

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
How to create a Partner Extreme Portal account.
The Extreme Support Portal provides separate registration forms for End Customers and
Partners. Use this task to create a Partner account.
The portal registration page is at https://extreme-networks.my.site.com/.
1. Go to the Extreme Support Portal and select Login or Signup on the login page.
2. On the login page, select Create a new Extreme Partner Portal Account.
3. Complete all required fields (marked *). Use your corporate email address to ensure the
appropriate access level.
Important
Do not register with a personal email address.
4. Read the following terms and select the required check boxes:
• Support Portal Terms of Use
• Extreme Networks Standard Reseller Terms and Conditions
• Trade Compliance Terms and Conditions
You can adjust or withdraw consent at any time through the Email Preference Center.
5. Select Register.
A confirmation message appears on the page and a password setup email is sent to your
corporate email address.
Preface Extreme Support Portal
Extreme Exchange™ v9.3.0 9


<!-- page 10 -->

6. Open the password setup email and follow the instructions to create your portal password.
Tip
If the email does not appear in your inbox within a few minutes, check your spam
or junk mail folder.
7. To log in to the support portal go to: https://extremesaas.my.site.com/.
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
Send Feedback Preface
10 Extreme Exchange™ v9.3.0


<!-- page 11 -->

Extreme Exchange™ Overview
The User Interface on page 11
Launch Extreme Exchange on page 13
Extreme Exchange™ provides a platform for managing your Extreme Agent ONE™ Coworker
deployment. You can use the features within Extreme Exchange to monitor the performance
and usage of Extreme Agent ONE Coworker, including which skills are being used, and
the success rate. You can also use the Audit Logs feature to review change requests for
troubleshooting purposes.
The User Interface
Extreme Exchange offers a simple, easy-to-use user interface with clear navigation and
access to all your AI needs.
Extreme Exchange™ v9.3.0 11


<!-- page 12 -->

Figure 1: The Extreme Exchange User Interface
Table 4: The Extreme Exchange User Interface
Callout Description
1 Navigation menu—Select the appropriate tab from the navigation menu to navigate
to different content pages within Extreme Exchange. The currently selected page is
highlighted.
The following navigation items are available:
• Home
• Catalog
• Dashboard
• Community
2 User Settings menu—Select this icon to access the user settings menu where you can
access options such as Sign Out.
3 Content window—The displayed contents depend on which tab you've selected.
Extreme Exchange uses a set of icons to initiate common user actions.
Table 5: Common Icons on Extreme Exchange
Icon Description
Widget Description—Hover your cursor over this icon for a text description of the widget
or scorecard.
Custom Dates—Select this icon to enter a custom date range. The widget or listing that
is associated with the date range displays information and records that fit within the
selected range.
Search—You can enter text in the Search box to search for a specific entry, such as a
specific audit log record.
The User Interface Extreme Exchange™ Overview
12 Extreme Exchange™ v9.3.0


<!-- page 13 -->

Table 5: Common Icons on Extreme Exchange (continued)
Icon Description
Refresh—Select this icon to refresh the current view.
 or
 Like—Select these icons to enter or remove a Like feedback response for the adjoining
site, video, or article. The following rules apply:
• The
  icon displays when you have not entered feedback for that site, video, or
article. Select this icon to enter your Like feedback.
• The
  icon displays if you have entered a Like response. Subsequently selecting this
icon removes your feedback.
• The adjacent number, irrespective of which icon displays, indicates the total number of
Likes received for that site, video, or article.
Launch—Select this icon to launch the referenced site or document.
Go to—Select the icon to go to the location specified by the adjacent text label.
Drill-down—Select this icon to drill down into the designated article or FAQ.
Launch Extreme Exchange
Use this task to launch Extreme Exchange.
1. Log in to Extreme Platform ONE™ Networking.
2. From the Extreme Agent ONE Command Bar, select the
  options menu.
3. Select
  (Manage Skills in Exchange).
Note
You can also launch Extreme Exchange from Extreme Platform ONE Networking by
selecting one of the following shortcut keys:
• <Command+E> from Mac.
• <Ctrl+E> from Windows.
Extreme Exchange™ Overview Launch Extreme Exchange
Extreme Exchange™ v9.3.0 13


<!-- page 14 -->

Extreme Exchange Site Options
Home on page 14
Catalog on page 14
Dashboard on page 15
Community on page 16
Home
By default, Extreme Exchange opens at the Home page, which can also be opened by
selecting the Home tab from the navigation menu. The home page has announcements and
lists the skills that are currently activated for Extreme Agent ONE Coworker.
Catalog
Select the Catalog tab to open a page that contains a directory of the skills that you can use
with Extreme Agent ONE Coworker. You can select each skill to obtain more information about
the skill. With this release, Extreme Agent ONE Coworker includes the following skills:
• Nudge—Nudge brings the information you need directly to you. It delivers proactive alerts
for high-severity issues so you can respond quickly and provides intelligent nudges that
help you discover features and work more efficiently. Instead of monitoring dashboards or
digging through menus, let the agent discover critical updates and helpful insights exactly
when you need them.
• Talk to Data—Talk to Data puts a conversational interface between you and your
onboarded networking devices, giving you the power to query live device data and explore
historical performance trends effortlessly. No more digging through dashboards or writing
complex queries—just ask a question in plain language and get the insights you need to
make informed decisions.
• Talk to Knowledge—Talk to Knowledge is an AI-powered agent that gives you answers
by searching Extreme Networks customer documentation, articles, and resolved support
cases. Instead of manually digging through manuals or sifting through past cases, simply
ask a question in plain language to access the information that you need.
• Talk to Support—Talk to Support provides 24–7 AI-powered support capability designed
to accelerate issue resolution and improve support efficiency. It automates evidence
collection and streamlines case creation, reducing manual effort while improving
data quality for faster troubleshooting. Built with Human-in-the-Loop (HITL) controls,
role-based access, and flexible trigger mechanisms, it delivers greater visibility, governance,
and confidence across the support lifecycle.
14 Extreme Exchange™ v9.3.0


<!-- page 15 -->

The following skills display on the Catalog page, but are not yet generally available:
• Canvas (Coming Soon)—Canvas gives you a fully customizable page to build the exact
network monitoring dashboard you need. Add widgets like tables, charts, and graphs, then
arrange them to fit your workflow and priorities. Whether you are tracking device health,
performance trends, or key metrics, Canvas puts the data that matters most front and
center. Stop adapting to rigid dashboards and start building your own.
• Radio Resource Management (Coming Soon)—The Radio Resource Management skill
is an intelligent system that, when configured, constantly analyzes Wi-Fi conditions
(interference, load, client behavior) and automatically adjusts radio settings including
channel, power, and bandwidth. This continuous optimization improves throughput,
reliability, and user experience while reducing the need for manual Radio Frequency (RF)
tuning by engineers.
Dashboard
Select the Dashboard tab to open a page where you can view widgets, charts, and scorecards
with performance data for Extreme Agent ONE Coworker. This page contains two subtabs:
• KPIs—Select this tab to view scorecards, charts, and widgets that illustrate AI adoption
in your workplace. You can use these elements to determine which Extreme Agent ONE
Coworker skills are being used the most, the success rate, the number of informational and
critical nudges, and the number of support cases created.
• Audit Logs—Select this tab to view audit logs that record change requests from an Extreme
Agent ONE Coworker chat. Only chats that resulted in a change request are logged.
View Audit Logs
The Audit Logs tab contains audit logs for every change request that results from an Extreme
Agent ONE Coworker chat. Only chats that result in a change request are logged. Refer to Table
6 for field descriptions for the displayed fields.
Note
Audit logs can be viewed only by users with the Admin or NetSecOps roles with the
following access rights:
• Admin users—Have read-only access to audit logs for all users under the tenant.
• NetSecOps users—Have read-only access to audit logs only for their own chats.
Table 6: Audit Log Field Descriptions
Field Description
Last 24 Hours
Last 30 Days
Last 90 Days
Custom Dates
Select one of these buttons to set the date range from which Extreme
Exchange pulls audit log records for display. Last 24 Hours is selected by
default.
You can select Last 30 Days or Last 90 Days buttons to reset the date
range to either of those values or you can select Custom Dates and select a
customized date range.
Timestamp The date and time of the change that created the audit log record.
Extreme Exchange Site Options Dashboard
Extreme Exchange™ v9.3.0 15


<!-- page 16 -->

Table 6: Audit Log Field Descriptions (continued)
Field Description
Chat Title The name of the chat from which the change originated.
User The user who initiated the change. Note that all changes that arose from an
Extreme Agent ONE Coworker conversation are logged under the user rather
than under Extreme Agent ONE Coworker.
Role The role of the user.
Skills Used The Extreme Agent ONE Coworker skills that were used in the chat that
resulted in the change.
Message Count The number of messages in the chat that resulted in the change.
Change Requests Made The number of change requests made from the chat.
To view specific audit logs, do the following:
1. In Extreme Exchange, select Dashboard.
2. Select Audit Logs.
3. Select the date range from which you want to pull logs.
• Last 24 Hours (the default setting)
• Last 30 Days
• Last 90 Days
• Custom Dates—Select this option to enter a customized date range.
4. Select the audit log record that you want to view.
Enter Custom Date Range
Use this procedure to enter a customized date range. You may want to do this to view widgets
that use data from the range that you specify or to view a listing of audit logs for the dates
that you want.
1. In Extreme Exchange, select Dashboard.
2. Go to one of the following subtabs.
• Select KPIs if you want the customized range to be applied to dashboard data.
• Select Audit Logs if you want the customized range to be applied to the listing of
available audit logs.
3. Select the Custom Dates icon.
4. From the calendar view, select the Start Date.
5. From the calendar view, select the End Date.
6. Select Done.
Community
Use the Community tab to access resources for developers and consumers who are
implementing AI solutions. You can view videos and demos that have been uploaded to
Extreme Exchange, read helpful articles, resources, and FAQs about how to use Extreme
Exchange and Extreme Agent ONE Coworker.
Enter Custom Date Range Extreme Exchange Site Options
16 Extreme Exchange™ v9.3.0


<!-- page 17 -->

Select a specific video, article, or FAQ to access that content. If you find the information to be
helpful, select
  (Like) to provide positive feedback for the item. Your feedback will help to
determine what to include in the future.
To filter the list of materials that displays, select from the following categories: GETTING
STARTED, AGENT ONE, SKILLS, EXCHANGE, and WALKTHROUGH. You can select more than
one category.
To sort the list of returned items, select either Most Recent (the default) or Most Liked.
Launch Documentation
Use this procedure to go to the latest documentation for Extreme Exchange:
1. From Extreme Exchange, select the Community tab.
2. Scroll down to the Documentation section.
3. Select the
  icon that is adjacent to the documentation page that you want to view.
Extreme Exchange Site Options Launch Documentation
Extreme Exchange™ v9.3.0 17
