---
title: GET BatchTask/{state}
uid: v1Batch_GetBatchTaskInfosByState
---

# GET BatchTask/{state}

```http
GET /api/v1/BatchTask/{state}
```

Gets an array of user BatchTaskInfo with state defined by a BatchTaskState.






| Path Part | Type | Description |
|-----------|------|-------------|
| state | Enum: Unknown, New, Aquired, Started, Succeeded, Failed, SucceededManualCleanup, All | The BatchTaskState to get batch tasks for. **Required** |



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


## Response:array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | Id of the task. |
| Name | string | Name of the task. |
| AssociateId | int32 | Task owner. If it is a System task, AssociateId = 0. |
| DetailsTable | int32 | Id of table with more information about the task. |
| DetailsRecord | int32 | Record Id of a row in the DetailsTable containing more info about the task. |
| IsSystemTask | bool | If IsSystemTask is true, the task is not initiated by an associate. |
| IsInternalTask | bool | If IsInternalTask is true, this task will not add a trace to the database. |
| ParameterObject | object | ParameterObject will be serialized to a binary blob and saved in the BinaryObject table. The link to the BinaryObject will be set using DetailsTable and DetailsRecord. |
| LastStarted | date-time | When was the task last started. |
| Created | date-time | Task creation time. |
| StartCount | int32 | Maps to the startcount field in the batchtask table. |
| DatabaseSerialNumber | string | Serial number of the database the task is to run on. |
| Context | string | Context for the executing task. |
| Result | string | Maps to the result field in the batchtask table. |
| State | string | BatchTaskState of the task. |
| Description | string | Description of the task. |
| Response | string | Maps to the response field in the batchtask table. |
| Request | string | Maps to the request field in the batchtask table. |
| ProgressDescription | string | Descriptive text for the current stage |
| ProgressPercent | int32 | Task progress, in percent of estimated total |
| FileName | string | The filename related to the batchtask. |
| CancellationBehaviour | string | Indicate if the task can be stopped. |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |

## Sample request

```http!
GET /api/v1/BatchTask/{state}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 992,
    "Name": "Marvin-Watsica",
    "AssociateId": 41,
    "DetailsTable": 13,
    "DetailsRecord": 358,
    "IsSystemTask": true,
    "IsInternalTask": false,
    "ParameterObject": {
      "ParameterObject1": "eum",
      "ParameterObject2": "enim"
    },
    "LastStarted": "1999-04-04T11:22:45.3817553+02:00",
    "Created": "2001-05-29T11:22:45.3817553+02:00",
    "StartCount": 337,
    "DatabaseSerialNumber": "479997",
    "Context": "aut",
    "Result": "culpa",
    "State": "All",
    "Description": "Future-proofed well-modulated portal",
    "Response": "nulla",
    "Request": "repellendus",
    "ProgressDescription": "Configurable 24/7 encoding",
    "ProgressPercent": 205,
    "FileName": "Bartell, Bogisich and Kub",
    "CancellationBehaviour": "CanCancel",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 811
      }
    }
  }
]
```