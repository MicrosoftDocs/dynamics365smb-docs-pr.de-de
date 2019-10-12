---
title: Automatische Übertragung und kombinierte Posten | Microsoft Docs
description: In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0c07e470c1df8b9d9b5e7f7c833ff83b3c61be69
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306436"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="10e90-105">Automatische Übertragung und kombinierte Posten</span><span class="sxs-lookup"><span data-stu-id="10e90-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="10e90-106">In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden.</span><span class="sxs-lookup"><span data-stu-id="10e90-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="10e90-107">Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="10e90-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="10e90-108">Die drei Optionen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="10e90-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="10e90-109">Posten kombinieren</span><span class="sxs-lookup"><span data-stu-id="10e90-109">Combine entries</span></span>|<span data-ttu-id="10e90-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10e90-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="10e90-111">"Keine"</span><span class="sxs-lookup"><span data-stu-id="10e90-111">None</span></span>|<span data-ttu-id="10e90-112">Jeder Sachposten wird einzeln in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="10e90-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="10e90-113">Tag</span><span class="sxs-lookup"><span data-stu-id="10e90-113">Day</span></span>|<span data-ttu-id="10e90-114">Sachposten mit dem gleichen Buchungsdatum werden wie ein Posten in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="10e90-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="10e90-115">Monat</span><span class="sxs-lookup"><span data-stu-id="10e90-115">Month</span></span>|<span data-ttu-id="10e90-116">Alle Sachposten im selben Kalendermonat werden wie ein Posten in die entsprechende Kostenart umgelagert.</span><span class="sxs-lookup"><span data-stu-id="10e90-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="10e90-117">Wenn Sie das Kontrollkästchen **Automatischer Übertrag vom Buch-Blatt** auf der Seite **Kostenrechnung einrichten** aktiviert haben, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kostenrechnung nach jeder Buchung in der Finanzbuchhaltung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="10e90-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="10e90-118">Kombinierte Posten sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="10e90-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10e90-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10e90-119">See Also</span></span>  
 <span data-ttu-id="10e90-120">[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="10e90-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="10e90-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10e90-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
