---
title: "Get team photo"
description: "Get the photo (picture) for a team."
author: "clearab"
localization_priority: Priority
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# Get team photo

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the photo (picture) for a team. The method first attempts to retrieve the specified photo from Office 365. If the photo is not available in Office 365, it attempts to retrieve the photo from Azure Active Directory instead.

The supported sizes of HD photos in Office 365 are as follows: 48x48, 64x64, 96x96, 120x120, 240x240, 360x360, 432x432, 504x504, and 648x648. Photos can be any dimension if they are stored in Azure Active Directory.

You can get the metadata of the largest available photo, or optionally specify a size to get the metadata for that photo size. If the size you request is not available, you can still get a smaller size that the user has uploaded and made available. For example, if the user uploads a photo that is 504x504 pixels, all but the 648x648 size of the photo will be available for download. If the specified size is not available in the user's mailbox or in Azure Active Directory, the size 1x1 is returned with the rest of the metadata.

> Note: There is a limit of 4 MB on the total size of the rest request. This limits the photo size to less than 4 MB.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Group.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Group.ReadWrite.All |

## HTTP Request

<!-- {
  "blockType": "request",
  "name": "get_team_photo"
}-->

```http
GET /beta/teams/{id}/photo
GET /beta/teams/{id}/photo/{size}
```

## Optional query parameters

This method supports an optional query parameter to specifiy the size of the photo to be retreived.
 
|**Parameter**|**Type**|**Description**|
|:-----|:-----|:-----|
|size  |String  | A photo size. The supported sizes of HD photos on Office 365 are as follows: 48x48, 64x64, 96x96, 120x120, 240x240, 360x360, 432x432, 504x504, and 648x648. Photos can be any dimension if they are stored in Azure Active Directory. |

## Request headers

| Header        | Value           |
|:--------------|:--------------  |
| Authorization | Bearer {token}. Required.  |

## Request body

Do not supply a body for this request.

## Response

If successful, this method returns a `200 OK` response code, metadata about the photo,  and the binary data for the photo.

## Example

### Request

Here is an example of the request.

<!-- {
  "blockType": "request",
  "name": "list_channels"
}-->
```http
https://graph.microsoft.com/beta/teams/{id}/photo/240x240
```

## Response

Here is an example of the response.

> **Note:** The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.


<!-- {
  "blockType": "response",
  "truncated": true,
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/jpeg",
    "@odata.mediaEtag": "\"BA09D118\"",
    "id": "240X240",
    "width": 240,
    "height": 240
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get team photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->