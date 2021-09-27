---
# required metadata

title: [EDI Core]
description: [EDI Core Documents - Functional acknowledgement outbound]
author: [jdutoit2]
manager: Kym Parker
ms.date: 23/09/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [Operations AOT form name to tie this topic to]
audience: [Application User]
# ms.devlang: 
ms.reviewer: [jdutoit2]
ms.search.scope: [Which Operations client to show this topic as help for, to be set by content strategist, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
# ms.tgt_pltfrm: 
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: [Global for most topics. Set Country/Region name for localizations]
# ms.search.industry: [leave blank for most, retail, public sector]
ms.author: [author's Microsoft alias]
ms.search.validFrom: [month/year of release that feature was introduced in, in format yyyy-mm-dd]
ms.dyn365.ops.version: [name of release that feature was introduced in, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
---

# Functional acknowledgement outbound

When a Trading partner requires a Functional Acknowledgement for sent EDI files, the following is required:
1.	Create document Template for Functional acknowledgement outbound.
2.	If required, create Setting profile for the Functional acknowledgement outbound
3.	Add the Functional acknowledgement outbound document type to Trading Partner’s Outgoing documents and Enable.
4.	On each applicable incoming documents for the Trading partner, set **Acknowledgement** to _Yes_.

## Setting profiles

**Field** 	                                | **Description**                     | **Options/example**
:--------------------------------           |:------------------------------------|:------------------------------------
**Document type mapping**                   | Assign applicable document type mapping to setting	| Mappings setup at [**EDI > Setup > Document type mapping**](../Setup/Document%20type%20mapping.md)

## View Staging table records

### Incoming staging records

Users can access the form by navigating to **EDI > Documents**
All Inbound EDI staging forms has a field **Sent** indicating if a Functional acknowledgement outbound has been sent to the trading partner for each incoming document.

### Functional acknowledgement outbound staging records

Users can access the form by navigating to **EDI > Documents > Functional acknowledgement outbound**. <br>
Use this form to review staging records and optionally manually process the staging record.

#### List page
**Field** 	                      | **Description**
:-------------------------------- |:-------------------------------------
**EDI number**                    |	EDI Staging table record id
**Company**                       |	Company account for the staging record
**Template Id**                   |	Document type template used to process the document
**Staging to target status**      |	The current status of the staging record. <br> Options include: <br> •	**Not Started**: The Functional Acknowledgement has been created but no file has yet been generated. <br> •	**Error**: The Functional Acknowledgement has been processed but no file has been created.  There are errors with the record that need to be reviewed. <br> •	**Completed**: The Functional Acknowledgement file has been created and added to the outbound file queue.
**Trading partner account**       |	Trading partner account for the staging record.
**Trading partner GLN**           |	The trading partners’ global location number is shown here.
**Company GLN**                   |	The company’s global location number is shown here.
**Group control number**          |	Trading partner’s original document that is being acknowledged's group control number.
**Document type**                 |	Trading partner’s original document type being acknowledged. [Document type mapping](../Setup/Document%20type%20mapping.md)
**Created date and time**         |	The date and time the staging record was created.