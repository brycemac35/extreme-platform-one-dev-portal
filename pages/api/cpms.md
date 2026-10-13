---
source: https://developer.extremeplatformone.com/api-reference/cpms
spec: https://developer.extremeplatformone.com/api/spec/cpms
title: "Extreme Platform ONE REST API - Performance Monitoring"
---

# Extreme Platform ONE REST API - Performance Monitoring

**Performance** · Services. Network Performance Monitoring and Analytics.

Build real-time performance monitoring and analytics experiences with the Extreme Platform ONE Performance API. Discover metric metadata dynamically, retrieve the latest operational state, analyze trends over time, and compare performance across the dimensions that matter to your business.

Version: `0.1.0`

## Servers

- `https://cloudapi.extremecloudiq.com/performance/v1` — Extreme Platform ONE REST API - Performance Monitoring

Full OpenAPI document: [`specs/cpms.json`](../../specs/cpms.json)

## Endpoints

37 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/entity-types` | Discover entity types |
| GET | `/entity-types/{entity_type}` | Get entity type metadata |
| GET | `/metric-groups` | Discover metric groups |
| GET | `/metric-groups/{metric_group}` | Get metric group metadata |
| GET | `/metric-groups/{metric_group}/min-interval` | Get minimum aggregation interval |
| GET | `/metric-groups/{metric_group}/metrics` | Discover metrics |
| GET | `/metric-groups/{metric_group}/metrics/{metric}` | Get metric metadata |
| POST | `/metric-groups/device-cpu-stats/latest/query` | Query latest samples |
| POST | `/metric-groups/device-cpu-stats/latest/count-by` | Count latest entities by dimensions |
| POST | `/metric-groups/device-cpu-stats/latest/count-by/dry-run` | Dry run a latest count grouping |
| POST | `/metric-groups/device-cpu-stats/latest/metrics/{metric}/group-by` | Group latest metric values |
| POST | `/metric-groups/device-cpu-stats/latest/metrics/{metric}/group-by/dry-run` | Dry run a latest metric grouping |
| POST | `/metric-groups/device-cpu-stats/latest/metrics/{metric}/summarize` | Summarize latest metric values |
| POST | `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/query` | Query metric time series |
| POST | `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/group-by` | Group metric values over a time range |
| POST | `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/group-by/dry-run` | Dry run a time-range metric grouping |
| POST | `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/summarize` | Summarize a metric over a time range |
| POST | `/metric-groups/device-interface-stats/latest/query` | Query latest samples |
| POST | `/metric-groups/device-interface-stats/latest/count-by` | Count latest entities by dimensions |
| POST | `/metric-groups/device-interface-stats/latest/count-by/dry-run` | Dry run a latest count grouping |
| POST | `/metric-groups/device-interface-stats/latest/metrics/{metric}/group-by` | Group latest metric values |
| POST | `/metric-groups/device-interface-stats/latest/metrics/{metric}/group-by/dry-run` | Dry run a latest metric grouping |
| POST | `/metric-groups/device-interface-stats/latest/metrics/{metric}/summarize` | Summarize latest metric values |
| POST | `/metric-groups/device-interface-stats/time-range/metrics/{metric}/query` | Query metric time series |
| POST | `/metric-groups/device-interface-stats/time-range/metrics/{metric}/group-by` | Group metric values over a time range |
| POST | `/metric-groups/device-interface-stats/time-range/metrics/{metric}/group-by/dry-run` | Dry run a time-range metric grouping |
| POST | `/metric-groups/device-interface-stats/time-range/metrics/{metric}/summarize` | Summarize a metric over a time range |
| POST | `/metric-groups/device-stats/latest/query` | Query latest samples |
| POST | `/metric-groups/device-stats/latest/count-by` | Count latest entities by dimensions |
| POST | `/metric-groups/device-stats/latest/count-by/dry-run` | Dry run a latest count grouping |
| POST | `/metric-groups/device-stats/latest/metrics/{metric}/group-by` | Group latest metric values |
| POST | `/metric-groups/device-stats/latest/metrics/{metric}/group-by/dry-run` | Dry run a latest metric grouping |
| POST | `/metric-groups/device-stats/latest/metrics/{metric}/summarize` | Summarize latest metric values |
| POST | `/metric-groups/device-stats/time-range/metrics/{metric}/query` | Query metric time series |
| POST | `/metric-groups/device-stats/time-range/metrics/{metric}/group-by` | Group metric values over a time range |
| POST | `/metric-groups/device-stats/time-range/metrics/{metric}/group-by/dry-run` | Dry run a time-range metric grouping |
| POST | `/metric-groups/device-stats/time-range/metrics/{metric}/summarize` | Summarize a metric over a time range |

## GET `/entity-types`

Operation: `listEntityTypes`

Discover entity types

Discover the supported analytics entities and their dimensions, including the dimensions that form each entity key. Use free-text search and exact-match filters together with AND semantics to find the metadata you need.

Tags: `Metadata`

Parameters:

- `search` query, optional (string) — Case-insensitive free-text search across searchable metadata fields such as name, display_name, and description.
- `name` query, optional (string) — Exact match for the machine-readable entity type name.
- `dimension` query, optional (string) — Returns entity types containing this dimension.

Responses:

- `200` — Successful response
- `400` — Invalid search or filter parameters

## GET `/entity-types/{entity_type}`

Operation: `getEntityType`

Get entity type metadata

Retrieve the dimensions and key definition for an entity type so your application can construct valid filters, groupings, sorting, and field selections dynamically.

Tags: `Metadata`

Parameters:

- `entity_type` path, required (string) — Entity type name.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Entity type not found

## GET `/metric-groups`

Operation: `listMetricGroups`

Discover metric groups

Explore the available metric groups and find the datasets that match your analytics use case. Use free-text search and exact-match filters together with AND semantics to narrow the results.

Tags: `Metadata`

Parameters:

- `search` query, optional (string) — Case-insensitive free-text search across searchable metadata fields such as name and description.
- `name` query, optional (string) — Exact match for the machine-readable metric group name.
- `entity_type` query, optional (string) — Exact match for the associated entity type.
- `dimension` query, optional (string) — Returns metric groups containing this dimension.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## GET `/metric-groups/{metric_group}`

Operation: `getMetricGroup`

Get metric group metadata

Retrieve the entity type, dimensions, metrics, and resolution and retention tiers for a metric group before submitting analytics queries.

Tags: `Metadata`

Parameters:

- `metric_group` path, required (string) — Metric group name.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## GET `/metric-groups/{metric_group}/min-interval`

Operation: `getMetricGroupMinInterval`

Get minimum aggregation interval

Choose an efficient, supported time-series resolution by retrieving the minimum aggregation interval in seconds for a requested range. Specify either last or start_time with an optional end_time; the two range styles are mutually exclusive.

Tags: `Metadata`

Parameters:

- `metric_group` path, required (string) — Metric group name.
- `last` query, optional (ShortDuration) — Relative lookback window, such as 30m, 24h, or 7d. Mutually exclusive with start_time/end_time.
- `start_time` query, optional (string) — Inclusive range start in RFC 3339 format. Required when last is not provided.
- `end_time` query, optional (string) — Exclusive range end in RFC 3339 format. Defaults to current time when omitted.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## GET `/metric-groups/{metric_group}/metrics`

Operation: `listMetricsForMetricGroup`

Discover metrics

Discover the metrics available in a metric group, including their semantic type, value type, unit, and supported aggregations. Use free-text search and exact-match filters together with AND semantics to narrow the results.

Tags: `Metadata`

Parameters:

- `metric_group` path, required (string) — Metric group name.
- `search` query, optional (string) — Case-insensitive free-text search across searchable metadata fields such as name, display_name, and description.
- `name` query, optional (string) — Exact match for the machine-readable metric name.
- `value_type` query, optional (MetricValueType) — Exact match for the metric value type.
- `metric_type` query, optional (MetricType) — Exact match for the metric's semantic type.
- `unit` query, optional (string) — Exact match for the metric unit.
- `supported_aggregation` query, optional (AggregationFunction) — Returns metrics supporting this aggregation function.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## GET `/metric-groups/{metric_group}/metrics/{metric}`

Operation: `getMetricMetadata`

Get metric metadata

Retrieve the definition and supported analytics capabilities for a specific metric before adding it to a query.

Tags: `Metadata`

Parameters:

- `metric_group` path, required (string) — Metric group name.
- `metric` path, required (string) — Metric name.

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/latest/query`

Operation: `queryLatestDeviceCpuStats`

Query latest samples

Retrieve the freshest available sample for each matching entity to power current-state dashboards and operational workflows. Control payload size with field selection, then filter, sort, and paginate the results.

Tags: `Device CPU Metrics`

Request body:

- `application/json` — DeviceCpuStatsLatestQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/latest/count-by`

Operation: `countLatestDeviceCpuStatsBy`

Count latest entities by dimensions

Understand the current distribution of matching entities by grouping them across the dimensions you choose. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device CPU Metrics`

Request body:

- `application/json` — DeviceCpuStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/latest/count-by/dry-run`

Operation: `dryRunLatestDeviceCpuStatsCountBy`

Dry run a latest count grouping

Plan high-cardinality analytics safely by validating a latest count-by request and estimating its group cardinality without executing the aggregation. The count-by operation performs authoritative checks again at execution time.

Tags: `Device CPU Metrics`

Request body:

- `application/json` — DeviceCpuStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-cpu-stats/latest/metrics/{metric}/group-by`

Operation: `groupLatestDeviceCpuStatsMetric`

Group latest metric values

Compare current performance across one or more operational dimensions by aggregating the latest metric value for each matching entity. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/latest/metrics/{metric}/group-by/dry-run`

Operation: `dryRunLatestDeviceCpuStatsMetricGroupBy`

Dry run a latest metric grouping

Evaluate a latest metric grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-cpu-stats/latest/metrics/{metric}/summarize`

Operation: `summarizeLatestDeviceCpuStatsMetric`

Summarize latest metric values

Create a concise current-state KPI by calculating one aggregate metric value across the latest samples from all matching entities.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/query`

Operation: `queryDeviceCpuStatsMetricTimeRange`

Query metric time series

Analyze how a metric changes over time with a chronologically ordered series of aggregated time buckets. Choose an aggregation interval in seconds that is an integer multiple of the minimum interval supported for the requested range.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsTimeRangeQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/group-by`

Operation: `groupDeviceCpuStatsMetricTimeRange`

Group metric values over a time range

Compare performance across one or more dimensions by calculating an aggregate metric value for each group over the full requested range, without time bucketing. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/group-by/dry-run`

Operation: `dryRunDeviceCpuStatsMetricTimeRangeGroupBy`

Dry run a time-range metric grouping

Assess a time-range grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention policy

## POST `/metric-groups/device-cpu-stats/time-range/metrics/{metric}/summarize`

Operation: `summarizeDeviceCpuStatsMetricTimeRange`

Summarize a metric over a time range

Produce a single KPI for the requested period by aggregating the metric across the full time range without dividing it into time buckets.

Tags: `Device CPU Metrics`

Parameters:

- `metric` path, required (DeviceCpuStatsMetricName) — Metric in the device-cpu-stats metric group.

Request body:

- `application/json` — DeviceCpuStatsTimeRangeSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/latest/query`

Operation: `queryLatestDeviceInterfaceStats`

Query latest samples

Retrieve the freshest available sample for each matching entity to power current-state dashboards and operational workflows. Control payload size with field selection, then filter, sort, and paginate the results.

Tags: `Device Interface Metrics`

Request body:

- `application/json` — DeviceInterfaceStatsLatestQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/latest/count-by`

Operation: `countLatestDeviceInterfaceStatsBy`

Count latest entities by dimensions

Understand the current distribution of matching entities by grouping them across the dimensions you choose. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Interface Metrics`

Request body:

- `application/json` — DeviceInterfaceStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/latest/count-by/dry-run`

Operation: `dryRunLatestDeviceInterfaceStatsCountBy`

Dry run a latest count grouping

Plan high-cardinality analytics safely by validating a latest count-by request and estimating its group cardinality without executing the aggregation. The count-by operation performs authoritative checks again at execution time.

Tags: `Device Interface Metrics`

Request body:

- `application/json` — DeviceInterfaceStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-interface-stats/latest/metrics/{metric}/group-by`

Operation: `groupLatestDeviceInterfaceStatsMetric`

Group latest metric values

Compare current performance across one or more operational dimensions by aggregating the latest metric value for each matching entity. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/latest/metrics/{metric}/group-by/dry-run`

Operation: `dryRunLatestDeviceInterfaceStatsMetricGroupBy`

Dry run a latest metric grouping

Evaluate a latest metric grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (DeviceInterfaceStatsMetricName) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-interface-stats/latest/metrics/{metric}/summarize`

Operation: `summarizeLatestDeviceInterfaceStatsMetric`

Summarize latest metric values

Create a concise current-state KPI by calculating one aggregate metric value across the latest samples from all matching entities.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/time-range/metrics/{metric}/query`

Operation: `queryDeviceInterfaceStatsMetricTimeRange`

Query metric time series

Analyze how a metric changes over time with a chronologically ordered series of aggregated time buckets. Choose an aggregation interval in seconds that is an integer multiple of the minimum interval supported for the requested range.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsTimeRangeQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/time-range/metrics/{metric}/group-by`

Operation: `groupDeviceInterfaceStatsMetricTimeRange`

Group metric values over a time range

Compare performance across one or more dimensions by calculating an aggregate metric value for each group over the full requested range, without time bucketing. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-interface-stats/time-range/metrics/{metric}/group-by/dry-run`

Operation: `dryRunDeviceInterfaceStatsMetricTimeRangeGroupBy`

Dry run a time-range metric grouping

Assess a time-range grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (DeviceInterfaceStatsMetricName) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention policy

## POST `/metric-groups/device-interface-stats/time-range/metrics/{metric}/summarize`

Operation: `summarizeDeviceInterfaceStatsMetricTimeRange`

Summarize a metric over a time range

Produce a single KPI for the requested period by aggregating the metric across the full time range without dividing it into time buckets.

Tags: `Device Interface Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-interface-stats metric group.

Request body:

- `application/json` — DeviceInterfaceStatsTimeRangeSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/latest/query`

Operation: `queryLatestDeviceStats`

Query latest samples

Retrieve the freshest available sample for each matching entity to power current-state dashboards and operational workflows. Control payload size with field selection, then filter, sort, and paginate the results.

Tags: `Device Metrics`

Request body:

- `application/json` — DeviceStatsLatestQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/latest/count-by`

Operation: `countLatestDeviceStatsBy`

Count latest entities by dimensions

Understand the current distribution of matching entities by grouping them across the dimensions you choose. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Metrics`

Request body:

- `application/json` — DeviceStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/latest/count-by/dry-run`

Operation: `dryRunLatestDeviceStatsCountBy`

Dry run a latest count grouping

Plan high-cardinality analytics safely by validating a latest count-by request and estimating its group cardinality without executing the aggregation. The count-by operation performs authoritative checks again at execution time.

Tags: `Device Metrics`

Request body:

- `application/json` — DeviceStatsCountByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-stats/latest/metrics/{metric}/group-by`

Operation: `groupLatestDeviceStatsMetric`

Group latest metric values

Compare current performance across one or more operational dimensions by aggregating the latest metric value for each matching entity. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/latest/metrics/{metric}/group-by/dry-run`

Operation: `dryRunLatestDeviceStatsMetricGroupBy`

Dry run a latest metric grouping

Evaluate a latest metric grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (DeviceStatsMetricName) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata

## POST `/metric-groups/device-stats/latest/metrics/{metric}/summarize`

Operation: `summarizeLatestDeviceStatsMetric`

Summarize latest metric values

Create a concise current-state KPI by calculating one aggregate metric value across the latest samples from all matching entities.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/time-range/metrics/{metric}/query`

Operation: `queryDeviceStatsMetricTimeRange`

Query metric time series

Analyze how a metric changes over time with a chronologically ordered series of aggregated time buckets. Choose an aggregation interval in seconds that is an integer multiple of the minimum interval supported for the requested range.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsTimeRangeQueryRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/time-range/metrics/{metric}/group-by`

Operation: `groupDeviceStatsMetricTimeRange`

Group metric values over a time range

Compare performance across one or more dimensions by calculating an aggregate metric value for each group over the full requested range, without time bucketing. Refine the results with filtering, sorting, and pagination, or combine sort order with page size for Top-N/Bottom-N insights. The service checks estimated group cardinality before execution to protect performance and reliability.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

## POST `/metric-groups/device-stats/time-range/metrics/{metric}/group-by/dry-run`

Operation: `dryRunDeviceStatsMetricTimeRangeGroupBy`

Dry run a time-range metric grouping

Assess a time-range grouping safely by validating the request and estimating its group cardinality without executing the aggregation. The group-by operation performs authoritative checks again at execution time.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (DeviceStatsMetricName) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsTimeRangeGroupByRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention policy

## POST `/metric-groups/device-stats/time-range/metrics/{metric}/summarize`

Operation: `summarizeDeviceStatsMetricTimeRange`

Summarize a metric over a time range

Produce a single KPI for the requested period by aggregating the metric across the full time range without dividing it into time buckets.

Tags: `Device Metrics`

Parameters:

- `metric` path, required (string) — Metric in the device-stats metric group.

Request body:

- `application/json` — DeviceStatsTimeRangeSummarizeRequest

Responses:

- `200` — Successful response
- `400` — Invalid request
- `404` — Metric group or metric not found
- `422` — Request is syntactically valid but unsupported by the metric metadata or retention/resolution policy

