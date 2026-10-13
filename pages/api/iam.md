---
source: https://developer.extremeplatformone.com/api-reference/iam
spec: https://developer.extremeplatformone.com/api/spec/iam
title: "Extreme Platform ONE REST API - IAM"
---

# Extreme Platform ONE REST API - IAM

**IAM** · Services. Identity and Access Management.

Extreme Platform ONE™ IAM (Identity and Access Management) API allows users to manage organization setting, user profile, identities, roles, external Identity Providers (IDPs), Multi-Factor Authentication (MFA), API Keys, etc.

Version: `25.14.0`

## Servers

- `https://cloudapi.extremecloudiq.com/iam/v1` — Extreme Platform ONE REST API - IAM (Identity and Access Management)

Full OpenAPI document: [`specs/iam.json`](../../specs/iam.json)

## Endpoints

143 operations.

| Method | Path | Summary |
| --- | --- | --- |
| GET | `/myaccount` | Get my account information |
| PUT | `/myaccount` | Update my account information |
| PATCH | `/myaccount` | Patch update my account information |
| PUT | `/myaccount/password` | Change password |
| GET | `/myaccount/avatar` | Get my account avatar |
| PUT | `/myaccount/avatar` | Update my account avatar |
| DELETE | `/myaccount/avatar` | Delete my account avatar |
| GET | `/myaccount/app-catalog` | Get the list of applications |
| POST | `/myaccount/:verify-phone` | Verify phone by code |
| POST | `/myaccount/:send-verify-code` | Send phone verify code |
| GET | `/myaccount/permissions` | Get my permissions |
| POST | `/myaccount/:send-reset-password-email` | Send email for reset password |
| GET | `/myaccount/organizations` | Get accessible organizations |
| POST | `/myaccount/organizations/{id}/:switch` | Switch organization |
| PUT | `/myaccount/organizations/{id}/alias` | Update alias of organization |
| PUT | `/myaccount/organizations/{id}/favorite` | Update favorite of organization |
| PUT | `/myaccount/organizations/{id}/hidden` | Update hidden of organization |
| POST | `/myaccount/:accept_terms` | Accept terms & conditions |
| GET | `/myaccount/log-types` | Get the list of log types |
| GET | `/myorganization/security/mfa` | Get MFA enabled status for organization |
| POST | `/myorganization/security/mfa/:disable` | Disable MFA for organization |
| POST | `/myorganization/security/mfa/:enable` | Enable MFA for organization |
| GET | `/myorganization/setting` | Get the setting for organization |
| PATCH | `/myorganization/setting` | Update the setting for organization |
| GET | `/security/mfa` | Get MFA authenticators |
| POST | `/security/mfa/authenticator/app/:disable` | Disable "APP" authenticator |
| POST | `/security/mfa/authenticator/app/:enable` | Enable "APP" authenticator |
| POST | `/security/mfa/authenticator/app/:set-default` | Set "APP" to default authenticator type |
| GET | `/security/mfa/authenticator/app/secret/qr` | Get QR image for "APP" authenticator |
| GET | `/security/mfa/authenticator/app/secret` | Get secret code and QR URL for "APP" authenticator |
| POST | `/security/mfa/authenticator/email/:disable` | Disable "EMAIL" authenticator |
| POST | `/security/mfa/authenticator/email/:enable` | Enable "EMAIL" authenticator |
| POST | `/security/mfa/authenticator/email/:set-default` | Set "EMAIL" to default authenticator type |
| POST | `/security/mfa/authenticator/email/otp` | Send OTP to email |
| POST | `/security/password/:validate` | Validate user password |
| GET | `/saml2/asserting-parties` | List external IdPs |
| POST | `/saml2/asserting-parties` | Create new external IdP |
| GET | `/saml2/asserting-parties/{id}` | Get external IdP |
| PATCH | `/saml2/asserting-parties/{id}` | Update external IdP |
| DELETE | `/saml2/asserting-parties/{id}` | Delete external IdP |
| PUT | `/saml2/asserting-parties/{id}/enabled` | Update enabled of external IdP |
| POST | `/saml2/asserting-parties/domain/:validate` | Validate Domain |
| POST | `/saml2/asserting-parties/metadata/:import-from-file` | Import external IdP from file |
| POST | `/saml2/asserting-parties/metadata/:import-from-uri` | Import external IdP from URI |
| GET | `/saml2/asserting-parties/types` | List asserting party types |
| GET | `/saml2/asserting-parties/types/{type}/attribute-mapping-template` | Get attribute mapping template |
| POST | `/saml2/asserting-parties/certificates` | Upload certificate for creating external IdP |
| GET | `/saml2/asserting-parties/{id}/certificates` | List certificates of external IdP |
| POST | `/saml2/asserting-parties/{id}/certificates` | Upload certificate of external IdP |
| DELETE | `/saml2/asserting-parties/certificates/{id}` | Delete certificate of external IdP |
| PUT | `/saml2/asserting-parties/certificates/{id}/active` | Update active of external IdP certificate |
| GET | `/saml2/service-provider/{registrationId}` | Get service provider detail |
| GET | `/saml2/service-provider/{registrationId}/metadata` | Download metadata |
| GET | `/saml2/service-provider/certificate` | Download certificate |
| GET | `/app-types` | List application types |
| GET | `/apps` | List applications |
| GET | `/apps/{id}/avatar` | Get app avatar |
| GET | `/apps/cloud-app` | List cloud applications |
| GET | `/apps/cloud-service` | List cloud services |
| GET | `/apps/xcd-app` | List XCD applications |
| GET | `/default-app` | Get default application |
| PUT | `/default-app` | Set default application |
| POST | `/default-app/:reset` | Reset default application |
| GET | `/users` | Get page of users |
| POST | `/users` | Create new user |
| DELETE | `/users` | Delete users |
| GET | `/users/{id}` | Get user detail |
| PUT | `/users/{id}` | Update user detail |
| PATCH | `/users/{id}` | Patch update user detail and permission |
| POST | `/users/{id}/:add-groups` | Add a user to user groups |
| POST | `/users/{id}/:remove-groups` | Remove a user from user groups |
| POST | `/users/{id}/:add-roles` | Grant new roles to the user |
| POST | `/users/{id}/:remove-roles` | Remove roles from user |
| GET | `/users/{id}/avatar` | Get user avatar |
| PUT | `/users/{id}/avatar` | Update user avatar |
| GET | `/users/{id}/groups` | Get user groups for user |
| PUT | `/users/{id}/groups` | Replace the user assigned user groups |
| GET | `/users/{id}/roles` | Get roles for user |
| PUT | `/users/{id}/roles` | Replace roles for the user |
| GET | `/users/{id}/permissions` | Get user permissions |
| POST | `/users/{id}/:resend-email` | Resend user initialized email |
| POST | `/users/:enable` | Enable user account |
| POST | `/users/:disable` | Disable user account |
| POST | `/users/:check-email-exist` | Check existing email |
| POST | `/users/:check-email-existence` | Check if email exists and find user ID |
| POST | `/users/:check-email-vadlidity` | Check email vadlidity |
| GET | `/external-users` | List external users |
| POST | `/external-users` | Create new external user |
| DELETE | `/external-users` | Delete external users |
| GET | `/external-users/{id}` | Get external user detail |
| PATCH | `/external-users/{id}` | Patch Update external users |
| POST | `/external-users/{id}/:add-groups` | Add groups to the external user |
| POST | `/external-users/{id}/:remove-groups` | Remove groups from external user |
| POST | `/external-users/{id}/:add-roles` | Grant new roles to the external user |
| POST | `/external-users/{id}/:remove-roles` | Remove roles from external user |
| GET | `/external-users/{id}/groups` | Get user groups for external user |
| PUT | `/external-users/{id}/groups` | Replace the external user assigned user groups |
| GET | `/external-users/{id}/roles` | Get roles for external user |
| PUT | `/external-users/{id}/roles` | Replace roles for the external user |
| GET | `/external-users/{id}/permissions` | Get external user permissions |
| GET | `/external-users/{id}/avatar` | Get external user avatar |
| POST | `/external-users/:check-availability` | Check users who can be added as external users |
| GET | `/user-groups` | List user groups |
| POST | `/user-groups` | Create new user group |
| GET | `/user-groups/{id}` | Get user group detail |
| PUT | `/user-groups/{id}` | Update user group |
| DELETE | `/user-groups/{id}` | Delete user group |
| POST | `/user-groups/{id}/:add-users` | Add users to user group |
| POST | `/user-groups/{id}/:remove-users` | Remove users from the user group |
| POST | `/user-groups/{id}/:grant-roles` | Grant roles to user group |
| POST | `/user-groups/{id}/:remove-roles` | Remove roles from user group |
| GET | `/user-groups/{id}/users` | Get users for user group |
| PUT | `/user-groups/{id}/users` | Replace users in the user group |
| GET | `/user-groups/{id}/roles` | Get roles for user group |
| PUT | `/user-groups/{id}/roles` | Replace the roles assigned to the user group |
| GET | `/user-groups/{id}/permissions` | Get user group permissions |
| GET | `/user-groups/{id}/avatar` | Get user group avatar |
| GET | `/roles` | List roles |
| POST | `/roles` | Create a new role |
| GET | `/roles/names` | Get list of role names |
| GET | `/roles/{id}` | Get role by ID |
| PUT | `/roles/{id}` | Update the role |
| DELETE | `/roles/{id}` | Delete the role |
| POST | `/roles/{id}/:add-permissions` | Add permissions to the role |
| POST | `/roles/{id}/:remove-permissions` | Remove permissions from a role |
| GET | `/roles/{id}/permissions` | Get permissions associated with a role |
| PUT | `/roles/{id}/permissions` | Replace permissions for the role |
| GET | `/api-keys/{id}` | Get an API key |
| PATCH | `/api-keys/{id}` | Update an existing API key |
| DELETE | `/api-keys/{id}` | Delete an API key |
| POST | `/api-keys/{id}/:enable` | Enable an API key |
| POST | `/api-keys/{id}/:disable` | Disable an API key |
| GET | `/api-keys` | Fetch all API keys |
| POST | `/api-keys` | Create a new API key |
| GET | `/myaccount/api-keys` | Fetch my API keys |
| GET | `/redirect` | Execute redirects |
| GET | `/data-centers` | List data centers |
| GET | `/customers` | List customers |
| POST | `/customers` | Create new customer |
| GET | `/customers/{id}` | Get customer |
| GET | `/msp-setting` | Get MSP setting |
| POST | `/customers/features/ai-data-use/:enable` | Enable AI Data Use for Customers |
| POST | `/customers/features/ai-data-use/:disable` | Disable AI Data Use for Customers |

## GET `/myaccount`

Operation: `getMyAccount`

Get my account information

Get my account information.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount`

Operation: `updateMyAccount`

Update my account information

Update my account information.

Tags: `My Account`

Request body:

- `application/json` — IamUpdateMyaccountRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/myaccount`

Operation: `patchUpdateMyaccountInfo`

Patch update my account information

Patch update my account information.

Tags: `My Account`

Request body:

- `application/json` — IamPatchUpdateMyaccountRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount/password`

Operation: `changePasswordByOldPassword`

Change password

Change password by providing old password.

Tags: `My Account`

Request body:

- `application/json` — IamChangePasswordRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/avatar`

Operation: `getAvatar`

Get my account avatar

Get my account picture.

Tags: `My Account`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount/avatar`

Operation: `uploadAvatar`

Update my account avatar

Update my account picture.

Tags: `My Account`

Request body:

- `multipart/form-data` — image

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/myaccount/avatar`

Operation: `deleteAvatar`

Delete my account avatar

Delete my account picture.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/app-catalog`

Operation: `getAppCatalog`

Get the list of applications

Get the list of applications authorized for the current user.

Tags: `My Account`

Parameters:

- `viewName` query, optional (string) — The name of the view used in various applications, if not specified, EP1_NETWORKING_VIEW is used by default.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myaccount/:verify-phone`

Operation: `verifyPhone`

Verify phone by code

Verify phone by code.

Tags: `My Account`

Request body:

- `application/json` — IamVerifyPhoneRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myaccount/:send-verify-code`

Operation: `sendVerifyCode`

Send phone verify code

Send phone verify code.

Tags: `My Account`

Parameters:

- `requestId` query, optional (string) — requestId

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/permissions`

Operation: `permissions`

Get my permissions

Get permissions for the current login user.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myaccount/:send-reset-password-email`

Operation: `sendEmailForResetPassword`

Send email for reset password

Send email for reset password.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/organizations`

Operation: `listOrganizations`

Get accessible organizations

Get all accessible organizations.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myaccount/organizations/{id}/:switch`

Operation: `switchOrganization`

Switch organization

Switch organization to the specified ID.

Tags: `My Account`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `302` — Redirects to the organization SAML authentication URL.
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount/organizations/{id}/alias`

Operation: `updateOrganizationAlias`

Update alias of organization

Update alias of organization for a specific ID, currently only support EXTERNAL organization.

Tags: `My Account`

Parameters:

- `None` , optional
- `type` query, optional (string) — Type of organization, internal or external

Request body:

- `application/json` — alias

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount/organizations/{id}/favorite`

Operation: `updateOrganizationFavorite`

Update favorite of organization

Update favorite of organization for a specific ID, currently only support EXTERNAL organization.

Tags: `My Account`

Parameters:

- `None` , optional
- `type` query, optional (string) — Type of organization internal or external

Request body:

- `application/json` — favorite

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/myaccount/organizations/{id}/hidden`

Operation: `updateOrganizationHidden`

Update hidden of organization

Update hidden of organization for a specific ID, currently only support EXTERNAL organization.

Tags: `My Account`

Parameters:

- `None` , optional
- `type` query, optional (string) — Type of organization internal or external

Request body:

- `application/json` — hidden

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myaccount/:accept_terms`

Operation: `acceptTerms`

Accept terms & conditions

Accept terms & conditions.

Tags: `My Account`

Request body:

- `application/json` — IamAcceptTermsRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/log-types`

Operation: `listLogTypes`

Get the list of log types

Get the list of log types authorized for the current user.

Tags: `My Account`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myorganization/security/mfa`

Operation: `getMyOrganizationMfa`

Get MFA enabled status for organization

Get MFA enabled status for organization.

Tags: `My Organization`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myorganization/security/mfa/:disable`

Operation: `disableMyOrganizationMfa`

Disable MFA for organization

Disable MFA for organization.

Tags: `My Organization`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/myorganization/security/mfa/:enable`

Operation: `enableMyOrganizationMfa`

Enable MFA for organization

Enable MFA for organization.

Tags: `My Organization`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/myorganization/setting`

Operation: `getMyOrganizationSetting`

Get the setting for organization

Get setting for organization.

Tags: `My Organization`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/myorganization/setting`

Operation: `patchMyOrganizationSetting`

Update the setting for organization

Update the setting for organization.

Tags: `My Organization`

Request body:

- `application/json` — IamMyOrganizationPatchSetting

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/security/mfa`

Operation: `authenticators`

Get MFA authenticators

Get MFA authenticators.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/app/:disable`

Operation: `disableAppAuthenticator`

Disable "APP" authenticator

Disable "APP" authenticator.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/app/:enable`

Operation: `enableAppAuthenticator`

Enable "APP" authenticator

Enable "APP" authenticator.

Tags: `Security`

Request body:

- `application/json` — IamMfaEnableAppRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/app/:set-default`

Operation: `setAppDefault`

Set "APP" to default authenticator type

Set "APP" to default authenticator type.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/security/mfa/authenticator/app/secret/qr`

Operation: `getQrImage`

Get QR image for "APP" authenticator

Get QR image for "APP" authenticator.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/security/mfa/authenticator/app/secret`

Operation: `appSecret`

Get secret code and QR URL for "APP" authenticator

Get secret code and QR URL for "APP" authenticator.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/email/:disable`

Operation: `disableEmailAuthenticator`

Disable "EMAIL" authenticator

Disable "EMAIL" authenticator.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/email/:enable`

Operation: `enableEmailAuthenticator`

Enable "EMAIL" authenticator

Enable "EMAIL" authenticator.

Tags: `Security`

Request body:

- `application/json` — IamMfaEnableEmailRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/email/:set-default`

Operation: `setEmailDefault`

Set "EMAIL" to default authenticator type

Set "EMAIL" to default authenticator type.

Tags: `Security`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/mfa/authenticator/email/otp`

Operation: `sendEmailOtp`

Send OTP to email

Send OTP to email.

Tags: `Security`

Parameters:

- `email` query, required (string) — Email address

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/security/password/:validate`

Operation: `validateUserPassword`

Validate user password

Validate user password.

Tags: `Security`

Request body:

- `application/json` — IamValidateUserPasswordRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/asserting-parties`

Operation: `listAssertingParties`

List external IdPs

List external IdP configurations.

Tags: `SAML`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties`

Operation: `createAssertingParty`

Create new external IdP

Create a new external IdP configuration.

Tags: `SAML`

Request body:

- `application/json` — IamCreateSaml2AssertingPartyRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/asserting-parties/{id}`

Operation: `getAssertingParty`

Get external IdP

Get external IdP configuration detail for a specific ID.

Tags: `SAML`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/saml2/asserting-parties/{id}`

Operation: `updateAssertingParty`

Update external IdP

Partially update external IdP configuration for a specific ID.

Tags: `SAML`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamUpdateSaml2AssertingPartyRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/saml2/asserting-parties/{id}`

Operation: `deleteAssertingParty`

Delete external IdP

Delete external IdP configuration for a specific ID.

Tags: `SAML`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/saml2/asserting-parties/{id}/enabled`

Operation: `updateEnabled4AssertingParty`

Update enabled of external IdP

Update enabled of external IdP configuration for a specific ID.

Tags: `SAML`

Parameters:

- `None` , optional

Request body:

- `text/plain` — boolean

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties/domain/:validate`

Operation: `validateIdpDomain`

Validate Domain

Check whether the given domain is valid.

Tags: `SAML`

Parameters:

- `name` query, required (string) — Domain name to validate.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties/metadata/:import-from-file`

Operation: `importAssertingPartyFromFile`

Import external IdP from file

Import external IdP configuration from a specific metadata file.

Tags: `SAML`

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties/metadata/:import-from-uri`

Operation: `importAssertingPartyFromUri`

Import external IdP from URI

Import external IdP configuration from a specific URI.

Tags: `SAML`

Request body:

- `text/plain` — string

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/asserting-parties/types`

Operation: `listAssertingPartyTypes`

List asserting party types

List asserting party types.

Tags: `SAML`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/asserting-parties/types/{type}/attribute-mapping-template`

Operation: `getAssertingPartyAttributeMappingTemplate`

Get attribute mapping template

Get attribute mapping template by type.

Tags: `SAML`

Parameters:

- `type` path, required (string) — External IDP type.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties/certificates`

Operation: `uploadTemporaryAssertingPartyCertificate`

Upload certificate for creating external IdP

Upload temporary certificate for creating external IdP. The certificate will be expired in 5 minutes.

Tags: `SAML`

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/asserting-parties/{id}/certificates`

Operation: `listAssertingPartyCertificates`

List certificates of external IdP

List certificates for a specific external IdP.

Tags: `SAML`

Parameters:

- `None` , optional
- `sortField` query, optional (IamListCertificateSortField) — The field for sorting
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/saml2/asserting-parties/{id}/certificates`

Operation: `uploadAssertingPartyCertificate`

Upload certificate of external IdP

Upload certificate for a specific external IdP.

Tags: `SAML`

Parameters:

- `None` , optional

Request body:

- `multipart/form-data` — file

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/saml2/asserting-parties/certificates/{id}`

Operation: `deleteAssertingPartyCertificate`

Delete certificate of external IdP

Delete the specific certificate of external IdP.

Tags: `SAML`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/saml2/asserting-parties/certificates/{id}/active`

Operation: `updateActive4AssertingPartyCertificate`

Update active of external IdP certificate

Update active of external IdP certificate for a specific ID.

Tags: `SAML`

Parameters:

- `None` , optional

Request body:

- `text/plain` — boolean

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/service-provider/{registrationId}`

Operation: `getServiceProvider`

Get service provider detail

Get service provider detail for a specific registration ID.

Tags: `SAML`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/service-provider/{registrationId}/metadata`

Operation: `downloadServiceProviderMetadata`

Download metadata

Download metadata for service provider.

Tags: `SAML`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/saml2/service-provider/certificate`

Operation: `downloadServiceProviderCertificate`

Download certificate

Download certificate for service provider.

Tags: `SAML`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/app-types`

Operation: `listAppTypes`

List application types

List application types.

Tags: `Application`

Parameters:

- `global` query, optional (boolean) — Filter global app types
- `builtin` query, optional (boolean) — Filter builtin app types
- `licensed` query, optional (boolean) — Filter licensed app types

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/apps`

Operation: `listApps`

List applications

List available applications.

Tags: `Application`

Parameters:

- `appTypeIds` query, optional (string) — App type IDs
- `global` query, optional (boolean) — Filter application types based on whether they are global
- `builtin` query, optional (boolean) — Filter application types based on whether they are builtin
- `licensed` query, optional (boolean) — Filter application types based on whether they are licensed

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/apps/{id}/avatar`

Operation: `getAppAvatar`

Get app avatar

Get app avatar by ID.

Tags: `Application`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/apps/cloud-app`

Operation: `listCloudApps`

List cloud applications

List cloud applications.

Tags: `Application`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/apps/cloud-service`

Operation: `listCloudServices`

List cloud services

List cloud services.

Tags: `Application`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/apps/xcd-app`

Operation: `listXcdApps`

List XCD applications

List XCD applications.

Tags: `Application`

Parameters:

- `view` query, optional (string) — The views to return XCD application fields

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/default-app`

Operation: `getDefaultApp`

Get default application

Get default application for current user.

Tags: `Application`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/default-app`

Operation: `set`

Set default application

Set default application for current user.

Tags: `Application`

Parameters:

- `appId` query, required (integer) — Application ID

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/default-app/:reset`

Operation: `resetDefaultApp`

Reset default application

Reset default application for current user.

Tags: `Application`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users`

Operation: `getUserList`

Get page of users

Get page of users.

Tags: `Identity`

Parameters:

- `keyword` query, optional (string) — This field is used to filter users
- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `sortField` query, optional (IamListUserSortField) — The field for sorting
- `views` query, optional (array) — The logic collections of user fields (Check details at IamUserView schema)
- `fields` query, optional (array) — The user fields to return
- `applicationIds` query, optional (array) — Filter users by checking if they have a specific role in the application
- `lastLoginBefore` query, optional (string) — Last login before
- `roleIds` query, optional (array) — Role ids
- `siteIds` query, optional (array) — Site ids
- `isRootUser` query, optional (boolean) — Filter by if the user is root user or not
- `mfaEnabled` query, optional (boolean) — Filter by if the user has MFA enabled

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users`

Operation: `createUser`

Create new user

Create/Add a new user.

Tags: `Identity`

Request body:

- `application/json` — IamCreateUserRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/users`

Operation: `bulkDeleteUsers`

Delete users

Bulk delete users by identifiers.

Tags: `Identity`

Parameters:

- `ids` query, required (array) — The user identifiers to delete.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users/{id}`

Operation: `getUser`

Get user detail

Get user detail by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/users/{id}`

Operation: `updateUser`

Update user detail

Update user detail.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamUpdateUserRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/users/{id}`

Operation: `patchUpdateUser`

Patch update user detail and permission

Patch update user detail and permission.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamPatchUpdateUserRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/{id}/:add-groups`

Operation: `addUserGroup`

Add a user to user groups

Add a user to user groups.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/{id}/:remove-groups`

Operation: `removeUserGroup`

Remove a user from user groups

Remove a user from user groups.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/{id}/:add-roles`

Operation: `addUserRole`

Grant new roles to the user

Grant new roles to the user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/{id}/:remove-roles`

Operation: `removeUserRole`

Remove roles from user

Remove roles from user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users/{id}/avatar`

Operation: `getUserAvatar`

Get user avatar

Get avatar for given user.

Tags: `Identity`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/users/{id}/avatar`

Operation: `uploadUserAvatar`

Update user avatar

Update user avatar.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `multipart/form-data` — image

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users/{id}/groups`

Operation: `getUserGroup`

Get user groups for user

Get user groups for user.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/users/{id}/groups`

Operation: `replaceUserGroup`

Replace the user assigned user groups

Replace the user assigned user groups.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users/{id}/roles`

Operation: `getUserRole`

Get roles for user

Get roles for a specific user.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/users/{id}/roles`

Operation: `replaceUserRole`

Replace roles for the user

Replace roles for the user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/users/{id}/permissions`

Operation: `getUserPermissions`

Get user permissions

Get user permissions.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/{id}/:resend-email`

Operation: `resendUserInitializedEmail`

Resend user initialized email

Resend user initialized email.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/:enable`

Operation: `enableUserAccount`

Enable user account

Enable user account.

Tags: `Identity`

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/:disable`

Operation: `disableUserAccount`

Disable user account

Disable user account.

Tags: `Identity`

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/:check-email-exist`

Operation: `checkExistingEmail`

Check existing email

Check existing email. - No longer maintained and will be removed in the future. Please use this api /users/:check-email-existence.

Tags: `Identity`

Request body:

- `application/json` — IamCheckExistingEmailRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/:check-email-existence`

Operation: `checkEmailAndFindUser`

Check if email exists and find user ID

Check if email exists and find the corresponding user ID if user belongs to the same organization.

Tags: `Identity`

Request body:

- `application/json` — IamCheckEmailExistenceRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/users/:check-email-vadlidity`

Operation: `checkEmailVadlidity`

Check email vadlidity

Check email vadlidity.

Tags: `Identity`

Request body:

- `application/json` — IamCheckEmailValidityRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users`

Operation: `listExternalUsers`

List external users

List available external users.

Tags: `Identity`

Parameters:

- `keyword` query, optional (string) — This field is used to filter external users
- `None` , optional
- `None` , optional
- `None` , optional
- `sortField` query, optional (IamExternalUserSortField) — The field for sorting
- `None` , optional
- `applicationIds` query, optional (array) — Filter users by checking if they have a specific role in the application
- `accessTimeRemain` query, optional (string) — Access status
- `lastAccessBefore` query, optional (string) — Last access before
- `roleIds` query, optional (array) — Role ids
- `siteIds` query, optional (array) — Site ids

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users`

Operation: `createExternalUser`

Create new external user

Create a new external user.

Tags: `Identity`

Request body:

- `application/json` — IamCreateExternalUserRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/external-users`

Operation: `deleteExternalUsers`

Delete external users

Delete external users by identifiers.

Tags: `Identity`

Parameters:

- `ids` query, required (array) — The external user identifiers to delete.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users/{id}`

Operation: `getExternalUserById`

Get external user detail

Get external user detail by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PATCH `/external-users/{id}`

Operation: `patchUpdateExternalUsers`

Patch Update external users

Patch update external users by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamPatchUpdateExternalUserRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users/{id}/:add-groups`

Operation: `addGroupsToExternalUser`

Add groups to the external user

Add groups to the external user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users/{id}/:remove-groups`

Operation: `removeGroupsFromExternalUser`

Remove groups from external user

Remove groups from external user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users/{id}/:add-roles`

Operation: `grantRolesToExternalUser`

Grant new roles to the external user

Grant new roles to the external user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users/{id}/:remove-roles`

Operation: `removeRolesFromExternalUser`

Remove roles from external user

Remove roles from external user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users/{id}/groups`

Operation: `getExternalUserGroups`

Get user groups for external user

Get user groups for external user.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/external-users/{id}/groups`

Operation: `replaceExternalUserGroups`

Replace the external user assigned user groups

Replace the external user assigned user groups.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users/{id}/roles`

Operation: `getExternalUserRoles`

Get roles for external user

Get roles for a specific external user.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/external-users/{id}/roles`

Operation: `replaceExternalUserRoles`

Replace roles for the external user

Replace roles for the external user.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users/{id}/permissions`

Operation: `getExternalUserPermissions`

Get external user permissions

Get external user permissions.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/external-users/{id}/avatar`

Operation: `getExternalUserAvatar`

Get external user avatar

Get external avatar for given user.

Tags: `Identity`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/external-users/:check-availability`

Operation: `checkExternalUserAvailability`

Check users who can be added as external users

Check if there are any available users to be added as external users.

Tags: `Identity`

Request body:

- `application/json` — IamCheckExternalUserAvailabilityRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups`

Operation: `listUserGroups`

List user groups

List available user groups.

Tags: `Identity`

Parameters:

- `keyword` query, optional (string) — This field is used to filter groups by group name
- `direction` query, optional (string) — The sort direction
- `sortField` query, optional (IamListUserGroupSortField) — The field for sorting

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/user-groups`

Operation: `createUserGroup`

Create new user group

Create a new custom user group.

Tags: `Identity`

Request body:

- `application/json` — IamCreateUserGroupRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups/{id}`

Operation: `getUserGroupDetail`

Get user group detail

Get user group detail.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/user-groups/{id}`

Operation: `updateUserGroup`

Update user group

Update user group info.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamUpdateUserGroupRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/user-groups/{id}`

Operation: `deleteUserGroup`

Delete user group

Delete a user group by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/user-groups/{id}/:add-users`

Operation: `addUsersToUserGroup`

Add users to user group

Add users to user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/user-groups/{id}/:remove-users`

Operation: `removeUsersFromUserGroup`

Remove users from the user group

Remove users from the user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/user-groups/{id}/:grant-roles`

Operation: `grantRolesToUserGroup`

Grant roles to user group

Grant roles to user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/user-groups/{id}/:remove-roles`

Operation: `removeRolesForUserGroup`

Remove roles from user group

Remove roles from user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups/{id}/users`

Operation: `getUserGroupUsers`

Get users for user group

Get users for user group.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/user-groups/{id}/users`

Operation: `replaceUsersInUserGroup`

Replace users in the user group

Replace users in the user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups/{id}/roles`

Operation: `getUserGroupRoles`

Get roles for user group

Get roles for user group.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/user-groups/{id}/roles`

Operation: `replaceRolesForUserGroup`

Replace the roles assigned to the user group

Replace the roles assigned to the user group.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups/{id}/permissions`

Operation: `getUserGroupPermissions`

Get user group permissions

Get user group permissions.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/user-groups/{id}/avatar`

Operation: `getUserGroupAvatar`

Get user group avatar

Get user group avatar.

Tags: `Identity`

Parameters:

- `None` , optional
- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/roles`

Operation: `listRoles`

List roles

List available roles.

Tags: `Identity`

Parameters:

- `appIds` query, optional (array) — App IDs.
- `keyword` query, optional (string) — This field is used to filter roles by role name.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/roles`

Operation: `createRole`

Create a new role

Create a new custom role.

Tags: `Identity`

Request body:

- `application/json` — IamCreateRoleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/roles/names`

Operation: `listRoleNames`

Get list of role names

Get list of role names.

Tags: `Identity`

Parameters:

- `appIds` query, optional (array) — App IDs.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/roles/{id}`

Operation: `getRoleById`

Get role by ID

Get a role detail by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/roles/{id}`

Operation: `updateRole`

Update the role

Update a role profile.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamUpdateRoleRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## DELETE `/roles/{id}`

Operation: `deleteRole`

Delete the role

Delete a role by ID.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/roles/{id}/:add-permissions`

Operation: `addRolePermissions`

Add permissions to the role

Add permissions to the role.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/roles/{id}/:remove-permissions`

Operation: `removeRolePermissions`

Remove permissions from a role

Remove permissions from a role.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/roles/{id}/permissions`

Operation: `getRolePermissions`

Get permissions associated with a role

Get permissions associated with a role.

Tags: `Identity`

Parameters:

- `None` , optional

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## PUT `/roles/{id}/permissions`

Operation: `replaceRolePermissions`

Replace permissions for the role

Replace permissions for the role.

Tags: `Identity`

Parameters:

- `None` , optional

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/api-keys/{id}`

Operation: `getApiKey`

Get an API key

Fetch metadata of an existing API key.

Tags: `API Keys`

Parameters:

- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## PATCH `/api-keys/{id}`

Operation: `updateApiKey`

Update an existing API key

Updates metadata of an existing API key.

Tags: `API Keys`

Parameters:

- `None` , optional

Request body:

- `application/json` — IamUpdateApiKeyRequest

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## DELETE `/api-keys/{id}`

Operation: `deleteApiKey`

Delete an API key

Deletes an API key so that access is no longer allowed.

Tags: `API Keys`

Parameters:

- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## POST `/api-keys/{id}/:enable`

Operation: `enableApiKey`

Enable an API key

Enable an API key to allow access to resources.

Tags: `API Keys`

Parameters:

- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## POST `/api-keys/{id}/:disable`

Operation: `disableApiKey`

Disable an API key

Disable an API key to prevent access to resources.

Tags: `API Keys`

Parameters:

- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## GET `/api-keys`

Operation: `listAllApiKeys`

Fetch all API keys

Fetch all API keys belonging to a customer.

Tags: `API Keys`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `sortField` query, optional (IamApiKeySortField) — The field for sorting
- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## POST `/api-keys`

Operation: `createApiKey`

Create a new API key

Create a new API key to access resources.

Tags: `API Keys`

Request body:

- `application/json` — IamCreateApiKeyRequest

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## GET `/myaccount/api-keys`

Operation: `listMyApiKeys`

Fetch my API keys

Fetch all API keys belonging to an user.

Tags: `API Keys`

Parameters:

- `None` , optional
- `None` , optional
- `None` , optional
- `None` , optional
- `sortField` query, optional (IamApiKeySortField) — The field for sorting
- `None` , optional

Responses:

- `200` — Successful operation
- `400`
- `401`
- `403`
- `500`

## GET `/redirect`

Operation: `redirect`

Execute redirects

Redirect to different landing pages.

Tags: `Redirect`

Responses:

- `200` — OK
- `302` — Redirects to the EP1 MSP homepage if customer type is MSP. Else, if customer has EP1 license, redirects to EP1 homepage. Otherwise, redirects to XIQ homepage.
- `400`
- `401`
- `403`
- `500`

## GET `/data-centers`

Operation: `listDataCenters`

List data centers

List available data centers for specific applications.

Tags: `Misc`

Parameters:

- `app_types` query, optional (array) — App types

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/customers`

Operation: `listCustomers`

List customers

List customers.

Tags: `My MSP`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/customers`

Operation: `createCustomer`

Create new customer

Create a new customer.

Tags: `My MSP`

Request body:

- `application/json` — IamCustomerRequest

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/customers/{id}`

Operation: `getCustomer`

Get customer

Get customer information.

Tags: `My MSP`

Parameters:

- `id` path, required (string) — The ID of the customer.

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## GET `/msp-setting`

Operation: `getMspSetting`

Get MSP setting

Get MSP setting based on the current customer.

Tags: `My MSP`

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/customers/features/ai-data-use/:enable`

Operation: `enableCustomersAiDataUse`

Enable AI Data Use for Customers

Enable AI Data Use for Customers.

Tags: `My MSP`

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

## POST `/customers/features/ai-data-use/:disable`

Operation: `disableCustomersAiDataUse`

Disable AI Data Use for Customers

Disable AI Data Use for Customers.

Tags: `My MSP`

Request body:

- `application/json` — array

Responses:

- `200` — OK
- `400`
- `401`
- `403`
- `500`

