---
title: Services85.AppointmentAgent.GetActivityInformationListByDatesAndAssociate SOAP
generated: 1
uid: Services85-Appointment-GetActivityInformationListByDatesAndAssociate
---

# Services85 Appointment GetActivityInformationListByDatesAndAssociate

SOAP request and response examples **Remote/Services85/Appointment.svc**
Implemented by the <see cref="M:SuperOffice.Services85.IAppointmentAgent.GetActivityInformationListByDatesAndAssociate">SuperOffice.Services85.IAppointmentAgent.GetActivityInformationListByDatesAndAssociate</see> method.

## GetActivityInformationListByDatesAndAssociate





[WSDL file for Services85/Appointment](../Services85-Appointment.md)

Obtain a ticket from the [Services85/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetActivityInformationListByDatesAndAssociate Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Appointment="http://www.superoffice.net/ws/crm/NetServer/Services85">
  <Appointment:ApplicationToken>1234567-1234-9876</Appointment:ApplicationToken>
  <Appointment:Credentials>
    <Appointment:Ticket>7T:1234abcxyzExample==</Appointment:Ticket>
  </Appointment:Credentials>
 <SOAP-ENV:Body>
   <Appointment:GetActivityInformationListByDatesAndAssociate>
    <Appointment:StartDate xsi:type="xsd:dateTime">2023-01-23T10:13:57Z</Appointment:StartDate>
    <Appointment:EndDate xsi:type="xsd:dateTime">2023-01-23T10:13:57Z</Appointment:EndDate>
    <Appointment:AssociateId xsi:type="xsd:int">0</Appointment:AssociateId>
   </Appointment:GetActivityInformationListByDatesAndAssociate>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetActivityInformationListByDatesAndAssociate Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Appointment="http://www.superoffice.net/ws/crm/NetServer/Services85">
 <SOAP-ENV:Body>
  <Appointment:GetActivityInformationListByDatesAndAssociateResponse>
   <Appointment:Response xsi:type="Appointment:ArrayOfActivityInformationListItem">
    <Appointment:ActivityInformationListItem xsi:type="Appointment:ActivityInformationListItem">
     <Appointment:Date xsi:type="xsd:dateTime">2023-01-23T10:13:57Z</Appointment:Date>
     <Appointment:ActivityInformation xsi:type="Appointment:ActivitySummary">
      <Appointment:NumBusyActivities xsi:type="xsd:int">0</Appointment:NumBusyActivities>
      <Appointment:NumFreeActivities xsi:type="xsd:int">0</Appointment:NumFreeActivities>
      <Appointment:PercentageBusy xsi:type="xsd:int">0</Appointment:PercentageBusy>
     </Appointment:ActivityInformation>
    </Appointment:ActivityInformationListItem>
   </Appointment:Response>
  </Appointment:GetActivityInformationListByDatesAndAssociateResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

