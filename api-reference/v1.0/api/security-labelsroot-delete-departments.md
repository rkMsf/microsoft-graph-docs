---
title: "Delete departmentTemplate"
description: "Delete a departmentTemplate object."
author: "sseth"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Delete departmentTemplate
Namespace: microsoft.graph.security

Delete a [departmentTemplate](../resources/security-departmenttemplate.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|RecordsManagement.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|RecordsManagement.ReadWrite.All|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /security/labels/departments/{departmentTemplateId}/$ref
DELETE /security/labels/retentionLabels/{retentionLabelId}/descriptors/departmentTemplate/$ref
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "delete_departmenttemplate"
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/security/labels/departments/{departmentTemplateId}
```


### Response
The following is an example of the response.
>
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

