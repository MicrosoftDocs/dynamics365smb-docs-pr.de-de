---
title: 'Vorgehensweise: Einrichten von Codes für Standardservices | Microsoft Docs'
description: Erfahren Sie, wie Codes für Dienstaktivitäten eingerichtet werden, die Sie häufig ausführen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 32699c3c509a9d3516d43d9fb76948460b75d41f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784634"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="e7e73-103">Standardservicecodes einrichten</span><span class="sxs-lookup"><span data-stu-id="e7e73-103">Set Up Standard Service Codes</span></span>

<span data-ttu-id="e7e73-104">Bei der Durchführung eines normalen Service müssen häufig Servicebelege erstellt werden, die Servicezeilen mit ähnlichen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e7e73-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="e7e73-105">Um dies Zeilen einfach zu erstellen, können Sie Standardservicecodes einrichten, die einen vordefinierten Satz Servicezeilen haben.</span><span class="sxs-lookup"><span data-stu-id="e7e73-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="e7e73-106">Wenn Sie den Code in einem Verkaufsbeleg auswählen, werden die Zeilen automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="e7e73-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="e7e73-107">Sie können eine beliebige Anzahl von Standardservicecodes einrichten und jeder Code kann eine unbegrenzte Anzahl von Servicezeilen verschiedener Arten aufweisen, z. B. Artikel, Ressourcen, Kosten oder damit verknüpfte Standardtexte.</span><span class="sxs-lookup"><span data-stu-id="e7e73-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standard text linked to it.</span></span> <span data-ttu-id="e7e73-108">Die Servicezeilen jedes Standardservicecodes werden auf der Karte **Standardservicecode** erstellt.</span><span class="sxs-lookup"><span data-stu-id="e7e73-108">You create service lines of each standard service code on the **Standard Service Code** card.</span></span> <span data-ttu-id="e7e73-109">Sie können dann die Standardservicecodes Servicecodeartikelgruppen zuweisen im Fenster **Standardservicecodes Serviceartikelgruppen**.</span><span class="sxs-lookup"><span data-stu-id="e7e73-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="e7e73-110">Wenn Sie später einen Servicebeleg erstellen, können Sie die **Standardservicecodes abrufen** Aktion verwenden, um Servicezeilen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7e73-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
> <span data-ttu-id="e7e73-111">Sie können das gleive Vorgehen verwenden, um Zeilen in Verkaufs- und Einkaufsbelegen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7e73-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="e7e73-112">Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="e7e73-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="e7e73-113">So richten Sie einen Standardservicecode ein</span><span class="sxs-lookup"><span data-stu-id="e7e73-113">To set up a standard service code</span></span>

1. <span data-ttu-id="e7e73-114">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Standardservicecodes** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e7e73-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e7e73-115">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="e7e73-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="e7e73-116">Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e7e73-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="e7e73-117">So weisen Sie einer Serviceartikelgruppe einen Standardservicecode zu</span><span class="sxs-lookup"><span data-stu-id="e7e73-117">To assign a standard service code to a service item group</span></span>

1. <span data-ttu-id="e7e73-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceartikelgruppen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e7e73-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e7e73-119">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="e7e73-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e7e73-120">Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e7e73-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e7e73-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e73-121">See Also</span></span>

[<span data-ttu-id="e7e73-122">Service</span><span class="sxs-lookup"><span data-stu-id="e7e73-122">Service Management</span></span>](service-service.md)