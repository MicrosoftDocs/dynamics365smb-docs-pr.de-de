---
title: Inventurbelege
description: "Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen."
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
ms.openlocfilehash: ab8643fda6d733558e1cfd45031987b3693a55fc
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="physical-inventory-documents"></a><span data-ttu-id="5fbb0-103">Inventurbelege</span><span class="sxs-lookup"><span data-stu-id="5fbb0-103">Physical Inventory Documents</span></span>
<span data-ttu-id="5fbb0-104">Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-104">You can take inventory of your items using the physical inventory order and the physical inventory recording documents.</span></span>  

<span data-ttu-id="5fbb0-105">Der Inventurauftrag enthält Daten für die Planung, Umsetzung und Analyse von Inventuren.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-105">The physical inventory order contains data for planning, realizing, and analyzing physical inventory.</span></span> <span data-ttu-id="5fbb0-106">Artikel-, Lagerort- und Lagerplatzinformationen sind ebenfalls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-106">The item, location, and bin information are also available.</span></span>  

## <a name="physical-inventory-recording"></a><span data-ttu-id="5fbb0-107">Inventurerfassung</span><span class="sxs-lookup"><span data-stu-id="5fbb0-107">Physical Inventory Recording</span></span>  
<span data-ttu-id="5fbb0-108">Die Inventurerfassung enthält die Artikelnamen und -mengen, die bei der Inventur gezählt wurden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-108">The physical inventory recording contains the item names and quantities counted while taking physical inventory.</span></span> <span data-ttu-id="5fbb0-109">Ein Artikel kann in mehreren Inventurerfassungen gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-109">An item may be counted in more than one physical inventory recording.</span></span>  

<span data-ttu-id="5fbb0-110">Ein Inventurauftrag kann sich auf mehr als eine Inventurerfassung beziehen, doch eine Inventurerfassung kann sich nur auf einen Inventurauftrag beziehen.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-110">A physical inventory order can be related to more than one physical inventory recording, but a physical inventory recording can be related to only one physical inventory order.</span></span> <span data-ttu-id="5fbb0-111">Weitere Informationen finden Sie unter [Vorgehensweise: Inventurhäufigkeiten für physische Lagererfassung einrichten](physical-inventory-recording-counting-physical-inventory.md)</span><span class="sxs-lookup"><span data-stu-id="5fbb0-111">For more information, see [Physical Inventory Recording - Counting Physical Inventory](physical-inventory-recording-counting-physical-inventory.md).</span></span>  

<span data-ttu-id="5fbb0-112">Nach Abschluss der Inventurerfassungen und des Inventurauftrags kann der Inventurauftrag gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-112">After completing the physical inventory recordings and the physical inventory order, you can post the physical inventory order.</span></span> <span data-ttu-id="5fbb0-113">Die Informationen werden an das Inventur-Buch.-Blatt übertragen.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-113">The information is transferred to the physical inventory journal.</span></span> <span data-ttu-id="5fbb0-114">Nach der Übertragung ist der Inventurauftrag als gebuchter Inventurauftrag zum späteren Abrufen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-114">After this transfer, the physical inventory order will be available as a posted physical inventory order for future retrieval.</span></span>  

## <a name="posted-physical-inventory-documents"></a><span data-ttu-id="5fbb0-115">Gebuchte physische Inventurbelege</span><span class="sxs-lookup"><span data-stu-id="5fbb0-115">Posted Physical Inventory Documents</span></span>  
<span data-ttu-id="5fbb0-116">Nach dem Buchen wird der Inventurauftrag gelöscht, und der Beleg kann als gebuchter Inventurauftrag angezeigt und ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-116">After posting the physical inventory order will be deleted and you can view and evaluate the document as posted physical inventory order.</span></span>  

<span data-ttu-id="5fbb0-117">Beim Buchen von Inventuraufträgen werden auch die Inventurerfassungsköpfe und die Inventurerfassungszeilen in die gebuchten Belege übertragen.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-117">When posting the physical inventory orders also physical inventory recording headers and physical inventory recording lines and physical inventory comment lines will be transferred to posted documents.</span></span>  

<span data-ttu-id="5fbb0-118">Die gebuchten Inventurbelege bieten die Möglichkeit, einen vollständigen Überblick über den gesamten Inventurprozess zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-118">The posted inventory documents offer you the possibility to get a complete overview about the whole process of physical inventory.</span></span> <span data-ttu-id="5fbb0-119">Sie können die Daten von gebuchten Inventurauftragsköpfen und gebuchten Inventurauftragszeilen nicht ändern, da diese Belege bereits gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-119">You cannot change the data of posted physical inventory order headers and posted physical inventory order lines because the documents have been already posted.</span></span>  

<span data-ttu-id="5fbb0-120">Wenn Sie Artikelverfolgungszeilen zum Registrieren von Seriennummern und Chargennummern verwendet haben, speichert die Anwendung die erwarteten Artikelverfolgungszeilen, die erfassten Artikelverfolgungszeilen und die gebuchten Artikelverfolgungsposten.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-120">If you have used also item tracking lines to register serial nos. and lot nos. the program will save the expected item tracking lines, the recorded item tracking lines and the posted item tracking ledger entries.</span></span>  

<span data-ttu-id="5fbb0-121">Es ist möglich, mithilfe der Kopierfunktion auf Basis des gebuchten Inventurauftrags neue Inventuraufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-121">It is possible to use the posted physical inventory order to create new physical inventory orders using the copy function.</span></span>  

<span data-ttu-id="5fbb0-122">Mit der Funktion "Navigate" können Inventurposten und andere zugehörige Posten eines gebuchten Inventurauftrags angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5fbb0-122">You can use Navigate to view the inventory ledger entries and other related ledger entries for a posted physical inventory order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5fbb0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fbb0-123">See Also</span></span>  
 <span data-ttu-id="5fbb0-124">[Logistik](../../warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-124">[Warehouse Management](../../warehouse-manage-warehouse.md) </span></span>  
 <span data-ttu-id="5fbb0-125">[Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-125">[Physical Inventory Order Lines With Item Tracking Lines](physical-inventory-order-lines-with-item-tracking-lines.md) </span></span>  
 <span data-ttu-id="5fbb0-126">[Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-126">[Physical Inventory Recording - Counting Physical Inventory](physical-inventory-recording-counting-physical-inventory.md) </span></span>  
 <span data-ttu-id="5fbb0-127">[Inventurbelege einrichten](how-to-set-up-physical-inventory-documents.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-127">[Set Up Physical Inventory Documents](how-to-set-up-physical-inventory-documents.md) </span></span>  
 <span data-ttu-id="5fbb0-128">[Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-128">[Enter Physical Inventory Orders](how-to-enter-physical-inventory-orders.md) </span></span>  
 <span data-ttu-id="5fbb0-129">[So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-129">[Create a Physical Inventory Recording](how-to-create-a-physical-inventory-recording.md) </span></span>  
 <span data-ttu-id="5fbb0-130">[So buchen Sie physische Inventuraufträge](how-to-post-physical-inventory-orders.md) </span><span class="sxs-lookup"><span data-stu-id="5fbb0-130">[Post Physical Inventory Orders](how-to-post-physical-inventory-orders.md) </span></span>  
 [<span data-ttu-id="5fbb0-131">Lokale Funktion (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="5fbb0-131">Germany Local Functionality</span></span>](germany-local-functionality.md)

