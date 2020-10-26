---
title: Zu synchronisierende Tabellen und Felder zuordnen | Microsoft Docs
description: Erfahren Sie, wie Sie Tabellen und Felder für die Datensynchronisation zwischen Business Central und Common Data Service zuordnen können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 382328e88c828afbf4316eb1f9bab73f6a2b7f95
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911380"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Zu synchronisierende Tabellen und Felder zuordnen
Die Basis für die Synchronisation von Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Daten in [!INCLUDE[d365fin](includes/cds_long_md.md)] ist das einander Zuordnen der Tabellen und Felder, die die Daten enthalten. Die Zuordnung erfolgt über Integrationstabellen. 

## <a name="mapping-integration-tables"></a>Zuordnen von Integrationstabellen
Eine Integrationstabelle ist eine Tabelle in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, die eine Entität wie ein Konto in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] darstellt. Integrationstabellen umfassten Felder, die Feldern in der Tabelle für die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Entität entsprechen. Die Kontointegrationstabelle stellt beispielsweise eine Verbindung zur Entität „Konten“ in [!INCLUDE[cds_short_md](includes/cds_long_md.md)] her. Es muss für jede Einheit in [!INCLUDE[cds_short_md](includes/cds_short_md.md)], die Sie mit Daten in [!INCLUDE[prodshort](includes/prodshort.md)] synchronisieren möchten, eine dazugehörende Integrationstabellenzuordnung vorhanden sein.

Wenn Sie die Verbindung zwischen den Apps herstellen, richtet [!INCLUDE[d365fin](includes/d365fin_md.md)] einige Standardzuordnungen für Tabellen und Felder ein. Sie können die Tabellenzuordnungen auf Wunsch ändern. Weitere Informationen finden Sie unter [Standard Entitätszuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Wenn Sie die Standardzuordnungen geändert haben und Ihre Änderungen rückgängig machen möchten, wählen Sie auf der Seite **[!INCLUDE[d365fin](includes/cds_long_md.md)] Verbindungseinrichtung** die Option **Standard-Synchronisierungseinrichtung verwenden** .

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden die Integrationstabellenzuordnungen in Tabelle 5335 „Integrationstabellenzuordnungen“ gespeichert und können auf der Seite 5335 „Integrationstabellenzuordnungen“ angezeigt und geändert werden. Komplexe Zuordnungen und Synchronisierungsregeln werden in der Codeunit 5341 definiert. 

### <a name="synchronization-rules"></a>Synchronisierungsregeln
Eine Integrationstabellenzuordnung enthält auch Regeln, die steuern, wie Integrationssynchronisationsaufträge Datensätze in einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und eine Einheit in [!INCLUDE[d365fin](includes/cds_long_md.md)] synchronisieren. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategien zur automatischen Lösung von Konflikten
Datenkonflikte können leicht auftreten, wenn Geschäftsanwendungen kontinuierlich Daten austauschen. Es kann beispielsweise vorkommen, dass ein Benutzer einen Datensatz in einer der Anwendungen oder in beiden löscht oder ändert. Um die Anzahl der Konflikte zu verringern, die Sie manuell lösen müssen, können Sie Lösungsstrategien angeben. [!INCLUDE[d365fin](includes/d365fin_md.md)] löst Konflikte dann automatisch gemäß den Regeln in den Strategien.

Integrationstabellenzuordnungen enthalten Regeln, die steuern, wie Datensätze von Synchronisierungsaufträgen synchronisiert werden. Auf der Seite **Integrationstabellenzuordnung** können Sie in den Spalten **Löschkonflikte auflösen** und **Aktualisierungskonflikte auflösen** angeben, wie [!INCLUDE[d365fin](includes/d365fin_md.md)] Konflikte lösen soll, die auftreten, weil Datensätze in Tabellen in der einen oder der anderen Geschäftsanwendung gelöscht oder in beiden aktualisiert wurden. 

In der Spalte **Löschkonflikte auflösen** können Sie auswählen, dass [!INCLUDE[d365fin](includes/d365fin_md.md)] gelöschte Datensätze automatisch wiederherstellen soll, die Kopplung zwischen den Datensätzen entfernen soll oder gar nichts unternehmen. Wenn Sie nichts unternehmen, müssen Sie Konflikte manuell lösen. 

In der Spalte **Aktualisierungskonflikte auflösen** können Sie festlegen, dass [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch eine Datenaktualisierung an die Integrationstabelle sendet, wenn Daten an [!INCLUDE[d365fin](includes/cds_long_md.md)] gesendet werden. Alternativ können Sie auswählen, dass eine Datenaktualisierung aus der Integrationstabelle abgerufen wird, wenn Daten von [!INCLUDE[d365fin](includes/cds_long_md.md)] abgerufen werden. Sie können auch gar nichts festlegen. Wenn Sie nichts unternehmen, müssen Sie Konflikte manuell lösen.

Nachdem Sie die Strategie festgelegt haben, können Sie auf der Seite **Gekoppelte Datensynchronisierungsfehler** die Aktion **Alle wiederholen** zum automatischen Lösen von Konflikten auswählen. 

## <a name="mapping-integration-fields"></a>Zuordnen von Integrationsfeldern
Das Zuordnen von Tabellen ist nur der erste Schritt. Sie müssen auch die Felder in den Tabellen zuordnen. Integrationsfeldzuordnungen verknüpfen Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen entsprechenden Feldern in [!INCLUDE[d365fin](includes/cds_long_md.md)] zu und bestimmen, ob Daten in jeder Tabelle synchronisiert werden sollen. Die Standardtabellenzuordnung, die von [!INCLUDE[d365fin](includes/d365fin_md.md)] bereitgestellt wird, umfasst Feldzuordnungen, aber Sie können diese, wenn gewünscht ändern. Weitere Informationen finden Sie unter [Anzeigen von Entitätszuordnungen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden Integrationsfeldzuordnungen in Tabelle 5336 „Integrationsfeldzuordnung“ definiert.

### <a name="handling-differences-in-field-values"></a>Behandlung von Unterschieden in Feldwerten
Manchmal sind die Werte in den Feldern, die Sie zuordnen möchten, unterschiedlich. Zum Beispiel ist in [!INCLUDE[crm_md](includes/crm_md.md)] der Sprachcode für die Vereinigten Staaten „U.S.“, aber in [!INCLUDE[d365fin](includes/d365fin_md.md)] ist es „US“. Das bedeutet, daß Sie den Wert bei der Datensynchronisation umwandeln müssen. Dies geschieht durch Transformationsregeln, die Sie für die Felder definieren. Sie definieren Transformationsregeln auf der Seite **Integrationstabellenzuordnungen** , indem Sie **Zuordnungen** und dann **Felder** wählen. Vordefinierte Regeln werden bereitgestellt, aber Sie können auch eigene Regeln erstellen. Weitere Informationen finden Sie unter [Transformationsregeln](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Behandlung fehlender Optionswerte bei der Zuordnung
[!INCLUDE[d365fin](includes/cds_long_md.md)] enthält Optionssatzfelder, die Werte liefern, die Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] Feldern vom Typ **Option** zur automatischen Synchronisation zuordnen können. Während der Synchronisierung werden nicht zugeordnete Optionen ignoriert und die fehlenden Optionen werden an die zugehörige [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle angehängt und der **CDS-Optionszuordnung** Systemtabelle hinzugefügt, um später manuell behandelt zu werden. Zum Beispiel, indem er die fehlenden Optionen in einem der beiden Produkte hinzufügt und dann die Zuordnung aktualisiert. Weitere Informationen finden Sie unter [Behandlung fehlender Optionswerte](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Kopplungsdatensätze
Kopplungsverknüpfungssätze in [!INCLUDE[d365fin](includes/cds_long_md.md)] zu Datensätzen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zum Beispiel sind Konten in [!INCLUDE[d365fin](includes/cds_long_md.md)] in der Regel mit Kunden in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt. Das Koppeln von Datensätzen bietet folgende Vorteile:

* Es ermöglicht die Synchronisation.
* Benutzer können Datensätze in einer Geschäftsanwendung eines anderen Benutzers öffnen. Dies setzt voraus, dass die Apps bereits integriert sind.

Kopplungen können automatisch eingerichtet werden, indem die Synchronisierungsaufgaben verwendet werden, oder sie können manuell erfolgen, indem der Datensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] bearbeitet wird. Weitere Informationen finden Sie unter [Synchronisieren von Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)]und [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) und [Manuelles Koppeln und Synchronisieren von Datensätzen ](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Datensätze filtern  
Falls Sie nicht alle Datensätze für eine bestimmte Einheit in [!INCLUDE[d365fin](includes/cds_long_md.md)] oder Tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, können Sie Filter einrichten, um die Datensätze zu begrenzen, die synchronisiert werden. Sie können Filter auf der Seite **Integrationstabellenzuordnungen** einrichten.  

#### <a name="to-filter-records-for-synchronization"></a>So filtern Sie Datensätze für die Synchronisierung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Um die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze zu filtern, legen Sie das Feld **Tabellenfilter** fest.  

3.  Um die [!INCLUDE[d365fin](includes/cds_long_md.md)]-Datensätze zu filtern, legen Sie das Feld **Integrationstabellenfilter** fest.  

## <a name="creating-new-records"></a>Neue Datensätze erstellen  
Standardmäßig werden nur Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)], die gekoppelt sind, durch die Integrationssynchronisierungsprojekte synchronisiert. Sie können Tabellenzuordnungen einrichten, sodass für jeden Datensatz am Quellort (z. B. [!INCLUDE[d365fin](includes/d365fin_md.md)]), der nicht bereits gekoppelt ist, neue Datensätze am Zielort (z. B. [!INCLUDE[d365fin](includes/cds_long_md.md)]) erstellt werden.  

Beispielsweise verwendet der SALESPEOPLE - Dynamics 365 Sales Synchronisierungsauftrag die Tabellenzuordnung VERKÄUFER. Das Synchronisierungsprojekt kopiert Daten aus Benutzerdatensätzen in [!INCLUDE[d365fin](includes/cds_long_md.md)] in Verkäuferdatensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wenn Sie die Tabellenzuordnung einrichten, um neue Datensätze zu erstellen, wird für jeden Benutzer in [!INCLUDE[d365fin](includes/cds_long_md.md)], der nicht bereits an einen Verkäufer in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt ist, ein neuer Verkäuferdatensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt.  

#### <a name="to-create-new-records-during-synchronization"></a>So erstellen Sie neue Datensätze während der Synchronisierung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Deaktivieren Sie im Tabellenzuordnungseintrag in der Liste das Feld **Nur gekoppelte Datensätze synchronisieren** .  

## <a name="using-configuration-templates-on-table-mappings"></a>Konfigurationsvorlagen für Tabellenzuordnungen verwenden
Sie können den Tabellenzuordnungen Konfigurationsvorlagen zur Verwendung für neue Datensätze zuweisen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[d365fin](includes/cds_long_md.md)] erstellt werden. Für jede Tabellenzuordnung können Sie eine Konfigurationsvorlage zur Verwendung für neue [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze und eine andere Vorlage zur Verwendung für neue [!INCLUDE[d365fin](includes/cds_long_md.md)]-Datensätze angeben.  

Wenn Sie das Standard-Synchronisationssetup installieren, werden in den meisten Fällen automatisch zwei Konfigurationsvorlagen erstellt und für die Tabellenzuordnung für [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren und [!INCLUDE[crm_md](includes/crm_md.md)] Konten verwendet: **CDSCUST** und **CDSACCOUNT** .  

-   **CDSCUST** wird verwendet, um neue Debitoren in [!INCLUDE[d365fin](includes/d365fin_md.md)] basierend auf einem Konto in [!INCLUDE[crm_md](includes/crm_md.md)] zu erstellen und zu synchronisieren.  

     Diese Vorlage wird erstellt, indem eine vorhandene Konfigurationsvorlage für Debitoren in der Anwendung kopiert wird. Die Seite **CDSCUST** wird nur erstellt, wenn eine bestehende Konfigurationsvorlage vorhanden ist und das Feld **Währungscode** in der Vorlage leer ist. Wenn ein Feld in der Konfigurationsvorlage einen Wert enthält, wird der Wert anstelle des Werts in dem zugeordneten Feld im [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konto verwendet. Wenn es sich beispielsweise beim Feld **Land/Region** in einem [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konto um *US* handelt und das Feld **Land/Region** in der Konfigurationsvorlage *GB* lautet, dann wird *GB* für **Land/Region** im Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet.  

-   **CDSACCOUNT** erstellt und synchronisiert neue Konten in [!INCLUDE[d365fin](includes/cds_long_md.md)] basierend auf einem Konto in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>So bestimmen Sie Konfigurationsvorlagen für eine Tabellenzuordnung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Wählen Sie im Tabellenzuordnungseintrag in der Liste im Feld **Vorlagencode Tabellenkonfiguration** die Konfigurationsvorlage aus, die für neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden soll.  

3.  Legen Sie das Feld **Int. Vorlagencode Tabellenkonfiguration** auf die Konfigurationsvorlage fest, die für neue Datensätze in [!INCLUDE[d365fin](includes/cds_long_md.md)] verwendet werden soll.

## <a name="see-also"></a>Siehe auch  
[Über das Integrieren von Dynamics 365 Business Central mit [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Central und [!INCLUDE[d365fin](includes/cds_long_md.md)] synchronisieren](admin-synchronizing-business-central-and-sales.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
