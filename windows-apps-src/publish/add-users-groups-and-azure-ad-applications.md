﻿---
author: jnHs
Description: You can add users, groups, and Azure AD applications to your Dev Center account.
title: Add users, groups, and Azure AD applications to your Dev Center account
ms.author: wdg-dev-content
ms.date: 07/17/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
---

# Add users, groups, and Azure AD applications to your Dev Center account

The [Manage users](manage-account-users.md) section of Dev Center lets you use Azure Active Directory to add users to your Dev Center account. Each user is assigned a role (or set of custom permissions) that defines their access to the account. You can also add [groups of users](#groups) and [Azure AD applications](#azure-ad-applications) to grant them access to your Dev Center account.

After users have been added to the account, you can [edit account details](#edit), change [roles and permissions](set-custom-permissions-for-account-users.md), or [remove users](#remove).

> [!IMPORTANT]
> In order to add users to your account, you must first [associate your Dev Center account with your organization's Azure Active Directory tenant](associate-azure-ad-with-dev-center.md). 

When adding users, keep the following considerations in mind. (These apply to groups and Azure AD applications as well as individual users.)

-   All Dev Center users must have an active account in your organization's directory. Creating a new user in Dev Center will also create an account for that user in your organization's Azure AD tenant.
-   [Making changes](#edit) to a user's name in Dev Center will make the same changes in your organization's Azure AD tenant.
-   When adding users, you will need to specify their access to Dev Center account by assigning them a [role or set of custom permissions](set-custom-permissions-for-account-users.md). 

> [!NOTE]
> If your organization uses [directory integration](http://go.microsoft.com/fwlink/p/?LinkID=724033) to sync the on-premises directory service with your Azure AD, you won't be able to create new users, groups, or Azure AD applications in Dev Center. You (or another admin in your on-premises directory) will need to create them directly in the on-premises directory before you'll be able to see and add them in Dev Center.


<span id="users" />
## Add users to your Dev Center account

You can add individual users to your Dev Center account in any of the following ways:
-   Add users who already exist in your organization's directory
-   Create a new user to add to both your organization's directory and your Dev Center account
-   Add existing users who are not currently in your organization's directory


<span id="from-directory" />
### Add users from your organization's directory

1.  From the **Manage users** page, click **Add users**.
2.  Select one or more users from the list that appears. You can use the search box to search for specific users.
    > [!TIP]
    > If you select more than one user to add to your Dev Center account, you must assign them the same role or set of custom permissions. To add multiple users with different roles/permissions, repeat the steps below for each role or set of custom permissions.

3.  When you are finished selecting users, click **Add selected**.
4.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the selected user(s).
5.  Click **Save**.


<span id="new-user" />
### Create a new user account in your organization's directory and add them to your Dev Center account

If you want to grant Dev Center access to a brand new account in your Azure AD tenant, you can create one in the **Manage users** section by clicking **New user**. 

> [!IMPORTANT]
> You must be signed in with a global administrator account in your Azure AD tenant in order to add new users to the directory.

If you want the new user to have a [global administrator account](http://go.microsoft.com/fwlink/p/?LinkId=746654) in your organization's directory, check the box labeled **Make this user a Global administrator in your Azure AD, with full control over all directory resources**. This will give the user full access to all administrative features in your company's Azure AD. They'll be able to add and manage users in your organization's directory (though not in Dev Center, unless you grant the account the appropriate [role/permissions](set-custom-permissions-for-account-users.md)). If you check this box, you'll need to provide a **Password recovery email** for the user.

1.  From the **Manage users** page, click **Add users**.
2.  On the next page, click **New user**.
3.  Ensure that the **Add to Azure AD** radio button is selected to create a new account in your organization's directory and add that user to your Dev Center account. 
4.  Enter the first name, last name, and username for the new user.
5.  Enter an email that the user can use if they need to recover their password. This is only required if you checked the box to **Make this user a Global administrator in your Azure AD**.
6.  In the **Group membership** section, select any groups to which you want the new user to belong.
7.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the user.
8.  Click **Save**.
9.  On the confirmation page, you'll see login info for the new user, including a temporary password. Be sure to note this info and provide it to the new user, as you won't be able to access the temporary password after you leave this page.


<span id="email" />
### Add a user from outside of your Azure AD tenant to your Dev Center account and your directory

To invite users who aren't currently part of your Azure AD tenant to your account, follow the steps below. The users will get an email invitation to join their account, and a new [guest user](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b) account will be created for them in your Azure AD tenant. 

1.  From the **Manage users** page, click **Add users**.
2.  On the next page, click **New user**.
3.  Select the **Invite users by email** radio button.
3.  Enter one or more email addresses (up to ten), separated by commas or semicolons.
4.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the user.
6.  Click **Save**.

The users you've invited will get an email with an invitation to access your Dev Center account. Each user will need to accept their invitation before they can access your account.

If you need to resend an invitation, find the user on your **Manage users** page and select their email address (or the text that says **Invitation pending**) to edit the account. Then, at the bottom of the page, click **Resend invitation**.


### Changing a user's directory password

If you need to change a password for a user account that you've added to your Dev Center account, you can do so in the **Manage users** section. Note that this will change the user's password in your Azure AD tenant, along with the password they use to access Dev Center. 

If you've provided a **Password recovery email** when creating the user account, they will be able to reset their own password. You can also update a user's password by following the steps below.

1.  From the **Manage users** page, click the name of the user account that you want to edit.
2.  Click the **Reset password** button at the bottom of the page.
3.  A confirmation page will appear showing the login info for the user, including a temporary password.
    > [!IMPORTANT]
    >  Be sure to print or copy this info and provide it to the user, as you won't be able to access the temporary password after you leave this page.

<span id="groups" />
## Add groups to your Dev Center account

You can add a group from your organization's directory to your Dev Center account. When you do so, every user who is a member of that group will be able to access it, with the permissions associated with the group's assigned role.

### Add groups from your organization's directory

1.  From the **Manage users** page, click **Add groups**.
2.  Select one or more groups from the list that appears. You can use the search box to search for specific groups.
    > [!TIP]
    > If you select more than one group to add to your Dev Center account, you must assign them the same role or set of custom permissions. To add multiple groups with different roles/permissions, repeat the steps below for each role or set of custom permissions.

3.  When you are finished selecting groups, click **Add selected**.
4.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the selected group(s). All members of the group will be able to access your Dev Center account with the permissions you apply to the group, regardless of the roles/permissions associated with their individual account.
5.  Click **Save**.


### Create a new group account in your organization's directory and add it to your Dev Center account

If you want to grant Dev Center access to a brand new group, you can create a new group in the **Manage users** section. Note that the new group will be created in your organization's directory, not just in your Dev Center account.

1.  From the **Manage users** page, click **Add groups**.
2.  On the next page, click **New group**.
3.  Enter the display name for the new group.
4.  Specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the group. All members of the group will be able to access your Dev Center account with the permissions you apply to the group, regardless of the roles/permissions associated with their individual account.
5.  Select the user(s) to assign to the new group from the list that appears. You can use the search box to search for specific users.
6.  When you are finished selecting users, click **Add selected** to add them to the new group.
7.  Click **Save**.


<span id="azure-ad-applications" />
## Add Azure AD applications to your Dev Center account

You can allow applications or services that are part of your organization's Azure AD to access your Dev Center account.

### Add Azure AD applications from your organization's directory

1.  From the **Manage users** page, click **Add Azure AD applications**.
2.  Select one or more Azure AD applications from the list that appears. You can use the search box to search for specific Azure AD applications.
    > [!TIP]
    > If you select more than one Azure AD application to add to your Dev Center account, you must assign them the same role or set of custom permissions. To add multiple Azure AD applications with different roles/permissions, repeat the steps below for each role or set of custom permissions.

3.  When you are finished selecting Azure AD applications, click **Add selected**.
4.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the selected Azure AD application(s).
5.  Click **Save**.


### Create a new Azure AD application account in your organization's directory and add it to your Dev Center account

If you want to grant Dev Center access to a brand new Azure AD application account, you can create one in the **Manage users** section. Note that this will create a new account in your organization's directory, not just in your Dev Center account.

> [!TIP]
> If you are primarily using this Azure AD application for Dev Center authentication, and don't need users to access it directly, you can enter any valid address for the **Reply URL** and **App ID URI**, as long as those values are not used by any other Azure AD application in your directory.

1.  From the **Manage users** page, click **Add Azure AD applications**.
2.  On the next page, click **New Azure AD application**.
3.  Enter the **Reply URL** for the new Azure AD application. This is the URL where users can sign in and use your Azure AD application (sometimes also known as the App URL or Sign-On URL). The **Reply URL** can't be longer than 256 characters.
4.  Enter the **App ID URI** for the new Azure AD application. This is a logical identifier for the Azure AD application that is presented when it sends a single sign-on request to Azure AD. Note that the **App ID URI** must be unique for each Azure AD application in your directory, and it can't be longer than 256 characters.
5.  In the **Roles** section, specify the [role(s) or customized permissions](set-custom-permissions-for-account-users.md) for the Azure AD application.
6.  Click **Save**.

After you add or create an Azure AD application, you can return to the **Manage users** section and click the application name to review settings for the application, including the Tenant ID, Client ID, Reply URL, and App ID URI.

> [!NOTE]
> If you intend to use the REST APIs provided by the [Windows Store services](../monetize/using-windows-store-services.md), you will need the Tenant ID and Client ID values shown on this page to obtain an Azure AD access token that you can use to authenticate the calls to services.   

<span id="manage-keys" />
### Manage keys for an Azure AD application

If your Azure AD application reads and writes data in Microsoft Azure AD, it will need a key. You can create keys for an Azure AD application by editing its info in Dev Center. You can also remove keys that are no longer needed.

1.  From the **Manage users** page, click the name of the Azure AD application.
    > [!TIP]
    > When you click the name of the Azure AD application, you'll see all of the active keys for the Azure AD application, including the date on which the key was created and when it will expire. To remove a key that is no longer needed, click **Remove**.

2.  To add a new key, click **Add new key**.
3.  You will see a screen showing the **Client ID** and **Key** values.
    > [!IMPORTANT]
    > Be sure to print or copy this info, as you won't be able to access it again after you leave this page.

4.  If you want to create more keys, click **Add another key**.

<span id="edit" />
## Edit a user, group, or Azure AD application

After you've added users, groups, and/or Azure AD applications to your Dev Center account, you can make changes to their account info. 

> [!IMPORTANT]
> Changes made to roles or permissions will only affect Dev Center access. All other changes (such as changing a user's name or group membership, or the Reply URL and App ID URI for an Azure AD application) will be reflected in your organization's Azure AD tenant as well as in your Dev Center account. 

USER
1.  From the **Manage users** page, click the name of the user, group, or Azure AD application account that you want to edit.
2.  Make your desired changes. The items you can edit are as follows:
    -   For a **user**, you can edit the user's first name, last name, or username. You can also select or deselect groups in the **Group membership** section to update their group membership.
    -   For a **group**, you can edit the name of the group. (To update group membership, edit the users you want to add or remove from the group and make changes to the **Group membership** section.)
    -   For an **Azure AD application**, you can enter new values for the **Reply URL** or **App ID URI**.
    Remember that these changes will be made in your organization's directory as well as in your Dev Center account.
3.  For changes related to Dev Center access, select or deselect the role(s) that you want to apply, or select **Customize permissions** and make the desired changes. These changes only impact Dev Center access and will not change any permissions within your organization's Azure AD tenant.
3.  Click **Save**.


## View history for account users

As an account owner, you can view the detailed browsing history for any additional users you’ve added to the account.

On the **Manage users** page, click the link shown under **Last activity** for the user whose browsing history you’d like to review. You'll be able to view the URLs for all pages that the user visited in the last 30 days.

<span id="remove" />
## Remove users, groups, and Azure AD applications

To remove a user, group, or Azure AD application from your Dev Center account, click the **Remove** link that appears by their name on the **Manage users** page. After confirming that you want to remove it, that user, group, or Azure AD application will no longer be able to access to your Dev Center account (unless you add it again later).

> [!IMPORTANT] 
> Removing a user, group, or Azure AD application means that it will no longer have access to your Dev Center account. It does **not** delete the user, group, or Azure AD application from your organization's directory.

 

