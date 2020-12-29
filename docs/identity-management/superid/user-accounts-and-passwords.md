---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: user_accounts_and_passwords       # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description:  User accounts and passwords  # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:  
so.topic: concept                      # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
# so.envir:                     # cloud or onsite
# so.client:                    # online, web, win, pocket, or mobile
---

# User accounts and passwords

Let's look at how SuperID affects user accounts and passwords.

## How it works

* Each CRM Online user accounts can belong to 1 SuperID user account.

* A user is a SuperID user **linked to an associate** in a customer database.

* **The SuperID username must be a valid email address!** It is the same as the new username field on the associate record and in the Admin client.

* Credentials are **account-specific**: 1 SuperID user account + password can belong to 0 or more tenants.

* The password hash is unique for the person's SuperID account and stored in SuperID.

* The sign-in page will list all tenants the account has access to (if more than 1) and the user must select which tenant to sign in to.

## User admin

* Admin registers a new user in the Admin client and the user will get a link to sign in. (You can set a global preference to not send welcome emails, but it should only be used in combination with federated sign-in (IdP).)

* If the user attempts to sign in directly (not via link), they are sent to the IdP if set and otherwise they will get a code and need to validate their email address.

* Only an admin in the primary tenant can change the username and email address.

* Passwords can be reset by self-service or via email triggered by the admin. Only the user knows and sets their own human-readable password!

The SuperID sign-in service has 2 levels - basic and federated.

The **basic level** of the SuperID sign-in service uses a password to authenticate like the standard sign-in service. However, this centralized model doesn't store passwords in the CRM Online database. It actually uses SuperID as the identity provider.

SuperID supports using **3rd-party federated sign-in** services as an add-on. You can choose either Microsoft or Google to authenticate. This is sometimes referred to as **identity provider sign-in** or **SuperID with IdP**.

If the SuperID account is federated, the username must be the user principal name  (UPN) of the IdP (Microsoft or Google).

**Passwords and user accounts:**

| Model | Password granularity | Password type | Password storage | Password management | Authentication |
|-----------|-------------|-----------|-------------|-----------|-------------|-------------|
| Standard (before) | one-to-one | text string or key phrase | in the database of a specific tenant | admin client of the tenant | email address or username + password for 1 specific tenant |
| SuperID - basic | one-to-many | text string or key phrase | centrally | id.superoffice.com | SuperID user account |
| SuperID - federated | one-to-many | up to the identity provider | Microsoft or Google | identity provider | Microsoft or Google account |