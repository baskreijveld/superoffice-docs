---
title: Services86.PersonAgent.CreateTemporaryKey SOAP
generated: 1
uid: Services86-Person-CreateTemporaryKey
---

# Services86 Person CreateTemporaryKey

SOAP request and response examples **Remote/Services86/Person.svc**
Implemented by the <see cref="M:SuperOffice.Services86.IPersonAgent.CreateTemporaryKey">SuperOffice.Services86.IPersonAgent.CreateTemporaryKey</see> method.

## CreateTemporaryKey





[WSDL file for Services86/Person](../Services86-Person.md)

Obtain a ticket from the [Services86/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## CreateTemporaryKey Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices862="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Person="http://www.superoffice.net/ws/crm/NetServer/Services86">
  <Person:ApplicationToken>1234567-1234-9876</Person:ApplicationToken>
  <Person:Credentials>
    <Person:Ticket>7T:1234abcxyzExample==</Person:Ticket>
  </Person:Credentials>
 <SOAP-ENV:Body>
   <Person:CreateTemporaryKey>
    <Person:Domain xsi:type="Person:TemporaryKeyDomain">Unknown</Person:Domain>
    <Person:TargetId xsi:type="xsd:int">0</Person:TargetId>
    <Person:PersonId xsi:type="xsd:int">0</Person:PersonId>
    <Person:Expires xsi:type="xsd:dateTime">2023-01-23T10:17:08Z</Person:Expires>
   </Person:CreateTemporaryKey>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## CreateTemporaryKey Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices862="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Person="http://www.superoffice.net/ws/crm/NetServer/Services86">
 <SOAP-ENV:Body>
  <Person:CreateTemporaryKeyResponse>
   <Person:Response xsi:type="xsd:string"></Person:Response>
  </Person:CreateTemporaryKeyResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

