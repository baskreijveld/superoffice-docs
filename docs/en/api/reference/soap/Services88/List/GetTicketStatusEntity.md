---
title: Services88.ListAgent.GetTicketStatusEntity SOAP
generated: 1
uid: Services88-List-GetTicketStatusEntity
---

# Services88 List GetTicketStatusEntity

SOAP request and response examples **Remote/Services88/List.svc**
Implemented by the <see cref="M:SuperOffice.Services88.IListAgent.GetTicketStatusEntity">SuperOffice.Services88.IListAgent.GetTicketStatusEntity</see> method.

## GetTicketStatusEntity





[WSDL file for Services88/List](../Services88-List.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetTicketStatusEntity Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:List="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <List:ApplicationToken>1234567-1234-9876</List:ApplicationToken>
  <List:Credentials>
    <List:Ticket>7T:1234abcxyzExample==</List:Ticket>
  </List:Credentials>
 <SOAP-ENV:Body>
   <List:GetTicketStatusEntity>
    <List:TicketStatusEntityId xsi:type="xsd:int">0</List:TicketStatusEntityId>
   </List:GetTicketStatusEntity>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetTicketStatusEntity Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:List="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <List:GetTicketStatusEntityResponse>
   <List:Response xsi:type="List:TicketStatusEntity">
    <List:TicketStatusId xsi:type="xsd:int">0</List:TicketStatusId>
    <List:Name xsi:type="xsd:string"></List:Name>
    <List:Status xsi:type="List:TicketBaseStatus">Unknown</List:Status>
    <List:TimeCounter xsi:type="List:TicketStatusTimeCounter">None</List:TimeCounter>
    <List:NoEmailReopen xsi:type="xsd:boolean">false</List:NoEmailReopen>
    <List:IsDefault xsi:type="xsd:boolean">false</List:IsDefault>
    <List:UsedInQueue xsi:type="xsd:boolean">false</List:UsedInQueue>
   </List:Response>
  </List:GetTicketStatusEntityResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

