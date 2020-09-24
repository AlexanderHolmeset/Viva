---

title: MyAnalytics configuration for Office 365 administrators
description: Configuration options that Office 365 administrators can make for MyAnalytics users
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: Mya
---

# Configure MyAnalytics

**Role:** Office 365 admins

The steps in this topic describe how to configure MyAnalytics for the users in your organization. Note the following:

 * **Prerequisite:** Users have access to MyAnalytics only if they have licenses that include the MyAnalytics service plan, as described in [plans and environments for MyAnalytics](../Overview/plans-environments.md).

 * **Data privacy:** See the [MyAnalytics privacy guide](../Overview/Privacy-Guide.md) to understand how privacy is built into MyAnalytics and to learn what you can configure to address specific privacy requirements.

**To configure MyAnalytics:**

* [Assign licenses with a MyAnalytics service plan](#assign-licenses-with-a-myanalytics-service-plan)
* [Configure access at the tenant level](#configure-access-at-the-tenant-level) or [at the user level](#configure-access-at-the-user-level)

> [!Note] 
> When you set the defaults (at either the tenant or user level), users can individually override these settings. For example, if you keep the dashboard tenant setting as opt in, users can open the dashboard and opt themselves out. Similarly, if you opt out users with a user-level setting, those users can choose to opt back in. The exception is if a user's license with a MyAnalytics service plan expires, that user cannot opt in.

## Assign licenses with a MyAnalytics service plan

MyAnalytics is available to users who are assigned a license with a MyAnalytics service plan. For more details about which licenses have MyAnalytics service plans and when users get access to MyAnalytics elements after license assignment, see [plans and environments for MyAnalytics](../Overview/plans-environments.md).

For information on how to assign a license, see [Assign licenses to users in Office 365 for business](https://support.office.com/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc).

<!-- If you don't want a user to see any statistics from MyAnalytics, you can disable the MyAnalytics service plan for that user. -->

> [!Note]
> If you want to notify your organization before you assign licenses with a MyAnalytics service plan, you can use [this email template](MyAnalytics-announcement-2020-template.docx). You can download it, customize it with your company's information, and then email it to the new MyAnalytics participants. To learn more about adopting MyAnalytics, see [Adopt MyAnalytics](../Use/MyA-Adoption/adopt-myanalytics.md).  

## Configure access at the tenant level

You can configure access to MyAnalytics elements for all users in your organization.

### To enable access to the dashboard and digests

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure you're using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)

3. In the left pane, expand **Settings**, and then select **Services & add-ins**.
4. Under **Services & add-ins**, select **MyAnalytics**. This opens a page to configure access to MyAnalytics elements.

   ![Select visibility](../../images/mya/setup/assign-mya-access-new.png)

5. Select **Insights dashboard** to keep all MyAnalytics users in your organization opted _in_ for access to the MyAnalytics dashboard. Deselect **Insights dashboard** to opt users _out_ of access to the dashboard.

6. Select **Weekly insights** to keep all MyAnalytics users in your organization opted _in_ for access to the weekly [digest](../../myanalytics/use/email-digest-2.md) (and the MyAnalytics [welcome email](../../myanalytics/use/mya-welcome-email.md)). Deselect **Weekly insights email** to opt users _out_ of the weekly digest (and the MyAnalytics welcome email).  

7. Select **Insights Outlook add-in** to keep all MyAnalytics users in your organization opted in for access to the Insights Outlook add-in. Deselect it to opt users out of access to the Insights Outlook add-in.

> [!Note]
> After a new tenant is established, it might take up to 48 hours for this functionality to become available. 

<!-- REMOVING THIS SECTION PER HIMANI 12 NOV. 2019, BUT KEEPING IT AROUND (ALSO PER HIMANI) IN CASE WE NEED TO BRING IT BACK:

### To disable the add-in for a tenant

You can disable the Insights Outlook add-in for all licensed users in your organization or at the tenant level through the Exchange admin center.

> [!Note] 
> This procedure also removes [inline suggestions in Outlook](../use/mya-notifications.md). The removal of inline suggestions might take up to 26 hours.

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. In the left navigation pane, select **Exchange**. This opens the dashboard of the Exchange admin center. (If **Exchange** is not visible, first select **Show all** to see more admin centers and then select **Exchange**.)
3. In the dashboard, select **add-ins**.
4. In the list of add-ins, select **Insights**, and then select the **Edit** (pencil) icon.
5. In the **Edit add-in settings** dialog box, clear the **Make this add-in available to users in your organization** checkbox to disable the add-in, and then select **Save**.

-->

## Configure access at the user level

Configure MyAnalytics access for individual users in your organization. At this level, you can opt-out the user completely, which would turn off all MyAnalytics functionality for that user. However, the user can choose to opt back in. <!--To remove this choice from the user so that they cannot opt back in, you remove their MyAnalytics service plan. -->

You can configure MyAnalytics (change its default behavior) for users in your organization by setting the *PrivacyMode* parameter. For information about the values of PrivacyMode, see [User configuration settings](#user-configuration-settings).

You can set this parameter for one or many users:

* [Set MyAnalytics access for one user](#set-myanalytics-access-for-one-user)
* [Set MyAnalytics access for multiple users](#set-myanalytics-access-for-multiple-users)

### User configuration settings

PrivacyMode parameter  | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users</li><li>Dashboard is available</li><li>User can opt out</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users</li><li>Admins can opt out unlicensed users through the admin PowerShell </li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users</li><li> Dashboard is not available</li><li>User can opt in through the Feature settings menu</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul> |

> [!Important] 
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.

### Set MyAnalytics access for one user

Configure MyAnalytics access settings for a user with the following PowerShell cmdlet:

```powershell
Set-MyAnalyticsFeatureConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD)   |   --
PrivacyMode   |   Yes   | <ul><li>**Opt-out**: MyAnalytics won't use the user's data to compute derived statistics for other users. The user won't see statistics in MyAnalytics, but can choose to opt in from the Feature settings menu.</li><li>**Opt-in**: MyAnalytics uses the user's data to compute derived statistics for other users. The user can see statistics in MyAnalytics, but can choose to opt out from the Feature settings menu.</li></ul>|  Opt-in

> [!Important]
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.

Use Set-MyAnalyticsFeatureConfig to change the configuration settings of the user who is identified by the -Identity parameter. The following is a sample output of this cmdlet. It indicates that the user has been opted in and that all of that user's MyAnalytics features were turned off except the weekly digest:

    UserId  : \<username\>@\<domain><p>
    PrivacyMode : opt-in<p>
    IsDashboardEnabled : False<p>
    IsAddInEnabled  : False<p>
    IsWeeklyDigestEnabled : True

### Confirm MyAnalytics access for a user

Use the following to confirm whether a user has access to MyAnalytics (the value for PrivacyMode):

```powershell
Get-MyAnalyticsFeatureConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | - 

Get-MyAnalyticsFeatureConfig reveals the current configuration settings of the user who is identified by the -Identity parameter. The following is a sample output of this cmdlet. It indicates that the user is currently opted in and that they have all MyAnalytics features turned off except the weekly digest:

UserId  : \<username\>@\<domain><p>
PrivacyMode : opt-in<p>
IsDashboardEnabled : False<p>
IsAddInEnabled  : False<p>
IsWeeklyDigestEnabled : True

### Set MyAnalytics access for multiple users

Use the following steps in the [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2) to change access to MyAnalytics (the value of PrivacyMode) for multiple users by running a PowerShell script that iterates through the users, changing the value one user at a time.

1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field of the users you want to configure. For example:

   ```
   UserPrincipalName
   ClaudeL@contoso.onmicrosoft.com
   LynneB@contoso.onmicrosoft.com
   ShawnM@contoso.onmicrosoft.com
   ```

2. Specify the location of the input .csv file, the output .csv file, and the value of PrivacyMode that you want to set for each user:

   ```powershell
   $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2License..csv>"
   $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2License-Done..csv>"
   $privacyMode = "Opt-in"

   $users=Import-Csv $inFileName
   ForEach ($user in $users)
   {
   $user.Userprincipalname
   $upn=$user.UserPrincipalName

   Set-MyAnalyticsFeatureConfig –Identity $upn -PrivacyMode $privacyMode
   Get-MyAnalyticsFeatureConfig –Identity $upn | Export-Csv $outFileName
   }
   ```

3. Run the resulting commands at the Exchange Online PowerShell V2 module command prompt. For more information about the module, see [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).

This PowerShell script:

* Displays the user principal name for each user.
* Sets the specified privacy mode for each user.
* Creates a .csv file with all the users that were processed and shows their status.

<!--

[!INCLUDE [Configure user settings](../setup/configure-mya-user-settings.md)]  
## Related topics

[How users can opt out of MyAnalytics](../use/dashboard-2.md#can-i-opt-out-of-myanalytics)

[How users can remove the Insights add-in from Outlook](../use/add-in.md#to-remove-insights-add-in-from-outlook)
-->
