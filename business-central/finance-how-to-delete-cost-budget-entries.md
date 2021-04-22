---
title: "So geht's: Kostenbudgetposten löschen | Microsoft Docs"
description: Sie verwenden den Batchauftrag Kostenbudgeteinträge löschen , um Kostenbudgetposten in der Kostenbudgeterfassung zu stornieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e2f05388149e9e6587f916db79b652e64ad5d02e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774839"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="628f7-103">Kostenbudgetposten löschen</span><span class="sxs-lookup"><span data-stu-id="628f7-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="628f7-104">Sie verwenden den Batchauftrag **Kostenbudgeteinträge löschen** , um Kostenbudgetposten in der Kostenbudgeterfassung zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="628f7-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="628f7-105">Um keine Lücken in den Kostenbudgetposten und den Kostenjournalposten entstehen zu lassen, können Sie einen einzelnen Posten oder eine Gruppe von Posten nicht mitten in der Liste der Journalposten löschen.</span><span class="sxs-lookup"><span data-stu-id="628f7-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="628f7-106">Kostenbudgetposten löschen:</span><span class="sxs-lookup"><span data-stu-id="628f7-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="628f7-107">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kostenbudgeteinträge löschen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="628f7-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="628f7-108">Die **Zu-Register-Nr.**</span><span class="sxs-lookup"><span data-stu-id="628f7-108">The **To Register No.**</span></span> <span data-ttu-id="628f7-109">Das Feld enthält die letzte Journalpostennummer und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="628f7-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="628f7-110">Sie können **Von Journalnr.** verwenden</span><span class="sxs-lookup"><span data-stu-id="628f7-110">You can use the **From Register No.**</span></span> <span data-ttu-id="628f7-111">Sie können das Feld verwenden, um eine Journalpostennummer auszuwählen, ab der der Löschvorgang beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="628f7-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="628f7-112">Wählen Sie die Schaltfläche **OK** aus, um die ausgewählten Kostenbudgetposten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="628f7-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="628f7-113">Um ein versehentliches Löschen von Kostenbudgetposten zu vermeiden, können Sie Journalposten schließen, indem Sie die Zeilen als **Abgeschlossen** im Feld **Abgeschlossen** auf der Seite **Kostenbudget-Register** markieren.</span><span class="sxs-lookup"><span data-stu-id="628f7-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="628f7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="628f7-114">See Also</span></span>  
<span data-ttu-id="628f7-115">[Kostenrechnung](finance-manage-cost-accounting.md)
[Erstellen von Kostenbudgets](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="628f7-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="628f7-116">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="628f7-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]