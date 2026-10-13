---
source: https://developer.extremeplatformone.com/api-reference/auditlog
spec: https://developer.extremeplatformone.com/api/spec/auditlog
title: "Extreme Platform ONE REST API - Audit Log"
---

# Extreme Platform ONE REST API - Audit Log

**Audit Log** · Services. User Activities.

Extreme Platform ONE™ Audit Log API provides comprehensive tracking of user activities within Extreme Platform ONE, ensuring transparency, traceability, and accountability across all applications.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/auditlog/v1` — Extreme Platform ONE REST API - Audit Log

Full OpenAPI document: [`specs/auditlog.json`](../../specs/auditlog.json)

## Endpoints

7 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/user-activities` | Search user activity audit logs |
| POST | `/user-activities/search` | Search user activity audit logs by request body |
| GET | `/user-activities/export` | Export user activity audit logs |
| GET | `/my-activities` | Search my activity audit logs |
| GET | `/user-apps` | List supported applications |
| GET | `/categories` | List supported categories |
| GET | `/user-operations` | List supported user operations |

## GET `/user-activities`

Operation: `searchUserActivities`

Search user activity audit logs

Search user activity audit logs based on the query parameters.

Tags: `User Activity Audit Logs`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `operationNames` query, optional (array) — Filter by specific operation names to retrieve only audit logs matching these operations
- `categories` query, optional (array) — Filter by audit log categories to narrow results to specific operational domains
- `sortField` query, optional (string) — The field name to sort results by
- `customerIds` query, optional (string) — Filter by specific customer IDs to retrieve audit logs associated with MSP. Ignored for non-MSP callers. Use a comma-separated string in query, for example customerIds=1001,1002.
- `None` , optional

Responses:

- `200` — User activity audit logs retrieved successfully
- `400`
- `401`
- `403`
- `500`

## POST `/user-activities/search`

Operation: `searchUserActivitiesByBody`

Search user activity audit logs by request body

Search user activity audit logs based on the request body parameters.

Tags: `User Activity Audit Logs`

Request body:

- `application/json` — UserActivitySearchRequest

Responses:

- `200` — User activity audit logs retrieved successfully
- `400`
- `401`
- `403`
- `500`

## GET `/user-activities/export`

Operation: `exportUserActivities`

Export user activity audit logs

Export user activity audit logs based on the query parameters.

Tags: `User Activity Audit Logs`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `fields` query, optional (array) — Specify which fields to include in the exported CSV file
- `operationNames` query, optional (array) — Filter by specific operation names to retrieve only audit logs matching these operations
- `categories` query, optional (array) — Filter by audit log categories to narrow results to specific operational domains
- `sortField` query, optional (string) — The field name to sort results by
- `None` , optional

Responses:

- `200` — User activity audit logs exported successfully
- `400`
- `401`
- `403`
- `500`

## GET `/my-activities`

Operation: `searchMyActivities`

Search my activity audit logs

Search my activity audit logs based on the query parameters.

Tags: `User Activity Audit Logs`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `operationNames` query, optional (array) — Filter by specific operation names to retrieve only audit logs matching these operations
- `categories` query, optional (array) — Filter by audit log categories to narrow results to specific operational domains
- `sortField` query, optional (string) — The field name to sort results by
- `None` , optional

Responses:

- `200` — My activity audit logs retrieved successfully
- `400`
- `401`
- `403`
- `500`

## GET `/user-apps`

Operation: `listUserApps`

List supported applications

List supported applications that generate audit logs.

Tags: `Audit Log Metadata`

Responses:

- `200` — Supported applications list retrieved successfully
- `400`
- `401`
- `403`
- `500`

## GET `/categories`

Operation: `listCategories`

List supported categories

List supported categories.

Tags: `Audit Log Metadata`

Responses:

- `200` — Supported categories list retrieved successfully
- `400`
- `401`
- `403`
- `500`

## GET `/user-operations`

Operation: `listUserOperations`

List supported user operations

List supported user operations.

Tags: `Audit Log Metadata`

Responses:

- `200` — Supported user operations list retrieved successfully
- `400`
- `401`
- `403`
- `500`

