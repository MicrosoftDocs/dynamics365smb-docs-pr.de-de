---
title: Manuelle Synchronisation von Tabellenzuordnungen | Microsoft Docs
description: Die Synchronisierung kopiert Daten zwischen Dynamics 365 Sales-Einträgen und Business Central, um beide Systeme auf dem neuesten Stand zu halten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4aa56deaef4cd32f58fe4ad17abbc72a58b94ed9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307938"
---
# <a name="manually-synchronize-table-mappings"></a>Synchronisieren Sie Tabellenzuordnungen manuell
Eine Integrationstabellenzuordnung ordnet eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle (Datensatztyp), beispielsweise Debitor, einer [!INCLUDE[crm_md](includes/crm_md.md)]-Entität wie einem Konto zu. Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht es Ihnen, Daten in allen Datensätzen der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und der [!INCLUDE[crm_md](includes/crm_md.md)]-Entität, die gekoppelt sind, zu synchronisieren. Je nach Konfiguration der Tabellenzuordnung kann die Synchronisierung zudem neue Datensätze in der Ziellösung für ungekoppelte Datensätze in der Quelle erstellen und koppeln.  

Manuelle Synchronisation von Integrationstabellenzuordnungen kann bei der anfänglichen Einrichtung einer Integration und bei der Diagnose von Synchronisierungsfehlern hilfreich sein.  

Dieser Artikel beschreibt drei Methoden für manuelle Synchronisierung von Integrationstabellenzuordnungen. Jede Methode bietet eine andere Stufe der Synchronisierung.

## <a name="run-a-full-synchronization"></a>Ausführen einer vollständigen Synchronisierung
Eine vollständige Synchronisierung führt alle Standardintegrationssynchronisierungsprojekte für die Synchronisierung von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und [!INCLUDE[crm_md](includes/crm_md.md)]-Entitäten aus, wie auf der Seite **Integrationstabellenzuordnungen** definiert. 

Eine vollständige Synchronisierung führt die folgenden Arbeitsgänge für [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze aus, und zwar:

* Nicht gekoppelt, ein neuer zugeordneter Datensatz wird in der entgegengesetzten Lösung erstellt und gekoppelt.
Ob und wo ein Datensatz erstellt wird, hängt von der Synchronisierungsrichtung ab. Wenn beispielsweise Daten von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren mit [!INCLUDE[crm_md](includes/crm_md.md)]-Konten synchronisiert werden und ein Debitor nicht mit einem Konto gekoppelt ist, wird ein automatisch neues Konto in [!INCLUDE[crm_md](includes/crm_md.md)] hinzugefügt und in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit dem Kunden gekoppelt. Das Gegenteil ist der Fall, wenn die Synchronisierungsrichtung von [!INCLUDE[crm_md](includes/crm_md.md)] zu [!INCLUDE[d365fin](includes/d365fin_md.md)] führt. Für jedes Konto, das nicht bereits mit einem Debitor gekoppelt ist, wird ein neuer passender Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt und mit dem Konto in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt.  

     > [!NOTE]  
     >  Dazu löscht der gesamte Synchronisierungsarbeitsgang vorübergehend die Option **Nur gekoppelte Datensätze synchronisieren** in der Integrationstabellenzuordnung, die vom Synchronisierungsprojekt verwendet wird. Am Ende des vollständigen Synchronisierungsprozesses werden Sie aufgefordert zu entscheiden, ob Sie diese Option für alle Projekte löschen möchten.  

* Im gekoppelt Zustand wird die Synchronisierungsrichtung (zum Beispiel von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu [!INCLUDE[crm_md](includes/crm_md.md)] oder von [!INCLUDE[crm_md](includes/crm_md.md)]zu [!INCLUDE[d365fin](includes/d365fin_md.md)]) von den Integrationstabellenzuordnungen vorbestimmt. Weitere Informationen finden Sie unter [Standard-Sales-Entitätszuordnungen für die Synchronisierung](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

Die Projekte werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Einheiten zu vermeiden.  

1.  WÄHRUNG - Dynamics 365 Sales Synchronisierungsauftrag  
2.  VERKäUFER - Dynamics 365 Sales Synchronisierungsauftrag  
3.  UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag  
4.  DEBITOR - Dynamics 365 Sales Synchronisierungsauftrag  
5.  KONTAKTE - Dynamics 365 Sales Synchronisierungsauftrag  
6.  RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
7.  ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  

> [!IMPORTANT]  
>  In der Regel nutzen Sie die vollständige Synchronisierung nur, wenn Sie erstmalig die Integration zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] einrichten und nur eine Lösung Daten enthält, die Sie zur anderen Lösung kopieren möchten. Eine vollständige Synchronisierung kann in einer Demonstrationsumgebung hilfreich sein. Da die vollständige Synchronisierung automatisch Datensätze zwischen den Lösungen erstellt, ist es schneller, zwischen Datensätzen mit der Synchronisierungsdatenarbeit zu beginnen. Andererseits sollten Sie nur dann eine vollständige Synchronisierung ausführen, wenn Sie einen Datensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] für jeden Datensatz in [!INCLUDE[crm_md](includes/crm_md.md)] für eine bestimmte Tabellenzuordnungen wünschen. Andernfalls können Sie unerwünschte oder doppelten Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] oder [!INCLUDE[d365fin](includes/d365fin_md.md)] erhalten.  

### <a name="see-the-process-for-a-full-synchronization"></a>Sehen Sie sich den Vorgang für eine vollständige Synchronisierung an
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>So führen Sie eine vollständige Synchronisierung aus  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Microsoft Dynamics 365 Sales Verbindungseinrichtung** ein, und wählen dann den zugehörigen Link aus.
2.  Wählen Sie die Aktion **Vollständige Synchronisierung ausführen** aus und wählen Sie dann die Schaltfläche **Ja** aus.  
3.  Wenn die vollständige Synchronisierung abgeschlossen ist, können Sie angeben, ob Sie allen geplanten Synchronisierungsprojekten das Erstellen neuer Datensätze erlauben möchten.  

    Wenn alle Synchronisierungsprojekte neue Datensätze im Ziel für nicht gekoppelte Datensätze in der Quelle erstellen sollen, wählen Sie **Ja**. Dies legt für das Feld **Nur gekoppelte Datensätze synchronisieren** für die Tabellenzuordnungen fest, die von den Synchronisierungsprojekten verwendet werden.  

    Wenn die Synchronisierungsprojekte hinsichtlich der Erstellung neuer Datensätze ausgeführt werden sollen, wie vor der vollständigen Synchronisierung, wählen Sie **Nein**. Damit wird das Feld **Nur gekoppelte Datensätze synchronisieren** auf die Einstellung festgelegt, die es vor der vollständigen Synchronisierung hatte.  

Sie können die Ergebnisse der vollständigen Synchronisierung auf der Seite **Integrationssynchronisierungsprojekte** anzeigen. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synchronisierung aller geänderten Datensätze
Sie können die Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** verwenden, um Änderungen an den Daten in allen Integrationstabellenzuordnungen zu synchronisieren. Dies ist einer vollständigen Synchronisierung ähnlich. Es werden Daten in allen gekoppelten Datensätzen in den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen und [!INCLUDE[crm_md](includes/crm_md.md)]-Einheiten synchronisiert, die in den Tabellenzuordnungen definiert werden. Standardmäßig werden nur Datensätze synchronisiert, die seit der letzten Synchronisierung geändert wurden. Die Tabellenzuordnungen werden in der folgenden Reihenfolge synchronisiert, um Kopplungsabhängigkeiten zwischen den Einheiten zu vermeiden:  

1.  WÄHRUNG - Dynamics 365 Sales Synchronisierungsauftrag  
2.  VERKäUFER - Dynamics 365 Sales Synchronisierungsauftrag  
3.  UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag  
4.  DEBITOR - Dynamics 365 Sales Synchronisierungsauftrag  
5.  KONTAKTE - Dynamics 365 Sales Synchronisierungsauftrag  
6.  RESSOURCE-PRODUKT \- Dynamics 365 Sales Synchronisierungsauftrag  
7.  ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  

Sie können die Ergebnisse der Synchronisierung auf der Seite **Integrationssynchronisierungsprojekte** anzeigen. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Indem die Integrationstabelle im Voraus geändert wird, können Sie die Synchronisation mit Filtern konfigurieren, um zu steuern, welche Datensätze synchronisiert werden, oder sie so konfigurieren, dass neue Datensätze in der Ziellösung für nicht gekoppelte Datensätze in der Quelle erstellt werden. Weitere Informationen finden Sie unter [Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>So synchronisieren Sie Datensätze für alle Tabellen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Microsoft Dynamics 365 Sales Verbindungseinrichtung** ein, und wählen dann den zugehörigen Link aus.
2.  Wählen Sie die Aktion **Bearbeitete Datensätze synchronisieren** und dann die Schaltfläche **Ja** aus.  

## <a name="synchronize-individual-table-mappings"></a>Synchronisieren einzelner Tabellenzuordnungen
Sie können die Seite **Integrationstabellenzuordnungen** verwenden, um ein Synchronisationsprojekt für bestimmte Tabellenzuordnungen auszuführen. Dadurch werden Daten in allen gekoppelten Datensätzen in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und der [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisiert, die von der Tabellenzuordnung definiert werden. Standardmäßig werden nur Datensätze synchronisiert, die seit der letzten Synchronisierung geändert wurden.  

Durch die Änderung der im Voraus erfolgten Integrationstabellenzuordnung können Sie das Synchronisierungsprojekt konfigurieren, um neue Datensätze in der Ziellösung für nicht gekoppelte Datensätze in der Quelle zu erstellen.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>So synchronisieren Sie Datensätze einer Integrationstabellenzuordnung  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link aus.
2.  Wählen Sie die Aktion **Bearbeitete Datensätze synchronisieren** und dann die Schaltfläche **Ja** aus.  

## <a name="see-also"></a>Siehe auch  
[Synchronisieren von Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   
