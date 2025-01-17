---
# required metadata

title: [EDI Core]
description: [Introduction to EDI Core]
author: [jdutoit2]
manager: Kym Parker
ms.date: 1/12/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [EDI]
audience: [Application User]
# ms.devlang: 
ms.reviewer: [jdutoit2]
ms.search.scope: [Which Operations client to show this topic as help for, to be set by content strategist, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
# ms.tgt_pltfrm: 
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: [Global]
# ms.search.industry: [leave blank for most, retail, public sector]
ms.author: [jdutoit2]
ms.search.validFrom: [September 2017]
ms.dyn365.ops.version: [name of release that feature was introduced in, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
---

# Introduction
This section will provide a quick overview of the Core EDI module.

## Documents
### Core EDI documents (All trading partners)

EDI contains the following documents pertaining to all Trading partners.
- **Inbound**
	- **Functional Acknowledgement** – Receive functional acknowledgement that outbound document has been received by Trading partner.
- **Outbound**
	- **Functional Acknowledgement** – Send functional acknowledgement that inbound document has been received.

Depending on licensing additional documents are available per module, view all trading partner documents [here](Trading-partners-and-documents.md).

## Setup
### Core setup
The following core setup is available under **EDI > Setup**:
- [Connections](../Setup/Connection-setup.md) - Setup the applicable ftp/ftps/sftp/azure blob connection(s)
- [Cleanup profile](../Setup/Cleanup-profile.md) - (Optional) Can be used to automatically delete staging records based on status and age days
- [Reset status](../Setup/Reset-status.md) - (Optional) Automatic retry by resetting Error records to Not started based on a recurrence pattern
- [EDI parameters](../Setup/EDI-parameters.md) - Refresh module after deployment, and other parameter setup
- [EDI shared parameters](../Setup/EDI-shared-parameters.md) - Setup shared parameters
- [UOM mapping](../Setup/UOM-mapping.md) - Create unit of measure mappings that can be assigned on applicable trading partners, for example kgs to kg
- [Document type mapping](../Setup/Document-type-mapping.md) - (Optional) Document type mapping for functional acknowledgement documents
- [Document types](../Setup/Document-types.md) - Setup document templates, setting profiles, validation profiles, outbound filenames and field metadata for all applicable documents
- [Trading partners](../Setup/Trading-partners.md) - Setup trading partners and assign the applicable mappings and documents
- [EDI Batches](../Setup/EDI-Batches.md) - Enable batches for all the EDI steps

## Processing

### Import files
Ability to manually import or review inbound files
- [Inbound files](../Managing-files/Inbound-files.md) - View and/or manually process importing of files and processing to staging.

### Export files
Ability to manually export or review outbound files
- [Outbound files](../Managing-files/Outbound-files.md) - View and/or manually process exporting of files.

[Process overview for import and export](Process-overview.md) of EDI documents.

### Archive file attachments and Delete records
- [Archive file queue](../Managing-files/Archiving-files.md) - Ability to periodically archive document handling attachments for inbound and outbound files
- [Cleanup profile](../Setup/Cleanup-profile.md) - Can be used to automatically delete staging records based on status and age days

### Automatically reset error records
- [Reset status](../Setup/Reset-status.md#retryreset-process) - Optional automatic retry by resetting Error records to Not started based on a recurrence pattern

### EDI Core documents
Review staging records. <br>
Users can access the forms by navigating to **EDI > Documents**
- [Functional acknowledgement inbound](../Documents/Functional-acknowledgement-inbound.md)
- [Functional acknowledgement outbound](../Documents/Functional-acknowledgement-outbound.md)

### Workspaces
The following workspaces are available in core EDI and will contain a tab per licensed module:
- [EDI Document maintenance](../Workspaces/EDI-Document-maintenance-workspace.md) - Manage file import and staging record errors. These records have not been successfully processed to a target D365 document

## Inquiries
The following is available for Core EDI by navigating to **EDI > Inquiries and reports**:
- [Functional acknowledgement received](../Inquiries/Functional-acknowledgement-received.md) - Provides a view of outgoing documents where the Inbound functional acknowledgement is outstanding
- [Trading partner documents](../Inquiries/Trading-partner-documents.md) - List of all EDI Trading partners and their enabled document types

## Other
- [Data entities](../Other/Data-entities.md) - Core data entities 
- [Security configuration](../Other/Security-configuration.md) - EDI security roles
- [Frequently asked questions](../OTHER/FAQ.md) - Includes example errors and recommended fixes
