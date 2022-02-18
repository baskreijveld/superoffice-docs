---
title: PUT List/SelectionCategory/Items/{id}/UserGroups
id: v1SelectionCategoryList_PutSelectionCategoryUserGroupsForListItem
---

# PUT List/SelectionCategory/Items/{id}/UserGroups

```http
PUT /api/v1/List/SelectionCategory/Items/{itemId}/UserGroups
```

Saves user groups visible for the SelectionCategory list's item.

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

## Sample Request

```http!
PUT /api/v1/List/SelectionCategory/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 672,
    "Name": "Daniel, Schaden and Heller",
    "ToolTip": "Cupiditate pariatur.",
    "Deleted": true,
    "Rank": 295,
    "Type": "excepturi",
    "ColorBlock": 120,
    "IconHint": "corrupti",
    "Selected": true,
    "LastChanged": "2012-02-23T18:25:52.2039861+01:00",
    "ChildItems": [
      {
        "Id": 263,
        "Name": "Gottlieb Group",
        "ToolTip": "Consequatur quibusdam quaerat repellat ut est.",
        "Deleted": false,
        "Rank": 998,
        "Type": "et",
        "ColorBlock": 604,
        "IconHint": "voluptatem",
        "Selected": true,
        "LastChanged": "2014-09-17T18:25:52.2039861+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "culpa",
        "StyleHint": "corrupti",
        "Hidden": true,
        "FullName": "Ada Schoen"
      }
    ],
    "ExtraInfo": "repellendus",
    "StyleHint": "neque",
    "Hidden": false,
    "FullName": "Krystel Nienow Jr."
  }
]
```

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 330,
    "Name": "Thiel Group",
    "ToolTip": "Alias blanditiis et dolor unde vero sit.",
    "Deleted": false,
    "Rank": 126,
    "Type": "repellat",
    "ColorBlock": 517,
    "IconHint": "id",
    "Selected": true,
    "LastChanged": "2011-11-03T18:25:52.2049859+01:00",
    "ChildItems": [
      {
        "Id": 350,
        "Name": "McClure LLC",
        "ToolTip": "Sed dicta ullam modi officiis.",
        "Deleted": false,
        "Rank": 707,
        "Type": "veniam",
        "ColorBlock": 756,
        "IconHint": "non",
        "Selected": false,
        "LastChanged": "2015-05-11T18:25:52.2049859+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "enim",
        "StyleHint": "odit",
        "Hidden": false,
        "FullName": "Joaquin Orn",
        "TableRight": {},
        "FieldProperties": {
          "fieldName": {
            "FieldRight": {
              "Mask": "FULL",
              "Reason": ""
            },
            "FieldType": "System.String",
            "FieldLength": 775
          }
        }
      }
    ],
    "ExtraInfo": "dolores",
    "StyleHint": "voluptatibus",
    "Hidden": true,
    "FullName": "Clara Hyatt",
    "TableRight": {
      "Mask": "Delete",
      "Reason": ""
    },
    "FieldProperties": {
      "fieldName": {
        "FieldRight": {
          "Mask": "FULL",
          "Reason": ""
        },
        "FieldType": "System.String",
        "FieldLength": 197
      }
    }
  }
]
```