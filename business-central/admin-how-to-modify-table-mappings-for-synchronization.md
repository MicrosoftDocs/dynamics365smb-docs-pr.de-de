---
title: Tabellenzuordnungen für die Synchronisierung ändern | Microsoft Docs
description: Erfahren Sie, wie die Tabellenzuordnungen geändert werden, die verwendet werden, wenn Daten zwischen Business Central und Dynamics 365 for Sales synchronisiert werden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: de924baa494ae00c09dcb7657c050f2d9ae3ba87
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940174"
---
# <a name="modify-table-mappings-for-synchronization"></a>Tabellenzuordnungen für die Synchronisierung ändern
Eine Integrationstabellenzuordnung verknüpft eine Tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit einer Integrationstabelle für die [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit. Für jede Einheit in [!INCLUDE[crm_md](includes/crm_md.md)], die Sie mit dazugehörenden Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, muss eine dazugehörende Integrationstabellenzuordnung vorhanden sein. Eine Integrationstabellenzuordnung umfasst eine Reihe von Einstellungen, mit denen Sie steuern können, wie Datensätze in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und einer [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit von den entsprechenden Integrationssynchronisierungsprojekten synchronisiert werden.  

## <a name="filtering-records"></a>Datensätze filtern  
 Falls Sie nicht alle Datensätze für eine bestimmte Einheit in [!INCLUDE[crm_md](includes/crm_md.md)] oder Tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, können Sie Filter einrichten, um die Datensätze zu begrenzen, die synchronisiert werden. Sie können Filter auf der Seite **Integrationstabellenzuordnungen** einrichten.  

#### <a name="to-filter-records-for-synchronization"></a>So filtern Sie Datensätze für die Synchronisierung:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link aus.

2.  Um die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze zu filtern, legen Sie das Feld **Tabellenfilter** fest.  

3.  Um die [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze zu filtern, legen Sie das Feld **Integrationstabellenfilter** fest.  

## <a name="creating-new-records"></a>Neue Datensätze erstellen  
 Standardmäßig werden nur Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)], die gekoppelt sind, durch die Integrationssynchronisierungsprojekte synchronisiert. Sie können Tabellenzuordnungen einrichten, sodass für jeden Datensatz am Quellort (z. B. [!INCLUDE[d365fin](includes/d365fin_md.md)]), der nicht bereits gekoppelt ist, neue Datensätze am Zielort (z. B. [!INCLUDE[crm_md](includes/crm_md.md)]) erstellt werden.  

 Das Dynamics 365 for Sales-Synchronisierungsprojekt VERKÄUFER verwendet zum Beispiel die Tabellenzuordnung VERKÄUFER. Das Synchronisierungsprojekt kopiert Daten aus Benutzerdatensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] in Verkäuferdatensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wenn Sie die Tabellenzuordnung einrichten, um neue Datensätze zu erstellen, wird für jeden Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)], der nicht bereits an einen Verkäufer in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt ist, ein neuer Verkäuferdatensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt.  

#### <a name="to-create-new-records-during-synchronization"></a>So erstellen Sie neue Datensätze während der Synchronisierung:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link aus.

2.  Deaktivieren Sie im Tabellenzuordnungseintrag in der Liste das Feld **Nur gekoppelte Datensätze synchronisieren**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Konfigurationsvorlagen für Tabellenzuordnungen verwenden
Sie können den Tabellenzuordnungen Konfigurationsvorlagen zur Verwendung für neue Datensätze zuweisen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden. Für jede Tabellenzuordnung können Sie eine Konfigurationsvorlage zur Verwendung für neue [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze und eine andere Vorlage zur Verwendung für neue [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze angeben.  

Wenn Sie die standardmäßige Synchronisierungskonfiguration einrichten, werden meistens zwei Konfigurationsvorlagen automatisch erstellt und in der Tabellenzuordnung für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren und [!INCLUDE[crm_md](includes/crm_md.md)]-Konten verwendet: **CRMCUST** und **CRMACCOUNT**.  

-   **CRMCUST** wird verwendet, um neue Debitoren in [!INCLUDE[d365fin](includes/d365fin_md.md)] auf der Basis eines Kontos in [!INCLUDE[crm_md](includes/crm_md.md)] zu erstellen und zu synchronisieren.  

     Diese Vorlage wird erstellt, indem eine vorhandene Konfigurationsvorlage für Debitoren in der Anwendung kopiert wird. **CRMCUST** wird nur erstellt, fall es eine vorhandene Konfigurationsvorlage gibt und das Feld **Währungscode** in der Vorlage leer ist. Wenn ein Feld in der Konfigurationsvorlage einen Wert enthält, wird der Wert anstelle des Werts in dem zugeordneten Feld im [!INCLUDE[crm_md](includes/crm_md.md)]-Konto verwendet. Wenn es sich beispielsweise beim Feld **Land/Region** in einem [!INCLUDE[crm_md](includes/crm_md.md)]-Konto um *US* handelt und das Feld **Land/Region** in der Konfigurationsvorlage *GB* lautet, dann wird *GB* für **Land/Region** im Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet.  

-   **CRMACCOUNT** erstellt und synchronisiert neue Konten in [!INCLUDE[crm_md](includes/crm_md.md)] auf der Basis eines Kontos in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>So bestimmen Sie Konfigurationsvorlagen für eine Tabellenzuordnung:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link aus.

2.  Wählen Sie im Tabellenzuordnungseintrag in der Liste im Feld **Vorlagencode Tabellenkonfiguration** die Konfigurationsvorlage aus, die für neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden soll.  

3.  Legen Sie das Feld **Int. Vorlagencode Tabellenkonfiguration** auf die Konfigurationsvorlage fest, die für neue Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] verwendet werden soll.

## <a name="see-also"></a>Siehe auch  
[Über das Integrieren von Dynamics 365 Business Central mit Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Central und Dynamics 365 for Sales synchronisieren](admin-synchronizing-business-central-and-sales.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
