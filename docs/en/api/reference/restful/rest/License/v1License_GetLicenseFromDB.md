---
title: GET License/{ownerName}
uid: v1License_GetLicenseFromDB
---

# GET License/{ownerName}

```http
GET /api/v1/License/{ownerName}
```

Get license, with usage, as it is stored in the database for one particular module owner.






| Path Part | Type | Description |
|-----------|------|-------------|
| ownerName | string | Name of the module owner. **Required** |



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

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: RecurrenceInfo

| Property Name | Type |  Description |
|----------------|------|--------------|
| Reason | string |  |
| CanBeActivated | bool |  |
| New | RecurrenceInfo |  |
| Current | RecurrenceInfo |  |
| ExtendedModuleLicenses | array |  |
| AccumulatedNextCheckDate | date-time |  |

## Sample request

```http!
GET /api/v1/License/{ownerName}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "Reason": "",
  "CanBeActivated": false,
  "New": null,
  "Current": null,
  "ExtendedModuleLicenses": [
    {
      "New": null,
      "Current": null,
      "NumberOfLicensesInUse": 373,
      "NumberOfLicensesFree": 213,
      "NumberOfLicensesAdded": 813,
      "NumberOfLicensesNewTotal": 872,
      "NumberOfLicensesNewFree": 674,
      "NumberOfLicensesTotal": 464
    }
  ],
  "AccumulatedNextCheckDate": "2011-06-28T11:22:45.412996+02:00"
}
```