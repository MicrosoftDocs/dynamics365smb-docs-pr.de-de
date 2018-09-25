---
title: "Designdetails ‑ Codebeispiele von geänderten Mustern in Änderungen | Microsoft Docs"
description: "Codebeispiele, die geänderte Muster in der Dimensionscodeänderung und -Migration für fünf unterschiedliche Szenarien anzuzeigen. Vergleicht die Codebeispiele in früheren Versionen mit den Codebeispielen in Business Central."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/13/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ded6baf8247bfbc34063f5595d42ebaf6bb300d8
ms.openlocfilehash: a20a40e0f2d7198ce8af71298093893f16df5299
ms.contentlocale: de-de
ms.lasthandoff: 08/13/2018

---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="d5217-104">Designdetails: Codebeispiele von geänderten Mustern in Änderungen</span><span class="sxs-lookup"><span data-stu-id="d5217-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="d5217-105">Dieses Thema enthält Codebeispiele, um geänderte Muster in der Dimensionscodeänderung und -Migration für fünf unterschiedliche Szenarien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d5217-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="d5217-106">Vergleicht die Codebeispiele in früheren Versionen mit den Codebeispielen in Business Central.</span><span class="sxs-lookup"><span data-stu-id="d5217-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="d5217-107">Buchen einer Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="d5217-107">Posting a Journal Line</span></span>  
<span data-ttu-id="d5217-108">Wesentliche Änderungen werden wie folgt aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="d5217-108">Key changes are listed as follows:</span></span>  
  
- <span data-ttu-id="d5217-109">Buch.-Blattzeilen-Dimensionstabellen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5217-109">Journal line dimension tables are removed.</span></span>  
  
- <span data-ttu-id="d5217-110">Eine Dimensionssatz-ID wird im Feld **Dimensionssatz-ID** erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5217-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  
  
<span data-ttu-id="d5217-111">**Frühere Versionen**</span><span class="sxs-lookup"><span data-stu-id="d5217-111">**Earlier Versions**</span></span>  
  
```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  
  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  
  
```  
  
## <a name="posting-a-document"></a><span data-ttu-id="d5217-112">Buchen eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="d5217-112">Posting a Document</span></span>  
 <span data-ttu-id="d5217-113">Wenn Sie einen Beleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] buchen, müssen Sie die Belegabmessungen nicht mehr kopieren.</span><span class="sxs-lookup"><span data-stu-id="d5217-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  
  
 <span data-ttu-id="d5217-114">**Frühere Versionen**</span><span class="sxs-lookup"><span data-stu-id="d5217-114">**Earlier Versions**</span></span>  
  
```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  
  
## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="d5217-115">Bearbeiten von Dimensionen von einem Beleg</span><span class="sxs-lookup"><span data-stu-id="d5217-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="d5217-116">Bearbeiten von Dimensionen von einem Beleg</span><span class="sxs-lookup"><span data-stu-id="d5217-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="d5217-117">Beispielsweise können Sie eine Verkaufsauftragszeile bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5217-117">For example, you can edit a sales order line.</span></span>  
  
 <span data-ttu-id="d5217-118">**Frühere Versionen**</span><span class="sxs-lookup"><span data-stu-id="d5217-118">**Earlier Versions**</span></span>  
  
```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  
  
## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="d5217-119">Anzeigen von Dimensionen von gebuchten Posten</span><span class="sxs-lookup"><span data-stu-id="d5217-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="d5217-120">Sie können Dimensionen aus gebuchten Posten anzeigen, wie Verkaufslieferzeilen.</span><span class="sxs-lookup"><span data-stu-id="d5217-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  
  
 <span data-ttu-id="d5217-121">**Frühere Versionen**</span><span class="sxs-lookup"><span data-stu-id="d5217-121">**Earlier Versions**</span></span>  
  
```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  
  
## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="d5217-122">Abrufen von Standarddimensionen für einen Beleg</span><span class="sxs-lookup"><span data-stu-id="d5217-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="d5217-123">Sie können Vorgabedimensionen für einen Beleg, wie z.B. als eine Verkaufsauftragszeile, erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5217-123">You can get default dimensions for a document, such as a sales order line.</span></span>  
  
 <span data-ttu-id="d5217-124">**Frühere Versionen**</span><span class="sxs-lookup"><span data-stu-id="d5217-124">**Earlier Versions**</span></span>  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="d5217-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5217-125">See Also</span></span>  
<span data-ttu-id="d5217-126">[Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d5217-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
<span data-ttu-id="d5217-127">[Designdetails: Tabellenstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="d5217-127">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="d5217-128">Designdetails: Codeunit 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="d5217-128">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)
