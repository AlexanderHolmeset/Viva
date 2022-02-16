---

title: Language support and guidelines for Advanced insights in Viva Insights
description: Describes the languages supported by Advanced insights within Microsoft Viva Insights
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.collection: 
- viva-insights-advanced
- viva-insights-leader
ms.localizationpriority: medium 
ms.service: viva 
ms.subservice: viva-insights 
manager: scott.ruble
audience: Admin

---

# Advanced insights language support and guidelines

The user interface in Microsoft Viva Insights in Workplace Analytics is currently available in the languages listed in [Supported languages](#supported-languages).

The Workplace Analytics app automatically uses your language identifier (language and region) setting, as specified in one of the following sources:

* Windows
* Your web browser
* Location that's set for your Exchange Online mailbox

You can override this setting by replacing the language identifier in the URL. [Supported languages](#supported-languages) lists the languages currently supported for Workplace Analytics.

For example, replace '/en-us/' with '/ja-jp/' in the following URL to indicate Japanese as the language to view it in: 'https://workplaceanalytics.office.com/ja-jp/'

## Supported languages

Language and region | Language identifier
------ | ------
English | en-us
Japanese | ja-jp
German | de-de
Chinese (Simplified) | zh-cn
Spanish | es-es
French | fr-fr
Portuguese (Brazil) | pt-br
Russian | ru-ru
Italian | it-it
Chinese (Traditional) | zh-tw
Korean | ko-kr

## Use of data other than English

If and when you are able to use Workplace Analytics with _data_ that is in other languages, do the following as a guideline:

* Query names and descriptions must be in English, Japanese, or French.

   ![Query names and descriptions.](../Images/WpA/Overview/query-name-description.png)

* Column headers for the organizational data when you [prepare the organizational data](../Setup/Prepare-organizational-data.md) must be in English.

* When an analyst selects metrics while building a [query](../tutorials/query-basics.md), the metric names they choose can be in the language of their choice. See [Supported languages for column headers](../use/view-download-and-export-query-results.md?branch=pas-pd-other-char-sets#supported-languages-for-column-headers).

* For content within organizational data, you can use languages other than English.

## Privacy settings

In [Privacy settings](../use/privacy-settings.md), when adding the subject line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in other languages such as Japanese or Chinese. For best results, use single words, separated by a semicolon.

![Exclude terms from subject line.](../Images/WpA/Overview/exclude-terms-from-subject-line.png)

We appreciate all your feedback. To report any language-related issues, use **Send feedback** within the app.

## Related topics

* [Supported languages in meeting exclusion rules](../tutorials/meeting-exclusion-concept.md#supported-languages)
* [Control settings](../use/settings.md)
* [Privacy settings considerations](../Privacy/privacy-considerations.md)
