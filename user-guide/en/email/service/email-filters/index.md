---
uid: help-en-email-filter
title: Email filters
description: Email filters
author: SuperOffice RnD
so.date: 06.29.2022
keywords: Settings and maintenance
so.topic: help
language: en
---

# Email filters

An email filter is a tool used to analyze the content of inbound email, and generate a request based on this content.

You can also add advanced rules for handling email from specific senders. Email filters are often used in connection with web forms that the company has published and that generate a fixed format email message that is imported into SuperOffice Service.

## Example

For example, you can define fixed expressions to extract information that a customer has submitted using the form. Based on a defined rule set, data from the form is entered in the customer database. The request generate from the email/form is then placed into a specific category and a request handler is selected. Then the request is closed and the customer receives a customized receipt based on a reply template.In other words, there are many options for automatic handling of inbound email.

Here are some examples related to inbound email from web forms:

* Email received from a web form generally has a default sender address. You can replace this address with the customer's own email address.

* You can compare the customer's phone number with information in the customer database and link the request to the correct customer on this basis.

* You can overwrite address data in the event of a change of address.

* You can send a receipt with tailored information if a customer wants more information about a specific product, and assign the request to the right subcategory and request handler.

## Columns in the list of filters

The **E-mail filters** tab contains a list of existing email filters. This list contains the following columns:

| Column | Description |
|---|---|
| Description | A description of the email filter. |
| Priority | The email filter's priority. Only one filter per email is enabled. If more than one filter contains search criteria that match an inbound email, the highest priority filter is enabled. |
| E-mail addresses | The addresses of the mailbox the filter applies to. |
| Search string | The search string that the email filter uses. |

## Properties for generated requests

* **Set owner**: If you check here, you can select which user will be assigned e-mails processed by this filter.

* **Set category**: If you check here and select a category, e-mail processed by this filter will end up in the specified category.

* **Set priority**: If you check here and select a priority, e-mail processed by this filter will be assigned the specified priority.

* **Set access level**: If you check here and select an access level from the list box, e-mail processed by this filter will be assigned the specified access level. If you select **External**, the generated request will be accessible in SuperOffice Customer Centre.

* **Set messages**: If you check here and select a reply template, the request message will be set up in accordance with the selected template, merged with all the fixed expressions that are found. You can use this to present a form, which is sent by e-mail, and is much tidier. This message will replace the original e-mail.

* **Close request**: If you check here, the request is closed immediately and assigned the status **Closed**.

* **Ignore From address**: If you check here, SuperOffice Service ignores the original sender address. The request will then not be linked to a contact unless other rules in the e-mail filter create a link to a contact.

* **Block e-mail**: If you check here, the e-mail is not imported into SuperOffice Service. It is added instead to the list in the **Blocked e-mail** tab.

* **Permanently delete e-mail**: If you check here, the e-mail is deleted permanently.

    > [!NOTE]
    > It is not possible to restore e-mails that have been permanently deleted.

* **Forward to**: If you check here and enter an e-mail address, the e-mail will be forwarded to this address.

* **Include debug information in the message**: If you check here, the message will include debug data that you can use to check that the e-mail filter is working correctly.

* **Mark e-mail as bounced**: If you check here, e-mail processed by this filter will be marked as bounced. This may be relevant for e-mails received from postmaster, mailer-daemon, etc.

## What would you like to do now?

* [Create email filters][1]
* [Delete email filters][2]

<!-- Referenced links -->
[1]: create-email-filter.md
[2]: delete-email-filter.md

<!-- Referenced images -->