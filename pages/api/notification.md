---
source: https://developer.extremeplatformone.com/api-reference/notification
spec: https://developer.extremeplatformone.com/api/spec/notification
title: "Extreme Platform ONE REST API - Notification"
---

# Extreme Platform ONE REST API - Notification

**Notification** · Services. Notification.

The Extreme Platform ONE™ Notification API provides comprehensive management of notification subscriptions and delivery rules, enabling automated alerting across multiple channels to keep your team informed of critical network events, subscription lifecycle changes, and contract milestones. **📬 Multi-Channel Notification Delivery:** • **Email Notifications** - Configure email recipients for alert notifications with built-in verification workflow to ensure delivery to valid addresses • **Webhook Integration** - Set up HTTP endpoints to receive real-time JSON payloads with optional HMAC signature verification for secure integrations • **ServiceNow Integration** - Automatically create incidents in ServiceNow when alerts trigger, streamlining IT service management workflows • **Mobile Push Notifications** - Deliver instant notifications to mobile applications via APNs (iOS) and FCM (Android) for on-the-go alerting **📋 Intelligent Notification Rules:** • **Subscription Lifecycle Rules** - Timeline-based and event-based triggers for license expiration warnings, renewal reminders, and activation notifications • **Contract Lifecycle Rules** - Automated notifications for hardware support contract milestones, warranty expirations, and renewal deadlines • **Flexible Rule Configuration** - Predefined system rules plus custom user-defined rules with per-application filtering **🏢 Enterprise Management:** Built for enterprise environments with bulk operations for managing multiple subscriptions, organization-wide notification policies, and comprehensive audit trails for compliance and operational visibility.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/notification/v1` — Extreme Platform ONE REST API - Notification

Full OpenAPI document: [`specs/notification.json`](../../specs/notification.json)

## Endpoints

39 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/email` | List Email Subscriptions |
| POST | `/email` | Create Email Subscription |
| POST | `/email/:delete` | Bulk Delete Email Subscriptions |
| POST | `/email/:enable` | Bulk Enable/Disable Email Subscriptions |
| GET | `/email/{id}` | Get Email Subscription |
| PUT | `/email/{id}` | Update Email Subscription |
| PATCH | `/email/{id}` | Patch Email Subscription |
| POST | `/email/{id}/:verify` | Send Verification Email |
| POST | `/email/:verify` | Bulk Send Verification Emails |
| GET | `/webhook` | List Webhook Subscriptions |
| POST | `/webhook` | Create Webhook Subscription |
| POST | `/webhook/:delete` | Bulk Delete Webhook Subscriptions |
| POST | `/webhook/:enable` | Bulk Enable/Disable Webhook Subscriptions |
| GET | `/webhook/{id}` | Get Webhook Subscription |
| PUT | `/webhook/{id}` | Update Webhook Subscription |
| PATCH | `/webhook/{id}` | Patch Webhook Subscription |
| GET | `/servicenow` | List ServiceNow Subscriptions |
| POST | `/servicenow` | Create ServiceNow Subscription |
| POST | `/servicenow/:delete` | Bulk Delete ServiceNow Subscriptions |
| POST | `/servicenow/:enable` | Bulk Enable/Disable ServiceNow Subscriptions |
| GET | `/servicenow/{id}` | Get ServiceNow Subscription |
| PUT | `/servicenow/{id}` | Update ServiceNow Subscription |
| PATCH | `/servicenow/{id}` | Patch ServiceNow Subscription |
| GET | `/rules/contract` | List Contract Notification Rules |
| POST | `/rules/contract` | Create Contract Notification Rule |
| POST | `/rules/contract/:delete` | Delete Contract notification rules in bulk |
| GET | `/rules/contract/{id}` | Get a specific Contract notification rule |
| PUT | `/rules/contract/{id}` | Update Contract notification rule |
| PATCH | `/rules/contract/{id}` | Partial or full update Contract notification rule |
| GET | `/rules/contract/summary` | Get recipient count for the notification rule |
| GET | `/rules/subscription` | List Subscription Notification Rules |
| POST | `/rules/subscription` | Create Subscription Notification Rule |
| POST | `/rules/subscription/:delete` | Delete Subscription notification rules in bulk |
| GET | `/rules/subscription/{id}` | Get Subscription Notification Rule |
| PUT | `/rules/subscription/{id}` | Update Subscription Notification Rule |
| PATCH | `/rules/subscription/{id}` | Patch Subscription Notification Rule |
| GET | `/rules/subscription/summary` | Get recipient count for the notification rule |
| GET | `/metadata/timeline-rules` | List Timeline Rule Templates |
| GET | `/metadata/event-rules` | List Event Rules |

## GET `/email`

Operation: `listEmailSubscriptions`

List Email Subscriptions

Retrieves a paginated list of email notification subscriptions. Each subscription represents an email address configured to receive alert notifications based on specified rules and filters.

Tags: `Email Notification`

Parameters:

- `keyword` query, optional (string) — The keyword to filter email addresses. If blank then skip this filter criteria.
- `None` , optional
- `None` , optional
- `sortField` query, optional (CnsAlertEmailSortField) — The sort field is the email address.
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/email`

Operation: `createEmailSubscription`

Create Email Subscription

Creates one or more email notification subscriptions. Each subscription associates an email address with alert configurations, subscription rules, or contract rules. New email addresses require verification before notifications are sent.

Tags: `Email Notification`

Request body:

- `application/json` — XiqCreateAlertEmailSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/email/:delete`

Operation: `deleteBulkAlertSubscriptionEmail`

Bulk Delete Email Subscriptions

Deletes multiple email subscriptions in a single request. Returns a summary of successful and failed deletions. Deleted subscriptions will immediately stop receiving notifications.

Tags: `Email Notification`

Request body:

- `application/json` — notificationIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/email/:enable`

Operation: `enableBulkEmailNotification`

Bulk Enable/Disable Email Subscriptions

Enables or disables multiple email subscriptions in a single request. Disabled subscriptions remain configured but will not receive notifications until re-enabled.

Tags: `Email Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — notificationIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/email/{id}`

Operation: `getEmailSubscription`

Get Email Subscription

Retrieves detailed information for a specific email subscription, including its verification status, enabled state, and configured notification rules.

Tags: `Email Notification`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/email/{id}`

Operation: `updateEmailSubscription`

Update Email Subscription

Fully replaces an existing email subscription configuration. All fields in the request body will overwrite the current values. Use PATCH for partial updates.

Tags: `Email Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqUpdateAlertEmailSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/email/{id}`

Operation: `patchEmailSubscription`

Patch Email Subscription

Partially updates an email subscription. Only the fields provided in the request body will be modified; other fields retain their current values.

Tags: `Email Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqPatchAlertEmailSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/email/{id}/:verify`

Operation: `verifySubscriptionEmail`

Send Verification Email

Sends a verification email to the subscription's email address. The recipient must click the verification link in the email to confirm ownership. Unverified email addresses will not receive alert notifications. This endpoint can be called again to resend the verification email if the original expired or was not received.

Tags: `Email Notification`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/email/:verify`

Operation: `verifySubscriptionEmailsBulk`

Bulk Send Verification Emails

Sends verification emails to multiple email subscriptions in a single request. Each recipient must click their verification link to confirm ownership. This is useful for re-sending verification emails to multiple unverified addresses.

Tags: `Email Notification`

Request body:

- `application/json` — notificationIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/webhook`

Operation: `listWebhookSubscriptions`

List Webhook Subscriptions

Retrieves a paginated list of webhook notification subscriptions. Each subscription represents an HTTP endpoint configured to receive alert notification payloads via POST requests.

Tags: `Webhook Notification`

Parameters:

- `keyword` query, optional (string) — The keyword to filter webhook URL. If blank then skip this filter criteria.
- `None` , optional
- `None` , optional
- `sortField` query, optional (CnsAlertWebhookSortField) — The sort field is the webhook URL.
- `None` , optional
- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/webhook`

Operation: `createWebhookSubscription`

Create Webhook Subscription

Creates one or more webhook notification subscriptions. Each subscription configures an HTTPS endpoint to receive JSON payloads when alerts match the specified rules. Optionally include a shared secret for HMAC signature verification.

Tags: `Webhook Notification`

Request body:

- `application/json` — XiqCreateAlertWebhookSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/webhook/:delete`

Operation: `deleteBulkAlertSubscriptionWebhook`

Bulk Delete Webhook Subscriptions

Deletes multiple webhook subscriptions in a single request. Returns a summary of successful and failed deletions. Deleted subscriptions will immediately stop receiving notification payloads.

Tags: `Webhook Notification`

Request body:

- `application/json` — notificationIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/webhook/:enable`

Operation: `enableBulkWebhookNotification`

Bulk Enable/Disable Webhook Subscriptions

Enables or disables multiple webhook subscriptions in a single request. Disabled subscriptions remain configured but will not receive notification payloads until re-enabled.

Tags: `Webhook Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — notificationIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/webhook/{id}`

Operation: `getWebhookSubscription`

Get Webhook Subscription

Retrieves detailed information for a specific webhook subscription, including its endpoint URL, enabled state, and configured notification rules.

Tags: `Webhook Notification`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/webhook/{id}`

Operation: `updateWebhookSubscription`

Update Webhook Subscription

Fully replaces an existing webhook subscription configuration. All fields in the request body will overwrite the current values. Use PATCH for partial updates.

Tags: `Webhook Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqUpdateAlertWebhookSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/webhook/{id}`

Operation: `patchWebhookSubscription`

Patch Webhook Subscription

Partially updates a webhook subscription. Only the fields provided in the request body will be modified; other fields retain their current values.

Tags: `Webhook Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqPatchAlertWebhookSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/servicenow`

Operation: `listServiceNowSubscriptions`

List ServiceNow Subscriptions

Retrieves a paginated list of ServiceNow notification subscriptions. Each subscription represents a ServiceNow instance configured to receive alert notifications as incidents or events.

Tags: `ServiceNow Notification`

Parameters:

- `keyword` query, optional (string) — The keyword to filter ServiceNow accounts. If blank then skip this filter criteria.
- `None` , optional
- `None` , optional
- `sortField` query, optional (CnsAlertServiceNowSortField) — The sort field is the ServiceNow account email.
- `None` , optional
- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/servicenow`

Operation: `createServiceNowSubscription`

Create ServiceNow Subscription

Creates a new ServiceNow notification subscription. The subscription connects to a ServiceNow instance using provided credentials and creates incidents or events when alerts match the specified rules.

Tags: `ServiceNow Notification`

Request body:

- `application/json` — XiqCreateAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/servicenow/:delete`

Operation: `deleteBulkAlertSubscriptionServiceNow`

Bulk Delete ServiceNow Subscriptions

Deletes multiple ServiceNow subscriptions in a single request. Returns a summary of successful and failed deletions. Deleted subscriptions will immediately stop creating incidents in ServiceNow.

Tags: `ServiceNow Notification`

Request body:

- `application/json` — notificationIds1

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/servicenow/:enable`

Operation: `enableBulkServiceNowNotification`

Bulk Enable/Disable ServiceNow Subscriptions

Enables or disables multiple ServiceNow subscriptions in a single request. Disabled subscriptions remain configured but will not create incidents in ServiceNow until re-enabled.

Tags: `ServiceNow Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — notificationIds1

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/servicenow/{id}`

Operation: `getServiceNowSubscription`

Get ServiceNow Subscription

Retrieves detailed information for a specific ServiceNow subscription, including its instance URL, enabled state, and configured notification rules.

Tags: `ServiceNow Notification`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/servicenow/{id}`

Operation: `updateServiceNowSubscription`

Update ServiceNow Subscription

Fully replaces an existing ServiceNow subscription configuration. All fields in the request body will overwrite the current values. Use PATCH for partial updates.

Tags: `ServiceNow Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqUpdateAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/servicenow/{id}`

Operation: `patchServiceNowSubscription`

Patch ServiceNow Subscription

Partially updates a ServiceNow subscription. Only the fields provided in the request body will be modified; other fields retain their current values.

Tags: `ServiceNow Notification`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqPatchAlertServiceNowSubscriptionRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/rules/contract`

Operation: `listContractRules`

List Contract Notification Rules

Retrieves a paginated list of contract-based notification rules. Contract rules define triggers for hardware support contract lifecycle events such as warranty expiration, support renewal deadlines, and contract activation notifications.

Tags: `Notification Rules`

Parameters:

- `keyword` query, optional (string) — The keyword to filter Contract notification rules. If blank then skip this filter criteria.
- `None` , optional
- `None` , optional
- `sortField` query, optional (CnsNotificationRuleSortField) — The sort field is the Contract notification rule name.
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/rules/contract`

Operation: `createContractNotificationRule`

Create Contract Notification Rule

Creates a new contract-based notification rule. The rule can include timeline-based triggers (e.g., notify 60 days before contract expiration) and/or event-based triggers (e.g., notify when contract is renewed). Rules can be associated with email, webhook, or ServiceNow subscriptions.

Tags: `Notification Rules`

Request body:

- `application/json` — XiqCreateContractNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## POST `/rules/contract/:delete`

Operation: `deleteBulkContractNotificationRules`

Delete Contract notification rules in bulk

Delete Contract notification rules by a list of provided IDs.

Tags: `Notification Rules`

Request body:

- `application/json` — notificationRuleIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/rules/contract/{id}`

Operation: `getContractNotificationRule`

Get a specific Contract notification rule

Get details for a specific Contract notification rule.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/rules/contract/{id}`

Operation: `updateContractNotificationRule`

Update Contract notification rule

Update Contract notification rule.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqUpdateContractNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## PATCH `/rules/contract/{id}`

Operation: `patchContractNotificationRule`

Partial or full update Contract notification rule

Partial or full update Contract notification rule.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqPatchContractNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## GET `/rules/contract/summary`

Operation: `getContractNotificationRuleSummary`

Get recipient count for the notification rule

Get recipient count for the Contract notification rule.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/rules/subscription`

Operation: `listSubscriptionRules`

List Subscription Notification Rules

Retrieves a paginated list of subscription-based notification rules. Subscription rules define triggers for license and subscription lifecycle events such as expiration warnings, renewal reminders, and activation notifications.

Tags: `Notification Rules`

Parameters:

- `keyword` query, optional (string) — The keyword to filter Subscription notification rules. If blank then skip this filter criteria.
- `None` , optional
- `None` , optional
- `None` , optional
- `sortField` query, optional (CnsNotificationRuleSortField) — The sort field is the Subscription notification rule name.
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/rules/subscription`

Operation: `createSubscriptionNotificationRule`

Create Subscription Notification Rule

Creates a new subscription-based notification rule. The rule can include timeline-based triggers (e.g., notify 30 days before expiration) and/or event-based triggers (e.g., notify when subscription is activated). Rules can be associated with email, webhook, or ServiceNow subscriptions.

Tags: `Notification Rules`

Request body:

- `application/json` — XiqCreateSubscriptionNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## POST `/rules/subscription/:delete`

Operation: `deleteBulkSubscriptionNotificationRules`

Delete Subscription notification rules in bulk

Delete Subscription notification rules by a list of provided IDs.

Tags: `Notification Rules`

Request body:

- `application/json` — notificationRuleIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/rules/subscription/{id}`

Operation: `getSubscriptionNotificationRule`

Get Subscription Notification Rule

Retrieves detailed information for a specific subscription notification rule, including its timeline rules, event rules, and associated applications.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/rules/subscription/{id}`

Operation: `updateSubscriptionNotificationRule`

Update Subscription Notification Rule

Fully replaces an existing subscription notification rule configuration. All fields in the request body will overwrite the current values. Use PATCH for partial updates.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqUpdateSubscriptionNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## PATCH `/rules/subscription/{id}`

Operation: `patchSubscriptionNotificationRule`

Patch Subscription Notification Rule

Partially updates a subscription notification rule. Only the fields provided in the request body will be modified; other fields retain their current values.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Request body:

- `application/json` — XiqPatchSubscriptionNotificationRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `409`
- `500`

## GET `/rules/subscription/summary`

Operation: `getSubscriptionNotificationRuleSummary`

Get recipient count for the notification rule

Get recipient count for the Subscription notification rule.

Tags: `Notification Rules`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/timeline-rules`

Operation: `listTimelineRules`

List Timeline Rule Templates

Retrieves all available timeline rule templates. Timeline rules define time-based notification triggers relative to subscription events (e.g., "30 days before expiration", "7 days before renewal"). Use the returned rule IDs when creating subscription or contract notification rules.

Tags: `Metadata`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/event-rules`

Operation: `listEventRules`

List Event Rules

List all Event rules.

Tags: `Metadata`

Parameters:

- `rule_type` query, optional (RuleType) — Indicates if the event rule is targeted for any rule.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

