---
title: POST Hierarchy
uid: v1HierarchyEntity_PostHierarchyEntity
---

# POST Hierarchy

```http
POST /api/v1/Hierarchy
```

Creates a new HierarchyEntity


Calls the List agent service SaveHierarchyEntity.






## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category" Default = show all fields. |

```http
POST /api/v1/Hierarchy?$select=name,department,category/id
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

## Request Body: newEntity 

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

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

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
POST /api/v1/Hierarchy
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "HierarchyId": 507,
  "Domain": "Dashboards",
  "Name": "Pfeffer-Weber",
  "Fullname": "aut",
  "ParentId": 594,
  "Children": [
    {
      "HierarchyId": 856,
      "Domain": "Dashboards",
      "Name": "Ratke, Hermann and Farrell",
      "Fullname": "dolorum",
      "ParentId": 245,
      "Children": [
        {},
        {}
      ],
      "Registered": "2012-01-07T11:22:44.8818691+01:00",
      "RegisteredAssociateId": 910,
      "Updated": "2001-05-28T11:22:44.8818691+02:00",
      "UpdatedAssociateId": 45
    }
  ],
  "Registered": "2013-03-23T11:22:44.8818691+01:00",
  "RegisteredAssociateId": 766,
  "Updated": "2019-02-19T11:22:44.8818691+01:00",
  "UpdatedAssociateId": 419
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "HierarchyId": 215,
  "Domain": "Dashboards",
  "Name": "Stoltenberg, Watsica and Hintz",
  "Fullname": "repellendus",
  "ParentId": 191,
  "Children": [
    {
      "HierarchyId": 552,
      "Domain": "Dashboards",
      "Name": "Kshlerin, Hand and Jakubowski",
      "Fullname": "inventore",
      "ParentId": 310,
      "Children": [
        {},
        {}
      ],
      "Registered": "2011-12-08T11:22:44.8818691+01:00",
      "RegisteredAssociateId": 144,
      "Updated": "2007-06-05T11:22:44.8818691+02:00",
      "UpdatedAssociateId": 306,
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 84
        }
      }
    }
  ],
  "Registered": "2012-03-24T11:22:44.8818691+01:00",
  "RegisteredAssociateId": 461,
  "Updated": "2008-01-14T11:22:44.8818691+01:00",
  "UpdatedAssociateId": 957,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 44
    }
  },
  "_Links": {
    "Self": "https://www.example.com/api/v1/project/321",
    "Archive": "https://www.example.com/api/v1/project"
  }
}
```