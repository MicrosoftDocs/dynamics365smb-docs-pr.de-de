---
title: Aktualisieren von festen Einstandspreisen | Microsoft Docs
description: Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1f8f0bf70a72944d216f2b948224cd9f706bdff
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934235"
---
# <a name="update-standard-costs"></a><span data-ttu-id="2f457-103">Standardkosten aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2f457-103">Update Standard Costs</span></span>
<span data-ttu-id="2f457-104">Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen.</span><span class="sxs-lookup"><span data-stu-id="2f457-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="2f457-105">Der Prozess besteht in der Regel aus den folgenden vier Schritten:</span><span class="sxs-lookup"><span data-stu-id="2f457-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="2f457-106">Aktualisieren von Kosten auf der Komponenten- und Kapazitätsebene.</span><span class="sxs-lookup"><span data-stu-id="2f457-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="2f457-107">Weitere Informationen finden Sie unter dem Stapelverarbeitungsauftrag **Artikel Einst.-Preis (fest) vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="2f457-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="2f457-108">Konsolidieren Sie und rollen Sie Komponenten- und Kapazitätskosten auf, um die Gesamtkosten für Herstellung oder Montage der Artikel zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="2f457-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="2f457-109">Implementieren der festen Einstandspreise, die bei der Ausführung der obigen Batchaufträge eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f457-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="2f457-110">Die festen Einstandspreise treten erst in Kraft, wenn Sie implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2f457-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="2f457-111">Weitere Informationen finden Sie unter Mehrstufigen Einstandspreisänderungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="2f457-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="2f457-112">Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2f457-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="2f457-113">Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="2f457-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="2f457-114">Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="2f457-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="2f457-115">Einstandspreise aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2f457-115">To update standard costs</span></span>  
1.  <span data-ttu-id="2f457-116">Führen Sie die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** aus.</span><span class="sxs-lookup"><span data-stu-id="2f457-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="2f457-117">Aufruf der Stapelverarbeitung **Lagerregulierung buchen**.</span><span class="sxs-lookup"><span data-stu-id="2f457-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="2f457-118">Öffnen Sie den **Einst.-Preis (fest) Vorschlag** und verwenden Sie eine oder mehrere der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="2f457-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="2f457-119">Führen Sie die Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f457-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="2f457-120">Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="2f457-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="2f457-121">Führen Sie die Stapelverarbeitung **Einstandspreis (fest) für Kapazität vors&chlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f457-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="2f457-122">Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="2f457-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="2f457-123">Führen Sie die Stapelverarbeitung **Mehrstufigen Einstandspreis berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f457-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="2f457-124">Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="2f457-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="2f457-125">Führen Sie die Stapelverarbeitung **Einst.-Preis (fest) Vorschlag übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f457-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="2f457-126">Sehen Sie sich das  **Neubewertungs Buch.-Blatt** an, das mit Posten aus vorherigen Schritten in diesem Verfahren gefüllt wurde, und buchen Sie es.</span><span class="sxs-lookup"><span data-stu-id="2f457-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f457-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f457-127">See Also</span></span>  
 <span data-ttu-id="2f457-128">[Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="2f457-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="2f457-129">[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="2f457-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="2f457-130">[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md) [Finance](finance.md)</span><span class="sxs-lookup"><span data-stu-id="2f457-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="2f457-131">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f457-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
