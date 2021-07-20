---

title: Organizational network analysis (ONA) person-to-person queries 
description: Describes how to use Organizational network analysis (ONA) person-to-person queries in Workplace Analytics to determine the metrics that measure ties between individuals in your organization
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
manager: scott.ruble
audience: Admin
ms.prod: wpa
---

# Organizational network analysis person-to-person queries

Successful employees and teams use their networks to get work done effectively. Measuring network attributes tells you what network resources employees can access. Network size is just one attribute of a collaborative network. Network connections have other qualities that tell us more about the type of working relationship and what benefit it might present to the employee and team.

You can use the Organizational network analysis (ONA) queries to qualify a network connection between two people as a **strong tie**, a **diverse tie**, or neither.

A generic network tie is defined liberally: two people who've shared at least two [meaningful interactions](../use/glossary.md#meaningful-interaction-define) in the last four weeks.

Some network connections represent significantly more close collaboration than the generic minimum of just two meaningful interactions. When a network connection represents significantly more close collaboration time, Workplace Analytics will classify it as either a **strong tie** or as a **diverse tie**.

The difference between strong ties and diverse ties is determined by how many other network connections the two individuals have in common.

If the two people have **many** network connections in common, it is considered a **strong tie**. Strong ties typically indicate shared membership in a workgroup or team. Groups of employees with many strong ties often represent highly cohesive units.

If the two people have **few** network connections in common, it is considered a **diverse tie**. Although the two people work closely with each other, they do not typically operate in the same circles. Groups of employees with many diverse ties often represent teams with high innovative potential, as they are exposed to lots of information outside of their shared context.

The article will walk you through a query that will return strong and diverse tie scores. (See the following section, [Run a query to determine strong ties and diverse ties](#run-a-query-to-determine-strong-ties-and-diverse-ties).)

## Run a query to determine strong ties and diverse ties

You can use the tie metrics in ONA person-to-person queries; in this example procedure, you will query for strong and diverse tie scores.

**Role** - Analyst

1. In Workplace Analytics, select **Analyze** > **Query designer**, and then select **Get started** under **Queries**.

2. Select **Network: Person-to-person**.

3. Select and change **Enter query name here** to a name, and then, optionally, enter a description for the query.

4. For **Group by**, select a time-grouping option: **Month** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose.

    >[!Note]
    >Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with an ONA query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected.

5. If you want the query to run repeatedly, on a regular schedule, select **Auto-refresh**. (For more information, see [Auto-refresh option for queries](query-auto-refresh.md).)

6. Under **Select network boundary conditions**, define a filter to select the measured employees that you want to analyze in this query. For example, you can use the filters of this step to narrow the scope to a division or a group. If you skip this (optional) step, all measured employees will remain eligible for analysis.

    **More information about this option:** If you run this query on the entire company, the results will be based on all collaborations across the company. If this is your goal, you can retain the default search range, which is unlimited. But your goal might be to understand connectivity for a specific group of people, based on collaboration happening exclusively within that group. In this case, limit the query to search only within a particular division or group.

<!-- REMOVED (FOR NOW) PER SANJAY, 19 MAY 2021
7. Under **Select collaboration types**, specify the types of collaboration activities that you want to include in your analysis. Your choices are **Emails and meetings**, **Teams instant messages**, and **Teams calls**.

    **More information about this option:** As the nature of the workplace evolves, different ways to collaborate gain or lose popularity, doing so at different rates among different populations. Some people and organizations are more formal in nature -- for example, a legal division or HR -- and they might invariably use email. They might also tend to message more recipients at once, for which they might prefer email. Other people who have a less traditional, more casual, or more personal outlook might prefer Teams IMs or calls.

    Analysts who study this communication can reach different inferences based on formal or informal communication. Depending on the types of change they want to make in the company, they might want to focus the analysis on one group of employees or the other. -->

7. Under **Select metrics**, select **Strong and Diverse tie scores**.

8. Under **Select filters**, select the groups of people for whom you want to see results. This section offers two optional filters, one for selecting "tie-origin" employees, and the other for selecting "tie-destination" employees. <!-- For more information, see [Select filters](#select-filters). REMOVED THAT SECTION 19 MAY 2021 -->

9. Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.

10. Select **Run**. The query takes a few minutes to complete.

11. In **Query designer** > **Results**, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

>[!Note]
>You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA person-to-person query output

The query results show the quality of the relationship between two specific (but de-identified) people. Each row shows the information for a pair of people between whom a tie exists, or existed, over the time period of the query.

The following columns appear, from left to right, in the query results for ONA person-to-person queries:

### The first two columns identify the initiator of the tie

![first columns -- A and B](../images/wpa/tutorials/columns-a-b.png)

_Query results example: Columns A and B_

The column names for these attributes are organizational attribute names with the prefix _TieOrigin__. These first two columns appear automatically:

* TieOrigin_[**PersonId**](../setup/prepare-organizational-data.md#personid-define) - A de-identified ID number for the person represented in that data row. You do not select this column as you build a query; it appears automatically.  
* TieOrigin_[**GroupId**](#groupid-define) - A de-identified ID number of the group in the organization to which the person belongs. This column can help you discover Strong ties in a team to understand how cohesive it is and also discover Diverse ties in a team to understand whether there are opportunities for novel information to flow into the team. You do not select this column as you build a query; it appears automatically.

### The next columns describe the initiator of the tie

![first columns -- C through E](../images/wpa/tutorials/columns-c-e.png)

_Query results example: Columns C through E_

The column names for these attributes are organizational attribute names with the prefix _TieOrigin__. These three columns represent attributes that you selected while building the query:

* TieOrigin_[**FunctionType**](../setup/prepare-organizational-data.md#functiontype-define). The job function that the employee performs.
* TieOrigin_[**LevelDesignation**](../setup/prepare-organizational-data.md#leveldesignation-define). The employee's level within the organization.
* TieOrigin_[**Organization**](../setup/prepare-organizational-data.md#organization-define). The internal organization that the employee belongs to.

### The next two columns identify the other participant in the tie

![next columns -- F and G](../images/wpa/tutorials/columns-f-g.png)

_Query results example: Columns F and G_

The column names for these attributes are organizational attribute names with the prefix _TieDestination__. These first two columns for this person appear automatically:

* TieDestination_[**PersonId**](../setup/prepare-organizational-data.md#personid-define) - A de-identified ID number for the person represented in that data row. You do not select this column as you build a query; it appears automatically.
* TieDestination_[**GroupId**](#groupid-define) - A de-identified ID number of the group in the organization to which the person belongs. This column can help you discover Strong ties into another team to understand how well connected one is with that team and also discover Diverse ties in another team to understand  opportunities for novel information to flow from that team. You do not select this column as you build a query; it appears automatically.

### The next columns describe the other participant in the tie

![next columns -- H through J](../images/wpa/tutorials/columns-h-j.png)

_Query results example: Columns H through J_

The column names for these attributes are organizational attribute names with the prefix _TieDestination__. These three columns represent attributes that you selected while building the query:

* TieDestination_[**FunctionType**](../setup/prepare-organizational-data.md#functiontype-define). The job function that the employee performs.  
* TieDestination_[**LevelDesignation**](../setup/prepare-organizational-data.md#leveldesignation-define). The employee's level within the organization.  
* TieDestination_[**Organization**](../setup/prepare-organizational-data.md#organization-define). The internal organization that the employee belongs to.  

### The last columns give the results

![last columns -- K through O](../images/wpa/tutorials/columns-k-o.png)

_Query results example: Columns K through O_

* **Date** - The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Metrics** - The metrics that you included in the query. For more information, see [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics).

   The results for this query type always include the following metrics:

  * **[StrongTieScore](../use/metric-definitions.md#strong-tie-score-define)** - Sort on this column to find employees with the highest scores. These high scores represent strong ties between the two individuals.
  * **[DiverseTieScore](../use/metric-definitions.md#diverse-tie-score-define)** - Sort on this column to find employees with the highest scores. These high scores represent diverse ties between the two individuals.
  * **[StrongTieType](../use/metric-definitions.md#strong-tie-type-define)** - This column is present to help analysts quickly find the strongest ties. It contains values of 0, 1, or 2, based on the distribution of StrongTieScore. The values indicate the following:
    * **1:** This row clearly indicates a strong tie &mdash; 35th percentile and above, by strength.
    * **2:** This row indicates a tie that is significant but less strong: at or above the 30th percentile but below the 35th percentile.
    * **0:** This row indicates a tie that is not that strong: below the 30th percentile.  
  * **[DiverseTieType](../use/metric-definitions.md#diverse-tie-type-define)** - This column is present to help analysts quickly find the most diverse ties. It contains values of 0, 1, or 2, based on the distribution of DiverseTieScore. The values indicate the following:
    * **1:** This row clearly indicates a diverse tie &mdash; 50th percentile and above, by diversity.
    * **2:** This row indicates a tie that is significant but less diverse: at or above the 45th percentile but below the 50th percentile.
    * **0:** This row indicates a tie that is not that diverse: below the 45th percentile.

### Derived attributes

The following organizational attribute, GroupId, is used in this query type. Note that this attribute is not among the organization data that [admins upload to Workplace Analytics](../setup/upload-organizational-data-1st.md). Rather, it is derived from the [ManagerId](../setup/prepare-organizational-data.md#managerid-define) attribute, which _is_ in the organizational hierarchy data that admins upload.

Attribute (column header) | Description |
---------|----------|
| <a name="groupid-define"></a> GroupId | A unique, de-identified ID number that identifies a group. All members of a team who report to the same person in the organizational hierarchy have the same GroupId. Analysts can use the GroupId column to aggregate members of a team. |

## Related topics

* [ONA metrics](ona-metrics.md)
* [ONA person queries](ona-person-query.md)
* [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
