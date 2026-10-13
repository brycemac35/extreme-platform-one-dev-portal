---
source: https://developer.extremeplatformone.com/api-reference/uztna
spec: https://developer.extremeplatformone.com/api/spec/uztna
title: "Platform ONE Security OpenAPI Specs"
---

# Platform ONE Security OpenAPI Specs

**Security** · Applications. Security.

The OpenAPI specification provides a detailed description of the Platform ONE Security services API. This API enables seamless integration and interaction with the platform for managing user groups, device groups, devices, and access control capabilities. 🔑 Key Features: **User Group Operations** Create, update, retrieve, and manage user groups with detailed access control and user association capabilities. **Device Group Operations** Manage device groups with features like creating, updating, deleting, and retrieving device group details, including device associations and metadata. **Device Operations** Search, filter, and manage devices with advanced query capabilities, including action logs and pagination. **Access Control** Manage device access permissions with operations to allow or revoke access for specific devices. **End System Data Management** Manage and retrieve End system data. **Disconnect Client Sessions** Disconnect one or more client sessions. 🏢 Enterprise-Ready: Designed for enterprise-grade environments, this API ensures secure and scalable operations with support for pagination, filtering, and detailed response schemas. It also includes vendor extensions for enhanced documentation and integration capabilities.

Version: `25.11.0-20260522`

## Servers

- `https://cloudapi.extremecloudiq.com/uztna` — Extreme Platform ONE REST API - Security

Full OpenAPI document: [`specs/uztna.json`](../../specs/uztna.json)

## Endpoints

15 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/admin/resource/api/v2/access-groups` | Get the list of user groups |
| POST | `/admin/resource/api/v2/access-groups` | Create a user group |
| GET | `/admin/resource/api/v2/access-groups/{id}` | Get the user group by ID |
| PATCH | `/admin/resource/api/v2/access-groups/{id}` | Add or remove users from user group |
| GET | `/admin/resource/api/v2/access-groups/associations/{access_group_id}/details` | Get users associated with user group |
| GET | `/admin/resource/api/v2/resources/device-groups` | Get a list of device groups |
| POST | `/admin/resource/api/v2/resources/device-groups` | Create a device group |
| PATCH | `/admin/resource/api/v2/resources/device-groups/{device_group_id}` | Update a device group |
| DELETE | `/admin/resource/api/v2/resources/device-groups/{device_group_id}` | Delete a device group |
| GET | `/admin/resource/api/v2/resources/device-groups/associations/details` | Get device group associations list |
| PATCH | `/admin/resource/api/v2/resources/devices/access` | Revoke or allow device access |
| GET | `/admin/resource/api/v2/resources/devices/search-devices` | Retrieve devices list |
| GET | `/admin/auth/api/v2/accounts/workspace-users` | List of all End Users |
| GET | `/cnac/endsystem-service/api/endsystems/v2/clients` | Get Client list |
| POST | `/cnac/network-policy-engine/api/v1/npe/external/deauth` | Disconnect one or more client sessions |

## GET `/admin/resource/api/v2/access-groups`

Operation: `getUserGroups`

Get the list of user groups

Retrieve a paginated list of user groups. Supports pagination using `limit` and `offset`. Use `ordering` to sort results and `search` to filter by name or description.

Tags: `User Groups`

Parameters:

- `limit` query, optional (integer) — Number of results to return per page.
- `offset` query, optional (integer) — The initial index from which to return the results.
- `ordering` query, optional (string) — Field used to order the results. Defaults to user group name.
- `search` query, optional (string) — User group search by description or name.

Responses:

- `200` — List of user groups.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## POST `/admin/resource/api/v2/access-groups`

Operation: `createUserGroup`

Create a user group

Create a new user group with a unique name.

Tags: `User Groups`

Request body:

- `application/json` — AccessGroupRequest
- `application/x-www-form-urlencoded` — AccessGroupRequest
- `multipart/form-data` — AccessGroupRequest

Responses:

- `200` — User group created successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/resource/api/v2/access-groups/{id}`

Operation: `getUserGroupbyId`

Get the user group by ID

Retrieve a specific user group by its unique ID.

Tags: `User Groups`

Parameters:

- `id` path, required (string) — The unique identifier of the user group.
- `search` query, optional (string) — User group search by description or name.

Responses:

- `200` — User group details retrieved successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## PATCH `/admin/resource/api/v2/access-groups/{id}`

Operation: `updateUserGroup`

Add or remove users from user group

Update a user group by adding or removing users or updating name or description field.

Tags: `User Groups`

Parameters:

- `id` path, required (string) — The unique identifier of the user group to update.

Request body:

- `application/json` — PatchedAccessGroupRequest
- `application/x-www-form-urlencoded` — PatchedAccessGroupRequest
- `multipart/form-data` — PatchedAccessGroupRequest

Responses:

- `200` — User group updated successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/resource/api/v2/access-groups/associations/{access_group_id}/details`

Operation: `getUserGroupDetailsWithPagination`

Get users associated with user group

Get users associated with user group.

Tags: `User Groups`

Parameters:

- `access_group_id` path, required (string) — User Group ID
- `limit` query, optional (integer) — Number of users to fetch
- `offset` query, optional (integer) — Offset for pagination
- `search` query, optional (string) — Search users by email

Responses:

- `200` — Associated Users.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/resource/api/v2/resources/device-groups`

Operation: `getDeviceGroups`

Get a list of device groups

Retrieve a list of device groups. Supports pagination using `limit` and `offset`. Use `search` to filter by group name or description.

Tags: `Device Groups`

Parameters:

- `limit` query, optional (integer) — Number of results to return per page.
- `offset` query, optional (integer) — The initial index from which to return the results.
- `ordering` query, optional (string) — Field used to order the results. Defaults to device group name.
- `search` query, optional (string) — Search device groups by name or description.

Responses:

- `200` — List of device groups.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## POST `/admin/resource/api/v2/resources/device-groups`

Operation: `createDeviceGroups`

Create a device group

Create a new device group. Rules: - `name` must be unique. - If `workspace_all_devices` is true, `device_ids` must not be provided. - If `workspace_all_devices` is false, `device_ids` may be provided. - `meta_data` is required when `type` is `MAC_OUI` or `CUSTOM_MAC`. - `meta_data` must be empty when `type` is `DEVICE`. This endpoint creates and configures a device group based on the provided configuration.

Tags: `Device Groups`

Request body:

- `application/json` — DeviceGroupPostRequest
- `application/x-www-form-urlencoded` — DeviceGroupPostRequest
- `multipart/form-data` — DeviceGroupPostRequest

Responses:

- `200` — Device group created successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## PATCH `/admin/resource/api/v2/resources/device-groups/{device_group_id}`

Operation: `patchDeviceGroups`

Update a device group

Partially update a device group. All fields are optional. - `device_ids.added_devices` adds devices. - `device_ids.removed_devices` removes devices. - Setting `workspace_all_devices` to true includes all devices. - If changing `type` to `MAC_OUI` or `CUSTOM_MAC`, `meta_data` must be provided. This endpoint updates the device group configuration according to the provided fields.

Tags: `Device Groups`

Parameters:

- `device_group_id` path, required (string) — Device Group unique identifier (UUID).

Request body:

- `application/json` — PatchedPatchedDeviceGroupPostRequest
- `application/x-www-form-urlencoded` — PatchedPatchedDeviceGroupPostRequest
- `multipart/form-data` — PatchedPatchedDeviceGroupPostRequest

Responses:

- `200` — Device group updated successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## DELETE `/admin/resource/api/v2/resources/device-groups/{device_group_id}`

Operation: `deleteDeviceGroups`

Delete a device group

Delete an existing device group by its unique identifier.

Tags: `Device Groups`

Parameters:

- `device_group_id` path, required (string) — Device Group unique identifier (UUID).

Responses:

- `200` — Device Group has been successfully deleted.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/resource/api/v2/resources/device-groups/associations/details`

Operation: `getDeviceGroupDetailsWithPagination`

Get device group associations list

Get device group details.

Tags: `Device Groups`

Parameters:

- `device_group_id` query, required (string) — Device group ID
- `limit` query, optional (integer) — Number of results to return per page.
- `offset` query, optional (integer) — The initial index from which to return the results.
- `search` query, optional (string) — Search query based on Device alias, or MAC address, MDM Type, or MAC OUI. Applicable only when type is DEVICE.
- `type` query, required (string) — Type of device group. Must be one of: DEVICE, MAC_OUI, CUSTOM_MAC.

Responses:

- `200` — Device group details fetched successfully.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## PATCH `/admin/resource/api/v2/resources/devices/access`

Operation: `manageDeviceAccess`

Revoke or allow device access

Revoke or allow device access for users or specific devices (by MAC address). You can provide a list of user emails in `users` and/or MAC addresses in `mac_addresses`. The `operation` field determines whether access will be 'ALLOWED' or 'REVOKED'.

Tags: `Devices`

Request body:

- `application/json` — PatchedPatchedDeviceAccessManagementRequest
- `application/x-www-form-urlencoded` — PatchedPatchedDeviceAccessManagementRequest
- `multipart/form-data` — PatchedPatchedDeviceAccessManagementRequest

Responses:

- `200` — Device access successfully updated.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/resource/api/v2/resources/devices/search-devices`

Operation: `searchDevicesList`

Retrieve devices list

Retrieve a paginated list of all devices belonging to a Tenant. Supports pagination using `limit` and `offset`. Each device object includes all fields defined in the WorkspaceDeviceSerializer.

Tags: `Devices`

Parameters:

- `limit` query, optional (integer) — Number of results to return per page.
- `offset` query, optional (integer) — The initial index from which to return the results.

Responses:

- `200` — List of devices.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/admin/auth/api/v2/accounts/workspace-users`

Operation: `workspaceUsersList`

List of all End Users

Retrieve a paginated list of all end users. This included both IDP synced users as well as local users.

Tags: `Users`

Parameters:

- `blocked_users` query, optional (boolean) — Filter users based on access status. Set to 'true' to get blocked users (blocked_users=True), 'false' to get active users (blocked_users=False). If not provided, returns all users.
- `limit` query, optional (integer) — Number of results to return per page.
- `offset` query, optional (integer) — The initial index from which to return the results.
- `ordering` query, optional (string) — Field used to order the results. Defaults to user email.
- `search` query, optional (string) — User search by email.

Responses:

- `200` — List of associated users.
- `400` — Bad Request. Validation failed or request data is invalid.
- `401` — Unauthorized. Authentication credentials were not provided or are invalid.
- `403` — Forbidden. You do not have permission to perform this action.
- `404` — Not Found. The requested resource does not exist.
- `405` — Method Not Allowed.

## GET `/cnac/endsystem-service/api/endsystems/v2/clients`

Operation: `clientslist`

Get Client list

List of client device data with optional filtering based on query parameters. Filters include time range (start-time and end-time), authentication type, client state, ZTNA agent status, compliance status, user identity, and keyword-based searches across multiple fields. Pagination and sorting options are supported for efficient data retrieval. The response provides detailed information about the clients, such as their authentication status, compliance, VLAN configuration, and more. This endpoint enables administrators to manage and analyze client's authentication data effectively.

Tags: `Clients`

Parameters:

- `start-time` query, optional (integer) — start-time is epoch time in seconds. It represents the start of the time range (start-time - end-time) in which the auth request was last seen (inclusive). Both start-time and end-time parameters should be provided together.Unix Epoch (Jan…
- `end-time` query, optional (integer) — end-time is epoch time in seconds. It represents the end of the time range (start-time - end-time) in which the auth request was last seen (exclusive). Both start-time and end-time parameters should be provided together.Unix Epoch (Jan…
- `mac-address` query, optional (string) — client's mac address its a search for given mac-address with delimeter.
- `auth-type` query, optional (string) — Authentication Type.
- `state` query, optional (string) — Authentication state of client device
- `ztna-agent-status` query, optional (string) — Status of client agent
- `compliance-status` query, optional (string) — Compliance status of client device
- `user-name` query, optional (string) — User identity with a maximum limit of 194 characters.
- `keyword` query, optional (string) — keyword for case-insensitive search on all the string fields including mac-address, user-name, nas-ip, nas-port-id, auth-type, ssid, ip-address, ipv6-address, es-type, os-name, host-name, state, last-nac-profile, last-nac-rule,…
- `page` query, optional (integer) — next page number for pagination. Default value is 1 (used if set value is not an integer > 0).
- `size` query, optional (integer) — current page size for pagination. Default value is 20 (used if set value is not an integer > 0).
- `sort` query, optional (string) — column on which the sort is required and the sort order (ASC, DESC). Sorting can be applied only one column at a time.

Responses:

- `200` — OK
- `400` — Bad Request
- `401` — Unauthorized
- `403` — Forbidden
- `404` — Not Found
- `405` — Method Not Allowed
- `500` — Internal Server Error

## POST `/cnac/network-policy-engine/api/v1/npe/external/deauth`

Operation: `deauthClient`

Disconnect one or more client sessions

Forcibly disconnects one or more client devices from the network by deauthorizing their active sessions. This endpoint accepts client MAC addresses and optional RADIUS session identifiers to immediately terminate connectivity. It is typically used for logout events, policy changes, or security remediation. Cloud‑onboarded devices are disconnected directly, while clients on third‑party devices are deauthorized via a RADIUS Change of Authorization (CoA) request.

Tags: `Trigger Client Session Deauthorization`

Request body:

- `application/json` — ExternalDeauth

Responses:

- `200` — OK
- `400` — Bad Request
- `401` — Unauthorized
- `403` — Forbidden

