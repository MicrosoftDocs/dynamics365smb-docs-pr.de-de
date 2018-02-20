---
title: 'Designdetails: Suche nach Dimensionskombinationen | Microsoft Docs'
description: "Wenn Sie ein Fenster schließen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft Finance and Operations, Business edition, ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist. Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 821ddebee02d1ea922c0c13a181ae0e29e4eb40e
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="29274-104">Designdetails: Suche nach Dimensionskombinationen</span><span class="sxs-lookup"><span data-stu-id="29274-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="29274-105">Wenn Sie ein Fenster schließen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)], ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29274-105">When you close a window after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="29274-106">Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29274-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="29274-107">Erstellungs-Suchstruktur</span><span class="sxs-lookup"><span data-stu-id="29274-107">Building Search Tree</span></span>  
 <span data-ttu-id="29274-108">Tabelle 481 D**imensionssatz-Strukturknoten** wird verwendet, wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft, ob ein Satz von Dimensionen bereits in Tabelle 480 **Dimensionssatzposten** existiert.</span><span class="sxs-lookup"><span data-stu-id="29274-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="29274-109">Die Auswertung wird ausgeführt, indem die Suchstruktur rekursiv verläuft, beginnend bei der oben ausgerichteten numerierte 0.</span><span class="sxs-lookup"><span data-stu-id="29274-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="29274-110">Die oberste Ebene 0 stellt einen Dimensionssatz ohne Dimensionssatzposten dar.</span><span class="sxs-lookup"><span data-stu-id="29274-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="29274-111">Die untergeordneten Elemente dieses Dimensionssatzes stellen Dimensionssätze mit nur einem Dimensionssatzposten dar.</span><span class="sxs-lookup"><span data-stu-id="29274-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="29274-112">Die untergeordneten Elemente dieser Dimensionssätze stellen Dimensionssätze mit zwei untergeordneten Elementen dar usw.</span><span class="sxs-lookup"><span data-stu-id="29274-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="29274-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29274-113">Example 1</span></span>  
 <span data-ttu-id="29274-114">Das folgende Diagramm stellt eine Suchstruktur mit sechs Dimensionssätzen dar.</span><span class="sxs-lookup"><span data-stu-id="29274-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="29274-115">Nur der unterscheidene Dimensionssatzposten wird im Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29274-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="29274-116">![Dimensionsstruktur Datenträger](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span><span class="sxs-lookup"><span data-stu-id="29274-116">![Dimension tree structure](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span></span>  

 <span data-ttu-id="29274-117">Die folgende Tabelle enthält eine vollständige Liste der Dimensionssatzposten, die jeden Dimensionssatz ergeben.</span><span class="sxs-lookup"><span data-stu-id="29274-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="29274-118">Dimensionssätze</span><span class="sxs-lookup"><span data-stu-id="29274-118">Dimension Sets</span></span>|<span data-ttu-id="29274-119">Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="29274-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="29274-120">0 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-120">Set 0</span></span>|<span data-ttu-id="29274-121">Keine</span><span class="sxs-lookup"><span data-stu-id="29274-121">None</span></span>|  
|<span data-ttu-id="29274-122">1 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-122">Set 1</span></span>|<span data-ttu-id="29274-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="29274-123">AREA 30</span></span>|  
|<span data-ttu-id="29274-124">2 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-124">Set 2</span></span>|<span data-ttu-id="29274-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="29274-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="29274-126">3 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-126">Set 3</span></span>|<span data-ttu-id="29274-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="29274-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="29274-128">4 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-128">Set 4</span></span>|<span data-ttu-id="29274-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="29274-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="29274-130">5 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-130">Set 5</span></span>|<span data-ttu-id="29274-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="29274-131">AREA 40</span></span>|  
|<span data-ttu-id="29274-132">6 Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="29274-132">Set 6</span></span>|<span data-ttu-id="29274-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="29274-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="29274-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="29274-134">Example 2</span></span>  
 <span data-ttu-id="29274-135">In diesem Beispiel wird gezeigt, wie [!INCLUDE[d365fin](includes/d365fin_md.md)] bestimmt, ob ein Dimensionssatz, der aus den Dimensionssatzposten AREA 40, DEPT PROD besteht, vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29274-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="29274-136">Außerdem aktualisiert[!INCLUDE[d365fin](includes/d365fin_md.md)] die Tabelle **Dimensionssatz-Strukturknoten**, um sicherzustellen, dass die Suchstruktur wie das folgende Diagramm aussieht.</span><span class="sxs-lookup"><span data-stu-id="29274-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="29274-137">Daher wird Dimensionssatz 7 zu einem untergeordneten Element des Dimensionssatzes 5.</span><span class="sxs-lookup"><span data-stu-id="29274-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="29274-138">![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span><span class="sxs-lookup"><span data-stu-id="29274-138">![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="29274-139">Suchen der Dimensionssatz-ID</span><span class="sxs-lookup"><span data-stu-id="29274-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="29274-140">Auf konzeptioneller Ebene werden **Übergeordnete Kennung**, **Dimension** und **Dimensionswert**, in der Suchstruktur, als Primärschlüssel kombiniert und verwendet, da [!INCLUDE[d365fin](includes/d365fin_md.md)] die Struktur in derselben Reihenfolge wie die Dimensionsposten durchläuft.</span><span class="sxs-lookup"><span data-stu-id="29274-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="29274-141">Die GET-Funktion (Datensatz) wird verwendet, um nach der Dimensionssatz-ID zu suchen</span><span class="sxs-lookup"><span data-stu-id="29274-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="29274-142">Das folgende Codebeispiel zeigt, wie Sie die Dimensionssatz-ID finden, wenn es drei Dimensionswerte gibt.</span><span class="sxs-lookup"><span data-stu-id="29274-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 <span data-ttu-id="29274-143">Um jedoch die Möglichkeit von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu gewährleisten, eine Dimension und einen Dimensionswert umzubenennen, wird die Tabelle 348 **Dimensionswert** mit einem ganzzahligen Feld aus **Dimensionswert-ID** erweitert.</span><span class="sxs-lookup"><span data-stu-id="29274-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename a dimension and dimension value, table 348 **Dimension Value** is extended with an integer field of **Dimension Value ID**.</span></span> <span data-ttu-id="29274-144">Diese Tabelle wandelt die Feldpaare **Dimension** und **Dimensionswert** zu einem ganzzahligen Wert um.</span><span class="sxs-lookup"><span data-stu-id="29274-144">This table converts the field pair **Dimension** and **Dimension Value** to an integer value.</span></span> <span data-ttu-id="29274-145">Wenn Sie die Dimension sowie den Dimensionswert umbenennen, wird der ganzzahlige Wert nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="29274-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="29274-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29274-146">See Also</span></span>  
 <span data-ttu-id="29274-147">[Funktion ABRUFEN (Datensatz)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="29274-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="29274-148">[Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="29274-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="29274-149">[Dimensionssatz-Eintrags-Übersicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="29274-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="29274-150">[Designdetails: Tabellenstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="29274-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="29274-151">[Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="29274-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="29274-152">Designdetails: Codebeispiele von geänderten Mustern in Änderungen</span><span class="sxs-lookup"><span data-stu-id="29274-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

