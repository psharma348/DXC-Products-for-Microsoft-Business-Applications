---
# required metadata

title: [EDI Vendor]
description: [EDI Vendor setup - Charges code]
author: [jdutoit2]
manager: Kym Parker
ms.date: 9/11/2021
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

# Vendor setup
## Setup charges code

Users can access the form by navigating to **EDI > Setup > Vendor setup > Charges code**

Code identifying the service, promotion, allowance, or charge. <br>

- Click **New** to create a new record
-	In the **Name** field, enter the name of the charges code
-	In the **Description** field, enter a description of the charges code
-	In the **Mappings** FastTab, select **Add** to create a new record
-	Select the **Charges code**. Options are obtained from **Charges code** setup at **Procurement and sourcing > Setup > Charges > Charges code**, examples: <br>
    -	Fee
    -	Freight
    -	Handling
    -	Install
    -	Insurance
-	Specify the vendor's value used to identify the **EDI charges code**.

## Where used
Charges code is assigned on the [Vendor Trading partner's](../Trading-partner.md) Options field called **Charges code**. <br>
Used on field **MiscCode** on EDI documents:
- Vendor purchase order
- Vendor purchase order change
- Purchase invoice

## Data entities:
- Vendor EDI charges code group
- Vendor EDI charges code lines
