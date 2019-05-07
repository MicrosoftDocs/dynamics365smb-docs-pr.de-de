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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940181"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="1fed2-103">Den Status einer Synchronisierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="1fed2-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="1fed2-104">Sie können den Status der einzelnen Synchronisierungsprojekte anzeigen, die für [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="1fed2-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="1fed2-105">Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="1fed2-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1fed2-106">Dies ist hilfreich beim Beheben von Synchronisierungsproblemen, da es Ihnen ermöglicht, auf ausführliche Informationen zu bestimmten Fehlern zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1fed2-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="1fed2-107">So zeigen Sie alle Synchronisierungsprobleme an</span><span class="sxs-lookup"><span data-stu-id="1fed2-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="1fed2-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gekoppelte Datensynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1fed2-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="1fed2-109">Auf der Seite **Gekoppelte Datensynchronisierungsfehler** können Sie alle Probleme anzeigen, die bei der Synchronisierung von Daten zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] aufgetreten sind, Datensätze der Seite nach Tabelle und Fehlermeldung filtern und sortieren, und Maßnahmen wie **Wiederholen** oder **Kopplung entfernen** ergreifen, um Probleme einzeln oder in einer Massenoperation zu lösen.</span><span class="sxs-lookup"><span data-stu-id="1fed2-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="1fed2-110">So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an</span><span class="sxs-lookup"><span data-stu-id="1fed2-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="1fed2-111">Öffnen Sie beispielsweise Debitor, Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Vertrieb synchronisiert</span><span class="sxs-lookup"><span data-stu-id="1fed2-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="1fed2-112">Wählen Sie die Aktion **Synchronisierungsprotokoll** aus, um das Synchronisierungsprotokoll für den ausgewählten Datensatz anzuzeigen, beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten</span><span class="sxs-lookup"><span data-stu-id="1fed2-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="1fed2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fed2-113">See Also</span></span>  
[<span data-ttu-id="1fed2-114">Einrichten von Dynamics 365 for Sales-Integration in Business Central</span><span class="sxs-lookup"><span data-stu-id="1fed2-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="1fed2-115">Verwenden von Dynamics 365 for Sales aus Business Central heraus</span><span class="sxs-lookup"><span data-stu-id="1fed2-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
