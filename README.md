# Extreme Platform ONE Developer Portal

Snapshot of [developer.extremeplatformone.com](https://developer.extremeplatformone.com/).

Guides are under `pages/guides/`. Each API is a Markdown reference under `pages/api/` plus the original OpenAPI JSON in `specs/`.

The portal hides the Configuration service in the sidebar. It is included here because `/api/spec/configuration` is published.

SDKs and Community pages on the site only say coming soon, so they are not copied.

## Support documentation

Markdown and original PDFs from [Extreme Platform ONE - Latest Documentation](https://supportdocs.extremenetworks.com/support/documentation/extreme-platform-one-latest-documentation/).

| Document | Markdown | PDF |
| --- | --- | --- |
| Aerohive API Migration Reference Guide Jun 2026 | [pages/support/Aerohive_API_Migration_Reference_Guide.md](pages/support/Aerohive_API_Migration_Reference_Guide.md) | [pdfs/Aerohive_API_Migration_Reference_Guide.pdf](pdfs/Aerohive_API_Migration_Reference_Guide.pdf) |
| Extreme Agent ONE Coworker v9.3.0 Release Notes Oct 2026 | [pages/support/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.md](pages/support/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.md) | [pdfs/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.pdf](pdfs/Extreme_Agent_ONE_Coworker_9_3_0_Release_Notes.pdf) |
| Extreme Agent ONE Coworker v9.3.0 User Guide Oct 2026 | [pages/support/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.md](pages/support/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.md) | [pdfs/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.pdf](pdfs/Extreme_Agent_ONE_Coworker_9_3_0_User_Guide.pdf) |
| Extreme Exchange v9.3.0 User Guide Oct 2026 | [pages/support/Extreme_Exchange_9_3_0_User_Guide.md](pages/support/Extreme_Exchange_9_3_0_User_Guide.md) | [pdfs/Extreme_Exchange_9_3_0_User_Guide.pdf](pdfs/Extreme_Exchange_9_3_0_User_Guide.pdf) |
| Extreme Platform ONE Networking v25.14.0-331 (Patch 1) Release Notes Oct 2026 | [pages/support/Extreme_Platform_ONE_Networking_25_14_0_331_Patch_1_Release_Notes.md](pages/support/Extreme_Platform_ONE_Networking_25_14_0_331_Patch_1_Release_Notes.md) | [pdfs/Extreme_Platform_ONE_Networking_25_14_0_331_Patch_1_Release_Notes.pdf](pdfs/Extreme_Platform_ONE_Networking_25_14_0_331_Patch_1_Release_Notes.pdf) |
| Extreme Platform ONE Networking v25.14.0-331 Release Notes Sep 2026 | [pages/support/Extreme_Platform_ONE_Networking_25_14_0_331_Release_Notes.md](pages/support/Extreme_Platform_ONE_Networking_25_14_0_331_Release_Notes.md) | [pdfs/Extreme_Platform_ONE_Networking_25_14_0_331_Release_Notes.pdf](pdfs/Extreme_Platform_ONE_Networking_25_14_0_331_Release_Notes.pdf) |
| Extreme Platform ONE Networking v25.14.0 Universal Switch Deployment Guide Sep 2026 | [pages/support/Extreme_Platform_ONE_Networking_25_14_0_Universal_Switch_Deployment_Guide.md](pages/support/Extreme_Platform_ONE_Networking_25_14_0_Universal_Switch_Deployment_Guide.md) | [pdfs/Extreme_Platform_ONE_Networking_25_14_0_Universal_Switch_Deployment_Guide.pdf](pdfs/Extreme_Platform_ONE_Networking_25_14_0_Universal_Switch_Deployment_Guide.pdf) |
| Extreme Platform ONE Networking v25.14.0 User Guide Sep 2026 | [pages/support/Extreme_Platform_ONE_Networking_25_14_0_User_Guide.md](pages/support/Extreme_Platform_ONE_Networking_25_14_0_User_Guide.md) | [pdfs/Extreme_Platform_ONE_Networking_25_14_0_User_Guide.pdf](pdfs/Extreme_Platform_ONE_Networking_25_14_0_User_Guide.pdf) |
| Extreme Platform ONE Networking and ExtremeCloud IQ v25.14.0 Licensing Guide Sep 2026 | [pages/support/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.md](pages/support/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.md) | [pdfs/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.pdf](pdfs/Extreme_Platform_ONE_Networking_and_ExtremeCloud_IQ_25_14_0_Subscription_Licensing_Guide.pdf) |

## Guides

- [guides/best-practices/error-handling.md](guides/best-practices/error-handling.md)
- [guides/best-practices/security.md](guides/best-practices/security.md)
- [guides/get-started/authentication.md](guides/get-started/authentication.md)
- [guides/get-started/pagination.md](guides/get-started/pagination.md)
- [guides/get-started/quickstart.md](guides/get-started/quickstart.md)
- [guides/get-started/rate-limiting.md](guides/get-started/rate-limiting.md)
- [guides/get-started/status-code.md](guides/get-started/status-code.md)
- [guides/get-started/trace-id.md](guides/get-started/trace-id.md)
- [guides/overview/introduction.md](guides/overview/introduction.md)

## APIs

| Group | Service | Operations | Doc | Spec |
| --- | --- | ---: | --- | --- |
| Applications | MSP | 13 | [pages/api/msp.md](pages/api/msp.md) | [specs/msp.json](specs/msp.json) |
| Applications | SDWAN | 295 | [pages/api/sdwan.md](pages/api/sdwan.md) | [specs/sdwan.json](specs/sdwan.json) |
| Applications | Security | 15 | [pages/api/uztna.md](pages/api/uztna.md) | [specs/uztna.json](specs/uztna.json) |
| Applications | XIQ | 693 | [pages/api/xiq.md](pages/api/xiq.md) | [specs/xiq.json](specs/xiq.json) |
| Services | Alert | 28 | [pages/api/alert.md](pages/api/alert.md) | [specs/alert.json](specs/alert.json) |
| Services | Asset | 23 | [pages/api/asset.md](pages/api/asset.md) | [specs/asset.json](specs/asset.json) |
| Services | Audit Log | 7 | [pages/api/auditlog.md](pages/api/auditlog.md) | [specs/auditlog.json](specs/auditlog.json) |
| Services | Client | 15 | [pages/api/pcs.md](pages/api/pcs.md) | [specs/pcs.json](specs/pcs.json) |
| Services | Config State | 1803 | [pages/api/ccs.md](pages/api/ccs.md) | [specs/ccs.json](specs/ccs.json) |
| Services | Configuration | 87 | [pages/api/configuration.md](pages/api/configuration.md) | [specs/configuration.json](specs/configuration.json) |
| Services | Device Lifecycle | 56 | [pages/api/dlcs.md](pages/api/dlcs.md) | [specs/dlcs.json](specs/dlcs.json) |
| Services | IAM | 143 | [pages/api/iam.md](pages/api/iam.md) | [specs/iam.json](specs/iam.json) |
| Services | MetaStore | 12 | [pages/api/metastore.md](pages/api/metastore.md) | [specs/metastore.json](specs/metastore.json) |
| Services | Notification | 39 | [pages/api/notification.md](pages/api/notification.md) | [specs/notification.json](specs/notification.json) |
| Services | Performance | 37 | [pages/api/cpms.md](pages/api/cpms.md) | [specs/cpms.json](specs/cpms.json) |
| Services | Performance Monitoring | 19 | [pages/api/pm.md](pages/api/pm.md) | [specs/pm.json](specs/pm.json) |
| Services | Site | 36 | [pages/api/site.md](pages/api/site.md) | [specs/site.json](specs/site.json) |
| Services | Subscription | 20 | [pages/api/subscription.md](pages/api/subscription.md) | [specs/subscription.json](specs/subscription.json) |
| Services | Tagging | 38 | [pages/api/tagging.md](pages/api/tagging.md) | [specs/tagging.json](specs/tagging.json) |
| Services | Visualization | 40 | [pages/api/nvo.md](pages/api/nvo.md) | [specs/nvo.json](specs/nvo.json) |
