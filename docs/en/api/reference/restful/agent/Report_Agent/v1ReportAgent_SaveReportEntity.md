---
title: POST Agents/Report/SaveReportEntity
uid: v1ReportAgent_SaveReportEntity
---

# POST Agents/Report/SaveReportEntity

```http
POST /api/v1/Agents/Report/SaveReportEntity
```

Updates the existing ReportEntity or creates a new ReportEntity if the id parameter is empty








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

The ReportEntity to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| ReportId | Integer | The id of the report. |
| ReportCategory | String | The category of the report. |
| Description | String | The description of the report. |
| ReportLayout | String | The layout of the report. |
| Name | String | The name of the report |
| AssociateId | Integer | The owner of the report. |
| TemplateId | Integer | The id of report template. |
| Published | Boolean | Is the report published? |

## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: ReportEntity

| Property Name | Type |  Description |
|----------------|------|--------------|
| ReportId | int32 | The id of the report. |
| ReportCategory | string | The category of the report. |
| Description | string | The description of the report. |
| ReportLayout | string | The layout of the report. |
| Name | string | The name of the report |
| AssociateId | int32 | The owner of the report. |
| TemplateId | int32 | The id of report template. |
| Published | bool | Is the report published? |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Report/SaveReportEntity
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "ReportId": 84,
  "ReportCategory": "All",
  "Description": "Implemented radical portal",
  "ReportLayout": "CalendarMonth",
  "Name": "Dibbert Group",
  "AssociateId": 804,
  "TemplateId": 877,
  "Published": false
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "ReportId": 130,
  "ReportCategory": "All",
  "Description": "Cloned asynchronous solution",
  "ReportLayout": "CalendarMonth",
  "Name": "Funk-Weimann",
  "AssociateId": 882,
  "TemplateId": 502,
  "Published": false,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 755
    }
  }
}
```