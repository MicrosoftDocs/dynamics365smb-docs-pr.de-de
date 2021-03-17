---
title: Anlagen abschreiben oder amortisieren| Microsoft Docs
description: Sie müssen festlegen, wie Sie jede Ihrer Anlagen abschreiben oder amortisieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 46a138d7168c48e47f9db823108abc6d6af280ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380581"
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Anlagen abschreiben oder amortisieren
Abschreibung wird verwendet, um die Anschaffungskosten von Anlagen wie Maschinen und Ausrüstung über die Nutzungsdauer zu verteilen. Sie müssen für jede Anlage definieren, wie diese abgeschrieben wird.  

 Es gibt zwei Wege, Abschreibungen zu buchen:  

* Automatisch durch Ausführen der Stapelverarbeitung **AfA berechnen**  
* Manuell, unter Verwendung des Anlagen Fibu Buch.-Blattes.  

[!INCLUDE[prod_short](includes/prod_short.md)] kann tägliche Abschreibungen berechnen, sodass Sie Abschreibungen für beliebige Perioden berechnen können. Sie können damit das aktuelle operative Ergebnis beispielsweise auf monatlicher, quartalsweiser oder jährlicher Basis analysieren. Die Berechnungen verwendet ein standardisiertes Jahr mit 360 Tagen und einen standardisierten Monat mit 30 Tagen. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md).  

Falls eine Anlage von verschiedenen Abteilungen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Abteilungen verteilt werden.  

Sie können falsche AfA-Posten aus einem AfA-Buch mit Hilfe der Stapelverarbeitung **Anlagenposten stornieren** stornieren. Danach können Sie die korrekten Beträge buchen, indem Sie die Stapelverarbeitung **AfA berechnen** erneut ausführen. Wenn Sie Fehler korrigieren, werden diese als Anlagenstornoposten gebucht.  

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die AfA-Beträge neu zu berechnen.  

## <a name="to-calculate-depreciation-automatically"></a>So berechnen Sie AfA automatisch
Einmal monatlich oder in beliebigen anderen Intervallen können Sie die Stapelverarbeitung **AfA berechnen** ausführen. Der Stapelverarbeitungsjob ignoriert Anlagen, die verkauft wurden, auf der Anlagenkarte gesperrt oder inaktiv sind, und Anlagen, die die AfA-Methode "Manuell" verwenden.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Abschreibung berechnen** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Schaltfläche **OK** aus.  

    Die Stapelverarbeitung berechnet die AfA und erstellt Zeilen im Anlagen Fibu Buch.-Blatt.

4. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen-Fibu Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  

    Auf der Seite **Anlagen-Fibu Buch.-Blatt** können Sie im Feld **Anzahl AfA-Tage** sehen, wie viele AfA-Tage berechnet wurden.  
5. Wählen Sie die Aktion **Buchen** aus.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>So buchen Sie eine AfA aus dem Anlagen Fibu Buch.-Blatt
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen-Fibu Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.  
3. Wählen Sie im Feld **Anlagenbuchungsart** die **AfA**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die AfA-Buchung eingerichtet ist. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Wählen Sie die Aktion **Buchen**, um das Journal zu buchen.  

Das Feld **Buchwert** auf der Seite **Anlagenkarte** wird entsprechend aktualisiert.

Falls Sie Anlagenverteilungsschlüssel eingerichtet haben, um Beträge auf verschiedene Kostenstellen und/oder Kostenträger zu verteilen, werden die Beträge während der Buchung zugeordnet. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>So werden Erinnerungswerte verwaltet
Im Feld **Erinnerungswert** auf der Seite **Anlagenabschreibungsbücher** können Sie den Buchwert angeben, den Ihre Anlage im aktuellen Abschreibungsbuch haben soll, nachdem es vollständig abgeschrieben wurde. Sie können dies manuell tun oder Sie können das Feld **Standarderinnerungswert** auf der zugehörigen Seite **AfA-Buch** ausfüllen, womit dann das Feld automatisch ausgefüllt wird.

> [!NOTE]
> Wenn die letzte Abschreibung bedeutet, dass das Feld **Buchwert** auf der Seite **Anlagenkarte** null ist, wird die letzte Abschreibung automatisch um diesen Betrag reduziert.<br /><br />
> Wenn der Wert im Feld **Buchwert** nach der letzten Abschreibung größer als null ist, beispielsweise wegen eines Rundungsproblems oder weil ein Restwert besteht, wird der Wert im Feld **Erinnerungswert** auf der Seite **Anlagen-AfA-Bücher** ignoriert. Weitere Informationen finden Sie unter [Wie der Restwert zusammen mit den Anschaffungskosten gebucht wird](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>So berechnen Sie Verteilungen in Anlagen Fibu Buch.-Blättern
Falls eine Anlage von verschiedenen Kostenstellen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Kostenstellen verteilt werden.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen-Fibu Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine ursprüngliche Zeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Verteilung**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer Verteilung eingerichtet wird.  
5. Wählen Sie die Aktion **Buchen**, um das Journal zu buchen.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Kopiervorgänge zum Vorbereiten von Buchungen in mehrere AfA-Bücher verwenden
Ausfüllen der Zeilen in einem Buch.-Blatt für die Buchung auf ein AfA-Buch und anschließendes Kopieren der Zeilen in ein anderes Buch.-Blatt, von wo aus sie auf ein anderes AfA-Buch gebucht werden können Weitere Informationen finden Sie unter [So buchen Sie Posten auf verschiedene Abschreibungsbücher](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AfA-Bücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das entsprechende AfA-Buch aus und aktivieren Sie dann das Kontrollkästchen **Teil des Kopiervorgangs**.  

> [!IMPORTANT]  
>   Wenn Sie das Feld **Kopiervorgang aktivieren** aktiviert haben, dürfen Sie im Buch.-Blatt keine Nummernserien verwenden. Der Grund dafür ist, dass die Nummernserie für das Anlagen Fibu Buch.-Blatt nicht der Nummernserie im Anlagen Buch.-Blatt entspricht.  

## <a name="to-post-entries-to-different-depreciation-books"></a>So buchen Sie Posten auf verschiedene AfA-Bücher
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen-Fibu Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2. Aktivieren Sie im Buch.-Blatt, das Sie zum Buchen der AfA verwenden möchten, das Kontrollkästchen **Kopiervorgang aktivieren**.  
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Buchen**.  
5. Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  

    > [!NOTE]  
    >   Auf der Seite **Anlagen Buch.-Blatt** enthält neue Zeilen für verschiedene AfA-Bücher entsprechend der Verdopplungsliste.  
6. Prüfen oder bearbeiten Sie die Zeilen, und wählen Sie dann die Aktion **Buchen** aus.  

    > [!NOTE]  
    >   Eine andere Art, einen Posten in ein anderes Buch zu kopieren, ist es, einen AfA-Buchcode in dem Feld **In AfA-Buch kopieren** anzugeben, wenn Sie eine Buch.-Blattzeile ausfüllen.  

Sie können mit Hilfe der Stapelverarbeitung **AfA-Buch kopieren** Posten von einem AfA-Buch in ein anderes AfA-Buch kopieren. Die Stapelverarbeitung erstellt Buch.-Blattzeilen in dem Buch.-Blatt, das Sie auf der Seite **Anlagen Buch.-Blatt Einr.** für das AfA-Buch angegeben haben, aus dem Sie kopieren möchten. Weitere Informationen finden Sie in der folgenden Prozedur.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>So kopieren Sie Anlagenposten zwischen AfA-Büchern
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AfA-Bücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die entsprechende AfA-Buch - Karte und wählen Sie dann die Aktion **AfA-Buch kopieren**.  
3. Füllen Sie im Inforegister **AfA-Buchkarte kopieren** die Seite nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus.  

Die kopierten Zeilen werden entweder in einem Anlagen Fibu Buch.-Blatt oder im Anlagen Buch.-Blatt erstellt. Dies hängt davon ab, ob das AfA-Buch, das Sie kopieren, in der Finanzbuchhaltung aktiviert wurde.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]