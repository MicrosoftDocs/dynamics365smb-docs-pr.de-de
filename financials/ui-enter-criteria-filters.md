---
title: Suchkriterien definieren| Microsoft Docs
description: Beschreibt, wie mit Filtern, wie Schnellfilter, gearbeitet wird, um Suchergebnisse zu verfeinern, wenn Sie Daten suchen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="199ef-103">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="199ef-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="199ef-104">Wenn Sie nach Daten, wie Debitorennamen, Adressen oder Produktgruppen suchen möchten, geben Sie Kriterien ein.</span><span class="sxs-lookup"><span data-stu-id="199ef-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="199ef-105">Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="199ef-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="199ef-106">Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="199ef-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="199ef-107">Suchen mithilfe des Schnellfilters</span><span class="sxs-lookup"><span data-stu-id="199ef-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="199ef-108">Sie können allen Seiten Filter hinzufügen, indem Sie Schnellfilter oder erweiterte Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="199ef-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="199ef-109">Der Schnellfilter wird aktiviert, indem Sie das Lupensymbol in der oberen rechten Ecke einer Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="199ef-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="199ef-110">Diese Filterart wird für die schnelle Eingabe von Kriterien verwendet.</span><span class="sxs-lookup"><span data-stu-id="199ef-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="199ef-111">Der Schnellfilter bietet einen einfachen Zugriff auf Filterdaten durch die Eingabe reinen Texts, bietet aber auch zahlreiche Optionen für Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="199ef-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="199ef-112">Abhängig davon, ob Sie Freitext oder Text mit Symbolen eingeben, verhält sich der Schnellfilter unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="199ef-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="199ef-113">Wenn Sie Freitextangaben in den Suchkriterien eingeben, werden die Suchkriterien als die Groß-/Kleinschreibung nicht beachtend angesehen.</span><span class="sxs-lookup"><span data-stu-id="199ef-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="199ef-114">Wenn Sie Text mit Symbolen in den Suchkriterien eingeben, werden die Suchkriterien genau wie angegeben interpretiert, und die Groß-/Kleinschreibung wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="199ef-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="199ef-115">Schnelle Filterkriterien</span><span class="sxs-lookup"><span data-stu-id="199ef-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="199ef-116">Suchkriterien</span><span class="sxs-lookup"><span data-stu-id="199ef-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="199ef-117">Interpretiert als...</span><span class="sxs-lookup"><span data-stu-id="199ef-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="199ef-118">Reklamationen...</span><span class="sxs-lookup"><span data-stu-id="199ef-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="199ef-119">man</span><span class="sxs-lookup"><span data-stu-id="199ef-119">man</span></span></TD>
    <TD><span data-ttu-id="199ef-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="199ef-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="199ef-121">Alle Datensätze, die den Text <b>Mann</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</span><span class="sxs-lookup"><span data-stu-id="199ef-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="199ef-122">se</span><span class="sxs-lookup"><span data-stu-id="199ef-122">se</span></span></TD>
    <TD><span data-ttu-id="199ef-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="199ef-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="199ef-124">Alle Datensätze, die den Text <b>se</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</span><span class="sxs-lookup"><span data-stu-id="199ef-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="199ef-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="199ef-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="199ef-126">Beginnt mit <b>Man</b> und Groß-/Kleinschreibung beachten</span><span class="sxs-lookup"><span data-stu-id="199ef-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="199ef-127">Alle Datensätze, die mit dem Text <b>Mann</b> beginnen.</span><span class="sxs-lookup"><span data-stu-id="199ef-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="199ef-128">'man'</span><span class="sxs-lookup"><span data-stu-id="199ef-128">'man'</span></span></TD>
    <TD><span data-ttu-id="199ef-129">Exakter Text unter Berücksichtigung der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="199ef-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="199ef-130">Alle Datensätze, die mit <b>Mann</b> genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="199ef-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="199ef-131">@man*</span><span class="sxs-lookup"><span data-stu-id="199ef-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="199ef-132">Beginnt mit, Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="199ef-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="199ef-133">Alle Datensätze, die mit <b>Mann</b> beginnen.</span><span class="sxs-lookup"><span data-stu-id="199ef-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="199ef-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="199ef-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="199ef-135">Endet mit, Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="199ef-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="199ef-136">Alle Datensätze, die mit <b>mann</b> enden.</span><span class="sxs-lookup"><span data-stu-id="199ef-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="199ef-137">Sie können keinen Platzhalter beim Filtern in Aufzählungsfeldern, wie das Feld **Status** in Verkaufsaufträgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="199ef-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="199ef-138">Wenn Sie einen Filter für diese Art von Feld eingeben möchten, können Sie den numerischen Wert als Filterparameter eingeben.</span><span class="sxs-lookup"><span data-stu-id="199ef-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="199ef-139">Beispielsweise im Feld **Status** in einem Verkaufsauftrag, der die Werte **Offen**, **Freigegeben**, **Genehmigung ausstehend** und **Vorauszahlung ausstehend** hat, verwenden Sie die Werte **0**, **1**, **2** und **3**, um für diese Optionen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="199ef-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="199ef-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="199ef-140">See Also</span></span>
<span data-ttu-id="199ef-141">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="199ef-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

