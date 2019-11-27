---
# Metadata Sample
# required metadata

title: Upload organizational data to Workplace Analytics (subsequent uploads)
description: How to upload data from your organization to Workplace Analytics. Follow these steps if this is not the first time you are uploading data. 
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Upload organizational data (subsequent uploads)

This article presents the steps that administrators take to upload (import) organizational data to Workplace Analytics. Complete these steps after preparing data as described in [Prepare organizational data](Prepare-organizational-data.md).

  > [!Important] 
  > Follow the steps in this section if this is **not** the first time that you have uploaded organizational data to Workplace Analytics. If this **is** the first time, follow the steps in [Upload organizational data (first upload)](upload-organizational-data-1st.md).

## Import tasks

The task of importing organizational data has three parts:

1. [File upload](#file-upload)
2. [Field mapping](#field-mapping)
3. [Data validation](#data-validation)

After you prepare the source data, you can upload the .csv file and map fields. After you map fields, Workplace Analytics validates the data. When the data successfully validates, the overall data-import task is complete. If the data validation is not successful, you can choose from a few options that are described in [Validation fails](#validation-fails).

### Video: Upload organizational data

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897809" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## File upload

In the following steps, you specify a .csv file to upload to Workplace Analytics.

**To select the file to upload**

1. Open [Workplace Analytics](https://workplaceanalytics.office.com). If prompted, enter your organizational credentials.
2. In the left navigation pane, select **Settings**.
3. Select **Organizational data**. The **Upload history** area of this page displays the previous data uploads from your organization.
4. Select **New upload**.
5. On the **Upload** page, select **Name your upload**, and then type the name of your new upload file.
6. Optionally, select **Add an optional description** and type a description of this upload.
7. In the **Select file** section, click **Select file**. In the dialog box that appears, select the .csv file that you want to import.

### Important upload considerations
 
  * The .csv file that you upload must be UTF-8 encoded.
  * Make sure that the file you are uploading is not open in a different program when you begin the upload process.
  * After the upload process begins, the process is irreversible.  

  > [!Note]
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Append or replace organizational data_.

8. To complete a new-file upload, select **Next**. This displays the System fields table. Go to [Field mapping](#field-mapping).
9. To append or replace organizational data, locate the **Append or replace** area. In this area, you can select either of the following options:
    * **Append the existing organization data** to update attribute values for existing employees, to add new employees, or to add new attributes.
    * **Replace all existing organizational data with this file** to delete all previous HR data uploads and make this the first new HR data upload. If you choose this option, please note the following: 
      * **Permanent deletion:** The replace option permanently deletes all previously uploaded organizational data. 
      * **Column omission:** The schema of the new data file need not exactly match the schema of the previously uploaded HR data. However, omitting columns that were present in previous uploads can cause errors in [auto-refresh](../tutorials/query-auto-refresh.md) queries that depend on the presence of those HR columns. For more information, see [Prepare organizational data](prepare-organizational-data.md).
       
11. After reviewing the warning message, select **Continue** and then [map your fields](#field-mapping).

## Field Mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these on the **Upload** page.

<img src="../images/wpa/setup/upload2-map-top.png" alt="Upload page">

The **Upload** page includes tables for System fields and Custom fields for mapping the data for the upload file.

When appending new attributes to an existing upload, you need to select all the same required and optional attributes that you mapped before in previous uploads, in addition to the new attributes you want to add (append).

### System fields table

<!-- The following include is for "system" fields and is meant only for subsequent uploads, and only temporarily. After the UI changes, switch to the "system default" include file. -->
[!INCLUDE [System fields table](../includes/org-data-sys-fields.md)]

[!INCLUDE [Fields tables](../includes/org-data-fields-tables.md)]

**To map fields**

After you complete the steps in [File upload](#file-upload), the **Upload** page with the System fields table will appear.

1. Map the required fields.
   
    a. Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name):

    <img src="../images/wpa/setup/upload2-map-sys-fields.png" alt="System fields table">

    b. Under Source column (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data.

    c. Fill in appropriate values for the other columns in the table: Workplace Analytics name, Data type, and so on. Repeat these mapping steps for the rest of the required fields and for any optional fields that you choose to map.

   > [!Note]
   > For more information, see [Columns in the fields tables](#columns-in-the-fields-tables).

2. Map the optional and custom fields, as applicable. You only need to map the columns in your source (.csv) file that your organization considers important for analysis. For example, if "StartDate" is important and your data contains this field, map it.

    <img src="../images/wpa/setup/upload3-map-custom2.png" alt="Custom fields table">

    a. Under **Source column** (the first column in the table), select the down arrow to display the list of column names that were found in the data file. From the list, select the correct column name for the data. In this example, you'd select <b>StartDate</b>.
    
    b. Set values for the other columns in the table, such as the data type, the validity threshold, and the hash setting for reports.
     
    c. Repeat these steps for all custom fields that are important to your organization.

3. In the **Submit for validation** area, select **I confirm that these mappings are correct**, and then select **Submit**. This uploads the data file and starts the validation process.

4. Go to the next phase, [Data validation](#data-validation).

## Data validation

After you complete the steps in [Field mapping](#field-mapping), the organizational data file is uploaded and validated, and the **Upload** page displays the _File is being uploaded_ screen:

![Upload in progress](../images/wpa/setup/upload4-uploading.png)

In most cases, file validation should complete very quickly. If your organizational data file is very large, validation could take up to one or two minutes. 

<!-- THE FOLLOWING IS NOT VALID FOR SUBSEQUENT UPLOADS
During this step, if you decide that the data you are uploading is not the correct data and that you want to upload a different data file instead, select **Cancel**. 
-->

After this phase completes, the file has either passed or failed validation. Go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page. 
 
> [!Important] 
> You must stay logged in while the file is uploading or the upload will be canceled. The upload requires this page to be open in your web browser during the upload. If you close the browser (or this browser page), the upload will fail.

## Validation succeeds

If validation succeeds, the **Upload** page will indicate it and show the size of the upload and that the overall process is complete. After successful validation, Workplace Analytics processes your new data. 
 
<img src="../images/wpa/setup/upload6-validated.png" alt="Validation succeeded">

You can select **Settings** > **Organizational data** **Upload** > **Organizational data** to show the **Upload history** page. You can then select **Successes** to see the workflows that were successfully validated (and uploaded).

On this page, you have the following options:

 * Select the **View** (eye) icon to see a summary of the validation results.
 * Select the **Mapping** icon to see the mapping settings for the workflow.
 * Select the **Validation** (download) icon to see a list of validation warnings.

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page.

## Validation fails

If data validation fails, the **Data load** page shows a "failed" notification. It also shows details about the validation attempt and presents you with options:

<img src="../images/wpa/setup/upload9-val-failed-upload-flow.png" alt="Validation failed">

After a failed validation, it's best to first gain an understanding of the errors by scanning the error summary table. You can also select **Download issues** to examine the error log.

This information about the errors helps you decide which path to choose next &mdash; whether to fix the source data, change your mapping settings, or abandon the current upload. The following section describes these options: 

### Options upon failed validation

[!INCLUDE [Options upon failed validation](../includes/org-data-failed-validation.md)]

### Addition of a new data column

Let's say that you've already uploaded at least 13 months of snapshot data, which contained the five required columns (PersonId, EffectiveDate, LevelDesignation, ManagerId, Organization) for all employees. Now, you want to upload one new column of data – for example, an engagement score value for each employee – and you want it to apply to all of the historical data. When you upload to append the new "EngagementScore" data column, remember to reupload all five of the minimum required fields along with the new field. 

### Set Validity threshold for custom fields

The threshold checks for non-null values, so it depends on the intended use of the custom field. If you intend to use this data in much of your analysis, consider setting it to a high percentage. You can set a lower threshold for data that applies, for example, to only a small subset of people in your organization.

#### Set a high value

Generally, you should set the Validity threshold to a high value. This is especially important if your analysis will focus on that field.

For example, you might include a "SupervisorIndicator" attribute. At first, you might not think that you're analyzing manager behavior and you might be tempted to omit this attribute. But the organization hierarchy is used implicitly by many Workplace Analytics analyses – for differentiating different work groups, for determining high- and low-quality meetings based on how many levels attend, and more.

#### Set a lower value

The goal of your analysis might be to determine sales effectiveness. Your data might include an attribute for sales attainment that only makes sense for members of your sales force, who constitute about 10% of the company. This number doesn't apply to engineers or program managers, but it is critical for high-performers in sales.  


