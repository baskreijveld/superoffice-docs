---
title: POST Agents/Quote/SaveQuoteVersion
uid: v1QuoteAgent_SaveQuoteVersion
---

# POST Agents/Quote/SaveQuoteVersion

```http
POST /api/v1/Agents/Quote/SaveQuoteVersion
```

Saves a quote version







## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/Quote/SaveQuoteVersion?$select=name,department,category/id
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

QuoteVersion 

| Property Name | Type |  Description |
|----------------|------|--------------|
| QuoteVersion | QuoteVersion | Information about a version of the . <para /> Carrier object for QuoteVersion. Services for the QuoteVersion Carrier is available from the <see cref="T:SuperOffice.CRM.Services.IQuoteAgent">Quote Agent</see>. |

## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: QuoteVersion

| Property Name | Type |  Description |
|----------------|------|--------------|
| QuoteVersionId | int32 | Primary key |
| ERPQuoteVersionKey | string | Key in the ERP system that uniquely identifies this Version within the ERP system (if available, the field may be empty). |
| QuoteId | int32 | Foreign key to CRM quote (the conceptual parent). Owning Quote of this Quote Version. |
| Description | string | Description of Version. Potentially longer text description, typically used in a tooltip. Max 2K. |
| Number | string | A quote number that the user (or ERP connector) can fill out. |
| State | string | Current state of this quote version. |
| ArchivedState | string | State that this quote version had, right before it was changed to Archived; in this way we can show what happened before the archiving. |
| Status | string | If there was a problem with for instance calculation, this field is set to warning or error. |
| Reason | string | If there was a problem, this field contains a localized explanation of the problem and possible steps to fix it that the user can be shown. |
| LikelyQuoteAlternativeId | int32 | The alternative that is considered most likely to be accepted. Used to calculate probable income. |
| SentDate | date-time | The date the version was sent to the customer. |
| FollowupId | int32 | Link to a follow-up activity, created when this quote version was sent to the customer. |
| ExpirationDate | date-time | Last date the quote Version is valid, expiration is at midnight end of this day. |
| DeliveryCountryId | int32 | Country of delivery address, typically copied from the contact record |
| HasOwnDeliveryAddress | bool | The delivery address is not the same as the contact's Street address |
| InvoiceCountryId | int32 | Country of invoice address, typically copied from contact record |
| HasOwnInvoiceAddress | bool | The quote has an address for Invoicing. This will typically be copied from the company's addresses. |
| ERPPaymentTermsKey | string | Either a List id to an id from a connector provided list, or, if the connection doesn’t support lists, a text. For instance: ‘Standard 30 days’. |
| ERPPaymentTypeKey | string | Either a List id to an id from a connector provided list, or, if the connection doesn’t support lists, a text. For instance: 'Invoice'. |
| ERPDeliveryTermsKey | string | Either a List id to an id from a connector provided list, or, if the connection doesn’t support lists, a text. For instance: ‘FOB’ (‘Free on board’). |
| ERPDeliveryTypeKey | string | Either a List id to an id from a connector provided list, or, if the connection doesn’t support lists, a text. For instance: ‘Air’. |
| Rank | int32 | Rank/Version number, starts at 1 |
| ApprovedBy | int32 | Id of associate who approved (or rejected approval) for this version |
| ApprovedText | string | Text with comments on why approval was granted (or rejected) |
| ApprovedRegisteredBy | int32 | Id of associate who actually entered the approval; might be different from ApprovedBy (f.x. due to telephone consultation/approval) |
| ApprovedRegisteredDate | date-time | When was approval granted or rejected |
| ExtraField1 | string | Optional information added by Quote Connector; usable in the quote document merge process |
| ExtraField2 | string | Optional information added by Quote Connector; usable in the quote document merge process |
| ExtraField3 | string | Optional information added by Quote Connector; usable in the quote document merge process |
| ExtraField4 | string | Optional information added by Quote Connector; usable in the quote document merge process |
| ExtraField5 | string | Optional information added by Quote Connector; usable in the quote document merge process |
| LastRecalculated | date-time | When this version was last subjected to a total recalculation. This field must be set by the connector, since the connector may choose to ignore a RecalculateVersion call based on policies and possibly the current value of this field. SuperOffice will set this field to 1.1.1760 whenever any change occurs to the quote, to indicate that a recalculation is needed. |
| Updated | date-time | Last updated when  in UTC. |
| UpdatedAssociateId | int32 | Last updated by whom |
| Registered | date-time | Registered when  in UTC. |
| RegisteredAssociateId | int32 | Registered by whom |
| RequestAssociateId | int32 | User to whom the request proposal should be delivered |
| RequestComment | string | Comment for why quote should be approved |
| QuoteAlternatives | array | The QuoteAlternatives for the QuoteVersion |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Quote/SaveQuoteVersion
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
Content-Type: application/json; charset=utf-8

{
  "QuoteVersion": null
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "QuoteVersionId": 249,
  "ERPQuoteVersionKey": "at",
  "QuoteId": 11,
  "Description": "Front-line encompassing intranet",
  "Number": "773200",
  "State": "Archived",
  "ArchivedState": "Archived",
  "Status": "Error",
  "Reason": "",
  "LikelyQuoteAlternativeId": 545,
  "SentDate": "2014-03-18T11:22:38.8833285+01:00",
  "FollowupId": 617,
  "ExpirationDate": "1997-10-31T11:22:38.8833285+01:00",
  "DeliveryCountryId": 368,
  "HasOwnDeliveryAddress": true,
  "InvoiceCountryId": 540,
  "HasOwnInvoiceAddress": false,
  "ERPPaymentTermsKey": "laborum",
  "ERPPaymentTypeKey": "et",
  "ERPDeliveryTermsKey": "aut",
  "ERPDeliveryTypeKey": "a",
  "Rank": 203,
  "ApprovedBy": 914,
  "ApprovedText": "nihil",
  "ApprovedRegisteredBy": 302,
  "ApprovedRegisteredDate": "1995-12-06T11:22:38.8833285+01:00",
  "ExtraField1": "minima",
  "ExtraField2": "aut",
  "ExtraField3": "tenetur",
  "ExtraField4": "non",
  "ExtraField5": "quia",
  "LastRecalculated": "2006-12-03T11:22:38.8833285+01:00",
  "Updated": "1997-10-21T11:22:38.8833285+02:00",
  "UpdatedAssociateId": 130,
  "Registered": "2013-11-27T11:22:38.8833285+01:00",
  "RegisteredAssociateId": 715,
  "RequestAssociateId": 367,
  "RequestComment": "sunt",
  "QuoteAlternatives": [
    {
      "QuoteAlternativeId": 144,
      "ERPQuoteAlternativeKey": "ad",
      "QuoteVersionId": 786,
      "Name": "Gerlach, Carroll and Braun",
      "Description": "Phased bifurcated installation",
      "Status": "Error",
      "Reason": "",
      "ERPDiscountPercent": 26560.649999999998,
      "ERPDiscountAmount": 31311.793999999998,
      "DiscountPercent": 27516.52,
      "DiscountAmount": 19534.221999999998,
      "UserValueOverride": "DiscountAmount",
      "VATInfo": "corrupti",
      "VAT": 10777.826,
      "EarningPercent": 3485.008,
      "EarningAmount": 12072.168,
      "SubTotal": 30866.766,
      "TotalPrice": 6957.48,
      "ExtraField1": "corrupti",
      "ExtraField2": "optio",
      "ExtraField3": "quis",
      "ExtraField4": "error",
      "ExtraField5": "quibusdam",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 951
        }
      }
    }
  ],
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.String",
      "FieldLength": 525
    }
  }
}
```