---
title: "shiftItem resource type"
description: "A shiftItem represents a version of the shift."
author: "nkramer"
localization_priority: Normal
ms.prod: "microsoft-teams"
---

# shiftItem resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a version of a [shift](shift.md).

## Properties
| Name                         | Type                    | Req. | R.O. | Nav. | Description                                                                                                                                                                        |
|------------------------------|-------------------------|------|------|------|---------------------------------------------------------------------------------------------|
| notes               | `string`                  |      |      |      | The notes for the `shiftItem`.      |
| displayName               | `string`                  |      |      |      | The name of the `shiftItem`.     |
| startDateTime               | `DateTimeOffset`                  | ✓    |      |      | The start date and time for the `shiftItem`.     |
| endDateTime               | `DateTimeOffset`                  | ✓    |      |      | The end date and time for the `shiftItem`.     |
| theme | `enum`   |    |  |  | Supported colors: white; blue; green; purple; pink; yellow; gray; darkBlue; darkGreen; darkPurple; darkPink; darkYellow. |
| activities 	| `collection(shiftActivity)`    |    |  |  | An incremental part of a shift which can cover details of when and where an employee is during their shift. For example, an assignment or a scheduled break or lunch. |

## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.shiftItem"
}-->
```json
{
  "notes": "string",
  "displayName": "string",
  "startDateTime": "2018-10-04T00:58:45.340Z",
  "endDateTime": "2018-10-04T00:58:45.340Z",
  "theme": "white",
  "activities": [
    {
      "isPaid": true,
      "startDateTime": "2018-10-04T00:58:45.340Z",
      "endDateTime": "2018-10-04T00:58:45.340Z",
      "code": "string",
      "displayName": "string"
    }
  ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "shiftItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/shiftitem.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->