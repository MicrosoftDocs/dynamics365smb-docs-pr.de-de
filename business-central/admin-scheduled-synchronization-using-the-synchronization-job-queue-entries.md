---
title: Synchronisieren von Business Central und Common Data Service | Microsoft Docs
description: Erfahren Sie mehr über die Synchronisierung von Daten zwischen Business Central und Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196591"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Planen einer Synchronisierung zwischen Business Central und Common Data Service
Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[d365fin](includes/cds_long_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten. Die Synchronisierungsprojekte synchronisieren Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und [!INCLUDE[d365fin](includes/cds_long_md.md)]-Datensätzen, die zuvor gekoppelt wurden. Für Datensätze, die nicht bereits gekoppelt sind, können die Synchronisierungsprojekte entsprechend der Synchronisierungsrichtung und -regeln neue Datensätze im Zielsystem erstellen und koppeln. 

Es gibt mehrere Synchronisierungsprojekte, die standardmäßig verfügbar sind. Die Jobs werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Entitäten zu vermeiden. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. CURRENCY - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag.
2. VENDOR - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag. 
3. CONTACT - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag.
4. CUSTOMER - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag.
5. SALESPEOPLE - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag.

Sie können die Stellen auf der Seite **Projektwarteschlangeneinträge** ansehen. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Standard-Synchronisations-Job-Warteschlangeneinträge  
Die folgende Tabelle beschreibt die Standard-Synchronisierungsaufträge für [!INCLUDE[d365fin](includes/cds_long_md.md)].  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|Standard-Synchronisationsfrequenz (Min.)|Standardmäßige Inaktivitäts-Ruhezeit (Min.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKT – [!INCLUDE[d365fin](includes/cds_long_md.md)]-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[d365fin](includes/cds_long_md.md)]-Kontakte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Kontakten.|Bidirektional|KONTAKT|30|720 <br>(12 Stunden)| 
|WÄHRUNG – [!INCLUDE[d365fin](includes/cds_long_md.md)]-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[d365fin](includes/cds_long_md.md)]-Transaktionswährungen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Währungen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[d365fin](includes/cds_long_md.md)]|WÄHRUNG|30|720 <br> (12 Std.)| 
|KUNDE – [!INCLUDE[d365fin](includes/cds_long_md.md)]-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren.|Bidirektional|DEBITOR|30|720<br> (12 Std.)|
|VENDOR - [!INCLUDE[d365fin](includes/cds_long_md.md)] Synchronisierungsauftrag|Synchronisiert [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konten mit [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren.|Bidirektional|VENDOR|30|720<br> (12 Std.)|
|VERKÄUFER – [!INCLUDE[d365fin](includes/cds_long_md.md)]-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkäufer mit [!INCLUDE[d365fin](includes/cds_long_md.md)]-Benutzern.|Von [!INCLUDE[d365fin](includes/cds_long_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKÄUFER|30|1440<br> (24 Std.)|

## <a name="synchronization-process"></a>Synchronisierungsvorgang  
Jeder Synchronisierungsprojektwarteschlangenposten verwendet eine bestimmte Integrationstabellenzuordnung, die angibt, welche [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[d365fin](includes/cds_long_md.md)]-Einheit synchronisiert werden sollen. Die Tabellenzuordnungen umfassen auch einige Einstellungen, die steuern, welche Datensätze in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[d365fin](includes/cds_long_md.md)]-Einheit synchronisiert werden sollen.  

Um Daten zu synchronisieren, müssen [!INCLUDE[d365fin](includes/cds_long_md.md)]-Einheitendatensätze an [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze gekoppelt werden. Beispielsweise muss ein [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitor an ein [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konto gekoppelt werden. Sie können Kopplungen manuell einrichten, bevor Sie die Synchronisierungsprojekte ausführen, oder Sie können die Kopplungen automatisch durch die Synchronisierungsprojekte erstellen lassen. Die folgende Liste zeigt, wie Daten zwischen Common Data Service und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden, wenn Sie die Synchronisierungsprojektwarteschlangenposten verwenden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md).

-   Das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** steuert, ob neue Datensätze erstellt werden, wenn Sie synchronisieren. Standardmäßig ist das Kontrollkästchen aktiviert. Dies bedeutet, dass nur gekoppelte Datensätze synchronisiert werden. In der Integrationstabellenzuordnung können Sie die Tabellenzuordnung zwischen einer [!INCLUDE[d365fin](includes/cds_long_md.md)]-Einheit und einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle ändern, sodass die Integrationssynchronisierungsaufträge neue Datensätze in der Zieldatenbank für jeden Datensatz in der Quelldatenbank erstellen, der nicht gekoppelt ist. Weitere Informationen finden Sie unter [Neue Datensätze erstellen](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Beispiel** Wenn Sie das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** deaktivieren, wenn Sie Kunden synchronisieren in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Konten in [!INCLUDE[d365fin](includes/cds_long_md.md)], wird für jeden Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein neues Konto erstellt und automatisch gekoppelt. Da darüberhinaus die Synchronisierung in diesem Fall bidirektional verläuft, wird ein neuer Debitor für jedes [!INCLUDE[d365fin](includes/cds_long_md.md)]-Konto erstellt und gekoppelt, das nicht bereits gekoppelt ist.  

    > [!NOTE]  
    > Es gibt Regeln und Filter, die bestimmen, welche Daten synchronisiert werden. Weitere Informationen finden Sie unter [Synchronisierungsregeln](admin-synchronizing-business-central-and-sales.md).

-   Wenn neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt werden, verwenden die Datensätze entweder die Vorlage, die für die Integrationstabellenzuordnung definiert ist, oder die Standardvorlage, die für den Datensatztyp verfügbar ist. Felder werden mit Daten von [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[d365fin](includes/cds_long_md.md)] ausgefüllt, je nach Synchronisierungsrichtung. Weitere Informationen finden Sie unter [Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bei nachfolgenden Synchronisierungen werden nur Datensätze aktualisiert, die nach dem letzten erfolgreichen Synchronisierungsprojekt für die Einheit geändert oder hinzugefügt wurden.  

     Neue Datensätze in [!INCLUDE[d365fin](includes/cds_long_md.md)] werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt. Wenn sich Daten in Feldern in [!INCLUDE[d365fin](includes/cds_long_md.md)] ändern, werden die Daten ins entsprechende Feld in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiert.  

-   Bei bidirektionaler Synchronisierung synchronisiert das Projekt von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[d365fin](includes/cds_long_md.md)], und anschließend von [!INCLUDE[d365fin](includes/cds_long_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Über Inaktivitätszeitlimits
Einige Aufgabenwarteschlangeneinträge, z. B. diejenigen, die die Synchronisierung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)] planen, verwenden das Feld **Inaktivitätszeitlimit** auf der Karte Aufgabenwarteschlangeneintrag, um zu verhindern, dass der Aufgabenwarteschlangeneintrag unnötig ausgeführt wird.  
<br><br>

> ![Flussdiagramm für den Fall, dass Aufgabenwarteschlangeneinträge aufgrund von Inaktivität gesperrt werden.](media/on-hold-with-inactivity-timeout.png)

Wenn der Wert in diesem Feld nicht Null ist und die Aufgabenwarteschlange während der letzten Ausführung keine Änderungen gefunden hat, sperrt [!INCLUDE[d365fin](includes/d365fin_md.md)] den Aufgabenwarteschlangeneintrag. Wenn das passiert, wird das **Status der Aufgabenwarteschlange**-Feld **Gesperrt wegen Inaktivität**, und [!INCLUDE[d365fin](includes/d365fin_md.md)] wartet auf den Zeitraum, der im Feld **Inaktivitätszeitlimit** angegeben ist, bevor der Aufgabenwarteschlangeneintrag erneut ausgeführt wird. 

Beispiel: Standardmäßig sucht die Aufgabenwarteschlange WÄHRUNG, die Währungen in [!INCLUDE[d365fin](includes/cds_long_md.md)] mit Wechselkursen in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert, alle 30 Minuten nach Änderungen bei Wechselkursen. Wenn keine Änderungen gefunden werden, sperrt [!INCLUDE[d365fin](includes/d365fin_md.md)] die Aufgabenwarteschlange WÄHRUNG für 720 Minuten (sechs Stunden). Wenn ein Wechselkurs in [!INCLUDE[d365fin](includes/d365fin_md.md)] geändert wird, während der Aufgabenwarteschlangeneintrag gesperrt ist, aktiviert [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch den Aufgabenwarteschlangeneintrag neu und startet die Aufgabenwarteschlange neu. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert automatisch Aufgabenwarteschlangeneinträge, die nur dann gesperrt werden, wenn Änderungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfolgen. Änderungen in [!INCLUDE[d365fin](includes/cds_long_md.md)] aktivieren keine Aufgabenwarteschlangeneinträge.

## <a name="to-view-the-synchronization-job-log"></a>So zeigen Sie das Synchronisierungsprojektprotokoll an:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Integrationssynchronisierungsprotokoll** ein, und wählen Sie dann den zugehörigen Link.
2.  Wenn Fehler bei einem Synchronisierungsprojekt aufgetreten sind, erscheint die Anzahl der Fehler in der Spalte **Fehler**. Um die Fehler für das Projekt anzuzeigen, wählen Sie die Zahl aus.  

    > [!TIP]  
    > Sie können alle Synchronisierungsprojektfehler anzeigen, indem Sie das Protokoll mit den Synchronisierungsprojektfehlern direkt öffnen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>So zeigen Sie das Protokoll der Synchronisierungsprojekte über die Tabellenzuordnungen an:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.
2.  Wählen Sie auf der Seite **Integrationstabellenzuordnungen** einen wählen Sie einen Posten aus und wählen Sie dann **Integrationssynchronisierungs-Auftragsprotokoll** aus.  

## <a name="to-view-the-synchronization-error-log"></a>So zeigen Sie das Synchronisierungsfehlerprotokoll an:  
* Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Integrationssynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link.

## <a name="see-also"></a>Siehe auch  
[Synchronisieren von Daten in Business Central und [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synchronisieren Sie Tabellenzuordnungen manuell](admin-manual-synchronization-of-table-mappings.md)  
[Planen einer Synchronisierung zwischen Business Central und [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Über das Integrieren von Dynamics 365 Business Central mit [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
