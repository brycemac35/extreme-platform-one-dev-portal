---
source: https://developer.extremeplatformone.com/api-reference/subscription
spec: https://developer.extremeplatformone.com/api/spec/subscription
title: "Extreme Platform ONE REST API - Subscriptions & Licensing"
---

# Extreme Platform ONE REST API - Subscriptions & Licensing

**Subscription** · Services. Subscription and Licensing.

The Extreme Platform ONE™ License API provides comprehensive management of software licenses, subscriptions, and entitlements across your Extreme network infrastructure, enabling centralized visibility and control over all licensing aspects from trial activation through operational management. **🔑 License & Entitlement Management:** • **License Summary & Details** - Centralized dashboard view of all licenses with health status indicators, expiration tracking, and utilization metrics across applications • **Entitlement Tracking** - Complete visibility into license entitlements with filtering by application, license type, and status for effective license inventory management • **License Synchronization** - On-demand synchronization with Extreme Portal to ensure license information is current and accurate • **License Reporting** - Exportable reports for compliance auditing, capacity planning, and license utilization analysis **🔗 Portal Integration:** • **Extreme Portal Linking** - Seamless account linking between ExtremeCloud IQ and Extreme Portal for automated license provisioning and management • **Partner Portal Integration** - MSP and partner account linking for multi-tenant license management and entitlement distribution • **Legacy Entitlement Migration** - Tools for managing and migrating legacy license entitlements to the current licensing model **⚡ Advanced License Operations:** • **Trial License Requests** - Self-service trial license provisioning for evaluating Extreme platform capabilities • **NAC Entitlement Allocation** - Granular allocation of Network Access Control licenses across organizational units • **Credit Activation** - AI credit and service credit activation for consumption-based services **🏢 MSP & Enterprise Support:** Built for service providers and enterprises with multi-tenant license management, hierarchical entitlement distribution, and comprehensive audit trails for license compliance and governance.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/subscription/v1` — Extreme Platform ONE REST API - Subscriptions & Licensing

Full OpenAPI document: [`specs/subscription.json`](../../specs/subscription.json)

## Endpoints

20 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/setting` | Get License Settings |
| GET | `/license-types` | List License Types |
| GET | `/summary` | Get License Summary |
| POST | `/portal/link-url` | Get Portal Link URL |
| POST | `/portal/:unlink` | Unlink Portal Account |
| POST | `/portal/linkPartnerAccount` | Link Partner Portal Account |
| GET | `/license/apps` | List Licensed Applications |
| GET | `/entitlements` | List License Entitlements |
| GET | `/license-details` | List License Details |
| PUT | `/entitlements/{licenseKey}/note` | Update License Note |
| GET | `/license/report` | Download License Report |
| POST | `/license/:synchronize` | Synchronize Licenses |
| POST | `/trial-licenses/:request` | Request Trial Licenses |
| GET | `/nac-entitlements/allocations` | Get NAC Entitlement Allocations |
| PUT | `/nac-entitlements/allocations` | Set NAC Entitlement Allocations |
| GET | `/nac-entitlements/stats` | Get NAC Entitlement Statistics |
| POST | `/legacy-entitlements` | Add legacy entitlement |
| DELETE | `/legacy-entitlements/{id}` | Delete legacy entitlement |
| GET | `/enterprise-agreements/{eaContractNumber}` | Get Enterprise Agreement |
| GET | `/msp/entitlements` | List MSP License Entitlements |

## GET `/setting`

Operation: `getLicenseSetting`

Get License Settings

Retrieves the license settings for this account, including the default trial subscription period in days.

Tags: `Setting`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/license-types`

Operation: `listLicenseTypes`

List License Types

Retrieves the catalog of supported license types, optionally filtered by application. Returns license type metadata including names and descriptions for each license type.

Tags: `License Management`

Parameters:

- `app` query, optional (ClicsApplicationName) — The application name filter

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/summary`

Operation: `getLicenseSummary`

Get License Summary

Retrieves the shared CUID and legacy entitlements information, as well as portal link related information.

Tags: `License Management`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/portal/link-url`

Operation: `requestPortalLinkUrl`

Get Portal Link URL

Generates a link_url for initiating the ExtremeCloud IQ account linking process with an Extreme Portal account. The request body url field specifies the callback URL to redirect the user to after the linking process is complete. The user must use the link_url returned in the response to navigate to the Extreme Portal and authenticate, which initiates the account linking process.

Tags: `Link and Unlink`

Request body:

- `application/json` — ClicsPortalLinkRequestUrl

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/portal/:unlink`

Operation: `unlinkPortal`

Unlink Portal Account

Disconnects the ExtremeCloud IQ account from the linked Extreme Portal account. After unlinking, license synchronization will stop and you will need to re-link to access portal-based license management.

Tags: `Link and Unlink`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/portal/linkPartnerAccount`

Operation: `linkPartnerAccount`

Link Partner Portal Account

Establishes a connection between your ExtremeCloud IQ account and an Extreme Partner Portal account. This integration enables partners to manage customer licenses, access partner-specific pricing, and streamline license provisioning workflows.

Tags: `Link and Unlink`

Request body:

- `application/json` — ClicsLinkPartnerPortalAccountRequest

Responses:

- `200` — Link Extreme partner portal account response
- `400`
- `401`
- `403`
- `500`

## GET `/license/apps`

Operation: `getApps`

List Licensed Applications

Retrieves the list of current applications and their license status for the VIQ. Optionally filter by specific application IDs to retrieve targeted application information.

Tags: `License Management`

Parameters:

- `applicationIds` query, optional (array) — List of application names to filter by

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/entitlements`

Operation: `listEntitlements`

List License Entitlements

Retrieves license entitlements with optional filtering by application, keyword search, and quick filter options. Results can be grouped by application for organized viewing. Use simpleView to populate the license_details section for each license_type.

Tags: `License Management`

Parameters:

- `app` query, optional (ClicsApplicationName) — The application name filter
- `groupByApp` query, optional (boolean) — Whether group by app, if app is null, groupByApp will be false
- `keyword` query, optional (string) — The keyword to filter, will search the license type and license description
- `quickFilter` query, optional (ClicsLicenseQuickFilter) — Quick filter option
- `simpleView` query, optional (boolean) — Show simple view with license details without group by and quickfilter options

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/license-details`

Operation: `listLicenseDetails`

List License Details

Retrieves detailed information for licenses of a specific type, including individual license keys, activation dates, expiration dates, and current status. Use quickFilter to filter by health status (current, future, or expiring).

Tags: `License Management`

Parameters:

- `licenseType` query, required (string) — The license type identifier (product_feature name, not the display name). The correct value can be obtained from the license_type field in the listEntitlements response.
- `quickFilter` query, optional (ClicsLicenseQuickFilter) — Quick filter option
- `sharedCuid` query, optional (string) — Customer Unique Identifier used for MSP admin to view license details across multiple license accounts

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/entitlements/{licenseKey}/note`

Operation: `setLicenseEntitlementNote`

Update License Note

Updates or sets a custom note for a specific license entitlement. Notes can be used to track internal references, deployment locations, cost centers, or any other relevant metadata for license organization and management.

Tags: `License Management`

Parameters:

- `licenseKey` path, required (string) — The license key

Request body:

- `application/json` — ClicsSetLicenseEntitlementNotesRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/license/report`

Operation: `downloadLicenseReport`

Download License Report

Generates and downloads a license report as a ZIP file. Reports can be filtered by application, keyword, and license status. Useful for compliance auditing, capacity planning, and license inventory documentation.

Tags: `License Management`

Parameters:

- `app` query, optional (ClicsApplicationName) — The application name filter
- `groupByApp` query, optional (boolean) — Whether group by application, if app is null, groupByApp will be false
- `keyword` query, optional (string) — The keyword to filter, will search the license type and license description
- `quickFilter` query, optional (ClicsLicenseQuickFilter) — Quick filter option
- `sharedCuid` query, optional (string) — The shared Customer Unique Identifier (CUID) to filter licenses for a specific License Account

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/license/:synchronize`

Operation: `synchronizeLicense`

Synchronize Licenses

Triggers an on-demand synchronization of license information from Extreme Portal. Use this to refresh license data after purchasing new licenses or when license status appears out of date.

Tags: `License Management`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/trial-licenses/:request`

Operation: `requestTrialLicenses`

Request Trial Licenses

Submits a request for trial licenses to evaluate Extreme platform features. Trial licenses are time-limited and provide full functionality for the specified applications during the evaluation period.

Tags: `Trial License`

Request body:

- `application/json` — ClicsRequestTrialLicenseRequest

Responses:

- `200` — Trial license request submitted successfully. The trial period begins immediately and lasts for the configured number of trial days for the specified application.
- `400`
- `401`
- `403`
- `500`

## GET `/nac-entitlements/allocations`

Operation: `getNacEntitlementAllocations`

Get NAC Entitlement Allocations

Retrieves the current allocation of Network Access Control (NAC) license entitlements across organizational units. Shows how NAC licenses are distributed and consumed.

Tags: `Xiq`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/nac-entitlements/allocations`

Operation: `setNacEntitlementAllocations`

Set NAC Entitlement Allocations

Configures the allocation of Network Access Control (NAC) license entitlements across organizational units. Allows redistribution of NAC licenses based on organizational needs.

Tags: `Xiq`

Request body:

- `application/json` — array

Responses:

- `200` — NAC entitlement allocations have been successfully updated. The allocations are applied to the specified XIQ Site Engine appliances by serial number and percentage.
- `400`
- `401`
- `403`
- `500`

## GET `/nac-entitlements/stats`

Operation: `getNacEntitlementStats`

Get NAC Entitlement Statistics

Retrieves statistics for Network Access Control (NAC) license entitlements. Returns metrics of total number of NAC licenses and the number of available NAC licenses to help monitor NAC deployment and capacity planning.

Tags: `Xiq`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/legacy-entitlements`

Operation: `addLegacyEntitlement`

Add legacy entitlement

Adds a legacy entitlement key to the account. Legacy entitlement keys are no longer supported in ExtremeCloud IQ (XIQ) and Wireless Switching (WS) products. This endpoint is deprecated and will be removed in a future release. Please use the standard license activation workflow instead.

Tags: `Xiq`

Request body:

- `application/json` — ClicsAddLegacyEntitlementRequest

Responses:

- `201` — Created
- `400`
- `401`
- `403`
- `500`

## DELETE `/legacy-entitlements/{id}`

Operation: `deleteLegacyEntitlement`

Delete legacy entitlement

Removes a legacy entitlement from the account by its ID. Legacy entitlement keys are no longer supported in ExtremeCloud IQ (XIQ) and Wireless Switching (WS) products. This endpoint is deprecated and will be removed in a future release.

Tags: `Xiq`

Parameters:

- `id` path, required (integer) — The legacy entitlement ID

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/enterprise-agreements/{eaContractNumber}`

Operation: `getEnterpriseAgreement`

Get Enterprise Agreement

Retrieves enterprise agreement contract information with associated license types grouped by application from downstream service.

Tags: `License Management`

Parameters:

- `eaContractNumber` path, required (string) — The enterprise agreement contract number

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `404`
- `500`

## GET `/msp/entitlements`

Operation: `listMspEntitlements`

List MSP License Entitlements

Retrieves license entitlements for a specific MSP customer. Returns license details including types, quantities, expiration dates, and usage status. Supports filtering by application, keyword search, and quick filter options. This endpoint is deprecated - use the standard entitlements endpoint with MSP context instead.

Tags: `MSP License Management`

Parameters:

- `app` query, optional (ClicsApplicationName) — The application name filter
- `groupByApp` query, optional (boolean) — Whether group by app, if app is null, groupByApp will be false
- `keyword` query, optional (string) — The keyword to filter, will search the license type and license description
- `quickFilter` query, optional (ClicsLicenseQuickFilter) — Quick filter option
- `cuid` query, required (string) — Customer Unique Identifier

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

