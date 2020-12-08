---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: set_up_dkim # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: How to set up a DKIM Record # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id} # Your GitHub alias.
keywords:
so.topic:     # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud              # cloud or onsite
so.client: online              # online, web, win, pocket, or mobile
---

# How to set up a DKIM Record

Before creating the DKIM record for your domain, it is important to find out what the server address for the mail service to be authorized (which is going to be permitted to send emails on your behalf).

## Overview

1. Order the public domain key for your domain.
2. Add the key to your domain's DNS records so recipients can retrieve it for reading the DKIM header.
3. Tell SuperOffice DKIM is set up - to turn on email signing to begin adding the DKIM header to outgoing mail messages.

[!include[ALT](../includes/envir-google.md)]

[!include[ALT](../includes/hosted-by-enom.md)]

Learn more about [DKIM on DNS][2].

## Order a DKIM for your domain name

To be able to create a DKIM for your domain name, we need to know your domain name.
To make sure no one else, besides your company orders a DKIM key for your domain name, we need to make sure you are the owner of this domain name.

1. Fill out this form and submit it: [DKIM ORDER FORM][1].
2. We will reply with the DKIM to the submitted email address.
3. You will now need to add this DKIM to your DNS, see next step.

## Open the domain settings for the Google domain

[!include[ALT](../includes/open-google-domain-settings.md)]

## Add the DKIM record

1. Go to **Host Records** in the DNS console. The existing records for your Google account are there by default.

![x][3]

2. We want to add the DKIM record from Mailgun. Click **Add New** to add the new DKIM record.

  * Some DNS servers may require "version of DKIM". Add this by adding "v=DKIM1; " in front of the key: `Example: "k=rsa; p=XXX..."  -->  "_v=DKIM1;_ k=rsa; p=XXX..."`
  * Add "Host name" value ("pic.\_domainkey.\[yourdomainName\]") you received from us.
  * Add "Address" value ("_v=DKIM1;_ k=rsa; p=XXX..") you received from us (see note above)
  * Choose "txt" as record type

![x][4]

3. Click **Save** to update the information.

[!include[ALT](../includes/note-dns-propagation-time.md)]

## Test a new DKIM record

Use a tool to make sure the DKIM is propagated. Via CMD:

1. Open Windows Command Prompt: Press Win+R, type `CMD`, and click **OK**.

2. Type `nslookup` and press Enter.

3. Type `set type=txt` and press Enter.

4. Type: `pic._domainkey.yourdomainName` and press Enter.

If your key is deployed successfully, it should return your key.

There are several tools online to use - to test your DKIM record.

* [https://mxtoolbox.com/dkim.aspx#][5]
* [https://www.mail-tester.com/spf-dkim-check][6]

Here, we have used [MX Toolbox][7]. "DKIM Record Lookup"

1. Open the DKIM tool:

![x][8]

2. Add your domain name and "DKIM Selector" you received from us, and click **DKIM Lookup**.

3. The result should show the values of your public DKIM key data:

![x][9]

## Verify back to SuperOffice

Once the DKIM DNS record has been propagated and it tests OK, SuperOffice needs to be informed, so the new DKIM can be activated and used (signing your outgoing emails). Send your confirmation as a reply to the mail you received for the DKIM order. This activation may take a couple of days.

<!-- Referenced links -->
[1]: https://community.superoffice.com/en/technical/documentation/administration/mailgun-options-and-security/order-setup-dkim/order-dkim/
[2]: http://www.enom.com/kb/kb/kb_1042-dkim-on-dns.htm
[3]: https://community.superoffice.com/contentassets/82b4f8fa4d504029b3cb22e279051a89/enomdkimedit.png
[4]: https://community.superoffice.com/contentassets/82b4f8fa4d504029b3cb22e279051a89/enomdkimadd.png
[5]: https://mxtoolbox.com/dkim.aspx
[6]: https://www.mail-tester.com/spf-dkim-check
[7]: https://www.mxtoolbox.com/dkim.aspx
[8]: https://community.superoffice.com/contentassets/82b4f8fa4d504029b3cb22e279051a89/mxtoolsboxdkim.png
[9]: https://community.superoffice.com/contentassets/82b4f8fa4d504029b3cb22e279051a89/mxtoolsboxdkimresult.png