---
source: https://developer.extremeplatformone.com/api-reference/pm
spec: https://developer.extremeplatformone.com/api/spec/pm
title: "PerfMonitor Infrastructure API"
---

# PerfMonitor Infrastructure API

**Performance Monitoring** · Services. Network Performance Monitoring and Analytics.

# Performance Monitor Infrastructure API for MCP Servers This comprehensive API provides advanced network performance monitoring capabilities specifically optimized for MCP (Model Context Protocol) servers and automated monitoring systems. The API enables sophisticated monitoring of device health, performance metrics, and network analytics across various network components with intelligent automation support. ## MCP Server Integration Features - **Automated Performance Monitoring**: Continuous collection and analysis of network performance metrics - **Intelligent Alerting**: AI-driven anomaly detection and automated alert generation - **Time-Series Analytics**: Advanced time-series data processing for trend analysis and forecasting - **Real-time Health Monitoring**: Live device health status tracking with automated response capabilities - **Scalable Data Collection**: High-performance metric collection supporting thousands of devices - **Integration-Ready**: Designed for seamless integration with monitoring platforms and automation tools ## Key Features - **Application Discovery**: List supported monitoring applications and their capabilities - **Metric Collection**: Retrieve time-series performance data from network devices with advanced filtering - **Device Health Analytics**: Monitor device health status and performance indicators with trend analysis - **Flexible Filtering**: Advanced filtering and pagination optimized for large-scale monitoring deployments - **Real-time Data**: Access to current and historical performance metrics with microsecond precision - **Bulk Operations**: Efficient batch processing for monitoring large network infrastructures ## MCP Use Cases - **Infrastructure Monitoring**: Automated monitoring of switches, routers, and network devices - **Performance Optimization**: AI-driven performance analysis and optimization recommendations - **Capacity Planning**: Predictive analytics for network capacity planning and resource allocation -…

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/pm/v1` — Extreme Platform ONE REST API - Performance Monitoring

Full OpenAPI document: [`specs/pm.json`](../../specs/pm.json)

## Endpoints

19 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/applications` | Discover Supported Monitoring Applications for MCP Integration |
| GET | `/metric-capabilities` | Advanced Metric Capability Discovery for MCP Servers |
| GET | `/metric-schema` | Get the complete metric capability schema for all groups |
| GET | `/metric-capabilities/{metricGroup}` | Get detailed metric capability for a specific metric group |
| POST | `/metric-data` | Advanced Time-Series Metric Retrieval for MCP Servers |
| POST | `/analytics/device-health` | Advanced Wired Device Health Analytics for MCP Servers |
| POST | `/analytics/device-health/wireless` | Wireless Device Health Analytics for MCP Servers |
| POST | `/analytics/usage-capacity` | Advanced Usage and Capacity Analytics for MCP Servers |
| POST | `/analytics/client-health` | Advanced Wired Client Health Analytics for MCP Servers |
| POST | `/analytics/client-health/history` | Historical Client Session Data at Network/Site Level for both wired and wireless clients |
| POST | `/analytics/client-health/stats` | Client Health Stats Time-Series Data for MCP Servers |
| POST | `/analytics/client-health/wireless` | Advanced Wireless Client Health Analytics for MCP Servers |
| POST | `/analytics/client-health/wireless/filter-metadata` | Advanced Client Health Analytics Metadata for MCP Servers |
| POST | `/analytics/client-health/wireless/issue` | Client Issue Details for Wireless Devices |
| POST | `/analytics/usage-capacity/wireless` | Wireless Usage Capacity Analytics for MCP Servers |
| POST | `/analytics/dashboard` | Dashboard Summary and Grid Data |
| POST | `/analytics/client-trail/roaming` | Client Trail Roaming Data for AI and MCP Servers |
| POST | `/analytics/client-trail/connectivity-experience` | Client Trail Connectivity Experience for AI and MCP Servers |
| GET | `/analytics/ip-routing/devices/{device_id}` | Retrieve IPv4 routing details for a specific device |

## GET `/applications`

Operation: `GetApplications`

Discover Supported Monitoring Applications for MCP Integration

**Application Discovery for MCP Servers** Retrieves a comprehensive list of monitoring applications supported by the performance monitoring service, specifically designed for MCP (Model Context Protocol) servers and automated monitoring systems. This endpoint provides the foundation for understanding available monitoring capabilities and building intelligent monitoring automation. **MCP Server Features:** - **Dynamic Application Discovery**: Programmatically discover available monitoring applications and their capabilities - **Capability Validation**: Validate application support before implementing automated monitoring workflows - **Configuration Automation**: Enable dynamic configuration of monitoring systems based on available applications - **Integration Planning**: Understand monitoring scope for automated infrastructure management **Use Cases for MCP Servers:** - **Monitoring System Bootstrap**: Initialize automated monitoring systems with available application discovery - **Dynamic UI Generation**: Build adaptive monitoring interfaces based on supported applications - **Workflow Automation**: Configure automated monitoring workflows based on application capabilities - **Integration Validation**: Verify application support before deploying monitoring automation - **Capability Assessment**: Assess monitoring coverage for infrastructure automation planning **Response Details:** Returns an array of application objects optimized for programmatic consumption: - Application…

Tags: `application management`

Responses:

- `200` — Successfully retrieved the list of supported applications. The response contains an array of application objects with their names and descriptions.
- `429`
- `500` — Internal server error occurred while retrieving applications
- `503`

## GET `/metric-capabilities`

Operation: `GetMetricCapabilities`

Advanced Metric Capability Discovery for MCP Servers

**Metric Capability Analysis for MCP Servers** Returns comprehensive information about metric collection capabilities for specific applications, designed for MCP (Model Context Protocol) servers implementing intelligent monitoring automation. This endpoint provides rich metadata essential for planning automated monitoring strategies and building sophisticated performance analytics workflows. **MCP Server Features:** - **Comprehensive Metric Discovery**: Detailed capability analysis for automated monitoring planning - **Intelligent Scope Planning**: Rich metadata for building optimized monitoring strategies - **Automation Configuration**: Detailed metric group information for automated collector configuration - **Performance Planning**: Capability information for building high-performance monitoring systems **Use Cases for MCP Servers:** - **Monitoring Strategy Planning**: Analyze available metrics for comprehensive monitoring automation - **Collector Configuration**: Configure automated metric collectors based on available capabilities - **Performance Analytics Setup**: Plan time-series analytics based on available metric groups - **Resource Planning**: Understand metric collection scope for infrastructure capacity planning - **Integration Validation**: Verify metric availability before implementing monitoring workflows - **Dynamic Monitoring**: Build adaptive monitoring systems based on runtime capability discovery **Enhanced Metric Groups for Automation:** - **device…

Tags: `metric capabilities`

Parameters:

- `application` query, required (string) — The name of the application for which to retrieve metric capabilities. Must be one of the supported application names returned by the /applications endpoint. Currently only 'network' is supported.
- `detail` query, optional (string) — Controls the level of detail returned in the response. - **summary** (default): Returns metric group names and descriptions only (backward compatible) - **full**: Returns complete field-level metadata including field names, types, units,…

Responses:

- `200` — Successfully retrieved metric capabilities for the specified application. Returns an array of metric capability objects containing detailed information about available metric groups and their…
- `400` — Bad request - invalid application name provided. The application parameter is required and must be one of the supported values.
- `404` — Application not found - the specified application is not supported or does not exist.
- `409` — Validation conflict - the application name conflicts with system requirements.
- `429`
- `500` — Internal server error occurred while retrieving metric capabilities
- `503`

## GET `/metric-schema`

Operation: `GetMetricSchema`

Get the complete metric capability schema for all groups

Returns the full metric registry in a single call — all metric groups, sub-metrics, field names, types, units, supported filters, and example requests. **This is the recommended first call for any AI agent or automation system** that needs to understand what data is available before constructing `/metric-data` requests. No parameters are required. The response is keyed by metric group name (e.g. `"device stats"`, `"interface stats"`) and each entry contains the same structure as `/metric-capabilities/{metricGroup}`.

Tags: `metric capabilities`

Responses:

- `200` — Successfully retrieved the complete metric capability schema.
- `429`
- `500` — Internal server error
- `503`

## GET `/metric-capabilities/{metricGroup}`

Operation: `GetMetricCapabilityDetail`

Get detailed metric capability for a specific metric group

Returns full field-level metadata for a single metric group, including all available fields with their names, types, units, and descriptions, plus supported filters and an example request payload. **Use Case:** After discovering available metric groups via `/metric-capabilities`, use this endpoint to get the complete schema for a specific group before constructing a `/metric-data` request.

Tags: `metric capabilities`

Parameters:

- `metricGroup` path, required (string) — The metric group name to retrieve detailed capabilities for. Must be URL-encoded if it contains spaces (e.g., "device%20stats").
- `application` query, required (string) — The application name. Currently only 'network' is supported.

Responses:

- `200` — Successfully retrieved detailed metric capability for the specified group.
- `400` — Bad request - invalid parameters
- `404` — Metric group not found
- `429`
- `500` — Internal server error
- `503`

## POST `/metric-data`

Operation: `RetrieveMetricData`

Advanced Time-Series Metric Retrieval for MCP Servers

**High-Performance Time-Series Data Retrieval for MCP Servers** Retrieves comprehensive time-series metric data from monitored network devices with advanced filtering, intelligent pagination, and optimized time range processing. This primary data endpoint is specifically designed for MCP (Model Context Protocol) servers implementing sophisticated performance monitoring, analytics, and automated alerting systems. **MCP Server Features:** - **High-Performance Time-Series Processing**: Optimized queries for large-scale monitoring deployments - **Intelligent Data Sampling**: Configurable sampling rates for efficient data processing and storage - **Real-Time and Historical Analytics**: Support for both live monitoring and historical trend analysis - **Single Device Per Request**: Exactly one device per request; issue parallel requests for multi-device scenarios - **Automated Filtering**: Advanced pattern matching for interface and metric-specific data extraction - **Scalable Pagination**: Optimized pagination for processing massive datasets in monitoring workflows **Advanced Time-Series Capabilities:** - **Microsecond Precision**: High-resolution timestamps for precise performance analysis - **Multi-Dimensional Filtering**: Complex filtering across time, devices, interfaces, and metric types - **Adaptive Sampling**: Intelligent data sampling based on monitoring requirements and system load - **Stream Processing Ready**: Optimized for real-time stream processing and event-driven…

Tags: `Metric Data`

Request body:

- `application/json` — MetricDataRequest

Responses:

- `200` — Successfully retrieved metric data. The response contains an array of metric data objects, each including the metrics information and pagination details. **Response Structure:** - `items`: Array of…
- `400` — Bad Request - Invalid request parameters provided. **Common Causes:** - Missing required fields (applicationName, metricGroup) - Invalid time format (must be ISO 8601 UTC) - Invalid frequency value -…
- `404` — No metric data found for the specified criteria. **Common Causes:** - No devices found matching the specified identifiers - No data available for the requested time range - Specified metric group not…
- `409` — Conflict in request parameters. **Common Causes:** - Conflicting time range parameters - Invalid combination of device identification methods - Metric group not supported for specified application -…
- `429`
- `500` — Internal server error occurred while processing the metric data request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/device-health`

Operation: `RetrieveDeviceHealthData`

Advanced Wired Device Health Analytics for MCP Servers

**Intelligent Wired Device Health Analytics for MCP Servers** Provides comprehensive health analytics for wired network devices with advanced health scoring, predictive analytics, and intelligent status assessment. This endpoint is specifically designed for MCP (Model Context Protocol) servers implementing proactive network management, predictive maintenance, and automated health monitoring systems. **MCP Server Features:** - **Intelligent Health Scoring**: AI-driven health assessment with composite health scores - **Predictive Analytics**: Early warning indicators for potential device failures and issues - **Location-Aware Monitoring**: Hierarchical location filtering for geographic monitoring strategies - **Automated Health Assessment**: Continuous health evaluation with threshold-based alerting - **Trend Analysis Ready**: Health data optimized for time-series analysis and trending - **Integration-Optimized**: Health data formatted for ITSM and automation platform integration **Advanced Health Analytics:** - **Composite Health Scoring**: Multi-dimensional health assessment combining all device metrics - **Anomaly Detection**: Statistical analysis for identifying abnormal health patterns - **Baseline Comparison**: Health status compared to historical baselines and peer devices - **Predictive Indicators**: Early warning metrics for proactive maintenance planning - **Risk Assessment**: Device risk scoring based on health trends and failure probability **MCP Use Cases:** -…

Tags: `Device health data`

Parameters:

- `download` query, optional (string) — When set to `csv`, the response is returned as a CSV file download instead of JSON. The CSV contains flattened device health data with one row per device. When this parameter is set, `responseType` is automatically forced to `grid` and…

Request body:

- `application/json` — DeviceHealthDataRequest

Responses:

- `200` — Successfully retrieved network device health data. **Response Structure:** - `applicationName`: Always "network" for network device health - `metricGroup`: Always "device health" for this endpoint -…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Unsupported device stats parameter values - Page size exceeds…
- `404` — No device health data found for the specified criteria. **Common Causes:** - No devices found in specified locations - Invalid location IDs provided - No health data available for accessible devices…
- `409` — Conflict in request parameters or data state. **Common Causes:** - Conflicting location filter parameters - Data consistency issues during retrieval
- `429`
- `500` — Internal server error occurred while processing the device health request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/device-health/wireless`

Operation: `RetrieveWirelessDeviceHealthData`

Wireless Device Health Analytics for MCP Servers

**Wireless Device Health Analytics for MCP Servers** Provides comprehensive health analytics exclusively for wireless network devices (Access Points). This endpoint automatically filters for wireless devices only, returning health metrics including CPU, Memory and PoE data for all APs. **Key Differences from /analytics/device-health:** - **Wireless-Only**: Automatically filters for AP/wireless devices — no need to specify deviceType - **All Metrics Included**: Returns all available health metrics (cpu, memory, poe) by default - **Simplified Request**: Fewer required parameters for wireless-focused monitoring **MCP Server Features:** - **Intelligent Health Scoring**: AI-driven health assessment with composite health scores for APs - **Location-Aware Monitoring**: Hierarchical location filtering for geographic AP monitoring - **Automated Health Assessment**: Continuous health evaluation with threshold-based alerting - **Integration-Optimized**: Health data formatted for ITSM and automation platform integration **Wireless-Specific Health Metrics:** - **CPU Analytics**: AP processor utilization trends and performance degradation detection - **Memory Intelligence**: AP RAM usage patterns and capacity forecasting - **Power Analytics**: PoE consumption tracking

Tags: `Wireless device health data`

Parameters:

- `download` query, optional (string) — When set to `csv`, the response is returned as a CSV file download instead of JSON. The CSV contains flattened device health data with one row per device. When this parameter is set, `responseType` is automatically forced to `grid` and…

Request body:

- `application/json` — WirelessDeviceHealthDataRequest

Responses:

- `200` — Successfully retrieved wireless device health data. **Response Structure:** - `applicationName`: Always "network" for network device health - `metricGroup`: Always "wireless device health" for this…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Page size exceeds maximum allowed limit
- `404` — No wireless device health data found for the specified criteria. **Common Causes:** - No wireless devices found in specified locations - Invalid location IDs provided - No health data available for…
- `409` — Conflict in request parameters. **Common Causes:** - Conflicting location filter parameters
- `429`
- `500` — Internal server error occurred while processing the wireless device health request.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/usage-capacity`

Operation: `RetrieveUsageCapacityData`

Advanced Usage and Capacity Analytics for MCP Servers

**Intelligent Network Device Usage and Capacity Analytics for MCP Servers** Provides usage and capacity analytics for wired network devices for intelligent status assessment. This endpoint is specifically designed for MCP (Model Context Protocol) servers implementing proactive network management, predictive maintenance, and automated monitoring systems. **MCP Server Features:** - **Intelligent Usage and Capacity Scoring**: AI-driven usage and capacity assessment with composite usage and capacity data - **Location-Aware Monitoring**: Hierarchical location filtering for geographic monitoring strategies - **Automated Usage and Capacity Assessment**: Continuous usage and capacity evaluation - **Trend Analysis Ready**: Usage and Capacity data optimized for time-series analysis and trending - **Integration-Optimized**: Usage and Capacity data formatted for ITSM and automation platform integration **Advanced Usage and Capacity Analytics:** - **Composite Usage and Capacity Data**: Multi-dimensional usage and capacity assessment combining all device metrics **MCP Use Cases:** - **Proactive Monitoring Systems**: Automated usage and capacity monitoring - **Predictive Maintenance**: ML-driven maintenance scheduling based on usage and capacity analytics - **Infrastructure Optimization**: Usage and Capacity-based recommendations for infrastructure improvements - **Automated Remediation**: Usage and Capacity-triggered automated response and remediation workflows - **Compliance…

Tags: `Usage capacity data`

Parameters:

- `download` query, optional (string) — When set to `csv`, the response is returned as a CSV file download instead of JSON. The CSV contains flattened usage capacity data with one row per device. When this parameter is set, `responseType` is automatically forced to `grid` and…

Request body:

- `application/json` — UsageCapacityDataRequest

Responses:

- `200` — Successfully retrieved network usage capacity data. **Response Structure:** - `applicationName`: Always "network" for network usage capacity - `metricGroup`: Always "usage capacity" for this endpoint…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Unsupported device stats parameter values - Page size exceeds…
- `404` — No usage capacity data found for the specified criteria. **Common Causes:** - No devices found in specified locations - Invalid location IDs provided - No usage capacity data available for accessible…
- `409` — Conflict in request parameters or data state. **Common Causes:** - Conflicting location filter parameters - Data consistency issues during retrieval
- `429`
- `500` — Internal server error occurred while processing the device usage capacity request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health`

Operation: `RetrieveClientHealthData`

Advanced Wired Client Health Analytics for MCP Servers

**Intelligent Wired Client Health Analytics for MCP Servers** Provides comprehensive health analytics for wired client devices with advanced health scoring, predictive analytics, and intelligent status assessment. This endpoint is specifically designed for MCP (Model Context Protocol) servers implementing proactive network management, predictive maintenance, and automated health monitoring systems. **Enhanced Health Metrics:** - **IP Connectivity Issues**: Indicates problems with device IP reachability, such as failed ping responses, unreachable gateways, or network isolation events. - **Port Congestion**: Represents high utilization or saturation on network ports, potentially causing packet delays, drops, or degraded performance. - **Traffic Anomalies**: Detects unusual or unexpected traffic patterns, including spikes, protocol mismatches, or abnormal flows that may impact network stability. - **Port Errors**: Captures error events on network ports, such as CRC errors, collisions, or link flaps, which can affect data transmission reliability **Intelligent Location Hierarchy:** Advanced location-based filtering with geographic intelligence: 1. **Site-Level Analytics**: Comprehensive site health overview with comparative analysis 2. **Building-Level Intelligence**: Building-specific health trends and environmental correlation 3. **Floor-Level Precision**: Granular floor-level monitoring with spatial health mapping 4. **Zone-Based Analysis**: Custom zone definitions for…

Tags: `Client health data`

Parameters:

- `download` query, optional (string) — When set to `csv`, the response is returned as a CSV file download instead of JSON. The CSV contains flattened wired client health data with one row per client. When this parameter is set, `responseType` is automatically forced to `grid`…

Request body:

- `application/json` — ClientHealthDataRequest

Responses:

- `200` — Successfully retrieved network client health data. **Response Structure:** - `applicationName`: Always "network" for network device health - `metricGroup`: Always "client health" for this endpoint -…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Unsupported device stats parameter values - Page size exceeds…
- `404` — No device health data found for the specified criteria. **Common Causes:** - No devices found in specified locations - Invalid location IDs provided - No health data available for accessible devices…
- `409` — Conflict in request parameters or data state. **Common Causes:** - Conflicting location filter parameters - Data consistency issues during retrieval
- `429`
- `500` — Internal server error occurred while processing the device health request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health/history`

Operation: `RetrieveHistoricalClientHealthData`

Historical Client Session Data at Network/Site Level for both wired and wireless clients

**Historical Client Session Data at Network/Site Level** Retrieves historical client session records for both wired and wireless clients across an entire network or site without requiring a specific DeviceID. This endpoint answers queries like "Show me all clients that connected to my network/site in the past 7 days." Unlike `/client-health` (which shows only currently active), this endpoint returns raw historical session records`.

Tags: `Client health data`

Request body:

- `application/json` — HistoricalClientHealthRequest

Responses:

- `200` — Successfully retrieved historical client session data. **Response Structure:** - `timeRange`: The queried time window - `clients`: Raw session records — one entry per client session (not…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Missing required startTime or endTime - Time range exceeds maximum allowed (30 days) - startTime is after endTime - Invalid location IDs
- `404` — No historical client data found for the specified criteria.
- `429`
- `500` — Internal server error.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health/stats`

Operation: `RetrieveClientHealthStatsData`

Client Health Stats Time-Series Data for MCP Servers

**Client Health Stats Time-Series Analytics for MCP Servers** Retrieves aggregated healthy and unhealthy client counts per device over time from the `client_health_stats` hypertable. This endpoint supports both real-time latest-value queries and historical time-range queries with automatic aggregation tier selection. **Query Modes:** - **Latest Value** (`latestValue: true`): Returns the most recent data point from the base hypertable for each requested device. Ideal for real-time dashboards and current status monitoring. - **Time Range** (`startTime` + `endTime`): Returns time-series data points within the specified range. The system automatically selects the optimal aggregation tier based on the time span: - **≤15 days**: Raw base table (1-minute granularity) - **≤30 days**: 5-minute aggregation (`client_health_stats_agg1`) - **≤90 days**: 10-minute aggregation (`client_health_stats_agg2`) - **≤13 months**: 1-hour aggregation (`client_health_stats_agg3`) - **≤24 months**: 1-day aggregation (`client_health_stats_agg4`) **Use Cases for MCP Servers:** - **Health Trending**: Track healthy vs unhealthy client ratios over time for capacity planning - **Anomaly Detection**: Identify sudden changes in client health for automated alerting - **Historical Analysis**: Review client health patterns for root cause analysis - **Dashboard Widgets**: Power real-time and historical health visualizations **Data Source:** Data is populated by the wired client event handler…

Tags: `Client health data`

Request body:

- `application/json` — ClientHealthStatsRequest

Responses:

- `200` — Successfully retrieved client health stats data. **Response Structure:** - `metricGroup`: Always "client health stats" for this endpoint - `ownerID`: Identifier for the data owner/tenant - `items`:…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Missing required `deviceID` - Neither `latestValue` nor time range (`startTime` + `endTime`) specified - `startTime` is after `endTime`…
- `404` — No client health stats data found for the specified criteria.
- `429`
- `500` — Internal server error occurred while processing the request.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health/wireless`

Operation: `RetrieveWirelessClientHealthData`

Advanced Wireless Client Health Analytics for MCP Servers

**Intelligent Client Health Analytics for MCP Servers** Provides comprehensive health analytics for wireless clients with advanced health scoring, predictive analytics, and intelligent status assessment. This endpoint is specifically designed for MCP (Model Context Protocol) servers implementing proactive network management, predictive maintenance, and automated health monitoring systems. **Enhanced Health Metrics:** - **IP Address Issues**: Identifies clients with self-assigned, unassigned, or valid IP addresses to assess connectivity status. - **Roaming Issues**: Identifies clients experiencing frequent or failed roaming events between access points, which can impact connectivity and performance. - **Authentication Issues**: Detects clients with authentication failures or issues that may prevent them from connecting to the network. - **Association Issues**: Identifies clients with association problems, such as frequent disconnections or failures to associate with access points. - **Frequency Distribution**: Provides insights into client distribution across different frequency bands (2.4 GHz vs 5 GHz) to optimize network performance and capacity planning. **Intelligent Location Hierarchy:** Advanced location-based filtering with geographic intelligence: 1. **Site-Level Analytics**: Comprehensive site health overview with comparative analysis 2. **Building-Level Intelligence**: Building-specific health trends and environmental correlation 3. **Floor-Level Precision**:…

Tags: `Client health data for wireless devices`

Parameters:

- `download` query, optional (string) — When set to `csv`, the response is returned as a CSV file download instead of JSON. The CSV contains flattened wireless client health data with one row per client. When this parameter is set, `responseType` is automatically forced to…

Request body:

- `application/json` — WirelessClientHealthDataRequest

Responses:

- `200` — Successfully retrieved network client health data. **Response Structure:** - `applicationName`: Always "network" for network device health - `metricGroup`: Always "client health" for this endpoint -…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Unsupported device stats parameter values - Page size exceeds…
- `404` — No device health data found for the specified criteria. **Common Causes:** - No devices found in specified locations - Invalid location IDs provided - No health data available for accessible devices…
- `409` — Conflict in request parameters or data state. **Common Causes:** - Conflicting location filter parameters - Data consistency issues during retrieval
- `429`
- `500` — Internal server error occurred while processing the device health request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health/wireless/filter-metadata`

Operation: `RetrieveWirelessClientHealthMetadata`

Advanced Client Health Analytics Metadata for MCP Servers

**Intelligent Client Health Analytics for MCP Servers** Provides comprehensive health analytics filtering criteria for wireless network devices. This endpoint is specifically designed for MCP (Model Context Protocol) servers implementing proactive network management, predictive maintenance, and automated health monitoring systems.

Tags: `Client health data values for wireless devices`

Request body:

- `application/json` — WirelessClientHealthMetadataRequest

Responses:

- `200` — Successfully retrieved network client metadata. **Response Structure:** - `applicationName`: Always "network" for network device health - `metricGroup`: Always "client health" for this endpoint -…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Invalid site, building, or floor IDs - Invalid page number or page size - Unsupported device stats parameter values - Page size exceeds…
- `404` — No device health data found for the specified criteria. **Common Causes:** - No devices found in specified locations - Invalid location IDs provided - No health data available for accessible devices…
- `409` — Conflict in request parameters or data state. **Common Causes:** - Conflicting location filter parameters - Data consistency issues during retrieval
- `429`
- `500` — Internal server error occurred while processing the device health request. This may indicate database connectivity issues or internal processing errors.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-health/wireless/issue`

Operation: `RetrieveWirelessClientIssueDetails`

Client Issue Details for Wireless Devices

**Client Issue Detail Retrieval for MCP Servers** Returns a chronological list of issue events for a specific wireless client, filtered by issue type. Each event includes the timestamp, human-readable reason, duration, and the device name where the issue was observed. **Supported Issue Types:** - **association**: Association failures (problem IDs 0–3, −3) - **authentication**: Authentication failures (problem IDs 65536–65553, −4) - **network**: Network connectivity issues (problem IDs 131072–131074, −2) - **roaming**: Roaming failures (problem ID −5) History of Data is sourced from `legacy_wireless_client_monitor_problem_stats` over the last 24 hours. **Pagination (Optional):** - `page`: Page number to retrieve, 1-based (default: 1, in request body) - `limit`: Number of items per page (default: 100, max: 1000, in request body) - If not provided, all results are returned

Tags: `Client health data for wireless devices`

Request body:

- `application/json` — WirelessClientIssueRequest

Responses:

- `200` — Successfully retrieved client issue details. **Response Structure:** - `macAddress`: The queried client MAC address - `issueType`: The queried issue category - `totalCount`: Total number of issue…
- `400` — Bad Request - Invalid request parameters. **Common Causes:** - Missing or invalid macAddress format - Invalid issueType value
- `404` — No issue data found for the specified client and issue type.
- `429`
- `500` — Internal server error occurred while processing the request.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/usage-capacity/wireless`

Operation: `RetrieveWirelessUsageCapacityData`

Wireless Usage Capacity Analytics for MCP Servers

Retrieves wireless usage capacity analytics including RF stats, client counts, channel utilization, interference, noise, packet loss, and retry rates per AP device. Supports grid (paginated device-level) and summary (aggregated) response types.

Tags: `Usage capacity data`

Request body:

- `application/json` — WirelessUsageCapacityDataRequest

Responses:

- `200` — Successful response
- `404` — No wireless data found for the specified criteria.
- `429`
- `500` — Internal server error occurred while processing the request.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/dashboard`

Operation: `GetDashboardData`

Dashboard Summary and Grid Data

Provides aggregated dashboard data across device health, client health, usage capacity, device status, and alerts. Supports three response modes via the `responseType` field in the request body: - **omitted or empty**: Returns both summary and grid in a combined response (default). - **summary**: Returns aggregated issue counts (total, wired, wireless) for each section. - **grid**: Returns per-site location rows with health status for each section, supporting keyword filtering, sorting, and pagination. Use `siteIds` to filter data to specific sites. Use `keyword` to filter by site name.

Tags: `dashboard`

Request body:

- `application/json` — DashboardRequest

Responses:

- `200` — Successfully retrieved dashboard data. The response shape depends on the `responseType` parameter. When omitted, returns DashboardCombinedResponse with both summary and grid.
- `400` — Invalid or missing responseType parameter
- `429`
- `500` — Internal server error
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-trail/roaming`

Operation: `RetrieveClientTrailRoamingData`

Client Trail Roaming Data for AI and MCP Servers

**Client Roaming Trail Analysis for MCP Servers** Retrieves roaming trail data from the Historical Client Session table, showing the sequence of access point transitions (roams) for a specific client within a given time range. A roam event is detected when the device serial number changes between consecutive session records sorted by timestamp in ascending order. **Roam Detection Logic:** - Sessions are sorted by timestamp ascending for the specified client MAC - A roam is identified when the device serial number changes between consecutive records - The "from" fields come from the previous record, "to" fields from the next record - Roam duration is taken from the `roaming_time` field of the destination (to) record **Roam Status Determination:** The status is determined by correlating with the Client Monitor Problem table: - If any association, authentication, DHCP, DNS, or gateway issue exists for the client MAC within the time window → status = `FAILED` - Otherwise → status = `ROAMING_COMPLETED` **Problem ID Mapping (from HiveOsProblem):** - Association issues: problem_id 0–3 (category 1) or -3 (slow association) - Authentication issues: problem_id 65536–65553 (category 2) or -4 (slow auth) - DHCP issues: problem_id 131072 or -2 (DHCP slow) - DNS issues: problem_id 131073 - Gateway issues: problem_id 131074 **Data Sources:** - `legacy_wireless_historical_client_session_stats` — session records - `legacy_wireless_client_monitor_problem_stats` — problem/failure detection -…

Tags: `Client trail data`

Request body:

- `application/json` — ClientTrailRoamingRequest

Responses:

- `200` — Successfully retrieved client roaming trail data.
- `400` — Bad Request - Invalid request parameters.
- `404` — No roaming data found for the specified client and time range.
- `429`
- `500` — Internal server error occurred while processing the request.
- `503`
- `default` — Unexpected error occurred

## POST `/analytics/client-trail/connectivity-experience`

Operation: `RetrieveClientTrailConnectivityExperience`

Client Trail Connectivity Experience for AI and MCP Servers

**Client Connectivity Experience Analysis for MCP Servers** Retrieves the connectivity experience timeline for a specific client, showing the session-level details including association, authentication, DHCP, DNS, and gateway status for each connection event within the specified time range. **Connectivity Flow:** Each session record represents one connection event. The circle statuses indicate the outcome of each connectivity phase: 1. **Association** — Did the client successfully associate with the AP? 2. **Authentication** — Did the client pass authentication? 3. **DHCP** — Did the client obtain an IP address? 4. **DNS** — Is DNS resolution functioning? 5. **Gateway** — Is the default gateway reachable? **Circle Status Determination (from Client Monitor Problem table):** - `associationCircleStatus`: `FAILED` if problem_id in 0–3 or -3, else `SUCCESS` - `authCircleStatus`: `FAILED` if problem_id in 65536–65553 or -4, else `SUCCESS` - `dhcpCircleStatus`: `INVALID` if problem_id in 131072 or -2, else `OK` - `dnsCircleStatus`: `DISABLED` if problem_id = 131073, else `OK` - `gatewayCircleStatus`: `DISABLED` if problem_id = 131074, else `OK` **Data Sources:** - `legacy_wireless_historical_client_session_stats` — session records - `legacy_wireless_client_metrics_stats` — DHCP/DNS/gateway IPs and response times - `legacy_wireless_client_monitor_problem_stats` — circle status derivation - Redis AssetDevice cache — device name resolution

Tags: `Client trail data`

Request body:

- `application/json` — ClientTrailConnectivityExperienceRequest

Responses:

- `200` — Successfully retrieved client connectivity experience data.
- `400` — Bad Request - Invalid request parameters.
- `404` — No connectivity data found for the specified client and time range.
- `429`
- `500` — Internal server error occurred while processing the request.
- `503`
- `default` — Unexpected error occurred

## GET `/analytics/ip-routing/devices/{device_id}`

Operation: `GetDeviceIpRoutingAnalytics`

Retrieve IPv4 routing details for a specific device

Returns IPv4 routing table details for a given device, including route origin, next-hop information, VLAN association, ping protection state, and timing metadata. Supports pagination via `pageNumber` and `pageSize` query parameters.

Tags: `IP Routing Analytics`

Parameters:

- `device_id` path, required (integer) — The unique identifier of the network device.
- `pageNumber` query, optional (integer) — Page number for pagination (1-based indexing).
- `pageSize` query, optional (integer) — Number of items per page.

Responses:

- `200` — Successfully retrieved IP routing details for the device.
- `400` — Invalid request parameters.
- `404` — Device not found or no routing data available.
- `429`
- `500` — Internal server error.
- `503`
- `default` — Unexpected error occurred.

