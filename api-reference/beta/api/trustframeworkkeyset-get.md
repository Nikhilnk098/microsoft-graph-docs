---
title: "Get trustFrameworkKeySet"
description: "Retrieve the properties and relationships of trustframeworkkeyset object."
localization_priority: Normal
author: "valnav"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Get trustFrameworkKeySet

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve the properties and associations for a [Trustframeworkkeyset](../resources/trustframeworkkeyset.md).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | TrustFrameworkKeySet.Read.All, TrustFrameworkKeySet.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | TrustFrameworkKeySet.Read.All, TrustFrameworkKeySet.ReadWrite.All |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /trustFramework/keySets/{id}
```

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and the requested [trustFrameworkKeySet](../resources/trustframeworkkeyset.md) object in the response body.

## Examples

### Request

The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_trustframeworkkeyset"
}-->

```http
GET https://graph.microsoft.com/beta/trustFramework/keySets/{id}
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.trustFrameworkKeySet"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "id-value",
  "keys": [
    {
      "k": "k-value",
      "x5c": [
        "x5c-value"
      ],
      "x5t": "x5t-value",
      "kty": "kty-value",
      "use": "use-value",
      "exp": 99,
      "nbf": 99,
      "kid": "kid-value",
      "e": "e-value",
      "n": "n-value",
      "d": "d-value",
      "p": "p-value",
      "q": "q-value",
      "dp": "dp-value",
      "dq": "dq-value",
      "qi": "qi-value"
    }
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get trustFrameworkKeySet",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->