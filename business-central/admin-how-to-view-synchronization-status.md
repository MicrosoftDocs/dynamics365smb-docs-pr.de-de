---
title: Anzeigen des Status einer Synchronisierung | Microsoft Docs
description: Erfahren Sie, wie Sie den Status eines einzelnen Synchronisierungsprojekts anzeigen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620884"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="80069-103">Den Status einer Synchronisierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="80069-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="80069-104">Sie können den Status der einzelnen Synchronisierungsprojekte anzeigen, die für [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="80069-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="80069-105">Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="80069-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="80069-106">Dies ist hilfreich beim Beheben von Synchronisierungsproblemen, da es Ihnen ermöglicht, auf ausführliche Informationen zu bestimmten Fehlern zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="80069-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="80069-107">Um Synchronisierungsprobleme für gekoppelte Datensätze anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="80069-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="80069-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gekoppelte Datensynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="80069-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="80069-109">Die Seite **Gekoppelte Daten-Synchronisierungs-Fehler** zeigt Probleme an, die auftraten, als Sie gekoppelte Datensätze synchronisierten.</span><span class="sxs-lookup"><span data-stu-id="80069-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="80069-110">Sie können Datensätze nach Aktionen filtern und sortieren wie **Wiederherstellen** oder **Datensätze löschen**, um Problemen eines nach dem anderen zu lösen.</span><span class="sxs-lookup"><span data-stu-id="80069-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="80069-111">So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an</span><span class="sxs-lookup"><span data-stu-id="80069-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="80069-112">Öffnen Sie beispielsweise einen Debitor, Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Vertrieb synchronisiert</span><span class="sxs-lookup"><span data-stu-id="80069-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="80069-113">Wählen Sie die Aktion**Synchronisierungs-Protokoll** aus, um das Synchronisierungsprotokoll für einen ausgewählten Datensatz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="80069-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="80069-114">Beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten.</span><span class="sxs-lookup"><span data-stu-id="80069-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="80069-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80069-115">See Also</span></span>  
[<span data-ttu-id="80069-116">Einrichten von Dynamics 365 for Sales-Integration in Business Central</span><span class="sxs-lookup"><span data-stu-id="80069-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="80069-117">Verwenden von Dynamics 365 for Sales aus Business Central heraus</span><span class="sxs-lookup"><span data-stu-id="80069-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
