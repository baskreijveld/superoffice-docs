---
title: GET ForeignApp/{id}
uid: v1ForeignAppEntity_GetForeignAppEntity
---

# GET ForeignApp/{id}

```http
GET /api/v1/ForeignApp/{id}
```

Gets a ForeignAppEntity object.


Calls the ForeignSystem agent service GetForeignAppEntity.





| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The id of the ForeignAppEntity to return. **Required** |


## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category" Default = show all fields. |

```http
GET /api/v1/ForeignApp/{id}?$select=name,department,category/id
```


## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |


## Response:

ForeignAppEntity found.

| Response | Description |
|----------------|-------------|
| 200 | ForeignAppEntity found. |
| 304 | ForeignAppEntity has not changed since the requested If-Modified-Since date. |
| 404 | Not Found. |

### Response body: ForeignAppEntityWithLinks

| Property Name | Type |  Description |
|----------------|------|--------------|
| ForeignAppId | int32 | Primary key |
| Name | string | Name of foreign application |
| CreatedDate | date-time | Registered when  in UTC. |
| UpdatedDate | date-time | Last updated when  in UTC. |
| CreatedBy | Associate | The person that created the foreign application. |
| UpdatedBy | Associate | The person that last updated this foreign application. |
| Devices | array | The devices that belong to this foreign app. |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |
| _Links | object |  |

## Sample request

```http!
GET /api/v1/ForeignApp/{id}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 200 ForeignAppEntity found.
Content-Type: application/json; charset=utf-8
Last-Modified: Sat, 26 Sep 1998 11:22:44 G9T

{
  "ForeignAppId": 103,
  "Name": "Bruen-Zemlak",
  "CreatedDate": "1998-06-07T11:22:44.8662479+02:00",
  "UpdatedDate": "1998-09-26T11:22:44.8662479+02:00",
  "CreatedBy": null,
  "UpdatedBy": null,
  "Devices": [
    {
      "ForeignDeviceId": 604,
      "Name": "Bosco, Kuphal and Boehm",
      "CreatedDate": "2001-11-13T11:22:44.8662479+01:00",
      "UpdatedDate": "2014-06-11T11:22:44.8662479+02:00",
      "AssociateFullName": "Dorothea Effertz",
      "CreatedBy": "qui",
      "UpdatedBy": "et",
      "DeviceIdentifier": "commodi",
      "ForeignAppId": 533,
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 941
        }
      }
    }
  ],
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 262
    }
  },
  "_Links": {
    "Self": "https://www.example.com/api/v1/project/321",
    "Archive": "https://www.example.com/api/v1/project"
  }
}
```