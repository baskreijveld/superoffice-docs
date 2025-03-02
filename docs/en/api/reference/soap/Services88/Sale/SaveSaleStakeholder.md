---
title: Services88.SaleAgent.SaveSaleStakeholder SOAP
generated: 1
uid: Services88-Sale-SaveSaleStakeholder
---

# Services88 Sale SaveSaleStakeholder

SOAP request and response examples **Remote/Services88/Sale.svc**
Implemented by the <see cref="M:SuperOffice.Services88.ISaleAgent.SaveSaleStakeholder">SuperOffice.Services88.ISaleAgent.SaveSaleStakeholder</see> method.

## SaveSaleStakeholder





[WSDL file for Services88/Sale](../Services88-Sale.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## SaveSaleStakeholder Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Sale="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <Sale:ApplicationToken>1234567-1234-9876</Sale:ApplicationToken>
  <Sale:Credentials>
    <Sale:Ticket>7T:1234abcxyzExample==</Sale:Ticket>
  </Sale:Credentials>
 <SOAP-ENV:Body>
   <Sale:SaveSaleStakeholder>
    <Sale:SaleStakeholder xsi:type="Sale:SaleStakeholder">
     <Sale:StakeholderRoleName xsi:type="xsd:string"></Sale:StakeholderRoleName>
     <Sale:Comment xsi:type="xsd:string"></Sale:Comment>
     <Sale:StakeholderRoleId xsi:type="xsd:int">0</Sale:StakeholderRoleId>
     <Sale:CountryId xsi:type="xsd:int">0</Sale:CountryId>
     <Sale:PersonId xsi:type="xsd:int">0</Sale:PersonId>
     <Sale:EmailDescription xsi:type="xsd:string"></Sale:EmailDescription>
     <Sale:EmailId xsi:type="xsd:int">0</Sale:EmailId>
     <Sale:EmailAddress xsi:type="xsd:string"></Sale:EmailAddress>
     <Sale:PhoneId xsi:type="xsd:int">0</Sale:PhoneId>
     <Sale:ContactName xsi:type="xsd:string"></Sale:ContactName>
     <Sale:ContactId xsi:type="xsd:int">0</Sale:ContactId>
     <Sale:SaleId xsi:type="xsd:int">0</Sale:SaleId>
     <Sale:Mrmrs xsi:type="xsd:string"></Sale:Mrmrs>
     <Sale:Firstname xsi:type="xsd:string"></Sale:Firstname>
     <Sale:MiddleName xsi:type="xsd:string"></Sale:MiddleName>
     <Sale:Lastname xsi:type="xsd:string"></Sale:Lastname>
     <Sale:SaleStakeholderId xsi:type="xsd:int">0</Sale:SaleStakeholderId>
     <Sale:Rank xsi:type="xsd:short">0</Sale:Rank>
     <Sale:Phone xsi:type="xsd:string"></Sale:Phone>
    </Sale:SaleStakeholder>
   </Sale:SaveSaleStakeholder>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## SaveSaleStakeholder Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Sale="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <Sale:SaveSaleStakeholderResponse>
   <Sale:Response xsi:type="Sale:SaleStakeholder">
    <Sale:StakeholderRoleName xsi:type="xsd:string"></Sale:StakeholderRoleName>
    <Sale:Comment xsi:type="xsd:string"></Sale:Comment>
    <Sale:StakeholderRoleId xsi:type="xsd:int">0</Sale:StakeholderRoleId>
    <Sale:CountryId xsi:type="xsd:int">0</Sale:CountryId>
    <Sale:PersonId xsi:type="xsd:int">0</Sale:PersonId>
    <Sale:EmailDescription xsi:type="xsd:string"></Sale:EmailDescription>
    <Sale:EmailId xsi:type="xsd:int">0</Sale:EmailId>
    <Sale:EmailAddress xsi:type="xsd:string"></Sale:EmailAddress>
    <Sale:PhoneId xsi:type="xsd:int">0</Sale:PhoneId>
    <Sale:ContactName xsi:type="xsd:string"></Sale:ContactName>
    <Sale:ContactId xsi:type="xsd:int">0</Sale:ContactId>
    <Sale:SaleId xsi:type="xsd:int">0</Sale:SaleId>
    <Sale:Mrmrs xsi:type="xsd:string"></Sale:Mrmrs>
    <Sale:Firstname xsi:type="xsd:string"></Sale:Firstname>
    <Sale:MiddleName xsi:type="xsd:string"></Sale:MiddleName>
    <Sale:Lastname xsi:type="xsd:string"></Sale:Lastname>
    <Sale:SaleStakeholderId xsi:type="xsd:int">0</Sale:SaleStakeholderId>
    <Sale:Rank xsi:type="xsd:short">0</Sale:Rank>
    <Sale:Phone xsi:type="xsd:string"></Sale:Phone>
   </Sale:Response>
  </Sale:SaveSaleStakeholderResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

