---
uid: listagent-setticketcategoriesforusergroup
title: ListAgent.SetTicketCategoriesForUserGroup event method
description: Scripting events called on the SetTicketCategoriesForUserGroup method on the ListAgent service agent.
so.generated: true
keywords:
  - "netserver"
  - "scripting"
so.date: 11.29.2022
so.topic: reference
so.envir:
  - "onsite"
---
# ListAgent.SetTicketCategoriesForUserGroup

Scripting events called on the <see cref='M:SuperOffice.CRM.Services.IListAgent.SetTicketCategoriesForUserGroup'>SetTicketCategoriesForUserGroup</see> method on the <see cref='IListAgent'>IListAgent</see>  service agent.

## BeforeSetTicketCategoriesForUserGroup
```cs
    static void BeforeSetTicketCategoriesForUserGroup(
       Int32  userGroupId,
       Int32[]  categoryIds,
       ref object  eventState
      );
```
Executes before the service method is invoked.
It can store some state in the *eventState* parameter, that is passed to the **After** and **AfterAsync** methods in this service call.
Event state is not preserved between different service calls. It is set to null at the start of each service call.
## AfterSetTicketCategoriesForUserGroup
```cs
    static void AfterSetTicketCategoriesForUserGroup(
       Int32  userGroupId,
       Int32[]  categoryIds,
       ref object  eventState
      );
```
Executes after the service method has been invoked. The service waits for this method to complete before returning the result to the caller.
This service call has no return value, so there is no **returnValue** parameter
Any state you set in the **Before** method is passed in through the *eventState* parameter.
## AfterSetTicketCategoriesForUserGroupAsync
```cs
    static void AfterSetTicketCategoriesForUserGroupAsync(
       Int32  userGroupId,
       Int32[]  categoryIds,
       ref object  eventState
      );
```
Executes after the service method is invoked, without waiting for the call to return.
The service call is not blocked waiting for this method to complete.
Any state you set in the **Before** method is passed in through the *eventState* parameter.

