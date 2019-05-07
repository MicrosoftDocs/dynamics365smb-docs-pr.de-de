---
title: 'Vorgehensweise: Planen von Einlagerungen in Vorschlägen | Microsoft Docs'
description: Wenn für Ihren Lagerort die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist und Sie Einlagerungsanweisungen für mehrere Wareneingänge planen möchten – anstatt die Mitarbeiter Anweisungen ausführen zu lassen, die die Anwendung für einzelne gebuchte Wareneingänge erzeugt – können Sie den Einlagerungsvorschlag nutzen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3bf24a32ba4a411ada744092d594b874c0154588
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930801"
---
# <a name="plan-put-aways-in-worksheets"></a>Planen von Einlagerungen in Arbeitsblättern
Wenn für Ihren Lagerort die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist und Sie Einlagerungsanweisungen für mehrere Wareneingänge planen möchten – anstatt die Mitarbeiter Anweisungen ausführen zu lassen, die die Anwendung für einzelne gebuchte Wareneingänge erzeugt – können Sie den Einlagerungsvorschlag nutzen.  

Um Ihr Lager so einzurichten, dass die Wareneingangszeilen im Einlagerungsvorschlag verfügbar sind, sobald sie gebucht wurden, wählen das Feld **Einlagerungsvorschl. verwenden** im Inforegister **Lager** der Lagerortkarte des jeweiligen Lagers. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

Wenn Sie dieses Feld nicht wählen, erzeugt die Anwendung automatisch Einlagerungsanweisungen für Wareneingänge, wenn diese gebucht werden.  

> [!NOTE]  
>  Unabhängig vom Status des Feldes **Einlagerungsvorschl. verwenden** auf der Lagerortkarte können Sie immer Einlagerungsanweisungszeilen, d. h. gebuchte Wareneingangszeilen, in den Einlagerungsvorschlag holen, indem Sie Folgendes tun:  
>   
>  1.  Drücken Sie auf der Seite **Einlagerung** die Tastenkombination Strg+D, um die gesamte Einlagerungsanweisung zu löschen oder wählen Sie die Zeilen, die Sie im Vorschlag bearbeiten möchten, und löschen Sie sie.  
> 2.  Setzen Sie dieses Vorgehen in so vielen Einlagerungen fort, wie Sie möchten, bis Sie die Zeilen gelöscht haben, die Sie im Vorschlag bearbeiten möchten. Wählen Sie jetzt **Einlagerungsvorschläge** und setzen Sie die Planung fort.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>So planen Sie Anweisungen im Einlagerungsvorschlag:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Einlagerungsvorschlag** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die **Logistikbeleg holen** Aktion aus. Die Seite **Einlagerungsauswahl** wird geöffnet.  

    Sie sehen alle gebuchten Wareneingänge und registrierten internen Einlagerungen, die zur Einlagerungsfunktion weitergeleitet wurden, einschließlich derer, für die bereits Einlagerungsanweisungen erstellt wurden. Belege mit Einlagerungszeilen, die bereits vollständig eingelagert und registriert wurden, werden in dieser Übersicht nicht angezeigt.  

3. Wählen Sie die Belege, die Sie im Vorschlag bearbeiten möchten. Sie können gleichzeitig an Zeilen aus verschiedenen Belegen arbeiten.  

    > [!NOTE]  
    >  Wenn Sie versuchen, einen Beleg auszuwählen (Wareneingang oder interne Einlagerung), für den Sie bereits Anweisungen für alle Zeilen erzeugt haben, werden Sie von der Anwendung darüber informiert, dass es keine Mengen zu bewegen gibt.  

4. Füllen Sie das Feld **Sortiermethode** aus, um die Zeilen nach Wunsch zu sortieren.  

    > [!NOTE]  
    >  Die Art, auf die die Zeilen im Vorschlag sortiert sind, wird nicht automatisch an die Einlagerungsanweisungen übergeben, es bestehen aber dieselben Sortiermöglichkeiten neben der Lagerplatzpriorität. Es gibt jedoch dieselben Sortiermöglichkeiten – und noch eine weitere, Lagerplatzpriorität – für die Einlagerungsanweisungen. Die Zeilenreihenfolge, die Sie im Vorschlag planen, kann daher leicht wiederhergestellt werden, wenn Sie die Einlagerungsanweisungen erstellen oder durch Sortierung in den Einlagerungsanweisungen.  

5.  Füllen Sie das Feld **Bewegungsmenge** aus. Wählen Sie die **Bewegungsmenge autom. ausfüllen** Aktion aus, oder füllen Sie die Felder manuell aus.  
6.  Falls notwendig, bearbeiten Sie die Zeilen manuell. Sie können z. B. Zeilen löschen, wenn einige Artikel in einen Lagerplatz weit entfernt von den Lagerplätzen der anderen Artikel eingelagert werden müssen.  

    > [!NOTE]  
    >  Gelöschte Zeilen werden nur aus diesem Vorschlag gelöscht, nicht aus der Einlagerungsauswahlliste.  

7.  Wählen Sie die Aktion **Einlagerung erstellen** aus. Auf der Seite **Beleg erstellen**, das sich jetzt öffnet, können Sie weitere Informationen zu der Einlagerung hinzufügen, die Sie erstellen, wie folgt:  

    -   Sie können die Einlagerung einem bestimmten Mitarbeiter zuordnen.  
    -   Sie können die Einlagerungsanweisungszeilen so sortieren, wie Sie es im Vorschlag getan haben oder nach Lagerplatzpriorität. Wenn Sie nach der Lagerplatzpriorität sortieren, erscheinen zuerst die Zeilen der Art "Entnahme", da die meisten Wareneingangslagerplätze eine Lagerplatzpriorität 0 haben, und als Letztes erscheinen die Zeilen der Art "Einlagerung", beginnend mit den Lagerplätzen mit der niedrigsten Lagerplatzpriorität. Wenn Sie Ihr Lager so strukturiert haben, dass sich Lagerplätze von ähnlicher Lagerplatzpriorität nebeneinander befinden, verkürzt eine auf diese Art durchgeführte Sortierung die Wege, die die Lagermitarbeiter zurücklegen müssen.  
    -   Sie können wählen, dass die Zwischenzeilen nicht angezeigt werden sollen, die die Anwendung erzeugt, wenn sie eine größere Einheit in kleinere Einheiten aufbricht, indem Sie das Feld **Gebindeanbruchsfilter verw.** wählen. Weitere Informationen finden Sie unter [Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Sie können wählen, dass nicht automatisch das Feld **Bewegungsmenge** in den Einlagerungsanweisungen ausgefüllt wird.  
    -   Sie können sich entscheiden, den Beleg sofort zu drucken.  

8.  Bestätigen Sie mit **OK**, und die Anwendung erzeugt die Einlagerung entsprechend Ihren Anforderungen.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
