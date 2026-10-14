---
title: 'Extreme Agent ONE Coworker v9.3.0 User Guide Oct 2026'
source: https://documentation.extremenetworks.com/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.pdf
pages: 29
---

# Extreme Agent ONE Coworker v9.3.0 User Guide Oct 2026

Source PDF: [Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.pdf](../../pdfs/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.pdf)

<!-- page 1 -->

Extreme Agent ONE™
Coworker v9.3.0
User Guide
AI Agent Usage Instructions
9041301-00 Rev. AA
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
Extreme Agent ONE™ Coworker Overview................................................................................... 11
Extreme Agent ONE Coworker Skills...................................................................................................................................................12
Nudge..............................................................................................................................................................................................................12
Talk to Data................................................................................................................................................................................................. 14
Talk to Knowledge.................................................................................................................................................................................. 14
Talk to Support.........................................................................................................................................................................................15
Chats.......................................................................................................................................................................................................................... 17
Archived Canvas................................................................................................................................................................................................17
Best Practices for Communicating with Extreme Agent ONE Coworker................................................................17
Restrictions and Controls...........................................................................................................................................................................18
Requirements.......................................................................................................................................................................................................19
Set Preferred Language................................................................................................................................................................................19
Using Extreme Agent ONE Coworker............................................................................................20
The User Interface..........................................................................................................................................................................................20
Getting Started with Extreme Agent ONE Coworker........................................................................................................... 25
Start a New Chat..............................................................................................................................................................................................25
Open Existing Chat........................................................................................................................................................................................ 26
View Chat History........................................................................................................................................................................................... 26
Snooze Informational Nudges.................................................................................................................................................................27
Respond to Nudge.......................................................................................................................................................................................... 27
Open Archived Canvas................................................................................................................................................................................28
Download Chat..................................................................................................................................................................................................28
Copy Chat.............................................................................................................................................................................................................28
Submit Feedback............................................................................................................................................................................................ 29
Launch Extreme Exchange.......................................................................................................................................................................29
Extreme Agent ONE™ Coworker v9.3.0 iii


<!-- page 4 -->

Abstract
The Extreme Agent ONE™ Coworker User Guide documents Extreme Networks' embedded
AI assistant for the Extreme Platform ONE™ environment. Extreme Agent ONE Coworker is a
conversational, natural-language helper that monitors a user's network from login, surfaces
critical issues, provides contextual guidance, retrieves and analyzes telemetry, pulls relevant
documentation, and assists with support-case creation and tracking. It operates through four
default, always-on skills: Nudge (proactive informational and critical Sev 1 alerts), Talk to Data
(read-only retrieval and analysis of wired/wireless network data), Talk to Knowledge (answers
grounded in Extreme product documentation, GTAC articles, and CVE/security advisories),
and Talk to Support (troubleshooting, automated evidence collection, and GTAC case creation
with Human-in-the-Loop authorization). The guide emphasizes that the assistant takes no
autonomous action, never executes changes without explicit user approval, enforces role-
based data access, and grounds responses in Extreme sources to reduce hallucination. It
covers the user interface (launch page, Command Bar, Command Center, and Chat Window),
requirements (Admin or NetSecOps role and an Extreme Platform ONE Networking or Security
subscription), and step-by-step procedures for starting and managing chats, responding
to nudges, snoozing notifications, downloading or copying chats, submitting feedback, and
launching Extreme Exchange. The intended audience is network administrators and security
operations staff using Extreme Platform ONE.
iv Extreme Agent ONE™ Coworker v9.3.0


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
Extreme Agent ONE™ Coworker v9.3.0 5


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
6 Extreme Agent ONE™ Coworker v9.3.0


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
Extreme Agent ONE™ Coworker v9.3.0 7


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
Subscribe to Product Announcements Preface
8 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 9 -->

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
Extreme Agent ONE™ Coworker v9.3.0 9


<!-- page 10 -->

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
10 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 11 -->

Extreme Agent ONE™ Coworker Overview
Extreme Agent ONE Coworker Skills on page 12
Chats on page 17
Archived Canvas on page 17
Best Practices for Communicating with Extreme Agent ONE Coworker on page 17
Restrictions and Controls on page 18
Requirements on page 19
Set Preferred Language on page 19
Extreme Agent ONE™ Coworker can make it easy to manage your network. Extreme Agent ONE
Coworker is a virtual AI helper that is there to assist while you are working in Extreme Platform
ONE™ Networking.
Extreme Agent ONE Coworker calls your attention to critical items that need to be addressed,
provides guidance when you're unsure of next steps, retrieves relevant information and data,
and helps you create and manage support cases when they're needed.
Extreme Agent ONE Coworker can reduce the amount of time that you spend searching for
information and the amount of time that it takes you to resolve issues. As soon as you log in
to Extreme Platform ONE Networking, Extreme Agent ONE Coworker is on and is monitoring no
matter where you are in Extreme Platform ONE Networking.
Extreme Agent ONE Coworker helps you by doing the following:
• Alerts you to critical issues that need to be addressed right away.
• Provides guidance when you are unsure of your next action.
• Nudges you to features and capabilities that you might not be aware of.
• Extracts and analyzes relevant telemetry information from your network.
• Pulls documentation that is relevant to your task.
• Helps you troubleshoot and address network issues.
• Helps you manage and track support cases: Case creation, analysis, detailed investigation,
and suggested solutions. It can also isolate priority support cases for easier access and
management.
You can use Extreme Agent ONE Coworker with ordinary human language. You simply type
in your questions, commands, and text prompts in regular language and Extreme Agent ONE
Coworker provides a response that always includes a written summary and may also include
telemetry data, tables, visualizations, procedures, and perhaps its own questions to you.
Extreme Agent ONE™ Coworker v9.3.0 11


<!-- page 12 -->

Extreme Agent ONE Coworker has the persona of a knowledgeable and helpful team member
who respects your authority and never initiates changes without your approval.
To help build confidence with its abilities, Extreme Agent ONE Coworker doesn’t just provide
you with suggested actions—it also includes reasoning for its decisions and analysis. If it
doesn’t know the answer, it tells you, and then provides possible alternatives. Also, if an
investigation is going to take time to reach a decision, Extreme Agent ONE Coworker tells you
so that you know a response is in progress.
Note
Extreme Agent ONE Coworker responses are generated by artificial intelligence and
are designed to reduce the risk of hallucination by grounding answers in Extreme
documentation, GTAC knowledge articles, and release notes. However, like any AI, it
can make mistakes, and you should check important information.
Extreme Agent ONE Coworker Skills
As an AI helper, Extreme Agent ONE Coworker offers skills that accomplish specific tasks. It
comes with four default skills that it can access for various tasks:
• Nudge
• Talk to Data
• Talk to Knowledge
• Talk to Support
No configuration or setup is necessary to use these four skills as they are on automatically and
configured by default. There is also no need to specify which skill to use—Extreme Agent ONE
Coworker analyzes your prompt, determines which skill(s) will help it to complete the task, and
automatically invokes the skill.
Nudge
Note
Nudges are supported in Extreme Platform ONE Networking only. Nudges are not
supported in Extreme Platform ONE™ Security.
The Nudge skill is a proactive helper that tells you what to do next or calls attention to items
of importance to you. This skill gives Extreme Agent ONE Coworker the ability to prompt you
whenever it sees something on the network that needs your attention.
When Extreme Agent ONE Coworker prompts you, the Command Bar pulses gently and a text
bubble displays with a brief message about the issue. Select the text bubble to launch the
nudge in a full chat window where you can read a full analysis of the issue and ask follow-up
questions.
There are three types of nudges:
• Informational Nudges
• Critical Nudges
Extreme Agent ONE Coworker Skills Extreme Agent ONE™ Coworker Overview
12 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 13 -->

• Unread Response Nudges
Note
Critical nudges have the highest priority with unread response nudges having second
priority and informational nudges having the lowest priority. For example, if an admin
is viewing an informational nudge and a critical nudge gets triggered, the critical
nudge displays due to the higher priority ranking.
Informational Nudges
An informational nudge offers helpful information such as a tip or suggestion. Extreme Agent
ONE Coworker bases the nudge on the context of where you are on the Extreme Platform
ONE Networking site, what Extreme Agent ONE Coworker determines that you are trying to
accomplish, your roles and permissions, and as much context that can be gathered about you
and your network. In the Command Bar, informational nudges display alongside a blue dot (
 ).
Extreme Agent ONE Coworker uses informational nudges to call attention to Extreme Platform
ONE Networking features and capabilities that you may not know about, but which are well-
suited to what you’re doing, as well as tasks that are well-suited to where you are on the
site. Informational nudges help you navigate the network and offer suggestions to non-critical
issues when you appear to be unsure of next steps. The messages auto-dismiss within 20
seconds. You also have the option to snooze informational nudges for up to one hour.
Critical Nudge
A critical nudge is a high-priority prompt that Extreme Agent ONE Coworker provides to call
your attention to critical network issues that require your immediate attention. The nudge
gets sent whenever a Sev 1 alert arrives in the Extreme Platform ONE Networking Notification
Center. In the Command Bar, critical nudges display alongside a red dot (
 ).
Critical nudges can help improve acknowledgment time and resolution for critical network
issues. Critical nudges contain a preliminary analysis that helps to begin the troubleshooting
process. Once Extreme Agent ONE Coworker realizes that there is an issue, it completes a
preliminary analysis by analyzing what went wrong, which network elements and devices are
affected, what are the likely causes, and what are the likely fixes.
Selecting the nudge opens a new chat with the results of the analysis. You can issue an
acknowledgement, open a support case, or ask follow-up questions to investigate the issue
further.
Critical nudges do not auto-dismiss. They persist until you engage with them or snooze them.
You have the option to ask Extreme Agent ONE Coworker in chat to snooze critical nudges for
up to four hours.
Unread Response Nudge
A third type of nudge occurs due to an existing chat where Extreme Agent ONE Coworker
requires extra time to provide an answer. Extreme Agent ONE Coworker informs you that it
will nudge you when the response is ready. When it's ready, Extreme Agent ONE Coworker
sends a nudge so that you can reopen the chat and read the response. Unread response
nudges auto-dismiss after five minutes. In the Command Bar, unread response nudges display
alongside a gray dot (
 ).
Extreme Agent ONE™ Coworker Overview Nudge
Extreme Agent ONE™ Coworker v9.3.0 13


<!-- page 14 -->

Talk to Data
The Talk to Data skill provides you with relevant network data simply by asking for it using an
ordinary human language request. Once you make your request, Extreme Agent ONE Coworker
checks the available network data, and responds with whatever data you're asking for. For
example, you could ask about a specific access point (AP) or network switch and Extreme
Agent ONE Coworker responds with the relevant data. The response will typically include a
written summary along with any data tables and graphs that help to convey the information.
What kinds of questions it can answer
• Fact lookup—"What's the firmware version on AP site-3-floor-2?"
• Correlation—"Which sites have the highest error rates and which APs are in those sites?"
• Trend analysis—"Show me CPU utilization across my core switches over the last 30 days."
• Root cause analysis—"Why has client throughput at Site 14 degraded over the past week?"
• Comparisons—"Compare packet loss between Site 3 and Site 7 for the same time period
last month."
How responses are structured
Every Talk to Data response includes a natural-language summary of the answer. Depending
on the data requested, the response may include data tables (with up to 10 rows with
pagination) and widget visualizations. You can download the full result set as a CSV.
What it can't do
Talk to Data is a read-only skill that retrieves and analyzes data only. The skill does not change
network configuration, push firmware, or modify any device settings. It only accesses the data
that your role has permission to see—access controls are enforced at the data retrieval layer.
Talk to Data covers wireless and wired data in this release. Extreme Platform ONE Security
data is out of scope for the current release.
Suggested prompts to try
• "How many clients are connected right now, broken down by site?"
• "Which APs have the highest error rate in the last 24 hours?"
• "Show me devices with firmware older than the current recommended version."
• "What's the average client count per AP at Site 14 over the last 30 days?"
• "Find APs with CPU utilization above 80%."
• "Compare device health scores between my Boston and Dallas sites."
Talk to Knowledge
The Talk to Knowledge skill lets you ask technical networking questions using ordinary human
language and Extreme Agent ONE Coworker pulls the relevant information from the Extreme
Networks product documentation, support articles, and case studies.
Talk to Data Extreme Agent ONE™ Coworker Overview
14 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 15 -->

What it can answer:
• Product documentation questions—Supported firmware versions, hardware specs, new
feature explanations, and how to task procedures.
• Best practices—VLAN configuration, high-density Wi-Fi deployment, policy setup
• GTAC knowledge base—Factual Q&As, security advisories, field notices, best practices —
the non-troubleshooting content
• CVE and security advisory information relevant to your product portfolio
• Questions about Extreme Agent ONE Coworker and Extreme Exchange
What an answer looks like
Answers are summarized in natural language with citations and source references. If Talk to
Knowledge can't find an answer with sufficient confidence, it says so—it will tell you it can't find
it and suggest rephrasing with a specific product name or version.
Suggested prompts to try
• "What are the known CVEs affecting my current firmware versions?"
• "What's the best practice for configuring VLANs on EXOS switches?"
• "What is the health score in Extreme Platform ONE?"
• "How do I set up RADIUS authentication on my switches?"
Talk to Support
Talk to Support is the skill that helps you handle support-related tasks within Extreme Agent
ONE Coworker. This includes troubleshooting issues prior to escalation as well as opening and
tracking GTAC cases.
When a critical nudge fires and you engage with it, the nudge includes the [Troubleshoot] and
[Open a Case] Call-to-Action commands. Clicking either command brings Talk to Support into
the conversation with the pre-investigation context already loaded—the devices, the metrics,
the preliminary findings.
Talk to Support can also be invoked by asking Extreme Agent ONE Coworker to investigate an
issue.
What Talk to Support does:
• Self-resolution help desk (24-7)—When you describe a problem, Extreme Agent ONE
Coworker routes the intent to Talk to Support, which searches the GTAC knowledge base
and product documentation to narrow the issue to likely root causes and walk you through
resolution steps.
• Automated evidence collection—Before a case is submitted to GTAC, Talk to Support
compiles everything from the conversation—reported symptoms, troubleshooting steps,
diagnostic observations—into a structured evidence package automatically.
Extreme Agent ONE™ Coworker Overview Talk to Support
Extreme Agent ONE™ Coworker v9.3.0 15


<!-- page 16 -->

• GTAC case creation—When self-resolution doesn't work, Talk to Support creates a pre-
filled GTAC case formatted to best-practice standards. It shows you a preview and requires
your explicit confirmation before submitting.
• Case status—Ask "What's the status of case 12345?" and Talk to Support retrieves it from
Salesforce in real time. Admin users can see all cases for their tenant; other users see their
own cases.
Troubleshooting
Troubleshooting capabilities let Extreme Agent ONE Coworker diagnose problems,
troubleshoot your network, and provide remediation. For example, you could ask Extreme
Agent ONE Coworker to analyze CPU and memory utilization, whether a device has sufficient
power and cooling, or the effects of any recent configuration changes. Extreme Agent ONE
Coworker provides you with a diagnosis, a suggested fix, and then asks whether you want
to apply that fix. The remediation option is included for wireless networks only—with wired
networks, Extreme Agent ONE Coworker diagnoses, but does not apply any fix.
Note
Remediation includes a Human-in-the-Loop (HITL) requirement. Extreme Agent ONE
Coworker does not apply any fix unless you first authorize the fix. Also note that
remediation is limited to problems that are within the ability of Extreme Agent ONE
Coworker to fix. For example, if the resolution requires physical hardware to be
changed, a trained technician may be required.
Open a Case
If the issue cannot be quickly resolved, ask Extreme Agent ONE Coworker to open a support
case. Extreme Agent ONE Coworker creates a pre-filled GTAC case that includes everything
from the conversation—reported symptoms, troubleshooting steps, diagnostic observations—
in a structured evidence package that is formatted to best-practice standards. It shows you a
preview and requires your explicit confirmation before submitting.
Note the following requirements for opening a case:
• To create or view cases, your account needs a Salesforce (SFDC) portal account. If you
don't have one, Talk to Support tells you how to get one.
• Talk to Support depends on your device entitlements. If your device is covered under
ExtremeWorks or ExtremeWorks Premier, the case proceeds. If it's under a co-delivery
partner agreement, Talk to Support tells you to contact your partner instead.
Suggested prompts to try
• "My APs keep dropping clients—help me figure out what's happening."
• "Open a support case for the Building 3 uplink issue."
• "What's the status of my open support cases?"
• "I'm seeing intermittent packet loss on VLAN 20—help me collect what I need to file a
case."
Talk to Support Extreme Agent ONE™ Coworker Overview
16 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 17 -->

Chats
Interactions with Extreme Agent ONE Coworker take place in conversations called chats. You
can use everyday human language to communicate back and forth by making requests, asking
questions, and reading the Extreme Agent ONE Coworker responses. You use chats when
answering nudges, requesting data, and managing support cases.
Chats take place in a chat window, which can be launched from the Command Bar or
Command Center. A chat can have multiple prompts and responses before you get the
desired result. Each individual chat has its own contextual background and each question
and response within the chat adds to that contextual foundation. As a result, when you ask
follow-up questions within the chat, there is no need to repeat background information that
was established in earlier prompts and responses because Extreme Agent ONE Coworker
already knows all the preceding context from that chat.
Note
The chat prompts and responses are only saved within a single chat. After you open a
new chat, the previous chat context is not saved.
Archived Canvas
All existing canvases and widgets are archived and available using the Command Center. In
addition, you can create new widgets using the chat.
Extreme Agent ONE Coworker does not currently support the ability to create new canvases
or to add new widgets to a canvas. This functionality will be provided in a future release.
Best Practices for Communicating with Extreme Agent ONE Coworker
Chat with Extreme Agent ONE Coworker as if you were chatting with a colleague and
requesting information. To get the most accurate and useful information, use the following
communication best practices:
Be Specific
Provide as much detail as possible in your questions. For example, instead of asking "How do
I configure a device?" ask "How do I configure VLAN settings on an Extreme Networks 5420
Series switch?"
Specify the name of the product: management application, software, or hardware model. If you
do not specify the product, Extreme Agent ONE Coworker provides information about Extreme
Platform ONE Networking by default.
Extreme Agent ONE™ Coworker Overview Chats
Extreme Agent ONE™ Coworker v9.3.0 17


<!-- page 18 -->

Although Extreme Agent ONE Coworker can ask follow-up questions, it is better to include
additional context, such as specific settings or error messages, in your original query.
Note
Additional context also helps to improve response time by limiting the size of the
dataset to be scanned.
Example: Consider a large network with 70,000 users. The prompt "List all my
Windows clients." could take considerable time to process. The following prompts
include specific details such as time and region for faster, better results:
• "List all Windows clients connected in the last 24 hours."
• "List all Windows clients in the Toronto region."
• "List all Windows clients currently connected."
• "List all Windows clients currently connected, in the Toronto region."
Use Clear Language
Avoid overly technical language or acronyms that can have multiple meanings and be
confusing. Use straightforward terms that are commonly associated with your query, and
avoid complex sentence structure.
Ask One Question at a Time
If you have multiple questions, use a separate query for each. Break complex questions down
into parts to make it easier for Extreme Agent ONE Coworker to provide detailed and accurate
answers for each part of your request.
Example: Break the following query into two queries: "How do I configure VLAN settings and
update the firmware for an Extreme Networks 5520 switch?"
• "How do I configure VLAN settings for an Extreme Networks 5520 switch?"
• "How do I update the firmware for an Extreme Networks 5520 switch?"
Follow up
If the initial response does not fully answer your question, follow up with additional queries.
Extreme Agent ONE Coworker is designed to handle continuous conversations and to refine
answers based on your feedback.
Restrictions and Controls
Extreme Agent ONE Coworker is not equipped with the ability to take autonomous action.
Following are some of the restrictions and controls:
• Extreme Agent ONE Coworker never executes network changes or configuration
modifications on its own.
• Extreme Agent ONE Coworker never accesses or displays PII beyond what is shown in
Extreme Platform ONE Networking.
Restrictions and Controls Extreme Agent ONE™ Coworker Overview
18 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 19 -->

• Extreme Agent ONE Coworker limits Sev 1 pre-analysis to one notification at a time per
tenant with a timeout of four minutes. If the timeout is not done within 4 minutes, a
degraded nudge is delivered.
• All change requests that originate from an Extreme Agent ONE Coworker chat are logged
and viewable from the Audit Log page on Extreme Exchange™.
Requirements
The following requirements exist to use Extreme Agent ONE Coworker:
• Basic subscription to Extreme Platform ONE Networking or Extreme Platform ONE Security.
• Users must have one of the following roles:
◦ Admin
◦ NetSecOps
There is no specific configuration requirement to set up Extreme Agent ONE Coworker. It's on
as soon as you log in to Extreme Platform ONE using your Extreme ONE OS login credentials.
However, to use Extreme Agent ONE Coworker to monitor your network, you must first onboard
your network to Extreme Platform ONE. For information on how to onboard your network to
Extreme Platform ONE, see Extreme Platform ONE Networking User Guide.
Set Preferred Language
Extreme Agent ONE Coworker uses the preferred language setting from Extreme Platform ONE
Networking to determine the language used for user interface elements such as text labels,
shortcut commands, suggested actions, and nudges. Use this procedure to set the preferred
language.
Note
The response to a user-initiated prompt is always provided using the same language
that was used for the prompt, provided it's a language that Extreme Agent ONE
Coworker recognizes.
1. In Extreme Platform ONE Networking, select your user initials in the top right of the header.
2. Select Profile.
3. Under Language Preferences, select the preferred language.
4. Select Save Preferences.
Extreme Agent ONE™ Coworker Overview Requirements
Extreme Agent ONE™ Coworker v9.3.0 19


<!-- page 20 -->

Using Extreme Agent ONE Coworker
The User Interface on page 20
Getting Started with Extreme Agent ONE Coworker on page 25
Start a New Chat on page 25
Open Existing Chat on page 26
View Chat History on page 26
Snooze Informational Nudges on page 27
Respond to Nudge on page 27
Open Archived Canvas on page 28
Download Chat on page 28
Copy Chat on page 28
Submit Feedback on page 29
Launch Extreme Exchange on page 29
The User Interface
Extreme Agent ONE Coworker offers a chat interface that is woven throughout Extreme
Platform ONE Networking. From most pages in Extreme Platform ONE Networking, you can
always use one of the following user interface elements to engage with Extreme Agent ONE
Coworker:
• Extreme Agent ONE launch page
• Command Bar (full-sized or minimized)
• Command Center modal
• Chat Window
20 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 21 -->

User Interface Elements
Refer to Table 4 for a description of the Extreme Agent ONE Coworker User Interface elements.
Table 4: Extreme Agent ONE Coworker User Interface Elements
User Interface
Element
Details
Extreme Agent
ONE launch page
The launch page displays when you sign in to Extreme Platform ONE Networking
or by selecting Extreme Agent ONE from the left navigation menu on Extreme
Platform ONE Networking. The launch page provides announcements and includes
a built-in Command Bar for text prompts. However, note that you do not need to
be on this page to begin a chat.
Figure 1: Extreme Agent ONE launch page in Extreme Platform ONE Networking
Command Bar The floating Command Bar is your main tool while working in Extreme Platform ONE
Networking for initiating chats with Extreme Agent ONE Coworker. The Command
Bar sits on the Extreme Platform ONE Networking user interface and is visible from
most pages. You can start a chat by entering a text prompt or by selecting
  the
options menu and then selecting one of the commands there, including opening
the Command Center modal. You can also move the bar around the screen by
clicking and dragging it to where you want it to go.
Figure 2: Command Bar (Full-sized)
Optionally, you can select
  (Minimize) to reduce the size of the Command Bar.
The minimized Command Bar has the same options menu and functionality as the
full-sized version, but with no text prompt field. To enter a prompt, you can select
 (Expand) to return to the full-sized Command Bar.
Figure 3: Command Bar (Minimized)
Using Extreme Agent ONE Coworker The User Interface
Extreme Agent ONE™ Coworker v9.3.0 21


<!-- page 22 -->

Table 4: Extreme Agent ONE Coworker User Interface Elements (continued)
User Interface
Element
Details
Command Center A full command modal with multiple options for opening a chat, including entering
a text prompt or selecting one of the shortcut commands, suggested actions, or
chat history links.
You can launch Command Center using the Command Bar's
  options menu or
from the chat window by selecting
  (Command Center).
Figure 4: Command Center
Chat Window The Extreme Agent ONE chat window opens as a right-hand sidebar once a chat
is opened, either by entering a text prompt, answering a nudge, or by selecting one
of the available shortcuts, suggested actions, or existing chats. The chat window
displays the full chat, including the original prompt, any follow-up prompts, and
the responses. There's also a built-in text prompt field so that you can enter
additional prompts.
The chat window cannot be moved. However, depending on the data that is
returned, you can select
  (Expand) to view the results in the full window.
Figure 5: The Chat Window
The User Interface Using Extreme Agent ONE Coworker
22 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 23 -->

Common Icons
Refer to Table 5 for a description of the common icons that Extreme Agent ONE Coworker
uses.
Table 5: Common Icons used in Extreme Agent ONE Coworker
Icon Description
Minimize (Contract)—Select this icon from the main floating Command Bar to contract
the Command Bar to a minimized version that contains no text prompt field.
Note: This icon does not display when the Command Bar's text prompt field is built into
the page (for example, on the Extreme Agent ONE launch page, Command Center modal,
and in the Chat window).
This icon also displays if you previously selected the Expand option from the Chat window
to view the analysis in an expanded window. You can select
  to return the view to the
normal chat window.
Maximize (Expand)—Select this icon from the minimized Command Bar to return to the
full Command Bar with its text prompt field.
This icon also displays within the Extreme Agent ONE chat window when a table or screen
is pulled that appears in the main Extreme Platform ONE Networking interface. You can
select this icon if you'd like to see the results in the full Extreme Platform ONE Networking
window.
Options—Select this icon within the Command Bar (full or minimized versions) to view
a list of command options, including the ability to launch Command Center, start a new
chat, and snooze informational nudges.
Command Center—This icon opens the Command Center modal. From the Command
Center, you can enter text prompts or select from various shortcut commands, suggested
actions, and existing chats.
Suggested Actions contains three suggested prompts that Extreme Agent ONE Coworker
has provided. You can select the adjacent
  (Dismiss) icon to remove an action in which
case Extreme Agent ONE Coworker replaces it with a new suggestion.
Note: If
  is accompanied by the label Search, then this icon indicates a search box
where you can enter a search query, such as a specific device.
Copy—Select this icon to copy the chat. You can paste the result into another file such as
a text file or Word document.
Download—Select this icon to download the chat to a PDF file.
Snooze Informational Nudges—To snooze informational nudges, select one of the two
snooze timers: 15 min or 1 hour.
Note: Critical nudges can only be snoozed using chat. You can snooze critical nudges for
up to four hours.
New Chat—Select this icon to open a new chat in the chat window.
Last Chat—Select this icon to open the most recent chat in the chat window.
Using Extreme Agent ONE Coworker The User Interface
Extreme Agent ONE™ Coworker v9.3.0 23


<!-- page 24 -->

Table 5: Common Icons used in Extreme Agent ONE Coworker (continued)
Icon Description
Manage Skills from Exchange—Select this icon to open Extreme Exchange™. You can
use Extreme Exchange to view dashboards that monitor Extreme Agent ONE Coworker
performance as well as audit logs for any changes that get implemented as a result of an
Extreme Agent ONE Coworker conversation.
Good response—Select this icon when you want to provide Extreme Networks with
positive feedback for an Extreme Agent ONE Coworker response.
Bad response—Select this icon when you want to provide Extreme Networks with
negative feedback for an Extreme Agent ONE Coworker response.
Close—Select this icon to close an active chat or feedback window.
Rename—Select this icon in the Command Center to rename an existing chat. The new
name must be 8–50 alphanumeric characters.
,
 ,
 Nudge—A solid dot that displays in the Command Bar alongside a prompt indicates a
nudge. There are three types:
• Blue dot—Informational nudge
• Red dot—Critical nudge
• Gray dot—Unread response nudge
 or
 Read Chat—A hollow dot that displays within the Chat History indicates a chat that has
been viewed by the admin. If the hollow dot is red, the chat was initiated by a critical
nudge.
Note: If the dot is animated, it indicates a chat in which Extreme Agent ONE Coworker is
processing a response.
Delete—Select this icon in the Command Center to delete an existing chat. If the icon is
accompanied by a (Delete All) label, the action deletes all chats.
Shortcut Commands
Extreme Agent ONE Coworker includes a set of shortcut commands that you can use to
quickly execute functions. To use a shortcut, Extreme Agent ONE Coworker must be the active
window. If you are working in Extreme Platform ONE™ Networkign, select the Extreme Agent
ONE command bar or chat window to make it the active window and then select the shortcut
combination. Note that the shortcut combinations differ slightly for Windows and Mac.
Note
Shortcut commands are case insensitive.
Table 6: Shortcut Commands on Windows and MAC
Command (Windows) Command (Mac) Description
<Ctrl+I> <Command+I> Opens the introductory chat.
<Ctrl+O> <Command+O> Opens a new chat window.
<Ctrl+L> <Command+L> Opens the most recent chat.
<Ctrl+K> <Command+K> Opens the Command Center modal.
The User Interface Using Extreme Agent ONE Coworker
24 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 25 -->

Table 6: Shortcut Commands on Windows and MAC (continued)
Command (Windows) Command (Mac) Description
<Ctrl+E> <Command+E> Launches Extreme Exchange.
<Ctrl+M> <Command+M> Snooze or un-snooze informational nudges.
Snoozes initiated using this command use the
default snooze (15 min).
Getting Started with Extreme Agent ONE Coworker
An introductory chat is provided where Extreme Agent ONE Coworker introduces itself to you,
tells you what it knows about your network, and provides you with helpful information and
suggested prompts.
Note
It's a best practice to run the introductory chat when you first access Extreme Agent
ONE Coworker.
Use this task to get started:
1. Sign in to Extreme Platform ONE Networking.
2. From the Command Bar, select the
  options menu.
3. Select
  (Intro Chat).
The chat window opens at the introductory chat.
Note
• You can also open the introductory chat using one of the following shortcut
commands: <Ctrl+I> on Windows or <Command+I> on MAC.
• To sign out of Extreme Agent ONE Coworker, you must sign out of Extreme
Platform ONE Networking. To sign out, select your user initials in the top right
of the Extreme Platform ONE Networking header, and select Sign Out.
Start a New Chat
Use this task to start a new chat with Extreme Agent ONE Coworker.
1. From Extreme Platform ONE Networking, select the Command Bar.
Using Extreme Agent ONE Coworker Getting Started with Extreme Agent ONE Coworker
Extreme Agent ONE™ Coworker v9.3.0 25


<!-- page 26 -->

2. Enter a text prompt.
The Extreme Agent ONE chat window opens. Extreme Agent ONE Coworker thinks about
your question, provides information on its reasoning, and then responds.
Note
You can also start a new chat by doing the following:
• Enter the Open Chat shortcut command: <Ctrl+O> on Windows or <Command+O>
on Mac.
• From an existing chat window, select
  (New Chat).
• From the Command Bar, select the
  options menu and then select
  (New
Chat).
• From the Command Center, select one of the suggested actions to open a new
chat around the suggested topic.
• Answer a nudge. The nudge content displays in a new chat window once you
answer the nudge.
Open Existing Chat
Use this procedure to open an existing chat.
1. Launch the Command Center using either of these methods:
• From the Command Bar, select the
  options menu and then select
  (Command
Center).
• From the chat window, select
  (Command Center).
2. Under RECENT CHATS, search for the existing chat.
If the chat that you want to view is older than the three most recent chats, select All chats
to view the full list.
3. Select the chat that you want to view.
The chat window opens with the selected chat displaying. You can reinitiate the chat by
typing in a new prompt.
Note
You can also launch the most recent chat using either of these methods:
• From the Command Bar, select the
  options menu and then
  (Last Chat).
• Select the Last Chat shortcut command: <Ctrl+L> from Windows or
<Command+L> from Mac.
View Chat History
Use this procedure to access your Extreme Agent ONE chat history, which displays in
Command Center. By default, Command Center displays the three most recent chats.
1. Launch the Command Center using either of these methods:
• From the Command Bar, select the
  options menu and then select
  (Command
Center).
Open Existing Chat Using Extreme Agent ONE Coworker
26 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 27 -->

• From the Chat Window, select
  (Command Center).
2. Optional. Select All chats to expand the list of recent chats to include all chats.
Note
• Within the RECENT CHATS list, if the chat has an adjacent solid dot (for example,
), the chat has not been viewed. If the dot is hollow (for example,
 ), the
chat has been viewed. If the dot is animated, Extreme Agent ONE Coworker is
processing a response within the chat.
• To rename a chat, select the adjacent
  (Rename), enter a new chat name that is
8–50 alphanumeric characters, and press Enter.
• To delete a chat, select
  (Delete) and then select Delete. To delete all chats,
select
  (Delete All).
Snooze Informational Nudges
Use this procedure to turn snooze on for informational nudges.
1. From the Extreme Agent ONE Command Bar, select the
  options menu.
2. Under Snooze Informational Nudges, select 15 min (default option) or 1 hour.
The snooze icon
  displays in the Command Bar.
Note
• You can also snooze informational nudges using one of the shortcut commands:
<Ctrl+M> from Windows or <Command+M> from Mac. The default snooze timer (15
min) gets applied to snoozes initiated using this method.
• Turn the snooze off from the Command Bar by deselecting the
  icon or by
entering one of the preceding shortcut commands.
• Critical nudges can only be snoozed using the chat. You can snooze critical
nudges for up to four hours.
Respond to Nudge
Use this procedure to respond to an informational or critical nudge.
Note
You can tell that you have received a nudge, because the Command Bar pulses and a
message displays.
1. In the Command Bar, do a hover-over of the nudge message.
2. In the nudge text bubble, select See More.
The nudge opens in the chat window. The chat shows the nudge. For critical nudges, the
chat also shows the Extreme Agent ONE Coworker preliminary analysis. Respond to the
nudge by entering a prompt in the chat window's text prompt field, or by selecting any
shortcut responses that display.
Using Extreme Agent ONE Coworker Snooze Informational Nudges
Extreme Agent ONE™ Coworker v9.3.0 27


<!-- page 28 -->

Open Archived Canvas
Use this task to access the Archived Canvases option, which lets you view archived canvases
and widgets.
1. From the Command Bar, select the
  options menu.
2. Select
  (Command Center).
3. Select the Archived Canvases option and then select the canvas that you want to view.
The canvas displays with relevant tables, charts, or graphs.
Note
• To download or delete the canvas information, from the top right of the canvas,
select
  (Download) to download the canvas information in a zip file or select
 Delete to delete the canvas. Depending on the types of widgets in the canvas,
the zip file may include a .csv file for tabular data and a .png file for graphical
information.
• To download or delete information for a specific chart or table, from the top right
of the table or chart, select the
  options menu and then select
  (Download)
or
  (Delete). For tables, the download file will be a .csv file, and for charts, the
download file will be a .png file.
Download Chat
Use this procedure to download an existing chat in PDF.
1. Open the Extreme Agent ONE Coworker chat that you want to download.
2. From the chat window, select
  (Download).
A PDF with the chat dialogue downloads to your local machine.
Copy Chat
Extreme Agent ONE Coworker supports copy and paste from chat. Use this task to copy a
chat. You can paste the chat into a text file or other document.
1. Open the Extreme Agent ONE Coworker chat that you want to copy.
2. Select
  (Copy).
3. Paste the chat into a text file or other document.
Open Archived Canvas Using Extreme Agent ONE Coworker
28 Extreme Agent ONE™ Coworker v9.3.0


<!-- page 29 -->

Submit Feedback
Use the feedback icons (
  or
 ) to submit your feedback to Extreme Networks on the
quality of the Extreme Agent ONE response. The feedback icons display in the chat window
after the Extreme Agent ONE response.
Note
Your feedback is used by Extreme Networks to ensure the future quality of Extreme
Agent ONE responses.
1. In the Extreme Agent ONE chat window, select the icon that matches your evaluation of the
quality of the response:
•
  (Good response)
•
  (Bad response)
2. Optional. In the feedback window, provide extra information to qualify your rating:
• Select one of the shortcut buttons that matches your rating evaluation. For example,
Accurate or Incorrect.
• Enter a text explanation for your rating.
3. Select one of the following:
• Send Feedback—Select this option to submit your feedback to Extreme Networks.
• Maybe Next Time or
  (Close)—Selecting either option clears your qualifying
information, but retains the initial
  or
  rating.
Note
To change your response, close the feedback window and select the other icon.
To clear previously submitted feedback, select the same response icon that you
selected previously and then select Clear Feedback.
Launch Extreme Exchange
Use this task to launch Extreme Exchange™ from Extreme Platform ONE Networking. You can
use Extreme Exchange to view performance data, telemetry information, and audit logs for
Extreme Agent ONE Coworker.
1. From the Extreme Agent ONE Command Bar, select the
  options menu.
2. Select
  (Manage Skills in Exchange).
Note
• You can also launch Extreme Exchange by selecting one of the shortcut
commands: <Ctrl+E> from Windows or <Command+E> from Mac.
• For information on Extreme Exchange, see Extreme Exchange™ User Guide
Using Extreme Agent ONE Coworker Submit Feedback
Extreme Agent ONE™ Coworker v9.3.0 29
