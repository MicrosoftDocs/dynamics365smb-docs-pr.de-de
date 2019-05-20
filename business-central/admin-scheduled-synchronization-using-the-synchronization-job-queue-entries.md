---
title: Synchronisieren von Business Central und Dynamics 365 for Sales | Microsoft Docs
description: Erfahren Sie mehr über die Synchronisierung von Daten zwischen Business Central und Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: b3fb3d2680cd85da8b2def7e82fbf62c0046fcc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247421"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Planen einer Synchronisierung zwischen Business Central und Dynamics 365 for Sales
Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten. Die Synchronisierungsprojekte synchronisieren Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätzen, die zuvor gekoppelt wurden. Für Datensätze, die nicht bereits gekoppelt sind, können die Synchronisierungsprojekte entsprechend der Synchronisierungsrichtung und -regeln neue Datensätze im Zielsystem erstellen und koppeln. Es gibt mehrere Synchronisierungsprojekte, die standardmäßig verfügbar sind. Sie können sich diese auf der Seite **Projektwarteschlangeneinträge** ansehen. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synchronisierungsvorgang  
Jeder Synchronisierungsprojektwarteschlangenposten verwendet eine bestimmte Integrationstabellenzuordnung, die angibt, welche [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisiert werden sollen. Die Tabellenzuordnungen umfassen auch einige Einstellungen, die steuern, welche Datensätze in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle und [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisiert werden sollen.  

Um Daten zu synchronisieren, müssen [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitendatensätze an [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze gekoppelt werden. Beispielsweise muss ein [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitor an ein [!INCLUDE[crm_md](includes/crm_md.md)]-Konto gekoppelt werden. Sie können Kopplungen manuell einrichten, bevor Sie die Synchronisierungsprojekte ausführen, oder Sie können die Kopplungen automatisch durch die Synchronisierungsprojekte erstellen lassen. Die folgende Liste zeigt, wie Daten zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden, wenn Sie die Synchronisierungsprojektwarteschlangenposten verwenden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Standardmäßig werden nur Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert, die an Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt sind. Sie können die Tabellenzuordnung zwischen einer [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit und einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle ändern, sodass die Integrationssynchronisierungsprojekte neue Datensätze in der Zieldatenbank für jeden Datensatz in der Quelldatenbank erstellen, der nicht gekoppelt ist. Die neuen Datensätze werden ebenfalls mit den entsprechenden Datensätzen in der Quelle gekoppelt. Wenn Sie beispielsweise Debitoren mit [!INCLUDE[crm_md](includes/crm_md.md)]-Konten synchronisieren, wird ein neuer Kontodatensatz für jeden Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt. Die neuen Konten werden automatisch an Debitoren in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekoppelt. Da die Synchronisierung in diesem Fall bidirektional verläuft, wird ein neuer Debitor für jedes [!INCLUDE[crm_md](includes/crm_md.md)]-Konto erstellt und gekoppelt, das nicht bereits gekoppelt ist.  

    > [!NOTE]  
    >  Es gibt Regeln und Filter, die bestimmen, welche Daten synchronisiert werden. Weitere Informationen finden Sie unter [Synchronisierungsregeln](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Wenn neue Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt werden, verwenden die Datensätze entweder die Vorlage, die für die Integrationstabellenzuordnung definiert ist, oder die Standardvorlage, die für den Datensatztyp verfügbar ist. Felder werden mit Daten von [!INCLUDE[d365fin](includes/d365fin_md.md)] oder [!INCLUDE[crm_md](includes/crm_md.md)] ausgefüllt, je nach Synchronisierungsrichtung. Weitere Informationen finden Sie unter [Vorgehensweise: Tabellenzuordnungen für die Synchronisierung ändern](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bei nachfolgenden Synchronisierungen werden nur Datensätze aktualisiert, die nach dem letzten erfolgreichen Synchronisierungsprojekt für die Einheit geändert oder hinzugefügt wurden.  

     Neue Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt. Wenn sich Daten in Feldern in [!INCLUDE[crm_md](includes/crm_md.md)] ändern, werden die Daten ins entsprechende Feld in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiert.  

-   Bei bidirektionaler Synchronisierung synchronisiert das Projekt von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)], und anschließend von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Standardmäßige Synchronisierungsprojektwarteschlangenposten  
In der folgenden Tabelle werden die standardmäßigen Synchronisierungsprojekte beschrieben.  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|KONTAKT – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Kontakte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Kontakten.|Bidirektional|KONTAKT|  
|WÄHRUNG – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Transaktionswährungen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Währungen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|WÄHRUNG|  
|KUNDE – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren.|Bidirektional|DEBITOR|  
|DEBITORENPREISGRUPPEN-PREIS – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Verkaufspreislisten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorenpreisgruppen.| |DEBITORENPREISGRUPPEN – VERKAUFSPREISLISTEN|
|ARTIKEL – PRODUKT – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Artikeln.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL/PRODUKT|
|GEBUCHTE VERKAUFSRECHNUNGEN – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Rechnungen mit gebuchten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufsrechnungen.|Von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)]|RECHNUNGEN – GEBUCHTE VERKAUFSRECHNUNGEN|
|RESSOURCE – PRODUKT – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Ressourcen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE – PRODUKT|  
|VERKÄUFER – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkäufer mit [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzern.|Von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKÄUFER|
|VERKAUFSPREIS – PRODUKTPREIS – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produktpreise mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufspreisen.||PRODUKTPREIS – VERKAUFSPREIS|
|MASSEINHEIT – Dynamics 365 for Sales-Synchronisierungsprojekt|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitsgruppen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Maßeinheiten.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|MASSEINHEIT|  
|Debitorenstatistik – Dynamics 365 for Sales-Synchronisierungsprojekt|Aktualisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit den neuesten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorendaten. In [!INCLUDE[crm_md](includes/crm_md.md)] erscheinen diese Informationen im **Business Central-Kontostatistik**-Schnellansichtsformular von Konten, die mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren gekoppelt werden.<br /><br /> Diese Daten können auch manuell für jeden Debitorendatensatz aktualisiert werden. Weitere Informationen finden Sie unter [Vorgehensweise: Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Hinweis:** Dieser Projektwarteschlangeneintrag ist nur relevant, wenn die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist. Weitere Informationen finden Sie unter [Informationen über die Business Central-Integrationslösung](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Nicht anwendbar.|Nicht anwendbar.|   

## <a name="to-view-the-synchronization-job-log"></a>So zeigen Sie das Synchronisierungsprojektprotokoll an:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion "Wie möchten Sie weiter verfahren?" geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationssynchronisierungsprotokoll** ein und wählen Sie dann den zugehörigen Link aus.
2.  Wenn Fehler bei einem Synchronisierungsprojekt aufgetreten sind, erscheint die Anzahl der Fehler in der Spalte **Fehler**. Um die Fehler für das Projekt anzuzeigen, wählen Sie die Zahl aus.  

    > [!TIP]  
    >  Sie können alle Synchronisierungsprojektfehler anzeigen, indem Sie das Protokoll mit den Synchronisierungsprojektfehlern direkt öffnen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>So zeigen Sie das Protokoll der Synchronisierungsprojekte über die Tabellenzuordnungen an:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationstabellenzuordnungen** ein, und wählen Sie dann den zugehörigen Link aus.
2.  Wählen Sie auf der Seite **Integrationstabellenzuordnungen** einen wählen Sie einen Posten aus und wählen Sie dann **Integrationssynchronisierungs-Auftragsprotokoll** aus.  

## <a name="to-view-the-synchronization-error-log"></a>So zeigen Sie das Synchronisierungsfehlerprotokoll an:  
* Wählen Sie das Symbol ![Glühlampe, mit der die Funktion "Wie möchten Sie weiter verfahren?" geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Integrationssynchronisierungsfehler** ein und wählen Sie dann den zugehörigen Link aus.

## <a name="see-also"></a>Siehe auch  
[Synchronisieren von Daten in Business Central und Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Synchronisieren Sie Tabellenzuordnungen manuell](admin-manual-synchronization-of-table-mappings.md)  
[Planen einer Synchronisierung zwischen Business Central und Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Über das Integrieren von Dynamics 365 Business Central mit Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



