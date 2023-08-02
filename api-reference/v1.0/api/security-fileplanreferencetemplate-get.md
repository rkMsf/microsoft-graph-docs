---
title: "Get filePlanReferenceTemplate"
description: "Read the properties and relationships of a filePlanReferenceTemplate object."
author: "sseth"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Get filePlanReferenceTemplate
Namespace: microsoft.graph.security

Read the properties and relationships of a [filePlanReferenceTemplate](../resources/security-fileplanreferencetemplate.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|RecordsManagement.Read.All, RecordsManagement.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|RecordsManagement.Read.All, RecordsManagement.ReadWrite.All|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /security/labels/filePlanReferences/{filePlanReferenceTemplateId}
GET /security/labels/retentionLabels/{retentionLabelId}/descriptors/filePlanReferenceTemplate
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.filePlanReferenceTemplate](../resources/security-fileplanreferencetemplate.md) object in the response body.

## Examples

### Request
The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "get_fileplanreferencetemplate"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/security/labels/filePlanReferences/{filePlanReferenceTemplateId}
```


### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.filePlanReferenceTemplate"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.security.filePlanReferenceTemplate",
    "id": "b1f7b518-a44f-1d4b-c6f1-ab8771d3907c",
    "displayName": "String",
    "createdBy": {
      "@odata.type": "microsoft.graph.identitySet"
    },
    "createdDateTime": "String (timestamp)"
  }
}
```

