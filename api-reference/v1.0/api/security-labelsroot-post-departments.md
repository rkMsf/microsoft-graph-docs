---
title: "Create departmentTemplate"
description: "Create a new departmentTemplate object."
author: "sseth"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Create departmentTemplate
Namespace: microsoft.graph.security

Create a new [departmentTemplate](../resources/security-departmenttemplate.md) object.

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
POST /security/labels/departments
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [microsoft.graph.security.departmentTemplate](../resources/security-departmenttemplate.md) object.

You can specify the following properties when creating a **departmentTemplate**.

|Property|Type|Description|
|:---|:---|:---|
|displayName|String|Unique string that defines a department name. Inherited from [microsoft.graph.security.filePlanDescriptorTemplate](../resources/security-fileplandescriptor.md).|




## Response

If successful, this method returns a `201 Created` response code and a [microsoft.graph.security.departmentTemplate](../resources/security-departmenttemplate.md) object in the response body.

## Examples

### Request
The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "create_departmenttemplate_from_"
}
-->
``` http
POST https://graph.microsoft.com/v1.0/security/labels/departments
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.security.departmentTemplate",
  "displayName": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  }
}
```


### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.departmentTemplate"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.security.departmentTemplate",
  "id": "11b44677-9f06-c85a-4a0b-766b66904bf8",
  "displayName": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "createdDateTime": "String (timestamp)"
}
```

