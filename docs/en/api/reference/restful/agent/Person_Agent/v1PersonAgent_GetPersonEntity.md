---
title: POST Agents/Person/GetPersonEntity
uid: v1PersonAgent_GetPersonEntity
---

# POST Agents/Person/GetPersonEntity

```http
POST /api/v1/Agents/Person/GetPersonEntity
```

Gets a PersonEntity object.







## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| personEntityId | int32 | **Required** The primary key. |
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/Person/GetPersonEntity?personEntityId=355
POST /api/v1/Agents/Person/GetPersonEntity?$select=name,department,category/id
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

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: PersonEntity

| Property Name | Type |  Description |
|----------------|------|--------------|
| PersonId | int32 | Primary key |
| Firstname | string | First name |
| MiddleName | string | Middle name or 'van' etc. |
| Lastname | string | Last name |
| Mrmrs | string | e.g. Mrs   sex_title  <para>Use MDO List name "mrmrs" to get list items.</para> |
| Title | string | Title |
| UpdatedDate | date-time | Last updated date  in UTC. |
| CreatedDate | date-time | Registered date  in UTC. |
| BirthDate | date-time | The Person birth date as UTC Date. Year 1 = Null. Year 2 = unknown year. |
| CreatedBy | Associate | The user that created the person object |
| Emails | array | A collection of the person's emails |
| Description | string | The actual text, max 2047 significant characters even though it is stored as a larger data type on some databases |
| IsAssociate | bool | Checks if the person object is an associate. The property is read-only. |
| PrivatePhones | array | Returns a collection of phone numbers that belong to the contact person. |
| Faxes | array | Returns a collection of fax numbers that belong to the contact person. |
| MobilePhones | array | Returns a collection of mobile phone numbers that belong to the contact person. |
| OfficePhones | array | Returns a collection of office phone numbers that belong to the contact person. |
| OtherPhones | array | Returns a collection of pagers that belong to the contact person. |
| Position | Position | The position. This is a predefined SuperOffice value, different from Title  <para>Use MDO List name "perspos" to get list items.</para> |
| UpdatedBy | Associate | The person that last updated the person object |
| Contact | Contact | The contact the contact person is registered on. This is required unless the 'MandatoryContactOnPerson' preference is set.  <para>Use MDO List name "contact_new" to get list items.</para> |
| Country | Country | The country this contact person is located in.  <para>Use MDO List name "country" to get list items.</para> |
| Interests | array | The person's available and selected interests.  <para>Use MDO List name "persint" to get list items.</para> |
| PersonNumber | string | Alphanumeric user field |
| FullName | string | The person's full name localized to the current culture/country.  (internal name used in clients for employees) |
| NoMailing | bool | Spam filter. Indicates if this person should retrieve advertising. |
| UsePersonAddress | bool | True if the person's address should be used as mailing address, instead of the contact's address. |
| Retired | bool | True if the user is retired and should have no rights, not appear in lists, etc. |
| Urls | array | The urls related to this person. |
| FormalName | string | Get formal name for a person, as used in labels. (Full name + person title + academic title) |
| Address | Address | Structure holding formatted address data. The layout of the array structure indicates the layout of the localized address. |
| Post3 | string | Postal address, used in Japanese versions only |
| Post2 | string | Postal address, used in Japanese versions only |
| Post1 | string | Postal address, used in Japanese versions only |
| Kanalname | string | Kana last name, used in Japanese versions only |
| Kanafname | string | Kana first name, used in Japanese versions only |
| CorrespondingAssociate | Associate | The associate corresponding to this person. Will be empty if the person is not a user (internal associate user, external user). |
| Category | Category | Person's category. Usually null. Refer to the Contact.Category instead.  Intended for use when individual persons are created. (i.e. when Person.Contact is blank)  <para>Use MDO List name "category" to get list items.</para> |
| Business | Business | Person's business - usually blank. Use Contact.Business instead. Intended for use when individual persons are created. (i.e. when Person.Contact is blank)  <para>Use MDO List name "business" to get list items.</para> |
| Associate | Associate | The associate owning this person (similar to contact.Associate) - usually blank. Use the Person.Contact.Associate instead.  Intended for use when individual persons are created (i.e. when Person.Contact is blank)  <para>Use MDO List name "associate" to get list items.</para> |
| Salutation | string | Academic title, populated from Salutation list but can be overwritten with anything at all  <para>Use MDO List name "salutation" to get list items.</para> |
| ActiveInterests | int32 | The number of active interests. |
| SupportAssociate | Associate | <para>Use MDO List name "associate" to get list items.</para> |
| TicketPriority | TicketPriority | <para>Use MDO List name "ticketpriority" to get list items.</para> |
| CustomerLanguage | CustomerLanguage | <para>Use MDO List name "customerlanguage" to get list items.</para> |
| DbiAgentId | int32 | Integration agent (eJournal) |
| DbiKey | string | The primary key for the integrated entry in the external datasource. |
| DbiLastModified | date-time | When the entry was last modified. |
| DbiLastSyncronized | date-time | Last external syncronization. |
| SentInfo | int32 | Has information on username/password been sent (ejournal) |
| ShowContactTickets | int32 | Should tickets related to the company be shown to this person |
| UserInfo | UserInfo | Information about the user if this person is a user.  If IsAssociate (e.g. is user is true) the UserInfo will be provided. |
| ChatEmails | array |  |
| InternetPhones | array |  |
| Source | int32 | How did we get this person? For future integration needs |
| ActiveErpLinks | int32 | How many active ERP links are there for this person? |
| ShipmentTypes | array | The person's available and selected shipment types. |
| Consents | array | The person's available consent information. Missing consents are not deleted. To remove a consent, mark its legalbase as 'WITHDRAWN' |
| BounceEmails | array | Email addresses with a positive bounce counter. |
| ActiveStatusMonitorId | int32 | Active status monitor identity with the lowest rank for person |
| UserDefinedFields | object | Deprecated: Use {SuperOffice.CRM.Services.PersonEntity.CustomFields} instead. Dictionary of user defined field data. The key string is the ProgId of the UdefField, or if the ProgId is empty it is a string of the format "SuperOffice:[UdefFieldIdentity]", e.g. "SuperOffice:1234" |
| ExtraFields | object | Deprecated: Use {SuperOffice.CRM.Services.PersonEntity.CustomFields} instead. Extra fields added to the carrier. This could be data from Plug-ins, the foreign key system, external applications, etc. |
| CustomFields | object | Udef + Extra fields added to the carrier. Extra fields as defined by changes to database schema + user-defined fields as defined by admin. Custom fields combines user defined fields and extra fields into one bucket.  The individual {SuperOffice.CRM.Services.PersonEntity.ExtraFields} and <see cref="P:SuperOffice.CRM.Services.PersonEntity.UserDefinedFields">UserDefinedFields</see> properties are deprecated in favor of this combined collection. |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Person/GetPersonEntity
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: fr,de,ru,zh
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "PersonId": 561,
  "Firstname": "Genesis",
  "MiddleName": "Bednar-Swift",
  "Lastname": "Lowe",
  "Mrmrs": "sint",
  "Title": "nemo",
  "UpdatedDate": "2002-05-21T11:22:38.6490284+02:00",
  "CreatedDate": "2022-02-10T11:22:38.6490284+01:00",
  "BirthDate": "2013-01-17T11:22:38.6490284+01:00",
  "CreatedBy": null,
  "Emails": [
    {
      "Value": "distinctio",
      "StrippedValue": "asperiores",
      "Description": "Operative uniform superstructure",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 127
        }
      }
    },
    {
      "Value": "distinctio",
      "StrippedValue": "asperiores",
      "Description": "Operative uniform superstructure",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 127
        }
      }
    }
  ],
  "Description": "Digitized methodical portal",
  "IsAssociate": false,
  "PrivatePhones": [
    {
      "Value": "nam",
      "StrippedValue": "at",
      "Description": "Organic cohesive capacity",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 713
        }
      }
    },
    {
      "Value": "nam",
      "StrippedValue": "at",
      "Description": "Organic cohesive capacity",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 713
        }
      }
    }
  ],
  "Faxes": [
    {
      "Value": "voluptatibus",
      "StrippedValue": "voluptas",
      "Description": "Ameliorated contextually-based budgetary management",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 836
        }
      }
    },
    {
      "Value": "voluptatibus",
      "StrippedValue": "voluptas",
      "Description": "Ameliorated contextually-based budgetary management",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 836
        }
      }
    }
  ],
  "MobilePhones": [
    {
      "Value": "nostrum",
      "StrippedValue": "nesciunt",
      "Description": "Object-based global software",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 309
        }
      }
    },
    {
      "Value": "nostrum",
      "StrippedValue": "nesciunt",
      "Description": "Object-based global software",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 309
        }
      }
    }
  ],
  "OfficePhones": [
    {
      "Value": "ut",
      "StrippedValue": "debitis",
      "Description": "Progressive content-based frame",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 579
        }
      }
    },
    {
      "Value": "ut",
      "StrippedValue": "debitis",
      "Description": "Progressive content-based frame",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 579
        }
      }
    }
  ],
  "OtherPhones": [
    {
      "Value": "vel",
      "StrippedValue": "fuga",
      "Description": "User-friendly holistic hierarchy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 702
        }
      }
    },
    {
      "Value": "vel",
      "StrippedValue": "fuga",
      "Description": "User-friendly holistic hierarchy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 702
        }
      }
    }
  ],
  "Position": null,
  "UpdatedBy": null,
  "Contact": null,
  "Country": null,
  "Interests": [
    {
      "Id": 364,
      "Name": "DuBuque Inc and Sons",
      "ToolTip": "Quas iste et aspernatur.",
      "Deleted": true,
      "Rank": 818,
      "Type": "quam",
      "ColorBlock": 67,
      "IconHint": "occaecati",
      "Selected": false,
      "LastChanged": "2014-12-24T11:22:38.6490284+01:00",
      "ChildItems": [
        {},
        {}
      ],
      "ExtraInfo": "veniam",
      "StyleHint": "quisquam",
      "Hidden": false,
      "FullName": "Tate Upton",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 43
        }
      }
    }
  ],
  "PersonNumber": "1210674",
  "FullName": "Giles Pinkie Beahan I",
  "NoMailing": false,
  "UsePersonAddress": true,
  "Retired": false,
  "Urls": [
    {
      "Value": "ut",
      "StrippedValue": "quo",
      "Description": "Fundamental 5th generation policy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 370
        }
      }
    },
    {
      "Value": "ut",
      "StrippedValue": "quo",
      "Description": "Fundamental 5th generation policy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 370
        }
      }
    }
  ],
  "FormalName": "Green, Mills and Feil",
  "Address": null,
  "Post3": "nesciunt",
  "Post2": "delectus",
  "Post1": "impedit",
  "Kanalname": "non",
  "Kanafname": "veritatis",
  "CorrespondingAssociate": null,
  "Category": null,
  "Business": null,
  "Associate": null,
  "Salutation": "voluptates",
  "ActiveInterests": 700,
  "SupportAssociate": null,
  "TicketPriority": null,
  "CustomerLanguage": null,
  "DbiAgentId": 253,
  "DbiKey": "odit",
  "DbiLastModified": "1999-08-02T11:22:38.6490284+02:00",
  "DbiLastSyncronized": "2003-02-14T11:22:38.6490284+01:00",
  "SentInfo": 213,
  "ShowContactTickets": 280,
  "UserInfo": null,
  "ChatEmails": [
    {
      "Value": "labore",
      "StrippedValue": "repudiandae",
      "Description": "Devolved didactic policy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 453
        }
      }
    },
    {
      "Value": "labore",
      "StrippedValue": "repudiandae",
      "Description": "Devolved didactic policy",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 453
        }
      }
    }
  ],
  "InternetPhones": [
    {
      "Value": "dolor",
      "StrippedValue": "omnis",
      "Description": "Front-line non-volatile function",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 186
        }
      }
    },
    {
      "Value": "dolor",
      "StrippedValue": "omnis",
      "Description": "Front-line non-volatile function",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 186
        }
      }
    }
  ],
  "Source": 898,
  "ActiveErpLinks": 140,
  "ShipmentTypes": [
    {
      "Id": 938,
      "Name": "Wintheiser Group",
      "ToolTip": "Temporibus ut.",
      "Deleted": false,
      "Rank": 668,
      "Type": "sint",
      "ColorBlock": 436,
      "IconHint": "id",
      "Selected": false,
      "LastChanged": "2022-01-28T11:22:38.6490284+01:00",
      "ChildItems": [
        {},
        {}
      ],
      "ExtraInfo": "sit",
      "StyleHint": "voluptatum",
      "Hidden": false,
      "FullName": "Alison Mireya Stracke DDS",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 307
        }
      }
    }
  ],
  "Consents": [
    {
      "ConsentPersonId": 115,
      "Comment": "quis",
      "Registered": "1998-10-18T11:22:38.6490284+02:00",
      "RegisteredAssociateId": 876,
      "Updated": "1999-06-25T11:22:38.6490284+02:00",
      "UpdatedAssociateId": 330,
      "LegalBaseId": 643,
      "LegalBaseKey": "sint",
      "LegalBaseName": "Bayer, Zulauf and Dach",
      "ConsentPurposeId": 44,
      "ConsentPurposeKey": "animi",
      "ConsentPurposeName": "Lynch-Weimann",
      "ConsentSourceId": 929,
      "ConsentSourceKey": "repudiandae",
      "ConsentSourceName": "Keeling-Ratke",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 434
        }
      }
    }
  ],
  "BounceEmails": [
    "camylle@pfeffer.name",
    "gennaro@ziemedaniel.co.uk"
  ],
  "ActiveStatusMonitorId": 432,
  "UserDefinedFields": {
    "SuperOffice:1": "Bradly Kemmer DDS",
    "SuperOffice:2": "False"
  },
  "ExtraFields": {
    "ExtraFields1": "quod",
    "ExtraFields2": "vel"
  },
  "CustomFields": {
    "CustomFields1": "ut",
    "CustomFields2": "velit"
  },
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 983
    }
  }
}
```