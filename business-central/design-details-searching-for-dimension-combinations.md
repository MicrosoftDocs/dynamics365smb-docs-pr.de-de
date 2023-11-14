---
title: 'Designdetails: Suche nach Dimensionskombinationen | Microsoft Docs'
description: 'Wenn Sie eine Seite schließen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft Business Central, ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist. Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Designdetails: Suche nach Dimensionskombinationen
Wenn Sie eine Seite schließen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft [!INCLUDE[prod_short](includes/prod_short.md)], ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist. Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben.  

## Erstellungs-Suchstruktur  
 Tabelle 481 **Dimensionssatz-Strukturknoten** wird verwendet, wenn [!INCLUDE[prod_short](includes/prod_short.md)] prüft, ob ein Satz von Dimensionen bereits in Tabelle 480 **Dimensionssatzposten** existiert. Die Auswertung wird ausgeführt, indem die Suchstruktur rekursiv verläuft, beginnend bei der oben ausgerichteten numerierte 0. Die oberste Ebene 0 stellt einen Dimensionssatz ohne Dimensionssatzposten dar. Die untergeordneten Elemente dieses Dimensionssatzes stellen Dimensionssätze mit nur einem Dimensionssatzposten dar. Die untergeordneten Elemente dieser Dimensionssätze stellen Dimensionssätze mit zwei untergeordneten Elementen dar usw.  

### Beispiel 1  
 Das folgende Diagramm stellt eine Suchstruktur mit sechs Dimensionssätzen dar. Nur der unterscheidene Dimensionssatzposten wird im Diagramm angezeigt.  

 ![Beispiel für die Struktur eines Dimensionsbaums.](media/nav2013_dimension_tree.png "Beispiel einer Dimensionsbaumstruktur")  

 Die folgende Tabelle enthält eine vollständige Liste der Dimensionssatzposten, die jeden Dimensionssatz ergeben.  

|Dimensionssätze|Dimensionssatzposten|  
|--------------------|---------------------------|  
|0 Ausgewählt|Keine|  
|1 Ausgewählt|AREA 30|  
|2 Ausgewählt|AREA 30, DEPT ADM|  
|3 Ausgewählt|AREA 30, DEPT PROD|  
|4 Ausgewählt|AREA 30, DEPT ADM, PROJ VW|  
|5 Ausgewählt|AREA 40|  
|6 Ausgewählt|AREA 40, PROJ VW|  

### Beispiel 2  
 In diesem Beispiel wird gezeigt, wie [!INCLUDE[prod_short](includes/prod_short.md)] bestimmt, ob ein Dimensionssatz, der aus den Dimensionssatzposten AREA 40, DEPT PROD besteht, vorhanden ist.  

 Außerdem aktualisiert [!INCLUDE[prod_short](includes/prod_short.md)] die Tabelle **Dimensionssatz-Strukturknoten**, um sicherzustellen, dass die Suchstruktur wie das folgende Diagramm aussieht. Daher wird Dimensionssatz 7 zu einem untergeordneten Element des Dimensionssatzes 5.  

 ![Beispiel für die Struktur des Dimensionsbaums in NAV 2013.](media/nav2013_dimension_tree_example2.png "Beispiel einer Dimensionsbaumstruktur in NAV 2013")  

### Suchen der Dimensionssatz-ID  
 Auf konzeptioneller Ebene werden **Übergeordnete Kennung**, **Dimension** und **Dimensionswert**, in der Suchstruktur, als Primärschlüssel kombiniert und verwendet, da [!INCLUDE[prod_short](includes/prod_short.md)] die Struktur in derselben Reihenfolge wie die Dimensionsposten durchläuft. Die GET-Funktion (Datensatz) wird verwendet, um nach der Dimensionssatz-ID zu suchen Das folgende Codebeispiel zeigt, wie Sie die Dimensionssatz-ID finden, wenn es drei Dimensionswerte gibt.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Um jedoch die Möglichkeit von [!INCLUDE[prod_short](includes/prod_short.md)] zu gewährleisten, um eine Dimension und einen Dimensionswert umzubenennen, wird die Tabelle 349 **Dimensionswert** mit einem ganzzahligen Feld **Dimensionswert-ID** erweitert. Diese Tabelle wandelt die Feldpaare **Dimension** und **Dimensionswert** zu einem ganzzahligen Wert um. Wenn Sie die Dimension sowie den Dimensionswert umbenennen, wird der ganzzahlige Wert nicht geändert.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## Siehe auch
    
 [Designdetails: Dimensionssatzposten](/dynamics365/business-central/design-details-dimension-set-entries-overview)   
 [Dimensionssatz-Eintrags-Übersicht](design-details-dimension-set-entries-overview.md)   
 [Designdetails: Tabellenstruktur](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]