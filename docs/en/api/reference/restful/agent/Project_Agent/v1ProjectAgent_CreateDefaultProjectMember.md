---
title: POST Agents/Project/CreateDefaultProjectMember
uid: v1ProjectAgent_CreateDefaultProjectMember
---

# POST Agents/Project/CreateDefaultProjectMember

```http
POST /api/v1/Agents/Project/CreateDefaultProjectMember
```

Set default values into a new ProjectMember.


NetServer calculates default values on the entity, which is required when creating/storing a new instance







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

### Response body: ProjectMember

| Property Name | Type |  Description |
|----------------|------|--------------|
| ProjectmemberId | int32 | Primary key |
| ContactId | int32 | Contact ID of person who is the project member |
| ProjectId | int32 | Parent project - the project this project member belongs to. |
| ContactName | string | Contact name |
| ContactDepartment | string | Contact department |
| ProjectName | string | Name of the project this project member belongs to. |
| EmailId | int32 | The person's email address id |
| EmailAddress | string | The e-mail address |
| CountryId | int32 | Country |
| Firstname | string | First name |
| MiddleName | string | Middle name or 'van' etc. |
| Lastname | string | Last name |
| PersonId | int32 | The person's id - primary key |
| Mrmrs | string | e.g. Mrs, Dr, Ms. |
| ProjectMemberTypeName | string | The projectmembers type name: 'secretary', 'member', etc. |
| Phone | string | Phone number |
| PhoneId | int32 | The phone id |
| ProjectMemberTypeId | int32 | ProjectMember Type Id - from the ProjectMemberType list.  <para>Use MDO List name "PMembType" to get list items.</para> |
| EmailAddressName | string | The e-mail address description |
| Comment | string | Comment text on the project membership |
| FullName | string | The person's full name localized to the current culture/country.  (internal name used in clients for employees) |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Project/CreateDefaultProjectMember
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "ProjectmemberId": 263,
  "ContactId": 809,
  "ProjectId": 257,
  "ContactName": "Prohaska-Strosin",
  "ContactDepartment": "",
  "ProjectName": "Medhurst-Witting",
  "EmailId": 985,
  "EmailAddress": "newell_casper@pacocha.info",
  "CountryId": 601,
  "Firstname": "Mandy",
  "MiddleName": "Roberts-Raynor",
  "Lastname": "Mitchell",
  "PersonId": 85,
  "Mrmrs": "excepturi",
  "ProjectMemberTypeName": "Hagenes Group",
  "Phone": "892.937.1473 x835",
  "PhoneId": 176,
  "ProjectMemberTypeId": 885,
  "EmailAddressName": "meagan_blick@kulasdaugherty.biz",
  "Comment": "voluptatem",
  "FullName": "Miss Maxine Devan Hayes",
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.String",
      "FieldLength": 74
    }
  }
}
```