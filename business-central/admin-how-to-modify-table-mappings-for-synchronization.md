---
title: Zu synchronisierende Tabellen und Felder zuordnen | Microsoft Docs
description: 'Erfahren Sie, wie Sie Tabellen und Felder für die Datensynchronisation zwischen Business Central und Microsoft Dataverse zuordnen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Zu synchronisierende Tabellen und Felder zuordnen


Die Basis für die Synchronisation von Tabellen und Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] mit Tabellen und Spalten in [!INCLUDE[prod_short](includes/cds_long_md.md)], damit Daten ausgetauscht werden können. Die Zuordnung erfolgt über Integrationstabellen. 

## Zuordnen von Integrationstabellen
Eine Integrationstabelle ist eine Tabelle in der [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank, die eine Tabelle wie ein Konto in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] darstellt. Integrationstabellen umfassten Felder, die Feldern in der Spalte für die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Tabelle entsprechen. Die Kontointegrationstabelle stellt beispielsweise eine Verbindung zur Entität Tabelle in [!INCLUDE[cds_short_md](includes/cds_long_md.md)] her. Es muss für jede Tabelle in [!INCLUDE[cds_short_md](includes/cds_short_md.md)], die Sie mit Daten in [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, eine dazugehörende Integrationstabellenzuordnung vorhanden sein.

Wenn Sie die Verbindung zwischen den Apps herstellen, richtet [!INCLUDE[prod_short](includes/prod_short.md)] einige Standardzuordnungen für die Tabellen und Felder ein. Sie können die Tabellenzuordnungen auf Wunsch ändern. Weitere Informationen finden Sie unter [Standard Tabellenzuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Wenn Sie die Standardzuordnungen geändert haben und Ihre Änderungen rückgängig machen möchten, wählen Sie auf der Seite **Tabellenzuordnungsintegration** die Option **Standard-Synchronisierungseinrichtung** aus.

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, werden die Integrationstabellenzuordnungen in Tabelle 5335 Integrationstabellenzuordnungen gespeichert und können dort angezeigt und geändert werden. Komplexe Zuordnungen und Synchronisierungsregeln werden in der Codeunit 5341 definiert. 

### Zusätzliche Zuordnungen 
Zahlungsbedingungen, Lieferformen und Zusteller können sich ändern, und es kann wichtig sein, sie anpassen zu können. Wenn Sie die Funktion **Funktionsaktualisierung: Zuordnung zu Optionssätzen in Dataverse ohne Code** auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren, können Sie manuell Integrationstabellenzuordnungen für Zahlungsbedingungen (PAYMENT TERMS), Versandformen (SHIPMENT METHOD) und Zusteller (SHIPPING AGENT) hinzufügen. Mit dieser Zuordnung können Sie sicherstellen, dass Ihre Richtlinien für diese Einrichtungen in [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] gleich sind.

### Synchronisierungsregeln
Eine Integrationstabellenzuordnung enthält auch Regeln, die steuern, wie Integrationssynchronisationsaufträge Datensätze in einer [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle und eine Tabelle in [!INCLUDE[prod_short](includes/cds_long_md.md)] synchronisieren. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### Strategien zur automatischen Lösung von Konflikten
Datenkonflikte können leicht auftreten, wenn Geschäftsanwendungen kontinuierlich Daten austauschen. Es kann beispielsweise vorkommen, dass ein Benutzer eine Zeile in einer der Anwendungen oder in beiden löscht oder ändert. Um die Anzahl der Konflikte zu verringern, die Sie manuell lösen müssen, können Sie Lösungsstrategien angeben. [!INCLUDE[prod_short](includes/prod_short.md)] löst Konflikte dann automatisch gemäß den Regeln in den Strategien.

Integrationstabellenzuordnungen enthalten Regeln, die steuern, wie Datensätze von Synchronisierungsaufträgen synchronisiert werden. Auf der Seite **Integrationstabellenzuordnung** können Sie in den Spalten **Löschkonflikte auflösen** und **Aktualisierungskonflikte auflösen** angeben, wie [!INCLUDE[prod_short](includes/prod_short.md)] Konflikte lösen soll, die auftreten, weil Datensätze in Tabellen in der einen oder der anderen Geschäftsanwendung gelöscht oder in beiden aktualisiert wurden. 

In der Spalte **Löschkonflikte auflösen** können Sie auswählen, dass [!INCLUDE[prod_short](includes/prod_short.md)] gelöschte Datensätze automatisch wiederherstellen soll, die Kopplung zwischen den Datensätzen entfernen soll oder gar nichts unternehmen. Wenn Sie nichts unternehmen, müssen Sie Konflikte manuell lösen. 

In der Spalte **Aktualisierungskonflikte auflösen** können Sie festlegen, dass [!INCLUDE[prod_short](includes/prod_short.md)] automatisch eine Datenaktualisierung an die Integrationstabelle sendet, wenn Daten an [!INCLUDE[prod_short](includes/cds_long_md.md)] gesendet werden. Alternativ können Sie auswählen, dass eine Datenaktualisierung aus der Integrationstabelle abgerufen wird, wenn Daten von [!INCLUDE[prod_short](includes/cds_long_md.md)] abgerufen werden. Sie können auch gar nichts festlegen. Wenn Sie nichts unternehmen, müssen Sie Konflikte manuell lösen.

Nachdem Sie die Strategie festgelegt haben, können Sie auf der Seite **Gekoppelte Datensynchronisierungsfehler** die Aktion **Alle wiederholen** zum automatischen Lösen von Konflikten auswählen. 

## Zuordnen von Integrationsfeldern
Das Zuordnen von Tabellen ist nur der erste Schritt. Sie müssen auch die Felder in den Tabellen zuordnen. Integrationsfeldzuordnungen verknüpfen Felder in [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen entsprechenden Spalten in [!INCLUDE[prod_short](includes/cds_long_md.md)] zu und bestimmen, ob Daten in jeder Tabelle synchronisiert werden sollen. Die Standardtabellenzuordnung, die von [!INCLUDE[prod_short](includes/prod_short.md)] bereitgestellt wird, umfasst Feldzuordnungen, aber Sie können diese, wenn gewünscht ändern. Weitere Informationen finden Sie unter [Anzeigen von Tabellenzuordnungen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Wenn Sie eine on-premises Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, sind die Zuordnungen von Integrationsfeldern in Tabelle 5336 Zuordnung von Integrationsfeldern definiert.

Sie können die Felder manuell zuordnen oder den Prozess automatisieren, indem Sie mehrere Felder gleichzeitig anhand von Kriterien für die Übereinstimmung ihrer Werte zuordnen. Weitere Informationen finden Sie unter [Mehrere Datensätze auf der Basis von Feldwertabgleich koppeln](admin-how-to-couple-and-synchronize-records-manually.md).

### Behandlung von Unterschieden in Feldwerten
Manchmal sind die Werte in den Feldern, die Sie zuordnen möchten, unterschiedlich. Zum Beispiel ist in [!INCLUDE[crm_md](includes/crm_md.md)] der Sprachcode für die Vereinigten Staaten „U.S.“, aber in [!INCLUDE[prod_short](includes/prod_short.md)] ist es „US“. Das bedeutet, daß Sie den Wert bei der Datensynchronisation umwandeln müssen. Dies geschieht durch Transformationsregeln, die Sie für die Felder definieren. Sie definieren Transformationsregeln auf der Seite **Integrationstabellenzuordnungen**, indem Sie **Zuordnungen** und dann **Felder** wählen. Vordefinierte Regeln werden bereitgestellt, aber Sie können auch eigene Regeln erstellen. Weitere Informationen finden Sie unter [Transformationsregeln](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### Behandlung fehlender Optionswerte bei der Zuordnung
[!INCLUDE[prod_short](includes/cds_long_md.md)] enthält Optionssatzspalten, die Werte liefern, denen Sie [!INCLUDE[prod_short](includes/prod_short.md)] Felder vom Typ **Option** zur automatischen Synchronisation zuordnen können. Während der Synchronisierung werden nicht zugeordnete Optionen ignoriert und die fehlenden Optionen werden an die zugehörige [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle angehängt und der **CDS-Optionszuordnung** Systemtabelle hinzugefügt, um später manuell behandelt zu werden. Zum Beispiel, indem er die fehlenden Optionen in einem der beiden Produkte hinzufügt und dann die Zuordnung aktualisiert. Weitere Informationen finden Sie unter [Behandlung fehlender Optionswerte](admin-cds-missing-option-values.md).

## Kopplungsdatensätze
Kopplungsverknüpfungszeilen in [!INCLUDE[prod_short](includes/cds_long_md.md)] zu Datensätzen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zum Beispiel sind Konten in [!INCLUDE[prod_short](includes/cds_long_md.md)] in der Regel mit Kunden in [!INCLUDE[prod_short](includes/prod_short.md)] gekoppelt. Das Koppeln von Datensätzen bietet folgende Vorteile:

* Es ermöglicht die Synchronisation.
* Benutzer können Datensätze oder Zeilen in einer Geschäftsanwendung eines anderen Benutzers öffnen. Dies setzt voraus, dass die Apps bereits integriert sind.

Kopplungen können automatisch eingerichtet werden, indem die Synchronisierungsaufgaben verwendet werden, oder sie können manuell erfolgen, indem der Datensatz in [!INCLUDE[prod_short](includes/prod_short.md)] bearbeitet wird. Weitere Informationen finden Sie unter [Synchronisieren von Daten in [!INCLUDE[prod_short](includes/prod_short.md)]und [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) und [Manuelles Koppeln und Synchronisieren von Datensätzen ](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## Filtern von Datensätzen und Zeilen  
Falls Sie nicht alle Zeilen für eine bestimmte Tabelle in [!INCLUDE[prod_short](includes/cds_long_md.md)] oder Tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, können Sie Filter einrichten, um die Datensätze zu begrenzen, die synchronisiert werden. Sie können Filter auf der Seite **Integrationstabellenzuordnungen** einrichten.  

#### So filtern Sie Datensätze oder Zeilen für die Synchronisierung  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Integrationstabellenzuordnungen** ein und wählen Sie dann den zugehörigen Link.

2.  Um die [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze zu filtern, legen Sie das Feld **Tabellenfilter** fest.  

3.  Um die [!INCLUDE[prod_short](includes/cds_long_md.md)] Zeilen zu filtern, legen Sie das Feld **Integrationstabellenfilter** fest.  

## Neue Datensätze erstellen  
Standardmäßig werden nur Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] und Zeilen in [!INCLUDE[prod_short](includes/cds_long_md.md)], die gekoppelt sind, durch die Integrationssynchronisierungsprojekte synchronisiert. Sie können Tabellenzuordnungen einrichten, sodass für jeden Datensatz oder Zeile am Quellort (z. B. [!INCLUDE[prod_short](includes/prod_short.md)]), die nicht bereits gekoppelt sind, neue Datensätze am Zielort (z. B. [!INCLUDE[prod_short](includes/cds_long_md.md)]) erstellt werden.  

Beispielsweise verwendet der SALESPEOPLE - Dynamics 365 Sales Synchronisierungsauftrag die Tabellenzuordnung VERKÄUFER. Das Synchronisierungsprojekt kopiert Daten von Benutzern in [!INCLUDE[prod_short](includes/cds_long_md.md)] in Verkäuferdatensätze in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie die Tabellenzuordnung einrichten, um neue Datensätze zu erstellen, wird für jeden Benutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)], der nicht bereits an einen Verkäufer in [!INCLUDE[prod_short](includes/prod_short.md)] gekoppelt ist, eine neue Verkäuferzeile in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt.  

#### So erstellen Sie neue Datensätze während der Synchronisierung:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Integrationstabellenzuordnungen** ein und wählen Sie dann den zugehörigen Link.

2.  Deaktivieren Sie im Tabellenzuordnungseintrag in der Liste das Feld **Nur gekoppelte Datensätze synchronisieren**.  

## Konfigurationsvorlagen für Tabellenzuordnungen verwenden
Sie können den Tabellenzuordnungen Konfigurationsvorlagen zur Verwendung für neue Datensätze oder Zeilen zuweisen, die in [!INCLUDE[prod_short](includes/prod_short.md)] oder [!INCLUDE[prod_short](includes/cds_long_md.md)] erstellt werden. Für jede Tabellenzuordnung können Sie eine Konfigurationsvorlage zur Verwendung für neue [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze und eine andere Vorlage zur Verwendung für neue [!INCLUDE[prod_short](includes/cds_long_md.md)] Zeilen angeben.  

Wenn Sie das Standard-Synchronisationssetup installieren, werden in den meisten Fällen automatisch zwei Konfigurationsvorlagen erstellt und für die Tabellenzuordnung für [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren und [!INCLUDE[crm_md](includes/crm_md.md)] Konten verwendet: **CDSCUST** und **CDSACCOUNT**.  

-   **CDSCUST** wird verwendet, um neue Debitoren in [!INCLUDE[prod_short](includes/prod_short.md)] basierend auf einem Konto in [!INCLUDE[crm_md](includes/crm_md.md)] zu erstellen und zu synchronisieren.  

     Diese Vorlage wird erstellt, indem eine vorhandene Konfigurationsvorlage für Debitoren in der Anwendung kopiert wird. Die Seite **CDSCUST** wird nur erstellt, wenn eine bestehende Konfigurationsvorlage vorhanden ist und das Feld **Währungscode** in der Vorlage leer ist. Wenn ein Feld in der Konfigurationsvorlage einen Wert enthält, wird der Wert anstelle des Werts in dem zugeordneten Spalte im [!INCLUDE[prod_short](includes/cds_long_md.md)]-Konto verwendet. Wenn es sich beispielsweise bei der Spalte **Land/Region** in einem [!INCLUDE[prod_short](includes/cds_long_md.md)]-Konto um *US* handelt und das Feld **Land/Region** in der Konfigurationsvorlage *GB* lautet, dann wird *GB* für **Land/Region** im Debitor in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet.  

-   **CDSACCOUNT** erstellt und synchronisiert neue Konten in [!INCLUDE[prod_short](includes/cds_long_md.md)] basierend auf einem Konto in [!INCLUDE[prod_short](includes/prod_short.md)].  

#### So bestimmen Sie Konfigurationsvorlagen für eine Tabellenzuordnung:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Integrationstabellenzuordnungen** ein und wählen Sie dann den zugehörigen Link.

2.  Wählen Sie im Tabellenzuordnungseintrag in der Liste im Feld **Vorlagencode Tabellenkonfiguration** die Konfigurationsvorlage aus, die für neue Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden soll.  

3.  Legen Sie das Feld **Int. Vorlagencode Tabellenkonfiguration** auf die Konfigurationsvorlage fest, die für neue Datensätze in [!INCLUDE[prod_short](includes/cds_long_md.md)] verwendet werden soll.

## Siehe auch  
[Über das Integrieren von Dynamics 365 Business Central mit [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Central und [!INCLUDE[prod_short](includes/cds_long_md.md)] synchronisieren](admin-synchronizing-business-central-and-sales.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]