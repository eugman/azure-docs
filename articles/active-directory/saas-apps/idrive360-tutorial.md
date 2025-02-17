---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with IDrive360 | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and IDrive360.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 06/18/2021
ms.author: jeedes

---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with IDrive360

In this tutorial, you'll learn how to integrate IDrive360 with Azure Active Directory (Azure AD). When you integrate IDrive360 with Azure AD, you can:

* Control in Azure AD who has access to IDrive360.
* Enable your users to be automatically signed-in to IDrive360 with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* IDrive360 single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* IDrive360 supports **SP and IDP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add IDrive360 from the gallery

To configure the integration of IDrive360 into Azure AD, you need to add IDrive360 from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **IDrive360** in the search box.
1. Select **IDrive360** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for IDrive360

Configure and test Azure AD SSO with IDrive360 using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in IDrive360.

To configure and test Azure AD SSO with IDrive360, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure IDrive360 SSO](#configure-idrive360-sso)** - to configure the single sign-on settings on application side.
    1. **[Create IDrive360 test user](#create-idrive360-test-user)** - to have a counterpart of B.Simon in IDrive360 that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **IDrive360** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, the user does not have to perform any step as the app is already pre-integrated with Azure.

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type the URL:
    `https://www.idrive360.com/enterprise/sso`

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (PEM)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificate-base64-download.png)

1. On the **Set up IDrive360** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to IDrive360.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **IDrive360**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure IDrive360 SSO

1. Log in to your IDrive360 company site as an administrator.

2. Go to **Settings** > **Single Sign-on(SSO)** and perform the following steps.

    ![Single Sign-on](./media/idrive360-tutorial/settings.png "Single Sign-on")

    a. In the **SSO Name** textbox, type a valid name.
    
    b. In the **Issuer URL** textbox, paste the **Azure AD Identifier** value which you have copied from the Azure portal.

    c. In the **SSO Endpoint** textbox, paste the **Login URL** value which you have copied from the Azure portal.

    d. Click on **Upload Certificate** to upload the **Certificate (PEM)**, which you have downloaded from Azure portal.

    e. Click **Configure Single Sign-On**.

### Create IDrive360 test user

1. In a different web browser window, sign in to your IDrive360 company site as an administrator.

2. Navigate to the **Users** tab and click **Add User**.

    ![Users](./media/idrive360-tutorial/add-user.png "Users")

3. In the **Create new user(s)** section, perform the following steps.

    ![Create Users](./media/idrive360-tutorial/new-user.png "Create Users")
     
    a. Enter valid **Email Address** in the **Email** textbox.

    b. Click **Create**.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to IDrive360 Sign on URL where you can initiate the login flow.  

* Go to IDrive360 Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the IDrive360 for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the IDrive360 tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the IDrive360 for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure IDrive360 you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
