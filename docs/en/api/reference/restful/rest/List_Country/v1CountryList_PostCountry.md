---
title: POST List/Country/Items
uid: v1CountryList_PostCountry
---

# POST List/Country/Items

```http
POST /api/v1/List/Country/Items
```

Create a new Country list item


Calls the List agent service SaveCountry.







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

The Country to be created. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| CountryId | Integer | Primary key |
| Name | String | Name of country in installed language |
| CurrencyId | Integer | Default currency for this country |
| EnglishName | String | Name of country in english |
| TwoLetterISOCountry | String | Two-letter country-code according to ISO3166 |
| ThreeLetterISOCountry | String | Three-letter country-code according to ISO3166 |
| ImageDescription | String | Description of the country's flag image. (This is the country flag that is displayed in the CRM client) |
| OrgNrText | String | Lead text for organisation field |
| InterAreaPrefix | String | International prefix |
| DialInPrefix | String | Dial in prefix |
| ZipPrefix | String | Post prefix |
| DomainName | String | Domain name of the country |
| AddressLayoutId | Integer | Address layout of the country |
| DomesticAddressLayoutId | Integer | Domestic address layout of the country |
| ForeignAddressLayoutId | Integer | Foreign address layout of the country |
| Rank | Integer | The rank of the country |
| Tooltip | String | The tooltip of the country |
| Deleted | Boolean | true if the country is deleted |

## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: Country

| Property Name | Type |  Description |
|----------------|------|--------------|
| CountryId | int32 | Primary key |
| Name | string | Name of country in installed language |
| CurrencyId | int32 | Default currency for this country |
| EnglishName | string | Name of country in english |
| TwoLetterISOCountry | string | Two-letter country-code according to ISO3166 |
| ThreeLetterISOCountry | string | Three-letter country-code according to ISO3166 |
| ImageDescription | string | Description of the country's flag image. (This is the country flag that is displayed in the CRM client) |
| OrgNrText | string | Lead text for organisation field |
| InterAreaPrefix | string | International prefix |
| DialInPrefix | string | Dial in prefix |
| ZipPrefix | string | Post prefix |
| DomainName | string | Domain name of the country |
| AddressLayoutId | int32 | Address layout of the country |
| DomesticAddressLayoutId | int32 | Domestic address layout of the country |
| ForeignAddressLayoutId | int32 | Foreign address layout of the country |
| Rank | int32 | The rank of the country |
| Tooltip | string | The tooltip of the country |
| Deleted | bool | true if the country is deleted |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/List/Country/Items
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "CountryId": 606,
  "Name": "Zboncak Inc and Sons",
  "CurrencyId": 918,
  "EnglishName": "Deckow, Schowalter and Reichert",
  "TwoLetterISOCountry": "Sokovia",
  "ThreeLetterISOCountry": "Sokovia",
  "ImageDescription": "Operative impactful neural-net",
  "OrgNrText": "1031070",
  "InterAreaPrefix": "est",
  "DialInPrefix": "cupiditate",
  "ZipPrefix": "odit",
  "DomainName": "Gusikowski, Yundt and Kshlerin",
  "AddressLayoutId": 105,
  "DomesticAddressLayoutId": 582,
  "ForeignAddressLayoutId": 374,
  "Rank": 994,
  "Tooltip": "aut",
  "Deleted": false
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "CountryId": 956,
  "Name": "Reichel-Morar",
  "CurrencyId": 957,
  "EnglishName": "Gerlach, Nicolas and Rolfson",
  "TwoLetterISOCountry": "Sokovia",
  "ThreeLetterISOCountry": "Sokovia",
  "ImageDescription": "Front-line 24/7 moratorium",
  "OrgNrText": "1520672",
  "InterAreaPrefix": "voluptate",
  "DialInPrefix": "porro",
  "ZipPrefix": "qui",
  "DomainName": "Olson Inc and Sons",
  "AddressLayoutId": 790,
  "DomesticAddressLayoutId": 637,
  "ForeignAddressLayoutId": 27,
  "Rank": 299,
  "Tooltip": "commodi",
  "Deleted": false,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 335
    }
  }
}
```