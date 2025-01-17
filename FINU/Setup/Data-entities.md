---
# required metadata

title: [Finance Utilities ]
description: [Finance Utilities setup - Data Entities ]
author: [jdutoit2]
manager: Kym Parker
ms.date: 27/05/2022
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

# Data entities

## Finance utilities data entities:
Finance utilities includes the following data entities :

| **Entity**                            | **Manual setup path**   |
|-|-|
|  **Financial utilities parameters**   | Cash and bank management > Setup > Advanced bank reconciliation setup > Financial utilities parameters |
|  **Budget utilities parameters**      | Budgeting > Setup > Basic budgeting > Budget utilities parameters  |
| **Financial utilities connections**   | Cash and bank management > Setup > Advanced bank reconciliation setup > Financial utilities connections |

## Standard data entities
Finance utilities have extended the following standard data entities:

### Bank accounts
Cash and bank management > Bank accounts > Bank accounts

| **Entity**                          | **Additional Finance utilities fields for standard entity**                
|-                                    |-                        
| **Bank accounts**                   | **EFT parameters:** <br> • BPAY batch ID (DFUBPAYBATCHID) <br> •	Extra balance line on EFT (DFUEXTRABALANCELINE) <br> • Include balance line in record count (DFUBALANCELINECOUNT) <br> • Total line order (DFUTOTALLINEORDER) <br> • Use vendor bank name (DFUUSEVENDBANKNAME) <br> • User identification (DFUEFTUSERID) <br> **BPAY:** <br> • BPAY batch ID (DFUBPAYBATCHID) <br> **Import financial utilities connection:** <br> • Posting date (DFUBANKSTATEMENTPOSTINGDATETYPE)

### Vendor bank accounts
Accounts payable > Vendors > All vendors - Bank accounts on Vendor FastTab

| **Entity**                          | **Additional Finance utilities fields for standard entity**                 
|-                                    |-                                          
| **Vendor bank accounts**            | • Biller code (DFUBILLERCODE) <br> • Lodgement reference (DFULODGEMENTREF) <br> • Bank code (ECL_BANKCODE) <br> • Bank particulars (ECL_BANKPARTICULARS) <br> • Bank reference (ECL_BANKREFERENCE) 

### Vendor methods of payment
Accounts payable > Payment setup > Methods of payments

| **Entity**                          | **Additional Finance utilities fields for standard entity**                 
|-                                    |-                                          
| **Vendor payment method**           | • Sundry method of payment <br> • Auto payment reference number <br> • BPAY method of payment <br> • Payment control > Lodgement reference is mandatory (DFUVALIDATELODGEMENTREFISMANDATORY) <br> • Payment attributes > Lodgement reference (DFUATTRIBUTELODGEMENTREFENABLED)


### Reconciliation matching rules
Cash and bank management > Setup > Advanced bank reconciliation setup > Reconciliation matching rules

| **Entity**                          | **Additional Finance utilities fields for standard entity**                     
|-                                    |-  
| **Reconciliation matching rules**   | **Step 2: Do not mark when there are matching bank transactions:** <br>  •	Group by document number (SYSTEMGENERATEDTYPE = ECL_GroupByDocumentNum) <br> • Include in (DFUBANKRULEACTIVATEINCLUDEIN) <br> **Step 3: Extended financial details:** <br> • Company (DFUCOMPANY) <br> •	Offset company (DFUOFFSETCOMPANY) <br> •	Offset account type (DFUOffsetAccountType) <br> •	Offset account (DFUOFFSETLEDGERDIMENSIONDISPLAYVALUE) <br> •	Offset account dimension values (DFUOFFSETDEFAULTDIMENSIONDISPLAYVALUE) <br> •	Offset account bank statement field (DFUOFFSETACCOUNTFIELDNAME) <br> • Settle transaction (DFUSETTLETRANS) <br> •	Settle transaction bank statement field (DFUSETTLETRANSFIELDNAME) <br> •	Auto-post customer payment journal (DFUCUSTPAYMAUTOPOST) <br> •	GST group (DFUTAXGROUP) <br> •	Item GST group (DFUTAXITEMGROUP) | 

> Note: Ensure the **Financial dimension configuration for integrating applications** dimension format aligns with dimensions on the bank reconciliation matching rule before importing the **Reconciliation matching rules** entity. General ledger > Chart of accounts > Dimensions > Financial dimension configuration for integrating applications. <br> Define data entity format for **Default dimensions integration** and **Ledger dimensions integration**. <br>
> See [link](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration) for more detail.

### Bank statement format
Cash and bank management > Setup > Advanced bank reconciliation setup > Bank statement format <br> 
Bank statement format entities are a combination of Finance utilities entities and additional fields added to standard entity. 

| **Order** | **Entity**                          | **Standard / Finance <br> utilities entity**   | **Additional Finance utilities fields for standard entity**    |
|-          |-                                    |-                                          |-
| 1         | **Bank statement format**           | Standard                                  |  • Custom format (SAB_FINCUSTOMFORMAT) <br> • ABSR file type (SAB_FINFILETYPE) <br> • Field delimiter (SAB_FINFIELDDELIMITER) <br> •  Record code field position (SAB_FINFIELDPOSITION) <br> • Record code field length (DFUIMPORTLENGTHRECORDCODE) |
| 2         | **Custom line codes**               | Finance utilities                         | - 
| 3         | **Bank statement format lines**     | Finance utilities                         | - 
| 4         | **Line codes format**               | Finance utilities                         | - 

> Note: If comma is used in **Field delimiter** on the **Bank statement format**, set SAB_FINFIELDDELIMITER **Text qualifier** to _Yes_ in Mapping details.

