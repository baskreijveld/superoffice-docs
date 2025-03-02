---
title: Services88.SelectionAgent.GetSelectionMembersArchiveRows SOAP
generated: 1
uid: Services88-Selection-GetSelectionMembersArchiveRows
---

# Services88 Selection GetSelectionMembersArchiveRows

SOAP request and response examples **Remote/Services88/Selection.svc**
Implemented by the <see cref="M:SuperOffice.Services88.ISelectionAgent.GetSelectionMembersArchiveRows">SuperOffice.Services88.ISelectionAgent.GetSelectionMembersArchiveRows</see> method.

## GetSelectionMembersArchiveRows





[WSDL file for Services88/Selection](../Services88-Selection.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetSelectionMembersArchiveRows Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Selection="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <Selection:ApplicationToken>1234567-1234-9876</Selection:ApplicationToken>
  <Selection:Credentials>
    <Selection:Ticket>7T:1234abcxyzExample==</Selection:Ticket>
  </Selection:Credentials>
 <SOAP-ENV:Body>
   <Selection:GetSelectionMembersArchiveRows>
    <Selection:SelectionId xsi:type="xsd:int">0</Selection:SelectionId>
    <Selection:Select xsi:type="xsd:string"></Selection:Select>
   </Selection:GetSelectionMembersArchiveRows>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetSelectionMembersArchiveRows Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Selection="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <Selection:GetSelectionMembersArchiveRowsResponse>
   <Selection:Response xsi:type="Selection:ArrayOfArchiveListItem">
    <Selection:ArchiveListItem xsi:type="Selection:ArchiveListItem">
     <Selection:EntityName xsi:type="xsd:string"></Selection:EntityName>
     <Selection:PrimaryKey xsi:type="xsd:int">0</Selection:PrimaryKey>
     <Selection:ColumnData xsi:type="Selection:ColumnDataDictionary">
      <Selection:ColumnDataKeyValuePair>
       <Selection:Key xsi:type="xsd:string"></Selection:Key>
       <Selection:Value xsi:type="Selection:ArchiveColumnData">
        <Selection:DisplayValue xsi:type="xsd:string"></Selection:DisplayValue>
        <Selection:TooltipHint xsi:type="xsd:string"></Selection:TooltipHint>
        <Selection:LinkHint xsi:type="xsd:string"></Selection:LinkHint>
       </Selection:Value>
      </Selection:ColumnDataKeyValuePair>
     </Selection:ColumnData>
     <Selection:LinkHint xsi:type="xsd:string"></Selection:LinkHint>
     <Selection:StyleHint xsi:type="xsd:string"></Selection:StyleHint>
    </Selection:ArchiveListItem>
   </Selection:Response>
  </Selection:GetSelectionMembersArchiveRowsResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

