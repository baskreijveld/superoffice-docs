---
title: Services86.BLOBAgent.GetProductImage SOAP
generated: 1
uid: Services86-BLOB-GetProductImage
---

# Services86 BLOB GetProductImage

SOAP request and response examples **Remote/Services86/BLOB.svc**
Implemented by the <see cref="M:SuperOffice.Services86.IBLOBAgent.GetProductImage">SuperOffice.Services86.IBLOBAgent.GetProductImage</see> method.

## GetProductImage





[WSDL file for Services86/BLOB](../Services86-BLOB.md)

Obtain a ticket from the [Services86/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetProductImage Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:BLOB="http://www.superoffice.net/ws/crm/NetServer/Services86">
  <BLOB:ApplicationToken>1234567-1234-9876</BLOB:ApplicationToken>
  <BLOB:Credentials>
    <BLOB:Ticket>7T:1234abcxyzExample==</BLOB:Ticket>
  </BLOB:Credentials>
 <SOAP-ENV:Body>
   <BLOB:GetProductImage>
    <BLOB:ProductId xsi:type="xsd:int">0</BLOB:ProductId>
   </BLOB:GetProductImage>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetProductImage Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:BLOB="http://www.superoffice.net/ws/crm/NetServer/Services86">
 <SOAP-ENV:Body>
  <BLOB:GetProductImageResponse>
   <BLOB:Response xsi:type="xsd:base64Binary"></BLOB:Response>
  </BLOB:GetProductImageResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

