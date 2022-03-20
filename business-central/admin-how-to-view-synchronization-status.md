---
title: Den Status von Synchronisationsaufträgen anzeigen (enthält Video)
description: Verwenden Sie die Seite Gekoppelte Datensynchronisierungsfehler, um den Status der Synchronisierungsaufträge anzuzeigen, die für gekoppelte Datensätze in Integrationen ausgeführt wurden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 6112b025c08468a3e0f5bdfbb9147b2fbdaf6744
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383505"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Status von Synchronisationsaufträgen anzeigen


Verwenden Sie die Seite **Gekoppelte Datensynchronisationsfehler**, um den Status von Synchronisationsjobs anzuzeigen, die für gekoppelte Datensätze in einer Dataverse- oder [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausgeführt wurden. Dies umfasst Synchronisierungsprojekte, die aus der Projektwarteschlange ausgeführt wurden, sowie manuelle Synchronisierungsprojekte, die in Datensätzen von [!INCLUDE[prod_short](includes/prod_short.md)] ausgeführt wurden. Das Anzeigen des Status ist beispielsweise bei der Fehlerbehebung hilfreich, da Sie auf Details der Fehler zugreifen können, die sich auf gekoppelte Datensätze beziehen. In der Regel werden diese Fehlertypen durch Benutzeraktionen verursacht, z. B. wenn:  

* Zwei Personen haben in beiden Geschäftsanwendungen die selben Daten geändert.
* Jemand hat Daten in einer der Apps gelöscht, aber nicht in beiden.

> [!Note]
> Die **Fehler bei der gekoppelten Datensynchronisation** Seite zeigt Informationen zu Projekten an, die sich auf gekoppelte Datensätze beziehen. Wenn Sie alle Fehler beheben, aber die Datensätze immer noch nicht synchronisieren, hat dies möglicherweise mit einer Einstellung für die Integration zu tun. In der Regel muss Ihr Administrator diese Fehlertypen beheben.   

## <a name="example"></a>Beispiel
Dieses Video zeigt ein Beispiel für die Behebung von Fehlern, die bei der Synchronisierung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] aufgetreten sind. Der Prozess ist für alle Integrationen derselbe. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Anzeigen und Beheben von Synchronisationsfehlern für gekoppelte Datensätze
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Gekoppelte Datensynchronisierungsfehler** ein und wählen Sie dann den entsprechenden Link.
2. Die Seite **Gekoppelte Daten-Synchronisierungs-Fehler** zeigt Probleme an, die auftraten, als Sie gekoppelte Datensätze synchronisierten. Die folgende Tabelle enthält Aktionen, mit denen Sie Probleme einzeln beheben können:

|Aktion|Beschreibung|
|----|----|
|**Kopplung entfernen**|Entkoppelt die Datensätze und sie werden nicht mehr synchronisiert. Zum Fortsetzen der Synchronisierung der Datensätze, müssen Sie sie erneut koppeln. |
|**Wiederholen** und **Alle wiederholen**|Für jeden Datensatz, in dem ein Fehler gefunden wird, wird die Synchronisierung übersprungen, sofern Sie das Problem nicht beheben. „Wiederholen“ bezieht den ausgewählten Datensatz in die nächste Synchronisierung mit ein. **Alle wiederholen** umfasst alle Datensätze.|
|**Synchronisieren**|Die App versucht, einen Konflikt zu lösen, bei dem Daten in beiden Geschäftsanwendungen geändert wurde. Sie können sich entscheiden, die Daten zu verwenden.|
|**Datensätze wiederherstellen** und **Datensätze löschen**|Diese sind nützlich, wenn ein Datensatz in einer der Geschäftsanwendungen gelöscht wurde. Datensätze löschen löscht den Datensatz oder die Zeile in der App, in der er noch vorhanden ist. Wiederherstellen stellt den Datensatz oder die Zeile in der Geschäftsanwendung wieder her, in der er gelöscht wurde.|

> [!NOTE]
> Sie können Ihre Integrationstabellenzuordnungen so einrichten, dass diese Aktionen automatisch angewendet werden, um die Anzahl der Konflikte zu verringern, die Sie lösen müssen. Weitere Informationen finden Sie unter [Zuordnen von Integrationstabellen](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>So zeigen Sie das Synchronisierungsprotokoll für einen bestimmten (manuell synchronisierten) Datensatz an
1. Öffnen Sie z.B. einen Debitor, einen Artikel oder jeden anderen Datensatz, der Daten zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert.
2. Wählen Sie die Aktion **Synchronisierungs-Protokoll** aus, um das Synchronisierungsprotokoll für einen ausgewählten Datensatz anzuzeigen. Beispielsweise ein bestimmter Debitor, den Sie manuell synchronisierten.

## <a name="remove-couplings-between-records"></a>Kopplungen zwischen Datensätzen entfernen
Wenn bei Ihrer Integration ein Fehler auftritt und Sie Datensätze entkoppeln müssen, um die Synchronisierung zu beenden, können Sie dies für einen oder mehrere Datensätze gleichzeitig tun. Sie können einen oder mehrere Datensätze von Listenseiten oder der Seite **Fehler bei der Synchronisierung gekoppelter Daten** durch Auswahl einer oder mehrerer Zeilen und Auswahl von **Kopplung löschen** entkoppeln. Sie können auch alle Kupplungen für eine oder mehrere Tabellenzuordnungen auf der Seite **Zuordnungen der Integrationstabelle** entfernen. 

Wenn eine Entität mit einer unidirektionalen Kopplung in [!INCLUDE[prod_short](includes/prod_short.md)] gelöscht wird, müssen Sie die unterbrochene Kopplung manuell löschen. Wählen Sie dazu auf der Seite **Gekoppelte Daten-Synchronisationsfehler** die Aktion **Für Gelöschte suchen** und löschen Sie dann die Kopplungen.

## <a name="see-also"></a>Weitere Informationen  
[Einrichten von Benutzerkonten für die Integration mit Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]