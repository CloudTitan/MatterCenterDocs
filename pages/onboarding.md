---
title: Onboarding on Matter Center 365
layout: page
---

Prerequisites:
1. Office 365 license for each user wanting to use Matter Center 365


## Granting consent

Matter Center 365 was built as application that extends Office 365 functionalities and enables users greater productivity. To enable this Matter Center 365 requires permissions to access clients Office 365 data in user delegated mode (application behaves as a user, each action is user triggered). In order for users of Matter Center 365 to grant permissions, Office 365 Tenant administrator must grant consent to Matter Center 365 application by visiting [Consent link](https://login.microsoftonline.com/common/oauth2/authorize?resource=https:%2F%2Fgraph.microsoft.com%2F&client_id=bed9d0a9-1843-4892-80ee-42d1980c9966&response_type=code&redirect_uri=https:%2F%2Fapp.mattercenter365.com%2FAuthentication%2FAuthorize&x-client-SKU=.NET&x-client-Ver=2.24.0.0&x-client-CPU=x64&x-client-OS=Microsoft+Windows+NT+6.2.9200.0&prompt=admin_consent) and granting permissions.

After logging in, the admin is prompted with following dialog containing list of all permissions required by Matter Center 365. By accepting this request admin authorizes Matter Center 365 application for all users in his tenant.

![]({{"/images/screenshots/PermissionGrant.PNG" | relative_url }})


## Provisioning Add-ins

In order to have Office Apps (Word, Excel, PowerPoint) and Outlook add-ins present for all users, tenant administrator has to add Matter Center 365 Manifest files in certain places on Office 365 Admin portal. Manifest file can be added either through url, or by uploading the manifest file by hand. Both approaches are  explained in following sections.


#### Note
Office 365 will take some time to provision add-ins to users. This means that add-ins will not appear immediately upon finishing the steps below.

### Outlook Add-in

1. Open Office 365 Admin panel. Expand Admin centers menu on the bottom and click `Exchange`.
2. Under `organization` open `add-ins`
3. Click `+` icon and choose either Add from url or Add from file.
    1. In case of url copy following url: [Manifest Url]({{"/manifest/OutlookAddIn.xml" | relative_url }})
    2. In case of file, upload the following file: [Manifest File]({{""/manifest/OutlookAddIn.xml" | relative_url }})
4. Double click on Matter Center 365 on the add-in list.
    1. Check `Make this add-in available to users in your organizationIf `
    2. Select `Optional, enabled by default`


### Office Add-in

1. Open Office 365 Admin panel. Expand Settings menu and click on `Services & add-ins` link.
2. Click `+ Upload Add-in`
    1. In case of url copy following url: [Manifest Url]({{"/manifest/OutlookAddIn.xml" | relative_url }})
    2. In case of file, upload the following file: [Manifest File]({{"/manifest/OutlookAddIn.xml" | relative_url }})
3. Side menu should open with add-in configuration:
    1. Set status to On
    2. Define who can access the addin. Under Who has access? either select Everyone or define groups for whom do you wish to enable the Office add-in.

![]({{"/images/screenshots/OfficeAddinConfiguration.PNG" | relative_url }})
