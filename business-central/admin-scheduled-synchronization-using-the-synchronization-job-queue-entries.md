---
title: Business Central und Dataverse synchronisieren
description: Erfahren Sie mehr über die Synchronisierung von Daten zwischen Business Central und Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.service: dynamics-365-business-central
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Planen einer Synchronisierung zwischen Business Central und Dataverse

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten. Die Synchronisierungsprojekte synchronisieren Daten in [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätzen und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Datensätzen, die gekoppelt wurden. Für Datensätze, die nicht bereits gekoppelt sind, können die Synchronisierungsprojekte entsprechend der Synchronisierungsrichtung und -regeln neue Datensätze im Zielsystem erstellen und koppeln.

Es gibt mehrere Synchronisierungsprojekte, die standardmäßig verfügbar sind. Die Jobs werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Tabellen zu vermeiden. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

1. CURRENCY - Common Data Service Synchronisierungsauftrag.
2. VENDOR - Common Data Service Synchronisierungsauftrag.
3. CONTACT - Common Data Service Synchronisierungsauftrag.
4. CUSTOMER - Common Data Service Synchronisierungsauftrag.
5. SALESPEOPLE - Common Data Service Synchronisierungsauftrag.

Sie können die Stellen auf der Seite **Projektwarteschlangeneinträge** ansehen. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Standard-Synchronisations-Projektwarteschlangeneinträge

Die folgende Tabelle beschreibt die Standard-Synchronisierungsaufträge für [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Aufgabenwarteschlangenposten | Beschreibung | Richtung | Integrationstabellenzuordnung | Standard-Synchronisationsfrequenz (Min.) | Standardmäßige Inaktivitäts-Ruhezeit (Min.) |
|--|--|--|--|--|--|--|
| KONTAKT – Common Data Service-Synchronisierungsprojekt | Synchronisiert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Kontakte mit [!INCLUDE[prod_short](includes/prod_short.md)]-Kontakten. | Bidirektional | KONTAKT | 30 | 720 <br>(12 Stunden) |
| WÄHRUNG – Common Data Service-Synchronisierungsprojekt | Synchronisiert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Transaktionswährungen mit [!INCLUDE[prod_short](includes/prod_short.md)]-Währungen. | Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | WÄHRUNG | 30 | 720 <br> (12 Std.) |
| KUNDE – Common Data Service-Synchronisierungsprojekt | Synchronisiert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Konten mit [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren. | Bidirektional | DEBITOR | 30 | 720<br> (12 Std.) |
| VENDOR - Common Data Service Synchronisierungsauftrag | Synchronisiert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Konten mit [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren. | Bidirektional | VENDOR | 30 | 720<br> (12 Std.) |
| VERKÄUFER – Common Data Service-Synchronisierungsprojekt | Synchronisiert [!INCLUDE[prod_short](includes/prod_short.md)]-Verkäufer mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Benutzern. | Von [!INCLUDE[cds_long_md](includes/cds_long_md.md)] nach [!INCLUDE[prod_short](includes/prod_short.md)] | VERKÄUFER | 30 | 1440<br> (24 Std.) |

## <a name="synchronization-process"></a>Synchronisierungsprozess

Jeder Synchronisierungsprojektwarteschlangenposten verwendet eine bestimmte Integrationstabellenzuordnung, die angibt, welche [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] Tabelle synchronisiert werden sollen. Die Tabellenzuordnungen umfassen auch einige Einstellungen, die steuern, welche Datensätze in der [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Tabelle synchronisiert werden sollen.  

Um Daten zu synchronisieren, müssen [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Tabellenatensätze an [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze gekoppelt werden. Beispielsweise muss ein [!INCLUDE[prod_short](includes/prod_short.md)]-Debitor an ein [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Konto gekoppelt werden. Sie können Kopplungen manuell einrichten, bevor Sie die Synchronisierungsprojekte ausführen, oder Sie können die Kopplungen automatisch durch die Synchronisierungsprojekte erstellen lassen. Die folgende Liste zeigt, wie Daten zwischen [!INCLUDE[cds_long_md](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert werden, wenn Sie die Synchronisierungsprojektwarteschlangenposten verwenden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md).

- Das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** steuert, ob neue Datensätze erstellt werden, wenn Sie synchronisieren. Standardmäßig ist das Kontrollkästchen aktiviert. Dies bedeutet, dass nur gekoppelte Datensätze synchronisiert werden. In der Integrationstabellenzuordnung können Sie die Tabellenzuordnung zwischen einer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Tabelle und einer [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle ändern, sodass die Integrationssynchronisierungsaufträge neue Datensätze in der Zieldatenbank für jede Zeile in der Quelldatenbank erstellen, der nicht gekoppelt ist. Weitere Informationen finden Sie unter [Neue Datensätze erstellen](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Beispiel** Wenn Sie das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** deaktivieren, wenn Sie Kunden synchronisieren in [!INCLUDE[prod_short](includes/prod_short.md)] mit Konten in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], wird für jeden Debitor in [!INCLUDE[prod_short](includes/prod_short.md)] ein neues Konto erstellt und automatisch gekoppelt. Da darüberhinaus die Synchronisierung in diesem Fall bidirektional verläuft, wird ein neuer Debitor für jedes [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Konto erstellt und gekoppelt, das nicht bereits gekoppelt ist.  

    > [!NOTE]  
    > Es gibt Regeln und Filter, die bestimmen, welche Daten synchronisiert werden. Weitere Informationen finden Sie unter [Synchronisierungsregeln](admin-synchronizing-business-central-and-sales.md).

- Wenn neue Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt werden, verwenden die Datensätze entweder die Vorlage, die für die Integrationstabellenzuordnung definiert ist, oder die Standardvorlage, die für den Zeilentyp verfügbar ist. Felder werden mit Daten von [!INCLUDE[prod_short](includes/prod_short.md)] oder [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ausgefüllt, je nach Synchronisierungsrichtung. Weitere Informationen finden Sie unter [Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Bei nachfolgenden Synchronisierungen werden nur Datensätze aktualisiert, die nach dem letzten erfolgreichen Synchronisierungsprojekt für die Tabelle geändert oder hinzugefügt wurden.  

     Neue Datensätze in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] werden in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Wenn sich Daten in Feldern in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ändern, werden die Daten ins entsprechende Feld in [!INCLUDE[prod_short](includes/prod_short.md)] kopiert.  

- Bei bidirektionaler Synchronisierung synchronisiert das Projekt von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[cds_long_md](includes/cds_long_md.md)], und anschließend von [!INCLUDE[cds_long_md](includes/cds_long_md.md)] nach [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Über Inaktivitätszeitüberschreitungen

Einige Aufgabenwarteschlangeneinträge, z. B. diejenigen, die die Synchronisierung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] planen, verwenden das Feld **Inaktivitätszeitlimit** auf der Seite **Aufgabenwarteschlangeneintrag**, um zu verhindern, dass der Aufgabenwarteschlangeneintrag unnötig ausgeführt wird.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Flussdiagramm für den Fall, dass Aufgabenwarteschlangeneinträge aufgrund von Inaktivität gesperrt werden.":::

Wenn der Wert in diesem Feld nicht Null ist und die Aufgabenwarteschlange während der letzten Ausführung keine Änderungen gefunden hat, sperrt [!INCLUDE[prod_short](includes/prod_short.md)] den Aufgabenwarteschlangeneintrag. Wenn das passiert, wird das **Status der Aufgabenwarteschlange**-Feld **Gesperrt wegen Inaktivität**, und [!INCLUDE[prod_short](includes/prod_short.md)] wartet auf den Zeitraum, der im Feld **Inaktivitätszeitlimit** angegeben ist, bevor der Aufgabenwarteschlangeneintrag erneut ausgeführt wird.  

Beispiel: Standardmäßig sucht die Aufgabenwarteschlange WÄHRUNG, die Währungen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] mit Wechselkursen in [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert, alle 30 Minuten nach Änderungen bei Wechselkursen. Wenn keine Änderungen gefunden werden, sperrt [!INCLUDE[prod_short](includes/prod_short.md)] die Aufgabenwarteschlange WÄHRUNG für 720 Minuten (zwölf Stunden). Wenn ein Wechselkurs in [!INCLUDE[prod_short](includes/prod_short.md)] geändert wird, während der Aufgabenwarteschlangeneintrag gesperrt ist, aktiviert [!INCLUDE[prod_short](includes/prod_short.md)] automatisch den Aufgabenwarteschlangeneintrag neu und startet die Aufgabenwarteschlange neu. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert automatisch Aufgabenwarteschlangeneinträge, die nur dann gesperrt werden, wenn Änderungen in [!INCLUDE[prod_short](includes/prod_short.md)] erfolgen. Änderungen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] aktivieren keine Aufgabenwarteschlangeneinträge.

## <a name="to-view-the-synchronization-job-log"></a>So zeigen Sie das Synchronisierungsprojektprotokoll an:

1. Wählen Sie das :::image type="icon" source="media/ui-search/search_small.png" border="false":::-Symbol, geben Sie **Integrationssynchronisationsprotokoll** ein, und wählen Sie dann den entsprechenden Link.
2. Wenn Fehler bei einem Synchronisierungsprojekt aufgetreten sind, erscheint die Anzahl der Fehler in der Spalte **Fehler**. Um die Fehler für das Projekt anzuzeigen, wählen Sie die Zahl aus.  

    > [!TIP]  
    > Sie können alle Synchronisierungsprojektfehler anzeigen, indem Sie das Protokoll mit den Synchronisierungsprojektfehlern direkt öffnen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>So zeigen Sie das Protokoll der Synchronisierungsprojekte über die Tabellenzuordnungen an:

1. Wählen Sie das :::image type="icon" source="media/ui-search/search_small.png" border="false":::-Symbol, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Integrationstabellenzuordnungen** einen wählen Sie einen Posten aus und wählen Sie dann **Integrationssynchronisierungs-Auftragsprotokoll** aus.  

## <a name="to-view-the-synchronization-error-log"></a>So zeigen Sie das Synchronisierungsfehlerprotokoll an:

- Wählen Sie das :::image type="icon" source="media/ui-search/search_small.png" border="false":::-Symbol, geben Sie **Integrationssynchronisationsfehler** ein, und wählen Sie dann den entsprechenden Link.

## <a name="see-also"></a>Siehe auch

[Synchronisieren von Daten in Business Central und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synchronisieren Sie Tabellenzuordnungen manuell](admin-manual-synchronization-of-table-mappings.md)  
[Planen einer Synchronisierung zwischen Business Central und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Über das Integrieren von Dynamics 365 Business Central mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
