---
title: "Kriterien für die Übertragung von Sachposten in Kostenposten | Microsoft Docs"
description: "Es ist wichtig, die Kriterien für den Transfer von Sachposten in Kostenposten zu kennen. Während des Transfers verwendet der Batchauftrag **Sachposten in Kostenrechnung übertragen** die folgenden Kriterien, um zu ermitteln, ob und wie die Sachposten transferiert werden sollen."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 67cc593691b4d3fe6a13cd960dce150c1e552da0
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="d8edb-104">Kriterien für die Übertragung von Sachposten in Kostenposten</span><span class="sxs-lookup"><span data-stu-id="d8edb-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="d8edb-105">Es ist wichtig, die Kriterien für den Transfer von Sachposten in Kostenposten zu kennen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="d8edb-106">Während des Transfers verwendet der Batchauftrag **Sachposten in Kostenrechnung übertragen** die folgenden Kriterien, um zu ermitteln, ob und wie die Sachposten transferiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="d8edb-107">Sachposten werden transferiert, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="d8edb-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="d8edb-108">Die Posten haben Dimensionswerte, die entweder einer Kostenstelle oder einem Kostenträger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="d8edb-109">Die Posten haben Dimensionswerte, die einer Kostenstelle und einem Kostenträger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="d8edb-110">Bei diesen Posten hat die Kostenstelle Vorrang.</span><span class="sxs-lookup"><span data-stu-id="d8edb-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="d8edb-111">Dies ist hilfreich, um eine Situation zu vermeiden, in der eine Kostenart sowohl in einem Kostenträger als auch in einer Kostenstelle auftritt und daher in der Statistik zweimal gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="d8edb-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="d8edb-112">Die Belegnummer in den Posten ist leer, sodass sie mit einer Belegnummer von 0000 in den Kostenposten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8edb-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="d8edb-113">Die Posten werden in eine Kostenart transferiert, die kombinierte Posten zulässt, und diese Posten werden als kombinierter monatlicher oder täglicher Posten transferiert.</span><span class="sxs-lookup"><span data-stu-id="d8edb-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="d8edb-114">Sachposten werden nicht transferiert, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="d8edb-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="d8edb-115">Die Posten haben Dimensionswerte, die weder einer Kostenstelle noch einem Kostenträger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="d8edb-116">Die Posten weisen einen Betrag von Null auf.</span><span class="sxs-lookup"><span data-stu-id="d8edb-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="d8edb-117">Die Posten haben ein Sachkonto, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d8edb-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="d8edb-118">Die Posten haben ein Sachkonto, das nicht vom Typ **GuV** ist.</span><span class="sxs-lookup"><span data-stu-id="d8edb-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="d8edb-119">Die Posten haben ein Sachkonto, dem keine Kostenart zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8edb-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="d8edb-120">Die Posten haben ein Buchungsdatum vor **Startdatum für Sachkontenübertragung**.</span><span class="sxs-lookup"><span data-stu-id="d8edb-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="d8edb-121">Die Posten wurden mit einem Abschlussdatum gebucht.</span><span class="sxs-lookup"><span data-stu-id="d8edb-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="d8edb-122">Dies sind typische Posten, die den Saldo der GuV am Ende des Geschäftsjahres zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="d8edb-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8edb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8edb-123">See Also</span></span>  
[<span data-ttu-id="d8edb-124">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="d8edb-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="d8edb-125">[So übertragen Sie Sachposten in Kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d8edb-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="d8edb-126">[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d8edb-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="d8edb-127">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="d8edb-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="d8edb-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8edb-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

