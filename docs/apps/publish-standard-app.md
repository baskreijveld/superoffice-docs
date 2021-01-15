---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: publish_standard_app       # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: Publish standard app in CRM Online environment # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:
so.topic: howto           # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud           # cloud or onsite
so.client: online               # online, web, win, pocket, or mobile
---

# Publish standard app in CRM Online environment

Congratulations, your standard application is ready!

**Pre-requisites:**

* Your standard application has [passed certification][1], including Watchcom's security evaluation.
* Your commercial contact has [completed the application listing][2] for the App Store.

**Process:**

1. We will move your application from stage to production environment and list it in the public App Store with beta status.
2. A customer clicks **Sign up** on your application listing and completes the form. We get a notification and will automatically forward the request to you with some additional information.
    * In addition to the beta form, we ask customers to sign and accept any standard commercial contract you have for the application.
3. You contact the customer to initiate the [application setup][4].
4. The customer's administrator must sign in to SuperOffice and [give their consent][5] to allow your application to access their database tenant.
5. After the beta period, your application will transition to full status if everything is OK.

<!-- Referenced links -->
[1]: certification/certify-app.md
[2]: get-listed.md
[4]: provisioning.md
[5]: consent.md