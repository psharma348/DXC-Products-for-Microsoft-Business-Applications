---
# required metadata

title: [EDI Freight forwarder]
description: [EDI Freight forwarder setup - Shipping container types mapping]
author: [jdutoit2]
manager: Kym Parker
ms.date: 25/11/2021
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

# Freight forwarder setup
## Setup Shipping container types mapping

Users can access the form by navigating to **EDI > Setup > Freight forwarder landed cost setup > Shipping container types mapping**

Code mapping the Freight forwarders's value to a D365 Landed cost shipping containers. <br>

- Click **New** to create a new record
-	In the **Name** field, enter the name of the Shipping container types mapping group
-	In the **Description** field, enter a description of the Shipping container types mapping group
-	In the **Mappings** FastTab, select **Add** to create a new record
-	Select the **Shipping container type** from the available list. Options are obtained from **Shipping container type** setup at **Landed cost > Containers setup > Shipping container types**
-	Specify the Freight forwarder's **Value**. Blank is allowed.

## Where used
Shipping container types mapping is assigned on the [Freight forwarder landed cost Trading partner's](../Trading-partner.md) Options field called **Container type**.

Used on the following EDI documents (field):
- Voyage creator (ShipContainerTypeId) 

## Examples
D365 Landed cost Shipping container types	| Trading partner values
:--                                       |:--
**40’FCL**                                |	40HC
**40’FCL**                                |	4000
**20’FCL**                                |	2000

## Data entities:
- Shipping container type mapping
- Shipping container type mapping lines
