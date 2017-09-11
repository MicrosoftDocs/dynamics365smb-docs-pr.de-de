---
title: Eine Kreditorenkarte erstellen, um einen neuen Kreditor zu erfassen | Microsoft Docs
description: Erfahren Sie, wie Sie eine Kreditorenkarte erstellt, um einen neuen Kreditor oder einem Lieferanten zu erfassen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="9613f-103">Vorgehensweise: Einen neuen Kreditor registrieren</span><span class="sxs-lookup"><span data-stu-id="9613f-103">How to: Register New Vendors</span></span>
<span data-ttu-id="9613f-104">Kreditoren stellen die Produkte bereit, die Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="9613f-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="9613f-105">Jeder Kreditor, von dem Sie kaufen, muss als Kreditorenkarte erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9613f-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="9613f-106">Bevor Sie neue Kreditoren erfassen können, müssen Sie verschiedene Einkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Kreditorenkarten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="9613f-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="9613f-107">Nach der Erstellung aller erforderlichen Masterdaten können weitere Konfigurationsschritte für den Mandanten – wie Priorisieren des Kreditors zu Zahlungszwecken oder Aufführen von Artikeln, die von diesem und anderen Kreditoren geliefert werden – ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9613f-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="9613f-108">Eine weitere Gruppe von Einrichtungsaufgaben bildet die Erfassung von Vereinbarungen zu Rabatten, Preisen und Zahlungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="9613f-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="9613f-109">Weitere Informationen finden Sie unter [Einrichten des Einkaufs](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="9613f-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="9613f-110">Kreditorenkarten verwahren die Informationen, die benötigt werden, um Produkte vom Kreditor einzukaufen.</span><span class="sxs-lookup"><span data-stu-id="9613f-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="9613f-111">Weitere Informationen finden Sie unter [Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md) und [Vorgehensweise: Neue Produkte erfassen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="9613f-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="9613f-112">Wenn es Kreditorenvorlagen für verschiedene Kreditorenarten gibt, dann erscheint ein Fenster automatisch, wenn Sie eine neue Kreditorenkarte erstellen, von der aus Sie eine entsprechende Kreditorenvorlage auswählen können.</span><span class="sxs-lookup"><span data-stu-id="9613f-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="9613f-113">Wenn nur eine Kreditorenvorlage vorhanden ist, verwenden neue Kreditorenkarten immer diese Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9613f-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="9613f-114">Erstellen einer neue Kreditorenkarte</span><span class="sxs-lookup"><span data-stu-id="9613f-114">To create a new vendor card</span></span>
1. <span data-ttu-id="9613f-115">Auf der Startseite wählen Sie **Kreditoren**, um die Liste der Bestandskreditoren zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9613f-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="9613f-116">Im **Kreditoren**-Fenster wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9613f-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="9613f-117">Wenn mehr als eine Kreditorenvorlage vorhanden ist, dann öffnet sich ein Fenster mit verfügbaren Kreditorenvorlagen automatisch.</span><span class="sxs-lookup"><span data-stu-id="9613f-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="9613f-118">In diesem Fall, folgen Sie den nächsten zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="9613f-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="9613f-119">Wählen Sie im Fenster **Vorlage für neuen Kreditor auswählen** die Vorlage, die Sie für die neue Kreditorenkarte verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9613f-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="9613f-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9613f-120">Choose the **OK** button.</span></span> <span data-ttu-id="9613f-121">Eine neue Kreditorenkarte wird geöffnet mit einigen Feldern, die mit Daten aus der Vorlage ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9613f-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="9613f-122">Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Kreditorenkarte fort.</span><span class="sxs-lookup"><span data-stu-id="9613f-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="9613f-123">Der Kreditor ist nun erfasst und die Kreditorenkarte ist bereit, in Einkaufsbeleg verwendet zu werden, in denen Sie mit dem Kreditor handeln.</span><span class="sxs-lookup"><span data-stu-id="9613f-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="9613f-124">Wenn Sie diese Kreditorenkarte als Vorlage verwenden möchten, wenn Sie neue Kreditorenkarten erstellen, dann fahren sie fort, um sie als Kreditorenvorlage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9613f-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="9613f-125">Weitere Informationen finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="9613f-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="9613f-126">So speichern Sie die Kreditorenkarte als Vorlage</span><span class="sxs-lookup"><span data-stu-id="9613f-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="9613f-127">Wählen Sie im Fenster **Kreditorenkarte** die Aktion **Als Vorlage speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="9613f-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="9613f-128">Das Fenster **Kreditorenvorlage** wird geöffnet und zeigt die Kreditorenkarte als Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9613f-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="9613f-129">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="9613f-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9613f-130">Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**.</span><span class="sxs-lookup"><span data-stu-id="9613f-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="9613f-131">Das Fenster **Dimensionen Vorlagenübersicht** wird geöffnet und zeigt alle Dimensionscodes, die für den Kreditor eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9613f-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="9613f-132">Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Kreditorenkarten gelten, die mit der Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9613f-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="9613f-133">Wenn Sie die neue Kreditorvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="9613f-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="9613f-134">Die Kreditorvorlage wird der Liste von Kreditorvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Kreditorenkarten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9613f-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="9613f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9613f-135">See Also</span></span>
[<span data-ttu-id="9613f-136">Einkauf</span><span class="sxs-lookup"><span data-stu-id="9613f-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9613f-137">[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="9613f-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="9613f-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9613f-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

