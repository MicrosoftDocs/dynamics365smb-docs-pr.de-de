---
title: "Übersicht und Einrichten von Serviceartikel und Serviceartikelkomponenten  | Microsoft Docs"
description: "Erhalten von Informationen über die Elemente, die Sie einrichten müssen, bevor Sie Serviceartikel, einschließlich Vorgabewerte wie Reaktionszeit, Vertragsrabatt, und Servicepreisgruppen verwenden können."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 050456758a2bf4f3489ed382103d5fed99e8fada
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="8d679-103">Richten Sie Serviceartikel und Serviceartikelkomponenten ein.</span><span class="sxs-lookup"><span data-stu-id="8d679-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="8d679-104">Um mit Serviceartikeln arbeiten können, müssen Sie Folgendes einrichten</span><span class="sxs-lookup"><span data-stu-id="8d679-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="8d679-105">Serviceartikelgruppen</span><span class="sxs-lookup"><span data-stu-id="8d679-105">Service item groups.</span></span>
* <span data-ttu-id="8d679-106">Optional</span><span class="sxs-lookup"><span data-stu-id="8d679-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="8d679-107">Um Serviceartikelgruppen einzurichten:</span><span class="sxs-lookup"><span data-stu-id="8d679-107">To set up service item groups</span></span>
<span data-ttu-id="8d679-108">Sie können Artikelgruppen einrichten, die bezüglich Reparatur und Wartung miteinander in Verbindung stehen.</span><span class="sxs-lookup"><span data-stu-id="8d679-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="8d679-109">Sie können für Serviceartikel in einer Serviceartikelgruppe Vorgabewerte wie Reaktionszeit, Vertragsrabatt und Servicepreisgruppe festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d679-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="8d679-110">Für Artikel in einer Serviceartikelgruppe können Sie auswählen, ob sie beim Verkauf automatisch als Serviceartikel erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d679-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="8d679-111">Sie verbinden die Serviceartikelgruppen mit **Artikeln** auf der Artikelkarte und mit Serviceartikeln auf der **Serviceartikel**karte.</span><span class="sxs-lookup"><span data-stu-id="8d679-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="8d679-112">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceartikelgruppen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8d679-113">Erstellen Sie eine neue Serviceartikelgruppe.</span><span class="sxs-lookup"><span data-stu-id="8d679-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="8d679-114">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="8d679-115">Im Feld **Vorg.-Vertragsrabatt %** geben Sie den Vertragsrabattprozentsatz ein, der als Standardwert für Serviceartikel in dieser Gruppe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d679-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="8d679-116">Im Feld **Vorg.-Servicepreisgrp.-Code** geben Sie den Servicepreisgruppencode ein, der als Standardwert für Serviceartikel in dieser Gruppe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d679-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="8d679-117">Im Feld **Vorg.-Reaktionszeit (Std.)** geben Sie die Reaktionszeit in Stunden ein, die als Standardwert auf Serviceartikel in dieser Gruppe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d679-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="8d679-118">Wenn die Artikel in der Gruppe beim Verkauf als Serviceartikel erfasst werden sollen, aktivieren Sie das Feld **Serviceartikel erstellen**.</span><span class="sxs-lookup"><span data-stu-id="8d679-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="8d679-119">So richten Sie Serviceartikelkomponenten ein</span><span class="sxs-lookup"><span data-stu-id="8d679-119">To set up service item components</span></span>
<span data-ttu-id="8d679-120">Ein Serviceartikel kann aus mehreren Komponenten bestehen, die mit Ersatzteilen ersetzt werden können, wenn ein Service durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d679-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="8d679-121">Diese Komponenten werden in dem Fenster **Serviceartikelkomponenten** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="8d679-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="8d679-122">Wenn Sie Komponenten für Serviceartikel einrichten wollen, die Stücklisten sind, können die Stücklistenartikel als Serviceartikelkomponenten angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8d679-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="8d679-123">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Serivceartikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d679-124">Öffnen Sie den Serviceartikel, für den Sie Komponenten einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="8d679-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="8d679-125">Wählen Sie die Aktion **Komponenten** aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-125">Choose the **Components** action.</span></span> <span data-ttu-id="8d679-126">Das Fenster **Serviceartikelkomponenten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8d679-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="8d679-127">Fügen Sie eine neue Komponente hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d679-127">Add a new component.</span></span>  
5. <span data-ttu-id="8d679-128">Wählen Sie im Feld **Art** den Eintrag **Serviceartikel**, falls die Komponente selbst ein Serviceartikel ist.</span><span class="sxs-lookup"><span data-stu-id="8d679-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="8d679-129">Oder wählen Sie **Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="8d679-130">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="8d679-130">In the **No.**</span></span> <span data-ttu-id="8d679-131">Wählen Sie im Feld Nr. den Artikel oder Serviceartikel aus, der eine Komponente des Serviceartikels ist.</span><span class="sxs-lookup"><span data-stu-id="8d679-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="8d679-132">So richten Sie Serviceartikelkomponenten aus Stücklisten ein</span><span class="sxs-lookup"><span data-stu-id="8d679-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="8d679-133">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Serivceartikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8d679-134">Öffnen Sie den Serviceartikel, für den Sie Komponenten aus Stücklisten einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="8d679-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="8d679-135">Wählen Sie die Aktion **Komponenten** aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-135">Choose the **Components** action.</span></span> <span data-ttu-id="8d679-136">Das Fenster **Serviceartikelkomponenten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8d679-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="8d679-137">Wählen Sie im Fenster **Kopiere von Stückliste**</span><span class="sxs-lookup"><span data-stu-id="8d679-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="8d679-138">Ist der mit dem Serviceartikel verbundene Artikel eine Stückliste, werden für alle Artikel in der Stückliste automatisch Komponenten erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d679-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="8d679-139">So richten Sie ein Servicelagerfach ein</span><span class="sxs-lookup"><span data-stu-id="8d679-139">To set up a service shelf</span></span>
<span data-ttu-id="8d679-140">Sie können Servicelagerfächer einrichten, die identifizieren, wo Sie Serviceartikel speichern.</span><span class="sxs-lookup"><span data-stu-id="8d679-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="8d679-141">Servicelagerfächer werden im Fenster **Serviceauftrag** und im Fenster **Servicearbeitsschein** mit Serviceartikeln verbunden.</span><span class="sxs-lookup"><span data-stu-id="8d679-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="8d679-142">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicelagerfächer** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d679-143">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="8d679-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d679-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d679-144">See Also</span></span>
<span data-ttu-id="8d679-145">[Einrichten von Codes für Standardservices](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="8d679-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="8d679-146">Lösungsanleitung Einrichtung</span><span class="sxs-lookup"><span data-stu-id="8d679-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)

