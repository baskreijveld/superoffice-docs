---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: authentication_with_webtools_maillink_and_pocket       # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: Authentication with WebTools, MailLink and Pocket # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords: OAuth 2.0
so.topic: concept      # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
# so.envir:                     # cloud or onsite
# so.client:                    # online, web, win, pocket, or mobile
---

# Authentication with WebTools, MailLink and Pocket

Let's look at how SuperID changes authentication for WebTools, MailLink, and Pocket.

## Before SuperID

* We use proprietary tickets representing the user for authentication. A ticket is valid for a 10-hour sliding window.

* WebTools, MailLink, and the mobile client use classic usernames and passwords. The password is stored encrypted on the device.

* A user must re-authenticate when changing the password.

* Double-clicking the WebTools owl icon will sign the user directly in to the tenant.

An invalid cached password will sometimes result in locking the user account.

## With SuperID

* We use industry-standard [OAuth 2.0 access tokens and refresh tokens][1] representing a user signed in to an application.

* The access token is valid for 1 hour. The refresh token is valid for several years.

* Access tokens can't be shared between applications.

* The tokens are unique per user and application and are stored on the device.

* WebTools, MailLink, and the mobile client use industry-standard OAuth 2.0 for Native Apps ([RFC 8252][2]).

* Double-clicking the WebTools owl icon will send the user to the tenant. If the user is not signed in, the user will be redirected back to the sign-in dialog, must click **Next**, and then possibly authenticate to sign in.

<!-- Referenced links -->
[1]: https://community.superoffice.com/en/developer/create-apps/concepts/authentication/oauth/
[2]: https://tools.ietf.org/html/rfc5282