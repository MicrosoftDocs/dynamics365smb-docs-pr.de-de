---
title: Gebuchte Einkaufs- und Verkaufsbelege bearbeiten | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Einkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1041dda83552af3c2c805c08518600d89f0467fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188732"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="4424e-103">Gebuchte Belege bearbeiten</span><span class="sxs-lookup"><span data-stu-id="4424e-103">Edit Posted Documents</span></span>
<span data-ttu-id="4424e-104">Manchmal müssen Sie einen gebuchten Beleg aktualisieren, da sich die für das Dokument relevanten Informationen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="4424e-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="4424e-105">Bei einem gebuchten Verkaufsbeleg kann dies beispielsweise die Paketverfolgungsnummer des Zustellers sein.</span><span class="sxs-lookup"><span data-stu-id="4424e-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="4424e-106">Bei einem gebuchten Einkaufsbeleg kann es sich um einen Zahlungsreferenztext handeln.</span><span class="sxs-lookup"><span data-stu-id="4424e-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="4424e-107">Sie führen die Änderung an einer bearbeitbaren Version des Originaldokuments durch, was durch „**- Update**“ im Seitentitel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4424e-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="4424e-108">Die Seite enthält eine Teilmenge der Felder im Originaldokument, von denen einige nicht bearbeitbare Felder sind, die nur zu Informationszwecken angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4424e-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="4424e-109">Die Funktionalität ist für folgende Dokumente in allen Länderversionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4424e-109">The functionality is available for the following documents in all country versions:</span></span>
- <span data-ttu-id="4424e-110">Geb. Verkaufslieferung</span><span class="sxs-lookup"><span data-stu-id="4424e-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="4424e-111">Geb. Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="4424e-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="4424e-112">Gebuchte Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="4424e-112">Posted Return Shipment</span></span>
- <span data-ttu-id="4424e-113">Gebuchte Rücksendung</span><span class="sxs-lookup"><span data-stu-id="4424e-113">Posted Return Receipt</span></span>

<span data-ttu-id="4424e-114">Die folgenden zusätzlichen Dokumente können in ausgewählten Länderversionen bearbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="4424e-114">The following additional documents can be edited in selected country versions:</span></span>
- <span data-ttu-id="4424e-115">ES: Gebuchte Verkaufsrechnung, Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift</span><span class="sxs-lookup"><span data-stu-id="4424e-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="4424e-116">APAC: Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift</span><span class="sxs-lookup"><span data-stu-id="4424e-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="4424e-117">RU: Geb. Verkaufsgutschrift</span><span class="sxs-lookup"><span data-stu-id="4424e-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="4424e-118">IT: Geb. Umlag.-Ausgang, Gebuchte Servicelieferung</span><span class="sxs-lookup"><span data-stu-id="4424e-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="4424e-119">So bearbeiten Sie eine gebuchte Verkaufslieferung</span><span class="sxs-lookup"><span data-stu-id="4424e-119">To edit a posted sales shipment</span></span>
<span data-ttu-id="4424e-120">Im Folgenden wird erläutert, wie Sie eine gebuchte Verkaufslieferung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4424e-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="4424e-121">Die Schritte sind für die anderen unterstützten Dokumente ähnlich.</span><span class="sxs-lookup"><span data-stu-id="4424e-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="4424e-122">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="4424e-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="4424e-123">Wählen Sie das zu bearbeitende Dokument aus, und wählen Sie anschließend die Aktion **Beleg aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4424e-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="4424e-124">Alternativ können Sie das Dokument öffnen und dann die Aktion auswählen.</span><span class="sxs-lookup"><span data-stu-id="4424e-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="4424e-125">Auf der Seite **Gebuchte Verkaufslieferungen - Update** bearbeiten Sie das Feld **Paketverfolgungsnr.**</span><span class="sxs-lookup"><span data-stu-id="4424e-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="4424e-126">zum Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4424e-126">field, for example.</span></span>
4. <span data-ttu-id="4424e-127">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4424e-127">Choose the **OK** button.</span></span>

<span data-ttu-id="4424e-128">Die gebuchte Verkaufslieferung wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4424e-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="4424e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4424e-129">See Also</span></span>
[<span data-ttu-id="4424e-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4424e-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="4424e-131">Einkauf</span><span class="sxs-lookup"><span data-stu-id="4424e-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4424e-132">Journale und Dokumente buchen</span><span class="sxs-lookup"><span data-stu-id="4424e-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="4424e-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4424e-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
