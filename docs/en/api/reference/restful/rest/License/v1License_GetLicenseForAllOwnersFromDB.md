---
title: GET License
uid: v1License_GetLicenseForAllOwnersFromDB
---

# GET License

```http
GET /api/v1/License
```

Get all licenses, with usage, from all module owners as they are stored in the database








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


## Response: array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Reason | string |  |
| CanBeActivated | bool |  |
| New |  |  |
| Current |  |  |
| ExtendedModuleLicenses | array |  |
| AccumulatedNextCheckDate | date-time |  |

## Sample request

```http!
GET /api/v1/License
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Reason": "",
    "CanBeActivated": true,
    "New": null,
    "Current": null,
    "ExtendedModuleLicenses": [
      {
        "New": null,
        "Current": null,
        "NumberOfLicensesInUse": 197,
        "NumberOfLicensesFree": 6,
        "NumberOfLicensesAdded": 945,
        "NumberOfLicensesNewTotal": 482,
        "NumberOfLicensesNewFree": 316,
        "NumberOfLicensesTotal": 433
      }
    ],
    "AccumulatedNextCheckDate": "2012-02-04T02:49:51.7179026+01:00"
  },
  {
    "Reason": "",
    "CanBeActivated": true,
    "New": null,
    "Current": null,
    "ExtendedModuleLicenses": [
      {
        "New": null,
        "Current": null,
        "NumberOfLicensesInUse": 197,
        "NumberOfLicensesFree": 6,
        "NumberOfLicensesAdded": 945,
        "NumberOfLicensesNewTotal": 482,
        "NumberOfLicensesNewFree": 316,
        "NumberOfLicensesTotal": 433
      }
    ],
    "AccumulatedNextCheckDate": "2012-02-04T02:49:51.7179026+01:00"
  }
]
```