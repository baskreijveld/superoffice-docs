---
title: Services85.ConfigurationAgent.GetWindowPosSizeList SOAP
generated: 1
uid: Services85-Configuration-GetWindowPosSizeList
---

# Services85 Configuration GetWindowPosSizeList

SOAP request and response examples **Remote/Services85/Configuration.svc**
Implemented by the <see cref="M:SuperOffice.Services85.IConfigurationAgent.GetWindowPosSizeList">SuperOffice.Services85.IConfigurationAgent.GetWindowPosSizeList</see> method.

## GetWindowPosSizeList

Gets an array of WindowPosSize objects.

* **windowPosSizeIds:** The identifiers of the WindowPosSize object

**Returns:** Array of WindowPosSize objects


[WSDL file for Services85/Configuration](../Services85-Configuration.md)

Obtain a ticket from the [Services85/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetWindowPosSizeList Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Configuration="http://www.superoffice.net/ws/crm/NetServer/Services85">
  <Configuration:ApplicationToken>1234567-1234-9876</Configuration:ApplicationToken>
  <Configuration:Credentials>
    <Configuration:Ticket>7T:1234abcxyzExample==</Configuration:Ticket>
  </Configuration:Credentials>
 <SOAP-ENV:Body>
   <Configuration:GetWindowPosSizeList>
    <Configuration:WindowPosSizeIds xsi:type="NetServerServices852:ArrayOfint">
     <NetServerServices852:int xsi:type="xsd:int">0</NetServerServices852:int>
    </Configuration:WindowPosSizeIds>
   </Configuration:GetWindowPosSizeList>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetWindowPosSizeList Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Configuration="http://www.superoffice.net/ws/crm/NetServer/Services85">
 <SOAP-ENV:Body>
  <Configuration:GetWindowPosSizeListResponse>
   <Configuration:Response xsi:type="Configuration:ArrayOfWindowPosSize">
    <Configuration:WindowPosSize xsi:type="Configuration:WindowPosSize">
     <Configuration:OwnerWindow xsi:type="xsd:string"></Configuration:OwnerWindow>
     <Configuration:PersonId xsi:type="xsd:int">0</Configuration:PersonId>
     <Configuration:AssociateId xsi:type="xsd:int">0</Configuration:AssociateId>
     <Configuration:ExtraId xsi:type="xsd:int">0</Configuration:ExtraId>
     <Configuration:ExtraInfo xsi:type="xsd:string"></Configuration:ExtraInfo>
     <Configuration:Height xsi:type="xsd:int">0</Configuration:Height>
     <Configuration:LeftX xsi:type="xsd:int">0</Configuration:LeftX>
     <Configuration:State xsi:type="Configuration:ShowWindowState">Normal</Configuration:State>
     <Configuration:UpperY xsi:type="xsd:int">0</Configuration:UpperY>
     <Configuration:Width xsi:type="xsd:int">0</Configuration:Width>
     <Configuration:WindowPosSizeId xsi:type="xsd:int">0</Configuration:WindowPosSizeId>
    </Configuration:WindowPosSize>
   </Configuration:Response>
  </Configuration:GetWindowPosSizeListResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
