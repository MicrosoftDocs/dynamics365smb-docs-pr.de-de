---
title: Synchronisieren von Business Central und Dynamics 365 Sales | Microsoft Docs
description: Erfahren Sie mehr über die Synchronisierung von Daten zwischen Business Central und Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879082"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Planen einer Synchronisierung zwischen Business Central und Dynamics 365 Sales
Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten. Die Synchronisierungsprojekte synchronisieren Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätzen, die zuvor gekoppelt wurden. Für Datensätze, die nicht bereits gekoppelt sind, können die Synchronisierungsprojekte entsprechend der Synchronisierungsrichtung und -regeln neue Datensätze im Zielsystem erstellen und koppeln. Es gibt mehrere Synchronisierungsprojekte, die standardmäßig verfügbar sind. Sie können sich diese auf der Seite **Projektwarteschlangeneinträge** ansehen. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Synchronisierungsvorgang  
Jeder Synchronisierungsprojektwarteschlangenposten verwendet eine bestimmte Integrationstabellenzuordnung, die angibt, welche [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisiert werden sollen. Die Tabellenzuordnungen umfassen auch einige Einstellungen, die steuern, welche Datensätze in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisiert werden sollen.  

Um Daten zu synchronisieren, müssen [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitendatensätze an [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze gekoppelt werden. Beispielsweise muss ein [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitor an ein [!INCLUDE[crm_md](includes/crm_md.md)]-Konto gekoppelt werden. Sie können Kopplungen manuell einrichten, bevor Sie die Synchronisierungsprojekte ausführen, oder Sie können die Kopplungen automatisch durch die Synchronisierungsprojekte erstellen lassen. Die folgende Liste zeigt, wie Daten zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden, wenn Sie die Synchronisierungsprojektwarteschlangenposten verwenden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md).

-   Das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** steuert, ob neue Datensätze erstellt werden, wenn Sie synchronisieren. Standardmäßig ist das Kontrollkästchen aktiviert. Dies bedeutet, dass nur gekoppelte Datensätze synchronisiert werden. In der Integrationstabellenzuordnung können Sie die Tabellenzuordnung zwischen einer [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit und einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle ändern, sodass die Integrationssynchronisierungsaufträge neue Datensätze in der Zieldatenbank für jeden Datensatz in der Quelldatenbank erstellen, der nicht gekoppelt ist. Weitere Informationen finden Sie unter [Neue Datensätze erstellen](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Beispiel** Wenn Sie das Kontrollkästchen **Nur gekoppelte Datensätze synchronisieren** deaktivieren, wenn Sie Kunden synchronisieren in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Konten in [!INCLUDE[crm_md](includes/crm_md.md)], wird für jeden Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein neues Konto erstellt und automatisch gekoppelt. Da darüberhinaus die Synchronisierung in diesem Fall bidirektional verläuft, wird ein neuer Debitor für jedes [!INCLUDE[crm_md](includes/crm_md.md)]-Konto erstellt und gekoppelt, das nicht bereits gekoppelt ist.  

    > [!NOTE]  
    > Es gibt Regeln und Filter, die bestimmen, welche Daten synchronisiert werden. Weitere Informationen finden Sie unter [Synchronisierungsregeln](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Wenn neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt werden, verwenden die Datensätze entweder die Vorlage, die für die Integrationstabellenzuordnung definiert ist, oder die Standardvorlage, die für den Datensatztyp verfügbar ist. Felder werden mit Daten von [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[crm_md](includes/crm_md.md)] ausgefüllt, je nach Synchronisierungsrichtung. Weitere Informationen finden Sie unter [Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bei nachfolgenden Synchronisierungen werden nur Datensätze aktualisiert, die nach dem letzten erfolgreichen Synchronisierungsprojekt für die Einheit geändert oder hinzugefügt wurden.  

     Neue Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt. Wenn sich Daten in Feldern in [!INCLUDE[crm_md](includes/crm_md.md)] ändern, werden die Daten ins entsprechende Feld in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiert.  

-   Bei bidirektionaler Synchronisierung synchronisiert das Projekt von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)], und anschließend von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Standardmäßige Synchronisierungsprojektwarteschlangenposten  
In der folgenden Tabelle werden die standardmäßigen Synchronisierungsprojekte beschrieben.  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|Standard-Synchronisationsfrequenz (Minuten)|Standard-Inaktivitätsruhezustand (Minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Kontakte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Kontakten.|Bidirektional|KONTAKT|30|720 <br>(12 Stunden)| 
|WÄHRUNG - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Transaktionswährungen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Währungen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|WÄHRUNG|30|720 <br> (12 Std.)| 
|DEBITOR - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren.|Bidirektional|DEBITOR|30|720<br> (12 Std.)|
|CUSTPRCGRP-PREIS - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Verkaufspreislisten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorenpreisgruppen.| |DEBITORENPREISGRUPPEN – VERKAUFSPREISLISTEN|30|1440<br> (24 Std.)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Artikeln.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL/PRODUKT|30|1440<br> (24 Std.)|
|POSTEDSALESINV-INV - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Rechnungen mit gebuchten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufsrechnungen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RECHNUNGEN – GEBUCHTE VERKAUFSRECHNUNGEN|30|1440<br> (24 Std.)|
|RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Ressourcen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE – PRODUKT|30|720<br> (12 Std.)|  
|VERKäUFER - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkäufer mit [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzern.|Von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKÄUFER|30|1440<br> (24 Std.)|
|SALESPRC-PRODUCTPRICE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produktpreise mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufspreisen.||PRODUKTPREIS – VERKAUFSPREIS|30|1440<br> (24 Std.)|
|UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitsgruppen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Maßeinheiten.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|MASSEINHEIT|30|720<br> (12 Std.)|  
|Debitorenstatistik - Dynamics 365 Sales Synchronisierungsauftrag|Aktualisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit den neuesten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorendaten. In [!INCLUDE[crm_md](includes/crm_md.md)] erscheinen diese Informationen im **Business Central-Kontostatistik**-Schnellansichtsformular von Konten, die mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren gekoppelt werden.<br /><br /> Diese Daten können auch manuell für jeden Debitorendatensatz aktualisiert werden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Hinweis:** Dieser Projektwarteschlangeneintrag ist nur relevant, wenn die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist. Weitere Informationen finden Sie unter [Informationen über die Business Central-Integrationslösung](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Nicht anwendbar|Nicht anwendbar|30|Nicht anwendbar|   

## <a name="about-inactivity-timeouts"></a>Über Inaktivitätszeitlimits
Einige Aufgabenwarteschlangeneinträge, z. B. diejenigen, die die Synchronisierung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] planen, verwenden das Feld **Inaktivitätszeitlimit** auf der Karte Aufgabenwarteschlangeneintrag, um zu verhindern, dass der Aufgabenwarteschlangeneintrag unnötig ausgeführt wird.  
<br><br>

> ![Flussdiagramm für den Fall, dass Aufgabenwarteschlangeneinträge aufgrund von Inaktivität gesperrt werden.](media/on-hold-with-inactivity-timeout.png)

Wenn der Wert in diesem Feld nicht Null ist und die Aufgabenwarteschlange während der letzten Ausführung keine Änderungen gefunden hat, sperrt [!INCLUDE[d365fin](includes/d365fin_md.md)] den Aufgabenwarteschlangeneintrag. Wenn das passiert, wird das **Status der Aufgabenwarteschlange**-Feld **Gesperrt wegen Inaktivität**, und [!INCLUDE[d365fin](includes/d365fin_md.md)] wartet auf den Zeitraum, der im Feld **Inaktivitätszeitlimit** angegeben ist, bevor der Aufgabenwarteschlangeneintrag erneut ausgeführt wird. 

Beispiel: Standardmäßig sucht die Aufgabenwarteschlange WÄHRUNG, die Währungen in [!INCLUDE[crm_md](includes/crm_md.md)] mit Wechselkursen in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert, alle 30 Minuten nach Änderungen bei Wechselkursen. Wenn keine Änderungen gefunden werden, sperrt [!INCLUDE[d365fin](includes/d365fin_md.md)] die Aufgabenwarteschlange WÄHRUNG für 720 Minuten (sechs Stunden). Wenn ein Wechselkurs in [!INCLUDE[d365fin](includes/d365fin_md.md)] geändert wird, während der Aufgabenwarteschlangeneintrag gesperrt ist, aktiviert [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch den Aufgabenwarteschlangeneintrag neu und startet die Aufgabenwarteschlange neu. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert automatisch Aufgabenwarteschlangeneinträge, die nur dann gesperrt werden, wenn Änderungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfolgen. Änderungen in [!INCLUDE[crm_md](includes/crm_md.md)] aktivieren keine Aufgabenwarteschlangeneinträge.

## <a name="to-view-the-synchronization-job-log"></a>So zeigen Sie das Synchronisierungsprojektprotokoll an:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationssynchronisierungsprotokoll** ein, und wählen Sie dann den zugehörigen Link.
2.  Wenn Fehler bei einem Synchronisierungsprojekt aufgetreten sind, erscheint die Anzahl der Fehler in der Spalte **Fehler**. Um die Fehler für das Projekt anzuzeigen, wählen Sie die Zahl aus.  

    > [!TIP]  
    > Sie können alle Synchronisierungsprojektfehler anzeigen, indem Sie das Protokoll mit den Synchronisierungsprojektfehlern direkt öffnen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>So zeigen Sie das Protokoll der Synchronisierungsprojekte über die Tabellenzuordnungen an:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link.
2.  Wählen Sie auf der Seite **Integrationstabellenzuordnungen** einen wählen Sie einen Posten aus und wählen Sie dann **Integrationssynchronisierungs-Auftragsprotokoll** aus.  

## <a name="to-view-the-synchronization-error-log"></a>So zeigen Sie das Synchronisierungsfehlerprotokoll an:  
* Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Integrationssynchronisierungsfehler** ein, und wählen Sie dann den zugehörigen Link.

## <a name="see-also"></a>Siehe auch  
[Synchronisieren von Daten in Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synchronisieren Sie Tabellenzuordnungen manuell](admin-manual-synchronization-of-table-mappings.md)  
[Planen einer Synchronisierung zwischen Business Central und Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Über Integration von Dynamics 365 Business Central mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
