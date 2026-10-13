---
source: https://developer.extremeplatformone.com/api-reference/msp
spec: https://developer.extremeplatformone.com/api/spec/msp
title: "ExtremeCloud MSP Workspace API"
---

# ExtremeCloud MSP Workspace API

**MSP** · Applications. Managed Service Provider.

The **ExtremeCloud MSP Workspace API** enables Managed Service Providers (MSPs) to programmatically manage their tenant portfolio, licenses, network devices, users, and more. ## Authentication All endpoints require a valid **Bearer JWT token**. ### How to obtain an IAM access token **Option 1 — API Keys (recommended for automation)** 1. Log in to **Extreme Platform ONE** 2. Navigate to **Integrations → API Keys** 3. Generate a new API key — this is your IAM access token **Option 2 — Browser developer tools (for quick testing)** 1. Log in to **Extreme Platform ONE** in your browser 2. Open the browser **Developer Tools** (F12 or right-click → Inspect) 3. Go to the **Network** tab and look at any authenticated request 4. Copy the `Authorization: Bearer ` value from the request headers Include the token in every request: ``` Authorization: Bearer ``` ## Data Isolation All data is scoped to the authenticated MSP admin's **home account**. Cross-account access is not permitted. ## Support For API access or integration questions, contact [support@extremenetworks.com](mailto:support@extremenetworks.com).

Version: `2.11`

## Servers

- `https://cloudapi.extremecloudiq.com/msp/v1` — Extreme Platform ONE REST API - MSP

Full OpenAPI document: [`specs/msp.json`](../../specs/msp.json)

## Endpoints

13 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/msp-login-workflow` | Initiate MSP login workflow |
| POST | `/customer/v2/add` | Create a customer |
| GET | `/admingroups` | List admin groups |
| PATCH | `/customer/v2/edit/{customerOwnerId}` | Edit a customer |
| GET | `/licenses-added-to-msp` | Get linked licenses for the MSP |
| GET | `/license/name-for-customers` | Get assigned license name of given customer accountIDs |
| GET | `/license/customer-info` | Get License Info for an MSP |
| GET | `/deployments/datacenters` | Get available data centers |
| GET | `/customers/v2` | Get customer accounts v2 |
| GET | `/customers/list` | Get list of all available customers for MSP admin |
| GET | `/billing/monthly` | Get monthly billing usage |
| GET | `/billing/daily` | Get daily billing usage |
| DELETE | `/customer/delete/{customerOwnerId}` | Delete a customer |

## POST `/msp-login-workflow`

Operation: `iamLoginWorkflow`

Initiate MSP login workflow

Validates the MSP admin's ExtremeCloud IAM access token and initialises their MSP workspace session. This endpoint must be called once per session before accessing any other MSP API endpoints. The IAM access token must be provided as a Bearer token in the Authorization header.

Tags: `MSP Login Workflow`

Responses:

- `200` — Login workflow completed successfully — MSP session is active
- `400` — Bad request — missing or malformed Authorization header
- `401` — Unauthorized — IAM token is invalid, expired, or does not belong to an MSP admin
- `500` — Internal server error — MSP session initialisation failed

## POST `/customer/v2/add`

Operation: `createCustomerV2`

Create a customer

Creates a new customer account under the authenticated MSP admin's home account. Admin groups and a license account can be assigned to the customer as part of the creation request. Returns 206 Partial Content when the customer was created but one or more optional assignments (e.g. license, team) failed.

Tags: `Customer Management`

Request body:

- `application/json` — CreateCustomerV2Request

Responses:

- `200` — Successful operation
- `206` — Partial content
- `400` — Bad Request
- `401` — Unauthorized
- `424` — Failed dependency
- `500` — Internal Server Error

## GET `/admingroups`

Operation: `listUserGroups`

List admin groups

List all admin groups (user teams) created within the MSP workspace, including group names and member counts.

Tags: `Admin Group Management`

Responses:

- `200` — OK
- `400` — Bad Request
- `401` — Unauthorized
- `500` — Internal Server Error

## PATCH `/customer/v2/edit/{customerOwnerId}`

Operation: `editCustomerV2`

Edit a customer

Updates the specified customer account. Supported operations include adding or removing admin group access to the customer, and linking or unlinking a license account. Returns 206 Partial Content when some requested changes succeeded but others failed.

Tags: `Customer Management`

Parameters:

- `customerOwnerId` path, required (integer) — Owner ID of the customer account to edit

Request body:

- `application/json` — EditCustomerV2Request

Responses:

- `200` — Successful operation
- `206` — Partial content
- `400` — Bad Request
- `401` — Unauthorized
- `424` — Failed dependency
- `500` — Internal Server Error

## GET `/licenses-added-to-msp`

Operation: `getLicensesAddedToMsp`

Get linked licenses for the MSP

Returns the list of Extreme license accounts that have been linked (fully pairing-confirmed) to the authenticated MSP home account. Linked accounts have completed the full OAuth + Internal IT System linking flow and are eligible to be assigned to customers.

Tags: `License management - MSP`

Responses:

- `200` — OK
- `400` — Bad request
- `401` — Unauthorized
- `500` — Internal Server Error

## GET `/license/name-for-customers`

Operation: `getSoftlinkLicenseNameFromDB`

Get assigned license name of given customer accountIDs

Look up the softlinked license account name for one or more tenant account IDs. Returns the license name associated with each account via the soft-link relationship.

Tags: `License management - MSP`

Parameters:

- `accountIds` query, optional (string) — Account IDs

Responses:

- `200` — OK
- `400` — Bad request
- `401` — Unauthorized
- `500` — Internal Server Error

## GET `/license/customer-info`

Operation: `getLicenseInfo`

Get License Info for an MSP

Returns license customer information for the MSP's linked Extreme license accounts. Results can be filtered by license account name and/or product line: - `isSdwan=true` — include only SD-WAN license entries - `isUz=true` — include only UZTNA (Zero Trust Network Access) license entries - `search` — free-text search applied across all returned fields (account name, status, etc.) Omit all filters to retrieve the full license picture for the authenticated MSP home account.

Tags: `License management - MSP`

Parameters:

- `licenseAccountName` query, optional (string) — The license account name
- `isSdwan` query, optional (string) — isSdwan
- `isUz` query, optional (string) — isUz
- `search` query, optional (string) — General search in all fields

Responses:

- `200` — OK
- `400` — Bad request
- `401` — Unauthorized
- `500` — Internal Server Error

## GET `/deployments/datacenters`

Operation: `getDataCenters`

Get available data centers

Retrieves the list of available Regional Data Centers (RDCs) for creating tenant instances. Results can be filtered by SD-WAN or ZTNA capability. This endpoint is scoped to the authenticated MSP admin's home account.

Tags: `Deployed - Data Centers`

Parameters:

- `isSdwan` query, optional (string) — Whether to get list of SD-WAN enabled data centers.
- `isZtna` query, optional (string) — Whether to get list of ZTNA-enabled data centers.

Responses:

- `200` — Successfully retrieved the list of data centers
- `400` — Bad Request — invalid parameter value
- `401` — Unauthorized — missing or invalid Bearer token
- `500` — Internal Server Error

## GET `/customers/v2`

Operation: `getUserAccountsV2`

Get customer accounts v2

Get customer accounts with filter and pagination

Tags: `Customer`

Parameters:

- `id` query, optional (integer) — Filter by Account Id. Special case: when set, this account is always included via an OR match, bypassing the `ids` and `subAttributeIds` filters for this single account.
- `ids` query, optional (array) — Filter by Account Ids
- `name` query, optional (string) — Filter by Account Name
- `subAttributeIds` query, optional (array) — Filter to tenants that have ALL of the given Tenant Tag (sub-attribute) IDs assigned. Does not apply to the account matched by `id`, which is always included regardless of this filter.
- `page` query, optional (integer) — Zero-based page index (0..N)
- `size` query, optional (integer) — The size of the page to be returned
- `sort` query, optional (array) — Sorting criteria in the format: property,(asc|desc). Default sort order is ascending. Multiple sort criteria are supported.

Responses:

- `200` — OK
- `400` — Bad Request
- `401` — Unauthorized
- `500` — Internal Server Error

## GET `/customers/list`

Operation: `getCustomerList`

Get list of all available customers for MSP admin

Returns the full list of customer accounts visible to the authenticated MSP admin, optionally filtered by editability. Results are scoped to the MSP admin's home account — customers belonging to other MSPs are not returned.

Tags: `Customer`

Parameters:

- `isEditable` query, optional (boolean) — When true, returns only customers that the admin has permission to edit. When false or omitted, returns all visible customers.

Responses:

- `200` — Successful operation
- `400` — Bad request — invalid or missing query parameters
- `401` — Unauthorized — missing or invalid Bearer token
- `500` — Internal server error

## GET `/billing/monthly`

Operation: `getMonthlyUsage`

Get monthly billing usage

Returns aggregated monthly billing usage data for the MSP's license account. Supports filtering by date range (month granularity), tenant account, and license feature group or sub-group. This endpoint is scoped to the authenticated MSP admin's home account. Data from other accounts is not accessible.

Tags: `Billing [Beta]`

Parameters:

- `licenseAccountName` query, required (string) — License account name
- `startDate` query, required (string) — Invoice creation date range - From Date(mm/dd/yyyy)
- `endDate` query, required (string) — Invoice creation date range - To Date(mm/dd/yyyy)
- `accountId` query, optional (integer) — Filtering by Tenant
- `featureGroup` query, optional (string) — Filtering by License Feature Group or Subgroup

Responses:

- `200` — Successful operation — returns monthly usage records
- `400` — Bad request — missing or invalid query parameters
- `401` — Unauthorized — missing or invalid Bearer token
- `500` — Internal server error

## GET `/billing/daily`

Operation: `getDailyUsage`

Get daily billing usage

Returns day-level billing usage data for the MSP's license account. Supports filtering by date range (day granularity), tenant account, and license feature group or sub-group. This endpoint is scoped to the authenticated MSP admin's home account. Data from other accounts is not accessible.

Tags: `Billing [Beta]`

Parameters:

- `licenseAccountName` query, required (string) — License account name
- `startDate` query, required (string) — Usage date range - From Date(mm/dd/yyyy)
- `endDate` query, required (string) — Usage date range - To Date(mm/dd/yyyy)
- `accountId` query, optional (integer) — Filtering by Tenant
- `featureGroup` query, optional (string) — Filtering by License Feature Group or Subgroup

Responses:

- `200` — Successful operation — returns daily usage records
- `400` — Bad request — missing or invalid query parameters
- `401` — Unauthorized — missing or invalid Bearer token
- `500` — Internal server error

## DELETE `/customer/delete/{customerOwnerId}`

Operation: `deleteCustomer`

Delete a customer

Marks the specified customer account as inactive (pending deletion). This is a soft-delete operation — the customer record is deactivated rather than permanently removed. Additional steps by the CloudOps team are required to fully remove the underlying customer account. The MSP admin cannot delete their own home account.

Tags: `Customer Management`

Parameters:

- `customerOwnerId` path, required (integer) — Owner ID of the customer account to delete

Responses:

- `200` — Successful operation
- `400` — Bad Request
- `401` — Unauthorized
- `406` — Not Acceptable operation
- `424` — Failed dependency
- `500` — Internal Server Error

