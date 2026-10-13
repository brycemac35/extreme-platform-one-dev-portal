---
source: https://developer.extremeplatformone.com/api-reference/site
spec: https://developer.extremeplatformone.com/api/spec/site
title: "Extreme Platform ONE REST API - Site"
---

# Extreme Platform ONE REST API - Site

**Site** · Services. Site, Building and Floor.

Extreme Platform ONE™ Site API allows users to access and manage Site/Location information, such as Sites, Site Groups, Buildings, Floors, etc.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/site/v1` — Extreme Platform ONE REST API - Site

Full OpenAPI document: [`specs/site.json`](../../specs/site.json)

## Endpoints

36 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/sites` | List sites |
| POST | `/sites` | Create site |
| GET | `/sites/{id}` | Get site by ID |
| PUT | `/sites/{id}` | Update site by ID |
| DELETE | `/sites/{id}` | Delete site by ID |
| GET | `/site-groups` | List site groups |
| POST | `/site-groups` | Create site group |
| GET | `/site-groups/{id}` | Get site group by ID |
| PUT | `/site-groups/{id}` | Update site group by ID |
| DELETE | `/site-groups/{id}` | Delete site group by ID |
| GET | `/buildings` | List buildings |
| POST | `/buildings` | Create building |
| DELETE | `/buildings` | Delete multiple buildings |
| GET | `/buildings/{id}` | Get a building by ID |
| PUT | `/buildings/{id}` | Update building |
| DELETE | `/buildings/{id}` | Delete building by ID |
| GET | `/floors` | List floors |
| POST | `/floors` | Create floor |
| DELETE | `/floors` | Delete multiple floors |
| GET | `/floors/{id}` | Get a floor by ID |
| PUT | `/floors/{id}` | Update floor |
| DELETE | `/floors/{id}` | Delete floor by ID |
| GET | `/floors/floorplan` | List floorplan images |
| POST | `/floors/floorplan` | Upload floorplan |
| DELETE | `/floors/floorplan` | Delete floorplan images by ID |
| POST | `/floors/floorplan/{id}/:crop` | Crop floorplan image |
| GET | `/tree` | Get site tree |
| GET | `/tree/devices` | Get devices on the site hierarchy |
| GET | `/tree/maps` | Get maps on the site hierarchy |
| POST | `/tree/:import` | Import site tree |
| POST | `/tree/:export` | Export site tree |
| POST | `/location/{id}:clone` | Clone a location |
| POST | `/location/{id}:move` | Move a location |
| PUT | `/location/{id}:reorder` | Reorder floor |
| GET | `/status` | Returns tasks status |
| GET | `/count` | Returns Count of each folderType |

## GET `/sites`

Operation: `getSites`

List sites

List pages of sites by filter.

Tags: `Site`

Parameters:

- `None` , optional
- `None` , optional
- `order` query, optional (SortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — List sites by name (case insensitive)
- `ids` query, optional (array) — List sites by IDs

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/sites`

Operation: `createSite`

Create site

Create a new site under a site group or the root location.

Tags: `Site`

Request body:

- `application/json` — ClsCreateSiteRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/sites/{id}`

Operation: `getSite`

Get site by ID

Get the site for the specified ID.

Tags: `Site`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/sites/{id}`

Operation: `updateSite`

Update site by ID

Update the site information with the site ID.

Tags: `Site`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsUpdateSiteRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/sites/{id}`

Operation: `deleteSite`

Delete site by ID

Delete the site for the specified ID.

Tags: `Site`

Parameters:

- `id` path, required (integer) — The unique identifier of the site to be deleted.
- `force_delete` query, optional (boolean) — When true, forcefully deletes the site and all its descendant sites recursively. When false, deletion will fail if the site has dependencies.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/site-groups`

Operation: `getSiteGroups`

List site groups

List pages of site groups by filter.

Tags: `Site Group`

Parameters:

- `None` , optional
- `None` , optional
- `order` query, optional (SortOrder) — The sort order for site group name (ASC for ascending, DESC for descending; ascending by default)
- `name` query, optional (string) — List site groups by name (case insensitive)
- `ids` query, optional (array) — List site groups by IDs

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/site-groups`

Operation: `createSiteGroup`

Create site group

Create a new site group.

Tags: `Site Group`

Request body:

- `application/json` — ClsCreateSiteGroupRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/site-groups/{id}`

Operation: `getSiteGroup`

Get site group by ID

Get the site group for the specified ID.

Tags: `Site Group`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/site-groups/{id}`

Operation: `updateSiteGroup`

Update site group by ID

Update the site group information with the site group ID.

Tags: `Site Group`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsUpdateSiteGroupRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/site-groups/{id}`

Operation: `deleteSiteGroup`

Delete site group by ID

Delete the site group for the specified ID.

Tags: `Site Group`

Parameters:

- `id` path, required (integer) — The unique identifier of the site group to be deleted.
- `force_delete` query, optional (boolean) — When true, forcefully deletes the site group along with all its child site groups and associated resources (sites, buildings, floors) recursively. When false, deletion will fail if the site group has any dependencies.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/buildings`

Operation: `getBuildings`

List buildings

List pages of buildings by filter.

Tags: `Building`

Parameters:

- `None` , optional
- `None` , optional
- `order` query, optional (SortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — List buildings by name (case insensitive)
- `ids` query, optional (array) — List buildings by IDs

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/buildings`

Operation: `createBuilding`

Create building

Create a new building under the parent location.

Tags: `Building`

Request body:

- `application/json` — ClsCreateBuildingRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/buildings`

Operation: `deleteBuildings`

Delete multiple buildings

Delete buildings under the parent location.

Tags: `Building`

Parameters:

- `ids` query, required (array) — List of building IDs to delete.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/buildings/{id}`

Operation: `getBuilding`

Get a building by ID

Get the building for the specified ID.

Tags: `Building`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/buildings/{id}`

Operation: `updateBuilding`

Update building

Update the building information with the building ID.

Tags: `Building`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsUpdateBuildingRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/buildings/{id}`

Operation: `deleteBuilding`

Delete building by ID

Delete the building for the specified ID.

Tags: `Building`

Parameters:

- `id` path, required (integer) — The unique identifier of the building to be deleted.
- `force_delete` query, optional (boolean) — Force deletion of this building and all associated floors, rooms, and devices recursively

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/floors`

Operation: `getFloors`

List floors

List pages of floors by filter.

Tags: `Floor`

Parameters:

- `None` , optional
- `None` , optional
- `order` query, optional (SortOrder) — The sort order by name (ascending by default)
- `name` query, optional (string) — Filter floors by name (case insensitive).
- `ids` query, optional (array) — List floors by IDs

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/floors`

Operation: `createFloor`

Create floor

Create a new floor under the parent building.

Tags: `Floor`

Request body:

- `application/json` — ClsCreateFloorRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/floors`

Operation: `deleteFloors`

Delete multiple floors

Delete multiple floors under the parent building.

Tags: `Floor`

Parameters:

- `ids` query, required (array) — List of floor IDs to delete

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/floors/{id}`

Operation: `getFloor`

Get a floor by ID

Get the floor for the specified ID.

Tags: `Floor`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/floors/{id}`

Operation: `updateFloor`

Update floor

Update floor information with the floor ID.

Tags: `Floor`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsUpdateFloorRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/floors/{id}`

Operation: `deleteFloor`

Delete floor by ID

Delete the floor for the specified ID.

Tags: `Floor`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/floors/floorplan`

Operation: `getFloorplans`

List floorplan images

List pages of available floorplan images.

Tags: `Floor`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/floors/floorplan`

Operation: `uploadFloorplan`

Upload floorplan

Upload the floorplan map for the VIQ.

Tags: `Floor`

Parameters:

- `overrideBg` query, optional (boolean) — A flag indicating whether to override the existing floor plan image. Set to `true` to override, `false` to retain the existing image.

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/floors/floorplan`

Operation: `deleteFloorPlan`

Delete floorplan images by ID

Delete the floorplan images for the VIQ.

Tags: `Floor`

Parameters:

- `ids` query, required (array) — The IDs of the floorplan images to be deleted

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/floors/floorplan/{id}/:crop`

Operation: `cropImage`

Crop floorplan image

Crop floorplan image.

Tags: `Floor`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsImageCropRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/tree`

Operation: `getLocationTree`

Get site tree

Get site hierarchical tree.

Tags: `Tree`

Parameters:

- `parentId` query, optional (integer) — The parent location ID, return root locations if parent is null
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/tree/devices`

Operation: `getLocationDevicesList`

Get devices on the site hierarchy

Get devices on the site hierarchy with pagination.

Tags: `Tree`

Parameters:

- `None` , optional
- `None` , optional
- `locationId` query, optional (integer) — The location ID, or null for all locations.
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/tree/maps`

Operation: `getLocationMapsList`

Get maps on the site hierarchy

Get maps on the site hierarchy with pagination.

Tags: `Tree`

Parameters:

- `None` , optional
- `None` , optional
- `locationId` query, optional (integer) — The location ID, or null for all locations.
- `expandChildren` query, optional (boolean) — Whether to return the child locations recursively, default is true. Set it to false to improve performance when there are a lot of child locations.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/tree/:import`

Operation: `importTree`

Import site tree

Import sites groups and sites tree.

Tags: `Tree`

Parameters:

- `override` query, optional (boolean) — A flag indicating whether to override the existing floor plan image during import operation. Set to true to override the existing image, false to retain the existing image.
- `id` query, optional (integer) — id field corresponds to the folderId under which the XML file will be imported. The folderId can be obtained from the GET /tree API. Depending on the type of XML being imported, the folderId should be as follows: If folderId is not…

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/tree/:export`

Operation: `exportTree`

Export site tree

export sites groups and sites tree.

Tags: `Tree`

Request body:

- `application/json` — ClsExportTreeRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/location/{id}:clone`

Operation: `cloneLocation`

Clone a location

Clones a particular location, applicable to only buildings and floors.

Tags: `Location Management`

Parameters:

- `None` , optional

Request body:

- `application/json` — ClsCloneLocationRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/location/{id}:move`

Operation: `moveLocation`

Move a location

Move a site or site-group to a new parent location.

Tags: `Location Management`

Parameters:

- `id` path, required (integer) — The unique identifier of the site or site-group to be moved.

Request body:

- `application/json` — ClsMoveLocationRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/location/{id}:reorder`

Operation: `reorderFloor`

Reorder floor

Reorders floor up or down.

Tags: `Location Management`

Parameters:

- `id` path, required (integer) — The unique identifier of the floor to be reordered.

Request body:

- `application/json` — ClsReorderLocationRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/status`

Operation: `getStatus`

Returns tasks status

Returns tasks status.

Tags: `Miscellaneous`

Parameters:

- `taskId` query, required (string) — The unique task identifier returned by an asynchronous operation (e.g., importTree). The value is a string (e.g., 'WipTask-importFolderToRoot-d0aad673-293f-412c-8768-d92612908196').

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/count`

Operation: `getCount`

Returns Count of each folderType

Returns counts of each folderType.

Tags: `Miscellaneous`

Parameters:

- `folderType` query, optional (FolderType) — Filter to return count for a specific folder type. If omitted, returns counts for all folder types.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

