---
title: Die allgemeine Lagereinrichtung definieren
description: Beschreibt, wie Sie die allgemeine Lagereinrichtung definieren, damit Sie Ihr Lager und Ihren Lagerbestand verwalten können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 10344ae85edc8a63dcff1a5a5927bf2d19045810
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389399"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="eadef-103">So richten Sie allgemeine Lagerbestandsinformationen ein</span><span class="sxs-lookup"><span data-stu-id="eadef-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="eadef-104">Sie geben Ihre allgemeine Lagerbestandseinrichtung auf der Seite **Lager Einrichtung** an.</span><span class="sxs-lookup"><span data-stu-id="eadef-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="eadef-105">So richten Sie allgemeine Lagerbestandsinformationen ein</span><span class="sxs-lookup"><span data-stu-id="eadef-105">To set up general inventory information</span></span>

1. <span data-ttu-id="eadef-106">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Bestandseinrichtung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="eadef-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="eadef-107">Füllen Sie auf der Seite **Lager Einrichtung** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="eadef-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="eadef-108">Detaillierte Informationen zu den Kalkulationsfeldern **Automatische Kostenbuchung**, **Erwartete Kostenbuchung in Sachkonten** und **Standardmäßige Lagerabgangsmethode** finden Sie unter [Lagerkosten mit dem Hauptbuch abstimmen](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Entwurfsdetails: Lagernachkalkulation](design-details-inventory-costing.md) und [Entwurfsdetails: Buchung erwarteter Kosten](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="eadef-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="eadef-109">Weitere Informationen zur Kalkulation im Allgemeinen finden Sie unter [Lagerkosten verwalten](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="eadef-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="eadef-110">Wenn Sie möchten, dass die Anwendung die Lagerdurchlaufzeit bei der Berechnung der Lieferterminzusage in der Einkaufszeile berücksichtigt, können Sie sie als Vorgabewert für das Lager und für Ihren Lagerort im **Lager einrichten** einrichten.</span><span class="sxs-lookup"><span data-stu-id="eadef-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="eadef-111">Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="eadef-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="eadef-112">Der Umschalter **Automatischer Kostenausgleich** ist standardmäßig aktiviert, um sicherzustellen, dass Bestandswerte in der Finanzbuchhaltung immer korrekt sind, wodurch Ihre Umsatz- und Gewinnstatistik auf dem neuesten Stand gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="eadef-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="eadef-113">Kostenänderungen aus eingehenden Posten, wie diejenigen für Einkäufe oder Produktionsausstoß werden den zugehörigen ausgehenden Posten zugewiesen, wie z. B. Verkäufe oder Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="eadef-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="eadef-114">Dies ist hilfreich für neue [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren und kleine Unternehmen mit relativ geringem Lagerbestandstransaktionsumfang.</span><span class="sxs-lookup"><span data-stu-id="eadef-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="eadef-115">Wenn ein Unternehmen jedoch wächst und die Lagerebenen zunehmen, kann dies die Systemleistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="eadef-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="eadef-116">Um die Leistungsminderung während der Buchung zu minimieren, wählen Sie eine Zeitoption aus, um zu definieren, wie weit zurück vor dem Arbeitsdatum eine eingehende Transaktion erfolgen kann, um möglicherweise einen Ausgleich verknüpfter ausgehender Wertposten auszulösen.</span><span class="sxs-lookup"><span data-stu-id="eadef-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="eadef-117">Alternativ können Sie die Kosten in regelmäßigen Abständen manuell mit dem Stapelverarbeitungsauftrag „Kosten ausgleichen – Artikelposten“ ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="eadef-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="eadef-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eadef-118">See Also</span></span>
[<span data-ttu-id="eadef-119">Lager einrichten</span><span class="sxs-lookup"><span data-stu-id="eadef-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="eadef-120">[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="eadef-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="eadef-121">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="eadef-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="eadef-122">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eadef-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="eadef-123">Ändern, welche Merkmale angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="eadef-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="eadef-124">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="eadef-124">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]