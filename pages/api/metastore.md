---
source: https://developer.extremeplatformone.com/api-reference/metastore
spec: https://developer.extremeplatformone.com/api/spec/metastore
title: "MetaStore Event API"
---

# MetaStore Event API

**MetaStore** · Services. Network Device Events and Monitoring Data.

## Overview MetaStore is the event ingestion and query service for the ExtremeCloud platform. It stores enriched network device events that flow through the MetaFlow telemetry pipeline (devices → Kafka → MetaFlow enrichment → ClickHouse) and exposes them via this REST API. Events originate from **access points, switches, routers, and security devices**. Each event carries device identity, location context (site/building/floor), severity, and an `element_data` payload whose fields are event-type-specific. ## Intended Consumers This API is designed for both human operators and **AI agents / MCP tool hosts**. AI agents should follow this workflow: 1. **Discover** — Call `GET /catalog` to understand data range and available dimensions. 2. **Identify devices** — If you have a device name but not an ID, call `GET /catalog/devices`. 3. **Understand event types** — Call `GET /events/types` to list known event names, then `GET /catalog/event-schema/{event_name}` to understand `element_data` fields. 4. **Aggregate first** — Use `GET /events/summary` or `GET /events/trends` to answer counting/trending questions efficiently before paging through raw events. 5. **Query raw events** — Use `GET /events` only when you need individual event records. ## MCP Integration `GET /mcp/manifest` returns a machine-readable tool manifest that MCP-compatible hosts can use to auto-register this service as a tool provider.

Version: `25.13.0`

## Servers

- `https://cloudapi.extremecloudiq.com/metastore/v1` — Extreme Platform ONE REST API - MetaStore

Full OpenAPI document: [`specs/metastore.json`](../../specs/metastore.json)

## Endpoints

12 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/events` | Query network device events with filtering, pagination, and flexible payload format |
| GET | `/events/types` | List available event types |
| GET | `/events/severities` | List available severity levels |
| GET | `/events/{id}` | Get event by ID |
| GET | `/events/summary` | Summarize events by dimension |
| GET | `/events/trends` | Get event trends over time |
| GET | `/catalog` | Get service catalog overview |
| GET | `/catalog/devices` | Discover devices with event activity |
| GET | `/catalog/event-schema/{event_name}` | Get element_data schema for an event type |
| GET | `/mcp/manifest` | MCP tool manifest |
| GET | `/health` | Health check |
| GET | `/ready` | Readiness check |

## GET `/events`

Operation: `getEvents`

Query network device events with filtering, pagination, and flexible payload format

Retrieve a paginated list of network device events with optional filtering. This endpoint serves **all event types** ingested by MetaStore, including but not limited to: FanStateChange, PsuStateChange, InterfaceStateChange, IsisAdjacencyStateChange, LagMembersEvent, LinkFlapDetectEvent, MlagPeerStateChange, SshLoginFail, RebootEvent, SaveConfigEvent, CoreFileCreated, DeviceConnected, and many more. Call `GET /events/types` for the complete, authoritative list of event types available in the current deployment. **Supported event categories:** - **Hardware health:** FanStateChange, PsuStateChange, CoreFileCreated - **Interface/port:** InterfaceStateChange, LinkFlapDetectEvent, ChannelizedPortStateChange - **Routing protocols:** IsisAdjacencyStateChange, OspfNeighborStateChange, MlagPeerStateChange - **Security:** SshLoginFail, AuthenticationStateChange, MacLockingViolationEvent - **System lifecycle:** RebootEvent, SaveConfigEvent, UpgradeEvent - **Wireless:** RadioStateChange, AfcRadioStateChange, HMChannelPowerChangeEvent **Filter behaviour:** - All query parameters apply with AND semantics. - Multi-value parameters use **comma-separated format** (OpenAPI `style: form, explode: false`), e.g. `?severities=Critical,Error` or `?device_ids=1001,1002,1003`. This format is intentional for URL brevity and ClickHouse query compatibility. Generated clients should serialize arrays with comma separation, not repeated keys. - Invalid filter values return HTTP 400 with a descriptive error…

Tags: `events`

Parameters:

- `event_names` query, optional (array) — Event type names to filter by. Use GET /events/types to discover valid values.
- `severities` query, optional (array) — Severity levels to filter by.
- `device_ids` query, optional (array) — Numeric device IDs to filter by. Use GET /catalog/devices to resolve a hostname to a device_id. Returns 400 if any value is not a valid integer.
- `serial_numbers` query, optional (array) — Device serial numbers to filter by.
- `product_types` query, optional (array) — Device product categories to filter by.
- `device_functions` query, optional (array) — Device role filters.
- `owner_ids` query, optional (array) — Owner/tenant IDs to scope results. When IAM token owner scope is present, this must be a subset of token owner_ids; if omitted, token owner scope is applied automatically. Returns 400 if any value is not a valid integer.
- `start_time` query, optional (string) — Start of the time range (RFC3339 format, e.g. 2026-05-01T00:00:00Z)
- `end_time` query, optional (string) — End of the time range (RFC3339 format, e.g. 2026-05-07T23:59:59Z)
- `limit` query, optional (integer) — Maximum events to return (1–10000, default 100)
- `offset` query, optional (integer) — Events to skip for pagination (default 0)
- `order_by` query, optional (string) — Field to sort results by
- `order_dir` query, optional (string) — Sort direction
- `download` query, optional (string) — Set to "csv" to receive results as a CSV file download instead of JSON
- `payloadFormat` query, optional (string) — Format for element_data and raw_data fields. Case-insensitive. - **String** (default): Returns element_data and raw_data as JSON strings (backward compatible) - **Object**: Returns element_data and raw_data as parsed JSON objects (for AI…

Responses:

- `200` — Events matching the query
- `400`
- `500`

## GET `/events/types`

Operation: `getEventTypes`

List available event types

Returns all distinct event type names currently stored in the system.

Tags: `events`

Responses:

- `200` — List of event type names
- `500`

## GET `/events/severities`

Operation: `getSeverityLevels`

List available severity levels

Returns all distinct severity levels present in stored events, ordered from most to least critical.

Tags: `events`

Responses:

- `200` — Severity levels
- `500`

## GET `/events/{id}`

Operation: `getEventById`

Get event by ID

Retrieve a single event record by its unique ID.

Tags: `events`

Parameters:

- `id` path, required (string) — Unique event identifier
- `payloadFormat` query, optional (string) — Format for element_data and raw_data fields. Case-insensitive. - **String** (default): Returns element_data and raw_data as JSON strings (backward compatible) - **Object**: Returns element_data and raw_data as parsed JSON objects (for AI…

Responses:

- `200` — The requested event wrapped in an envelope object
- `400`
- `404`
- `500`

## GET `/events/summary`

Operation: `getEventSummary`

Summarize events by dimension

Returns event counts grouped by a specified dimension, ordered by count descending. **Supported group_by values:** | Value | Groups by | |---|---| | `severity` | Critical / Error / Warning / Information | | `event_name` | Event type (e.g. switch.port.down) | | `product_type` | Device category (access_point, switch, router) | | `device_function` | Device role (wireless, switching, routing) | | `site_name` | Site where events originated | | `host_name` | Device hostname |

Tags: `analytics`

Parameters:

- `group_by` query, required (string) — Dimension to group event counts by
- `start_time` query, optional (string) — Start of time range (RFC3339, e.g. 2026-05-01T00:00:00Z)
- `end_time` query, optional (string) — End of time range (RFC3339, e.g. 2026-05-07T23:59:59Z)
- `limit` query, optional (integer) — Maximum number of dimension groups to return (default 100, max 1000)

Responses:

- `200` — Grouped event counts
- `400`
- `500`

## GET `/events/trends`

Operation: `getEventTrends`

Get event trends over time

Returns event counts in fixed time buckets with a per-severity breakdown. Useful for detecting spikes, anomalies, or gradual escalation patterns. | Bucket | Best for | |---|---| | `1h` | Same-day analysis, incident timelines | | `6h` | 2–3 day views | | `1d` | Weekly trends | | `7d` | Monthly trends |

Tags: `analytics`

Parameters:

- `bucket` query, optional (string) — Time bucket size
- `start_time` query, optional (string) — Start of time range (RFC3339)
- `end_time` query, optional (string) — End of time range (RFC3339)

Responses:

- `200` — Time-bucketed event counts with severity breakdown
- `400`
- `500`

## GET `/catalog`

Operation: `getCatalog`

Get service catalog overview

Returns high-level metadata about the MetaStore service: data time range, event and device counts, and all supported query parameters.

Tags: `catalog`

Responses:

- `200` — Service catalog overview
- `500`

## GET `/catalog/devices`

Operation: `getCatalogDevices`

Discover devices with event activity

Returns devices that have recorded events, ranked by event volume. Use this to discover device IDs for use in GET /events filters, or to understand which devices are most active in the system.

Tags: `catalog`

Parameters:

- `product_type` query, optional (string) — Filter by device product type
- `device_function` query, optional (string) — Filter by device function role
- `limit` query, optional (integer) — Maximum devices to return (default 100, max 1000)

Responses:

- `200` — Devices with event activity, ranked by volume
- `500`

## GET `/catalog/event-schema/{event_name}`

Operation: `getEventSchema`

Get element_data schema for an event type

Returns the documented structure of `element_data` for a specific event type, including field names, types, descriptions, and example values. Also lists the typical severity and related event types for contextual understanding.

Tags: `catalog`

Parameters:

- `event_name` path, required (string) — The event type name (use GET /events/types to get valid names)

Responses:

- `200` — Event type schema documentation
- `500`

## GET `/mcp/manifest`

Operation: `getMCPManifest`

MCP tool manifest

Returns a machine-readable manifest describing all available MCP tools and their input parameters. MCP-compatible hosts can fetch this endpoint to auto-register MetaStore as a tool provider. Follows MCP schema version 2025-03. **Registered tools:** query_events, summarize_events, get_event_trends, discover_devices, get_catalog, get_event_schema, list_event_types

Tags: `mcp`

Responses:

- `200` — MCP tool manifest

## GET `/health`

Operation: `healthCheck`

Health check

Returns 200 if the service is healthy and the ClickHouse connection is live.

Tags: `health`

Responses:

- `200` — Service is healthy

## GET `/ready`

Operation: `readinessCheck`

Readiness check

Returns 200 if the service is ready to accept requests.

Tags: `health`

Responses:

- `200` — Service is ready

