---
title: PUT List/QuoteApproveReason/Items/{id}/UserGroups
uid: v1QuoteApproveReasonList_PutQuoteApproveReasonUserGroupsForListItem
---

# PUT List/QuoteApproveReason/Items/{id}/UserGroups

```http
PUT /api/v1/List/QuoteApproveReason/Items/{itemId}/UserGroups
```

Saves user groups visible for the QuoteApproveReason list's item.


Calls the List agent service SaveHeadingsForListItemFromListDefinition.





| Path Part | Type | Description |
|-----------|------|-------------|
| itemId | int32 | The ID of the item to save. **Required** |



## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Content-Type | Content-type of the request body: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |

## Request Body: entities  

The headings to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The Id of the ListItem |
| Name | string | The name of the ListItem |
| ToolTip | string | The tooltip of the ListItem |
| Deleted | bool | The deleted status of the ListItem |
| Rank | int32 | The rank of the ListItem |
| Type | string | The type of the ListItem. Custom field. |
| ColorBlock | int32 | The color indicator of the ListItem color block |
| IconHint | string | The Icon hint of the ListItem. Custom field. |
| Selected | bool | True if the ListItem is selected |
| LastChanged | date-time | Time of last change. |
| ChildItems | array | The child items of the SelectableMDOListItem |
| ExtraInfo | string | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | string | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | bool | True if the ListItem is hidden |
| FullName | string | The name of the ListItem in its context |


## Response: array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The Id of the ListItem |
| Name | string | The name of the ListItem |
| ToolTip | string | The tooltip of the ListItem |
| Deleted | bool | The deleted status of the ListItem |
| Rank | int32 | The rank of the ListItem |
| Type | string | The type of the ListItem. Custom field. |
| ColorBlock | int32 | The color indicator of the ListItem color block |
| IconHint | string | The Icon hint of the ListItem. Custom field. |
| Selected | bool | True if the ListItem is selected |
| LastChanged | date-time | Time of last change. |
| ChildItems | array | The child items of the SelectableMDOListItem |
| ExtraInfo | string | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | string | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | bool | True if the ListItem is hidden |
| FullName | string | The name of the ListItem in its context |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
PUT /api/v1/List/QuoteApproveReason/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 564,
    "Name": "Douglas-Beatty",
    "ToolTip": "Quod natus qui voluptatem neque ea voluptates ad.",
    "Deleted": false,
    "Rank": 924,
    "Type": "facere",
    "ColorBlock": 829,
    "IconHint": "quia",
    "Selected": false,
    "LastChanged": "1998-03-11T02:49:52.422202+01:00",
    "ChildItems": [
      {
        "Id": 997,
        "Name": "Bruen Inc and Sons",
        "ToolTip": "Ratione laboriosam laudantium voluptates sint.",
        "Deleted": false,
        "Rank": 960,
        "Type": "assumenda",
        "ColorBlock": 461,
        "IconHint": "saepe",
        "Selected": true,
        "LastChanged": "2001-11-14T02:49:52.422202+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "molestiae",
        "StyleHint": "aut",
        "Hidden": true,
        "FullName": "Ms. Karlee Hannah Rath Sr."
      }
    ],
    "ExtraInfo": "a",
    "StyleHint": "vel",
    "Hidden": false,
    "FullName": "Etha King"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 32,
    "Name": "Carter LLC",
    "ToolTip": "Ex assumenda hic.",
    "Deleted": false,
    "Rank": 791,
    "Type": "placeat",
    "ColorBlock": 305,
    "IconHint": "reiciendis",
    "Selected": false,
    "LastChanged": "2011-06-25T02:49:52.422202+02:00",
    "ChildItems": [
      {
        "Id": 597,
        "Name": "Lockman Inc and Sons",
        "ToolTip": "Eligendi beatae quia qui.",
        "Deleted": false,
        "Rank": 358,
        "Type": "et",
        "ColorBlock": 487,
        "IconHint": "et",
        "Selected": true,
        "LastChanged": "1995-12-14T02:49:52.422202+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "modi",
        "StyleHint": "totam",
        "Hidden": false,
        "FullName": "Taurean Labadie",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.String",
            "FieldLength": 80
          }
        }
      }
    ],
    "ExtraInfo": "corrupti",
    "StyleHint": "nulla",
    "Hidden": true,
    "FullName": "Rahul Gerlach",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.String",
        "FieldLength": 200
      }
    }
  }
]
```