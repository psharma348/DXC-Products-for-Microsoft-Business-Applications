---
# required metadata

title: [Finance Utilities ]
description: [Accounts payable setup - Vendor bank account changes workflow ]
author: [helenho]
manager: Kym Parker
ms.date: 02/03/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [Finance Utilities ]
audience: [Application User]
# ms.devlang: 
ms.reviewer: [jdutoit2]
ms.search.scope: [Which Operations client to show this topic as help for, to be set by content strategist, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core-Dynamics-AX-CP-requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions-list-for-docs-topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
# ms.tgt_pltfrm: 
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: [Global]
# ms.search.industry: [leave blank for most, retail, public sector]
ms.author: [helenho]
ms.search.validFrom: [September 2017]
ms.dyn365.ops.version: [name of release that feature was introduced in, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core-Dynamics-AX-CP-requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions-list-for-docs-topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
---

# Accounts payable functionality
The fields as described in the following subsections are available to control the additional functionality for accounts payable.

## Vendor bank account changes workflow

When changes are made to specific vendor fields, standard D365 vendor workflow can be used for approval before the changes are applied to the vendor. 
Finance utilities has added additional vendor fields that can be managed by the same workflow.

### Setup vendor approval
Users can access the **Accounts payable parameters** page by navigating to **Accounts payable > Setup > Accounts payable parameters**. <br>
The below fields have been added to the existing Vendor approval fields. When enabled they will be submitted using the existing **Proposed vendor changes workflow.**

**Vendor bank account:**
-	Bank groups
-	BSB number
-	Bank account number
-	SWIFT code
-	Biller code (Finance utilities BPAY field)
-	Lodgement reference (Finance utilities BPAY field)
-	IBAN
-	Active date
-	Expiration date

**Vendor:**
-	Payment id (existing field used for Finance utilities BPAY)
