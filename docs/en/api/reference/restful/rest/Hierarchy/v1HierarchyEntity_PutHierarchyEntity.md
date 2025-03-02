---
title: PUT Hierarchy/{id}
uid: v1HierarchyEntity_PutHierarchyEntity
---

# PUT Hierarchy/{id}

```http
PUT /api/v1/Hierarchy/{id}
```

Updates the existing HierarchyEntity






| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The HierarchyEntity id to update. **Required** |


## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category" Default = show all fields. |

```http
PUT /api/v1/Hierarchy/{id}?$select=name,department,category/id
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

## Request Body: entity 

The HierarchyEntity to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| HierarchyId | Integer | The primary key (auto-incremented) |
| Domain | String | Domain seperating the different hierarchy |
| Name | String | Name of this hierarchy folder. |
| Fullname | String | The full name of this category, i.e. Foo/bar/test. |
| ParentId | Integer | Parent table |
| Children | Array | Sub-items, if any. |
| Registered | String | Registered when  in UTC. |
| RegisteredAssociateId | Integer | Registered by whom |
| Updated | String | Last updated when  in UTC. |
| UpdatedAssociateId | Integer | Last updated by whom |

## Response:

HierarchyEntity updated.

| Response | Description |
|----------------|-------------|
| 200 | HierarchyEntity updated. |
| 400 | Bad request. Entity to save is not in request body. |

### Response body: HierarchyEntityWithLinks

| Property Name | Type |  Description |
|----------------|------|--------------|
| HierarchyId | int32 | The primary key (auto-incremented) |
| Domain | string | Domain seperating the different hierarchy |
| Name | string | Name of this hierarchy folder. |
| Fullname | string | The full name of this category, i.e. Foo/bar/test. |
| ParentId | int32 | Parent table |
| Children | array | Sub-items, if any. |
| Registered | date-time | Registered when  in UTC. |
| RegisteredAssociateId | int32 | Registered by whom |
| Updated | date-time | Last updated when  in UTC. |
| UpdatedAssociateId | int32 | Last updated by whom |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |
| _Links | object |  |

## Sample request

```http!
PUT /api/v1/Hierarchy/{id}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "HierarchyId": 278,
  "Domain": "Dashboards",
  "Name": "Marks LLC",
  "Fullname": "sint",
  "ParentId": 905,
  "Children": [
    {
      "HierarchyId": 193,
      "Domain": "Dashboards",
      "Name": "Quigley, Rippin and Blanda",
      "Fullname": "deserunt",
      "ParentId": 198,
      "Children": [
        {},
        {}
      ],
      "Registered": "2013-01-17T11:22:44.8818691+01:00",
      "RegisteredAssociateId": 428,
      "Updated": "2014-07-19T11:22:44.8818691+02:00",
      "UpdatedAssociateId": 894
    }
  ],
  "Registered": "2016-02-09T11:22:44.8818691+01:00",
  "RegisteredAssociateId": 848,
  "Updated": "2008-09-07T11:22:44.8818691+02:00",
  "UpdatedAssociateId": 875
}
```

## Sample response

```http_
HTTP/1.1 200 HierarchyEntity updated.
Content-Type: application/json; charset=utf-8

{
  "HierarchyId": 126,
  "Domain": "Dashboards",
  "Name": "D'Amore, Lemke and Walker",
  "Fullname": "dolor",
  "ParentId": 804,
  "Children": [
    {
      "HierarchyId": 151,
      "Domain": "Dashboards",
      "Name": "Effertz, Mann and Rath",
      "Fullname": "a",
      "ParentId": 102,
      "Children": [
        {},
        {}
      ],
      "Registered": "2015-11-06T11:22:44.8818691+01:00",
      "RegisteredAssociateId": 105,
      "Updated": "2008-09-22T11:22:44.8818691+02:00",
      "UpdatedAssociateId": 56,
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 770
        }
      }
    }
  ],
  "Registered": "1999-10-14T11:22:44.8818691+02:00",
  "RegisteredAssociateId": 233,
  "Updated": "1995-11-15T11:22:44.8818691+01:00",
  "UpdatedAssociateId": 375,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.String",
      "FieldLength": 986
    }
  },
  "_Links": {
    "Self": "https://www.example.com/api/v1/project/321",
    "Archive": "https://www.example.com/api/v1/project"
  }
}
```