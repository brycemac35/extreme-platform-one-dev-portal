---
source: https://developer.extremeplatformone.com/api-reference/configuration
spec: https://developer.extremeplatformone.com/api/spec/configuration
title: "Configuration Management and Device Targeting API"
---

# Configuration Management and Device Targeting API

**Configuration** · Services. Network Device Configuration Management.

API for managing network configuration templates, profiles, and device targeting ## Config Service API Behavior Guidelines This section defines the standard behavior for Create, Delete, Retrieve and Update operations exposed by the Config Service REST APIs. ### Idempotency Not Supported - Idempotency is **not supported** for any operation. - Repeating the same request may result in different outcomes depending on the current system state. - For example, creating a resource with the same name multiple times will result in an error after the first successful creation. ### HTTP Status Codes and Error Handling #### Success Responses: - **200 OK**: Returned for successful `RETRIEVE`, `DELETE` and API including **multiple operations**. - **201 Created**: Returned for successful `CREATE` operations. #### Error Responses: - Non-2xx status codes are used when all instances (i.e., each item in the request body) fail in a batch operation, or when a single instance operation fails. - Common HTTP status codes for failure responses: - **400 Bad Request**: Invalid input, malformed request and request validation errors. - **401 Unauthorized**: Authentication failure. - **403 Forbidden**: Forbidden - the user does not have permission to perform the operation. - **404 Not Found**: Resource not found. - **409 Conflict**: Returned when attempted to create a resource that already exists. - **500 Internal Server Error**: Unexpected internal failure during processing. - When all instances fail in a batch operation, the error response uses a non-2xx status code based on the following precedence: **(500 > 401 > 409 > 404 > 403 > 400)** This means the highest precedence error code among all failed instances determines the HTTP status code for the response. ### For Create, Delete, Clone, Deploy and Update operations: #### Response Schema for single operations: (SingleAPIResponse) - All responses, whether successful or failed, follow a consistent schema. - The response schema includes: (all…

Version: `1.0.0`

## Servers

- `https://cloudapi.extremecloudiq.com/configuration/v1` — Extreme Platform ONE REST API - Configuration

Full OpenAPI document: [`specs/configuration.json`](../../specs/configuration.json)

## Endpoints

87 operations.

| Method | Path | Summary |
| --- | --- | --- |
| POST | `/blueprints/retrieve` | Retrieve a list of blueprints, optionally filtered by name(s), category or level of detail |
| POST | `/blueprint/{name}/feature/retrieve` | Retrieve a specific feature from a blueprint |
| POST | `/configuration-profiles` | Retrieve configuration profile summaries with filtering, pagination, and fuzzy search |
| POST | `/configuration-profiles/deploy` | Deploy multiple configuration profiles |
| POST | `/configuration-profile/{name}/sites/deploy` | Deploy sites under a configuration profile |
| POST | `/configuration-profile/{name}/devices/deploy` | Deploy devices under a configuration profile |
| POST | `/configuration-profile/{name}/deploy/status` | Retrieve deployment status of a configuration profile |
| POST | `/configuration-profile/{name}/site/{siteName}/deploy/status` | Retrieve deployment status of a site under a configuration profile |
| POST | `/configuration-profile/{name}/device/{hostName}/deploy/status` | Retrieve deployment status of a device under a configuration profile |
| GET | `/configuration-profile/{name}/device/{hostName}/conflicts` | Retrieve device conflicts for a configuration profile |
| POST | `/configuration-profile/{name}/sites/deploy/edit-schedule` | Edit sites deployment under a configuration profile |
| POST | `/configuration-profile/{name}/devices/deploy/edit-schedule` | Edit devices deployment schedule under a configuration profile |
| POST | `/configuration-profile/{name}/sites/deploy/clear-schedule` | Clear sites deployment schedule under a configuration profile |
| POST | `/configuration-profile/{name}/devices/deploy/clear-schedule` | Clear devices deployment schedule under a configuration profile |
| GET | `/deployments` | List all deployments |
| POST | `/configuration-profiles/deploy/cancel` | Cancel configuration profile deployments |
| GET | `/configuration-profile/{name}` | Retrieve a configuration profile by name |
| POST | `/configuration-profile/{name}` | Create a configuration profile from blueprints |
| DELETE | `/configuration-profile/{name}` | Delete a configuration profile |
| POST | `/configuration-profile/{name}/add-remove-features` | Add/remove features from a configuration profile |
| POST | `/configuration-profile/{name}/clone` | Clone a configuration profile |
| POST | `/configuration-profile/{name}/feature/object/retrieve` | Retrieve objects within a feature |
| POST | `/configuration-profile/{name}/feature/object/modify` | Add or update objects within a feature |
| POST | `/configuration-profile/{name}/feature/object/delete` | Delete objects within a feature |
| POST | `/configuration-profile/{name}/feature/object/clone` | Clone a config object within a feature |
| POST | `/configuration-profile/{name}/feature/object/group/create` | Create a group from existing objects within a feature |
| POST | `/configuration-profile/{name}/feature/object/group/delete` | Delete a group within a feature |
| POST | `/configuration-profile/{name}/feature/object/group/modify` | Update objects in a configuration object group |
| POST | `/configuration-profile/{name}/feature/object/group/clone` | Clone a group within a feature |
| POST | `/configuration-profile/{name}/feature/object/retrieve-v2` | Retrieve objects within a feature |
| POST | `/configuration-profile/{name}/feature/object/retrieve-summary` | Retrieve objects within a feature (summary view) |
| GET | `/configuration-profile/{name}/feature/object/retrieve-by-id` | Retrieve object within a feature by Id |
| GET | `/blueprints/categories` | Retrieve a list of blueprint categories |
| GET | `/global-profile` | Retrieve the global profile feature tree |
| POST | `/global-profile/feature/object/retrieve` | Retrieve objects within a global feature |
| POST | `/global-profile/feature/object/modify` | Add or update objects within a global feature |
| POST | `/global-profile/feature/object/delete` | Delete objects within a global feature |
| POST | `/global-profile/feature/object/retrieve-v2` | Retrieve global objects within a feature |
| POST | `/global-profile/feature/usage` | Get configuration profiles using a specific global feature |
| GET | `/service-profile/{name}` | Retrieve a service profile by name |
| POST | `/service-profile/{name}` | Create a service profile from a blueprint |
| PATCH | `/service-profile/{name}` | Update a service profile (description only) |
| DELETE | `/service-profile/{name}` | Delete a service profile |
| POST | `/service-profiles` | Retrieve service profiles by name or feature criteria |
| POST | `/service-profile/{name}/feature/object/retrieve` | Retrieve objects within a feature |
| POST | `/service-profile/{name}/feature/object/retrieve-v2` | Retrieve service profile objects within a feature |
| POST | `/service-profile/{name}/feature/object/modify` | Add or update objects within a feature |
| POST | `/service-profile/{name}/feature/object/delete` | Delete objects within a feature of a service profile |
| GET | `/service-profile/{name}/usage` | Get configuration profiles using a specific service profile name |
| POST | `/authorized/sites-sitegroups/retrieve` | Get all sites and site groups available customer is authorized to use |
| GET | `/configuration-profile/{name}/models/retrieve` | Get all models either from defined scope or from all supported by org |
| POST | `/configuration-profile/{name}/scoped/devices/retrieve` | Get devices available for defined scope (supports optional pagination in request body) |
| GET | `/configuration-profile/{name}/scope` | Get current target query scope |
| POST | `/configuration-profile/{name}/scope` | Set target query scope by selecting site groups |
| GET | `/configuration-profile/{name}/target-query/profile` | Get target query associated with configuration profile |
| POST | `/configuration-profile/{name}/target-query/profile` | Associate target query with configuration profile |
| DELETE | `/configuration-profile/{name}/target-query/profile` | Remove target query from configuration profile |
| GET | `/configuration-profile/{name}/target-query/feature/{featureId}` | Get target query associated with configuration feature |
| POST | `/configuration-profile/{name}/target-query/feature/{featureId}` | Associate target query with configuration feature |
| DELETE | `/configuration-profile/{name}/target-query/feature/{featureId}` | Remove target query from configuration feature |
| GET | `/configuration-profile/{name}/target-query/object/{objectId}` | Get target query associated with configuration object |
| POST | `/configuration-profile/{name}/target-query/object/{objectId}` | Associate target query with configuration object |
| DELETE | `/configuration-profile/{name}/target-query/object/{objectId}` | Remove target query from configuration object |
| GET | `/configuration-profile/{name}/target-query/object-group/{objectGroupId}` | Get target query associated with configuration object group |
| POST | `/configuration-profile/{name}/target-query/object-group/{objectGroupId}` | Associate target query with configuration object group |
| DELETE | `/configuration-profile/{name}/target-query/object-group/{objectGroupId}` | Remove target query from configuration object group |
| GET | `/inventory/models` | Retrieve all available device models |
| GET | `/inventory/port-types` | Retrieve all available port types |
| POST | `/inventory/models/modelVariants/retrieve` | Retrieve variants for one or more device models |
| POST | `/inventory/models/modelVariants/porttypes/skus-retrieve` | Retrieve Extreme Networks device SKUs based on models, variants, port types, and OS |
| POST | `/inventory/models/hosts/porttypes/skus-retrieve` | Retrieve Extreme Networks device SKUs by hostname with optional filters |
| POST | `/configuration-profile/{name}/models/scoped/devices/retrieve` | Retrieve devices for one or more models within a configuration profile's scope |
| GET | `/configuration-profile/{name}/port-profile` | Get all port profiles for a configuration profile |
| POST | `/configuration-profile/{name}/port-profile/{portProfileName}/port-mappings/retrieve` | Retrieve all port mappings for a specific port profile |
| POST | `/configuration-profile/{name}/port-mappings` | Create a new port mapping with device resolution |
| DELETE | `/configuration-profile/{name}/port-mappings` | Delete a port mapping from a configuration profile |
| POST | `/configuration-profile/{name}/port-mappings/modify` | Modify an existing port mapping with device resolution |
| POST | `/configuration-profile/{name}/port-mappings/update-priorities` | Update priorities for one or more port mappings |
| POST | `/configuration-profile/{name}/port-mappings/retrieve` | Retrieve port mappings for a profile with advanced filtering and pagination |
| GET | `/configuration-profile/{name}/lag-configurations` | Retrieve all LAG configurations for a configuration profile |
| POST | `/configuration-profile/{name}/lag-configurations` | Create a new LAG configuration with device resolution |
| DELETE | `/configuration-profile/{name}/lag-configurations` | Delete a LAG configuration from a configuration profile |
| GET | `/configuration-profile/{name}/lag-configurations/{identifier}` | Retrieve a specific LAG configuration by name, ID, or MLT ID |
| POST | `/configuration-profile/{name}/feature/object/override/create-update` | Create or update overrides for config objects |
| GET | `/configuration-profile/{name}/feature/object/override/retrieve` | Retrieve complete object with override context |
| POST | `/configuration-profile/{name}/feature/object/override/delete` | Delete a specific override for a config object |
| GET | `/configuration-profile/{name}/feature/object/overrides` | Get list of all overrides on a config object |

## POST `/blueprints/retrieve`

Operation: `retrieveBlueprints`

Retrieve a list of blueprints, optionally filtered by name(s), category or level of detail

Returns all available blueprints, with optional filtering by name, category or level of detail.

Tags: `Blueprints`

Request body:

- `application/json` — names, categories, detailLevel

Responses:

- `200` — A list of blueprints matching the retrieval criteria
- `400` — Bad request
- `401` — Unauthorized - authentication required
- `404` — Blueprint not found
- `500` — Internal server error

## POST `/blueprint/{name}/feature/retrieve`

Operation: `retrieveBlueprintFeature`

Retrieve a specific feature from a blueprint

Returns detailed information about a feature (including nested features,object and property schemas) within a blueprint

Tags: `Blueprints`

Parameters:

- `name` path, required (string) — Name of the blueprint

Request body:

- `application/json` — featurePath

Responses:

- `200` — Feature details (including any nested features)
- `400` — Bad request
- `401` — Unauthorized
- `404` — Blueprint or feature not found
- `500` — Internal server error

## POST `/configuration-profiles`

Operation: `listConfigurationProfiles`

Retrieve configuration profile summaries with filtering, pagination, and fuzzy search

Retrieves a summary list of configuration profiles based on filter, pagination, and fuzzy search criteria.

Tags: `ConfigurationProfiles`

Request body:

- `application/json` — ConfigProfilesSummaryRequest

Responses:

- `200` — A list of configuration profile summaries with pagination.
- `400` — Bad request - invalid filter or pagination parameters
- `401` — Unauthorized - authentication required
- `500` — Internal server error

## POST `/configuration-profiles/deploy`

Operation: `deployMultipleConfigurationProfiles`

Deploy multiple configuration profiles

Deploy one or more configuration profiles. Only one deployment mode (immediate or scheduled) per request. Returns 202 Accepted and triggers deployment asynchronously.

Tags: `Deployment`

Request body:

- `application/json`

Responses:

- `202` — Deployment accepted and triggers deployment asynchronously.
- `400` — Bad Request - Invalid request payload or one or more specified profiles could not be found or processed.
- `401` — Unauthorized - authentication required
- `404` — One or more configuration profiles not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/sites/deploy`

Operation: `deploySitesConfigurationProfile`

Deploy sites under a configuration profile

Deploy one or more sites under a configuration profile. Only one deployment mode per request. Returns 202 Accepted and triggers deployment asynchronously.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json`

Responses:

- `202` — Deployment accepted and triggers deployment asynchronously.
- `400` — Bad Request - Invalid request payload or one or more specified sites could not be found or processed.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or sites not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/devices/deploy`

Operation: `deployDevicesConfigurationProfile`

Deploy devices under a configuration profile

Deploy one or more devices under a configuration profile (devices may be from different sites). Only one deployment mode per request. Returns 202 Accepted and triggers deployment asynchronously.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json`

Responses:

- `202` — Deployment accepted and triggers deployment asynchronously.
- `400` — Bad Request - Invalid request payload or one or more specified devices could not be found or processed.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or devices not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/deploy/status`

Operation: `getConfigurationProfileDeploymentStatus`

Retrieve deployment status of a configuration profile

Returns deployment status of a configuration profile. Response provides site level status for the requested profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — CommonQueryRequest

Responses:

- `200` — Configuration profile deployment status retrieved successfully.
- `400` — Bad Request - Invalid request payload or one or more specified profiles could not be found or processed.
- `401` — Unauthorized - authentication required
- `404` — One or more configuration profiles not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/site/{siteName}/deploy/status`

Operation: `getSiteDeploymentStatus`

Retrieve deployment status of a site under a configuration profile

Returns deployment status of a site under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `siteName` path, required (string) — Name of the site

Request body:

- `application/json` — CommonQueryRequest

Responses:

- `200` — Site deployment status retrieved successfully.
- `400` — Bad Request - Invalid request payload or configuration profile/site not found.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or site not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/device/{hostName}/deploy/status`

Operation: `getDeviceDeploymentStatus`

Retrieve deployment status of a device under a configuration profile

Returns deployment status of a device under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `hostName` path, required (string) — Hostname of the device

Request body:

- `application/json` — CommonQueryRequest

Responses:

- `200` — Device deployment status retrieved successfully.
- `400` — Bad Request - Invalid request payload or configuration profile/device not found.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or device not found
- `500` — Internal server error

## GET `/configuration-profile/{name}/device/{hostName}/conflicts`

Operation: `getDeviceConflicts`

Retrieve device conflicts for a configuration profile

Returns conflicts found when applying a configuration profile to a specific device.

Tags: `DeviceConflict`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `hostName` path, required (string) — Hostname of the device
- `detailLevel` query, optional (string) — Level of detail to return - 'summary' for high-level conflict information only, or 'detailed' for complete conflict details including objects and properties

Responses:

- `200` — Device conflicts retrieved successfully.
- `400` — Bad Request - Invalid request payload or configuration profile/device not found.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or device not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/sites/deploy/edit-schedule`

Operation: `editSitesDeploymentSchedule`

Edit sites deployment under a configuration profile

Edits scheduled deployment time for a set of sites under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — EditSitesScheduleRequest

Responses:

- `200` — Sites deployment schedule edited successfully.
- `400` — Bad Request - Invalid request body.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or sites not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/devices/deploy/edit-schedule`

Operation: `editDevicesDeploymentSchedule`

Edit devices deployment schedule under a configuration profile

Edits scheduled deployment time for a set of devices under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — EditDevicesScheduleRequest

Responses:

- `200` — Device deployment schedule edited successfully.
- `400` — Bad Request - Invalid request body.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or devices not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/sites/deploy/clear-schedule`

Operation: `clearSitesDeploymentSchedule`

Clear sites deployment schedule under a configuration profile

Clear the deployment schedule for a set of sites under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — sites

Responses:

- `200` — Sites deployment schedule cleared successfully.
- `400` — Bad Request - Invalid request body.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or sites not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/devices/deploy/clear-schedule`

Operation: `clearDevicesDeploymentSchedule`

Clear devices deployment schedule under a configuration profile

Clears the deployment schedule for a set of devices under a configuration profile.

Tags: `Deployment`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — devices

Responses:

- `200` — Devices deployment clear completed successfully.
- `400` — Bad Request - Invalid request body.
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or devices not found
- `500` — Internal server error

## GET `/deployments`

Operation: `listAllDeployments`

List all deployments

Retrieves a list of all deployment workflow executions, including their workflow IDs, associated profile names, status, and key timestamps. This endpoint is useful for monitoring deployment history and tracking the state of all configuration deployments.

Tags: `Deployment`

Responses:

- `200` — List of all deployment workflow executions retrieved successfully.
- `400` — Bad Request - Invalid request parameters.
- `401` — Unauthorized - authentication required
- `500` — Internal server error

## POST `/configuration-profiles/deploy/cancel`

Operation: `cancelConfigurationProfileDeployments`

Cancel configuration profile deployments

Cancel ongoing deployments of an array of configuration profiles.

Tags: `Deployment`

Request body:

- `application/json` — profiles

Responses:

- `200` — Deployment cancellation completed with success and failure details.
- `400` — Bad Request - Invalid request payload or configuration profiles not found.
- `401` — Unauthorized - authentication required
- `404` — Configuration profiles not found
- `500` — Internal server error

## GET `/configuration-profile/{name}`

Operation: `getConfigurationProfile`

Retrieve a configuration profile by name

Retrieves configuration profile details with control over the detail level

Tags: `ConfigurationProfiles`

Parameters:

- `name` path, required (string) — The name of the configuration profile
- `detailLevel` query, optional (string) — Controls the level of detail in the response - 'full' for complete profile with objects and properties, or 'summary' for just features and sub-features

Responses:

- `200` — Configuration profile details
- `400` — Invalid request parameters
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found
- `500` — Internal server error

## POST `/configuration-profile/{name}`

Operation: `createConfigProfileFromSource`

Create a configuration profile from blueprints

Creates a new configuration profile using features from one or more blueprint templates

Tags: `ConfigurationProfiles`

Parameters:

- `name` path, required (string) — Name of the new configuration profile

Request body:

- `application/json` — blueprints, description, serviceProfiles

Responses:

- `201` — Configuration profile created successfully
- `400` — Invalid request body
- `401` — Unauthorized - authentication required
- `404` — Blueprint or Service Profile not found
- `409` — Conflict - profile already exists
- `500` — Internal server error

## DELETE `/configuration-profile/{name}`

Operation: `deleteConfigurationProfile`

Delete a configuration profile

Permanently removes a configuration profile from the system

Tags: `ConfigurationProfiles`

Parameters:

- `name` path, required (string) — The name of the configuration profile to delete

Responses:

- `204` — Configuration profile deleted successfully
- `400` — Invalid request parameters
- `401` — Unauthorized - authentication required
- `403` — Forbidden delete operation
- `404` — Configuration profile not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/add-remove-features`

Operation: `addRemoveFeatures`

Add/remove features from a configuration profile

Tags: `ConfigurationProfiles`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — featuresToRemove, featuresToAdd, blueprintsToAdd

Responses:

- `200` — Features added/removed successfully
- `400` — Invalid request body
- `401` — Unauthorized - authentication required
- `403` — Forbidden delete operation
- `404` — Configuration profile or feature not found
- `409` — Conflict - feature already exists or cannot be added/removed
- `500` — Internal server error

## POST `/configuration-profile/{name}/clone`

Operation: `cloneConfigurationProfile`

Clone a configuration profile

Creates a copy of an existing configuration profile with a new name

Tags: `ConfigurationProfiles`

Parameters:

- `name` path, required (string) — Name of the source configuration profile to clone

Request body:

- `application/json` — targetName

Responses:

- `201` — Configuration profile cloned successfully
- `400` — Invalid request or target name
- `401` — Unauthorized - authentication required
- `404` — Source configuration profile not found
- `409` — Conflict - target profile already exists
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/retrieve`

Operation: `retrieveFeatureObjects`

Retrieve objects within a feature

Retrieves all or specific objects within a feature specified by featurePath

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json`

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/modify`

Operation: `modifyFeatureObjects`

Add or update objects within a feature

Adds new objects or updates existing objects within a feature specified by featurePath

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — ObjectModifyRequest

Responses:

- `200` — Objects successfully updated
- `201` — Objects successfully created
- `400` — Bad request - invalid feature path, object structure or validation failure
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `409` — Conflict - object id already exists
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/delete`

Operation: `deleteFeatureObjects`

Delete objects within a feature

Deletes objects within a feature specified by featurePath (to delete all objects within a featurePath) or list of Object ID

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json`

Responses:

- `200` — Objects successfully deleted
- `400` — Bad request - invalid feature path or object IDs
- `401` — Authorization failed
- `403` — Forbidden delete operation
- `404` — Configuration profile, feature, or object not found
- `500` — Internal Server Error

## POST `/configuration-profile/{name}/feature/object/clone`

Operation: `cloneFeatureObject`

Clone a config object within a feature

Creates a copy of an existing object along with its entire hierarchy, preserving the reference relationships within/across features in the cloned hierarchy.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — ObjectCloneRequest

Responses:

- `201` — Object cloned successfully
- `400` — Bad request
- `401` — Unauthorized request
- `404` — Configuration profile or object not found
- `409` — Object with requested key properties already exists
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/group/create`

Operation: `createObjectGroup`

Create a group from existing objects within a feature

Creates a group from existing objects specified by object IDs within a feature specified by featurePath.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile (up to 128 characters)

Request body:

- `application/json` — featurePath, groupName, objectIds

Responses:

- `201` — Group successfully created
- `400` — Bad request - invalid feature path, group name, or object IDs format
- `401` — Unauthorized - authentication required
- `404` — Configuration profile, feature, or one or more objects not found
- `409` — Conflict - group name already exists in the specified feature
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/group/delete`

Operation: `deleteObjectGroup`

Delete a group within a feature

Deletes a group specified by groupName in the request body.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile (up to 128 characters)

Request body:

- `application/json` — groupName

Responses:

- `204` — Group successfully deleted
- `400` — Bad request - invalid group name
- `401` — Unauthorized - authentication required
- `403` — Forbidden - group is assigned and cannot be deleted
- `404` — Configuration profile or group not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/group/modify`

Operation: `modifyObjectGroup`

Update objects in a configuration object group

Updates a specific configuration object group within a feature by adding or removing objects. You can specify object IDs to add to or remove from the group.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile (up to 128 characters)

Request body:

- `application/json` — groupName, newGroupName, objectIdsToAdd, objectIdsToRemove

Responses:

- `200` — Group successfully updated
- `400` — Bad request - invalid group name or object IDs format
- `401` — Unauthorized - authentication required
- `404` — Configuration profile, group, or one or more objects not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/group/clone`

Operation: `cloneObjectsGroup`

Clone a group within a feature

Creates a copy of an existing group with a new name within the same feature path

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — sourceGroupName, clonedGroupName

Responses:

- `201` — Group cloned successfully
- `400` — Bad request - invalid feature path, group names, or format
- `401` — Unauthorized - authentication required
- `404` — Configuration profile, feature, or source group not found
- `409` — Conflict - cloned group name already exists
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/retrieve-v2`

Operation: `retrieveFeatureObjectsV2`

Retrieve objects within a feature

Retrieves specified objects and its children within a feature specified by featurePath using objectType.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — ObjectRetrieveRequest

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/retrieve-summary`

Operation: `retrieveFeatureObjectsSummary`

Retrieve objects within a feature (summary view)

Retrieves specified objects and its children within a feature specified by featurePath using objectType in a summarized view.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — ObjectRetrieveRequest

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `500` — Internal server error

## GET `/configuration-profile/{name}/feature/object/retrieve-by-id`

Operation: `retrieveFeatureObjectById`

Retrieve object within a feature by Id

Retrieves specified object and its children within a feature specified by Id.

Tags: `ConfigurationFeatures`

Parameters:

- `name` path, required (string) — The name of the configuration profile
- `id` query, required (string) — The ID of the object to be retrieved
- `detailLevel` query, optional (string) — Level of detail for the retrieved object. 'full' returns related objects, 'summary' returns only the requested object.

Responses:

- `200` — Object retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `500` — Internal server error

## GET `/blueprints/categories`

Operation: `getBlueprintCategories`

Retrieve a list of blueprint categories

Returns a list of available blueprint categories.

Tags: `Blueprints`

Responses:

- `200` — List of categories
- `401` — Unauthorized - authentication required
- `500` — Internal server error

## GET `/global-profile`

Operation: `getGlobalProfile`

Retrieve the global profile feature tree

Gets the global profile containing all global features like DHCP Server, NTP Server, DNS Server, etc. Returns only the feature tree structure without object details.

Tags: `GlobalProfiles`

Responses:

- `200` — Global profile feature tree
- `401` — Authentication Failed
- `500` — Internal Server Error

## POST `/global-profile/feature/object/retrieve`

Operation: `retrieveGlobalFeatureObjects`

Retrieve objects within a global feature

Retrieves all or specific objects within a feature in the global profile

Tags: `GlobalProfiles`

Request body:

- `application/json`

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found
- `500` — Internal server error

## POST `/global-profile/feature/object/modify`

Operation: `modifyGlobalFeatureObjects`

Add or update objects within a global feature

Adds new objects or updates existing objects within a feature in the global profile

Tags: `GlobalProfiles`

Request body:

- `application/json` — ObjectModifyRequest

Responses:

- `200` — Objects successfully updated
- `201` — Objects successfully created
- `400` — Bad request - invalid feature path, object structure or validation failure
- `401` — Unauthorized - authentication required
- `404` — Global feature not found
- `409` — Conflict - object id already exists
- `500` — Internal server error

## POST `/global-profile/feature/object/delete`

Operation: `deleteGlobalFeatureObjects`

Delete objects within a global feature

Deletes objects within a feature specified by featurePath (to delete all objects within a featurePath) or list of Object ID

Tags: `GlobalProfiles`

Request body:

- `application/json`

Responses:

- `200` — Objects successfully deleted
- `400` — Bad request - invalid feature path or object IDs
- `401` — Authorization failed
- `403` — Forbidden delete operation
- `404` — Global profile, feature, or object not found
- `500` — Internal Server Error

## POST `/global-profile/feature/object/retrieve-v2`

Operation: `retrieveGlobalFeatureObjectsV2`

Retrieve global objects within a feature

Retrieves specified objects and its children within a feature specified by featurePath using objectType.

Tags: `GlobalProfiles`

Request body:

- `application/json` — ObjectRetrieveRequest

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Global profile or feature not found
- `500` — Internal server error

## POST `/global-profile/feature/usage`

Operation: `SpecificGlobalFeatureUsage`

Get configuration profiles using a specific global feature

Get a list of configuration profiles that are using a specific global feature

Tags: `GlobalProfiles`

Request body:

- `application/json` — featurePath

Responses:

- `200` — Global feature usage information
- `400` — Bad request - invalid feature path
- `401` — Authorization failed
- `404` — Global feature not found
- `500` — Internal server error

## GET `/service-profile/{name}`

Operation: `getServiceProfile`

Retrieve a service profile by name

Retrieves a service profile (full feature tree or summary) by name.

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Service profile name
- `detailLevel` query, optional (string) — full returns feature tree with objects; summary omits objects

Responses:

- `200` — Service profile details
- `400` — Invalid request parameters
- `401` — Unauthorized
- `404` — Service profile not found
- `500` — Internal server error

## POST `/service-profile/{name}`

Operation: `createServiceProfile`

Create a service profile from a blueprint

Creates a new service profile using the full feature tree from a single blueprint. No feature data supplied in request body.

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Name of the new service profile

Request body:

- `application/json` — description

Responses:

- `201` — Service profile created successfully
- `400` — Invalid request body
- `401` — Unauthorized - authentication required
- `409` — Conflict - service profile already exists
- `500` — Internal server error

## PATCH `/service-profile/{name}`

Operation: `updateServiceProfile`

Update a service profile (description only)

Updates mutable fields of a service profile. Name is immutable. Currently only 'description' can be modified.

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Service profile name (immutable)

Request body:

- `application/json` — ServiceProfileUpdateRequest

Responses:

- `200` — Service profile updated successfully
- `400` — Invalid request body (e.g., attempting to change name or empty body)
- `401` — Unauthorized - authentication required
- `404` — Service profile not found
- `500` — Internal server error

## DELETE `/service-profile/{name}`

Operation: `deleteServiceProfile`

Delete a service profile

Permanently deletes a service profile. Fails if referenced by one or more configuration profiles unless those references are removed first.

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Service profile name to delete

Responses:

- `204` — Service profile deleted successfully (no response body)
- `400` — Invalid request parameters
- `401` — Unauthorized - authentication required
- `403` — Forbidden - insufficient permissions
- `404` — Service profile not found
- `409` — Conflict - service profile in use
- `500` — Internal server error

## POST `/service-profiles`

Operation: `retrieveServiceProfiles`

Retrieve service profiles by name or feature criteria

Provide either 'name' OR both 'featureName' and 'featureValue'. Returns matching service profiles.

Tags: `ServiceProfiles`

Parameters:

- `detailLevel` query, optional (string) — full returns feature tree with objects; list returns only service profile names

Responses:

- `200` — Matching service profiles
- `400` — Invalid filter combination
- `401` — Unauthorized
- `404` — No matching service profiles found
- `500` — Internal server error

## POST `/service-profile/{name}/feature/object/retrieve`

Operation: `retrieveServiceProfileFeatureObjects`

Retrieve objects within a feature

Retrieves all or specific objects within a feature specified by featurePath

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — The name of the service profile

Request body:

- `application/json`

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Service profile or feature not found
- `500` — Internal server error

## POST `/service-profile/{name}/feature/object/retrieve-v2`

Operation: `retrieveServiceProfileFeatureObjectsV2`

Retrieve service profile objects within a feature

Retrieves specified objects and its children within a feature specified by featurePath using objectType.

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — The name of the service profile

Request body:

- `application/json` — ObjectRetrieveRequest

Responses:

- `200` — Objects retrieved successfully
- `400` — Bad request - invalid feature path or object types
- `401` — Unauthorized - authentication required
- `404` — Global profile or feature not found
- `500` — Internal server error

## POST `/service-profile/{name}/feature/object/modify`

Operation: `modifyServiceProfileFeatureObjects`

Add or update objects within a feature

Adds new objects or updates existing objects within a feature specified by featurePath

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Service profile name

Request body:

- `application/json` — featurePath, operation, objects

Responses:

- `200` — Successful operation
- `400` — Bad request - invalid feature path or object IDs
- `401` — Unauthorized
- `404` — Service profile, feature, or objects not found
- `500` — Internal server error

## POST `/service-profile/{name}/feature/object/delete`

Operation: `deleteServiceProfileFeatureObjects`

Delete objects within a feature of a service profile

Deletes objects within a feature specified by featurePath (all objects) or by objectIds (specific objects).

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Service profile name

Request body:

- `application/json`

Responses:

- `200` — Objects deleted (success/failure per object)
- `400` — Bad request - invalid feature path or object IDs
- `401` — Unauthorized
- `404` — Service profile, feature, or objects not found
- `500` — Internal server error

## GET `/service-profile/{name}/usage`

Operation: `getServiceProfileUsageInConfigurationProfiles`

Get configuration profiles using a specific service profile name

Retrieves list of configuration profiles that reference a specific feature defined within service profiles

Tags: `ServiceProfiles`

Parameters:

- `name` path, required (string) — Name of the service profile

Responses:

- `200` — Configuration profile usage information for the service profile feature
- `400` — Bad request - invalid feature name
- `401` — Unauthorized - authentication required
- `404` — Feature not found in any configuration profile
- `500` — Internal server error

## POST `/authorized/sites-sitegroups/retrieve`

Operation: `getCustomerAuthorizedSitesAndSiteGroups`

Get all sites and site groups available customer is authorized to use

Retrieves all sites and site groups that are owned by the customer is authorized to use for target query selection. Supports optional pagination through request body.

Tags: `TargetQuery`

Request body:

- `application/json` — PaginatedQueryRequest

Responses:

- `200` — Successfully retrieved sites and site groups customer is authorized to use for target query selection
- `400` — Bad request - invalid query parameters
- `401` — Unauthorized - authentication required
- `404` — No authorized sites or site groups found
- `500` — Internal server error

## GET `/configuration-profile/{name}/models/retrieve`

Operation: `getTargetQueryModels`

Get all models either from defined scope or from all supported by org

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile that provides the configuration profile-level context for target query
- `scoped` query, optional (boolean) — If true, only models within the selected scope are returned. If false or not present, all models available to the company are returned.

Responses:

- `200` — Successfully retrieved device models available for target query selection
- `400` — Bad request - invalid configuration profile name or query parameters
- `401` — Unauthorized - authentication required
- `403` — Forbidden - insufficient permissions
- `404` — Configuration profile not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/scoped/devices/retrieve`

Operation: `postTargetQueryScopedDevices`

Get devices available for defined scope (supports optional pagination in request body)

Retrieves devices within the configuration profile's defined scope. Supports optional pagination via a request body containing a `paginationQuery` (pageNumber, pageSize). Also supports optional `filterQuery` and `fuzzySearchQuery`.

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — PaginatedQueryRequest

Responses:

- `200` — Successfully retrieved devices available for defined scope of configuration profile
- `400` — Bad request - invalid query parameters
- `401` — Unauthorized - authentication required
- `403` — Forbidden - insufficient permissions
- `404` — Configuration profile not found
- `500` — Internal server error

## GET `/configuration-profile/{name}/scope`

Operation: `getTargetQueryScope`

Get current target query scope

Retrieves the current scope selection for the target query.

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Responses:

- `200` — Successfully retrieved target query scope
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found or no scope set
- `500` — Internal server error

## POST `/configuration-profile/{name}/scope`

Operation: `setTargetQueryScope`

Set target query scope by selecting site groups

Sets the initial scope for target query by selecting one or more site and site groups. This defines the universe of sites/devices available for subsequent target query selections.

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — selectedSiteGroups, selectedSites

Responses:

- `201` — Target query scope set successfully
- `400` — Bad request - invalid request body, site group selection, or validation failure
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found
- `409` — Conflict - scope already exists for this configuration profile
- `500` — Internal server error

## GET `/configuration-profile/{name}/target-query/profile`

Operation: `getTargetQueryFromProfile`

Get target query associated with configuration profile

Retrieves the saved target query criteria for a configuration profile so UI can display the previously saved selection. Supports optional pagination for resolved devices.

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `pageNumber` query, optional (integer) — Page number for pagination (1-based)
- `pageSize` query, optional (integer) — Number of devices per page

Responses:

- `200` — Target query criteria and resolved devices retrieved successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found or no target query associated
- `500` — Internal server error

## POST `/configuration-profile/{name}/target-query/profile`

Operation: `associateTargetQueryToProfile`

Associate target query with configuration profile

Associates targeting query with a configuration profile to determine which devices will receive this configuration

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — TargetQueryWithPagination

Responses:

- `200` — Target query associated successfully with resolved devices
- `400` — Invalid target query
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## DELETE `/configuration-profile/{name}/target-query/profile`

Operation: `removeTargetQueryFromProfile`

Remove target query from configuration profile

Removes the association between a configuration profile and its target query

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Responses:

- `204` — Target query removed successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## GET `/configuration-profile/{name}/target-query/feature/{featureId}`

Operation: `getTargetQueryFromFeature`

Get target query associated with configuration feature

Retrieves the saved target query criteria for a configuration feature so UI can display the previously saved selection

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `featureId` path, required (string) — ID of the configuration feature that provides the context for the target query

Responses:

- `200` — Target query criteria and resolved devices retrieved successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or feature not found, or no target query associated
- `500` — Internal server error

## POST `/configuration-profile/{name}/target-query/feature/{featureId}`

Operation: `associateTargetQueryToFeature`

Associate target query with configuration feature

Associates a device targeting query with a feature to determine which devices will receive this configuration

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `featureId` path, required (string) — ID of the configuration feature that provides the context for the target query

Request body:

- `application/json` — TargetQuery

Responses:

- `200` — Target query associated successfully with resolved devices
- `400` — Invalid target query
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## DELETE `/configuration-profile/{name}/target-query/feature/{featureId}`

Operation: `removeTargetQueryFromFeature`

Remove target query from configuration feature

Removes the association between a configuration feature and its target query

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `featureId` path, required (string) — ID of the configuration feature that provides the context for the target query

Responses:

- `204` — Target query removed successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## GET `/configuration-profile/{name}/target-query/object/{objectId}`

Operation: `getTargetQueryFromObject`

Get target query associated with configuration object

Retrieves the saved target query criteria for a configuration object so UI can display the previously saved selection. Supports optional pagination for resolved devices.

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `objectId` path, required (string) — ID of the configuration object that provides the context for the target query
- `pageNumber` query, optional (integer) — Page number for pagination (1-based)
- `pageSize` query, optional (integer) — Number of devices per page

Responses:

- `200` — Target query criteria and resolved devices retrieved successfully
- `400` — Bad request - Invalid pagination parameters or path parameters
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or object not found, or no target query associated
- `500` — Internal server error

## POST `/configuration-profile/{name}/target-query/object/{objectId}`

Operation: `associateTargetQueryToObject`

Associate target query with configuration object

Associates a device targeting query with a configuration object to determine which devices will receive this configuration

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `objectId` path, required (string) — ID of the configuration object that provides the context for the target query

Request body:

- `application/json` — TargetQuery

Responses:

- `200` — Target query associated successfully with resolved devices
- `400` — Invalid target query
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## DELETE `/configuration-profile/{name}/target-query/object/{objectId}`

Operation: `removeTargetQueryFromObject`

Remove target query from configuration object

Removes the association between a configuration object and its target query

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration Profile
- `objectId` path, required (string) — ID of the configuration object that provides the context for the target query

Responses:

- `204` — Target query removed successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## GET `/configuration-profile/{name}/target-query/object-group/{objectGroupId}`

Operation: `getTargetQueryFromObjectGroup`

Get target query associated with configuration object group

Retrieves the saved target query criteria for a configuration object group so UI can display the previously saved selection

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `objectGroupId` path, required (string) — ID of the configuration object group that provides the context for the target query

Responses:

- `200` — Target query criteria and resolved devices retrieved successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or object group not found, or no target query associated
- `500` — Internal server error

## POST `/configuration-profile/{name}/target-query/object-group/{objectGroupId}`

Operation: `associateTargetQueryToObjectGroup`

Associate target query with configuration object group

Associates a device targeting query with a configuration object group to determine which devices will receive this configuration

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `objectGroupId` path, required (string) — ID of the configuration object group that provides the context for the target query

Request body:

- `application/json` — TargetQuery

Responses:

- `200` — Target query associated successfully with resolved devices
- `400` — Invalid target query
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## DELETE `/configuration-profile/{name}/target-query/object-group/{objectGroupId}`

Operation: `removeTargetQueryFromObjectGroup`

Remove target query from configuration object group

Removes the association between a configuration object group and its target query

Tags: `TargetQuery`

Parameters:

- `name` path, required (string) — Name of the configuration Profile
- `objectGroupId` path, required (string) — ID of the configuration object that provides the context for the target query

Responses:

- `204` — Target query removed successfully
- `401` — Unauthorized - authentication required
- `404` — Configuration profile not found

## GET `/inventory/models`

Operation: `getAllModels`

Retrieve all available device models

Retrieves a list of all device models available in the system. This includes both switches and access points. This API is independent of configuration profiles and can be used to get a complete catalog of supported models.

Tags: `Inventory`

Responses:

- `200` — Models retrieved successfully
- `401` — Unauthorized - authentication required
- `500` — Internal server error

## GET `/inventory/port-types`

Operation: `getAllPortTypes`

Retrieve all available port types

Retrieves a list of all port types available in the system. Port types define the characteristics and capabilities of network ports (e.g., access port, trunk port, uplink port). This API is independent of configuration profiles and models, providing a complete catalog of supported port types.

Tags: `Inventory`

Responses:

- `200` — Port types retrieved successfully
- `401` — Unauthorized - authentication required
- `500` — Internal server error

## POST `/inventory/models/modelVariants/retrieve`

Operation: `retrieveModelVariants`

Retrieve variants for one or more device models

Retrieves all available variants for the specified device models (switches or access points). Each variant represents different port configurations (e.g., number of ports, PoE capabilities). This API is independent of configuration profiles and can be used across multiple profiles. Supports both single model and multiple model queries through the request body.

Tags: `Inventory`

Request body:

- `application/json` — modelNames

Responses:

- `200` — Model variants retrieved successfully
- `400` — Bad request - invalid request body or empty model list
- `404` — One or more models not found
- `500` — Internal server error

## POST `/inventory/models/modelVariants/porttypes/skus-retrieve`

Operation: `retrieveSkusByModelVariantsPorttypes`

Retrieve Extreme Networks device SKUs based on models, variants, port types, and OS

Retrieves all available Extreme Networks device SKUs (Stock Keeping Units) that match the specified filter criteria. You can filter by one or more of the following: models, variants, port types, and operating system types. This API supports flexible filtering: - Provide only **modelNames** to get all SKUs for those models - Provide only **variantIds** to get SKUs for specific variants across all models - Provide only **portTypeIds** to get SKUs that support specific port types - Provide only **osTypes** to get SKUs supporting specific operating systems - Provide **modelNames** and **variantIds** to get SKUs for specific model-variant combinations - Provide **modelNames**, **variantIds**, **portTypeIds**, and **osTypes** to get SKUs matching all criteria - Provide any combination of the above filters **Response includes detailed information for UI display:** - **Configurable Ports**: Module-level port configuration with slot numbers, port ranges, and types - **Speed Capability**: Detailed port speed specifications for each port type For Extreme Networks Switches: SKUs are associated with specific variants and port types within a model family. For Extreme Networks Access Points: SKUs are tied to the model, with variants affecting region/radio rules. This API is independent of configuration profiles and can be used across multiple profiles.

Tags: `Inventory`

Request body:

- `application/json` — modelNames, variantIds, portTypeIds, osTypes

Responses:

- `200` — SKUs retrieved successfully based on the provided filters
- `400` — Bad request - invalid request body or filter parameters
- `404` — No SKUs found matching the provided filters, or one or more filter values not found
- `500` — Internal server error

## POST `/inventory/models/hosts/porttypes/skus-retrieve`

Operation: `retrieveSkusByModelHostsPorttypes`

Retrieve Extreme Networks device SKUs by hostname with optional filters

Retrieves all available Extreme Networks device SKUs (Stock Keeping Units) and detailed configuration information for one or more device hostnames. This endpoint automatically determines the variant, model, and capabilities based on the actual deployed devices, making it useful when you have specific devices and want to know their configuration options. The hostname is used to lookup the actual device in the system and determine its variant characteristics, model, OS type, and port configurations. This API supports multiple query modes: 1. **Model-specific lookup**: Provide both modelName and hostName to validate the device matches the expected model 2. **Model-agnostic lookup**: Provide only hostName to retrieve SKUs/configurations regardless of model 3. **Filtered lookup**: Provide hostNames with optional portTypeIds and osTypes filters **Response includes detailed information for UI display:** - **Configurable Ports**: Module-level port configuration with slot numbers, port ranges, and types - **Speed Capability**: Detailed port speed specifications for each port type This API is independent of configuration profiles and can be used across multiple profiles.

Tags: `Inventory`

Request body:

- `application/json` — hostNames, modelNames, portTypeIds, osTypes

Responses:

- `200` — SKUs and detailed configuration retrieved successfully for all requested Extreme Networks devices
- `400` — Bad request - invalid request body or empty devices list
- `404` — One or more devices not found or model mismatch
- `500` — Internal server error

## POST `/configuration-profile/{name}/models/scoped/devices/retrieve`

Operation: `retrieveProfileModelDevices`

Retrieve devices for one or more models within a configuration profile's scope

Retrieves a comprehensive list of all devices that match one or more specified models within the scope of the specified configuration profile. Each device includes hostname, location, IP address, device type, and slot information with SKUs. For devices with multiple slots, each slot will have its own SKU information. This API respects the configuration profile's scope (site groups/sites) and only returns devices within that scope. This API is useful for getting an overview of all devices of particular models that are available for configuration within a specific profile. Supports both single model and multiple model queries through the request body.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — modelNames, includeSlotDetails, paginationQuery

Responses:

- `200` — Device list retrieved successfully for all requested models
- `400` — Bad request - invalid request body or empty model list
- `404` — Configuration profile not found, or one or more models not found, or no devices found
- `500` — Internal server error

## GET `/configuration-profile/{name}/port-profile`

Operation: `getPortProfiles`

Get all port profiles for a configuration profile

Retrieves all port profiles defined in the specified configuration profile. Each port profile includes name, port type, port mapping, and description.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Responses:

- `200` — Port profiles retrieved successfully
- `404` — Configuration profile not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/port-profile/{portProfileName}/port-mappings/retrieve`

Operation: `retrievePortMappingsByPortProfile`

Retrieve all port mappings for a specific port profile

Retrieves all port mappings that are associated with a specific port profile within the specified configuration profile. This API is useful when a user clicks on a port profile and wants to see all the different port mappings (rules) that use that port profile. For example, a trunk port profile might have multiple port mappings with different target query rules applied to different sites or device groups. The port profile can be identified by either portProfileName (path parameter) or objectId (query parameter). If both are provided, objectId takes precedence.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `portProfileName` path, required (string) — Name of the port profile to retrieve port mappings for
- `objectId` query, optional (string) — Object ID of the port profile (alternative to portProfileName)

Responses:

- `200` — Port mappings for the specified port configuration retrieved successfully
- `400` — Invalid request parameters
- `404` — Configuration profile or port configuration not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/port-mappings`

Operation: `createPortMapping`

Create a new port mapping with device resolution

Creates a new port mapping for the selected port configuration and returns the resolved devices that match the inventory criteria. Port mapping associates a port configuration with specific switches and ports, and the response includes the devices that will receive this configuration.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — PortMappingCreate

Responses:

- `201` — Port mapping created successfully with resolved devices
- `400` — Invalid port mapping data
- `404` — Configuration profile or port configuration not found
- `409` — Port mapping with same name already exists
- `500` — Internal server error

## DELETE `/configuration-profile/{name}/port-mappings`

Operation: `deletePortMapping`

Delete a port mapping from a configuration profile

Deletes a specific port mapping from the configuration profile. The port mapping can be identified by either its name or ID. This operation permanently removes the port mapping and its associated target query configuration.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `portMappingName` query, optional (string) — Name of the port mapping to delete (use either this or portMappingId)
- `portMappingId` query, optional (string) — ID of the port mapping to delete (use either this or portMappingName)

Responses:

- `204` — Port mapping deleted successfully (no content returned)
- `400` — Bad request - must provide either portMappingName or portMappingId, but not both
- `404` — Configuration profile or port mapping not found
- `409` — Conflict - port mapping is in use and cannot be deleted
- `500` — Internal server error

## POST `/configuration-profile/{name}/port-mappings/modify`

Operation: `modifyPortMapping`

Modify an existing port mapping with device resolution

Modifies an existing port mapping with new configuration details and returns the resolved devices that match the updated target query criteria. The port mapping can be identified by either its name or ID in the request body. **Priority**: When updating priority, ensure the new value doesn't conflict with existing port mappings on overlapping ports. Lower priority numbers (closer to 1) indicate higher precedence for conflict resolution. **Note**: This endpoint follows the same structure as the create endpoint but requires an identifier (portMappingName or portMappingId) in the request body to specify which port mapping to modify.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — portMappingName, portMappingId, portMappingDetails, selectSwitches, portSelection

Responses:

- `200` — Port mapping updated successfully with resolved devices
- `400` — Invalid port mapping data or missing identifier
- `404` — Configuration profile, port mapping, or port configuration not found
- `409` — Conflict - port mapping is deployed and cannot be updated, or update would create conflicts
- `500` — Internal server error

## POST `/configuration-profile/{name}/port-mappings/update-priorities`

Operation: `updatePortMappingPriorities`

Update priorities for one or more port mappings

Updates the priority values for one or more port mappings within a configuration profile. This API allows bulk priority updates in a single operation, useful for reordering port mappings or adjusting conflict resolution precedence. **How Priority Works**: - Priority is auto-assigned sequentially (1, 2, 3...) during creation - Lower numbers = higher precedence for port conflict resolution - Each profile maintains independent priority sequences - Gaps are automatically closed when port mappings are deleted **Update Behavior**: - Provide new priority values for specific port mappings - Other port mappings are automatically resequenced to maintain sequential order - If you set priority=1 for a mapping that was priority=5, others shift accordingly - Final result always maintains 1, 2, 3, 4... sequence with no gaps **Request Format**: Each port mapping update requires either `portMappingName` OR `portMappingId` plus the new `priority` value.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — priorityUpdates

Responses:

- `200` — Priorities updated successfully with final resequenced values
- `400` — Bad request - invalid priority values or identifiers
- `404` — Configuration profile or port mapping not found
- `409` — Conflict - port mapping is deployed and cannot be updated
- `500` — Internal server error

## POST `/configuration-profile/{name}/port-mappings/retrieve`

Operation: `retrievePortMappings`

Retrieve port mappings for a profile with advanced filtering and pagination

Retrieves port mappings defined in the specified configuration profile along with their resolved devices. Supports advanced pagination via request body containing `paginationQuery` (pageNumber, pageSize). Also supports optional `filterQuery` for port configuration name filtering, priority range filtering, and `fuzzySearchQuery` for text search. Each port mapping includes name, port configuration reference, priority, target query details, switch/port specifications, and the devices that match the target query criteria. **Priority Filtering**: Use the priority filter to find port mappings within specific priority ranges, useful for reviewing conflict resolution order or managing high/low priority configurations.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — paginationQuery, filterQuery, fuzzySearchQuery

Responses:

- `200` — Port mappings retrieved successfully with resolved devices
- `400` — Invalid request parameters
- `404` — Configuration profile not found
- `500` — Internal server error

## GET `/configuration-profile/{name}/lag-configurations`

Operation: `getLAGConfigurations`

Retrieve all LAG configurations for a configuration profile

Retrieves all Link Aggregation Group (LAG) configurations defined in the specified configuration profile. Each LAG configuration includes LAG details, settings, target switch criteria, port selection, and LACP settings. Supports optional pagination and filtering.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `pageNumber` query, optional (integer) — Page number for pagination (1-based)
- `pageSize` query, optional (integer) — Number of LAG configurations per page
- `filterByMLTID` query, optional (string) — Filter LAG configurations by MLT ID

Responses:

- `200` — LAG configurations retrieved successfully
- `404` — Configuration profile not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/lag-configurations`

Operation: `createLAGConfiguration`

Create a new LAG configuration with device resolution

Creates a new Link Aggregation Group (LAG) configuration for the specified configuration profile. The LAG configuration includes LAG properties (name, description, MLT ID, load balancing algorithm, LACP key), target switch selection criteria, and port selection with LACP settings. The response includes resolved devices that match the target query criteria and will receive this LAG configuration.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile

Request body:

- `application/json` — LAGConfigurationCreate

Responses:

- `201` — LAG configuration created successfully with resolved devices
- `400` — Invalid LAG configuration data
- `404` — Configuration profile not found
- `409` — Conflict - LAG configuration with same name or MLT ID already exists
- `500` — Internal server error

## DELETE `/configuration-profile/{name}/lag-configurations`

Operation: `deleteLAGConfiguration`

Delete a LAG configuration from a configuration profile

Deletes a specific LAG configuration from the configuration profile. The LAG configuration can be identified by either its name, ID, or MLT ID. This operation permanently removes the LAG configuration and its associated target query configuration. **Warning**: Deleting an active LAG configuration will disrupt network connectivity. Ensure proper migration or maintenance windows before deletion.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `lagName` query, optional (string) — Name of the LAG configuration to delete (use one of lagName, lagId, or mltId)
- `lagId` query, optional (string) — ID of the LAG configuration to delete (use one of lagName, lagId, or mltId)
- `mltId` query, optional (string) — MLT ID of the LAG configuration to delete (use one of lagName, lagId, or mltId)

Responses:

- `204` — LAG configuration deleted successfully (no content returned)
- `400` — Bad request - must provide exactly one identifier (lagName, lagId, or mltId)
- `404` — Configuration profile or LAG configuration not found
- `409` — Conflict - LAG configuration is in use and cannot be deleted
- `500` — Internal server error

## GET `/configuration-profile/{name}/lag-configurations/{identifier}`

Operation: `getLAGConfigurationByIdentifier`

Retrieve a specific LAG configuration by name, ID, or MLT ID

Retrieves a specific Link Aggregation Group (LAG) configuration from the specified configuration profile. The LAG configuration can be identified by name, UUID, or MLT ID in the path parameter. Returns the complete LAG configuration details including LAG settings, target switch criteria, port selection, LACP settings, and resolved devices that match the target query.

Tags: `PortMapping`

Parameters:

- `name` path, required (string) — Name of the configuration profile
- `identifier` path, required (string) — LAG configuration identifier - can be: - LAG name (e.g., "Core-Uplink-LAG") - LAG UUID (e.g., "770e8400-e29b-11d4-a716-446655440001") - MLT ID (e.g., "100")
- `includeDevices` query, optional (boolean) — Whether to include resolved devices in the response

Responses:

- `200` — LAG configuration retrieved successfully
- `400` — Invalid identifier format
- `404` — Configuration profile or LAG configuration not found
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/override/create-update`

Operation: `overrideFeatureObject`

Create or update overrides for config objects

Creates or updates overrides for multiple config objects. Supports device-level, model-level, and model-group-level overrides. The backend will decide whether to create new overrides or update existing ones based on the object ID, override type, and target ID combination.

Tags: `Override`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — array

Responses:

- `200` — Overrides updated successfully or with partial success
- `201` — Overrides created successfully or with partial success
- `400` — Bad request - invalid input parameters
- `404` — Not found - configuration profile or object does not exist
- `500` — Internal server error

## GET `/configuration-profile/{name}/feature/object/override/retrieve`

Operation: `retrieveFeatureObjectOverride`

Retrieve complete object with override context

Returns the complete configuration object with all properties, including both overridden and non-overridden properties. Shows the current effective values along with override indicators. For overridden properties, includes the sourceValue field showing what the value would be without the override. Properties are returned as a map keyed by property name, with each property containing name, label, description, type, value, origin, and sourceValue (for overridden properties only).

Tags: `Override`

Parameters:

- `name` path, required (string) — The name of the configuration profile
- `objectId` query, required (string) — UUID of the config object to retrieve with override context

Responses:

- `200` — Override retrieved successfully
- `400` — Bad request - invalid input parameters
- `404` — Not found - configuration profile, object, or override does not exist
- `500` — Internal server error

## POST `/configuration-profile/{name}/feature/object/override/delete`

Operation: `deleteFeatureObjectOverride`

Delete a specific override for a config object

Deletes a specific override (device, model, or model-group) for a config object. Once deleted, the object will inherit values from the next level in the hierarchy (device inherits from model, model from model-group, model-group from profile)

Tags: `Override`

Parameters:

- `name` path, required (string) — The name of the configuration profile

Request body:

- `application/json` — ObjectOverrideRetrieveRequest

Responses:

- `204` — Override deleted successfully - No Content
- `400` — Bad request - invalid input parameters
- `404` — Not found - configuration profile, object, or override does not exist
- `500` — Internal server error

## GET `/configuration-profile/{name}/feature/object/overrides`

Operation: `listObjectOverridesByQuery`

Get list of all overrides on a config object

Returns a summary list of all overrides (device, model, and model-group) configured for a specific object, without including the full object details or property values

Tags: `Override`

Parameters:

- `name` path, required (string) — The name of the configuration profile
- `objectId` query, required (string) — UUID of the config object

Responses:

- `200` — List of overrides retrieved successfully
- `400` — Bad request - invalid parameters
- `401` — Unauthorized - authentication required
- `404` — Configuration profile or object not found
- `500` — Internal server error

