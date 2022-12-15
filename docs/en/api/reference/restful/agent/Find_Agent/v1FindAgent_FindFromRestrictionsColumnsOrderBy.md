---
title: POST Agents/Find/FindFromRestrictionsColumnsOrderBy
uid: v1FindAgent_FindFromRestrictionsColumnsOrderBy
---

# POST Agents/Find/FindFromRestrictionsColumnsOrderBy

```http
POST /api/v1/Agents/Find/FindFromRestrictionsColumnsOrderBy
```

Execute a Find operation and return a page of results.


&lt;para/&gt;The criteria for the Find are passed in directly, not fetched by a restriction storage provider. &lt;para/&gt;The desired columns of the result set are also passed in directly.&lt;para/&gt;The orderby information is also passed in directly.&lt;para/&gt;Use the GetCriteriaInformation, GetDefaultDesiredColumns and GetDefaultOrderBy service methods to let the system calculate these values, if you want to use or modify them.






## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/Find/FindFromRestrictionsColumnsOrderBy?$select=name,department,category/id
```


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

## Request Body: request  

Restrictions, ProviderName, DesiredColumns, OrderBy, PageSize, PageNumber 

| Property Name | Type |  Description |
|----------------|------|--------------|
| Restrictions | array |  |
| ProviderName | string |  |
| DesiredColumns | array |  |
| OrderBy | array |  |
| PageSize | int32 |  |
| PageNumber | int32 |  |


## Response: 

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: 

| Property Name | Type |  Description |
|----------------|------|--------------|
| ArchiveColumns | array | Array of ColumnInfo column specifications |
| ArchiveRows | array | Array of archive list items, i.e., the service layer carrier for archive rows. These are the find results, represented as archive rows |
| RowCount | int32 | Count of rows, independent of paging. If you order up page 1 with page size 50, the row count may still be 279, that being the number of rows that would have been returned in a  paging-off situation |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Find/FindFromRestrictionsColumnsOrderBy
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "Restrictions": [
    {
      "Name": "Bosco-Conn",
      "Operator": "nulla",
      "Values": [
        "placeat",
        "consequatur"
      ],
      "DisplayValues": [
        "quia",
        "nisi"
      ],
      "ColumnInfo": null,
      "IsActive": true,
      "SubRestrictions": [
        {},
        {}
      ],
      "InterParenthesis": 84,
      "InterOperator": "And",
      "UniqueHash": 175
    }
  ],
  "ProviderName": "Moen-Wyman",
  "DesiredColumns": [
    "et",
    "modi"
  ],
  "OrderBy": [
    {
      "Name": "Douglas, Gleason and Wilkinson",
      "Direction": "ASC"
    },
    {
      "Name": "Douglas, Gleason and Wilkinson",
      "Direction": "ASC"
    }
  ],
  "PageSize": 860,
  "PageNumber": 879
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "ArchiveColumns": [
    {
      "DisplayName": "Stehr-Balistreri",
      "DisplayTooltip": "dolores",
      "DisplayType": "est",
      "CanOrderBy": false,
      "Name": "Quigley, DuBuque and Bailey",
      "CanRestrictBy": true,
      "RestrictionType": "officia",
      "RestrictionListName": "Sporer-Green",
      "IsVisible": true,
      "ExtraInfo": "quae",
      "Width": "ipsum",
      "IconHint": "harum",
      "HeadingIconHint": "nihil"
    }
  ],
  "ArchiveRows": [
    {
      "EntityName": "Krajcik, Dickinson and Huels",
      "PrimaryKey": 105,
      "ColumnData": {
        "fieldName": {
          "DisplayValue": "architecto",
          "TooltipHint": "sunt",
          "LinkHint": "exercitationem"
        }
      },
      "LinkHint": "et",
      "StyleHint": "temporibus",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 775
        }
      }
    }
  ],
  "RowCount": 342,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 367
    }
  }
}
```