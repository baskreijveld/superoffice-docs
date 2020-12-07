---
title: office_365_document_integration       
description:                    
author: {github-id}             # Your GitHub alias.
keywords:
---

# About Office365 Document Integration

The Office365 Integration app integrates the Office365 SharePoint’s document management features so that you can create, store, and find your documents within SuperOffice, and enjoy the benefits of both SuperOffice and Office365 services all in one place.

Simply sign in to SuperOffice using your Office365 login details and then open, edit and store documents in Office365 SharePoint directly from SuperOffice.

**Note:** Microsoft have changed their product name for Office 365 to Microsoft 365.

![x][1]

![x][2]

![imageokq0f.png][3]

Read more details in our App Store: [Office365-integration][4]

If you do not require Office365 SharePoint’s document management features, and only wish for using Office365 for login purposes (ie. federated login or Multi-factor authentication (MFA/2FA)) you don't need this document integration.

Read more here: [SuperOffice identity management][5]

## Integration overview

This section outlines how the integration works and what components are required and interacting.

### Description of integration

Integrating SuperOffice CRM Online against Microsoft Office365 enables the following functionality:

* Using Microsoft Office365's Office Online capabilities for viewing, create, and edit files on the go (if file-type is supported by Microsoft Office365 SharePoint).
* Signing in to SuperOffice CRM Online with a Microsoft Office365-account.
* Using Microsoft Office365 SharePoint to store documents and templates in the document archive.
* Using Microsoft Office365 SharePoint to edit documents in the document-archive (if file-type is supported by Microsoft Office365 SharePoint).

Read more about the [technical description in this article](../cloud-document-integrations.md).

### Component overview

The integration consists of these main components:

* SuperOffice CRM Online
* SuperOffice Federation Gateway (http://superid.superoffice.com/)
* Microsoft Office365 subscription
* Microsoft Office365 SharePoint
* SuperOffice SharePoint App ('SharePoint add-in') (our app acts as an “Add-in” iSharePoint to be able to upload and download files in the cloud, and to authenticate users):

The authorization process will grant rights to an app registered with Microsoft Office36SharePoint called “SuperOffice SharePoint App“. The SuperOffice Federation Gateway which handles secure communication between SuperOffice SharePoint App located in Microsoft Office365 SharePoint, SuperOffice Online, and other parties (like SuperOffice Mail Link).

**Step 1** is needed for setting up SharePoint to be able to use SharePoint’s document management features so that you can create, store, and find your documents within SuperOffice, and enjoy the benefits of both SuperOffice and Office365 services all in one place. The site collection created within this step will also be used for adding the SuperOffice SharePoint app.  

* If this is not a service you plan to use - you may skip step 1.7 ("template" folders and read access of root folder is enough)

**Step 2** is needed for creating new blank documents, spreadsheets, and presentations iSuperOffice CRM Admin's "Add template" -> "Create a new template" (from a SharePoint template).  

* If this is not a service you plan to use - you may skip it, and skip the SharePoint settings to "allow user to run custom scripts" - since you do not need to create new content types.

**Step 3** is needed for authentication of users and is the basis for enabling the other services.

**Step 4** is needed for enabling your SuperOffice tenant to store templates and documents in SharePoint

<!-- Referenced links -->
[1]: https://online.superoffice.com/AppStore/Image?imageId=28&applicationId=16
[2]: https://online.superoffice.com/AppStore/Image?imageId=29&applicationId=16
[3]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imageokq0f.png
[4]: https://online.superoffice.com/AppStore/superoffice-as/office-365-integration
[5]: https://community.superoffice.com/en/technical/documentation/identity-management/overview/