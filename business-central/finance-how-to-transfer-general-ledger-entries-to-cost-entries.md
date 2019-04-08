---
title: 'Vorgehensweise: Übertragen von Sachposten in Kostenposten | Microsoft Docs'
description: Sie können Sachposten in Kostenposten übertragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799117"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="df33d-103">So übertragen Sie Sachposten in Kostenposten</span><span class="sxs-lookup"><span data-stu-id="df33d-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="df33d-104">Sie können Sachposten in Kostenposten übertragen.</span><span class="sxs-lookup"><span data-stu-id="df33d-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="df33d-105">Bevor Sie den Vorgang für das Übertragen von Sachposten in Kostenposten durchführen, müssen Sie die Übertragung vorbereiten, um manuelle Korrekturbuchungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="df33d-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="df33d-106">So bereiten Sie die Übertragung vor</span><span class="sxs-lookup"><span data-stu-id="df33d-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="df33d-107">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenrechnung einrichten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="df33d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="df33d-108">Stellen Sie auf der Seite **Kostenrechnungseinrichtung** sicher, dass im Feld **Startdatum für Sachkontenübertragung** der richtige Wert eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="df33d-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="df33d-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kontenarten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="df33d-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="df33d-110">Auf der Seite **Kostenartkarte** prüfen Sie, dass das **Sachkontobereich** Feld für jede Kostenart korrekt verknüpft ist, um Posten aus dem Sachkonto zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="df33d-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="df33d-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="df33d-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="df33d-112">Überprüfen Sie für jedes Sachkonto auf der Seite **Sachkontokarte**, ob die **Kostenartnr.**</span><span class="sxs-lookup"><span data-stu-id="df33d-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="df33d-113">Feld wird korrekt zu einer Kostenart verknüpft.</span><span class="sxs-lookup"><span data-stu-id="df33d-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="df33d-114">Weitere Informationen finden Sie unter [Einrichten von Kostenrechnung](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="df33d-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="df33d-115">Vergewissern Sie sich, dass alle entsprechenden Sachposten Dimensionswerte haben, die einer Kostenstelle und zu einem Kostenträger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="df33d-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="df33d-116">So übertragen Sie Sachposten in Kostenposten</span><span class="sxs-lookup"><span data-stu-id="df33d-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="df33d-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transfer-Einträge‌ in CA** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="df33d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="df33d-118">Wählen Sie auf Schaltfläche **OK**, um die Umlagerung zu starten.</span><span class="sxs-lookup"><span data-stu-id="df33d-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="df33d-119">Der Prozess überträgt alle Sachposten, die nicht bereits übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="df33d-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="df33d-120">Während der Übertragung erstellt der Vorgang Verknüpfungen in den Posten **Posteneintrag** und **Kostentabelle**.</span><span class="sxs-lookup"><span data-stu-id="df33d-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="df33d-121">Dies ermöglicht es Ihnen, die Herkunft von Kostenposten nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="df33d-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df33d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df33d-122">See Also</span></span>  
<span data-ttu-id="df33d-123">[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="df33d-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="df33d-124">Einrichten der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="df33d-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
