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
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245685"
---
# <a name="view-the-status-of-a-synchronization"></a>Den Status einer Synchronisierung anzeigen
Sie können den Status der einzelnen Synchronisierungsprojekte anzeigen, die für [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden. Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden. Dies ist hilfreich beim Beheben von Synchronisierungsproblemen, da es Ihnen ermöglicht, auf ausführliche Informationen zu bestimmten Fehlern zuzugreifen.

### <a name="to-view-all-synchronization-issues"></a>So zeigen Sie alle Synchronisierungsprobleme an
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gekoppelte Datensynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link aus.
2. Auf der Seite **Gekoppelte Datensynchronisierungsfehler** können Sie alle Probleme anzeigen, die bei der Synchronisierung von Daten zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] aufgetreten sind, Datensätze der Seite nach Tabelle und Fehlermeldung filtern und sortieren, und Maßnahmen wie **Wiederholen** oder **Kopplung entfernen** ergreifen, um Probleme einzeln oder in einer Massenoperation zu lösen.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an
1. Öffnen Sie beispielsweise Debitor, Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Vertrieb synchronisiert
2. Wählen Sie die Aktion **Synchronisierungsprotokoll** aus, um das Synchronisierungsprotokoll für den ausgewählten Datensatz anzuzeigen, beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten

## <a name="see-also"></a>Siehe auch  
[Einrichten von Dynamics 365 for Sales-Integration in Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Verwenden von Dynamics 365 for Sales aus Business Central heraus](marketing-integrate-dynamicscrm.md)
