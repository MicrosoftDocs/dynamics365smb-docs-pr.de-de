---
title: Anlagen neu bewerten
description: 'Erfahren Sie, wie der Wert von Anlagen reguliert wird und neue Beträge als erhöhte AfA oder Zuschreibungen erfasst werden und wie Sie andere Anschaffungskosten buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5628, 5629, 5633'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="revalue-fixed-assets"></a>Anlagen neu bewerten

Eine Neubewertung von Anlagen kann aus Abschreibungen, erhöhter AfA oder allgemeinen Wertanpassungen bestehen.

Wenn sich der Wert einer Anlage erhöht, buchen Sie eine Buchungsblattzeile mit einer Zuschreibung auf das AfA-Buch. Der neue Betrag wird als Abschreibung gemäß der Einrichtung der Anlagenbuchung erfasst.

Wenn sich der Wert einer Anlage verringert, buchen Sie eine Buchungsblattzeile mit einem niedrigen Betrag, einer erhöhten AfA, auf das AfA-Buch. Der neue Betrag wird als erhöhte AfA gemäß der Anlagebuchung eingerichtet.

Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern.

## <a name="to-post-appreciation-from-the-fixed-asset-gl-journal"></a>So buchen Sie Zuschreibungen aus dem Anlagenfinanzbuchhaltungsbuchungsblatt

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Neubewertung**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung von Zuschreibungen eingerichtet wird.

    > [!NOTE]  
    >   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Zuschreibungskonto** der Buchungsgruppe der Anlage enthält das Feld **Kto. Wartung** das Sollkonto im Sachkonto und das Feld **Gegenkto. Wartung** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>So buchen Sie eine erhöhte AfA aus dem Anlagen Fibu Buch.-Blatt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Erhöhte AfA**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer erhöhten AfA eingerichtet wird.

    > [!NOTE]  
    >   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Abschreibungskonto** das Habenkonto im Sachkonto und das Feld **Ausgaben-Abschreibungskonto** das Sollkonto im Sachkonto, auf das die Gegenposten für erhöhte AfA gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>So führen Sie allgemeine Neubewertungen von Anlagen aus

Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern. Das Kontrollkästchen **Indexierung zulassen** auf der Seite **AfA-Buch** muss aktiviert sein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlage indexieren** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.

    Neubewertungszeilen werden in Schritt 2 gemäß Ihrer Einstellungen erstellt. Die Zeilen werden entweder im Anlagen Buch.-Blatt oder im Anlagen Fibu Buch.-Blatt, abhängig von Ihren Vorlagen und Stapeln, die auf der Seite **Anlagen Buch.-Blatt Einr.** installiert sind, erstellt. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
5. Wählen Sie das Buch.-Blatt mit den Anlagen, die Sie neu bewerten möchten und wählen die Aktion **Posten** aus.  
6. Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen** aus, um das Buch.-Blatt zu buchen.

    > [!TIP]  
    >   Falls die Indexzahlen nur für die Simulation verwendet werden, können Sie ein spezielles AfA-Buch dafür erstellen. Dann haben diese Posten keinen Einfluss auf andere AfA-Bücher.

## <a name="to-post-other-acquisition-costs"></a>So buchen Sie weitere Anschaffungskosten

Sie können weitere Anschaffungskosten einer Anlage aus einer Einkaufsrechnung oder aus einem Anlagen-Buch.-Blatt auf die gleiche Art buchen, auf die Sie die ursprünglichen Anschaffungskosten gebucht haben. Weitere Informationen finden Sie unter [Anlagen erwerben](fa-how-acquire.md).  

Falls bereits AfA für die Anlage berechnet wurde, aktivieren Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.**, damit die weiteren Anschaffungskosten abzüglich des Restwertes proportional zu dem Betrag abgeschrieben werden, der für angeschaffte Anlage bereits abgeschrieben wurde. Diese Methode stellt sicher, dass die AfA-Periode nicht geändert wird.  

Die Berechnung des Abschreibungsprozentsatzes erfolgt in dieser Weise:  

*P = (Gesamt AfA x 100) / AfA Basis*

*AfA Betrag = (P/100) x (zusätzliche Anschaffungskosten - Restwert)*  

Beachten Sie, dass Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung, dem Anlagen-Fibu-Buch.-Blatt oder den Anlagen-Buch.-Blattzeilen aktivieren müssen, um sicherzustellen, dass die AfA vom letzten Anlagenbuchungsdatum bis zum Buchungsdatum der weiteren Anschaffungskosten berechnet wird.

### <a name="example---posting-other-acquisition-costs"></a>Beispiel: Weitere Anschaffungskosten buchen

Eine Maschine wurde am 1. August 2000 erworben. Die Anschaffungskosten betragen 4.800. Die AfA-Methode ist linear über vier Jahre.

Am 31. August 2000 wird die Stapelverarbeitung **AfA berechnen** ausgeführt. Die AfA wird berechnet als:

*Buchwert x AfA-Tage / Gesamtzahl der AfA-Tage = 4800 x 30 / 1440 = 100*  

Am 15. September 2000 wird eine Rechnung für die Lackierung der Maschine gebucht. Der Rechnungsbetrag ist 480.

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, ergibt sich folgende Berechnung:  

15 Tage AfA (vom 01.09.00 bis zum 15.09.00) werden berechnet als:

*Buchwert x AfA-Tage / verbleibende Anzahl der AfA-Tage = (4800 - 100) x 15 / 1410 = 50*

Falls Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, ergibt sich folgende Berechnung:  

*Die weiteren Anschaffungskosten werden abgeschrieben als ((150 x 100) / 4800) / 100 x 480 = 15*

Die Grundlage für AfA ist jetzt *5280 = (4800 + 480)*, und die kumulierte AfA ist *165 = (100 + 50 + 15)*. Dies entspricht 45 AfA-Tagen der gesamten Anschaffungskosten. Diese Berechnung bedeutet, dass die Anlage innerhalb der geschätzten Lebensdauer von vier Jahren vollständig abgeschrieben wird.  

Wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt wird, wird die folgende Berechnung verwendet:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1.395 Tage*  

*Der Buchwert ist (5280 - 165) = 5115*  

*AfA-Betrag für September 2000: 5115 x 15 / 1395 = 55,00*  

*Gesamtsumme AfA = 165 + 55 = 220*  

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** nicht aktiviert haben, verliert die Anlage 15 AfA-Tage, weil der Batchauftrag **AfA berechnen**, der am 30.09.00 ausgeführt wurde, die AfA vom 15.09.00 bis zum 30.09.00 berechnen würde. D. h., wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt würde, würde die folgende Berechnung erfolgen:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1.395 Tage*  

*Der Buchwert ist (4800 + 480 - 100 - 15) = 5165*

*Der AfA-Betrag für September 2000: 5165 x 15 / 1395 = 55,54*  

*Gesamtsumme AfA = 100 + 15 + 55.54 = 170.54*

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[Finanzen](finance.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
