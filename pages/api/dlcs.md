---
source: https://developer.extremeplatformone.com/api-reference/dlcs
spec: https://developer.extremeplatformone.com/api/spec/dlcs
title: "Extreme Platform ONE REST API - Device Lifecycle Management"
---

# Extreme Platform ONE REST API - Device Lifecycle Management

**Device Lifecycle** · Services. Device Lifecycle Management.

The Extreme Platform ONE™ Device Lifecycle Management API provides comprehensive automation and orchestration for the complete network device lifecycle, from initial discovery and zero-touch onboarding through operational management and secure decommissioning. **🔄 Complete Lifecycle Management:** • **Zero-Touch Device Onboarding** - Fully automated provisioning for wireless devices (IQEngine/XIQ) and wired devices (EXOS/VOSS) with intelligent configuration validation and compliance checking • **Intelligent Bulk Operations** - Enterprise-scale batch processing with Excel-based import/export, template-driven workflows, and automated validation for efficient mass device management • **Advanced Device Discovery** - Device detection and classification with automatic product compatibility checking and network topology analysis • **Subscription & License Management** - Automated tracking and lifecycle management of device subscriptions, software licenses, and service entitlements • **Secure Lifecycle Transitions** - Complete device state management from onboarding through operational phases to secure decommissioning with audit trails **🏢 Enterprise Integration & Scale:** Built for enterprise environments with seamless integration capabilities, comprehensive audit trails, high-performance batch processing, and enterprise-grade security controls for large-scale network deployments.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/device-lifecycle` — Extreme Platform ONE REST API - Device Lifecycle

Full OpenAPI document: [`specs/dlcs.json`](../../specs/dlcs.json)

## Endpoints

56 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/v1/devices` | Get list of all devices |
| GET | `/v1/devices/applications` | Query device applications |
| POST | `/v1/devices/:export` | Export Devices List |
| POST | `/v1/devices/:delete` | Delete devices from management |
| GET | `/v1/devices:status` | Get device operation status (Deprecated) |
| POST | `/v1/devices/discovery/{device_sn}/:add` | Add Discovered Device to Management System |
| GET | `/v1/devices/discovery/{device_sn}/:result` | Get Discovered Devices for a Device |
| POST | `/v1/devices/discovery/{device_sn}/:result` | Get Discovered Devices for a Device |
| GET | `/v1/devices/discovery/{device_sn}/filters` | Get Device Discovery Filter Values |
| POST | `/v1/devices/discovery/{device_sn}/:start` | Start Discovery for a Device |
| GET | `/v1/devices/discovery/{device_sn}/:status` | Get Device Discovery Status |
| POST | `/v1/devices/discovery/{device_sn}/:stop` | Stop Discovery for a Device |
| GET | `/v1/devices/filters` | Get all available device filters |
| POST | `/v1/devices/filters` | Get device filter metadata |
| GET | `/v1/devices/images/:download` | Download Deployment Image |
| GET | `/v1/devices/images/:retrieve` | Retrieve Deployment Image Details |
| POST | `/v1/devices/onboard/appliance` | Onboard appliances to management platform |
| GET | `/v1/devices/onboard/device-info` | Product Info for Devices |
| POST | `/v1/devices/onboard/import-xlsx` | Onboarding of Bulk Devices |
| GET | `/v1/devices/onboard/import-xlsx/:sample` | Download device onboarding XLSX template |
| GET | `/v1/devices/onboard/status` | Get onboarding status (Deprecated) |
| POST | `/v1/devices/onboard/controller` | Onboard controllers to management platform |
| POST | `/v1/devices/onboard/wired` | Onboard wired devices to management platform |
| POST | `/v1/devices/onboard/wireless` | Onboard wireless devices to IQEngine |
| POST | `/v1/devices/onboard/controller-managed` | Onboard controller managed devices to Platform One |
| GET | `/v1/devices/rulesengine/action-types` | Get rules engine action types |
| GET | `/v1/devices/rulesengine/condition-fields` | Get rules engine condition fields |
| GET | `/v1/devices/rulesengine/operation-types` | Get rules engine operation types |
| POST | `/v1/devices/rulesengine/rules` | Create a new rules engine rule |
| POST | `/v1/devices/rulesengine/rules/:delete` | Delete rules engine rules |
| GET | `/v1/devices/rulesengine/rules/:list` | Get a paginated list of rules engine rules |
| PUT | `/v1/devices/rulesengine/rules/:reorder` | Reorder rules engine rules |
| GET | `/v1/devices/rulesengine/rules/{id}` | Get a rules engine rule by ID |
| PUT | `/v1/devices/rulesengine/rules/{id}` | Update a rules engine rule by ID |
| POST | `/v1/devices/token/:activate` | Activate Registration Token |
| POST | `/v1/devices/token/:register` | Get Registration Token |
| POST | `/v1/devices/firmware:summary` | Get Firmware Summary |
| POST | `/v1/devices/firmware:upgrade` | Initiate Firmware Upgrade |
| POST | `/v1/devices/firmware:versions` | Get Firmware Versions |
| POST | `/v1/devices:backup` | Initiate Configuration Backup |
| GET | `/v1/devices/{serial_number}/backups` | List Configuration Backups for a Device |
| GET | `/v1/devices/backup-file` | Get Configuration Backup File Content |
| POST | `/v1/devices:restore` | Restore Configuration Backup |
| GET | `/v1/devices/{serial_number}/backup-schedule` | Get Backup Schedule Details |
| POST | `/v1/devices/config:backup` | Schedule Configuration Backup |
| GET | `/v1/devices/config/{serial_number}/backup-schedule` | Get Configuration Backup Schedule |
| GET | `/v1/devices/{serial_number}/status` | Get Device Status |
| POST | `/v1/taskcenter/:list` | Get task details |
| GET | `/v1/taskcenter/{task_id}` | Get task details by task ID |
| GET | `/v1/taskcenter/{task_id}/run-instances/current` | Get current active run instance details of a task |
| POST | `/v1/taskcenter/{task_id}/run-instances/history/:list` | Get run instances history details of a task |
| GET | `/v1/taskcenter/{task_id}/summary` | Get task summary by task ID |
| POST | `/v1/taskcenter/run-instances/{run_instance_id}/entities/:list` | Get entities details by run instance ID |
| POST | `/v1/devices:execute-action` | Submit a device lifecycle operation |
| POST | `/v1/devices/upload/:image` | Upload device image metadata |
| POST | `/v1/devices/firmware:status` | Get Firmware Status Count |

## POST `/v1/devices`

Operation: `listDevices`

Get list of all devices

Retrieves a paginated list of devices with comprehensive filtering, searching, and sorting capabilities. Returns device status, configuration, network information, and links to detailed device views. Supports page-based pagination for flexible data retrieval in dashboards, reports, and monitoring systems.

Tags: `Device`

Parameters:

- `page` query, optional (integer) — Page number for pagination (1-based indexing)
- `limit` query, optional (integer) — Number of items per page (maximum 100)
- `search` query, optional (string) — Full-text search query to filter devices. Searches across hostname, MAC address, serial number, management IP, location, model, and operating system fields.
- `sort` query, optional (string) — Field name to sort results by. By default, results are sorted in ascending order if not explicitly specified. Users can specify the sort order by using the '+' character for ascending or the '-' character for descending.

Request body:

- `application/json` — DeviceFilter

Responses:

- `200` — Successful response with paginated device list
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/applications`

Operation: `queryDeviceApplications`

Query device applications

Retrieves either supported or installed applications on specified managed devices. Use query_type=SUPPORTED to discover available applications for deployment planning. Use query_type=INSTALLED to audit currently installed applications on target devices. Supports querying multiple devices via comma-separated serial numbers. Optionally filter by device_type (e.g., UNIVERSAL_COMPUTE_PLATFORM) to scope results to specific device classes.

Tags: `Device`

Parameters:

- `serial_numbers` query, required (array) — List of device serial numbers to query. Queries are scoped to managed devices only; unmanaged devices are silently skipped.
- `query_type` query, required (DeviceApplicationQueryTypeEnum) — Application query type. SUPPORTED: returns applications this device can support (available for deployment). INSTALLED: returns applications currently running on the device.
- `device_type` query, optional (DeviceActionDeviceTypeEnum) — Optional device type filter. When specified, limits results to devices of the specified type. If omitted, returns applications for all device types. Common values: UNIVERSAL_COMPUTE_PLATFORM. When combined with serial_numbers, acts as an…

Responses:

- `200` — Device applications retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`

## POST `/v1/devices/:export`

Operation: `exportDevicesList`

Export Devices List

Export device data displayed on the UI in CSV format based on filter criteria and search parameters.

Tags: `Device`

Parameters:

- `search` query, optional (string) — Full-text search query to filter devices. Searches across hostname, MAC address, serial number, management IP, location, model, and operating system fields.
- `sort` query, optional (string) — Field name to sort results by. By default, results are sorted in ascending order if not explicitly specified. Users can specify the sort order by using the '+' character for ascending or the '-' character for descending.

Request body:

- `application/json` — DeviceFilter

Responses:

- `200` — Successfully exported devices as CSV file
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/:delete`

Operation: `deleteDevices`

Delete devices from management

Removes devices from centralized management and inventory. Supports bulk deletion operations with comprehensive status tracking. Use with caution as this operation removes devices from monitoring and management oversight.

Tags: `Device`

Request body:

- `application/json` — DeleteDeviceRequestVo

Responses:

- `200` — Device deletion operation initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices:status`

Operation: `getDeviceStatus`

Get device operation status (Deprecated)

Returns the current status and progress of device delete operations. Provides real-time monitoring of delete tasks, including completion status, error information, and progress indicators. Essential for tracking bulk device delete operations. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use `GET /v2/devices/{task_key}/status` instead.

Tags: `Device`

Parameters:

- `task_key` query, required (string) — The task key of the device operation for which status is to be fetched.

Responses:

- `200` — The device operation status response
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/discovery/{device_sn}/:add`

Operation: `addDiscoveredDevice`

Add Discovered Device to Management System

Add a discovered device to the management system using its serial number and optional device type. This endpoint facilitates the onboarding of devices that have been identified on the network but are not yet managed.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Request body:

- `application/json` — DeviceDiscoveryAddRequestVo

Responses:

- `200` — The device discovery add response
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/discovery/{device_sn}/:result`

Operation: `getDeviceDiscoveryResultList`

Get Discovered Devices for a Device

Retrieves the list of devices discovered by a specified device. This endpoint provides detailed information about the devices that have been identified during the discovery process, enabling administrators to manage and monitor network assets effectively. **Deprecation Notice:** This endpoint is deprecated and will be removed in the future. Please use the POST /v1/devices/discovery/{device_sn}/:result endpoint instead, which offers enhanced filtering and search capabilities.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Responses:

- `200` — The device discovery result response
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/discovery/{device_sn}/:result`

Operation: `getDeviceDiscoveryResult`

Get Discovered Devices for a Device

Retrieves the list of devices discovered by a specified device. This endpoint provides detailed information about the devices that have been identified during the discovery process, enabling administrators to manage and monitor network assets effectively.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.
- `page` query, optional (integer) — Page number for pagination (1-based indexing)
- `limit` query, optional (integer) — Number of items per page (maximum 500)
- `search` query, optional (string) — Full-text search query to filter devices. Searches across hostname, serial number, management IP, location, model, and firmware version fields.
- `sort` query, optional (string) — Field name to sort results by (must match the server-side sort fields, such as 'ip_address'). By default, results are sorted in ascending order if not explicitly specified. Users can specify the sort order by using the '+' character for…

Request body:

- `application/json`

Responses:

- `200` — The device discovery result response
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/discovery/{device_sn}/filters`

Operation: `getDeviceDiscoveryResultFilter`

Get Device Discovery Filter Values

Retrieves all available device discovery filter values aggregated from existing devices. Returns unique values for each filter field that can be used to filter the device discovery results.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Responses:

- `200` — Successfully retrieved device filter values
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/discovery/{device_sn}/:start`

Operation: `startDeviceDiscovery`

Start Discovery for a Device

Initiates the discovery process for a specified device using its serial number. This endpoint allows administrators to start device discovery operations to identify and catalog devices within the network. It is essential for network management and ensuring that all devices are accounted for and properly configured.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Request body:

- `application/json` — DeviceDiscoveryStartRequestVo

Responses:

- `200` — The device discovery start response
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/discovery/{device_sn}/:status`

Operation: `getDeviceDiscoveryStatus`

Get Device Discovery Status

Retrieve the status of device discovery operations in the management system. This endpoint provides information on the progress and results of device discovery processes.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Responses:

- `200` — The device discovery status response
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/discovery/{device_sn}/:stop`

Operation: `stopDeviceDiscovery`

Stop Discovery for a Device

Stops the ongoing discovery process for a specified device. This endpoint allows administrators to halt device discovery operations that are no longer needed or were initiated in error. It ensures that network resources are conserved and prevents unnecessary processing.

Tags: `Device`

Parameters:

- `device_sn` path, required (string) — The serial number of the device to be discovered. This is a unique identifier for the device.
- `device_type` query, optional (DeviceTypeEnum) — The type of the device to be discovered. This can be used to filter the discovery results based on device type.

Responses:

- `200` — The device discovery stop response
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/filters`

Operation: `listDeviceFilters`

Get all available device filters

Retrieves all available device filter values aggregated from existing devices. Returns unique values for each filter field that can be used to filter the device list.

Tags: `Device`

Responses:

- `200` — Successfully retrieved device filter values
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/filters`

Operation: `listDeviceFilterMetadata`

Get device filter metadata

Retrieves available device filter values scoped to a specific device classification. Returns unique filter values aggregated from existing devices matching the given classification.

Tags: `Device`

Request body:

- `application/json` — DeviceFilterMetadataRequest

Responses:

- `200` — Successfully retrieved device filter values for the given classification
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/images/:download`

Operation: `downloadOvaImage`

Download Deployment Image

Download the deployment OVA image for a specific application type and deployment type directly into the service's pod.

Tags: `Device`

Parameters:

- `device_type` query, optional (DeviceTypeEnum) — The application type for which the OVA image is to be downloaded.
- `deploy_type` query, optional (DeployTypeEnum) — The deployment type for which the OVA image is to be downloaded.
- `image_name` query, optional (string) — The specific image name of the OVA image to be downloaded.

Responses:

- `200` — Successfully served the deployment OVA image URL to the UI
- `400`
- `401`
- `403`
- `404`
- `405`
- `500`
- `502`

## GET `/v1/devices/images/:retrieve`

Operation: `getDeploymentImageDetails`

Retrieve Deployment Image Details

Fetches the latest details of deployment images for a specific application type. Provides information about available deployment images for the given application.

Tags: `Device`

Parameters:

- `device_type` query, optional (DeviceTypeEnum) — The application type for which deployment image details are to be fetched.

Responses:

- `200` — Successfully retrieved deployment image details
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/appliance`

Operation: `onboardAppliances`

Onboard appliances to management platform

Initiates the onboarding process for appliance devices. Handles device discovery, authentication, and initial configuration for centralized device management.

Tags: `Device`

Request body:

- `application/json` — ApplianceOnboardingRequestVo

Responses:

- `200` — Appliance device onboarding initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/onboard/device-info`

Operation: `getDeviceInfo`

Product Info for Devices

Product info of the serial numbers based on the selected device make.

Tags: `Device`

Parameters:

- `device_make` query, required (DeviceMakeEnum) — The device make for which the product info is to be fetched.
- `serial_numbers` query, required (array) — The serial numbers for which the product info is to be fetched.

Responses:

- `200` — Device product info response
- `400` — Bad Request
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/import-xlsx`

Operation: `importXlsx`

Onboarding of Bulk Devices

Onboarding of Bulk Devices via XLSX file - Switch Engine/EXOS, Fabric Engine/VOSS, AP.

Tags: `Device`

Parameters:

- `auth_header` header, optional (string) — The authorization token from the UI.
- `network_policy_id` query, optional (integer) — The ID of the network policy to associate with the device (optional).
- `location_id` query, optional (integer) — The ID of the location to associate with the device (optional).
- `license_type` query, optional (LicenseTypeEnum) — The type of license to be applied to the device (optional).
- `managed_by` query, optional (ManagingDeviceType) — The type of device that manages this device.
- `primary_controller` query, optional (string) — Primary controller IP address for controller managed APs (optional).
- `backup_controller` query, optional (string) — Backup controller IP address for controller managed APs (optional).

Request body:

- `multipart/form-data` — file

Responses:

- `200` — Device Bulk Onboard response
- `400`
- `401`
- `403`
- `405`
- `413`
- `415`
- `500`

## GET `/v1/devices/onboard/import-xlsx/:sample`

Operation: `downloadXlsxTemplate`

Download device onboarding XLSX template

Downloads a sample XLSX template file for bulk device onboarding. The template includes proper column headers and example data to guide users in preparing their device import files.

Tags: `Device`

Responses:

- `200` — XLSX template file for device onboarding
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/onboard/status`

Operation: `getStatus`

Get onboarding status (Deprecated)

Returns the current status and progress of device onboarding operations. Provides real-time monitoring of onboarding tasks, including completion status, error information, and progress indicators. Essential for tracking bulk device operations. **Deprecation Notice:** This endpoint is deprecated and will be removed in a future release. Please use `GET /v2/devices/{task_key}/status` instead.

Tags: `Device`

Parameters:

- `task_key` query, required (string) — The task key of the onboarded device for which status is to be fetched.

Responses:

- `200` — Successfully retrieved device onboarding status
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/controller`

Operation: `onboardControllers`

Onboard controllers to management platform

Initiates the onboarding process for controllers. Handles device discovery, authentication, and initial configuration for centralized controller management.

Tags: `Device`

Request body:

- `application/json` — ControllerOnboardingRequestVo

Responses:

- `200` — Controller onboarding initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/wired`

Operation: `onboardWiredDevices`

Onboard wired devices to management platform

Initiates the onboarding process for wired devices including Switch Engine/EXOS and Fabric Engine/VOSS platforms. Handles device discovery, authentication, and initial configuration for centralized network management.

Tags: `Device`

Request body:

- `application/json` — WiredDeviceOnboardingRequestVo

Responses:

- `200` — Wired device onboarding initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/wireless`

Operation: `onboardWirelessDevices`

Onboard wireless devices to IQEngine

Initiates the onboarding process for wireless devices to the IQEngine platform. Handles device discovery, authentication, and initial configuration. Essential for bringing wireless devices under centralized management.

Tags: `Device`

Request body:

- `application/json` — WirelessDeviceOnboardingRequestVo

Responses:

- `200` — Wireless device onboarding initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/onboard/controller-managed`

Operation: `onboardControllerManagedDevices`

Onboard controller managed devices to Platform One

Initiates the onboarding process for controller managed devices to the Platform One. Handles device discovery, authentication, and initial configuration. Essential for bringing controller managed devices under centralized management.

Tags: `Device`

Request body:

- `application/json` — CtrlManagedDeviceOnboardingRequestVo

Responses:

- `200` — Controller managed device onboarding initiated successfully
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/rulesengine/action-types`

Operation: `getActionTypes`

Get rules engine action types

Retrieves the list of action types that can be configured and executed by the rules engine when rule conditions are met, such as assigning devices to sites, applying configuration profiles, or upgrading firmware. The verbose parameter controls whether detailed capability information is included in the response.

Tags: `Device`

Parameters:

- `verbose` query, optional (boolean) — When true, returns detailed information about each action type including descriptions and examples; when false, returns a simple list of action types.

Responses:

- `200` — Successfully retrieved the list of action types. Response includes a list array with action type names, and a details array with detailed capability information when verbose=true.
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/rulesengine/condition-fields`

Operation: `getConditionFields`

Get rules engine condition fields

Retrieves the list of device fields that can be used as condition fields in rules engine rules, such as device operating system, model, hostname, and IP subnet. Each field includes information about supported operation types (e.g., equals, contains, in range) that can be applied when creating rule conditions.

Tags: `Device`

Responses:

- `200` — Successfully retrieved an array of condition fields, each containing the field name, data type, and supported operations for rule conditions
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/rulesengine/operation-types`

Operation: `getOperationTypes`

Get rules engine operation types

Retrieves the list of operation types that can be used to evaluate rule conditions, including numeric comparisons (equal, not equal, less than, greater than, range checks), string operations (equal, contains, starts with, ends with, regex matching), and network operations (IPv4 subnet matching). The verbose parameter controls whether detailed capability information is included in the response.

Tags: `Device`

Parameters:

- `verbose` query, optional (boolean) — When true, returns detailed information about each operation type including descriptions and examples; when false, returns a simple list of operation types.

Responses:

- `200` — Successfully retrieved the list of operation types. Response includes a list array with operation type names, and a details array with detailed capability information when verbose=true.
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/rulesengine/rules`

Operation: `createRules`

Create a new rules engine rule

Creates a new rules engine rule with the specified configuration, including name, description, enabled status, condition definitions that determine when the rule triggers, and action configurations that execute when conditions are met. The rule is created with higher priority than existing rules. Returns the unique identifier of the newly created rule upon success.

Tags: `Device`

Request body:

- `application/json` — RulesEngineCreateRulesRequestVo

Responses:

- `200` — Successfully created the rule. Returns an object containing the unique identifier (id) assigned to the newly created rule, which can be used for subsequent retrieval, update, or deletion operations.
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/rulesengine/rules/:delete`

Operation: `deleteRules`

Delete rules engine rules

Deletes one or more rules engine rules from the system using their unique identifiers. This operation permanently removes the specified rules along with their associated conditions and actions. Accepts an array of rule IDs in the request body and returns a status code indicating the result of the deletion operation.

Tags: `Device`

Request body:

- `application/json` — RulesEngineDeleteRulesRequestVo

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/rulesengine/rules/:list`

Operation: `getRulesList`

Get a paginated list of rules engine rules

Retrieves a paginated list of rules engine rules with their complete configurations, including rule IDs, names, descriptions, enabled status, execution sequences, condition definitions, and action configurations. Supports pagination through page and limit query parameters.

Tags: `Device`

Parameters:

- `None` , optional
- `None` , optional
- `sort_by` query, optional (RulesEngineSortByEnum) — The field to sort the rules. Default sorting is by SEQUENCE in DESC order
- `order` query, optional (SortOrder) — The sort order
- `search` query, optional (string) — The search term to filter rules. Supports search on name
- `enabled` query, optional (boolean) — Filter rules by their enabled status

Responses:

- `200` — Successfully retrieved the paginated list of rules. Response includes pagination metadata (page, limit, total count) and a data array containing rule objects with their IDs and full configurations.
- `400`
- `401`
- `403`
- `405`
- `500`

## PUT `/v1/devices/rulesengine/rules/:reorder`

Operation: `reorderRules`

Reorder rules engine rules

Reorders one or more rules engine rules by updating their sequence positions to control rule evaluation priority and execution order. Higher sequence numbers have higher priority in rule evaluation.

Tags: `Device`

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `405`
- `500`

## GET `/v1/devices/rulesengine/rules/{id}`

Operation: `getRules`

Get a rules engine rule by ID

Retrieves the complete details of a rules engine rule by its unique identifier, including base entity fields (id, creation/modification timestamps), name, description, enabled status, execution sequence, condition definitions, and action configurations.

Tags: `Device`

Parameters:

- `None` , optional

Responses:

- `200` — Successfully retrieved the rule details. Response includes base entity fields (id, owner_id, create_time, update_time) and the complete rule configuration (name, description, enabled status,…
- `400`
- `401`
- `403`
- `405`
- `500`

## PUT `/v1/devices/rulesengine/rules/{id}`

Operation: `updateRules`

Update a rules engine rule by ID

Updates an existing rules engine rule with new configuration, including name, description, enabled status, execution sequence, conditions, and actions. The rule ID must be provided in both the path parameter and the request body.

Tags: `Device`

Parameters:

- `None` , optional

Request body:

- `application/json` — RulesEngineUpdateRulesRequestVo

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/token/:activate`

Operation: `activateToken`

Activate Registration Token

Activates a registration token for a given application type, deployment type, location, and token.

Tags: `Device`

Request body:

- `application/json` — ActivateTokenRequest

Responses:

- `200` — Activation response
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/token/:register`

Operation: `getOrCreateToken`

Get Registration Token

Creates a registration token for a given application type, deployment type, and location.

Tags: `Device`

Request body:

- `application/json` — RegisterTokenRequest

Responses:

- `200` — Token response
- `400`
- `401`
- `403`
- `405`
- `500`

## POST `/v1/devices/firmware:summary`

Operation: `getFirmwareSummary`

Get Firmware Summary

Retrieves firmware summary information with pagination support. This endpoint provides details about firmware summary for devices in the inventory.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome.
- `page` query, optional (integer) — Page number for pagination.
- `limit` query, optional (integer) — Number of items per page.

Request body:

- `application/json` — DeviceFwSummaryRequestFilter

Responses:

- `200` — The firmware summary response
- `400`
- `401`
- `403`
- `405`
- `429`
- `500`
- `503`

## POST `/v1/devices/firmware:upgrade`

Operation: `getFirmwareSummaryUpgrade`

Initiate Firmware Upgrade

Initiates firmware upgrade process for devices based on filter criteria. This endpoint allows scheduling or immediate execution of firmware upgrades.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second upgrade.

Request body:

- `application/json` — DeviceFwUpgradeRequestFilter

Responses:

- `200` — Firmware upgrade initiated successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `409`
- `429`
- `500`
- `503`

## POST `/v1/devices/firmware:versions`

Operation: `getFirmwareVersions`

Get Firmware Versions

Retrieves firmware versions information with pagination and filtering support. This endpoint provides details about firmware versions for devices in the inventory.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome.
- `search` query, optional (string) — Search filename or version for tpme managed devices (minimum 1 character, supports alphanumeric and special characters)
- `page` query, optional (integer) — Page number for pagination.
- `limit` query, optional (integer) — Number of items per page.

Request body:

- `application/json` — DeviceFirmwareRequestFilter

Responses:

- `200` — The firmware versions response
- `400`
- `401`
- `403`
- `405`
- `429`
- `500`
- `503`

## POST `/v1/devices:backup`

Operation: `triggerConfigurationBackup`

Initiate Configuration Backup

Initiates configuration backup process for devices based on filter criteria. This endpoint allows scheduling or immediate execution of configuration backup.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second backup.

Request body:

- `application/json` — DeviceFwBackupRequestFilter

Responses:

- `200` — Configuration backup initiated successfully.
- `400`
- `401`
- `403`
- `405`
- `409`
- `429`
- `500`
- `503`

## GET `/v1/devices/{serial_number}/backups`

Operation: `listConfigBackups`

List Configuration Backups for a Device

Returns the list of configuration backup files available for a single TPME-managed device. Backup names are formatted as Backup- . Date & Time values are always UTC (RFC3339 with Z suffix).

Tags: `Device`

Parameters:

- `serial_number` path, required (string) — Serial number of the TPME-managed device. This is the value of the serial_number field returned by GET /v1/devices.
- `page` query, optional (integer) — Page number for pagination (1-based indexing).
- `limit` query, optional (integer) — Number of items per page (maximum 500).
- `search` query, optional (string) — Search by file name only. Search by date-time is not supported. Supported characters: "-", ":", a-z, A-Z, 0-9.
- `sort_by` query, optional (string) — Field name to sort results by: backup_name, file_size, or date_time. Users can specify the sort order by using the '+' character for ascending or the '-' character for descending. The default sort is `date_time-` (date_time in descending…

Responses:

- `200` — Configuration backup list retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`
- `503`

## GET `/v1/devices/backup-file`

Operation: `getConfigBackupFileContent`

Get Configuration Backup File Content

Returns the human-readable text content of a configuration backup file for preview. For ZIP backups, returns the path of the file. There may be a delay during fetch; Returns an error if the file has been deleted on the TPME since the list was loaded, or if the file transfer fails.

Tags: `Device`

Parameters:

- `serial_number` query, required (string) — Serial number of the TPME-managed device.
- `backup_name` query, required (string) — The display backup name to preview (e.g., Backup-2026-05-15T06:38:07Z). This is the backup_name field from the List Configuration Backups response.

Responses:

- `200` — Backup file content retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`
- `503`

## POST `/v1/devices:restore`

Operation: `triggerConfigRestore`

Restore Configuration Backup

Initiates a configuration restore for a single TPME-managed device from a specified backup. Restore progress is reported asynchronously via TPME status callbacks Pre-conditions validated before restore is initiated: - Device must be online (CONNECTED state) - No other operations must be in progress on the device.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second restore.

Request body:

- `application/json` — ConfigRestoreRequest

Responses:

- `200` — Restore operation initiated successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `409`
- `429`
- `500`
- `503`

## GET `/v1/devices/{serial_number}/backup-schedule`

Operation: `getBackupSchedule`

Get Backup Schedule Details

Retrieves the configured backup schedule frequency (for example DAILY, WEEKLY or MONTHLY) for a single device, identified by its serial number in the path. Read-only: it returns the schedule but neither creates a backup nor alters the schedule. Returns 404 when the serial number is unknown or when no backup schedule has been configured for that device, so callers must treat "no schedule" as a valid outcome rather than an error.

Tags: `Device`

Parameters:

- `serial_number` path, required (string) — Serial number of the device to retrieve backup schedule for. This is the value of the serial_number field returned by GET /v1/devices.

Responses:

- `200` — Backup schedule details retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`
- `503`

## POST `/v1/devices/config:backup`

Operation: `updateConfigBackupSchedule`

Schedule Configuration Backup

Schedules configuration backup for a device based on daily, weekly, or monthly frequency. This endpoint allows setting up recurring configuration backup schedules.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of applying the schedule a second time.

Request body:

- `application/json` — DeviceConfigBackupScheduleRequest

Responses:

- `200` — Configuration backup schedule updated successfully.
- `400`
- `401`
- `403`
- `405`
- `409`
- `429`
- `500`
- `503`

## GET `/v1/devices/config/{serial_number}/backup-schedule`

Operation: `getConfigBackupSchedule`

Get Configuration Backup Schedule

Retrieves the stored configuration backup schedule for a single device, identified by its serial number in the path, including the timezone and the day-and-time fields that apply to the configured daily, weekly or monthly frequency. Read-only: it neither triggers a backup nor changes the schedule. Returns 404 when the serial number is unknown or no schedule has been configured, so callers must treat "no schedule" as a valid outcome rather than an error.

Tags: `Device`

Parameters:

- `serial_number` path, required (string) — Serial number of the device to retrieve configuration backup schedule for. This is the value of the serial_number field returned by GET /v1/devices.

Responses:

- `200` — Configuration backup schedule details retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`
- `503`

## GET `/v1/devices/{serial_number}/status`

Operation: `getDeviceStatusBySerialNumber`

Get Device Status

Retrieves the current operational status of a specific device identified by its serial number. Returns a map of operation types (backup, restore, firmware_upgrade, etc.) directly at the root of the response, with dynamic status fields for each operation that vary based on device type, configuration, and current state.

Tags: `Device`

Parameters:

- `serial_number` path, required (string) — Serial number of the device to retrieve status for. An alphanumeric identifier that may include hyphens, 5-64 characters long. Format varies by manufacturer/device type, e.g. switches typically use a plain alphanumeric string…

Responses:

- `200` — Device status retrieved successfully.
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`
- `503`

## POST `/v1/taskcenter/:list`

Operation: `listTasks`

Get task details

Retrieves a paginated list of tasks with optional filtering and sorting capabilities. Use to browse, search, or filter multiple tasks across your organization.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second restore.
- `None` , optional
- `None` , optional
- `search` query, optional (string) — Search string to filter tasks by name, created by, device hostname, IPv4 address or serial number
- `sort_by` query, optional (string) — Field name to sort / group results by. Default sort: STATUS (pre-defined order). Users can specify the sort order by adding a '+' suffix for ascending or a '-' suffix for descending. Known values: TASK_NAME, TASK_TYPE, STATUS,…

Request body:

- `application/json` — TaskListFilter

Responses:

- `200` — Successfully retrieved paginated task details
- `400`
- `401`
- `403`
- `405`
- `429`
- `500`

## GET `/v1/taskcenter/{task_id}`

Operation: `getTaskByTaskId`

Get task details by task ID

Retrieves detailed information about a specific task including configuration, status, progress, schedule, and device summary. Use to get comprehensive information about a single task's current state.

Tags: `Device`

Parameters:

- `task_id` path, required (string) — The `task_id` value returned by POST /v1/taskcenter/:list

Responses:

- `200` — Successfully retrieved task details
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`

## GET `/v1/taskcenter/{task_id}/run-instances/current`

Operation: `getRunInstancesCurrent`

Get current active run instance details of a task

Retrieves the currently active run instance for a task with real-time progress, status, and device summary. Use to monitor actively executing tasks. Returns no data once run completes.

Tags: `Device`

Parameters:

- `task_id` path, required (string) — The unique identifier of the task

Responses:

- `200` — Successfully retrieved the active run instance
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`

## POST `/v1/taskcenter/{task_id}/run-instances/history/:list`

Operation: `listRunInstancesHistory`

Get run instances history details of a task

Retrieves paginated historical run instances for a task with aggregate metrics like average duration and success rate. Use to analyze execution patterns, track trends, or audit past results.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second restore.
- `task_id` path, required (string) — The unique identifier of the task
- `None` , optional
- `None` , optional

Responses:

- `200` — Successfully retrieved run instance history
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`

## GET `/v1/taskcenter/{task_id}/summary`

Operation: `getTaskSummary`

Get task summary by task ID

Retrieves lightweight task summary with status, progress, timing, schedule details, and aggregated device statistics. Use for quick status overview without detailed configuration or entity data.

Tags: `Device`

Parameters:

- `task_id` path, required (string) — The unique identifier of the task

Responses:

- `200` — Successfully retrieved task summary
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`

## POST `/v1/taskcenter/run-instances/{run_instance_id}/entities/:list`

Operation: `listEntities`

Get entities details by run instance ID

Retrieves paginated entities (typically devices) for a run instance with execution status, progress, and outcomes. Use to inspect per-device results for a task execution run.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome instead of starting a second restore.
- `run_instance_id` path, required (string) — The unique identifier of the run instance
- `None` , optional
- `None` , optional
- `sort_by` query, optional (string) — Field name to sort / group results by. Default sort: STATUS (pre-defined order). Users can specify the sort order by adding a '+' suffix for ascending or a '-' suffix for descending. Known values: STATUS, LOCATION, START_TIME
- `search` query, optional (string) — Search string to filter entities by name, device hostname, IPv4 address, serial number or site

Request body:

- `application/json` — EntitiesListFilter

Responses:

- `200` — Successfully retrieved paginated entities details
- `400`
- `401`
- `403`
- `404`
- `405`
- `429`
- `500`

## POST `/v1/devices:execute-action`

Operation: `triggerDeviceAction`

Submit a device lifecycle operation

Submits an action to one or more managed devices and returns right away. The action runs in the background; poll the status URL returned in the response until it reports a final state.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated unique key (e.g. a UUID) that makes this mutating request safe to retry. A repeated request carrying the same key returns the original outcome instead of submitting the action a second time.

Request body:

- `application/json` — DeviceActionRequestVo

Responses:

- `202` — Action request accepted for asynchronous processing.
- `400`
- `401`
- `403`
- `404`
- `405`
- `409`
- `413`
- `415`
- `429`
- `500`
- `502`

## POST `/v1/devices/upload/:image`

Operation: `uploadImage`

Upload device image metadata

Uploads a device image file and retrieves image metadata information.

Tags: `Device`

Request body:

- `multipart/form-data` — file

Responses:

- `200` — Device image metadata uploaded successfully
- `400`
- `401`
- `403`
- `500`

## POST `/v1/devices/firmware:status`

Operation: `getFirmwareStatus`

Get Firmware Status Count

Retrieves firmware status count information for devices. Returns total updates, EOVM count, and security vulnerability count based on classification and location filters.

Tags: `Device`

Parameters:

- `Idempotency-Key` header, optional (string) — Client-generated key that makes this request safe to retry. Replaying the same key returns the original outcome.

Request body:

- `application/json` — DeviceFirmwareStatusRequestFilter

Responses:

- `200` — The firmware status count response
- `400`
- `401`
- `403`
- `405`
- `429`
- `500`
- `503`

