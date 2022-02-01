---
ROBOTS: NOINDEX,NOFOLLOW
title: Employee experience dashboard
description: Use the Employee experience dashboard in Power BI to visualize predefined data from Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium
ms.collection: m365initiative-viva-insights 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Employee experience

*This experience is only available through private preview*

As employees shift to remote work and to digital only collaboration, Microsoft Viva Insights can help you stay on track and make data-driven decisions that can help your employees do their best work.

The Employee experience dashboard in Power BI directionally highlights where a shift to remote work might have the largest impacts, offering a measurable starting point for helping leaders understand where they might use tools and processes to support and sustain new ways of working.

You can use this dashboard to visualize and explore your company’s collaboration activity in Microsoft Teams and Outlook and get ideas about how to help your organization be successful moving forward. 

The dashboard includes the following reports:

* **Protecting personal time** - Shows the percentage of employees who are successfully protecting their personal time by limiting their after-hours work to less than five hours each week. As digital collaboration becomes our new norm, it’s important to establish communication guidelines and boundaries to encourage employees to balance work and life and maintain good wellbeing.
* **Connecting in small groups** – Shows how much time employees spend interacting at least one hour each week with eight or fewer people to encourage small-group collaboration where most have a voice in the activity.
* **Finding time to focus** - Measures how much uninterrupted focus time your employees get during the workweek, which are one- to two-hour blocks of time with no collaboration activity. People need this valuable time to complete challenging work, think creatively, and generate new ideas.
* **Getting manager coaching** - Measure how much 1:1 time managers spend with their employees on average each month. Research shows that time spent 1:1 with your manager helps keep employees engaged and improves their job performance and career development.
* **Effective meetings** - Shows the percentage of employees who spend most of their time in short or focused meetings, which are less than one hour long with two to eight participants. Research shows short and targeted meetings are more inclusive with higher participation where decisions get made and work gets done.

![Power BI My organization template.](../Images/WpA/Tutorials/pbi-myorg.png)

Each report also includes the following details:

* **How we measure this** - Near the top of each report, you can select "How we measure this" to see what metrics were used to calculate the data and insights provided.
* **Top tools and suggestions** - In the blue area at the top right of each report, you'll see a few suggestions and tool tips that can help support the insights and analysis shown on the page.
* **Supporting articles** - To the right of "Current State," you'll see links to articles about why this analysis matters based on industry research and other businesses experience.
* **Go deeper** - Shows other available reports or options that you can use for more advanced and focused analysis relating to the data shown.
* **Supporting insights** - This section shows the top insights that are important to focus on based on the analysis shown. For example, for Protecting personal time, you might see insights about what activities drive most of your employees' after-hours work and how many hours they spend collaborating.

The following is an example of what you'll see in the Protecting personal time report:

![Protecting personal time report.](../Images/WpA/Tutorials/pbi-ppt-report.png)

To populate the dashboard in Power BI, you must set up the **Employee experience** template in Workplace Analytics for Viva Insights. The results will refresh your downloaded Power BI dashboard on a weekly basis.
<!--
## Demonstration

This uses sample data that is only representative of the dashboard and might not be exactly what you see in a live dashboard specific to your organization's unique data.

[Employee experience in Power BI demo](https://msit.powerbi.com/groups/me/reports/a46f5da2-58ba-467d-b1e8-68541ab302ea/ReportSection047f79d6110db8b7d45b?ctid=72f988bf-86f1-41af-91ab-2d7cd011db47&bookmarkGuid=Bookmarkcd33e1e642e6511e8d55) -->

## Prerequisites  

Before you can run the results and populate the dashboard in Power BI, you must:

* Be assigned [Insights Business Leader role](../use/user-roles.md).
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version.
Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

>[!Note]
>This dashboard is currently only available in English.

1. In **Query designer** > **Results**, select the **Download** icon for the **Employee experience** results, select **PBI template**, and then select **OK** to download the template.
2. Open the downloaded **Employee experience template**.
3. If prompted to select a program, select **Power BI**.
4. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. See [Troubleshooting](../tutorials/power-bi-templates.md#troubleshooting) for more details.

    ![Power BI sign in.](../Images/WpA/Tutorials/pbi-sign-in.png)

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

5. In Power BI Desktop, select Publish on the ribbon and then, sign in with the same email address you use for Microsoft Viva.
6. Follow the online instructions to view these reports in your Power BI workspace.

## Achieved or At Risk KPIs

Because Viva Insights respects user privacy, the Employee experience reports in Power BI do not show information about individual recipients and when necessary to protect privacy, it reports approximated values only. Groups with less than 10 employees are not shown in the reports. See [De-identification of personal data in Viva Insights](../privacy/de-identify-data.md) for details.

The following lists the minimum and maximum percentage range for the value thresholds that are used to categorize employees as Achieved or as compared to At Risk, which fall outside of these ranges.

Number of employees in a group | Value threshold range for Achieved
--------------| ------------
10 | 25 to 75 percent
11 to 20 | 10 to 90 percent
21 or more | 5 to 95 percent

For more information, see [Differential privacy in Viva Insights](../privacy/differential-privacy.md).  

## Organizational data

After the dashboard is set up and populated with data in Power BI, as a first step, confirm the date range and number of measured employees that's shown at the top of each page is what you expected for this analysis.

>[!Important]
>As new data is processed on a weekly basis, select **On** for **Keep your data up to date** in the **Scheduled refresh** section in Power BI if you want the report data to refresh in Power BI each week. For details, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh#scheduled-refresh).

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
