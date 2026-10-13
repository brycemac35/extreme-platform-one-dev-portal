---
source: https://developer.extremeplatformone.com/api-reference/pcs
spec: https://developer.extremeplatformone.com/api/spec/pcs
title: "Extreme Platform ONE REST API - Client"
---

# Extreme Platform ONE REST API - Client

**Client** · Services. Wireless Clients and Wired Clients.

Platform Client Service (PCS) API provides client cache details and wireless/wired client health grid information.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/client/v1` — Extreme Platform ONE REST API - Client

Full OpenAPI document: [`specs/pcs.json`](../../specs/pcs.json)

## Endpoints

15 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/wireless/details/{client_uuid}` | Get Wireless Client Details Info |
| GET | `/wired/details/{client_uuid}` | Get Wired Client Details Info |
| POST | `/wired` | Wired client data |
| POST | `/wired/grid` | Wired client health grid |
| POST | `/wireless` | Wireless client data |
| POST | `/wireless/grid` | Wireless client health grid |
| POST | `/mac-lookup` | Lookup clients by MAC addresses |
| GET | `/devices/{device_id}/monitor/ipv4-routing` | Get device IPv4 routing information |
| POST | `/wired/health-filter-metadata` | Wired client health filter metadata |
| POST | `/rtts-support` | Check RTTS support for multiple clients |
| GET | `/gdpr/all` | List GDPR audit log entries |
| GET | `/gdpr/all/download` | Download GDPR audit log entries as CSV |
| POST | `/gdpr/clients/report` | Generate GDPR reports for one or more clients |
| POST | `/gdpr/clients/delete` | Delete GDPR client data for one or more clients |
| GET | `/gdpr/client/download` | Download a GDPR client report file |

## GET `/wireless/details/{client_uuid}`

Operation: `getWirelessClientDetailsInfo`

Get Wireless Client Details Info

Retrieves detailed information about a wireless client using the client UUID from the grid response.

Tags: `Client Details`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/wired/details/{client_uuid}`

Operation: `getWiredClientDetailsInfo`

Get Wired Client Details Info

Retrieves detailed information about a wired client using the client UUID from the grid response.

Tags: `Client Details`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/wired`

Operation: `getWiredClientData`

Wired client data

Returns the client data of Wired devices based on the provided filters.

Tags: `Dashboard`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `connection_status` query, optional (string) — Connection Status
- `sort_field` query, optional (string) — Sort Field
- `None` , optional

Request body:

- `application/json` — WiredClientHealthGridRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/wired/grid`

Operation: `getWiredClientHealthGrid`

Wired client health grid

Returns the client health grid of Wired devices based on the provided filters.

Tags: `Dashboard`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `connection_status` query, optional (string) — Connection Status
- `sort_field` query, optional (string) — Sort Field
- `None` , optional

Request body:

- `application/json` — WiredClientHealthGridRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/wireless`

Operation: `getWirelessClientData`

Wireless client data

Returns the client data of Wireless devices based on the provided filters.

Tags: `Dashboard`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `connection_status` query, optional (string) — Connection Status
- `include_unassigned` query, optional (boolean) — Whether to include unassigned devices
- `sort_field` query, optional (string) — Sort Field
- `None` , optional

Request body:

- `application/json` — WirelessClientHealthGridRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/wireless/grid`

Operation: `getWirelessClientHealthGrid`

Wireless client health grid

Returns the client health grid of Wireless devices based on the provided filters.

Tags: `Dashboard`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `connection_status` query, optional (string) — Connection Status
- `include_unassigned` query, optional (boolean) — Whether to include unassigned devices
- `sort_field` query, optional (string) — Sort Field
- `None` , optional

Request body:

- `application/json` — WirelessClientHealthGridRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/mac-lookup`

Operation: `lookupClientsByMacAddress`

Lookup clients by MAC addresses

Lookup and retrieve basic client information based on a list of MAC addresses (max 100). It support both wired and wireless clients.

Tags: `Client Details`

Request body:

- `application/json` — ClientMacLookupRequest

Responses:

- `200` — Successfully retrieved client information
- `400`
- `401`
- `403`
- `500`

## GET `/devices/{device_id}/monitor/ipv4-routing`

Operation: `getDeviceIpv4Routing`

Get device IPv4 routing information

Retrieves IPv4 routing information for a specific device with pagination support. Returns routing details including destination, VLAN information, route origin, status, metrics, next hop details, and ping protection settings.

Tags: `Routing Details`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `sort_field` query, optional (string) — Sort Field
- `None` , optional

Responses:

- `200` — Successfully retrieved device IPv4 routing information
- `400`
- `401`
- `403`
- `404`
- `500`

## POST `/wired/health-filter-metadata`

Operation: `getWiredClientHealthFilterMetadata`

Wired client health filter metadata

Returns the client health filter metadata of Wired devices.

Tags: `Dashboard`

Request body:

- `application/json` — WiredClientHealthFilterMetadataRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/rtts-support`

Operation: `checkRttsSupport`

Check RTTS support for multiple clients

Checks if Route Table Tracking Support (RTTS) is supported for a list of clients. Takes client details including clientId, deviceId, and connectionStatus, and returns whether RTTS is supported for each client. Maximum 500 clients can be validated in a single request.

Tags: `Client Details`

Request body:

- `application/json` — RttsSupportRequest

Responses:

- `200` — Successfully checked RTTS support for all clients
- `400`
- `401`
- `403`
- `404`
- `500`

## GET `/gdpr/all`

Operation: `getGdprLogs`

List GDPR audit log entries

Returns a paginated, optionally sorted and filtered list of GDPR audit-log entries for the caller's tenant.

Tags: `GDPR`

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

Responses:

- `200` — Successfully retrieved the GDPR audit log page
- `400` — Invalid sort/order/time-range parameters
- `401` — Missing or invalid IAM access token
- `500` — Unexpected server error

## GET `/gdpr/all/download`

Operation: `downloadGdprLogsCsv`

Download GDPR audit log entries as CSV

Exports GDPR audit-log entries matching the given search/filter/sort criteria as a downloadable CSV file.

Tags: `GDPR`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional

Responses:

- `200` — CSV file containing the matching GDPR audit log entries
- `400` — Invalid sort/order/time-range/timeZone parameters
- `401` — Missing or invalid IAM access token
- `500` — Unexpected server error

## POST `/gdpr/clients/report`

Operation: `generateClientReports`

Generate GDPR reports for one or more clients

Generates a GDPR report for one or more clients identified by MAC address.

Tags: `GDPR`

Request body:

- `application/json` — BulkClientIdsRequest

Responses:

- `200` — All resolved clients have been processed
- `400` — clientMacs is empty or exceeds the configured maximum
- `401` — Missing or invalid IAM access token
- `500` — Unexpected server error

## POST `/gdpr/clients/delete`

Operation: `deleteClients`

Delete GDPR client data for one or more clients

Deletes client data for GDPR compliance for one or more clients identified by MAC address.

Tags: `GDPR`

Request body:

- `application/json` — BulkClientIdsRequest

Responses:

- `200` — All resolved clients have been processed
- `400` — clientMacs is empty or exceeds the configured maximum
- `401` — Missing or invalid IAM access token
- `500` — Unexpected server error

## GET `/gdpr/client/download`

Operation: `downloadGdprClientFile`

Download a GDPR client report file

Downloads the GDPR report file for a single client identified by its MAC address; since a client can have more than one report, `logID` identifies which one to download.

Tags: `GDPR`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — The GDPR client report file
- `400` — clientMac is missing or blank
- `401` — Missing or invalid IAM access token
- `404` — clientMac could not be resolved to a client id
- `500` — Unexpected server error, or the file was not found upstream

