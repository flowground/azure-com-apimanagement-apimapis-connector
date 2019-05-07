# ![LOGO](logo.png) ApiManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ApiManagementClient API (version 2018-06-01-preview).

Generated from: https://api.apis.guru/v2/specs/azure.com/apimanagement-apimapis/2018-06-01-preview/swagger.json<br/>
Generated at: 2019-05-07T17:37:07+03:00

## API Description

Use these REST APIs for performing operations on API entity and their Operations associated with your Azure API Management deployment.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists all APIs of the API Management service instance.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|description | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|serviceUrl | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|path | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `tags` - _optional_ - Include tags in the response.
* `expandApiVersionSet` - _optional_ - Include full ApiVersionSet resource in response
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified API of the API Management service instance.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `deleteRevisions` - _optional_ - Delete all revisions of the Api.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the API specified by its identifier.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the API specified by its identifier.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the specified API of the API Management service instance.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates new or updates existing specified API of the API Management service instance.

*Tags:* `Api`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all diagnostics of an API.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified Diagnostic from an API.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `diagnosticId` - _required_ - Diagnostic identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the Diagnostic for an API specified by its identifier.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `diagnosticId` - _required_ - Diagnostic identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the Diagnostic for an API specified by its identifier.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `diagnosticId` - _required_ - Diagnostic identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the details of the Diagnostic for an API specified by its identifier.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `diagnosticId` - _required_ - Diagnostic identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new Diagnostic for an API or updates an existing one.

*Tags:* `ApiDiagnostic`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `diagnosticId` - _required_ - Diagnostic identifier. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all issues associated with the specified API.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|userId | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|state | eq |    |

* `expandCommentsAttachments` - _optional_ - Expand the comment attachments. 
* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified Issue from an API.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the Issue for an API specified by its identifier.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `expandCommentsAttachments` - _optional_ - Expand the comment attachments. 
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the Issue for an API specified by its identifier.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates an existing issue for an API.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new Issue for an API or updates an existing one.

*Tags:* `ApiIssue`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all attachments for the Issue associated with the specified API.

*Tags:* `ApiIssueAttachment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|userId | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified comment from an Issue.

*Tags:* `ApiIssueAttachment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `attachmentId` - _required_ - Attachment identifier within an Issue. Must be unique in the current Issue.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the issue Attachment for an API specified by its identifier.

*Tags:* `ApiIssueAttachment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `attachmentId` - _required_ - Attachment identifier within an Issue. Must be unique in the current Issue.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the issue Attachment for an API specified by its identifier.

*Tags:* `ApiIssueAttachment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `attachmentId` - _required_ - Attachment identifier within an Issue. Must be unique in the current Issue.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new Attachment for the Issue in an API or updates an existing one.

*Tags:* `ApiIssueAttachment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `attachmentId` - _required_ - Attachment identifier within an Issue. Must be unique in the current Issue.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all comments for the Issue associated with the specified API.

*Tags:* `ApiIssueComment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|userId | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified comment from an Issue.

*Tags:* `ApiIssueComment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `commentId` - _required_ - Comment identifier within an Issue. Must be unique in the current Issue.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the issue Comment for an API specified by its identifier.

*Tags:* `ApiIssueComment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `commentId` - _required_ - Comment identifier within an Issue. Must be unique in the current Issue.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the issue Comment for an API specified by its identifier.

*Tags:* `ApiIssueComment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `commentId` - _required_ - Comment identifier within an Issue. Must be unique in the current Issue.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new Comment for the Issue in an API or updates an existing one.

*Tags:* `ApiIssueComment`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `issueId` - _required_ - Issue identifier. Must be unique in the current API Management service instance.
* `commentId` - _required_ - Comment identifier within an Issue. Must be unique in the current Issue.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists a collection of the operations for the specified API.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|method | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|description | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|urlTemplate | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `tags` - _optional_
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified operation in the API.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the API Operation specified by its identifier.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the API operation specified by its identifier.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the details of the operation in the API specified by its identifier.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new operation in the API or updates an existing one.

*Tags:* `ApiOperation`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the list of policy configuration at the API Operation level.

*Tags:* `ApiOperationPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the policy configuration at the Api Operation.

*Tags:* `ApiOperationPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the policy configuration at the API Operation level.

*Tags:* `ApiOperationPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the API operation policy specified by its identifier.

*Tags:* `ApiOperationPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates policy configuration for the API Operation level.

*Tags:* `ApiOperationPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all Tags associated with the Operation.

*Tags:* `ApiOperationTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Detach the tag from the Operation.

*Tags:* `ApiOperationTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get tag associated with the Operation.

*Tags:* `ApiOperationTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state version of the tag specified by its identifier.

*Tags:* `ApiOperationTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Assign tag to the Operation.

*Tags:* `ApiOperationTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `operationId` - _required_ - Operation identifier within an API. Must be unique in the current API Management service instance.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists a collection of operations associated with tags.

*Tags:* `ApiOperationsByTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|apiName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|description | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|method | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|urlTemplate | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `includeNotTaggedOperations` - _optional_ - Include not tagged Operations.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the policy configuration at the API level.

*Tags:* `ApiPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the policy configuration at the Api.

*Tags:* `ApiPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the policy configuration at the API level.

*Tags:* `ApiPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the API policy specified by its identifier.

*Tags:* `ApiPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates policy configuration for the API.

*Tags:* `ApiPolicy`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `policyId` - _required_ - The identifier of the Policy.
    Possible values: policy.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all Products, which the API is part of.

*Tags:* `ApiProduct`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all releases of an API. An API release is created when making an API Revision current. Releases are also used to rollback to previous revisions. Results will be paged and can be constrained by the $top and $skip parameters.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|notes | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the specified release in the API.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `releaseId` - _required_ - Release identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Returns the details of an API release.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `releaseId` - _required_ - Release identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Returns the etag of an API release.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `releaseId` - _required_ - Release identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the details of the release of the API specified by its identifier.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `releaseId` - _required_ - Release identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates a new Release for the API.

*Tags:* `ApiRelease`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `releaseId` - _required_ - Release identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all revisions of an API.

*Tags:* `ApiRevision`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|apiRevision | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the schema configuration at the API level.

*Tags:* `ApiSchema`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|contentType | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes the schema configuration at the Api.

*Tags:* `ApiSchema`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `schemaId` - _required_ - Schema identifier within an API. Must be unique in the current API Management service instance.
* `force` - _optional_ - If true removes all references to the schema before deleting it.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get the schema configuration at the API level.

*Tags:* `ApiSchema`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `schemaId` - _required_ - Schema identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the schema specified by its identifier.

*Tags:* `ApiSchema`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `schemaId` - _required_ - Schema identifier within an API. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates schema configuration for the API.

*Tags:* `ApiSchema`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `schemaId` - _required_ - Schema identifier within an API. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all Tags descriptions in scope of API. Model similar to swagger - tagDescription is defined on API level but tag may be assigned to the Operations

*Tags:* `ApiTagDescription`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Delete tag description for the Api.

*Tags:* `ApiTagDescription`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get Tag description in scope of API

*Tags:* `ApiTagDescription`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state version of the tag specified by its identifier.

*Tags:* `ApiTagDescription`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Create/Update tag description in scope of the Api.

*Tags:* `ApiTagDescription`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all Tags associated with the API.

*Tags:* `ApiTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Detach the tag from the Api.

*Tags:* `ApiTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Get tag associated with the API.

*Tags:* `ApiTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state version of the tag specified by its identifier.

*Tags:* `ApiTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Assign tag to the Api.

*Tags:* `ApiTag`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `apiId` - _required_ - API revision identifier. Must be unique in the current API Management service instance. Non-current revision has ;rev=n as a suffix where n is the revision number.
* `tagId` - _required_ - Tag identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-apimanagement-apimapis-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
