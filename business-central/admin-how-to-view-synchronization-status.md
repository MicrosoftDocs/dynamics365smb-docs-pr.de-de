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
# <a name="view-the-status-of-a-synchronization"></a>Den Status einer Synchronisierung anzeigen
Sie können den Status der einzelnen Synchronisierungsprojekte anzeigen, die für [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden. Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden. Dies ist hilfreich beim Beheben von Synchronisierungsproblemen, da es Ihnen ermöglicht, auf ausführliche Informationen zu bestimmten Fehlern zuzugreifen.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Um Synchronisierungsprobleme für gekoppelte Datensätze anzuzeigen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gekoppelte Datensynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link aus.
2. Die Seite **Gekoppelte Daten-Synchronisierungs-Fehler** zeigt Probleme an, die auftraten, als Sie gekoppelte Datensätze synchronisierten. Sie können Datensätze nach Aktionen filtern und sortieren wie **Wiederherstellen** oder **Datensätze löschen**, um Problemen eines nach dem anderen zu lösen.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an
1. Öffnen Sie beispielsweise einen Debitor, Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Vertrieb synchronisiert
2. Wählen Sie die Aktion **Synchronisierungs-Protokoll** aus, um das Synchronisierungsprotokoll für einen ausgewählten Datensatz anzuzeigen. Beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten.

## <a name="see-also"></a>Siehe auch  
[Einrichten von Dynamics 365 for Sales-Integration in Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Verwenden von Dynamics 365 for Sales aus Business Central heraus](marketing-integrate-dynamicscrm.md)
