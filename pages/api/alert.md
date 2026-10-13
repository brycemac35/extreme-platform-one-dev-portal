---
source: https://developer.extremeplatformone.com/api-reference/alert
spec: https://developer.extremeplatformone.com/api/spec/alert
title: "Extreme Platform ONE REST API - Alert"
---

# Extreme Platform ONE REST API - Alert

**Alert** · Services. Events and Alerts.

The Extreme Platform ONE™ Alert API provides comprehensive monitoring and management of network alerts, enabling proactive detection of issues across your Extreme network infrastructure through configurable alert policies and intelligent rule-based alerting. **🔔 Intelligent Alert Management:** • **Real-Time Alert Monitoring** - Centralized visibility into network alerts with filtering by severity, category, site, device, and acknowledgment status for rapid issue identification and triage • **Flexible Alert Policies** - Global policies for organization-wide alerting with optional site-specific policy overrides for customized alerting behavior per location • **Configurable Alert Rules** - Event-based and metric-based rules with multiple trigger types (immediate, deferred, and repeated) to match your operational requirements • **Alert Analytics & Reporting** - Statistical analysis by device, location, severity, and category with exportable reports for compliance and trending • **Alert Acknowledgment Workflow** - Track alert review status to coordinate team response and filter out already-addressed alerts from active monitoring **🏢 Enterprise-Scale Operations:** Built for enterprise environments with support for multi-site deployments, hierarchical location-based alerting, bulk alert operations, and comprehensive audit trails for large-scale network monitoring.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/alert/v1` — Extreme Platform ONE REST API - Alert

Full OpenAPI document: [`specs/alert.json`](../../specs/alert.json)

## Endpoints

28 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/alerts` | List Alerts |
| POST | `/alerts` | List alerts with more supporting filters |
| POST | `/alerts/:acknowledge` | Acknowledge Alerts |
| POST | `/alerts/:clear` | Clear Alerts |
| GET | `/alerts/count-by-{group}` | Count Alerts by Group |
| GET | `/alerts/stats-by-device` | Get Alert Statistics by Device |
| GET | `/alerts/stats-by-location` | Get Alert Statistics by Location |
| GET | `/alerts/{deviceId}/stats` | Get Device Alert Statistics |
| POST | `/alerts/reports` | Create Alert Report |
| GET | `/alerts/reports/{id}` | Download Alert Report |
| GET | `/alert-policies` | List Alert Policies |
| POST | `/alert-policies` | Create Site Alert Policy |
| GET | `/alert-policies/site-policies` | List Site Alert Policies |
| GET | `/alert-policies/{policyId}` | Get Alert Policy |
| PUT | `/alert-policies/{policyId}` | Update Site Alert Policy |
| DELETE | `/alert-policies/{policyId}` | Delete Site Alert Policy |
| GET | `/alert-policies/available-sites` | List Available Sites |
| GET | `/alert-policies/sites` | List Sites by Filter |
| GET | `/alert-policies/{policyId}/rules` | List Alert Policy Rules |
| GET | `/alert-policies/{policyId}/rules/{ruleId}` | Get Alert Rule |
| PUT | `/alert-policies/{policyId}/rules/{ruleId}` | Update Alert Rule |
| POST | `/alert-policies/{policyId}/rules/{ruleId}/:enable` | Enable Alert Rule |
| POST | `/alert-policies/{policyId}/rules/{ruleId}/:disable` | Disable Alert Rule |
| GET | `/metadata/apps` | List Alert Applications |
| GET | `/metadata/categories` | List Alert Categories |
| GET | `/metadata/message-types` | List Alert Message Types |
| GET | `/metadata/severities` | List Alert Severities |
| GET | `/metadata/source-types` | List Alert Source Types |

## GET `/alerts`

Operation: `listAlerts`

List Alerts

Retrieves a paginated list of alerts filtered by time range, severity, category, site, device, and acknowledgment status. Alerts represent network events or metric threshold violations detected by the alert policy rules.

Tags: `Alert`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
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

## POST `/alerts`

Operation: `listAlertsPost`

List alerts with more supporting filters

POST request for listing alerts that can filter 30+ Site IDs and other supported filters from the GET alerts API.

Tags: `Alert`

Request body:

- `application/json` — alertFilterRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alerts/:acknowledge`

Operation: `acknowledgeAlerts`

Acknowledge Alerts

Marks one or more alerts as acknowledged. Acknowledged alerts indicate that an operator has reviewed and noted the alert. This helps teams track which alerts have been addressed and filter out already-reviewed alerts from active monitoring views.

Tags: `Alert`

Request body:

- `application/json` — alertIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alerts/:clear`

Operation: `clearAlerts`

Clear Alerts

Marks one or more alerts as inactive (cleared). Clearing an alert sets its status to inactive, indicating it has been resolved or dismissed. This helps teams remove resolved alerts from active monitoring views.

Tags: `Alert`

Request body:

- `application/json` — alertIds

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alerts/count-by-{group}`

Operation: `countAlertsByGroup`

Count Alerts by Group

Retrieves alert counts grouped by the specified dimension (severity, category, or alert type). Useful for generating dashboards and understanding the distribution of alerts across different classifications.

Tags: `Alert`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
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

## GET `/alerts/stats-by-device`

Operation: `statsAlertsByDevice`

Get Alert Statistics by Device

Retrieves alert count statistics grouped by device. Useful for identifying devices with the most alerts and prioritizing troubleshooting efforts. Results can be filtered by time range, severity, site, and acknowledgment status.

Tags: `Alert`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
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

## GET `/alerts/stats-by-location`

Operation: `statsAlertsByLocation`

Get Alert Statistics by Location

Retrieves alert count statistics grouped by location hierarchy (site, building, or floor). Useful for identifying locations with the most alerts and understanding geographic distribution of network issues.

Tags: `Alert`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
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

## GET `/alerts/{deviceId}/stats`

Operation: `alertCountStats`

Get Device Alert Statistics

Retrieves alert statistics for a specific device, including alert counts aggregated by severity level and time-series data showing alert trends over the specified time range.

Tags: `Alert`

Parameters:

- `deviceId` path, required (integer) — The required device ID
- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alerts/reports`

Operation: `createAlertReport`

Create Alert Report

Initiates generation of an alert report based on the specified filters. The report is generated asynchronously and can be downloaded using the returned report ID. Reports can be filtered by time range, severity, category, site, device, and other criteria.

Tags: `Alert`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `timeZoneOffset` query, optional (integer) — The time zone offset in minutes from UTC, used to localize timestamps in the report. Range: -720 (UTC-12:00) to 840 (UTC+14:00). Examples: -480 for PST (UTC-8), 0 for UTC, 60 for CET (UTC+1), 330 for IST (UTC+5:30).

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alerts/reports/{id}`

Operation: `downloadAlertReport`

Download Alert Report

Downloads a previously generated alert report by its ID. The report is returned as a binary file (CSV or Excel format based on the original request).

Tags: `Alert`

Parameters:

- `id` path, required (integer) — The report ID

Responses:

- `200` — OK. Returns the report as a binary file. The content is in CSV or Excel format depending on the export headers specified when creating the report.
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies`

Operation: `listAlertPolicies`

List Alert Policies

Retrieves all alert policies (global and site-specific) belonging to the current user, including an overview of associated alert rules. Each account has one global policy that applies to all sites, plus optional site-specific policies that override the global policy for designated sites.

Tags: `Alert Policy`

Parameters:

- `keyword` query, optional (string) — The keyword to filter, such as policy name or site name
- `policyType` query, optional (CasAlertPolicyType) — The policy type to filter, such as SITE or GLOBAL
- `displayRules` query, optional (boolean) — Display event & metric rules configured on the application. This value is true by default.
- `enable` query, optional (boolean) — Filter policy rules based on their enabled status. The default value is empty. Note that this parameter has no effect if displayRules is set to false, as rules will not be displayed in that case.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alert-policies`

Operation: `createAlertPolicy`

Create Site Alert Policy

Creates a new site-based alert policy. Site policies override the global policy for the assigned sites, allowing customized alerting behavior per location. The global policy is created automatically for each account and cannot be created via this endpoint.

Tags: `Alert Policy`

Request body:

- `application/json` — CasCreateAlertPolicyRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/site-policies`

Operation: `listAlertSitePolicies`

List Site Alert Policies

Retrieves a paginated list of site-based alert policies along with their assigned sites. Optionally includes the event and metric rules configured for each policy. Does not include the global policy. Supports filtering by site ID and policy name.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `None` , optional
- `sortField` query, optional (CasAlertPolicySortField) — The sort field
- `None` , optional
- `keyword` query, optional (string) — The keyword to filter by policy name or site name.
- `displayRules` query, optional (boolean) — Display event & metric rules configured on the application. This value is false by default.
- `enable` query, optional (boolean) — Filter policy rules based on their enabled status. The default value is empty. Note that this parameter has no effect if displayRules is set to false, as rules will not be displayed in that case.
- `siteIds` query, optional (array) — Filter policies by site IDs. Returns only policies assigned to any of the specified sites.
- `policyNames` query, optional (array) — Filter policies by site policy names. Returns policies matching any of the specified names.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/{policyId}`

Operation: `getAlertPolicy`

Get Alert Policy

Retrieves detailed information for a specific alert policy, including all configured alert rules with their trigger conditions, severity levels, and enabled states.

Tags: `Alert Policy`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/alert-policies/{policyId}`

Operation: `updateAlertPolicy`

Update Site Alert Policy

Updates a site-based alert policy's name and assigned sites. The global policy cannot be modified through this endpoint. Use the available-sites endpoint to get a list of sites that can be assigned to a policy.

Tags: `Alert Policy`

Parameters:

- `None` , optional

Request body:

- `application/json` — CasUpdateAlertPolicyRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/alert-policies/{policyId}`

Operation: `deleteAlertPolicy`

Delete Site Alert Policy

Permanently deletes a site-based alert policy and all its associated alert rules. Sites previously assigned to this policy will revert to using the global policy. The global policy cannot be deleted.

Tags: `Alert Policy`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/available-sites`

Operation: `listAvailableSites`

List Available Sites

Retrieves sites that are available for assignment to a new site-based alert policy. Sites already assigned to an existing site policy are excluded from this list. Only sites using the global policy are returned.

Tags: `Alert Policy`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/sites`

Operation: `listSites`

List Sites by Filter

Retrieves sites filtered by their alert policy assignment status. Use the sitesFilter parameter to get sites with a specific policy, sites using the global policy, or all sites.

Tags: `Alert Policy`

Parameters:

- `sitesFilter` query, optional (CasSitesFilter) — Filter sites by alert policy assignment status. AVAILABLE: sites without a site-specific alert policy assignment (they use the global policy). UNAVAILABLE: sites with a site-specific alert policy assignment. ALL: all sites, whether they…

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/{policyId}/rules`

Operation: `queryAlertRules`

List Alert Policy Rules

Retrieves alert rules for a specific policy, with optional filtering by application, rule type (event or metric), rule status (enabled or disabled), and keyword search. Rules define the conditions that trigger alerts.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `app` query, optional (string) — The application code to filter rules by (e.g., 'XIQ', 'XSW', 'XUZ', 'XCA'). Use the listAlertApps API to retrieve all valid application codes.
- `ruleType` query, optional (CasAlertRuleType) — The rule type to query
- `ruleStatus` query, optional (CasAlertRuleStatus) — The rule status to query
- `keyword` query, optional (string) — The rule name to query

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/alert-policies/{policyId}/rules/{ruleId}`

Operation: `getAlertRule`

Get Alert Rule

Retrieves detailed configuration for a specific alert rule, including trigger type, severity, threshold settings, and enabled state.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/alert-policies/{policyId}/rules/{ruleId}`

Operation: `updateAlertRule`

Update Alert Rule

Updates an alert rule's configuration including severity, trigger type, and threshold settings. Note that the rule's identifier may change as a result of this operation; use the returned rule object for subsequent operations.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `None` , optional

Request body:

- `application/json` — XiqUpdateAlertRuleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alert-policies/{policyId}/rules/{ruleId}/:enable`

Operation: `enableAlertRule`

Enable Alert Rule

Enables an alert rule so it actively monitors for the configured conditions and generates alerts when triggered. Note that the rule's identifier may change as a result of this operation.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/alert-policies/{policyId}/rules/{ruleId}/:disable`

Operation: `disableAlertRule`

Disable Alert Rule

Disables an alert rule so it stops monitoring and generating alerts. The rule configuration is preserved and can be re-enabled later. Note that the rule's identifier may change as a result of this operation.

Tags: `Alert Policy`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/apps`

Operation: `listAlertApps`

List Alert Applications

Retrieves the list of applications (e.g., XIQ, XCA, SD-WAN) that support alerting. Use the returned app codes when filtering alerts or configuring alert rules.

Tags: `Metadata`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/categories`

Operation: `listAlertCategories`

List Alert Categories

Retrieves all available alert categories (e.g., Network, Security, Hardware). Categories group related alert types and can be used to filter alerts in list and report queries.

Tags: `Metadata`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/message-types`

Operation: `listAlertMessageTypes`

List Alert Message Types

Retrieves all available alert message types. Message types define specific alert conditions (e.g., "Device Offline", "High CPU Usage") and are used when configuring alert rules.

Tags: `Metadata`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/severities`

Operation: `listAlertSeverities`

List Alert Severities

Retrieves all available alert severity levels (e.g., Critical, Major, Minor, Warning, Informational). Severities indicate the urgency of alerts and can be used for filtering and prioritization.

Tags: `Metadata`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/metadata/source-types`

Operation: `listAlertSourceTypes`

List Alert Source Types

Retrieves all available alert source types. Source types identify the origin of alerts (e.g., Device, Client, Network Service) and can be used to filter alerts by their source.

Tags: `Metadata`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

