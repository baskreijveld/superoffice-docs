---
title: GET Sale/{id}/Simple
uid: v1SaleEntity_Simple
---

# GET Sale/{id}/Simple

```http
GET /api/v1/Sale/{id}/Simple
```

A simple Sale object.


This is a simpler, smaller variation of the full SaleEntity. Calls the Sale agent service GetSale.





| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The id of the Sale to return. **Required** |



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

SaleEntity found.

| Response | Description |
|----------------|-------------|
| 200 | SaleEntity found. |
| 404 | Not Found. |

### Response body: Sale

| Property Name | Type |  Description |
|----------------|------|--------------|
| ContactName | string | Contact name |
| SaleDate | date-time | (expected / lost / won) sales date |
| SaleId | int32 | Primary key |
| Probability | int32 | Actual probability, may differ from the one in the list |
| Title | string | Sale heading (short description?) |
| Amount | double | Total sale amount |
| Currency | string | Currency the sale was made in. |
| ProjectName | string | Project name |
| AssociateFullName | string | The sale's owner |
| Description | string | The sales description |
| Status | string | The sale's status, indicating wether the sale is open, sold or lost. |
| WeightedAmount | double | The weighted amount ( amount *  probability / 100) |
| ProjectId | int32 | Optional project reference |
| EarningPercent | double | Earning as percent of total |
| Earning | double | Earning on sale |
| ContactId | int32 | Optional contact reference |
| AssociateId | int32 | The sale's owner id |
| PersonId | int32 | The sale's contact persons id |
| SaleTypeId | int32 | The sale's type id |
| SaleTypeName | string | The sale's type name |
| PersonFullName | string | The name of the person this sale belongs to. |
| Completed | string | The Sale completed state. The completed state is either Started or Completed. NotStarted is treated as Started. The value maps to the Done database field. |
| ActiveErpLinks | int32 | The number of active erp links |
| NextDueDate | date-time | Next due date, this is a denormalization of 'closest future activity date, or most recent if no future activities'. Maintained by the system, but very convenient for searching. |
| Number | string | Alphanumeric user field |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |

## Sample request

```http!
GET /api/v1/Sale/{id}/Simple
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
```

## Sample response

```http_
HTTP/1.1 200 SaleEntity found.
Content-Type: application/json; charset=utf-8

{
  "ContactName": "Beer-Vandervort",
  "SaleDate": "2011-01-15T11:22:45.1787253+01:00",
  "SaleId": 596,
  "Probability": 14,
  "Title": "dolores",
  "Amount": 8521.346,
  "Currency": "in",
  "ProjectName": "Wolf, Reilly and Koch",
  "AssociateFullName": "Mr. Aaron Tremblay",
  "Description": "Re-engineered mission-critical standardization",
  "Status": "Lost",
  "WeightedAmount": 4973.6579999999994,
  "ProjectId": 262,
  "EarningPercent": 22790.448,
  "Earning": 4165.086,
  "ContactId": 690,
  "AssociateId": 4,
  "PersonId": 639,
  "SaleTypeId": 102,
  "SaleTypeName": "Cremin, King and Ondricka",
  "PersonFullName": "Miss Julius Freeda Price",
  "Completed": "Completed",
  "ActiveErpLinks": 149,
  "NextDueDate": "2015-02-28T11:22:45.1787253+01:00",
  "Number": "570433",
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 121
    }
  }
}
```