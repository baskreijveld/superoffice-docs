---
title: Services87.QuoteAgent.ToggleSaleTypeQuoteAttachmentDefaultIncluded SOAP
generated: 1
uid: Services87-Quote-ToggleSaleTypeQuoteAttachmentDefaultIncluded
---

# Services87 Quote ToggleSaleTypeQuoteAttachmentDefaultIncluded

SOAP request and response examples **Remote/Services87/Quote.svc**
Implemented by the <see cref="M:SuperOffice.Services87.IQuoteAgent.ToggleSaleTypeQuoteAttachmentDefaultIncluded">SuperOffice.Services87.IQuoteAgent.ToggleSaleTypeQuoteAttachmentDefaultIncluded</see> method.

## ToggleSaleTypeQuoteAttachmentDefaultIncluded





[WSDL file for Services87/Quote](../Services87-Quote.md)

Obtain a ticket from the [Services87/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## ToggleSaleTypeQuoteAttachmentDefaultIncluded Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Quote="http://www.superoffice.net/ws/crm/NetServer/Services87">
  <Quote:ApplicationToken>1234567-1234-9876</Quote:ApplicationToken>
  <Quote:Credentials>
    <Quote:Ticket>7T:1234abcxyzExample==</Quote:Ticket>
  </Quote:Credentials>
 <SOAP-ENV:Body>
   <Quote:ToggleSaleTypeQuoteAttachmentDefaultIncluded>
    <Quote:SaleTypeQuoteAttachmentId xsi:type="xsd:int">0</Quote:SaleTypeQuoteAttachmentId>
   </Quote:ToggleSaleTypeQuoteAttachmentDefaultIncluded>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## ToggleSaleTypeQuoteAttachmentDefaultIncluded Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Quote="http://www.superoffice.net/ws/crm/NetServer/Services87">
 <SOAP-ENV:Body>
  <Quote:ToggleSaleTypeQuoteAttachmentDefaultIncludedResponse>
   <Quote:Response xsi:type="xsd:boolean">false</Quote:Response>
  </Quote:ToggleSaleTypeQuoteAttachmentDefaultIncludedResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

