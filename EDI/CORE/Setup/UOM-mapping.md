---
# required metadata

title: [EDI Core]
description: [EDI Core - UOM mapping]
author: [jdutoit2]
manager: Kym Parker
ms.date: 31/03/2022
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

# Unit of measure mapping

Ability to map a trading partner’s unit of measure (example kgs) to D365 unit of measure (example kg). <br>
Users can access the form by navigating to **EDI > Setup > UOM mapping**

- Click **New** to create a new record. 
-	In the **Name** field, enter the name of the unit of measure mapping
-	In the **Description** field, enter a description of the unit of measure mapping
-	In the **Company accounts ID** field, select a company if the mapping applies only to a specific company. Also a requirement if **Item code** _Group_ or _Table_ is used. Blank Company is allowed where all the mapping lines’ **Item code** is set to _All_.
-	In the **Mappings** FastTab, select **Add** to create a new record
-	Select the D365 **Unit**. Options are obtained from Units setup at Organization administration > Setup > Units, examples:
    - box
    - pcs
- Specify the **indicator**/trading partner's value used to identify the Trading partner's **Value**
- Select **Item code** - All, Group or Table
- Where applicable, select the **Item relation**
- **Inventory dimensions** are also available to limit the unit of mapping to a specific inventory dimension combination

## Customer EDI module
For **Customer** Trading partners, the Unit of measure mapping is utilized on **Sales unit**:
- Inbound – receive and ability to use Customer’s unit of measure
    - Customer purchase order and 
    - Customer purchase order change
-	Outbound - sent with Customer’s unit of measure
    - Customer purchase order acknowledgement
    - Customer advanced shipping notice
    - Sales invoice

## Vendor EDI module
For **Vendor** Trading partners, the Unit of measure mapping is utilized on **Purchase unit**:
-	Outbound - sent with Vendor’s unit of measure
    - Vendor purchase order and 
    - Vendor purchase order change
- Inbound – receive and ability to use Vendor’s unit of measure
    - Vendor purchase order acknowledgement
    - Vendor advanced shipping notice
    - Sales invoice

## Freight forwarder landed cost EDI module
For **Freight forwarder** Trading partners, the Unit of measure mapping is utilized on **Purchase unit** and **Inventory unit**
- Inbound – receive and ability to use Freight forwarder’s unit of measure
    - Voyage creator

## Where used
UOM mapping is assigned on the Customer, Vendor and Freight forwarder Trading partner's Options field called **UOM**.

## Data entities:
-	UOM mapping
-	UOM mapping lines

