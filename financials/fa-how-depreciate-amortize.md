---
title: 'So geht''s: Anlagen abschreiben oder amortisieren| Microsoft Docs'
description: Beschreibt, wie Anlagen abgeschrieben oder amortisiert werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3ea185979c2339a578149259f53aa81c18e5161b
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Anlagen abschreiben oder amortisieren
<a id="how-to-depreciate-or-amortize-fixed-assets" class="xliff"></a>
Abschreibung wird verwendet, um die Anschaffungskosten von Anlagen wie Maschinen und Ausrüstung über die Nutzungsdauer zu verteilen. Sie müssen für jede Anlage definieren, wie diese abgeschrieben wird.  

 Es gibt zwei Wege, Abschreibungen zu buchen:  

* Automatisch durch Ausführen der Stapelverarbeitung **AfA berechnen**  
* Manuell, unter Verwendung des Anlagen Fibu Buch.-Blattes.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kann tägliche Abschreibungen berechnen, sodass Sie Abschreibungen für beliebige Perioden berechnen können. Sie können damit das aktuelle operative Ergebnis beispielsweise auf monatlicher, quartalsweiser oder jährlicher Basis analysieren. Die Berechnungen verwendet ein standardisiertes Jahr mit 360 Tagen und einen standardisierten Monat mit 30 Tagen. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md).  

Falls eine Anlage von verschiedenen Abteilungen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Abteilungen verteilt werden.  

Sie können falsche AfA-Posten aus einem AfA-Buch mit Hilfe der Stapelverarbeitung **Anlagenposten stornieren** stornieren. Danach können Sie die korrekten Beträge buchen, indem Sie die Stapelverarbeitung **AfA berechnen** erneut ausführen. Wenn Sie Fehler korrigieren, werden diese als Anlagenstornoposten gebucht.  

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die AfA-Beträge neu zu berechnen.  

## So berechnen Sie AfA automatisch
<a id="to-calculate-depreciation-automatically" class="xliff"></a>
Einmal monatlich oder in beliebigen anderen Intervallen können Sie die Stapelverarbeitung **AfA berechnen** ausführen. Der Stapelverarbeitungsjob ignoriert Anlagen, die verkauft wurden, auf der Anlagenkarte gesperrt oder inaktiv sind, und Anlagen, die die AfA-Methode "Manuell" verwenden.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Abschreibung berechnen** ein und wählen Sie dann den entsprechenden Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Schaltfläche **OK** aus.  

    Die Stapelverarbeitung berechnet die AfA und erstellt Zeilen im Anlagen Fibu Buch.-Blatt.  
4. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.  

    Im Fenster **Anlagen-Fibu Buch.-Blatt** können Sie im Feld **Anzahl AfA-Tage** sehen, wie viele AfA-Tage berechnet wurden.  
5. Wählen Sie die Aktion **Buchen** aus.  

## So buchen Sie eine AfA aus dem Anlagen Fibu Buch.-Blatt
<a id="to-post-depreciation-manually-from-the-fixed-asset-gl-journal" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen Fibu Buch.-Blatt** eingeben und den entsprechenden Link auswählen.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.  
3. Wählen Sie im Feld **Anlagenbuchungsart** die **AfA**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die AfA-Buchung eingerichtet ist. Weitere Informationen finden Sie im Abschnitt "So richten Sie Anlagenbuchungsgruppen ein" in [So geht's: Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  
5. Wählen Sie auf der Registerkarte **Start** die Option **Buchen** aus, um das Buch.-Blatt zu buchen.  

Falls Sie Anlagenverteilungsschlüssel eingerichtet haben, um Beträge auf verschiedene Kostenstellen und/oder Kostenträger zu verteilen, werden die Beträge während der Buchung zugeordnet. Weitere Informationen finden Sie unter [So geht's: Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  

## So berechnen Sie Verteilungen in Anlagen Fibu Buch.-Blättern
<a id="to-calculate-allocations-in-the-fixed-asset-gl-journal" class="xliff"></a>
Falls eine Anlage von verschiedenen Kostenstellen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Kostenstellen verteilt werden.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen Fibu Buch.-Blatt** eingeben und den entsprechenden Link auswählen.  
2. Erstellen Sie eine ursprüngliche Zeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Verteilung**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer Verteilung eingerichtet wird.  
5. Wählen Sie auf der Registerkarte **Start** die Option **Buchen** aus, um das Buch.-Blatt zu buchen.  

## Kopiervorgänge zum Vorbereiten von Buchungen in mehrere AfA-Bücher verwenden
<a id="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books" class="xliff"></a>
Ausfüllen der Zeilen in einem Buch.-Blatt für die Buchung auf ein AfA-Buch und anschließendes Kopieren der Zeilen in ein anderes Buch.-Blatt, von wo aus sie auf ein anderes AfA-Buch gebucht werden können Weitere Informationen finden Sie im Abschnitt "So buchen Sie Posten auf verschiedene AfA-Bücher".

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Abschreibungsbuch** ein und wählen Sie dann den entsprechenden Link aus.  
2. Öffnen Sie das entsprechende AfA-Buch aus und aktivieren Sie dann das Kontrollkästchen **Teil des Kopiervorgangs**.  

**Wichtig:** Wenn Sie das Feld **Kopierliste verwenden** ausgewählt haben, dürfen Sie im Buch.-Blatt keine Nummernserien verwenden. Der Grund dafür ist, dass die Nummernserie für das Anlagen Fibu Buch.-Blatt nicht der Nummernserie im Anlagen Buch.-Blatt entspricht.  

## So buchen Sie Posten auf verschiedene AfA-Bücher
<a id="to-post-entries-to-different-depreciation-books" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen Fibu Buch.-Blatt** eingeben und den entsprechenden Link auswählen.  
2. Aktivieren Sie im Buch.-Blatt, das Sie zum Buchen der AfA verwenden möchten, das Kontrollkästchen **Kopiervorgang aktivieren**.  
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Buchen** aus.  
5. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.  

    **Hinweis:** Das Fenster **Anlagen Buch.-Blatt** enthält neue Zeilen für verschiedene AfA-Bücher entsprechend der Verdopplungsliste.  
6. Prüfen oder bearbeiten Sie die Zeilen, und wählen Sie dann die Aktion **Buchen** aus.  

    **Hinweis:** Eine andere Art, einen Posten in ein separates Buch zu kopieren ist es, einen AfA-Buchcode im Feld **In AfA-Buch kopieren** anzugeben, wenn Sie eine Buch.-Blattzeile ausfüllen.  

Sie können mit Hilfe der Stapelverarbeitung **AfA-Buch kopieren** Posten von einem AfA-Buch in ein anderes AfA-Buch kopieren. Die Stapelverarbeitung erstellt Buch.-Blattzeilen in dem Buch.-Blatt, das Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das AfA-Buch angegeben haben, aus dem Sie kopieren möchten. Weitere Informationen finden Sie in der folgenden Prozedur.  

## So kopieren Sie Anlagenposten zwischen AfA-Büchern
<a id="to-copy-fixed-asset-ledger-entries-between-depreciation-books" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Abschreibungsbuch** ein und wählen Sie dann den entsprechenden Link aus.  
2. Öffnen Sie die entsprechende AfA-Buch - Karte und wählen Sie dann die Aktion **AfA-Buch kopieren**.  
3. Füllen Sie im Fenster **AfA-Buch kopieren** die Felder nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus.  

Die kopierten Zeilen werden entweder in einem Anlagen Fibu Buch.-Blatt oder im Anlagen Buch.-Blatt erstellt. Dies hängt davon ab, ob das AfA-Buch, das Sie kopieren, in der Finanzbuchhaltung aktiviert wurde.  

## Siehe auch
<a id="see-also" class="xliff"></a>
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

