---
title: Services88.UserDefinedFieldInfoAgent.GetCustomFieldInfo SOAP
generated: 1
uid: Services88-UserDefinedFieldInfo-GetCustomFieldInfo
---

# Services88 UserDefinedFieldInfo GetCustomFieldInfo

SOAP request and response examples **Remote/Services88/UserDefinedFieldInfo.svc**
Implemented by the <see cref="M:SuperOffice.Services88.IUserDefinedFieldInfoAgent.GetCustomFieldInfo">SuperOffice.Services88.IUserDefinedFieldInfoAgent.GetCustomFieldInfo</see> method.

## GetCustomFieldInfo





[WSDL file for Services88/UserDefinedFieldInfo](../Services88-UserDefinedFieldInfo.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetCustomFieldInfo Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:UserDefinedFieldInfo="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <UserDefinedFieldInfo:ApplicationToken>1234567-1234-9876</UserDefinedFieldInfo:ApplicationToken>
  <UserDefinedFieldInfo:Credentials>
    <UserDefinedFieldInfo:Ticket>7T:1234abcxyzExample==</UserDefinedFieldInfo:Ticket>
  </UserDefinedFieldInfo:Credentials>
 <SOAP-ENV:Body>
   <UserDefinedFieldInfo:GetCustomFieldInfo>
    <UserDefinedFieldInfo:TableName xsi:type="xsd:string"></UserDefinedFieldInfo:TableName>
    <UserDefinedFieldInfo:FieldName xsi:type="xsd:string"></UserDefinedFieldInfo:FieldName>
   </UserDefinedFieldInfo:GetCustomFieldInfo>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetCustomFieldInfo Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:UserDefinedFieldInfo="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <UserDefinedFieldInfo:GetCustomFieldInfoResponse>
   <UserDefinedFieldInfo:Response xsi:type="UserDefinedFieldInfo:FieldInfoBase">
    <UserDefinedFieldInfo:FieldType xsi:type="UserDefinedFieldInfo:CustomFieldType">Unknown</UserDefinedFieldInfo:FieldType>
    <UserDefinedFieldInfo:FieldName xsi:type="xsd:string"></UserDefinedFieldInfo:FieldName>
    <UserDefinedFieldInfo:DisplayName xsi:type="xsd:string"></UserDefinedFieldInfo:DisplayName>
    <UserDefinedFieldInfo:Description xsi:type="xsd:string"></UserDefinedFieldInfo:Description>
    <UserDefinedFieldInfo:ShortLabel xsi:type="xsd:string"></UserDefinedFieldInfo:ShortLabel>
    <UserDefinedFieldInfo:HideLabel xsi:type="xsd:boolean">false</UserDefinedFieldInfo:HideLabel>
    <UserDefinedFieldInfo:HideField xsi:type="xsd:boolean">false</UserDefinedFieldInfo:HideField>
    <UserDefinedFieldInfo:IsIndexed xsi:type="xsd:boolean">false</UserDefinedFieldInfo:IsIndexed>
    <UserDefinedFieldInfo:IsMandatory xsi:type="xsd:boolean">false</UserDefinedFieldInfo:IsMandatory>
    <UserDefinedFieldInfo:IsReadOnly xsi:type="xsd:boolean">false</UserDefinedFieldInfo:IsReadOnly>
    <UserDefinedFieldInfo:IsExternal xsi:type="xsd:boolean">false</UserDefinedFieldInfo:IsExternal>
    <UserDefinedFieldInfo:Rank xsi:type="xsd:int">0</UserDefinedFieldInfo:Rank>
    <UserDefinedFieldInfo:TemplateVariableName xsi:type="xsd:string"></UserDefinedFieldInfo:TemplateVariableName>
   </UserDefinedFieldInfo:Response>
  </UserDefinedFieldInfo:GetCustomFieldInfoResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

