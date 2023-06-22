---
title: Manuelle Synchronisation von Tabellenzuordnungen | Microsoft Docs
description: 'Die Synchronisierung kopiert Daten zwischen Microsoft Dataverse Tabellen und Business Central, um beide Systeme auf dem neuesten Stand zu halten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="manually-synchronize-table-mappings" />Synchronisieren Sie Tabellenzuordnungen manuell


Eine Integrationstabellenzuordnung ordnet eine [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle (Datensatztyp), beispielsweise Debitor, einer [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabelle wie einem Konto zu. Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht es Ihnen, Daten in allen Datensätzen der [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle und der [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabelle, die gekoppelt sind, zu synchronisieren. Je nach Konfiguration der Tabellenzuordnung kann die Synchronisierung zudem neue Datensätze in der Ziellösung für ungekoppelte Datensätze in der Quelle erstellen und koppeln.  

Manuelle Synchronisation von Integrationstabellenzuordnungen kann bei der anfänglichen Einrichtung einer Integration und bei der Diagnose von Synchronisierungsfehlern hilfreich sein.  

Dieser Artikel beschreibt drei Methoden für manuelle Synchronisierung von Integrationstabellenzuordnungen. Jede Methode bietet eine andere Stufe der Synchronisierung.

## <a name="run-a-full-synchronization" />Ausführen einer vollständigen Synchronisierung
Eine vollständige Synchronisierung führt alle Standardintegrationssynchronisierungsprojekte für die Synchronisierung von [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätzen und [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabellen aus, wie auf der Seite **Integrationstabellenzuordnungen** definiert. 

Eine vollständige Synchronisierung führt die folgenden Arbeitsgänge für [!INCLUDE[prod_short](includes/prod_short.md)] oder [!INCLUDE[prod_short](includes/cds_long_md.md)]-Datensätze aus, und zwar:

* Nicht gekoppelt, ein neuer zugeordneten Zeile wird in der entgegengesetzten Lösung erstellt und gekoppelt.
Ob und wo eine Zeile erstellt wird, hängt von der Synchronisierungsrichtung ab. Wenn beispielsweise Daten von [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren mit [!INCLUDE[prod_short](includes/cds_long_md.md)]-Konten synchronisiert werden und ein Debitor nicht mit einem Konto gekoppelt ist, wird ein automatisch neues Konto in [!INCLUDE[prod_short](includes/cds_long_md.md)] hinzugefügt und in [!INCLUDE[prod_short](includes/prod_short.md)] mit dem Kunden gekoppelt. Das Gegenteil ist der Fall, wenn die Synchronisierungsrichtung von [!INCLUDE[prod_short](includes/cds_long_md.md)] zu [!INCLUDE[prod_short](includes/prod_short.md)] führt. Für jedes Konto, das nicht bereits mit einem Debitor gekoppelt ist, wird ein neuer passender Debitor in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt und mit dem Konto in [!INCLUDE[prod_short](includes/cds_long_md.md)] gekoppelt.  

     > [!NOTE]  
     >  Dazu löscht der gesamte Synchronisierungsarbeitsgang vorübergehend die Option **Nur gekoppelte Datensätze synchronisieren** in der Integrationstabellenzuordnung, die vom Synchronisierungsprojekt verwendet wird. Am Ende des vollständigen Synchronisierungsprozesses werden Sie aufgefordert zu entscheiden, ob Sie diese Option für alle Projekte löschen möchten.  

* Im gekoppelt Zustand wird die Synchronisierungsrichtung (zum Beispiel von [!INCLUDE[prod_short](includes/prod_short.md)] zu [!INCLUDE[prod_short](includes/cds_long_md.md)] oder von [!INCLUDE[prod_short](includes/cds_long_md.md)]zu [!INCLUDE[prod_short](includes/prod_short.md)]) von den Integrationstabellenzuordnungen vorbestimmt. Weitere Informationen finden Sie unter [Standard Tabellenzuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  In der Regel nutzen Sie die vollständige Synchronisierung nur, wenn Sie erstmalig die Integration zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] einrichten und nur eine Lösung Daten enthält, die Sie zur anderen Lösung kopieren möchten. Eine vollständige Synchronisierung kann in einer Demonstrationsumgebung hilfreich sein. Da die vollständige Synchronisierung automatisch Datensätze zwischen den Lösungen erstellt, ist es schneller, zwischen Datensätzen mit der Synchronisierungsdatenarbeit zu beginnen. Andererseits sollten Sie nur dann eine vollständige Synchronisierung ausführen, wenn Sie eine Zeile in [!INCLUDE[prod_short](includes/prod_short.md)] für jede Zeile in [!INCLUDE[prod_short](includes/cds_long_md.md)] für eine bestimmte Tabellenzuordnungen wünschen. Andernfalls können Sie unerwünschte oder doppelten Datensätze in [!INCLUDE[prod_short](includes/cds_long_md.md)] oder [!INCLUDE[prod_short](includes/prod_short.md)] erhalten.  

### <a name="to-run-a-full-synchronization" />So führen Sie eine vollständige Synchronisierung aus
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Dataverse Einrichtung der Verbindung** ein und wählen Sie dann den zugehörigen Link.

    > [!NOTE]
    > Wenn Sie eine vollständige Synchronisierung für Tabellen über Dynamics 365 Sales ausführen möchten, verwenden Sie stattdessen die Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung**.

2.  Wählen Sie die Aktion **Vollständige Synchronisierung ausführen** aus und wählen Sie dann die Schaltfläche **Ja** aus.  
3.  Wenn die vollständige Synchronisierung abgeschlossen ist, können Sie angeben, ob Sie allen geplanten Synchronisierungsprojekten das Erstellen neuer Datensätze erlauben möchten.  

    Wenn alle Synchronisierungsprojekte neue Datensätze im Ziel für nicht gekoppelte Datensätze in der Quelle erstellen sollen, wählen Sie **Ja**. Dies legt für das Feld **Nur gekoppelte Datensätze synchronisieren** für die Tabellenzuordnungen fest, die von den Synchronisierungsprojekten verwendet werden.  

    Wenn die Synchronisierungsprojekte hinsichtlich der Erstellung neuer Datensätze ausgeführt werden sollen, wie vor der vollständigen Synchronisierung, wählen Sie **Nein**. Damit wird das Feld **Nur gekoppelte Datensätze synchronisieren** auf die Einstellung festgelegt, die es vor der vollständigen Synchronisierung hatte.  

Sie können die Ergebnisse der vollständigen Synchronisierung auf der Seite **Integrationssynchronisierungsprojekte** anzeigen. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records" />Synchronisierung aller geänderten Datensätze
Sie können die Seite **Common Data Service-Verbindungseinrichtung** verwenden, um Änderungen an den Daten in allen Integrationstabellenzuordnungen zu synchronisieren. Dies ist einer vollständigen Synchronisierung ähnlich. Es werden Daten in allen gekoppelten Datensätzen in den [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen und [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabellen synchronisiert, die in den Tabellenzuordnungen definiert werden. Standardmäßig werden nur Daten synchronisiert, die seit der letzten Synchronisierung geändert wurden. Synchronisierungsjobs synchronisieren Tabellenzuordnungen in der folgenden Reihenfolge, um Kopplungsabhängigkeiten zwischen den Tabellen zu vermeiden:  

1.  WÄHRUNG  
2.  VERKÄUFER  
3.  VENDOR  
4.  DEBITOR  
5.  CONTACTS  

Sie können die Ergebnisse der Synchronisierung auf der Seite **Integrationssynchronisierungsprojekte** anzeigen. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Indem die Integrationstabelle im Voraus geändert wird, können Sie die Synchronisation mit Filtern erstellen, um zu steuern, welche Datensätze synchronisiert werden, oder sie so zuzuordnen, dass neue Datensätze in der Ziellösung für nicht gekoppelte Datensätze oder Zeilen in der Quelle erstellt werden. Weitere Informationen finden Sie unter [Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables" />So synchronisieren Sie Daten für alle Tabellen
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Microsoft Dynamics 365 Sales Connection Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2.  Wählen Sie die Aktion **Bearbeitete Datensätze synchronisieren** und dann die Schaltfläche **Ja** aus.  

## <a name="synchronize-individual-table-mappings" />Synchronisieren einzelner Tabellenzuordnungen
Sie können die Seite **Integrationstabellenzuordnungen** verwenden, um das Synchronisationsprojekt für bestimmte Tabellenzuordnungen auszuführen. Dadurch werden Daten für alle gekoppelten Datensätze und Zeilen in der [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle und der [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabelle synchronisiert, die von der Tabellenzuordnung definiert werden. Standardmäßig werden nur Daten synchronisiert, die seit der letzten Synchronisierung geändert wurden.  

### <a name="to-synchronize-records-of-an-integration-table-mapping" />So synchronisieren Sie Datensätze einer Integrationstabellenzuordnung
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Integrationstabellenzuordnungen** ein und wählen Sie dann den zugehörigen Link.
2.  Wählen Sie die Aktion **Bearbeitete Datensätze synchronisieren** und dann die Schaltfläche **Ja** aus.  

## <a name="see-also" />Siehe auch
[Synchronisieren von Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Einrichten von Benutzerkonten für die Integration mit Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
