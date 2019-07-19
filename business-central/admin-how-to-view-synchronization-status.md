---
title: Anzeigen des Status von Synchronisierungsprojekten | Microsoft Docs
description: Erfahren Sie, wie Sie den Status nach dem Synchronisieren gekoppelter Datensätze anzeigen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 06/13/2019
ms.author: bholtorf
ms.openlocfilehash: 8d7421d5fee1a6498c204730f873c3746aafc637
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726744"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Den Status von Synchronisierungsprojekten anzeigen
Verwenden Sie die **Fehler bei der gekoppelten Datensynchronisation**Seite, um den Status von Synchronisationsprojekten anzuzeigen, die für gekoppelte Datensätze in einer [!INCLUDE[crm_md](includes/crm_md.md)] Integration ausgeführt wurden. Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden. Das Anzeigen des Status ist beispielsweise bei der Fehlerbehebung hilfreich, da Sie auf Details der Fehler zugreifen können, die sich auf gekoppelte Datensätze beziehen. In der Regel werden diese Fehlertypen durch Benutzeraktionen verursacht, z. B. wenn:  

* Zwei Personen haben in beiden Geschäftsanwendungen denselben Datensatz geändert.
* Jemand hat einen Datensatz in einer der Apps gelöscht, aber nicht in beiden.

> [!Note]
> Die **Fehler bei der gekoppelten Datensynchronisation** Seite zeigt Informationen zu Projekten an, die sich auf gekoppelte Datensätze beziehen. Wenn Sie alle Fehler beheben, aber die Datensätze immer noch nicht synchronisieren, hat dies möglicherweise mit einer Einstellung für die Integration zu tun. In der Regel muss Ihr Administrator diese Fehlertypen beheben.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Anzeigen und Beheben von Synchronisationsfehlern für gekoppelte Datensätze
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gekoppelte Datensynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link aus.
2. Die Seite **Gekoppelte Daten-Synchronisierungs-Fehler** zeigt Probleme an, die auftraten, als Sie gekoppelte Datensätze synchronisierten. Die folgende Tabelle enthält Aktionen, mit denen Sie Probleme einzeln beheben können:

|Aktion|Beschreibung|
|----|----|
|**Kopplung entfernen**|Entkoppelt die Datensätze und sie werden nicht mehr synchronisiert. Um die Synchronisierung der Datensätze fortzusetzen, müssen Sie sie erneut koppeln.|
|**Wiederholen**|Für jeden Datensatz, in dem ein Fehler gefunden wird, wird die Synchronisierung übersprungen, sofern Sie das Problem nicht manuell beheben. Wiederholen schließt den Datensatz in der nächsten Synchronisation ein.|
|**Synchronisieren**|Die App versucht, einen Konflikt zu lösen, bei dem ein Datensatz in beiden Geschäftsanwendungen geändert wurde. Sie können die Version des Datensatzes auswählen, die in beiden Apps verwendet werden soll.|
|**Datensätze wiederherstellen** und **Datensätze löschen**|Diese sind nützlich, wenn ein Datensatz in einer der Apps gelöscht wurde. Datensätze löschen löscht den Datensatz in der App, in der er noch vorhanden ist. Durch die Wiederherstellung wird der Datensatz in der App wiederhergestellt, in der er gelöscht wurde.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an
1. Öffnen Sie beispielsweise einen Debitor, Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert.
2. Wählen Sie die Aktion**Synchronisierungs-Protokoll** aus, um das Synchronisierungsprotokoll für einen ausgewählten Datensatz anzuzeigen. Beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten.

## <a name="see-also"></a>Siehe auch  
[Einrichten des Benutzerkontos für die Integration in Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Verwenden von Dynamics 365 for Sales aus Business Central heraus](marketing-integrate-dynamicscrm.md)
