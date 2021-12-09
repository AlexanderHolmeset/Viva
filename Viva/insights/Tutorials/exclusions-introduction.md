---

title: Introduction to Analyst settings in Workplace Analytics
description: Introduction to Analyst settings in Microsoft Viva Insights in Workplace Analytics
author: madehmer
ms.author: v-mideh
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

# Analyst settings

As an analyst of Microsoft Viva Insights in Workplace Analytics, you use Analyst settings to set up meeting and attendee exclusion rules for data analysis purposes.

You can use Query designer in Workplace Analytics to measure work-related calendar collaboration. For this type of analysis, you want to make sure the queried data is applicable. That is, you want to include only participation in meetings that reflect actual work-related collaboration and exclude unrelated events from the data.

You can exclude events with one of the following exclusion types:

* [Meeting exclusions](meeting-exclusions-intro.md) - Exclude types of meetings from analysis (such as all-day training meetings) where their inclusion might skew query results.

* [Attendee exclusions](attendee-exclusion-rules.md) - Use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default. By adding an attendee exclusion, you can explicitly exclude them. In this way, creating attendee exclusions lets you effectively redefine "meeting attendance."

**Owners** – Viva Insights Analysts have full access and limited Analysts have read-only access to these settings. For details, see [Assign roles](../setup/assign-roles-to-wpa-admins.md).

![Analyst exclusion settings](../images/WpA/Tutorials/analyst-exclusion-settings.png)

## Notes

* **Exclusion types are independent** &ndash; These two exclusion types are not mutually exclusive. As you define a query, you can select exclusions of both types. This lets you exclude data about particular types of meetings (such as long or large meetings) while you, independently, also exclude attendee data for those who responded as "Tentative" or didn't respond to meeting invitations.

* **Rules are applied only in Explore and in Query designer** &ndash; Analysts in your organization might have created meeting or attendee exclusion rules during the setup of Workplace Analytics. After these rules are created, they are applied only in the [Explore](../use/explore-intro.md) page dashboards and in [queries](query-basics.md) (see Q1/A1 in [Application of meeting exclusion rules](meeting-exclusion-concept.md#application-of-meeting-exclusion-rules)). Exclusion rules are _not_ applied to the data shown in the **Data sources** pages, including on the **Office 365 data** page.

## Related topics

* [Controls](../Use/settings.md)
* [Data sources](../Use/data-sourcesv2.md)
