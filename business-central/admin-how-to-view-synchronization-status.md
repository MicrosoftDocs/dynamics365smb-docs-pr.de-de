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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c185ab8fecc8f8d70dad7696a5fb5f67207717aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924603"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Den Status von Synchronisierungsprojekten anzeigen
Verwenden Sie die Seite **Gekoppelte Datensynchronisationsfehler**, um den Status von Synchronisationsjobs anzuzeigen, die für gekoppelte Datensätze in einer Common Data Service- oder [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden. Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgeführt wurden. Das Anzeigen des Status ist beispielsweise bei der Fehlerbehebung hilfreich, da Sie auf Details der Fehler zugreifen können, die sich auf gekoppelte Datensätze beziehen. In der Regel werden diese Fehlertypen durch Benutzeraktionen verursacht, z. B. wenn:  

* Zwei Personen haben in beiden Geschäftsanwendungen denselben Datensatz geändert.
* Jemand hat einen Datensatz in einer der Apps gelöscht, aber nicht in beiden.

> [!Note]
> Die **Fehler bei der gekoppelten Datensynchronisation** Seite zeigt Informationen zu Projekten an, die sich auf gekoppelte Datensätze beziehen. Wenn Sie alle Fehler beheben, aber die Datensätze immer noch nicht synchronisieren, hat dies möglicherweise mit einer Einstellung für die Integration zu tun. In der Regel muss Ihr Administrator diese Fehlertypen beheben.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Anzeigen und Beheben von Synchronisationsfehlern für gekoppelte Datensätze
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Gekoppelte Datensynchronisationsfehler** ein, und wählen Sie dann den entsprechenden Link.
2. Die Seite **Gekoppelte Daten-Synchronisierungs-Fehler** zeigt Probleme an, die auftraten, als Sie gekoppelte Datensätze synchronisierten. Die folgende Tabelle enthält Aktionen, mit denen Sie Probleme einzeln beheben können:

|Aktion|Beschreibung|
|----|----|
|**Kopplung entfernen**|Entkoppelt die Datensätze und sie werden nicht mehr synchronisiert. Zum Fortsetzen der Synchronisierung der Datensätze, müssen Sie sie erneut koppeln. |
|**Wiederholen** und **Alle wiederholen**|Für jeden Datensatz, in dem ein Fehler gefunden wird, wird die Synchronisierung übersprungen, sofern Sie das Problem nicht beheben. „Wiederholen“ bezieht den ausgewählten Datensatz in die nächste Synchronisierung mit ein. **Alle wiederholen** umfasst alle Datensätze.|
|**Synchronisieren**|Die App versucht, einen Konflikt zu lösen, bei dem ein Datensatz in beiden Geschäftsanwendungen geändert wurde. Sie können die Version des Datensatzes auswählen, die verwendet werden soll.|
|**Datensätze wiederherstellen** und **Datensätze löschen**|Diese sind nützlich, wenn ein Datensatz in einer der Geschäftsanwendungen gelöscht wurde. Datensätze löschen löscht den Datensatz in der App, in der er noch vorhanden ist. Wiederherstellen stellt den Datensatz in der Geschäftsanwendung wieder her, in der er gelöscht wurde.|

> [!NOTE]
> Sie können Ihre Integrationstabellenzuordnungen so einrichten, dass diese Aktionen automatisch angewendet werden, um die Anzahl der Konflikte zu verringern, die Sie lösen müssen. Weitere Informationen finden Sie unter [Zuordnen von Integrationstabellen](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an
1. Öffnen Sie z.B. einen Debitor, einen Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Common Data Service oder [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert.
2. Wählen Sie die Aktion**Synchronisierungs-Protokoll** aus, um das Synchronisierungsprotokoll für einen ausgewählten Datensatz anzuzeigen. Beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten.

## <a name="see-also"></a>Siehe auch  
[Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md)
