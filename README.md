# ![LOGO](logo.png) Stackdriver Error Reporting **flow**ground Connector

## Description

A generated **flow**ground connector for the Stackdriver Error Reporting API (version v1beta1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/clouderrorreporting/v1beta1/swagger.json<br/>
Generated at: 2019-05-07T17:41:18+03:00

## API Description

Groups and counts similar errors from cloud services and applications, reports new errors, and provides access to error groups and their associated errors.


## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Get the specified group.

*Tags:* `projects`

#### Input Parameters
* `groupName` - _required_ - [Required] The group resource name. Written as
<code>projects/<var>projectID</var>/groups/<var>group_name</var></code>.
Call
<a href="/error-reporting/reference/rest/v1beta1/projects.groupStats/list">
<code>groupStats.list</code></a> to return a list of groups belonging to
this project.

Example: <code>projects/my-project-123/groups/my-group</code>
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Replace the data for the specified group.<br/>
> Fails if the group does not exist.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The group resource name.
Example: <code>projects/my-project-123/groups/my-groupid</code>
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes all error events of a given project.

*Tags:* `projects`

#### Input Parameters
* `projectName` - _required_ - [Required] The resource name of the Google Cloud Platform project. Written
as `projects/` plus the
[Google Cloud Platform project
ID](https://support.google.com/cloud/answer/6158840).
Example: `projects/my-project-123`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the specified events.

*Tags:* `projects`

#### Input Parameters
* `groupId` - _optional_ - [Required] The group for which events shall be returned.
* `pageSize` - _optional_ - [Optional] The maximum number of results to return per response.
* `pageToken` - _optional_ - [Optional] A `next_page_token` provided by a previous response.
* `projectName` - _required_ - [Required] The resource name of the Google Cloud Platform project. Written
as `projects/` plus the
[Google Cloud Platform project
ID](https://support.google.com/cloud/answer/6158840).
Example: `projects/my-project-123`.
* `serviceFilter.resourceType` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.resource_type`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.resource_type).
* `serviceFilter.service` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.service`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.service).
* `serviceFilter.version` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.version`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.version).
* `timeRange.period` - _optional_ - Restricts the query to the specified time range.
    Possible values: PERIOD_UNSPECIFIED, PERIOD_1_HOUR, PERIOD_6_HOURS, PERIOD_1_DAY, PERIOD_1_WEEK, PERIOD_30_DAYS.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Report an individual error event.<br/>
> <br/>
> This endpoint accepts **either** an OAuth token,<br/>
> **or** an [API key](https://support.google.com/cloud/answer/6158862)<br/>
> for authentication. To use an API key, append it to the URL as the value of<br/>
> a `key` parameter. For example:<br/>
> <br/>
> `POST https://clouderrorreporting.googleapis.com/v1beta1/projects/example-project/events:report?key=123ABC456`

*Tags:* `projects`

#### Input Parameters
* `projectName` - _required_ - [Required] The resource name of the Google Cloud Platform project. Written
as `projects/` plus the
[Google Cloud Platform project ID](https://support.google.com/cloud/answer/6158840).
Example: `projects/my-project-123`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the specified groups.

*Tags:* `projects`

#### Input Parameters
* `alignment` - _optional_ - [Optional] The alignment of the timed counts to be returned.
Default is `ALIGNMENT_EQUAL_AT_END`.
    Possible values: ERROR_COUNT_ALIGNMENT_UNSPECIFIED, ALIGNMENT_EQUAL_ROUNDED, ALIGNMENT_EQUAL_AT_END.
* `alignmentTime` - _optional_ - [Optional] Time where the timed counts shall be aligned if rounded
alignment is chosen. Default is 00:00 UTC.
* `groupId` - _optional_ - [Optional] List all <code>ErrorGroupStats</code> with these IDs.
* `order` - _optional_ - [Optional] The sort order in which the results are returned.
Default is `COUNT_DESC`.
    Possible values: GROUP_ORDER_UNSPECIFIED, COUNT_DESC, LAST_SEEN_DESC, CREATED_DESC, AFFECTED_USERS_DESC.
* `pageSize` - _optional_ - [Optional] The maximum number of results to return per response.
Default is 20.
* `pageToken` - _optional_ - [Optional] A `next_page_token` provided by a previous response. To view
additional results, pass this token along with the identical query
parameters as the first request.
* `projectName` - _required_ - [Required] The resource name of the Google Cloud Platform project. Written
as <code>projects/</code> plus the
<a href="https://support.google.com/cloud/answer/6158840">Google Cloud
Platform project ID</a>.

Example: <code>projects/my-project-123</code>.
* `serviceFilter.resourceType` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.resource_type`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.resource_type).
* `serviceFilter.service` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.service`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.service).
* `serviceFilter.version` - _optional_ - [Optional] The exact value to match against
[`ServiceContext.version`](/error-reporting/reference/rest/v1beta1/ServiceContext#FIELDS.version).
* `timeRange.period` - _optional_ - Restricts the query to the specified time range.
    Possible values: PERIOD_UNSPECIFIED, PERIOD_1_HOUR, PERIOD_6_HOURS, PERIOD_1_DAY, PERIOD_1_WEEK, PERIOD_30_DAYS.
* `timedCountDuration` - _optional_ - [Optional] The preferred duration for a single returned `TimedCount`.
If not set, no timed counts are returned.

## License

**flow**ground :- Telekom iPaaS / googleapis-com-clouderrorreporting-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
