---
ROBOTS: NOINDEX, NOFOLLOW
title: Hybrid workforce experience dashboard
description: Learn how to understand how hybrid work affects employees differently through the Hybrid workforce experience Power BI dashboard
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: helayne
audience: Admin
---

# Hybrid workforce experience dashboard

*This experience is available only through private preview*

## Introduction

As leaders figure out their organization’s new working models, the Hybrid workforce experience Power BI dashboard helps them understand how hybrid work affects employees differently. The dashboard identifies opportunities to improve the experience of employees working in the following ways:

* Mostly onsite
* Mostly remote
* Onsite some days of the week and remote on others (hybrid)

This dashboard has six sections, which each address different facets of the employee experience that hybrid working models may impact. Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and **recommended actions**.  

<iframe title="Hybrid workforce experience - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiZTExZGI0ZDEtNjRjYS00YzRjLWE0OWQtZmFmOWVhZjQ5ZTJmIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run queries and populate the dashboard in Power BI, make sure you:

* Are assigned the role of [Analyst](/viva/insights/use/user-roles) in Workplace Analytics with Viva Insights

* Have installed the latest version of Power BI Desktop
  * If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then, download and install the latest version from [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab).

* Have the following attributes uploaded as part of your organizational data:
  * An attribute identifying the number of days someone works onsite (we recommend **OnsiteDays**). You might get this data in one of two ways—through a weekly update of onsite days, or by using a monthly update of onsite days to calculate the weekly number.
    * If an employee’s number of onsite days becomes available on a weekly basis (that is, values are between 0 and 5), make sure to upload this new value in weekly increments—in your data file, include a row with an **EffectiveDate** and **OnsiteDays** value per person per week.
    * If you’re using an employee’s number of onsite days per month to calculate their average weekly onsite days, make sure to round off the average weekly onsite days numbers to limit the number of possible values uploaded in the dashboard.
  * An attribute indicating whether someone is a manager (we recommend **SupervisorIndicator**)
  * An attribute indicating the person’s hire date (we recommend **HireDate**), which is required to be able to load the **New hire onboarding insights**. Without this attribute, however, the rest of the dashboard will still load.

You can add new attributes to your organizational data in Workplace Analytics at any time.
For more details on how to add new data for existing employees, review the documentation on [subsequent uploads](/viva/insights/setup/upload-organizational-data2).

## Set up the template

>[!NOTE]
> This dashboard is currently only available in English and only works with data generated from the English version of Workplace Analytics. Before completing the following steps, confirm that the browser language contains **en-us** in the app's URL, or change it to read: https://workplaceanalytics.office.com/en-us/Home.

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Query designer**.
2. In **Create** > **Other templates**, select **Hybrid workforce experience**, which takes you to required setup steps.
    :::image type="complex" source="../images/wpa/tutorials/hwfe-select-hwfe-cropped.png" alt-text="Screenshot of Other templates window in Workplace Analytics' Query designer; Hybrid workforce experience is highlighted" lightbox="../images/wpa/tutorials/hwfe-select-hwfe.png":::
       Screenshot that shows the "Other templates" window within Workplace Analytics' Query designer. On the left-hand pane, "Query designer" is highlighted beneath "Analyze." Beneath "Other templates," there are nine templates presented as cards. The last template card, "Hybrid workforce experience," is highlighted.  
    :::image-end:::
    In the second setup step, select **Set up** next to **Hybrid workforce experience** (if repeating this process per step 8 below, select **Strong and diverse ties**).
3. When prompted, select or confirm the options for **Group by**, **Time period**, and **Meeting exclusions**.
4. In **Select metrics**, keep the preselected metrics (these are required for the template to work).
5. In **Select filters**, select **Active only** for **Which measured employees do you want to include in your query results**? Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, refer to [Create a Person Query](/viva/insights/Tutorials/person-queries).
6. In **Organizational data**, add the attribute that specifies someone’s number of onsite work days (for example, **OnsiteDays**), the attribute that indicates whether someone is a manager (for example, **SupervisorIndicator**), and the HireDate. Add any other attributes you want to be able to use in the dashboard. For best performance, select no more than seven attributes.
7. Select **Run** (located in the upper right) to run the query, which can take between a few minutes and a few hours to complete.
8. When prompted, select to return to the **Query designer**. Repeat preceding steps 2-7, except this time, select the **Strong and diverse ties** query. Make the same selections that you did for the Hybrid workforce experience. Skip step 6; there's no need to include any organizational attributes in this Strong and diverse ties query.
9. When prompted, select to go to **Results**. After both queries successfully run, navigate to **Query designer > Results**. Select the download icon for the **Hybrid workforce experience** query results, select **PBI template**, and then select **OK** to download the template.

    :::image type="content" source="../images/wpa/tutorials/hwfe-download-pbi-template(1).png" alt-text="Screenshot of download icon and pop-up list; the icon and 'PBI template' are highlighted":::

1. Open the downloaded **Hybrid workforce experience** template.
1. If prompted to select a program, select **Power BI**.
1. When prompted by Power BI:
    1. In the Workplace Analytics **Query designer > Results**, select the link icon for each query, and select to copy the generated OData URL link.
    1. In Power BI, paste each copied link into its respective URL field.
    1. Map the attribute in your organizational data that specifies the number of days someone works onsite (for example, **OnsiteDays**).
    1. Map the attribute that identifies whether someone is a manager (for example, **SupervisorIndicator**).
    1. Map the **HireDate** attribute (if available).
    1. Set the **Minimum group size** for data aggregation within this dashboard's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    1. Select **Load** to import the query results into Power BI. Loading these large files might take between a few minutes and a few hours to complete.
    :::image type="complex" source="../images/wpa/tutorials/hwfe-edit-parameters.png" alt-text="Screenshot of Edit Parameters window in Power BI":::
       Screenshot that shows the "Edit Parameters" window within Power BI. Each part of the image is labeled with the sub-step above to which it corresponds, "b" - "f". The first two sections, "Hybrid work person query file path" and "Hybrid work person-to-person query file path," are highlighted and labeled "b." Beneath each section header is an editable field that contains a file path to a .csv file; the first field, for the Person query, contains a path to a HybridWorkforceExp.csv file and the second field, for the Person-to-person query, contains a path to a StrongAndDiverseTies.csv file. The next field is titled, "Number of onsite days," has a "c" label to its right, and its editable field contains the text, "OnsiteDays." The next field is titled, "SupervisorIndicator," has a "d" label to its right, and its editable field contains the text, "SupervisorIndicator." The second-to-last field is titled, "Hire date," has an "e" label to its right, and its editable field contains the text, "HireDate." The last field is titled, "Minimum group size," has an "f" label to its right, and its editable field contains "5" selected from a dropdown menu.  
    :::image-end:::

1. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. At this point, you’ve completed the setup process and can skip to [Customize the dashboard](#customize-the-dashboard).
1. If you're not signed into Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](/viva/insights/Tutorials/power-bi-templates#troubleshooting) for more details.

    :::image type="complex" source="../images/wpa/tutorials/hwfe-o-data-not-signed-in.png" alt-text="Screenshot of pop-up window in Power BI prompting users to sign in":::
       Screenshot that shows a pop-up window in Power BI, titled "OData feed." There is square icon beneath the window title; a URL to its right reads, "https://workplaceanalytics.office.com/205951...". In smaller font, a note underneath the URL reads, "You aren't signed in." Beneath the note, there is a Sign in button. The left-hand sidebar contains five section titles arranged vertically; "Organizational account" is selected. Save and Cancel buttons are in the bottom right of the window.
    :::image-end:::

1. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!IMPORTANT]
    > You'll need to sign in to Power BI with the same account you use to access Workplace Analytics.

16. Select **Connect** to prepare and load the data, which can take a few minutes to complete. After the data loads, charts appear in Power BI with insights about the hybrid workforce’s experience.

## Customize the dashboard

After the **Workforce experience** dashboard is set up and populated with Workplace Analytics data in Power BI, you’re prompted to map the following attribute values:

* **Mostly onsite** –  Select the number of onsite days that define the work mode of employees that work mostly onsite (that is, from the company’s main worksite).
* **Hybrid** – Select the number of onsite days that define the work mode of employees that work onsite some days during the week and remote on others.
* **Mostly remote** – Select the number of onsite days that define the work mode of employees that work mostly remote (that is, from home or some other location outside the company’s main worksite).
* **Individual contributor** – Select the attribute values that identify employees as individual contributors who do not manage people within your organization.
* **Manager indicator** – Select the attribute values that identify managers who manage people within your organization, like **Mgr** and **Mgr+**.

    :::image type="complex" source="../images/wpa/tutorials/hwfe-a-couple-of-questions_cropped.png" alt-text="Screenshot of pop-up window in Power BI prompting users to assign onsite days to attributes and values to Individual contributors and Managers":::
       Screenshot that shows a pop-up window in Power BI, titled "A couple of questions to get you started..." There are two sections; the first section is titled, "Select which of your onsite days values best map to the following 'work mode' definitions" and the second section is titled "Select which values identify individual contributors, managers and managers of managers," which is parenthetically defined as "Manager" with a plus icon--"Manager-plus." In the first section, there are three fields, and each contain a dropdown menu to their right: "Mostly onsite," which shows "5" in the dropdown menu, "Hybrid," which shows "1,2,3,4" in the dropdown menu, and "Mostly remote," which shows "0" in the dropdown menu. In the second section, there are two fields, and each also contain a dropdown menu to their right: "Individual contributors," which shows "IC" in the dropdown menu, and "Managers," which shows "Multiple selections" in the dropdown menu.
    :::image-end:::

After this initial prompt, you can then select **Settings** in the upper right of any page to view and change the following attribute values:

* **Select the time period for the dashboard** – Select the time period for which you want to view data in the dashboard.
* **Select an attribute to group data by** – Select the primary group-by attribute shown in all the report pages. You can change this attribute at any time and all reportages will show group values by the new attribute.
* **Select optional report filter** – Select the organizational attribute and values by which you want to filter employees in the dashboard.
* Exclusions – Use the check boxes to:
  * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats).
  * Exclude weeks that are likely holiday weeks.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, refer to [Power BI tips, FAQ, and troubleshooting](/viva/insights/Tutorials/power-bi-templates).

## Related topic

[View, download, and export query results](/viva/insights/use/view-download-and-export-query-results)