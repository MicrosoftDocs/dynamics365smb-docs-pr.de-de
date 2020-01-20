---
title: Zu synchronisierende Tabellen und Felder zuordnen | Microsoft Docs
description: Erfahren Sie, wie Sie Tabellen und Felder zum Synchronisieren von Daten zwischen Business Central und Dynamics 365 Sales zuordnen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943113"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Zu synchronisierende Tabellen und Felder zuordnen
Die Basis für die Synchronisation von Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Daten in [!INCLUDE[crm_md](includes/crm_md.md)] ist das einander Zuordnen der Tabellen und Felder, die die Daten enthalten. Die Zuordnung erfolgt über Integrationstabellen. 

## <a name="mapping-integration-tables"></a>Zuordnen von Integrationstabellen
Eine Integrationstabelle ist eine Tabelle in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, die eine Entität wie ein Konto in [!INCLUDE[crm_md](includes/crm_md.md)] darstellt. Integrationstabellen umfassten Felder, die Feldern in der Tabelle für die [!INCLUDE[crm_md](includes/crm_md.md)]-Entität entsprechen. Die Kontointegrationstabelle stellt beispielsweise eine Verbindung zur Entität „Konten“ in [!INCLUDE[crm_md](includes/crm_md.md)] her. Es muss für jede Einheit in [!INCLUDE[crm_md](includes/crm_md.md)], die Sie mit Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, eine dazugehörende Integrationstabellenzuordnung vorhanden sein.

Wenn Sie die Verbindung zwischen den Apps herstellen, richtet [!INCLUDE[d365fin](includes/d365fin_md.md)] einige Standardzuordnungen für Tabellen und Felder ein. Sie können die Tabellenzuordnungen auf Wunsch ändern. Weitere Informationen finden Sie unter [Standard-Sales-Entitätszuordnungen für die Synchronisierung](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Wenn Sie die Standardzuordnungen geändert haben und Ihre Änderungen rückgängig machen möchten, wählen Sie auf der Seite **Dynamics 365-Verbindungseinrichtung** die Option **Standard-Synchronisierungskonfiguration verwenden** aus.

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden die Integrationstabellenzuordnungen in Tabelle 5335 „Integrationstabellenzuordnungen“ gespeichert und können auf der Seite 5335 „Integrationstabellenzuordnungen“ angezeigt und geändert werden. Komplexe Zuordnungen und Synchronisierungsregeln werden in der Codeunit 5341 definiert. 

### <a name="synchronization-rules"></a>Synchronisierungsregeln
Eine Integrationstabellenzuordnung enthält auch Regeln, die steuern, wie Integrationssynchronisationsaufträge Datensätze in einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und eine Einheit in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisieren. Weitere Informationen finden Sie unter [Synchronisierungsregeln](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Zuordnen von Integrationsfeldern
Das Zuordnen von Tabellen ist nur der erste Schritt. Sie müssen auch die Felder in den Tabellen zuordnen. Integrationsfeldzuordnungen verknüpfen Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen entsprechenden Feldern in [!INCLUDE[crm_md](includes/crm_md.md)] zu und bestimmen, ob Daten in jeder Tabelle synchronisiert werden sollen. Die Standardtabellenzuordnung, die von [!INCLUDE[d365fin](includes/d365fin_md.md)] bereitgestellt wird, umfasst Feldzuordnungen, aber Sie können diese, wenn gewünscht ändern. Weitere Informationen finden Sie unter [Anzeigen von Entitätszuordnungen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden Integrationsfeldzuordnungen in Tabelle 5336 „Integrationsfeldzuordnung“ definiert.

## <a name="coupling-records"></a>Kopplungsdatensätze
Kopplungsverknüpfungssätze in [!INCLUDE[crm_md](includes/crm_md.md)] zu Datensätzen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zum Beispiel sind Konten in [!INCLUDE[crm_md](includes/crm_md.md)] in der Regel mit Kunden in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt. Das Koppeln von Datensätzen bietet folgende Vorteile:

* Es ermöglicht die Synchronisation.
* Benutzer können Datensätze in einer Geschäftsanwendung eines anderen Benutzers öffnen. Dazu ist es erforderlich, dass die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert wurde.

Kopplungen können automatisch eingerichtet werden, indem die Synchronisierungsaufgaben verwendet werden, oder sie können manuell erfolgen, indem der Datensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] bearbeitet wird. Weitere Informationen finden Sie unter [Synchronisieren von Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)]und [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) und [Manuelles Koppeln und Synchronisieren von Datensätzen ](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Datensätze filtern  
Falls Sie nicht alle Datensätze für eine bestimmte Einheit in [!INCLUDE[crm_md](includes/crm_md.md)] oder Tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, können Sie Filter einrichten, um die Datensätze zu begrenzen, die synchronisiert werden. Sie können Filter auf der Seite **Integrationstabellenzuordnungen** einrichten.  

#### <a name="to-filter-records-for-synchronization"></a>So filtern Sie Datensätze für die Synchronisierung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Um die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze zu filtern, legen Sie das Feld **Tabellenfilter** fest.  

3.  Um die [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze zu filtern, legen Sie das Feld **Integrationstabellenfilter** fest.  

## <a name="creating-new-records"></a>Neue Datensätze erstellen  
 Standardmäßig werden nur Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)], die gekoppelt sind, durch die Integrationssynchronisierungsprojekte synchronisiert. Sie können Tabellenzuordnungen einrichten, sodass für jeden Datensatz am Quellort (z. B. [!INCLUDE[d365fin](includes/d365fin_md.md)]), der nicht bereits gekoppelt ist, neue Datensätze am Zielort (z. B. [!INCLUDE[crm_md](includes/crm_md.md)]) erstellt werden.  

 Beispielsweise verwendet der SALESPEOPLE - Dynamics 365 Sales Synchronisierungsauftrag die Tabellenzuordnung VERKÄUFER. Das Synchronisierungsprojekt kopiert Daten aus Benutzerdatensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] in Verkäuferdatensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wenn Sie die Tabellenzuordnung einrichten, um neue Datensätze zu erstellen, wird für jeden Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)], der nicht bereits an einen Verkäufer in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt ist, ein neuer Verkäuferdatensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt.  

#### <a name="to-create-new-records-during-synchronization"></a>So erstellen Sie neue Datensätze während der Synchronisierung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Deaktivieren Sie im Tabellenzuordnungseintrag in der Liste das Feld **Nur gekoppelte Datensätze synchronisieren**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Konfigurationsvorlagen für Tabellenzuordnungen verwenden
Sie können den Tabellenzuordnungen Konfigurationsvorlagen zur Verwendung für neue Datensätze zuweisen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden. Für jede Tabellenzuordnung können Sie eine Konfigurationsvorlage zur Verwendung für neue [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze und eine andere Vorlage zur Verwendung für neue [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze angeben.  

Wenn Sie die standardmäßige Synchronisierungskonfiguration einrichten, werden meistens zwei Konfigurationsvorlagen automatisch erstellt und in der Tabellenzuordnung für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren und [!INCLUDE[crm_md](includes/crm_md.md)]-Konten verwendet: **CRMCUST** und **CRMACCOUNT**.  

-   **CRMCUST** wird verwendet, um neue Debitoren in [!INCLUDE[d365fin](includes/d365fin_md.md)] auf der Basis eines Kontos in [!INCLUDE[crm_md](includes/crm_md.md)] zu erstellen und zu synchronisieren.  

     Diese Vorlage wird erstellt, indem eine vorhandene Konfigurationsvorlage für Debitoren in der Anwendung kopiert wird. **CRMCUST** wird nur erstellt, fall es eine vorhandene Konfigurationsvorlage gibt und das Feld **Währungscode** in der Vorlage leer ist. Wenn ein Feld in der Konfigurationsvorlage einen Wert enthält, wird der Wert anstelle des Werts in dem zugeordneten Feld im [!INCLUDE[crm_md](includes/crm_md.md)]-Konto verwendet. Wenn es sich beispielsweise beim Feld **Land/Region** in einem [!INCLUDE[crm_md](includes/crm_md.md)]-Konto um *US* handelt und das Feld **Land/Region** in der Konfigurationsvorlage *GB* lautet, dann wird *GB* für **Land/Region** im Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet.  

-   **CRMACCOUNT** erstellt und synchronisiert neue Konten in [!INCLUDE[crm_md](includes/crm_md.md)] auf der Basis eines Kontos in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>So bestimmen Sie Konfigurationsvorlagen für eine Tabellenzuordnung:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.

2.  Wählen Sie im Tabellenzuordnungseintrag in der Liste im Feld **Vorlagencode Tabellenkonfiguration** die Konfigurationsvorlage aus, die für neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden soll.  

3.  Legen Sie das Feld **Int. Vorlagencode Tabellenkonfiguration** auf die Konfigurationsvorlage fest, die für neue Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] verwendet werden soll.

## <a name="see-also"></a>Siehe auch  
[Über Integration Dynamics 365 Business Central mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synchronisieren von Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
