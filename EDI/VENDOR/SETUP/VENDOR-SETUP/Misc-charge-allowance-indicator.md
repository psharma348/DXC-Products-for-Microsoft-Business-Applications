---
# required metadata

title: [EDI Vendor]
description: [EDI Vendor setup - Misc charge/allowance indicator]
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
## Setup misc. charge/allowance indicator

Users can access the form by navigating to **EDI > Setup > Vendor setup > Misc charge/allowance indicator**

Code which indicates an allowance or charge for the service specified. <br>

- Click **New** to create a new record
-	In the **Name** field, enter the name of the misc. charge/allowance indicator
-	In the **Description** field, enter a description of the misc. charge/allowance indicator
-	In the **Mappings** FastTab, select **Add** to create a new record
-	Select the **Indicator**. Options are: <br>
    - **Allowance** - When charge value maintained on purchase order is less than zero
    - **Charge** - When charge value maintained on purchase order is more than zero
    - **No allowance or charge** - When charge value maintained on purchase order equal zero
-	Specify the vendor's value used to identify the **EDI indicator**.

## Where used
Misc. charge/allowance indicator is assigned on the [Vendor Trading partner's](../Trading-partner.md) Options field called **Misc charge/allowance indicator**. <br>
Used on field **MiscIndicator** on EDI documents:
- Vendor purchase order
- Vendor purchase order change
- Purchase invoice

## Data entities:
- Vendor EDI misc. charge/allowance indicator group
- Vendor EDI misc. charge/allowance indicator lines
