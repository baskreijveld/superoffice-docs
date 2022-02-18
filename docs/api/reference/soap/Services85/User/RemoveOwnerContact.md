---
title: Services85.UserAgent.RemoveOwnerContact SOAP
generated: 1
uid: Services85-User-RemoveOwnerContact
---

# Services85 User RemoveOwnerContact

SOAP request and response examples **Remote/Services85/User.svc**
Implemented by the <see cref="M:SuperOffice.Services85.IUserAgent.RemoveOwnerContact">SuperOffice.Services85.IUserAgent.RemoveOwnerContact</see> method.

## RemoveOwnerContact

Remove a contact from the ownercontactlink table

* **contactId:** The id of the contact to remove



[WSDL file for Services85/User](../Services85-User.md)

Obtain a ticket from the [Services85/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## RemoveOwnerContact Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:User="http://www.superoffice.net/ws/crm/NetServer/Services85">
  <User:ApplicationToken>1234567-1234-9876</User:ApplicationToken>
  <User:Credentials>
    <User:Ticket>7T:1234abcxyzExample==</User:Ticket>
  </User:Credentials>
 <SOAP-ENV:Body>
   <User:RemoveOwnerContact>
    <User:ContactId xsi:type="xsd:int">0</User:ContactId>
   </User:RemoveOwnerContact>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## RemoveOwnerContact Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:User="http://www.superoffice.net/ws/crm/NetServer/Services85">
 <SOAP-ENV:Body>
  <User:RemoveOwnerContactResponse>
  </User:RemoveOwnerContactResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
