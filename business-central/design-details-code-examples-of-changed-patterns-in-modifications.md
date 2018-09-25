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
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a>Designdetails: Codebeispiele von geänderten Mustern in Änderungen
Dieses Thema enthält Codebeispiele, um geänderte Muster in der Dimensionscodeänderung und -Migration für fünf unterschiedliche Szenarien anzuzeigen. Vergleicht die Codebeispiele in früheren Versionen mit den Codebeispielen in Business Central.

## <a name="posting-a-journal-line"></a>Buchen einer Buch.-Blattzeile.  
Wesentliche Änderungen werden wie folgt aufgelistet:  
  
- Buch.-Blattzeilen-Dimensionstabellen werden entfernt.  
  
- Eine Dimensionssatz-ID wird im Feld **Dimensionssatz-ID** erstellt.  
  
**Frühere Versionen**  
  
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
  
## <a name="posting-a-document"></a>Buchen eines Dokuments  
 Wenn Sie einen Beleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] buchen, müssen Sie die Belegabmessungen nicht mehr kopieren.  
  
 **Frühere Versionen**  
  
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
  
## <a name="editing-dimensions-from-a-document"></a>Bearbeiten von Dimensionen von einem Beleg  
 Bearbeiten von Dimensionen von einem Beleg Beispielsweise können Sie eine Verkaufsauftragszeile bearbeiten.  
  
 **Frühere Versionen**  
  
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
  
## <a name="showing-dimensions-from-posted-entries"></a>Anzeigen von Dimensionen von gebuchten Posten  
 Sie können Dimensionen aus gebuchten Posten anzeigen, wie Verkaufslieferzeilen.  
  
 **Frühere Versionen**  
  
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
  
## <a name="getting-default-dimensions-for-a-document"></a>Abrufen von Standarddimensionen für einen Beleg  
 Sie können Vorgabedimensionen für einen Beleg, wie z.B. als eine Verkaufsauftragszeile, erhalten.  
  
 **Frühere Versionen**  
  
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

## <a name="see-also"></a>Siehe auch  
[Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md)   
[Designdetails: Tabellenstruktur](design-details-table-structure.md)   
[Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md)
