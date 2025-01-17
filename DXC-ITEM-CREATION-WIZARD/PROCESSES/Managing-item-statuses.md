---
# required metadata

title: [DXC Item Creation Wizard ]
description: [DXC Item Creation Wizard - Managing item statuses  ]
author: [Liam Coll]
manager: Kym Parker
ms.date: 23/07/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [DXC Item Creation Wizard ]
audience: [Application User]
# ms.devlang: 
ms.reviewer: [liamcoll]
ms.search.scope: [Which Operations client to show this topic as help for, to be set by content strategist, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
# ms.tgt_pltfrm: 
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: [Global]
# ms.search.industry: [leave blank for most, retail, public sector]
ms.author: [helenho]
ms.search.validFrom: [September 2017]
ms.dyn365.ops.version: [name of release that feature was introduced in, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
---

#	Managing Item Status

## Updating using a creation template

A status value can be assigned to an [item creation template](../SETUP/ITEM-CREATION/Item-creation-templates.md). Use of this template to create, release or update an item will apply the template status to the released product where the Change item status element has been included in the approval [workflow](../SETUP/Item-creation-workflows.md).

Where no item status exists on a released product and the template does not have a value defined, the default value set in the [parameters](../SETUP/Item-creation-parameters.md) form will be used.

## Updating a single item

The item status can be held at the item or item dimension level. The item status can be manually updated via the *item status link* menu in the action pane of the released products form. **Item creation > Products > Released products > Item creation > Item status link**.

The form will display the current record on opening, historical records can be viewed by selecting *As of date* from the action pane.  

#### To create a new item status;
1. Select *New* from the action pane.
2. Select the new *Status* value.
3. Enter the effective date of the new status
    * The previous record will have the expiration date set to the day prior.

*Note: The Item Status displayed at the top of the released products form is the item status at the item level, not the item dimension level.*

## Updating a group of items

A periodic job is available that can update the item status with a specified effective date, this can be run for a range of items. Category hierarchy can be used to help select these products to be included. This allows for item status to be planned and updated prior to the effective date. The periodic job can be accessed from **Item creation > Periodic tasks > Update item status**.

#### Update item status
1.	Select the *From Status*, only the selected items matching this status will be updated.
2.	Select the *To Status*.
3.	Enter an *Effective date* if required.  
    * To make effective immediately, leave blank.
4.	Select a *Category hierarchy* if required to filter down to a group of products.
5.	Select the items to be updated. 
6.	Select OK.

*Note: Optionally select the Run in the background tab to run in batch processing. Please see [Microsoft User Guides](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/sysadmin/batch-processing-overview) for further information*

## Updating based on stock on hand rules

[Automatic status change rules](../SETUP/ITEM-SETUP/Automatic-status-change-rules.md) can be setup to update the item status based on certain events. For example, a status that indicates a low level of inventory can be updated to a discontinued status once the stock on hand becomes zero. The periodic job can be accessed from **Item creation > Periodic tasks > Item status > Automatic status update**.

#### Automatic status update
1.	Using the filter, select the *status* being updated from and the *event* being used
    * To run for all events, leave blank
2.	Select OK.

*Note: Optionally select the Run in the background tab to run in batch processing. Please see [Microsoft User Guides](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/sysadmin/batch-processing-overview) for further information*

#	Item Status Visibility

## Released products
When viewing the Released Product details, the inventory status symbol will be displayed directly below the Item number and description.

## Inventory transactions
When creating a sales/purchase order, the inventory status symbol will be displayed on the sales/purchase line. This will enable the user to identify the current status at a glance.
