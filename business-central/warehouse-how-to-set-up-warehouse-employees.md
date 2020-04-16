---
title: So richten Sie Lagermitarbeiter ein | Microsoft Docs
description: Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmäßigen Lagerorten zugeordnet werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7abdb225967bc402195d0811c26de1f237238c8b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196115"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="4932b-103">Lagermitarbeiter einrichten</span><span class="sxs-lookup"><span data-stu-id="4932b-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="4932b-104">Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmäßigen Lagerorten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4932b-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="4932b-105">Durch diese Benutzereinrichtung werden alle Lageraktivitäten innerhalb der Datenbank nach dem Lagerort des Mitarbeiters gefiltert, sodass der Mitarbeiter lediglich Lageraktivitäten am Standardlagerort ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4932b-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="4932b-106">Ein Benutzer kann zusätzlichen, nicht standardmäßigen Lagerorten zugeordnet werden, für die der Mitarbeiter zwar Aktivitätszeilen anzeigen, aber keine Aktivitäten ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4932b-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="4932b-107">So richten Sie die Lagermitarbeiter ein:</span><span class="sxs-lookup"><span data-stu-id="4932b-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="4932b-108">Wählen Sie die ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Lagermitarbeiter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4932b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4932b-109">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4932b-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="4932b-110">Wählen Sie das Feld **Benutzer-ID** und dann den Benutzer aus, der als Lagermitarbeiter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4932b-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="4932b-111">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4932b-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="4932b-112">Geben Sie im Feld **Lagerortcode** den Code des Lagerorts ein, an dem der Lagermitarbeiter arbeitet.</span><span class="sxs-lookup"><span data-stu-id="4932b-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="4932b-113">Aktivieren Sie das Kontrollkästchen **Standard**, um den Lagerort als einzigen Lagerort zu definieren, an dem der Mitarbeiter Lageraktivitäten ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4932b-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="4932b-114">Wiederholen Sie diese Schritte, um Lagerorten weitere Mitarbeiter zuzuordnen oder um nicht standardmäßige Lagerorte bestehenden Lagermitarbeitern zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4932b-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4932b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4932b-115">See Also</span></span>  
[<span data-ttu-id="4932b-116">Logistik</span><span class="sxs-lookup"><span data-stu-id="4932b-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4932b-117">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="4932b-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4932b-118">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="4932b-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="4932b-119">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4932b-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4932b-120">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="4932b-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4932b-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4932b-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
