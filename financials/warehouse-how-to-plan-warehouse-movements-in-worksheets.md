---
title: "Vorgehensweise: Planen von Lagerplatzumlagerungen in Vorschlägen | Microsoft Docs"
description: "Planen Sie Lagerplatzumlagerungen im Vorschlag, indem Sie eine Wiederauffüllfunktion nutzen oder manuell die Zeilen planen, die Sie als Umlagerungsanweisungen erstellen möchten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e2cefcc91b823ac4a75d1eb209e892bc56b13de2
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-warehouse-movements-in-worksheets"></a>Vorgehensweise: Planen von Umlagerungen in Vorschlägen
Planen Sie Lagerplatzumlagerungen im Vorschlag, indem Sie eine Wiederauffüllfunktion nutzen oder manuell die Zeilen planen, die Sie als Umlagerungsanweisungen erstellen möchten.  

## <a name="to-calculate-a-replenishment-movement"></a>So berechnen Sie Lagerplatzauffüllungen:  
Wenn aus dem Lager Artikel an Kunden geliefert werden, enthalten die Lagerplätze mit den höchsten Prioritäten (höchstwahrscheinlich die, die am dichtesten am Warenausgangsbereich liegen) kontinuierlich weniger Artikel. Um diese Lagerplätze mit den höchsten Prioritäten mit Artikeln aus anderen Lagerplätzen wiederaufzufüllen, können Sie die Funktion **Lagerplatz-Auffüllung berechnen** im Fenster **Lagerplatzumlagerungsvorschlag** verwenden.

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen] Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplatzumlagerungsvorschlag** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Lagerplatzauffüllung berechnen**.  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt Zeilen, die genau angeben, wie Artikel von den Lagerplätzen mit niedriger Priorität in die mit höherer Priorität umgelagert werden sollen.  

    > [!NOTE]  
    >  Eine Umlagerung wird gemäß FEFO vorgeschlagen, wenn Sie die Funktion **Lagerplatzumlagerung erstellen** aktivieren und wenn die folgenden Bedingungen für einen Artikel erfüllt sind:  
    >   
    >  -   Der Artikel weist ein Ablaufdatum auf.  
    > -   Das Feld **Gemäß FEFO kommissionieren** ist auf der Lagerortkarte aktiviert, und  
    > -   Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.  
    > -   Die Felder **Von Zone** und **Von Lagerplatz** sind leer.  

    Weitere Informationen finden Sie unter[ Korrigieren der FEFO..](warehouse-picking-by-fefo.md)  

3.  Sehen Sie sich die Zeilen an und ändern Sie sie – falls notwendig – oder löschen Sie einige von ihnen, wenn Sie nicht genug Zeit haben, alle auszuführen.  
4.  Wählen Sie die Aktion **Lagerplatzumlagerung erstellen** aus, um eine Anweisung zu erstellen, die die Lagermitarbeiter ausführen sollen.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Den gesamten Inhalt eines oder mehrerer Lagerplätze umlagern, indem Sie die Funktion "Lagerplatzinhalt holen" verwenden  
Sie können den Lagerplatzumlagerungsvorschlag auch nutzen, um andere Umlagerungen von Artikeln innerhalb des Lagers zu planen. Wenn Sie z. B. Artikel für die Qualitätskontrolle in einen Lagerplatz einlagern möchten, können Sie den Lagerplatzumlagerungsvorschlag verwenden, um diese Aktion zu planen, und dann eine Lagerplatzumlagerung erstellen, die eine Anweisung für einen Mitarbeiter darstellt.  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen] Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplatzumlagerungsvorschlag** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die **Lagerplatzinhalt holen** Aktion aus. Verwenden Sie das Anforderungsfenster, um Filter auf die Lagerplätze und Artikel zu setzen, die in den Lagerplatzumlagerungsvorschlagszeilen erscheinen sollen.  
3.  Füllen Sie die entsprechenden Felder im Anforderungsfenster der Stapelverarbeitung aus. Wenn Sie z. B. den Lagerplatzinhalt aller Lagerplätze in einer bestimmten Zone des Lagerorts sehen möchten, füllen Sie das Feld **Zonencode** aus. Wenn Sie Zeilen für alle Lagerplätze holen möchten, die einen bestimmten Artikel enthalten, füllen Sie das Feld **Artikelnr.** aus.  

    > [!NOTE]  
    >  Sie können Artikel aus einem Lagerplatz der Lagerplatzart "Wareneingang" nicht manuell ein- oder auslagern, da Artikel in Lagerplätzen der Art "Wareneingang" als eingelagert registriert sein müssen, bevor sie ein Teil des verfügbaren Lagerbestands sind.  

4.  Wenn Sie viele Zeilen abrufen, wählen Sie **Sortierung**, um eine Sortiermethode zum Festlegen der Reihenfolge auszuwählen, in der die Zeilen im Vorschlag erscheinen sollen, und wählen Sie **OK**.  

    > [!NOTE]  
    >  Umlagerungszeilen werden gemäß FEFO übernommen, wenn Sie die Funktion **Lagerplatzumlagerung erstellen** aktivieren und wenn die folgenden Bedingungen für einen Artikel erfüllt sind:  
    >   
    >  -   Der Artikel weist ein Ablaufdatum auf.  
    > -   Das Feld **Gemäß FEFO kommissionieren** ist auf der Lagerortkarte aktiviert, und  
    > -   Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.  
    > -   Die Felder **Von Zone** und **Von Lagerplatz** sind leer.  

5.  Vervollständigen Sie einige der geholten Zeilen, um die Änderungen abzubilden, die Sie durchführen möchten. Für jeden Artikel, den Sie umlagern möchten, müssen Sie die Felder **Artikelnr.**, **Von Lagerplatzcode**, **Nach Lagerplatzcode** und **Menge** ausfüllen.  
6.  Löschen Sie alle unvollständigen Zeilen, die Sie nur zu Informationszwecken verwendet haben.  
7.  Sobald die Lagerplatzumlagerungsvorschlagszeilen genau die Umlagerungen darstellen, die von dem Lagermitarbeiter ausgeführt werden sollen, wählen Sie die Aktionen **Lagerplatzumlagerung erstellen**, um die Anweisungen für den Mitarbeiter zu erzeugen.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

