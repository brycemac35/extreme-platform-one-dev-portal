---
source: https://developer.extremeplatformone.com/api-reference/asset
spec: https://developer.extremeplatformone.com/api/spec/asset
title: "Extreme Platform ONE REST API - Asset Management"
---

# Extreme Platform ONE REST API - Asset Management

**Asset** · Services. Inventory and Assets.

The Extreme Platform ONE™ Asset Management API provides comprehensive automation and intelligent orchestration for enterprise network asset lifecycle management, enabling seamless device inventory tracking, contract management, and automated compliance monitoring across complex network infrastructures.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/assets/v1` — Extreme Platform ONE REST API - Assets

Full OpenAPI document: [`specs/asset.json`](../../specs/asset.json)

## Endpoints

23 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/devices` | List Devices |
| POST | `/devices/export` | Export Devices List |
| GET | `/devices/licenses` | Get License Information |
| POST | `/devices/column/filters` | List filters for columns |
| GET | `/devices/subscriptions/unmanaged` | Get count of UNMANAGED devices |
| POST | `/devices/productTypes` | Get Product Types |
| POST | `/devices/firmwareMetadatas` | Get Device Firmware Metadatas |
| GET | `/devices/status/count` | Get Device Status Count |
| POST | `/devices/licenseCount` | Get License Count Per Location |
| POST | `/contracts` | List Filtered Contracts |
| GET | `/contracts/export` | Export Contracts (Deprecated) |
| POST | `/contracts/export` | Export Contracts with filters |
| GET | `/contracts/{contract_id}/lines` | List Contract Lines |
| GET | `/contracts/{contract_id}/export` | Export Contract with Lines |
| GET | `/contracts/filter` | Get Contract Filters |
| POST | `/summary/firmwareStatus` | Get Firmware Status Count (Deprecated) |
| POST | `/summary/firmwareSummary` | Get Firmware Summary (Deprecated) |
| POST | `/summary/firmwareUpgrade` | Initiate Firmware Upgrade (Deprecated) |
| POST | `/summary/firmwareVersions` | Get Firmware Versions (Deprecated) |
| POST | `/summary/hardwareLifeCycle` | Get Hardware Lifecycle Summary |
| POST | `/summary/history` | Get Device History (Deprecated) |
| POST | `/summary/history/column/filters` | Get History Column Filters (Deprecated) |
| POST | `/summary/psirts/list` | List PSIRTs (Deprecated) |

## POST `/devices`

Operation: `listDevices`

List Devices

List devices with pagination, sorting, search and optional filters. The request body accepts **one of two mutually exclusive forms**: **1. Filter by device IDs** — provide only `device_ids` (1–100 items). No other fields may be present. The response contains exactly the devices matching the supplied IDs. **2. Filter by device attributes** — provide any combination of fields from `ListDevicesRequestFilter` (e.g. `classification`, `states`, `connection_states`, `site_ids`, etc.) exactly as before. All existing filter behaviour is unchanged. **Notes on specific fields:** - `switch_type` and `appliance_type` are **mutually exclusive** — they are combined with AND, so sending both in the same request returns no results. Use one or the other. - `column_list` applies only to the device list **export (CSV)** endpoint and is **ignored** by this List Devices endpoint.

Tags: `Device`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional

Request body:

- `application/json` — ListDevicesRequestBody

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/devices/export`

Operation: `exportAssetsDeviceList`

Export Devices List

Export the filtered devices list data in CSV format.

Tags: `Device`

Parameters:

- `search` query, optional (string) — Search string to be used as a parameter for searching
- `sort` query, optional (string) — Sort string in the format of "field:direction", e.g. "host_name-" or "ip_address+"

Request body:

- `application/json` — ListDevicesRequestFilter

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/devices/licenses`

Operation: `getLicenseInfo`

Get License Information

Get information about licenses.

Tags: `Device`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/devices/column/filters`

Operation: `listColumnFilters`

List filters for columns

List all filter values for each column.

Tags: `Device`

Request body:

- `application/json` — ColumnFiltersRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/devices/subscriptions/unmanaged`

Operation: `getUnmanagedDevicesCount`

Get count of UNMANAGED devices

Get count of UNMANAGED devices for each Device Type.

Tags: `Device`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/devices/productTypes`

Operation: `getProductTypes`

Get Product Types

Retrieve product types information filtered by OS types.

Tags: `Device`

Request body:

- `application/json` — ProductTypesRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/devices/firmwareMetadatas`

Operation: `getDeviceFirmwareMetadatas`

Get Device Firmware Metadatas

Retrieve compatible firmware metadata for specified product types and firmware types.

Tags: `Device`

Request body:

- `application/json` — FirmwareMetadatasRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/devices/status/count`

Operation: `getDeviceStatusCount`

Get Device Status Count

Retrieve count of devices grouped by their connection status.

Tags: `Device`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/devices/licenseCount`

Operation: `licenseCount`

Get License Count Per Location

Retrieve license count per location information for devices in the inventory.

Tags: `Device`

Parameters:

- `licenseTypes` query, optional (array) — Filter on specific license types to include in the count results. Provide one or more license types (e.g., PILOT, LEGACY) to limit the counts to those types.

Request body:

- `application/json` — LicenseInfoFilter

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/contracts`

Operation: `listContracts`

List Filtered Contracts

List contracts with pagination, sorting and filtering options.

Tags: `Contract`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional

Request body:

- `application/json` — ContractFilter

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/contracts/export`

Operation: `exportContracts`

Export Contracts (Deprecated)

Deprecated. Use POST /assets/v1/contracts/export instead, which supports full filter options. This endpoint will be removed in a future release.

Tags: `Contract`

Parameters:

- `contract_id` query, optional (array) — Comma-separated list of contract IDs. If not provided, all contracts will be exported.

Responses:

- `200` — Excel file.
- `400`
- `401`
- `403`
- `500`

## POST `/contracts/export`

Operation: `exportContractsPost`

Export Contracts with filters

Export contracts to Excel format with optional filters.

Tags: `Contract`

Parameters:

- `contract_id` query, optional (string) — Comma-separated list of contract IDs. If not provided, all contracts will be exported.
- `contract_end_in_days` query, optional (integer) — Filter contracts ending within the specified number of days from today

Request body:

- `application/json` — ContractFilter

Responses:

- `200` — Excel file.
- `400`
- `401`
- `403`
- `500`

## GET `/contracts/{contract_id}/lines`

Operation: `listContractLines`

List Contract Lines

List contract lines by pagination.

Tags: `Contract`

Parameters:

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

## GET `/contracts/{contract_id}/export`

Operation: `exportContractWithLines`

Export Contract with Lines

Export a specific contract along with its lines to Excel format.

Tags: `Contract`

Parameters:

- `None` , optional

Responses:

- `200` — Returns an Excel file containing contract and line items data.
- `400` — Bad Request
- `401`
- `500`

## GET `/contracts/filter`

Operation: `getContractFilters`

Get Contract Filters

Retrieve available contract filters for querying contracts.

Tags: `Contract`

Responses:

- `200` — OK
- `400` — Bad Request
- `401`
- `403`
- `500`

## POST `/summary/firmwareStatus`

Operation: `getFirmwareStatusCount`

Get Firmware Status Count (Deprecated)

Retrieves firmware status count information for devices. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use POST /v1/devices/firmware:status instead.

Tags: `Summary`

Request body:

- `application/json` — DeviceClassificationAndSiteFilter

Responses:

- `200` — Firmware status count retrieved successfully
- `400`
- `401`
- `403`
- `500`

## POST `/summary/firmwareSummary`

Operation: `getFirmwareSummary`

Get Firmware Summary (Deprecated)

Retrieves firmware summary information with pagination support. This endpoint provides details about firmware summary for devices in the inventory. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use POST /v1/devices/firmware:summary instead.

Tags: `Summary`

Parameters:

- `page` query, optional (integer) — Page number for pagination.
- `limit` query, optional (integer) — Number of items per page.

Request body:

- `application/json` — DeviceFwSummaryRequestFilter

Responses:

- `200` — The firmware summary response
- `400`
- `401`
- `403`
- `500`

## POST `/summary/firmwareUpgrade`

Operation: `getFirmwareSummaryUpgrade`

Initiate Firmware Upgrade (Deprecated)

Initiates firmware upgrade process for devices based on filter criteria. This endpoint allows scheduling or immediate execution of firmware upgrades. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use POST /v1/devices/firmware:upgrade instead.

Tags: `Summary`

Request body:

- `application/json` — DeviceFwUpgradeRequestFilter

Responses:

- `200` — Firmware upgrade initiated successfully.
- `400`
- `401`
- `409`
- `500`

## POST `/summary/firmwareVersions`

Operation: `getFirmwareVersions`

Get Firmware Versions (Deprecated)

Retrieves firmware versions information with pagination and filtering support. This endpoint provides details about firmware versions for devices in the inventory. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use POST /v1/devices/firmware:versions instead.

Tags: `Summary`

Parameters:

- `page` query, optional (integer) — Page number for pagination.
- `limit` query, optional (integer) — Number of items per page.
- `sort` query, optional (string) — Sorting criteria in the format field:direction where direction is asc or desc . Common sortable fields for this endpoint include model and version (for example: model:asc , version:desc ).

Request body:

- `application/json` — DeviceFirmwareRequestFilter

Responses:

- `200` — The firmware versions response
- `400`
- `401`
- `403`
- `500`

## POST `/summary/hardwareLifeCycle`

Operation: `getHardwareSummary`

Get Hardware Lifecycle Summary

Retrieves hardware lifecycle summary information for devices in the inventory. This endpoint provides details about the lifecycle stages of hardware devices.

Tags: `Summary`

Request body:

- `application/json` — DeviceClassificationAndSiteFilter

Responses:

- `200` — The hardware lifecycle summary response
- `400`
- `401`
- `403`
- `500`

## POST `/summary/history`

Operation: `listDeviceHistory`

Get Device History (Deprecated)

Retrieves device history with pagination, sorting, and search capabilities. This endpoint provides historical data for device firmware upgrades. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. History will be shown in Task Center instead.

Tags: `Summary`

Parameters:

- `page` query, optional (integer) — Page number for pagination (1-based indexing).
- `limit` query, optional (integer) — Number of records per page.
- `sort` query, optional (string) — Comma-separated list of fields to sort by. Each field can be optionally suffixed with `+` (ascending) or `-` (descending). If no suffix is provided, ascending order is used by default.
- `search` query, optional (string) — Search keyword to filter device history (minimum 3 characters, supports alphanumeric and special characters)

Request body:

- `application/json` — ListDeviceHistoryFilter

Responses:

- `200` — The device history response
- `400`
- `401`
- `403`
- `500`

## POST `/summary/history/column/filters`

Operation: `listHistoryColumnFilters`

Get History Column Filters (Deprecated)

Retrieves available filter options for device history columns. This endpoint provides unique values for each column in the device history table. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. History will be shown in Task Center instead.

Tags: `Summary`

Request body:

- `application/json` — DeviceHistoryRequestFilter

Responses:

- `200` — The history column filters response
- `400`
- `401`
- `403`
- `500`

## POST `/summary/psirts/list`

Operation: `psirtsList`

List PSIRTs (Deprecated)

Retrieves a paginated list of Product Security Incident Response Team (PSIRT) entries. This endpoint provides details about PSIRTs for devices in the inventory. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release.

Tags: `Summary`

Parameters:

- `page` query, optional (integer) — Page number for pagination.
- `limit` query, optional (integer) — Number of items per page.

Request body:

- `application/json` — PsirtsFilter

Responses:

- `200` — The PSIRTs list response
- `400`
- `401`
- `403`
- `500`

