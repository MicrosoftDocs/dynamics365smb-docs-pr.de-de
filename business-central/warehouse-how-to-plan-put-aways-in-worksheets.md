---
title: So planen Sie Einlagerungen in Arbeitsblättern
description: Richten Sie Ihr Lager so ein, dass Ihnen Belegzeilen im Einlagerungs-Arbeitsblatt zur Verfügung stehen, wenn Sie Einlagerungsanweisungen für Belege planen wollen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 109ebfef1650c365cb383aac56cf51ab9ee8231b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518547"
---
# <a name="plan-put-aways-in-worksheets"></a>Planen von Einlagerungen in Arbeitsblättern
Wenn für Ihren Lagerort die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist und Sie Einlagerungsanweisungen für mehrere Wareneingänge planen möchten, anstatt die Mitarbeiter Anweisungen ausführen zu lassen, die die Anwendung für einzelne gebuchte Wareneingänge erzeugt – können Sie das Einlagerungsarbeitsblatt nutzen.  

Um Ihr Lager so einzurichten, dass die Wareneingangszeilen im Einlagerungsarbeitsblatt verfügbar sind, sobald sie gebucht wurden, wählen das Feld **Einlagerungsarbeitsblatt verwenden** im Inforegister **Lager** der Lagerortkarte des jeweiligen Lagers. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

Wenn Sie dieses Feld nicht wählen, erzeugt die Anwendung automatisch die Einlagerungsanweisungen für Wareneingänge, wenn diese gebucht werden.  

> [!NOTE]  
>  Unabhängig vom Status des Feldes **Einlagerungsarbeitsblatt verwenden** auf der Lagerortkarte können Sie immer Einlagerungsanweisungszeilen, d. h. gebuchte Wareneingangszeilen, in das Einlagerungsarbeitsblatt holen, indem Sie Folgendes tun:  
>   
>  1.  Drücken Sie auf der Seite **Einlagerung** die Tastenkombination Strg+D, um die gesamte Einlagerungsanweisung zu löschen oder wählen Sie die Zeilen, die Sie im Arbeitsblatt bearbeiten möchten, und löschen Sie sie.  
> 2.  Setzen Sie dieses Vorgehen in so vielen Einlagerungen fort, wie Sie möchten, bis Sie die Zeilen gelöscht haben, die Sie im Arbeitsblatt bearbeiten möchten. Wählen Sie jetzt **Einlagerungsarbeitsblätter** und setzen Sie die Planung fort.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>So planen Sie Anweisungen im Einlagerungsarbeitsblatt:  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einlagerungsarbeitsblatt** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die **Logistikbeleg holen** Aktion aus. Die Seite **Einlagerungsauswahl** wird geöffnet.  

    Sie sehen alle gebuchten Wareneingänge und registrierten internen Einlagerungen, die zur Einlagerungsfunktion weitergeleitet wurden, einschließlich derer, für die bereits Einlagerungsanweisungen erstellt wurden. Belege mit Einlagerungszeilen, die bereits vollständig eingelagert und registriert wurden, werden in dieser Übersicht nicht angezeigt.  

3. Wählen Sie die Belege, die Sie im Arbeitsblatt bearbeiten möchten. Sie können gleichzeitig an Zeilen aus verschiedenen Belegen arbeiten.  

    > [!NOTE]  
    >  Sollten Sie versuchen, einen Beleg auszuwählen (Wareneingang oder interne Einlagerung), für den Sie bereits Anweisungen für alle Zeilen erzeugt haben, werden Sie von der Anwendung darüber informiert, dass es keine Mengen zu bewegen gibt.  

4. Füllen Sie das Feld **Sortiermethode** aus, um die Zeilen nach Wunsch zu sortieren.  

    > [!NOTE]  
    >  Die Art, auf die die Zeilen im Arbeitsblatt sortiert sind, wird nicht automatisch an die Einlagerungsanweisungen übergeben, es bestehen aber dieselben Sortiermöglichkeiten neben der Lagerplatzpriorität. Es gibt jedoch dieselben Sortiermöglichkeiten – und noch eine weitere, Lagerplatzpriorität – für die Einlagerungsanweisungen. Die Zeilenreihenfolge, die Sie im Arbeitsblatt planen, kann daher leicht wiederhergestellt werden, wenn Sie die Einlagerungsanweisungen erstellen oder durch Sortierung in den Einlagerungsanweisungen.  

5.  Füllen Sie das Feld **Bewegungsmenge** aus. Wählen Sie die **Bewegungsmenge autom. ausfüllen** Aktion aus, oder füllen Sie die Felder manuell aus.  
6.  Falls notwendig, bearbeiten Sie die Zeilen manuell. Sie können z. B. Zeilen löschen, wenn einige Artikel in einen Lagerplatz weit entfernt von den Lagerplätzen der anderen Artikel eingelagert werden müssen.  

    > [!NOTE]  
    >  Gelöschte Zeilen werden nur aus diesem Arbeitsblatt gelöscht, nicht aus der Einlagerungsauswahlliste.  

7.  Wählen Sie die Aktion **Einlagerung erstellen** aus. Auf der Seite **Beleg erstellen**, das sich jetzt öffnet, können Sie weitere Informationen zu der Einlagerung hinzufügen, die Sie erstellen, wie folgt:  

    -   Sie können die Einlagerung einem bestimmten Mitarbeiter zuordnen.  
    -   Sie können die Einlagerungsanweisungszeilen so sortieren, wie Sie es im Arbeitsblatt getan haben oder nach Lagerplatzpriorität. Wenn Sie nach der Lagerplatzpriorität sortieren, erscheinen zuerst die Zeilen der Art "Entnahme", da die meisten Wareneingangslagerplätze eine Lagerplatzpriorität 0 haben, und als Letztes erscheinen die Zeilen der Art "Einlagerung", beginnend mit den Lagerplätzen mit der niedrigsten Lagerplatzpriorität. Wenn Sie Ihr Lager so strukturiert haben, dass sich Lagerplätze von ähnlicher Lagerplatzpriorität nebeneinander befinden, verkürzt eine auf diese Art durchgeführte Sortierung die Wege, die die Lagermitarbeiter zurücklegen müssen.  
    -   Sie können wählen, dass die Zwischenzeilen nicht angezeigt werden sollen, die die Anwendung erzeugt, wenn sie eine größere Einheit in kleinere Einheiten aufbricht, indem Sie das Feld **Gebindeanbruchsfilter festlegen** wählen. Weitere Informationen finden Sie unter [Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Sie können wählen, dass nicht automatisch das Feld **Bewegungsmenge** in den Einlagerungsanweisungen ausgefüllt wird.  
    -   Sie können sich entscheiden, den Beleg sofort zu drucken.  

8.  Wählen Sie die Schaltfläche **OK** und die Anwendung erzeugt die Einlagerung entsprechend Ihren Anforderungen.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]