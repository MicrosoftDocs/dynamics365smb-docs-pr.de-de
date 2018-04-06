---
title: "So geben Sie Dimensionen für den Inventurauftrag ein"
description: "Nachdem Sie einen Inventurauftrag erstellt haben, können Sie Dimensionen für diesen Auftrag eingeben."
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
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c3c11795ebb2061a18430b36ddaac8613d51ad58
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="enter-dimensions-for-physical-inventory-orders"></a><span data-ttu-id="ae382-103">So geben Sie Dimensionen für den physischen Inventurauftrag ein</span><span class="sxs-lookup"><span data-stu-id="ae382-103">Enter Dimensions for Physical Inventory Orders</span></span>
<span data-ttu-id="ae382-104">Nachdem Sie einen Inventurauftrag erstellt haben, können Sie Dimensionen für diesen Auftrag eingeben.</span><span class="sxs-lookup"><span data-stu-id="ae382-104">After you have created a physical inventory order, you can enter dimensions for this order.</span></span>  

<span data-ttu-id="ae382-105">Die Anwendung unterscheidet zwischen Dimensionen für den Inventurauftragskopf und Dimensionen für die Inventurauftragszeilen.</span><span class="sxs-lookup"><span data-stu-id="ae382-105">The application distinguishes between the dimensions for the physical inventory order header and the dimensions for the physical inventory order lines.</span></span> <span data-ttu-id="ae382-106">Die Dimensionen für den Inventurauftragskopf sind ein Muster für die Dimensionen der Inventurauftragszeilen.</span><span class="sxs-lookup"><span data-stu-id="ae382-106">The dimensions of the physical inventory header are a pattern for the dimensions of the physical inventory order lines.</span></span> <span data-ttu-id="ae382-107">Jedes Mal, wenn (manuell oder automatisch) eine neue Inventurauftragszeile erstellt wird, überträgt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die Dimensionen aus dem Kopf in die neue Zeile.</span><span class="sxs-lookup"><span data-stu-id="ae382-107">Every time you create a new physical inventory order line manually or automatically, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] will transfer the dimensions from the header to the new line.</span></span>  

<span data-ttu-id="ae382-108">Aus diesem Grund sollten die Inventurauftragszeilen erst erstellt werden, nachdem die Dimensionen für den Inventurauftragskopf vollständig eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ae382-108">That is why you should create the physical inventory order lines first after complete entering the dimensions for the physical inventory order header.</span></span> <span data-ttu-id="ae382-109">Sie können die Dimensionen für jede Inventurauftragszeile manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="ae382-109">You can manually change the dimensions for every physical inventory order line.</span></span> <span data-ttu-id="ae382-110">Zum Buchen verwendet [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die Dimensionen der Inventurauftragszeile.</span><span class="sxs-lookup"><span data-stu-id="ae382-110">For posting, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] will use the dimensions of the physical inventory order line.</span></span>  

## <a name="to-enter-dimensions-for-a-physical-inventory-order"></a><span data-ttu-id="ae382-111">So geben Sie Dimensionen für den Inventurauftrag ein</span><span class="sxs-lookup"><span data-stu-id="ae382-111">To enter dimensions for a physical inventory order</span></span>  

1.  <span data-ttu-id="ae382-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ae382-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ae382-113">Wählen Sie den Inventurauftrag aus, für den Sie eine Inventurerfassung erstellen möchten, klicken Sie auf Aktionen und anschließend auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ae382-113">Select the physical inventory order that you want to create an inventory recording for, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="ae382-114">Wählen Sie die Aktion **Dimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="ae382-114">Choose the **Dimensions** action.</span></span>  
4.  <span data-ttu-id="ae382-115">Im Fenster **Dimensionssatzposten bearbeiten** geben Sie die Dimensionen im Inventurauftragskopf ein.</span><span class="sxs-lookup"><span data-stu-id="ae382-115">In the **Edit Dimension Set Entries** window, enter the dimensions for the inventory order header.</span></span>  
5.  <span data-ttu-id="ae382-116">Erstellen Sie eine neue Inventurauftragszeile, und geben Sie die Artikelnummer ein.</span><span class="sxs-lookup"><span data-stu-id="ae382-116">Create a new physical inventory order line and enter the item number.</span></span>  
6.  <span data-ttu-id="ae382-117">Wählen Sie die Aktion **Position** und dann die Aktion **Dimensionen**.</span><span class="sxs-lookup"><span data-stu-id="ae382-117">Choose the **Line** action, and then choose the **Dimensions** action.</span></span>  
7.  <span data-ttu-id="ae382-118">Im Fenster **Dimensionssatzposten bearbeiten** geben Sie die Dimensionen im Inventurauftragskopf ein.</span><span class="sxs-lookup"><span data-stu-id="ae382-118">In the **Edit Dimension Set Entries** window, optionally, enter the dimensions for the inventory order line.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ae382-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae382-119">See Also</span></span>  
 <span data-ttu-id="ae382-120">[Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md) </span><span class="sxs-lookup"><span data-stu-id="ae382-120">[Enter Physical Inventory Orders](how-to-enter-physical-inventory-orders.md) </span></span>  
 <span data-ttu-id="ae382-121">[So buchen Sie physische Inventuraufträge](how-to-post-physical-inventory-orders.md) </span><span class="sxs-lookup"><span data-stu-id="ae382-121">[Post Physical Inventory Orders](how-to-post-physical-inventory-orders.md) </span></span>  
 [<span data-ttu-id="ae382-122">Dimensionssatz-Eintrags-Übersicht</span><span class="sxs-lookup"><span data-stu-id="ae382-122">Dimension Set Entries Overview</span></span>](../../design-details-dimension-set-entries-overview.md)

