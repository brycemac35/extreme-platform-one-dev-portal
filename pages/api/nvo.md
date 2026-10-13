---
source: https://developer.extremeplatformone.com/api-reference/nvo
spec: https://developer.extremeplatformone.com/api/spec/nvo
title: "Extreme Networks Common Infrastructure API"
---

# Extreme Networks Common Infrastructure API

**Visualization** · Services. Network Visualization.

# Common Infrastructure REST API This comprehensive API provides access to the Common Infrastructure services for Extreme Networks' network management platform. The API enables programmatic access to topology management, device management, service management, and network visualization capabilities. ## Key Features - **Topology Management**: Retrieve and manage network topologies (physical, fabric, service layers) - **Device Management**: Access device information, interfaces, neighbors, and fabric details - **Service Management**: Manage L2/L3 VSN, VLAN, and VRF services - **User Preferences**: Store and retrieve user-specific preferences - **Real-time Updates**: WebSocket notifications for topology and device changes - **Service Probing**: VLAN service probe utilities for network validation ## API Design This API follows RESTful principles and supports JSON payloads. Most operations use POST methods with detailed criteria objects to provide flexible filtering and querying capabilities suitable for complex network topologies. ## Authentication This API is designed to be integrated with MCP (Model Context Protocol) servers and other automation tools. Authentication and authorization should be handled at the infrastructure level. ## MCP Server Integration This API is optimized for MCP (Model Context Protocol) server integration with the following features: **AI-Friendly Design:** - Comprehensive endpoint descriptions with use cases and examples - Structured error responses for better error handling - Detailed parameter descriptions for automated API consumption - Response schemas optimized for AI interpretation **Automation Support:** - API Key authentication recommended for MCP servers - Asynchronous operations with proper status tracking - Bulk operations where applicable - Consistent data formats across endpoints **Rate Limiting Considerations:** - Recommended rate limit: 60 requests per minute - Burst allowance: 10 requests - Consider caching for topology and…

Version: `3.0.0`

## Servers

- `https://cloudapi.extremecloudiq.com/nvo/v1` — Extreme Platform ONE REST API - Network Visualization

Full OpenAPI document: [`specs/nvo.json`](../../specs/nvo.json)

## Endpoints

40 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/retrieve-topology` | Retrieve Network Topology |
| POST | `/retrieve-topology/device` | Retrieve Device Topology Data |
| POST | `/retrieve-topology/link` | Retrieve Link Topology Data |
| POST | `/hide` | Hide Node or Link |
| POST | `/unhide` | Unhide Node or Link |
| GET | `/group` | Get Group Hierarchy |
| GET | `/tags` | Retrieve Tags |
| POST | `/tags` | Create a new tag |
| PUT | `/tags` | Update a tag |
| DELETE | `/tags` | Delete a tag |
| POST | `/tags/entities` | Associate tags with entities |
| DELETE | `/tags/entities` | Disassociate tags from nodes |
| GET | `/user/preferences` | getUserPreferences |
| POST | `/user/preferences` | postUserPreferences |
| DELETE | `/user/preferences` | deleteUserPreferences |
| POST | `/custom-positions` | Update the Custom Position |
| DELETE | `/custom-positions` | Delete custom positions |
| GET | `/device/physical/link` | Get Physical Link Details |
| GET | `/device/fabric/link` | Get device fabric link details |
| GET | `/device/ports` | Get device interface details |
| GET | `/device/lldp-cdp-neighbors` | Get LLDP neighbors |
| GET | `/device/ssids` | Get Device SSIDs |
| GET | `/device/physical` | Get device physical details |
| GET | `/device/fabric` | Get device fabric details |
| POST | `/device/sync` | Sync the managed devices to clear the device inconsistencies |
| POST | `/retrieve-services` | Retrieve brief/details of L2 Vsn,L3 Vsn, Vlan and Vrf services |
| POST | `/services/retrieve-vlans` | Retrieve brief/details of Vlan Services |
| POST | `/services/retrieve-vrfs` | Retrieve brief/details of Vrf Services |
| POST | `/services/retrieve-l2s` | Retrieve brief/details of L2 Services |
| POST | `/services/retrieve-l3s` | Retrieve brief/details of L3 Services |
| GET | `/schemas` | Get schemas |
| GET | `/supported-schemas` | Get supported schemas |
| GET | `/suggestions` | Get suggestions |
| POST | `/refresh/group` | Refresh Group Topology |
| GET | `/custom-logging` | Retrieve the custom logging configuration |
| POST | `/custom-logging` | Create the custom logging |
| DELETE | `/custom-logging` | Reset the custom logging |
| POST | `/utilities/service-probe-vlan/start` | Start VLAN Service Probe Operation |
| POST | `/utilities/service-probe-vlan/stop` | Stop Service Probe VLAN |
| GET | `/utilities/service-probe-vlan/probe-data` | Get Service Probe VLAN Data |

## POST `/retrieve-topology`

Operation: `RetrieveTopology`

Retrieve Network Topology

Retrieves comprehensive network topology data including nodes, edges, and custom positioning information. This endpoint supports multiple topology types (physical, fabric, service) and view types (map, abstract, list). The response includes hierarchical node structures with detailed device and group information, interconnection data through edges, and user-customized positioning for visualization purposes. **Use Cases:** - Initial topology loading for network visualization - Refreshing topology data after network changes - Filtering topology by specific criteria (search, node states, etc.) - Supporting different visualization views (map-based, abstract diagrams) **Performance Considerations:** - Large topologies may require pagination or filtering - Consider using specific topology types to reduce response size - Custom positions are cached and updated incrementally

Tags: `Topology Management`

Request body:

- `application/json` — TopologyCriteria

Responses:

- `200` — Successfully retrieved topology data. The response contains nodes representing network devices and groups, edges representing connections between nodes, and custom positioning data for visualization.
- `400` — Bad Request - Invalid criteria provided. This can occur when: - Invalid topology type specified - Conflicting view type and topology type combination - Invalid UUID format for nodeID - Malformed…
- `500` — Internal Server Error - Unexpected error during topology retrieval. This occurs when: - Database connectivity issues - Internal service failures - Topology calculation errors

## POST `/retrieve-topology/device`

Operation: `RetrieveTopologyDevices`

Retrieve Device Topology Data

Retrieves comprehensive device information within the topology context, providing detailed device attributes, operational status, and relationships to other network elements. This endpoint focuses on device-specific data within the topology framework, including: - **Device Attributes**: Hardware specifications, software versions, and capabilities - **Operational Status**: Current device state, health metrics, and performance indicators - **Network Relationships**: Device roles, connections, and dependencies within the topology - **Management Information**: Device discovery details, monitoring status, and configuration state **Use Cases:** - Device inventory and asset management - Device health monitoring and status reporting - Topology-aware device troubleshooting - Integration with device management workflows - Network documentation and compliance reporting **Performance Considerations:** - Response size varies based on the number of devices and detail level requested - Consider filtering criteria to optimize response time and size - Device data is refreshed based on discovery intervals and real-time polling

Tags: `Topology Management`

Request body:

- `application/json` — TopologyDeviceCriteria

Responses:

- `200` — OK

## POST `/retrieve-topology/link`

Operation: `RetrieveTopologyLinks`

Retrieve Link Topology Data

Retrieves comprehensive link information within the topology context, providing detailed connectivity data, relationship mappings, and interconnection analytics between network elements. This endpoint specializes in link-specific topology data, including: - **Physical Connections**: Direct physical links between devices and ports - **Logical Associations**: VLAN trunks, LAG configurations, and virtual connections - **Link Properties**: Bandwidth, utilization, duplex settings, and operational parameters - **Relationship Context**: How links fit within the broader network topology structure - **Status Information**: Link state, health metrics, and performance indicators **Use Cases:** - Network connectivity analysis and path discovery - Link capacity planning and bandwidth management - Topology-aware network troubleshooting and fault isolation - Network documentation and relationship mapping - Integration with network monitoring and alerting systems **Performance Considerations:** - Response includes detailed link metadata which may result in larger payloads - Filter criteria can significantly reduce response time for large topologies - Link status information reflects real-time or near real-time device polling data

Tags: `Topology Management`

Request body:

- `application/json` — TopologyLinkCriteria

Responses:

- `200` — OK

## POST `/hide`

Operation: `Hide`

Hide Node or Link

Selectively hides specific nodes or links from topology visualizations to improve diagram clarity, reduce visual complexity, and create focused network views for specific analysis or presentation purposes. This operation provides granular control over topology visibility, supporting: - **Selective Hiding**: Hide individual nodes, links, or groups of network elements - **View Customization**: Create simplified views for different audiences or use cases - **Focus Management**: Reduce visual noise to highlight critical network paths or components - **Presentation Support**: Generate clean topology diagrams for documentation or presentations - **Troubleshooting Aid**: Hide non-relevant elements to focus on problem areas **Hide Operation Details:** - Hidden elements are removed from visual representation but remain in the data model - Hide state is maintained per user session or can be made persistent - Multiple elements can be hidden in a single operation - Hidden elements can be restored using the unhide operation **Use Cases:** - Creating simplified network diagrams for executive presentations - Focusing troubleshooting efforts on specific network segments - Generating role-specific topology views (access layer, core, etc.) - Reducing complexity for training and documentation purposes - Supporting network change management workflows **Operational Considerations:** - Hide operations are reversible and non-destructive - Hidden elements maintain their relationships and can affect…

Tags: `Hide Node or Link Management`

Request body:

- `application/json` — HideUnhideParamInfo

Responses:

- `200` — Hide of node or links are successful.
- `400` — Bad Request - The request was invalid or cannot be otherwise served.
- `404` — Not Found - The specified resource could not be found.
- `500` — Internal Server Error - An error occurred on the server.

## POST `/unhide`

Operation: `Unhide`

Unhide Node or Link

Restores visibility of previously hidden nodes or links in topology visualizations, returning network elements to their normal display state and re-enabling their participation in visual analysis and interactive operations. This operation provides comprehensive visibility restoration capabilities: - **Selective Restoration**: Unhide specific nodes, links, or element groups - **Bulk Operations**: Restore multiple hidden elements in a single request - **State Management**: Manage visibility state across different topology views - **Recovery Support**: Restore accidentally hidden critical network elements - **View Completion**: Return to full topology visibility for comprehensive analysis **Unhide Operation Details:** - Restored elements immediately become visible in topology visualizations - All relationships and connections are re-established in the visual representation - Previously hidden elements retain their original positioning and properties - Unhide operations can be applied to elements hidden in current or previous sessions **Use Cases:** - Recovering from accidental hide operations - Transitioning from focused to comprehensive network views - Restoring full topology visibility after targeted analysis - Supporting dynamic visualization workflows - Enabling collaborative topology analysis with shared visibility states **Operational Considerations:** - Unhide operations are immediate and affect real-time topology displays - Consider performance impact when unhiding…

Tags: `Unhide Node or Link Management`

Request body:

- `application/json` — HideUnhideParamInfo

Responses:

- `200` — Hide of node or links are successful.
- `400` — Bad Request - The request was invalid or cannot be otherwise served.
- `404` — Not Found - The specified resource could not be found.
- `500` — Internal Server Error - An error occurred on the server.

## GET `/group`

Operation: `GetGroupHierarchy`

Get Group Hierarchy

Retrieves the complete organizational group hierarchy structure that defines how network devices and elements are logically organized within the management framework. This endpoint provides comprehensive group structure information including: - **Hierarchical Organization**: Multi-level group structures with parent-child relationships - **Group Membership**: Device assignments and group population details - **Organizational Context**: Business logic groupings such as locations, departments, or functions - **Management Scope**: Access control and administrative boundary definitions - **Metadata Information**: Group descriptions, properties, and custom attributes **Group Hierarchy Features:** - **Nested Structures**: Support for complex multi-level organizational hierarchies - **Dynamic Membership**: Groups can contain devices, sub-groups, or mixed memberships - **Role-Based Organization**: Groups aligned with network roles, locations, or business units - **Inheritance Properties**: Configuration and policy inheritance through hierarchy levels **Use Cases:** - Generating organizational network diagrams and documentation - Supporting role-based access control and administrative workflows - Enabling hierarchical network management and policy deployment - Facilitating network segmentation and logical organization - Integration with identity management and organizational directory systems **Performance Considerations:** - Response size scales with organizational complexity and…

Tags: `Topology Management`

Responses:

- `200` — OK

## GET `/tags`

Operation: `GetTags`

Retrieve Tags

Retrieve tags with filtering and pagination support

Tags: `Tag Management`

Parameters:

- `page_number` query, optional (number)
- `filter` query, optional (string)
- `sort` query, optional (string)
- `page_size` query, optional (number)

Responses:

- `200` — Successfully retrieved tags
- `400` — Bad Request
- `500` — Internal Server Error

## POST `/tags`

Operation: `CreateTag`

Create a new tag

Tags: `Tag Management`

Request body:

- `application/json` — tagInfo

Responses:

- `200` — Successfully created tag

## PUT `/tags`

Operation: `UpdateTag`

Update a tag

Tags: `Tag Management`

Request body:

- `application/json` — tagInfo

Responses:

- `200` — Successfully updated tag

## DELETE `/tags`

Operation: `DeleteTags`

Delete a tag

Tags: `Tag Management`

Request body:

- `application/json` — UUIDList

Responses:

- `200` — Successfully deleted tag
- `204` — Successfully deleted tag

## POST `/tags/entities`

Operation: `AssociateTagEntities`

Associate tags with entities

Tags: `Tag Management`

Request body:

- `application/json` — AssociateEntities

Responses:

- `200` — Tags associated with entities successfully.
- `400` — Invalid request parameters or format.
- `404` — One or more entity/tags not found.
- `500` — Error occurred while associating tags.

## DELETE `/tags/entities`

Operation: `DisAssociateTagEntities`

Disassociate tags from nodes

Tags: `Tag Management`

Request body:

- `application/json` — AssociateEntities

Responses:

- `200` — Tags disassociated from entities successfully.
- `400` — Invalid request parameters or format.
- `404` — One or more entity/tags not found.
- `500` — Error occurred while disassociating tags.

## GET `/user/preferences`

Operation: `GetUserPreferences`

getUserPreferences

Retrieves user-specific preferences and configuration settings that personalize the network management interface and customize the user experience across different application features. This endpoint provides access to comprehensive user preference data including: - **Interface Customization**: Dashboard layouts, widget configurations, and display preferences - **Behavioral Settings**: Default views, auto-refresh intervals, and interaction preferences - **Personalization Data**: Custom filters, saved searches, and bookmark configurations - **Accessibility Options**: Display scaling, color themes, and accessibility accommodations - **Feature Toggles**: User-specific feature enablement and experimental feature access **Preference Categories:** - **Visualization**: Topology view preferences, chart types, and display options - **Workflow**: Default actions, confirmation settings, and automation preferences - **Notifications**: Alert preferences, delivery methods, and escalation settings - **Security**: Session management, authentication preferences, and privacy settings **Use Cases:** - Loading personalized user interface configurations on login - Synchronizing user preferences across multiple sessions or devices - Supporting user experience customization and accessibility requirements - Enabling preference backup and restoration workflows - Integration with single sign-on and identity management systems **Data Management:** - Preferences are stored per user and isolated between…

Tags: `User Preferences`

Parameters:

- `key` query, optional (string) — key of preferences

Responses:

- `200` — OK

## POST `/user/preferences`

Operation: `CreateUserPreferences`

postUserPreferences

Creates or updates user-specific preferences and configuration settings to personalize the network management interface and maintain consistent user experience across sessions. This endpoint enables comprehensive preference management including: - **Preference Creation**: Establish new user-specific configuration settings - **Preference Updates**: Modify existing settings while preserving unrelated preferences - **Bulk Operations**: Create or update multiple preference items in a single request - **Validation**: Ensure preference values conform to expected formats and constraints - **Persistence**: Store preferences securely with appropriate user data protection **Supported Preference Types:** - **Interface Settings**: Layout configurations, theme selections, and display customizations - **Operational Defaults**: Default time ranges, refresh intervals, and view preferences - **Workflow Configurations**: Custom automation settings and process preferences - **Security Preferences**: Session timeout preferences and security feature settings - **Integration Settings**: Third-party tool integrations and API preferences **Operation Characteristics:** - **Atomic Updates**: All preferences in a request are updated together or none are updated - **Merge Behavior**: New preferences are merged with existing ones, preserving unspecified settings - **Validation**: Invalid preference values result in request rejection with detailed error information - **Audit Trail**: Preference changes…

Tags: `User Preferences`

Request body:

- `application/json` — array

Responses:

- `200` — Successfully created/updated user preference(s)

## DELETE `/user/preferences`

Operation: `DeleteUserPreferences`

deleteUserPreferences

Deletes specific user preferences to reset customizations, clean up obsolete settings, or restore default application behavior for targeted preference categories. This endpoint provides granular preference removal capabilities including: - **Selective Deletion**: Remove specific preference keys while preserving others - **Category Cleanup**: Delete entire preference categories or groups - **Reset Functionality**: Restore specific settings to their default values - **Data Cleanup**: Remove deprecated or invalid preference entries - **Bulk Operations**: Delete multiple related preferences in a single operation **Deletion Behavior:** - **Targeted Removal**: Only preferences matching the specified key are deleted - **Cascading Effects**: Related preferences may be affected based on dependencies - **Default Restoration**: Deleted preferences revert to system or application defaults - **Audit Logging**: Deletion operations are logged for security and troubleshooting - **Validation**: Ensures critical system preferences cannot be accidentally deleted **Use Cases:** - Resetting user interface to default settings for troubleshooting - Cleaning up user accounts during offboarding or role changes - Removing obsolete preferences after application updates - Supporting user-initiated preference reset workflows - Enabling preference troubleshooting and support scenarios - Data privacy compliance and user data management **Safety Considerations:** - **Irreversible Operation**: Deleted…

Tags: `User Preferences`

Parameters:

- `key` query, required (string) — key of preferences

Responses:

- `200` — Successfully deleted user preferences
- `204` — Successfully deleted user preferences

## POST `/custom-positions`

Operation: `UpdateCustomPosition`

Update the Custom Position

Creates or updates custom positioning data for network elements in topology visualizations, enabling users to maintain consistent, personalized network diagram layouts that enhance understanding and presentation of network infrastructure. This endpoint provides comprehensive position management capabilities including: - **Element Positioning**: Define precise X,Y coordinates for nodes and network elements - **Layout Persistence**: Save custom arrangements that persist across sessions and users - **Multi-View Support**: Maintain different positioning schemes for various topology views - **Collaborative Layouts**: Share positioning schemes across teams or user groups - **Dynamic Updates**: Modify positions in real-time during interactive topology sessions **Positioning Features:** - **Coordinate Systems**: Support for various coordinate systems and scaling factors - **Element Relationships**: Maintain relative positioning and alignment between connected elements - **Layout Templates**: Create reusable positioning patterns for similar network structures - **Constraint Handling**: Respect positioning constraints and collision detection - **Version Control**: Track changes to positioning schemes over time **Use Cases:** - Creating standardized network documentation with consistent element placement - Maintaining logical network diagrams that reflect physical or functional relationships - Supporting collaborative network design and planning sessions - Enabling presentation-ready…

Tags: `Topology Management`

Request body:

- `application/json` — object

Responses:

- `200` — Successfully updated custom positions

## DELETE `/custom-positions`

Operation: `DeleteCustomPosition`

Delete custom positions

Deletes custom positioning data for specific topology views, resetting network elements to their default algorithmic positions and cleaning up personalized layout configurations. This operation provides comprehensive position data cleanup including: - **View-Specific Deletion**: Remove custom positions for specific topology chart contexts - **Selective Reset**: Target specific topology views while preserving others - **Layout Cleanup**: Remove obsolete or corrupted positioning data - **Default Restoration**: Return elements to automatic layout algorithm positioning - **Data Maintenance**: Clean up positioning data during system maintenance or migration **Deletion Behavior:** - **Targeted Removal**: Only positions associated with the specified chart hash are deleted - **Automatic Fallback**: Elements immediately revert to default algorithmic positioning - **Cascading Effects**: Related positioning constraints and relationships are also removed - **Performance Optimization**: Deletion operation is optimized for minimal disruption - **Audit Trail**: Deletion operations are logged for troubleshooting and recovery **Use Cases:** - Resetting topology layouts to default algorithmic positioning - Cleaning up corrupted or invalid positioning data - Supporting topology view maintenance and optimization workflows - Enabling layout troubleshooting and problem resolution - Facilitating topology migration and system upgrades - Supporting user interface reset and recovery scenarios…

Tags: `Topology Management`

Parameters:

- `chartHash` query, required (string) — Chart hash for the topology

Responses:

- `200` — OK

## GET `/device/physical/link`

Operation: `getDevicePhysicalLinkDetails`

Get Physical Link Details

Retrieves comprehensive physical link information including port utilization statistics, traffic counters, error statistics, and operational details for both ends of a network link. This endpoint provides detailed insights into: - **Utilization Metrics**: Current and maximum bandwidth utilization percentages - **Traffic Statistics**: Packet and byte counters for unicast, broadcast, and multicast traffic - **Error Statistics**: Various error counters including discards, CRC errors, collisions - **Port Details**: Administrative and operational states, speed, duplex, media type - **LAG Information**: For aggregated links, includes member port details and protocols **Use Cases:** - Network performance monitoring and troubleshooting - Capacity planning and bandwidth analysis - Link health assessment and error detection - Integration with network monitoring systems **Performance Impact:** - Statistics are collected in real-time from network devices - Response time depends on device responsiveness and network latency

Tags: `Device Management`

Parameters:

- `linkID` query, required (string) — Unique identifier (UUID) of the physical link for which to retrieve detailed information. This corresponds to the edge ID in topology data.
- `topologyType` query, required (TopologyType) — Type of topology context from which the link details are being queried. This affects which layer of information is emphasized in the response. - `physical`: Focus on physical layer details and statistics - `fabric`: Include fabric-aware…

Responses:

- `200` — Successfully retrieved physical link details. The response includes comprehensive information about both ports connected by the link, traffic statistics, error counters, and configuration details.
- `400` — Bad Request - Invalid parameters provided: - Invalid UUID format for linkID - Invalid topologyType value - Missing required parameters
- `500` — Internal Server Error - Failed to retrieve link details: - Device communication failure - Database query error - Service unavailable

## GET `/device/fabric/link`

Operation: `getDeviceFabricLinkDetails`

Get device fabric link details

Retrieves comprehensive operational and configuration details for fabric network links, providing deep insights into fabric connectivity, authentication status, and performance characteristics essential for fabric network management and troubleshooting. This endpoint specializes in fabric-specific link information including: - **Fabric Authentication**: Authentication protocols, key management, and security status - **Operational State**: Link operational status, fabric role, and connectivity health - **Performance Metrics**: Fabric-specific performance indicators and quality metrics - **Configuration Details**: Fabric protocols, parameters, and administrative settings - **Relationship Context**: How fabric links integrate with the broader network architecture **Fabric Link Characteristics:** - **Security Integration**: Authentication mechanisms, encryption status, and trust relationships - **Protocol Analysis**: Fabric-specific protocol states, negotiations, and capabilities - **Health Monitoring**: Fabric link health, error rates, and performance degradation indicators - **Dynamic Configuration**: Runtime configuration changes and adaptive protocol behaviors - **Interoperability**: Multi-vendor fabric integration and compatibility information **Use Cases:** - Monitoring fabric network health and authentication status - Troubleshooting fabric connectivity and security issues - Analyzing fabric performance and optimization opportunities - Supporting fabric network design and…

Tags: `Device Management`

Parameters:

- `linkID` query, required (string) — UUID of the link (edge)
- `topologyType` query, required (TopologyType) — Type of the topology from which link details are queried

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve fabric link details.

## GET `/device/ports`

Operation: `getDeviceInterfaceDetails`

Get device interface details

Retrieves comprehensive interface information for network devices, providing detailed visibility into both wired and wireless interfaces including configuration, status, performance metrics, and operational characteristics. This endpoint provides extensive interface data including: - **Interface Inventory**: Complete enumeration of all device interfaces (physical and logical) - **Configuration Details**: Administrative settings, protocol configurations, and feature enablement - **Operational Status**: Real-time interface states, link status, and health indicators - **Performance Metrics**: Traffic statistics, utilization rates, error counters, and quality metrics - **Capability Information**: Interface speeds, duplex modes, media types, and supported features **Interface Categories:** - **Physical Interfaces**: Ethernet ports, fiber connections, and copper interfaces - **Logical Interfaces**: VLANs, sub-interfaces, and protocol-specific virtual interfaces - **Wireless Interfaces**: Radio interfaces, SSID configurations, and wireless client associations - **Management Interfaces**: Out-of-band management, console ports, and administrative interfaces - **Aggregate Interfaces**: Link aggregation groups (LAGs), port channels, and bonded interfaces **Data Richness:** - **Historical Context**: Interface change history and configuration evolution - **Dependency Mapping**: Interface relationships and service dependencies - **Troubleshooting Data**: Error patterns, performance…

Tags: `Device Management`

Parameters:

- `deviceID` query, required (string) — UUID of the device (node)

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve device interface details.

## GET `/device/lldp-cdp-neighbors`

Operation: `getDeviceLLDPNeighbors`

Get LLDP neighbors

Retrieves comprehensive Link Layer Discovery Protocol (LLDP) and Cisco Discovery Protocol (CDP) neighbor information, providing essential network discovery data for topology mapping, connectivity validation, and network documentation workflows. This endpoint provides detailed neighbor discovery information including: - **Protocol Support**: Both LLDP (IEEE 802.1AB) and CDP neighbor discovery data - **Neighbor Identity**: Device names, system descriptions, and management addresses - **Connection Details**: Local and remote port information, interface mappings, and link characteristics - **Capability Information**: Discovered device capabilities, supported protocols, and system features - **Network Context**: VLAN information, network policies, and service advertisements **Discovery Protocol Features:** - **Multi-Protocol Support**: Unified view of LLDP and CDP discovery information - **Real-Time Data**: Current neighbor states with timestamp and aging information - **Detailed Attributes**: Extended device information including software versions and serial numbers - **Topology Correlation**: Neighbor data correlation with topology discovery and validation - **Change Detection**: Neighbor changes, additions, and removals with historical context **Neighbor Information Categories:** - **Device Identification**: System names, descriptions, chassis IDs, and management addresses - **Interface Mapping**: Local and remote port details, interface descriptions, and connection types -…

Tags: `Device Management`

Parameters:

- `deviceID` query, required (string) — UUID of the device (node)

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve LLDP/CDP neighbors.

## GET `/device/ssids`

Operation: `getDeviceSSIDs`

Get Device SSIDs

Retrieves comprehensive Service Set Identifier (SSID) information for wireless network devices, providing detailed visibility into wireless network configurations, security settings, and operational characteristics essential for wireless network management. This endpoint provides extensive wireless SSID data including: - **SSID Configuration**: Network names, broadcasting settings, and availability status - **Security Settings**: Authentication methods, encryption protocols, and access control configurations - **Operational Metrics**: Connection statistics, client associations, and performance indicators - **Coverage Information**: Signal strength data, channel assignments, and coverage area details - **Service Features**: Quality of Service settings, bandwidth management, and advanced wireless features **SSID Categories:** - **Guest Networks**: Public access SSIDs with captive portal and isolation configurations - **Corporate Networks**: Enterprise SSIDs with 802.1X authentication and policy enforcement - **IoT Networks**: Dedicated SSIDs for Internet of Things devices with specialized security - **Management Networks**: Administrative SSIDs for device management and maintenance access - **Service Networks**: Specialized SSIDs for specific applications or user groups **Wireless Network Details:** - **Security Protocols**: WPA3, WPA2, WEP, and enterprise authentication configurations - **Access Control**: MAC filtering, time-based restrictions, and user group assignments -…

Tags: `Device Management`

Parameters:

- `deviceID` query, required (string) — UUID of the device (node)

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve device SSIDs.

## GET `/device/physical`

Operation: `getDevicePhysicalDetails`

Get device physical details

Retrieves comprehensive physical device information including hardware specifications, component details, environmental status, and operational characteristics essential for device lifecycle management, capacity planning, and infrastructure operations. This endpoint provides extensive physical device data including: - **Hardware Specifications**: CPU, memory, storage capacity, and processing capabilities - **Component Inventory**: Modules, line cards, power supplies, and field-replaceable units - **Environmental Monitoring**: Temperature sensors, fan status, power consumption, and cooling metrics - **Asset Information**: Serial numbers, model identifiers, manufacturing details, and warranty status - **Operational Status**: Device health indicators, uptime statistics, and performance metrics **Physical Infrastructure Details:** - **Chassis Information**: Form factor, slot configurations, and expansion capabilities - **Power Systems**: Power supply status, redundancy configuration, and energy efficiency metrics - **Cooling Systems**: Fan operation, thermal management, and environmental threshold monitoring - **Interface Hardware**: Port counts, interface types, transceivers, and physical connectivity options - **Storage Systems**: Flash memory, configuration storage, and logging capacity information **Asset Management Features:** - **Lifecycle Tracking**: Installation dates, firmware versions, and update history - **Inventory Management**: Component part numbers, replacement…

Tags: `Device Management`

Parameters:

- `deviceID` query, required (string) — UUID of the device (node)

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve device physical details.

## GET `/device/fabric`

Operation: `getDeviceFabricDetails`

Get device fabric details

Retrieves comprehensive fabric-specific device configuration and operational state information, providing deep insights into fabric network participation, roles, capabilities, and performance characteristics essential for fabric network management and optimization. This endpoint provides extensive fabric device data including: - **Fabric Role Information**: Device function within fabric topology (spine, leaf, border, etc.) - **Protocol Configuration**: Fabric routing protocols, authentication settings, and service parameters - **Operational State**: Fabric connectivity status, peer relationships, and health indicators - **Performance Metrics**: Fabric-specific traffic statistics, convergence times, and efficiency measures - **Service Integration**: Overlay services, tenant configurations, and multi-tenancy support **Fabric Architecture Details:** - **Topology Participation**: Device position and role within fabric hierarchy and design patterns - **Protocol Support**: BGP EVPN, VXLAN, and other fabric protocol configurations and states - **Authentication Systems**: Fabric security mechanisms, key management, and trust relationships - **Load Balancing**: Traffic distribution, path selection, and fabric optimization configurations - **Redundancy Features**: High availability configurations, failover mechanisms, and resilience features **Service Capabilities:** - **Overlay Networks**: VXLAN tunnels, service VNIs, and overlay-to-underlay mappings - **Multi-Tenancy**: Tenant…

Tags: `Device Management`

Parameters:

- `deviceID` query, required (string) — UUID of the device (node)

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to retrieve device fabric details.

## POST `/device/sync`

Operation: `clearDeviceInconsistencies`

Sync the managed devices to clear the device inconsistencies

Performs comprehensive device inventory synchronization between the management system and cloud-based device registry to identify and resolve inconsistencies, ensuring accurate device records and eliminating orphaned or stale device entries. This operation provides robust device consistency management including: - **Inventory Reconciliation**: Compare local device records with authoritative cloud inventory - **Inconsistency Detection**: Identify orphaned devices, duplicate entries, and stale records - **Automated Cleanup**: Remove devices that no longer exist in the authoritative source - **Data Validation**: Verify device attributes, status information, and relationship integrity - **Audit Trail Generation**: Document all synchronization actions for compliance and troubleshooting **Synchronization Process:** - **Discovery Phase**: Enumerate all managed devices in local inventory - **Validation Phase**: Cross-reference with cloud device registry and authoritative sources - **Analysis Phase**: Identify inconsistencies, conflicts, and resolution requirements - **Reconciliation Phase**: Apply corrections, removals, and updates based on policy - **Verification Phase**: Confirm synchronization success and generate completion reports **Inconsistency Resolution:** - **Orphaned Devices**: Remove local devices that no longer exist in cloud inventory - **Stale Records**: Update device information that has changed in authoritative sources - **Duplicate Entries**: Consolidate multiple…

Tags: `Device Management`

Request body:

- `application/json` — deviceSyncAttribute

Responses:

- `200` — OK
- `400` — Bad Request - Invalid request parameters or format.
- `500` — Internal Server Error - Failed to sync devices.

## POST `/retrieve-services`

Operation: `RetrieveServices`

Retrieve brief/details of L2 Vsn,L3 Vsn, Vlan and Vrf services

Retrieves comprehensive network service information across multiple service types including Layer 2 Virtual Service Networks (VSNs), Layer 3 VSNs, VLANs, and VRF services, providing unified visibility into network service configurations, dependencies, and operational status. This endpoint provides extensive multi-service data including: - **Service Inventory**: Complete enumeration of all configured network services - **Configuration Details**: Service parameters, policies, and administrative settings - **Operational Status**: Real-time service health, connectivity, and performance indicators - **Dependency Mapping**: Inter-service relationships, prerequisites, and impact analysis - **Resource Utilization**: Bandwidth consumption, endpoint counts, and capacity metrics **Service Categories Supported:** - **Layer 2 VSN Services**: Ethernet VPN services, bridge domains, and switching services - **Layer 3 VSN Services**: IP VPN services, routing domains, and inter-subnet connectivity - **VLAN Services**: Virtual LAN configurations, trunking, and access control - **VRF Services**: Virtual Routing and Forwarding instances, route tables, and isolation - **Hybrid Services**: Multi-layer services combining L2 and L3 functionality **Service Information Depth:** - **Brief Mode**: Summary information optimized for overview and listing scenarios - **Detailed Mode**: Comprehensive configuration and operational data for analysis - **Relationship Data**: Service interdependencies, shared…

Tags: `Service Management`

Request body:

- `application/json` — ServicesCriteria

Responses:

- `200` — OK

## POST `/services/retrieve-vlans`

Operation: `RetrieveVlanServices`

Retrieve brief/details of Vlan Services

Retrieves comprehensive Virtual LAN (VLAN) service information providing detailed visibility into VLAN configurations, assignments, traffic patterns, and operational characteristics essential for Layer 2 network service management and optimization. This endpoint provides extensive VLAN service data including: - **VLAN Configuration**: VLAN IDs, names, descriptions, and administrative settings - **Port Assignments**: Interface mappings, tagging configurations, and access/trunk modes - **Traffic Analysis**: VLAN traffic patterns, utilization statistics, and performance metrics - **Spanning Tree Integration**: STP/RSTP/MSTP configurations and operational states - **Security Policies**: VLAN isolation, access control, and security feature configurations **VLAN Service Categories:** - **Access VLANs**: End-user access network segments with host connectivity - **Trunk VLANs**: Inter-switch communication and network infrastructure VLANs - **Management VLANs**: Administrative and management traffic isolation - **Guest VLANs**: Visitor and temporary access network segments - **Service VLANs**: Dedicated VLANs for specific applications or services **Configuration and Status Details:** - **Port Membership**: Complete interface assignment and participation details - **VLAN Databases**: VLAN table entries, learning states, and MAC address management - **Quality of Service**: VLAN-based QoS policies, traffic prioritization, and bandwidth management - **Interoperability**: Multi-vendor…

Tags: `Service Management`

Request body:

- `application/json` — ServicesCriteria

Responses:

- `200` — OK

## POST `/services/retrieve-vrfs`

Operation: `RetrieveVrfServices`

Retrieve brief/details of Vrf Services

Retrieves comprehensive Virtual Routing and Forwarding (VRF) service information providing detailed visibility into Layer 3 routing domain configurations, isolation mechanisms, and operational characteristics essential for multi-tenant and segmented network management. This endpoint provides extensive VRF service data including: - **VRF Configuration**: VRF instances, route distinguishers, and administrative settings - **Routing Tables**: Per-VRF routing information, route targets, and forwarding entries - **Interface Assignments**: VRF-aware interfaces, sub-interfaces, and service mappings - **Route Distribution**: BGP VPNv4/VPNv6 configurations, route import/export policies - **Isolation Verification**: Traffic separation validation and security boundary enforcement **VRF Service Categories:** - **Customer VRFs**: Dedicated routing domains for individual customers or tenants - **Service VRFs**: Specialized routing instances for specific network services - **Management VRFs**: Administrative traffic isolation and out-of-band management - **Global VRFs**: Default routing instances and shared network resources - **Transit VRFs**: Inter-VRF communication and service chaining instances **Routing and Connectivity Details:** - **Route Targets**: Import/export route target configurations and community management - **Redistribution Policies**: Inter-VRF and inter-protocol route redistribution - **Connectivity Matrix**: VRF-to-VRF communication policies and restrictions - **MPLS…

Tags: `Service Management`

Request body:

- `application/json` — ServicesCriteria

Responses:

- `200` — OK

## POST `/services/retrieve-l2s`

Operation: `RetrieveL2Services`

Retrieve brief/details of L2 Services

Retrieves comprehensive Layer 2 service information providing detailed visibility into switching services, bridge domains, and Layer 2 connectivity configurations essential for data link layer network service management and optimization. This endpoint provides extensive Layer 2 service data including: - **Bridge Domain Configuration**: L2 service instances, bridge tables, and forwarding behavior - **VLAN Integration**: VLAN mappings, service VLAN assignments, and tagging configurations - **MAC Learning**: MAC address tables, learning policies, and aging configurations - **Flooding Control**: Broadcast, multicast, and unknown unicast handling policies - **Service Connectivity**: Endpoint mappings, pseudowire configurations, and attachment circuits **Layer 2 Service Categories:** - **Ethernet Line Services**: Point-to-point Ethernet connectivity and dedicated circuits - **Ethernet LAN Services**: Multipoint Ethernet services and shared connectivity - **VPLS Services**: Virtual Private LAN Service instances and mesh connectivity - **EVPN Services**: Ethernet VPN services with BGP-based control plane - **Bridge Services**: Traditional bridging and switching service configurations **Service Configuration Details:** - **Service Policies**: Traffic handling, filtering, and quality of service configurations - **Redundancy Features**: Protection switching, link aggregation, and failover mechanisms - **Traffic Engineering**: Bandwidth management, traffic shaping, and congestion…

Tags: `Service Management`

Request body:

- `application/json` — ServicesCriteria

Responses:

- `200` — OK

## POST `/services/retrieve-l3s`

Operation: `RetrieveL3Services`

Retrieve brief/details of L3 Services

Retrieves comprehensive Layer 3 service information providing detailed visibility into routing services, IP connectivity, and Layer 3 forwarding configurations essential for network layer service management and optimization. This endpoint provides extensive Layer 3 service data including: - **Routing Service Configuration**: L3 service instances, routing domains, and forwarding policies - **IP Address Management**: Subnet assignments, address pools, and IP allocation policies - **Routing Protocol Integration**: OSPF, BGP, EIGRP, and static route configurations - **Inter-Subnet Connectivity**: Gateway services, routing between network segments - **Service Quality**: QoS policies, traffic classification, and performance management **Layer 3 Service Categories:** - **IP VPN Services**: Layer 3 VPN instances with customer routing table isolation - **Internet Services**: Internet connectivity, NAT services, and public IP management - **Intranet Services**: Internal routing services and enterprise connectivity - **Extranet Services**: Partner connectivity and controlled external access - **Managed Routing**: Provider-managed routing services and customer premise equipment **Routing and Connectivity Features:** - **Route Management**: Route tables, routing policies, and path selection algorithms - **Load Balancing**: Multi-path routing, traffic distribution, and failover configurations - **Security Integration**: Route filtering, access control lists, and security policy…

Tags: `Service Management`

Request body:

- `application/json` — ServicesCriteria

Responses:

- `200` — OK

## GET `/schemas`

Operation: `GetSchemas`

Get schemas

Retrieves comprehensive schema information for various application features and API components, providing structured metadata essential for dynamic form generation, data validation, and integration with automated systems and development tools. This endpoint provides extensive schema data including: - **Data Structure Definitions**: Complete field specifications, data types, and validation rules - **Form Generation Metadata**: UI rendering hints, field ordering, and user interface guidelines - **Validation Rules**: Field constraints, format requirements, and business logic validation - **Relationship Definitions**: Inter-schema dependencies, foreign key relationships, and data linkages - **Version Information**: Schema versioning, compatibility details, and evolution tracking **Schema Categories:** - **Configuration Schemas**: Device configuration, service setup, and system parameter schemas - **Operational Schemas**: Status reporting, monitoring data, and runtime information structures - **User Interface Schemas**: Form definitions, dashboard configurations, and user interaction models - **Integration Schemas**: API request/response formats, data exchange protocols, and external system interfaces - **Validation Schemas**: Data quality rules, compliance checks, and constraint definitions **Schema Applications:** - **Dynamic UI Generation**: Automatically generate user interfaces based on schema definitions - **Data Validation**: Implement client-side and server-side…

Tags: `Schemas`

Parameters:

- `type` query, required (SchemaType) — Type of schema which needs to be returned

Responses:

- `200` — OK

## GET `/supported-schemas`

Operation: `GetSupportedSchema`

Get supported schemas

Retrieves supported identifiers for devices and services used in tag policies, enabling consistent rule definitions, validation, and automation across the system. This endpoint provides structured metadata about the **criteria fields** that can be applied when creating or evaluating tagging policies. The response contains two categories of identifiers: - **Device Criteria**: Fields supported for device-level tagging, such as device type, model, location, and link - **Service Criteria**: Fields supported for service-level tagging, such as service name, service number, VLAN number, and VRF name **Schema Categories:** - **Device Identifiers**: Canonical attributes used for classifying and grouping devices - **Service Identifiers**: Canonical attributes used for classifying and grouping services **Schema Applications:** - **Dynamic UI Generation**: Automatically generate user interfaces based on schema definitions - **Data Validation**: Implement client-side and server-side validation using schema rules - **API Documentation**: Auto-generate API documentation with complete parameter specifications - **Code Generation**: Generate client libraries, data models, and integration code - **Configuration Management**: Validate configuration files and parameter settings **Use Cases:** - Define tag policies that operate on standardized device or service attributes - Dynamically generate user interfaces for selecting policy identifiers - Validate client-side input when creating or…

Tags: `Schemas`

Responses:

- `200` — OK

## GET `/suggestions`

Operation: `GetSuggestions`

Get suggestions

Provides intelligent auto-completion and search suggestions to enhance user experience and improve search efficiency across various application features and data elements. This endpoint offers comprehensive suggestion capabilities including: - **Auto-Completion**: Real-time completion suggestions for partial search terms - **Contextual Suggestions**: Context-aware recommendations based on current application state - **Historical Patterns**: Suggestions based on user search history and common patterns - **Fuzzy Matching**: Intelligent matching for misspelled or partially remembered terms - **Categorized Results**: Organized suggestions by category, relevance, and data type **Suggestion Categories:** - **Device Names**: Network device hostnames, aliases, and identification strings - **Service Names**: Network service identifiers, descriptions, and service instances - **Configuration Parameters**: Setting names, parameter values, and configuration options - **User Entities**: User names, groups, roles, and organizational units - **Network Objects**: IP addresses, subnet ranges, VLAN IDs, and network identifiers - **Status Values**: Operational states, health indicators, and system status options **Search Enhancement Features:** - **Intelligent Ranking**: Relevance-based suggestion ordering with popularity weighting - **Multi-Match Support**: Suggestions matching multiple search criteria simultaneously - **Abbreviation Expansion**: Expand common abbreviations and acronyms into…

Tags: `General`

Parameters:

- `term` query, required (string) — term to search for completion

Responses:

- `200` — OK

## POST `/refresh/group`

Operation: `RefreshGroupTopology`

Refresh Group Topology

Initiates comprehensive topology refresh operations for group hierarchies to ensure current and accurate representation of network organizational structures and device relationships within the management system. This operation provides robust topology synchronization including: - **Group Hierarchy Refresh**: Update organizational group structures and membership - **Device Relationship Updates**: Refresh device-to-group assignments and dependencies - **Topology Validation**: Verify topology integrity and resolve inconsistencies - **Real-Time Synchronization**: Synchronize with current network state and device status - **Change Detection**: Identify and process topology changes since last refresh **Refresh Operation Scope:** - **Group Structure Updates**: Refresh hierarchical organization and parent-child relationships - **Membership Validation**: Verify device group memberships and resolve conflicts - **Dependency Resolution**: Update inter-group dependencies and service relationships - **Status Synchronization**: Refresh operational status and health indicators - **Metadata Updates**: Update group descriptions, properties, and custom attributes **Refresh Triggers:** - **Scheduled Refresh**: Regular topology updates based on configured intervals - **Manual Refresh**: User-initiated refresh for immediate topology updates - **Event-Driven Refresh**: Automatic refresh triggered by network changes or device events - **Bulk Operations**: Large-scale topology refresh after major…

Tags: `Topology Management`

Request body:

- `application/json` — RefreshCriteria

Responses:

- `202` — OK

## GET `/custom-logging`

Operation: `GetCustomLogging`

Retrieve the custom logging configuration

Tags: `Custom logging`

Parameters:

- `service` query, required (string)
- `logging_type` query, required (string)

Responses:

- `200` — Successfully retrieved custom logging configurations

## POST `/custom-logging`

Operation: `CreateCustomLogging`

Create the custom logging

Tags: `Custom logging`

Request body:

- `application/json` — array

Responses:

- `200` — Successfully created custom logging

## DELETE `/custom-logging`

Operation: `ResetCustomLogging`

Reset the custom logging

Tags: `Custom logging`

Parameters:

- `service` query, required (string)
- `logging_type` query, required (string)

Responses:

- `200` — Successfully reset the custom logging
- `204` — Successfully reset the custom logging

## POST `/utilities/service-probe-vlan/start`

Operation: `StartServiceProbeVLAN`

Start VLAN Service Probe Operation

Initiates a comprehensive VLAN service probe operation to validate VLAN availability and configuration across the network infrastructure. This utility performs automated testing to determine which VLANs are properly configured, accessible, and functional on the specified device. **Probe Operation Details:** - **VLAN Discovery**: Automatically detects configured VLANs within the specified range - **Connectivity Testing**: Validates VLAN reachability and proper forwarding - **Configuration Validation**: Checks VLAN settings, tagging, and port assignments - **IP Address Assignment**: Tests dynamic IP assignment capabilities (DHCP) - **Gateway Verification**: Validates default gateway accessibility per VLAN **Use Cases:** - **Network Commissioning**: Validate VLAN configuration during initial setup - **Troubleshooting**: Identify VLAN connectivity issues and misconfigurations - **Compliance Verification**: Ensure VLAN setup meets network policies - **Change Management**: Verify VLAN functionality after configuration changes - **Documentation**: Generate current VLAN availability reports **Operational Considerations:** - Probe operations are non-disruptive to production traffic - Maximum of 500 VLANs can be probed in a single operation - Concurrent probe operations on the same device are not allowed - Results are cached and available for retrieval during and after completion **Progress Tracking:** Use the returned `taskKey` to monitor progress via the…

Tags: `Service Probe Vlan`

Request body:

- `application/json` — ServiceProbeVLANStartRequest

Responses:

- `202` — Service probe operation has been successfully initiated and is running asynchronously. The operation will continue in the background, and progress can be monitored using the returned task key. **Next…
- `400` — Bad Request - Invalid probe configuration provided: **Common Issues:** - **Invalid VLAN Range**: Range format is incorrect or exceeds 500 VLANs - **Invalid Device ID**: Device UUID format is…
- `500` — Internal Server Error - Unexpected error during probe initiation: - System resource limitations - Database connectivity issues - Internal service failures

## POST `/utilities/service-probe-vlan/stop`

Operation: `StopServiceProbeVLAN`

Stop Service Probe VLAN

Terminates an active VLAN service probe operation, gracefully stopping the validation process and cleaning up allocated resources while preserving any results collected up to the point of termination. This endpoint provides comprehensive probe termination capabilities including: - **Graceful Termination**: Stop ongoing probe operations without data corruption - **Resource Cleanup**: Release network resources and probe-related system allocations - **Result Preservation**: Maintain partial probe results for analysis and reporting - **State Management**: Update probe operation status and completion tracking - **Audit Trail**: Log termination actions for compliance and troubleshooting **Termination Scenarios:** - **Manual Termination**: User-initiated stop for probe operations that are no longer needed - **Timeout Prevention**: Stop long-running probes before system timeout limits - **Resource Management**: Terminate probes to free resources for other operations - **Error Recovery**: Stop malfunctioning or stuck probe operations - **Maintenance Preparation**: Clear active probes before system maintenance **Operation Characteristics:** - **Immediate Response**: Stop commands are processed immediately with confirmation - **Safe Termination**: Probe operations are stopped safely without affecting network stability - **Result Availability**: Partial results remain accessible after termination - **Resource Recovery**: Network interfaces and system resources are properly released -…

Tags: `Service Probe Vlan`

Request body:

- `application/json` — ServiceProbeVLANStopRequest

Responses:

- `200` — Service probe stopped successfully

## GET `/utilities/service-probe-vlan/probe-data`

Operation: `GetServiceProbeVLANData`

Get Service Probe VLAN Data

Retrieves comprehensive VLAN service probe results and operational data, providing detailed insights into probe progress, validation outcomes, and network connectivity analysis essential for network troubleshooting and validation workflows. This endpoint provides extensive probe data including: - **Probe Results**: Detailed validation outcomes for each tested VLAN - **Progress Information**: Real-time status updates and completion progress - **Connectivity Analysis**: VLAN reachability, configuration validation, and performance metrics - **Error Diagnostics**: Detailed error information for failed VLAN validations - **Performance Metrics**: Response times, success rates, and network quality indicators **Data Retrieval Options:** - **Task-Based Retrieval**: Get results for a specific probe operation using task key - **Device-Based Retrieval**: Get all probe results associated with a specific device - **Real-Time Updates**: Monitor ongoing probe operations with live status information - **Historical Data**: Access completed probe results for analysis and reporting - **Filtered Results**: Retrieve specific subsets of probe data based on criteria **Probe Result Categories:** - **Successful Validations**: VLANs that passed all connectivity and configuration tests - **Failed Validations**: VLANs with connectivity issues, configuration problems, or access failures - **Partial Results**: VLANs with mixed validation outcomes or incomplete testing - **Pending Tests**: VLANs currently…

Tags: `Service Probe Vlan`

Parameters:

- `taskKey` query, optional (string) — The ID of the task to retrieve the service probe data
- `deviceId` query, optional (string) — The ID of the device to retrieve the service probe data

Responses:

- `200` — Successfully retrieved service probe VLAN data
- `400` — Bad Request - Invalid parameters provided: - Neither taskKey nor deviceId provided - Both taskKey and deviceId provided (only one allowed) - Invalid UUID format for parameters
- `500` — Internal Server Error - Failed to retrieve probe data: - Database query error - Service unavailable

