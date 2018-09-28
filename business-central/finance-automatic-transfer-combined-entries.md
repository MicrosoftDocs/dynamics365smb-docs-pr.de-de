---
title: "Automatische Übertragung und kombinierte Posten | Microsoft Docs"
description: "In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d33fa549f48731c49734e7ecaf65b461c375ec90
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="fbd4f-105">Automatische Übertragung und kombinierte Posten</span><span class="sxs-lookup"><span data-stu-id="fbd4f-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="fbd4f-106">In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="fbd4f-107">Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="fbd4f-108">Die drei Optionen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="fbd4f-109">Posten kombinieren</span><span class="sxs-lookup"><span data-stu-id="fbd4f-109">Combine entries</span></span>|<span data-ttu-id="fbd4f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbd4f-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="fbd4f-111">"Keine"</span><span class="sxs-lookup"><span data-stu-id="fbd4f-111">None</span></span>|<span data-ttu-id="fbd4f-112">Jeder Sachposten wird einzeln in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="fbd4f-113">Tag</span><span class="sxs-lookup"><span data-stu-id="fbd4f-113">Day</span></span>|<span data-ttu-id="fbd4f-114">Sachposten mit dem gleichen Buchungsdatum werden wie ein Posten in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="fbd4f-115">Monat</span><span class="sxs-lookup"><span data-stu-id="fbd4f-115">Month</span></span>|<span data-ttu-id="fbd4f-116">Alle Sachposten im selben Kalendermonat werden wie ein Posten in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="fbd4f-117">Wenn Sie das Kontrollkästchen **Automatischer Übertrag vom Buch-Blatt** im Fenster **Kostenrechnung einrichten** aktiviert haben, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kostenrechnung nach jeder Buchung in der Finanzbuchhaltung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="fbd4f-118">Kombinierte Posten sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="fbd4f-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fbd4f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbd4f-119">See Also</span></span>  
 <span data-ttu-id="fbd4f-120">[So übertragen Sie Sachposten in Kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="fbd4f-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="fbd4f-121">[Kriterien für die Übertragung von Sachposten in Kostenposten](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="fbd4f-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="fbd4f-122">[Ergebnisse der Übertragung](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="fbd4f-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="fbd4f-123">Übertragung und Buchung von Kostenzuteilungen</span><span class="sxs-lookup"><span data-stu-id="fbd4f-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="fbd4f-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbd4f-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

