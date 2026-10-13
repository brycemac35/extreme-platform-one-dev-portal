---
source: https://developer.extremeplatformone.com/content/guides/get-started/pagination.md
---

---
title: "Pagination"
---

When working with large datasets, pagination is essential for performance and usability. This guide covers pagination strategies and best practices.

## Why Pagination Matters

Pagination provides several benefits:

- **Performance**: Reduces response size and server load
- **Memory**: Prevents overwhelming client applications
- **Usability**: Faster response times improve user experience
- **Rate Limits**: Spreads requests over time

## Pagination Types

### Offset-Based Pagination

#### Query Parameters

| Parameter | Description                              | Example     |
|-----------|------------------------------------------|-------------|
| `page`    | Page number (1-indexed)                  | `?page=2`   |
| `limit`   | Page size, i.e. items per page (max 100) | `?limit=50` |

#### Response

The paginated responses follow this structure:

| Field         | Description                         |
|---------------|-------------------------------------|
| `page`        | The current page number (1-indexed) |
| `count`       | The current page record count       |
| `total_pages` | Total page number                   |
| `total_count` | Total record count                  |
| `data`        | The current page records            |

### Cursor-Based Pagination

For large or frequently changing datasets, cursor-based pagination is more reliable.
Cursor-based pagination is used on audit log API.

#### Query Parameters

| Parameter   | Description                                                                      | Example               |
|-------------|----------------------------------------------------------------------------------|-----------------------|
| `pageToken` | An opaque, unique string that acts as a pointer to a specific item in a dataset. | `?pageToken=sd3423ds` |
| `limit`     | The max record count to fetch after pageToken, i.e. page size (max 100)          | `?limit=50`           |

#### Response

The cursor-based pagination responses follow this structure:

| Field           | Description                     |
|-----------------|---------------------------------|
| `nextPageToken` | The pageToken for the next page |
| `count`         | The current page record count   |
| `data`          | The current page records        |

## Pagination Best Practices

- ✅ Use appropriate page sizes (50-100 items)
- ✅ Respect rate limits between page requests
- ✅ Handle pagination metadata correctly
- ✅ Use cursor-based pagination for real-time data
- ✅ Cache pages when appropriate
- ✅ Show progress for long operations
- ✅ Handle errors gracefully for partial results

## Next Steps

- [Rate Limiting](/guides/rate-limiting) - Manage API rate limits
- [Error Handling](/guides/error-handling) - Handle pagination errors
- [HTTP Status Codes](/guides/status-code) - Understand API response codes
