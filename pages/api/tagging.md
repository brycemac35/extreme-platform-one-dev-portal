---
source: https://developer.extremeplatformone.com/api-reference/tagging
spec: https://developer.extremeplatformone.com/api/spec/tagging
title: "Tag Management API"
---

# Tag Management API

**Tagging** · Services. Tag and Entity Management.

# Tag Management System API This specification defines the comprehensive REST API for managing tags, entities, associations, and policies in the Extreme Networks platform. ## Overview The Tag Management API provides a powerful and flexible system for organizing and categorizing resources through: - **Tags**: Lightweight labels that can be applied to entities for organization and filtering - **Entities**: The actual resources (devices, services, etc.) that can be tagged - **Associations**: Bidirectional relationships between tags and entities - **Policies**: Rule-based automation for tag management - **Attributes**: Key-value metadata attached to tags for enhanced functionality ## Key Features - Bulk operations for creating, updating, and deleting tags and entities - Flexible search and filtering capabilities with pagination support - Policy-driven automation for tag lifecycle management - Rich attribute system for tag metadata - Owner-based multi-tenancy support - Comprehensive telemetry and monitoring ## Authentication All endpoints require proper authentication headers. Ensure you include valid credentials in your requests. ## Rate Limiting API requests are subject to rate limiting. Monitor the response headers for rate limit information.

Version: `1.0.0`

## Servers

- `https://cloudapi.extremecloudiq.com/tagging/v1` — Extreme Platform ONE REST API - Tagging

Full OpenAPI document: [`specs/tagging.json`](../../specs/tagging.json)

## Endpoints

38 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/tags` | Create one or more tags with MCP-ready bulk operations |
| POST | `/tags/delete` | Delete multiple tags in a single request |
| POST | `/tags/fetch` | Advanced tag search and retrieval with MCP server optimization |
| PUT | `/tags/tagId/{tagId}` | Update tags by tagId |
| PUT | `/tags/tagName/{tagName}` | Update tag by tagName |
| GET | `/tags/tagId/{tagId}/entities` | Get list of entities for a given tag Id |
| GET | `/tags/tagName/{tagName}/entities` | Get list of entities for a given tag name |
| POST | `/tags/tagId/entities/associate` | Associate entities to tag with MCP-optimized bulk operations |
| POST | `/tags/tagId/entities/disassociate` | Disassociates multiple entities from a specified tag. |
| POST | `/tags/tagName/entities/associate` | Associate list of entity to a specific tag name |
| POST | `/tags/tagName/entities/disassociate` | Disassociates multiple entities from a specified tag name. |
| POST | `/entities/entityName/tags/associate` | Associate list of tags to a specific entity name |
| POST | `/entities/entityName/tags/disassociate` | Disassociates multiple tags from a specified entity name. |
| POST | `/tags/entities/associate` | Associate lists of tags with entities |
| POST | `/tags/entities/disassociate` | Deletes associations between lists of tags with entities |
| POST | `/owner/tags/delete` | Delete all tags belonging to the specified owner ID |
| POST | `/entities` | Create one or more entities with MCP-optimized bulk operations |
| GET | `/entities/entityType` | Retrieve a list of all unique entity types present in the system. |
| POST | `/entities/delete` | Deletes multiple entities based on their IDs or names. |
| POST | `/entities/fetch` | Advanced entity search and retrieval with MCP server optimization |
| PUT | `/entities/id/{entityId}` | Update entity by entityId |
| PUT | `/entities/updateByName` | Update entity by entityName |
| POST | `/entities/entityName/tags/fetch` | Get all associated tags for a given entity name |
| GET | `/entities/entityId/{entityId}/tags` | Get all associated tags for a given entity Id |
| GET | `/entities/csId/{csId}/tags` | Get all associated tags for a given csId |
| POST | `/policies/fetch` | Fetch policy based on search criteria. |
| POST | `/policies` | Create new policies with MCP automation and rule engine support |
| PUT | `/policies/{policyName}` | Update a policy by policy name |
| PUT | `/policies/tag/{tagName}` | Update a policy by tag name |
| POST | `/policies/delete` | Delete a policy by tag name or policy name |
| POST | `/telemetry/fetch` | Fetch telemetry data |
| POST | `/tags/tagName/{tagName}/attributes` | Add rich metadata attributes to tags with MCP-optimized data enrichment |
| POST | `/tags/tagId/{tagId}/attributes` | Specify a set of attributes which should be attached to a tag, which is specified by ID |
| PUT | `/tags/tagName/{tagName}/attributes/update` | Specify a set of a tag's attributes which should be created or updated |
| PUT | `/tags/tagId/{tagId}/attributes/update` | Specify a set of a tag's attributes which should be created or updated |
| POST | `/tags/tagName/{tagName}/attributes/delete` | Delete attributes from a tag. |
| POST | `/tags/tagId/{tagId}/attributes/delete` | Delete attributes from a tag. |
| POST | `/tags/attributes/fetch` | Fetch all attributes for a given tag. |

## POST `/tags`

Operation: `CreateTags`

Create one or more tags with MCP-ready bulk operations

**Create Tags for MCP Server Integration** Creates one or more tags in the system with comprehensive support for MCP (Model Context Protocol) servers and automation systems. This endpoint is optimized for bulk operations, automated workflows, and integration scenarios. **MCP Server Features:** - **Idempotent Operations**: Safe for automated retry scenarios and batch processing - **Atomic Transactions**: All tags succeed or fail together, ensuring data consistency - **Rich Error Context**: Detailed error messages for automated error handling and recovery - **Bulk Optimization**: Efficient processing of large tag sets (recommended: 100-500 per request) - **Integration Patterns**: Designed for CMDB sync, infrastructure discovery, and compliance automation **Core Features:** - Bulk creation of multiple tags in a single request - Automatic validation of tag names and properties - Support for hierarchical tag relationships via parent field - Automatic owner isolation and multi-tenancy - Comprehensive response metadata for tracking and auditing **Tag Properties:** - `name`: Unique tag identifier within the owner scope (required, max 64 chars) - `type`: Tag classification ["auto", "manual", "policy", "provisional"] (required) - `serviceOwner`: Service ownership ["edge", "network", "iam", "system", "asset"] (required) - `description`: Human-readable description of the tag's purpose (optional) - `access`: Access level control ["read", "write", "admin"] (optional, default: "read") -…

Tags: `Tags`

Request body:

- `application/json` — tagInfoList

Responses:

- `200` — **Tags Created Successfully** One or more tags were created successfully. The response includes the details of each created tag including: - Generated unique tag ID - Original tag name as provided -…
- `400`
- `401`
- `403`
- `422` — **All Tag Creation Failed** None of the requested tags could be created due to validation errors or conflicts. Common failure reasons: - Duplicate tag names within owner scope - Invalid characters in…
- `429`
- `500`

## POST `/tags/delete`

Operation: `DeleteTags`

Delete multiple tags in a single request

This endpoint is used to delete multiple tags based on either array of tagIds or array of tagNames. The request body includes either the array of tag Ids, or the array of tagNames, which need to be deleted.

Tags: `Tags`

Request body:

- `application/json` — tagIds, tagNames

Responses:

- `200` — Tags deleted successfully
- `400`
- `401`
- `403`
- `429`
- `500`

## POST `/tags/fetch`

Operation: `FetchTags`

Advanced tag search and retrieval with MCP server optimization

**Advanced Tag Search for MCP Servers** Performs sophisticated search and retrieval of tags with extensive filtering capabilities, specifically optimized for MCP (Model Context Protocol) servers and automated systems. **MCP Server Features:** - **High-Performance Queries**: Optimized indexing for rapid tag discovery in large datasets - **Complex Filtering**: Multi-dimensional search across names, types, serviceowner, access and policy - **Batch Operations**: Efficiently retrieve multiple tag sets in single requests - **Streaming Support**: Paginated results for handling massive tag collections **Search Capabilities:** - **Name-based search**: Exact, partial, wildcard, and regex pattern matching - **ID-based lookup**: Direct retrieval by unique identifiers with validation - **Policy search**: Discover tags linked to specific resources or policies - **Type and ownership filtering**: Filter by tag classification and service ownership - **Hierarchical search**: Navigate parent-child tag relationships and taxonomies **MCP Integration Patterns:** - **Resource Discovery**: Find all tags associated with discovered infrastructure - **Compliance Querying**: Search for regulatory and policy-related tags - **Inventory Management**: Retrieve tags for asset tracking and CMDB synchronization - **Automation Triggers**: Query tags to determine automated workflow actions **Advanced Features:** - **Deep fetch**: Include associated entities, and complete policies sets - **Smart pagination**:…

Tags: `Tags`

Request body:

- `application/json` — search, pagination, deepFetch

Responses:

- `200` — Successfully retrieved tags based on the query criteria
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## PUT `/tags/tagId/{tagId}`

Operation: `UpdateTagById`

Update tags by tagId

This endpoint is used to update an existing tag by specifying its tagId. The tagId is provided as a path parameter and is required. The request body must contain the updated tag information.

Tags: `Tags`

Parameters:

- `tagId` path, required (string)

Request body:

- `application/json` — updateTagRequest

Responses:

- `200` — Tag updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## PUT `/tags/tagName/{tagName}`

Operation: `UpdateTagByName`

Update tag by tagName

This endpoint is used to update an existing tag by specifying its tagName. The tagName is provided as a path parameter and is required. The request body must contain the updated tag information.

Tags: `Tags`

Parameters:

- `tagName` path, required (string)

Request body:

- `application/json` — updateTagRequest

Responses:

- `200` — Tag updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## GET `/tags/tagId/{tagId}/entities`

Operation: `GetEntities`

Get list of entities for a given tag Id

This endpoint is used to get a list of entities associated with a specific tag identified by tagId. The tagId is specified as a path parameter and is required.

Tags: `Tags`

Parameters:

- `tagId` path, required (string) — The unique identifier of the tag.
- `page` query, optional (integer) — The page number for pagination. Defaults to 1.
- `limit` query, optional (integer) — The maximum number of items to return per page. Defaults to 10.
- `lastItem` query, optional (string) — The lastItem pointing to the last position of current results.

Responses:

- `200` — Successfully retrieved entities
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## GET `/tags/tagName/{tagName}/entities`

Operation: `GetEntitiesTagName`

Get list of entities for a given tag name

This endpoint is used to get a list of entities associated with a specific tag identified by tagName. The tagName is specified as a path parameter and is required.

Tags: `Tags`

Parameters:

- `tagName` path, required (string)
- `page` query, optional (integer) — The page number for pagination. Defaults to 1.
- `limit` query, optional (integer) — The maximum number of items to return per page. Defaults to 10.
- `lastItem` query, optional (string) — The lastItem pointing to the last position of current results.

Responses:

- `200` — Successfully retrieved entities
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/tags/tagId/entities/associate`

Operation: `AssociateTagEntityById`

Associate entities to tag with MCP-optimized bulk operations

**Tag-Entity Association for MCP Servers** Associates multiple entities to a specific tag in bulk operations, designed for MCP (Model Context Protocol) servers and automated infrastructure management. This endpoint enables efficient relationship management between tags and entities for categorization, organization, and automated workflows. **MCP Server Features:** - **Bulk Association Operations**: Associate hundreds of entities to tags in single operations for efficiency - **Automated Relationship Management**: Build complex entity taxonomies and categorizations programmatically - **Infrastructure Mapping**: Link discovered resources to classification and organizational tags - **Policy Application**: Automatically associate entities with policy and compliance tags - **Workflow Integration**: Support automated tagging workflows during resource provisioning and discovery **Association Capabilities:** - **One-to-Many Relationships**: Associate a single tag with multiple entities efficiently - **Atomic Operations**: All associations succeed or fail together for data consistency - **Duplicate Detection**: Automatic handling of existing associations to prevent errors - **Validation Support**: Comprehensive validation of tag and entity existence before association - **Audit Trail**: Complete tracking of association operations for compliance and debugging **MCP Use Cases:** - **Infrastructure Classification**: Tag discovered devices by type, location, function, and ownership -…

Tags: `Associate`

Request body:

- `application/json` — tagsEntitiesAssociationByTagId

Responses:

- `200` — Tag associated with entities successfully.
- `400`
- `401`
- `403`
- `404`
- `422` — Tag Entity Association failure
- `429`
- `500`

## POST `/tags/tagId/entities/disassociate`

Operation: `DisassociateEntitiesByTagIds`

Disassociates multiple entities from a specified tag.

This endpoint allows to delete multiple entity association from a tag identified by tag Id. The request body can have an operation object containing an array of tag IDs and an array of entity Ids to be disassociated from the specified tags.

Tags: `Associate`

Request body:

- `application/json` — tagsEntitiesAssociationByTagId

Responses:

- `200` — Successfully disassociated entities from tag
- `400`
- `401`
- `403`
- `404`
- `422` — Tag Entity disassociation failure
- `429`
- `500`

## POST `/tags/tagName/entities/associate`

Operation: `AssociateEntitiesByTagName`

Associate list of entity to a specific tag name

This endpoint is used to associate multiple entities to a tag. The request body should contain a tagName, which is the identifier of the tag to which entities will be associated, and an entityList, which contains the list of entities to be associated.

Tags: `Associate`

Request body:

- `application/json` — tagsEntitiesAssociationByTagName

Responses:

- `200` — Tags associated with entities successfully.
- `400`
- `401`
- `403`
- `404`
- `422` — Tags entity association Failure
- `429`
- `500`

## POST `/tags/tagName/entities/disassociate`

Operation: `DisassociateEntitiesByTagName`

Disassociates multiple entities from a specified tag name.

This endpoint allows to remove multiple entities from a tag Identified by tagName. The request body can have an operation object containing an array of entity names to be disassociated from the specified tag.

Tags: `Associate`

Request body:

- `application/json` — tagsEntitiesAssociationByTagName

Responses:

- `200` — Successfully disassociate entities to tag
- `400`
- `401`
- `403`
- `404`
- `422` — Tags entity disassociation failure
- `429`
- `500`

## POST `/entities/entityName/tags/associate`

Operation: `AssociateTagsByEntityName`

Associate list of tags to a specific entity name

This endpoint is used to associate multiple tags with an entity. The request body should contain an entity name, which is the identifier of the entity to which tags will be associated, and a tagList, which contains the list of tags to be associated.

Tags: `Associate`

Request body:

- `application/json` — tagsEntityAssociationByEntityName

Responses:

- `200` — Tags associated with entity successfully
- `400`
- `401`
- `403`
- `404`
- `422` — Tags entity association failure
- `429`
- `500`

## POST `/entities/entityName/tags/disassociate`

Operation: `DisassociateTagsByEntityName`

Disassociates multiple tags from a specified entity name.

This endpoint allows to remove multiple tags from a enity Identified by entityName. The request body can have an object containing an array of tag names to be disassociated from the specified entity.

Tags: `Associate`

Request body:

- `application/json` — EntitiesTagDisAssociationByEntityName

Responses:

- `200` — Successfully disassociate entities to tag
- `400`
- `401`
- `403`
- `404`
- `422` — Tags entity disassociation failure
- `429`
- `500`

## POST `/tags/entities/associate`

Operation: `AssociateTagsAndEntities`

Associate lists of tags with entities

Associates lists of existing tags with lists of existing entities. Lists are specified in mapping pairs: one list identifying tags; the other, entities. There are multiple ways of specifying a tag or entity: by id (UUID), name, or csid (UUID, entities only). Each list is constrained to use only one kind of identifying property; but, as multiple mappings can be specified in the same request, different discriminators can be used for different mapping pairs.

Tags: `Associate`

Request body:

- `application/json` — associateTagsEntitiesMappings

Responses:

- `200` — All or some tags and entities associated successfully.
- `400`
- `401`
- `403`
- `404`
- `422` — All associations failed.
- `429`
- `500`

## POST `/tags/entities/disassociate`

Operation: `DisassociateTagsAndEntities`

Deletes associations between lists of tags with entities

Deletes associations between lists of tags and lists of entities. Lists are specified in mapping pairs: one list identifying tags; the other, entities. There are multiple ways of specifying a tag or entity: by id (UUID), name, or csid (UUID, entities only). Each list is constrained to use only one kind of identifying property; but, as multiple mappings can be specified in the same request, different discriminators can be used for different mapping pairs.

Tags: `Associate`

Request body:

- `application/json` — associateTagsEntitiesMappings

Responses:

- `200` — All tag-entities associations deleted.
- `400`
- `401`
- `403`
- `404`
- `422` — Not all tags-entities associations deleted.
- `429`
- `500`

## POST `/owner/tags/delete`

Operation: `DeleteAllTagsByOwnerId`

Delete all tags belonging to the specified owner ID

This endpoint deletes all tags associated with a specific owner ID, including any associations of those tags. Additionally, the request provides the option to delete the entities linked to these tags.

Tags: `Owner`

Request body:

- `application/json` — deleteAllTagsRequest

Responses:

- `200` — All tags deleted successfully
- `401`
- `403`
- `429`
- `500`

## POST `/entities`

Operation: `CreateEntities`

Create one or more entities with MCP-optimized bulk operations

**Create Entities for MCP Server Integration** Creates one or more entities in the system with comprehensive support for MCP (Model Context Protocol) servers and automated resource management. This endpoint is designed for efficient bulk entity creation during infrastructure discovery, asset management, and automated provisioning workflows. **MCP Server Features:** - **Automated Resource Registration**: Seamlessly register discovered infrastructure, devices, and services - **Bulk Entity Creation**: Efficiently process large sets of entities in single operations (up to 1000 per request) - **Idempotent Operations**: Safe retry mechanisms for automated systems and recovery scenarios - **Rich Metadata Support**: Store comprehensive entity attributes, properties, and relationship data - **Integration Patterns**: Optimized for CMDB sync, cloud resource management, and asset tracking **Entity Management Capabilities:** - **Resource Discovery**: Register newly discovered network devices, servers, applications, and services - **Asset Lifecycle**: Track entities through creation, active use, maintenance, and decommissioning - **Multi-Source Integration**: Merge entity data from multiple discovery tools and management systems - **Relationship Mapping**: Establish parent-child and dependency relationships between entities - **Metadata Enrichment**: Attach custom properties, compliance data, and operational metrics **MCP Use Cases:** - **Infrastructure Auto-Discovery**: Register network…

Tags: `Entities`

Request body:

- `application/json` — entityRequestList

Responses:

- `200` — Entities created successfully
- `400`
- `401`
- `403`
- `422` — Entities creation failure
- `429`
- `500`

## GET `/entities/entityType`

Operation: `GetEntityTypes`

Retrieve a list of all unique entity types present in the system.

This endpoint fetches a list of distinct entity types that are currently stored in the system. It helps users understand the variety of entities managed within the platform.

Tags: `Entities`

Responses:

- `200` — Successfully retrieved entity types
- `400`
- `401`
- `403`
- `429`
- `500`

## POST `/entities/delete`

Operation: `DeleteEntitiesByIdsOrNames`

Deletes multiple entities based on their IDs or names.

This endpoint is used to delete one or more entities. The request body must include either an array of unique identifiers for the entities to be deleted or an array of names for the entities to be deleted

Tags: `Entities`

Request body:

- `application/json` — entityIds, entityNames

Responses:

- `200` — Entities deleted successfully
- `400`
- `401`
- `403`
- `429`
- `500`

## POST `/entities/fetch`

Operation: `FetchEntities`

Advanced entity search and retrieval with MCP server optimization

**Advanced Entity Search for MCP Servers** Performs comprehensive search and retrieval of entities with sophisticated filtering capabilities, specifically optimized for MCP (Model Context Protocol) servers and automated asset management systems. **MCP Server Features:** - **High-Performance Discovery**: Rapidly search through large entity inventories with optimized indexing - **Multi-Dimensional Filtering**: Search by names, IDs, types, attributes, and tag associations - **Relationship Queries**: Find entities by their tag associations and hierarchical relationships - **Bulk Entity Retrieval**: Efficiently process large entity datasets for inventory and reporting - **Real-time Integration**: Support for live asset management and configuration tracking **Entity Search Capabilities:** - **Name-based search**: Exact, partial, wildcard, and pattern matching for entity identification - **ID-based lookup**: Direct retrieval using unique identifiers with validation - **Type and classification filtering**: Search by entity types, categories, and service classifications - **Tag association queries**: Find entities based on their tag relationships and metadata - **Attribute-based filtering**: Query entities by custom properties and configuration data - **Status and lifecycle filtering**: Search by operational state, lifecycle phase, and health status **MCP Integration Patterns:** - **Asset Discovery Workflows**: Query entities during automated infrastructure scanning - **CMDB…

Tags: `Entities`

Request body:

- `application/json` — search, pagination, deepFetch

Responses:

- `200` — Successfully retrieved entities based on the query criteria
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## PUT `/entities/id/{entityId}`

Operation: `UpdateEntityById`

Update entity by entityId

This endpoint allows to update an existing entity by specifying its entityId. The entityId is provided as a path parameter and is required. The request body must contain the updated entity information.

Tags: `Entities`

Parameters:

- `entityId` path, required (string)

Request body:

- `application/json` — entity

Responses:

- `200` — Entity updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## PUT `/entities/updateByName`

Operation: `UpdateEntityByName`

Update entity by entityName

This endpoint allows to update an existing entity by specifying its name. The entityName is provided as a path parameter and is required. The request body must contain the updated entity information.

Tags: `Entities`

Request body:

- `application/json` — UpdateEntityByNameRequest

Responses:

- `200` — Entity updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/entities/entityName/tags/fetch`

Operation: `GetTagsByEntityName`

Get all associated tags for a given entity name

This endpoint is used to get a list of tags associated with a specific entity identified by entity name. The entity name is specified as a path parameter and is required. The pagination can also be applied to the results by including page_number and page_size as query parameters.

Tags: `Entities`

Parameters:

- `page` query, optional (integer) — The page number for pagination. Defaults to 1.
- `limit` query, optional (integer) — The maximum number of items to return per page. Defaults to 10.
- `lastItem` query, optional (string) — The lastItem pointing to the last position of current results.

Request body:

- `application/json` — getAssociatedTagsRequest

Responses:

- `200` — Retrieved all tags for given entity successfully
- `401`
- `403`
- `404`
- `429`
- `500`

## GET `/entities/entityId/{entityId}/tags`

Operation: `GetTagsByEntityId`

Get all associated tags for a given entity Id

This endpoint is used to get a list of tags associated with a specific entity identified by entity Id. The entity Id is specified as a path parameter is required. The pagination can also be applied to the results by including page_number and page_size as query parameters.

Tags: `Entities`

Parameters:

- `entityId` path, required (string)
- `page` query, optional (integer) — The page number for pagination. Defaults to 1.
- `limit` query, optional (integer) — The maximum number of items to return per page. Defaults to 10.
- `lastItem` query, optional (string) — The lastItem pointing to the last position of current results.

Responses:

- `200` — Retrieved all tags for given entity successfully
- `401`
- `403`
- `404`
- `429`
- `500`

## GET `/entities/csId/{csId}/tags`

Operation: `GetTagsByCSId`

Get all associated tags for a given csId

This endpoint is used to get a list of tags associated with a specific entity identified by CSId. The CSId is specified as a path parameter is required. The pagination can also be applied to the results by including 'page' number and page 'limit' as query parameters.

Tags: `Entities`

Parameters:

- `csId` path, required (string)
- `page` query, optional (integer) — The page number for pagination. Defaults to 1.
- `limit` query, optional (integer) — The maximum number of items to return per page. Defaults to 10.
- `lastItem` query, optional (string) — The lastItem pointing to the last position of current results.

Responses:

- `200` — Retrieved all tags for given entity successfully
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/policies/fetch`

Operation: `GetPolicies`

Fetch policy based on search criteria.

This endpoint is used to search for and retrieve policies based on various filters, with support for pagination. The request body can contain an empty search object that retrieves all policies, or with optional parameters such as policy name and tag name.

Tags: `Policies`

Request body:

- `application/json` — search, pagination, deepFetch

Responses:

- `200` — Policy retrieved successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/policies`

Operation: `CreatePolicies`

Create new policies with MCP automation and rule engine support

**Create Policies for MCP Server Automation** Creates one or more tagging policies with comprehensive support for MCP (Model Context Protocol) servers and automated rule-based tagging systems. This endpoint enables sophisticated automation workflows, compliance enforcement, and intelligent tag management. **MCP Server Features:** - **Rule-Based Automation**: Define complex tagging rules that automatically execute based on entity properties and conditions - **Compliance Enforcement**: Create policies that ensure regulatory and organizational compliance requirements - **Event-Driven Tagging**: Policies that trigger automatic tagging based on infrastructure changes and discovery events - **Bulk Policy Management**: Efficiently create multiple related policies for comprehensive automation coverage - **Integration Workflows**: Seamlessly integrate with CI/CD pipelines, monitoring systems, and management tools **Policy Automation Capabilities:** - **Conditional Logic**: Define complex conditions using entity attributes, types, and discovery metadata - **Multi-Action Policies**: Single policies that can create, update, or remove multiple tags based on conditions - **Hierarchical Rules**: Policies that respect tag hierarchies and parent-child relationships - **Time-Based Policies**: Schedule-based and lifecycle-driven automatic tagging operations - **Conflict Resolution**: Intelligent handling of overlapping policies and rule conflicts **MCP Use Cases:** - **Infrastructure…

Tags: `Policies`

Request body:

- `application/json` — policyRequestList

Responses:

- `200` — Policies created successfully
- `400`
- `401`
- `403`
- `422` — All policies failed to create
- `429`
- `500`

## PUT `/policies/{policyName}`

Operation: `UpdatePolicyByName`

Update a policy by policy name

This endpoint is used to update an existing policy by its policy name.

Tags: `Policies`

Parameters:

- `policyName` path, required (string)

Request body:

- `application/json` — policy

Responses:

- `200` — Policy updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## PUT `/policies/tag/{tagName}`

Operation: `UpdatePolicyByTagName`

Update a policy by tag name

This endpoint is used to update an existing policy by the specified tag name.

Tags: `Policies`

Parameters:

- `tagName` path, required (string)

Request body:

- `application/json` — policy

Responses:

- `200` — Policy updated successfully
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/policies/delete`

Operation: `DeletePolicyByTagNameOrPolicyName`

Delete a policy by tag name or policy name

This endpoint is used to delete a policy for specified tag name or policy name.

Tags: `Policies`

Request body:

- `application/json` — policyName, tagName

Responses:

- `200` — Policy deleted successfully
- `401`
- `403`
- `429`
- `500`

## POST `/telemetry/fetch`

Operation: `FetchTelemetry`

Fetch telemetry data

Fetch telemetry data for the tagging service. Optionally, provide an owner ID to fetch data specific to that owner.

Tags: `Telemetry`

Responses:

- `200` — Successfully retrieved telemetry data
- `400`
- `401`
- `403`
- `429`
- `500`

## POST `/tags/tagName/{tagName}/attributes`

Operation: `AddAttributesByTagName`

Add rich metadata attributes to tags with MCP-optimized data enrichment

**Add Tag Attributes for MCP Server Metadata Management** Attaches rich metadata attributes to tags by name, enabling comprehensive data enrichment for MCP (Model Context Protocol) servers and automated metadata management systems. This endpoint supports sophisticated attribute management for enhanced tag functionality and integration workflows. **MCP Server Features:** - **Rich Metadata Enrichment**: Attach comprehensive operational, technical, and business metadata to tags - **Bulk Attribute Operations**: Efficiently add multiple attributes to tags in single operations - **Schema Validation**: Support for structured attribute schemas and data type validation - **Integration Metadata**: Store integration-specific data for CMDB sync, monitoring, and automation - **Performance Attributes**: Attach performance metrics, thresholds, and operational characteristics **Attribute Management Capabilities:** - **Key-Value Storage**: Flexible attribute system supporting various data types and structures - **Metadata Enrichment**: Add technical specifications, operational parameters, and business context - **Custom Properties**: Store application-specific metadata and configuration parameters - **Relationship Data**: Attach dependency information, hierarchy details, and association metadata - **Temporal Attributes**: Support for time-based metadata like creation dates, expiration, and schedules **MCP Use Cases:** - **Infrastructure Metadata**: Store device specifications, firmware…

Tags: `Attributes`

Parameters:

- `tagName` path, required (string)

Request body:

- `application/json` — attributeRequestList

Responses:

- `200` — Attributes already present or successfully added
- `400`
- `401`
- `403`
- `404`
- `422` — The set of attributes could not be applied to the tag
- `429`
- `500`

## POST `/tags/tagId/{tagId}/attributes`

Operation: `AddAttributesByTagID`

Specify a set of attributes which should be attached to a tag, which is specified by ID

This endpoint is used to ensure the given attributes exist on the tag. The request body should contain an attributeList, which is the list of attributes which should exist on the tag, and added if required. If an attribute already exists on the tag with a different value, the operation fails.

Tags: `Attributes`

Parameters:

- `tagId` path, required (string)

Request body:

- `application/json` — attributeRequestList

Responses:

- `200` — Attributes already present or successfully added
- `400`
- `401`
- `403`
- `404`
- `422` — The set of attributes could not be applied to the tag
- `429`
- `500`

## PUT `/tags/tagName/{tagName}/attributes/update`

Operation: `UpdateAttributesByTagName`

Specify a set of a tag's attributes which should be created or updated

This endpoint is used to update the given attributes existing on the named tag. The request body should contain an attributeList, which is the updated list of attributes which should exist on the tag, and added if required.

Tags: `Attributes`

Parameters:

- `tagName` path, required (string)

Request body:

- `application/json` — attributeRequestList

Responses:

- `200` — Attributes successfully added or updated
- `400`
- `401`
- `403`
- `404`
- `422` — The set of attributes could not be applied to the tag
- `429`
- `500`

## PUT `/tags/tagId/{tagId}/attributes/update`

Operation: `UpdateAttributesByTagID`

Specify a set of a tag's attributes which should be created or updated

This endpoint is used to update the given attributes existing on the tag Id. The request body should contain an attributeList, which is the updated list of attributes which should exist on the tag, and added if required.

Tags: `Attributes`

Parameters:

- `tagId` path, required (string)

Request body:

- `application/json` — attributeRequestList

Responses:

- `200` — Attributes successfully added or updated
- `400`
- `401`
- `403`
- `404`
- `422` — The set of attributes could not be applied to the tag
- `429`
- `500`

## POST `/tags/tagName/{tagName}/attributes/delete`

Operation: `DeleteAttributesByTagName`

Delete attributes from a tag.

This endpoint ensures that a named tag does not have the given attributes, deleting attributes as necessary.

Tags: `Attributes`

Parameters:

- `tagName` path, required (string)

Request body:

- `application/json` — deleteAttributeRequestList

Responses:

- `200` — Attributes deleted as necessary
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/tags/tagId/{tagId}/attributes/delete`

Operation: `DeleteAttributesByTagID`

Delete attributes from a tag.

This endpoint ensures that a tag by Id does not have the given attributes, deleting attributes as necessary.

Tags: `Attributes`

Parameters:

- `tagId` path, required (string)

Request body:

- `application/json` — deleteAttributeRequestList

Responses:

- `200` — Attributes deleted as necessary
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

## POST `/tags/attributes/fetch`

Operation: `FetchTagAttributes`

Fetch all attributes for a given tag.

This endpoint retrieves all attributes attached to a given tag, specified by name or id. Optionally, a list of specific attribute keys can be provided to filter the attributes being fetched.

Tags: `Attributes`

Request body:

- `application/json` — tagSpec, pagination

Responses:

- `200` — Successfully retrieved attributes
- `400`
- `401`
- `403`
- `404`
- `429`
- `500`

