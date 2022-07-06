---
uid: help-en-customers-viewcompany-listinvoicescontact
title: customers viewCompany listInvoicesContact
description: customers viewCompany listInvoicesContact
author: SuperOffice RnD
so.date: 06.29.2022
keywords: Service
so.topic: help
language: en
---

# View invoice data for companies

When processing requests, you have the option of registering invoice data as you proceed (see [Invoice information](../topics/ticket.newTicket.md#InvoiceInformation)). When the request is closed, the customer can be invoiced for the work performed.

> [!NOTE]
> The invoice feature is only available if you have registered invoice types and have the required feature toggle. See [Invoice types](../topics/admin.listInvoiceTypes.md).

To view invoice information that has been registered for a specific company, do as follows:

1. Open the **Company** screen as described under [View companies](viewCompany.md).

2. Click the ![icon][img1] **Actions** button and select **Invoices**. The **Invoices for ...** screen appears. This contains both requests that include messages with invoiceable hours, and registered invoice items, in chronological order. Note in particular these columns:
    * **Credit**: Shows the total amount for invoicing.
    * **Debit** Shows the total amount invoiced.
    * **Balance**: Shows the running balance, i.e. the difference between **Credit** and **Debit**.
3. If you are sending an invoice out to the company, it is easier to keep an overview in SuperOffice Service if you add an invoice item at the same time. <!-- Fix reuse ID=a1 -->

    [!include[How to add invoice item](../../includes/howto-add-invoice-to-request.md)]

4. Click **Return to company** to go back to the **View company** screen.

<!-- Referenced links -->
[1]:

<!-- Referenced images -->
[img1]: ../../../../media/icons/btn-menu.png