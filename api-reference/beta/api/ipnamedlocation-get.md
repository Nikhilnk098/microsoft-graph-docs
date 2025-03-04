---
title: "Get ipNamedLocation"
description: "Retrieve the properties and relationships of an ipnamedlocation object."
localization_priority: Normal
author: "davidmu1"
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Get ipNamedLocation

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve the properties and relationships of an [ipNamedLocation](../resources/ipNamedLocation.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /conditionalAccess/namedLocations/{id}
```

## Optional query parameters

This method supports the `select` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and the requested [ipNamedLocation](../resources/ipnamedlocation.md) object in the response body.

## Examples

### Request

The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_ipnamedlocation"
}-->

```http
GET https://graph.microsoft.com/beta/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.ipNamedLocation"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#namedLocations/$entity",
    "@odata.type": "#microsoft.graph.ipNamedLocation",
    "id": "0854951d-5fc0-4eb1-b392-9b2c9d7949c2",
    "displayName": "Untrusted IP named location",
    "modifiedDateTime": "2019-09-04T01:11:34.9387578Z",
    "createdDateTime": "2019-09-04T01:11:34.9387578Z",
    "isTrusted": false,
    "ipRanges": [
        {
            "@odata.type": "#microsoft.graph.iPv4CidrRange",
            "cidrAddress": "12.34.221.11/22"
        },
        {
            "@odata.type": "#microsoft.graph.iPv6CidrRange",
            "cidrAddress": "2001:0:9d38:90d6:0:0:0:0/63"
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ipNamedLocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
