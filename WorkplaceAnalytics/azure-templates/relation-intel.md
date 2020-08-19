---

ROBOTS: NOINDEX,NOFOLLOW
title: Relationship Intelligence report 
description: Learn about the Relationship Intelligence Power BI report included in Workplace Analytics Azure Templates and how to use it
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid: 
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Relationship intelligence report

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Relationship Intelligence Power BI report. You can use this report to analyze relationships your organization has with collaborators external to the company, such as relationships with customers or partners.

Workplace Analytics has a variety of measures to help you visualize and analyze formal and informal relationships within your organization, this report can help you understand how internal groups are communicating and spending their time with external collaborators.

This report requires account and contact information from a Customer Relationship Management (CRM) platform, such as Dynamics or Salesforce. This report uses CRM data to provide account-level focus and insights into relationship patterns.

## Prerequisites
  
* **CRM data** –  Accounts and contacts exported as .csv files from your CRM, such as Microsoft Dynamics or Salesforce.
* **Data access** - You need access to unhashed ExternalCollaboratorIDs and unhashed Subject lines to view topics in your organization's Office 365 collaboration data, such as for email, meetings, instant messages, and unscheduled calls.
* **Power BI Desktop** - Have the latest version of Power BI Desktop installed locally. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.
* **Permissions** - The Azure Templates admin must explicitly add people who want to view the Relationship Intelligence reports to the group or access control list for the configured Azure Analysis Services.

To create a Relationship Intelligence report:

1. [Add account mapping](#add-account-mapping) - Follow the steps to upload your CRM data into a mapping file in Workplace Analytics Azure Templates.
2. [Add new analysis](#add-new-analysis) - Follow the steps to create the dataset in Workplace Analytics Azure Templates that uses the account mapping to create the report in Power BI.
3. [Load the data and view the report](#load-the-data-and-view-the-report) - Follow the steps to download the Power BI template, load the data in Power BI, and then analyze it in the Power BI report.

## Add account mapping

Before creating analysis, you need to upload the exported CRM data (.csv) data files for your customer accounts and contacts. See [Required file formats](#required-file-formats) for details about what the files must include based on the type of CRM.

1. In Workplace Analytics Azure Templates, select **Relationship Intelligence**.
2. Select **Account Mapping** > **Add New Mapping** (at top right) to upload a new set of files for customer accounts and contacts.

    ![Add a mapping file for the report](../Images/ri-account-map.png)

3. In **Name the Account mapping**, enter a friendly name for the mapping file.
4. In **Provide the accounts** and **Provide the contacts**, select **Choose File**, and then select the .csv files for accounts and contacts, which must be in the required format as described in [Required file formats](#required-file-formats).
5. In **Specify your CRM source**, select the CRM source for your accounts and contacts.  

## Required file formats

The following are examples of what the .csv file formats for accounts and contacts must include.

#### Dynamics accounts

![File format for Dynamics accounts](../Images/ri-dynamics-accounts.png)

#### Dynamics contacts

![File format for Dynamics contacts](../Images/ri-dynamics-contacts.png)

#### Salesforce accounts

![File format for Salesforce accounts](../Images/ri-salesforce-accounts.png)

#### Salesforce contacts

![File format for Salesforce contacts](../Images/ri-salesforce-contacts.png)

## Add new analysis

After you add a mapping file for your customer accounts and contacts, do the following to create the dataset for the report.

1. In Workplace Analytics Azure Templates, select **Relationship Intelligence** > **Add New Analysis** (at top right).
2. In **Define Analysis Settings**, enter a friendly name for the analysis and select the path to the dataset.

    ![Add new analysis for the report](../Images/ri-new-analysis.png)

3. In **Select Account Mapping**, select the mapping file you created in [Add account mappings](#add-account-mappings).
4. In **Select the Grouping Attributes**, select two to five HR attributes to analyze and use to pivot analysis in Power BI. These are the HR attributes imported with the organizational data from Workplace Analytics.
5. Select **Submit**. Creating the dataset will take a few minutes up to a few hours based on the size of the data.
6. In **Relationship Intelligence** > **Analysis**, the analysis table includes the name, the source, the date is was submitted, who submitted it, and the following:

   * **Download** - Select to copy a link to this dataset and download the Power BI template.
   * **Parameters** - Lists details about the job parameters, such as the input path, output folder, excluded keywords, the mapping file name, the HR attributes included, and the person who created this analysis.
   * **Status** - Analysis shows a green check mark when it successfully adds it. A red X means it failed.
   * **Details** - Lists the job details including error messages (far right column) to help troubleshoot a failure.
   * **Delete** - Select to delete analysis that failed or that's no longer needed.

    ![Analysis table details](../Images/ri-analysis-table.png)

    ![Download Power BI template and copy data link](../Images/ri-download.png)

## Load the data and view the report

1. In **Relationship Intelligence** > **Analysis**, when the analysis status has a green check mark, select the **Download** icon for the analysis.
2. Select **Copy** to save the database name for this analysis to the clipboard.
3. Select **Download PBIX File** to download the Power BI template for the report.
4. Open the downloaded file in Power BI Desktop.
5. If prompted, authenticate your credentials, which the Azure Templates admin used to give you access to the Azure Analysis services.
6. In Power BI, select **Transform Data**, and then paste the database name you copied for the analysis in **Step 2**, and then select **OK**.
7. If prompted, select **Model**, and then **OK**.
8. 

## About the report


## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

