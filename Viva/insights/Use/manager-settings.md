---

title: Manager settings for Viva Insights
description: Learn about the manager settings for Viva Insights in Teams and in Workplace Analytics and how administrators can set up and edit them for your organization
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Manager settings

>[!Important]
>Manager settings only control **Group insights** within **My team** in the Viva Insights app in Teams. To set up or opt in or out of the **My team** page in Teams, see [Admin tasks](myteam.md#admin-tasks).

As an admin for Microsoft Viva Insights or Workplace Analytics, you can set up and edit **Manager settings** to allow all measured people managers or a specified group of managers access to aggregated collaboration insights about their team.

Only managers whose team meets or exceeds the **Minimum team size** setting can access [Group insights](group-insights.md) within **My team** in Viva Insights in Teams. The other admin tasks required for Group insights access are the same as for access to My team. See [Admin tasks](myteam.md#admin-tasks) for details.

The size of the team counts the manager and all the employees who directly or indirectly report to that manager within the organization's reporting hierarchy. The following are based on the latest organizational (HR) data that's been successfully uploaded and processed for Viva Insights in Workplace Analytics:

* **Measured managers** - Managers who were assigned licenses in Workplace Analytics prior to October 2021 can see manager insights in Workplace Analytics. Managers who are assigned licenses starting October 2021, can see their team's insights through [Group insights](group-insights.md) within **My team** in Viva Insights in Teams.
* **Managers enabled** - Only managers who meet the minimum team size can view their team's insights.

![Manager settings.](../images/wpa/use/manager-settings.png)

* **Minimum team size** - You can set the minimum size of a team that a manager is allowed to view insights about and start plans for. The minimum size allowed is 10 (including the manager). This section also shows you how many measured managers currently have teams that are equal to or more than the minimum setting.
* **Insights** - You can select to allow all licensed managers access to aggregated collaboration insights about their teams. Or you can upload a .csv file that lists the email addresses for the managers you want to have access.

<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021. 
  * If you turn **Insights and plans** on, your organizational hierarchy file will also be used to power personal insights for managers in the [Insights add-in](../myanalytics/use/add-in.md), the [MyAnalytics dashboard](../myanalytics/use/dashboard-2.md), and other MyAnalytics surfaces. This file will complement hierarchy information from Azure AD. If a manager in your organization has team members who are listed in both Azure AD and Workplace Analytics, the system will default to using the Workplace Analytics data; otherwise it will use whichever source is available.
   
     Personal insights help managers improve their personal impact on and relationships with direct reports, and are powered exclusively by information from the manager's own Outlook mailbox. Learn more about personal insights for people managers in [Assistance for people managers](../myanalytics/overview/privacy-guide.md#assistance-for-people-managers). -->

## To configure manager settings

Only Viva Insights or Workplace Analytics admins can access **Manager settings**. Also, before managers can access Viva Insights in Teams or in Workplace Analytics, they must be assigned a license and have a team that meets or exceeds the **Minimum team size** setting.

1. In **Leader & manager settings** > **Manager settings**, select to change the switch **On** to allow managers with the minimum team size access to their team data in Viva Insights.
2. Select one of the following:

   * **All managers** - Allows all measured managers access.
   * **Select managers** (upload .csv) - Enables you to give specific managers access. You then need to:

      1. Create a .csv file that lists the email addresses for the select managers.
      2. Select **Upload .csv** to upload this list.

3. If you're allowing all managers access, continue to **Step 4**. If setting up access for select managers, select **Download currently enabled manual upload manager list .csv** to confirm which managers now have access. If an error occurs, such as an invalid email or an unlicensed manager, the .csv file will show the error for that manager.
4. In **Minimum team size**, you can change the minimum to a number more than 10 (the lowest allowed setting). This setting limits access to only those managers who have teams equal to or more than that number, which includes the manager in the team count.
5. Select **Save**.

>[!Note]
>Changes to these settings will apply after one hour.

## Related topics

* [Plans](../Tutorials/solutionsv2-intro.md)
* [Controls](settings.md)
