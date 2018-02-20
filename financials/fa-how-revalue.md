---
title: Anlagen neu bewerten| Microsoft Docs
description: "Erfahren Sie, wie der Wert von Anlagen reguliert wird und neue Beträge als erhöhte AfA oder Zuschreibungen erfasst werden, und buchen Sie zusätzliche Anschaffungskosten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b7ed3e38b4a697de678e11a8735869b666910081
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="revalue-fixed-assets"></a>Anlagen neu bewerten
Eine Neubewertung von Anlagen kann aus Abschreibungen, erhöhter AfA oder allgemeinen Wertanpassungen bestehen.

Wenn sich der Wert einer Anlage erhöht hat, buchen Sie eine Buch.-Blattzeile mit einem höheren Betrag, einer Abschreibung, auf das AfA-Buch. Der neue Betrag wird als Abschreibung gemäß der Anlagebuchung eingerichtet.

Wenn sich der Wert einer Anlage verringert hat, buchen Sie eine Buch.-Blattzeile mit einem niedrigen Betrag, einer erhöhten AfA, auf das AfA-Buch. Der neue Betrag wird als erhöhte AfA gemäß der Anlagebuchung eingerichtet.

Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal"></a>So buchen Sie Zuschreibungen aus dem Anlagen Fibu Buch.-Blatt
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Neubewertung**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung von Zuschreibungen eingerichtet wird.

    > [!NOTE]  
>   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Im Fenster **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Abschreibungskonto** das Sollkonto im Sachkonto und das Feld **Gegenkto. Abschreibung** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie im Abschnitt "So richten Sie Anlagenbuchungsgruppen ein" in [ Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>So buchen Sie eine erhöhte AfA aus dem Anlagen Fibu Buch.-Blatt
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Erhöhte AfA**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer erhöhten AfA eingerichtet wird.

    > [!NOTE]  
>   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Im Fenster **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Abschreibungskonto** das Habenkonto im Sachkonto und das Feld **Ausgaben-Abschreibungskonto** das Sollkonto im Sachkonto, auf das die Gegenposten für erhöhte AfA gebucht werden sollen. Weitere Informationen finden Sie im Abschnitt "So richten Sie Anlagenbuchungsgruppen ein" in [ Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>So führen Sie allgemeine Neubewertungen von Anlagen aus
Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern. Das Kontrollkästchen **Indexierung zulassen** im Fenster **AfA-Buch** muss aktiviert sein.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Analgenindex** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.

    Neubewertungszeilen werden in Schritt 2 gemäß Ihrer Einstellungen erstellt. Die Zeilen werden entweder im Anlagen Buch.-Blatt oder im Anlagen Fibu Buch.-Blatt, abhängig von Ihren Vorlagen und Stapeln, die im Fenster **Anlagen Buch.-Blatt Einr.** installiert sind, erstellt. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).
4. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
5. Wählen Sie das Buch.-Blatt mit den Anlagen, die Sie neu bewerten möchten und wählen die Aktion **Posten** aus.  
6. Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen** aus, um das Buch.-Blatt zu buchen.

    > [!TIP]  
>   Falls die Indexzahlen nur für die Simulation verwendet werden, können Sie ein spezielles AfA-Buch dafür erstellen. Dann haben diese Posten keinen Einfluss auf andere AfA-Bücher.

   ## <a name="to-post-additional-acquisition-costs"></a>So buchen Sie zusätzliche Anschaffungskosten
   Sie können zusätzliche Anschaffungskosten einer Anlage auf die gleiche Art buchen, auf die Sie die ursprünglichen Anschaffungskosten gebucht haben: aus einer Einkaufsrechnung oder aus einem Anlagen Buch.-Blatt. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).  

Falls bereits AfA für die Anlage berechnet wurde, aktivieren Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.**, damit die zusätzlichen Anschaffungskosten abzüglich des Restwertes proportional zu dem Betrag abgeschrieben werden, der für angeschaffte Anlage bereits abgeschrieben worden ist. Dies stellt sicher, dass die AfA Periode nicht geändert wird.  

Die Berechnung des Abschreibungsprozentsatzes erfolgt in dieser Weise:  

*P = (Gesamt AfA x 100) / AfA Basis*

*AfA Betrag = (P/100) x (zusätzliche Anschaffungskosten - Restwert)*  

Beachten Sie, dass Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung, dem Anlagen Fibu Buch.-Blatt oder den Anlagen Buch.-Blattzeilen aktivieren müssen, um sicherzustellen, dass die AfA vom letzten Anlagenbuchungsdatum bis zum Buchungsdatum der zusätzlichen Anschaffungskosten berechnet wird.

### <a name="example---posting-additional-acquisition-costs"></a>Beispiel – Buchen von zusätzlichen Anschaffungskosten
Eine Maschine wurde am 1. August 2000 erworben. Die Anschaffungskosten betragen 4.800. Die AfA-Methode ist linear über vier Jahre.

Am 31. August 2000 wird die Stapelverarbeitung **AfA berechnen** ausgeführt. Die AfA wird berechnet als:

*Buchwert x AfA-Tage / Gesamtzahl der AfA-Tage = 4800 x 30 / 1440 = 100*  

Am 15. September 2000 wird eine Rechnung für die Lackierung der Maschine gebucht. Der Rechnungsbetrag ist 480.

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, würde die folgende Berechnung erfolgen:  

15 Tage AfA (vom 01.09.00 bis zum 15.09.00) werden berechnet als:

*Buchwert x AfA-Tage / verbleibende Anzahl der AfA-Tage = (4800 - 100) x 15 / 1410 = 50*

Falls Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, würde die folgende Berechnung erfolgen:  

*Die zusätzlichen Anschaffungskosten werden abgeschrieben als ((150 x 100) / 4800) / 100 x 480 = 15*

Die Grundlage für AfA ist jetzt *5280 = (4800 + 480)*, und die kumulierte AfA ist *165 = (100 + 50 + 15)*. Dies entspricht 45 AfA-Tagen der gesamten Anschaffungskosten. Das bedeutet, dass die Anlage innerhalb der geschätzten Lebensdauer von vier Jahren vollständig abgeschrieben wird.  

Wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt wird, wird die folgende Berechnung verwendet:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1395 Tage*  

*Der Buchwert ist (5280 - 165) = 5115*  

*AfA-Betrag für September 2000: 5115 x 15 / 1395 = 55,00*  

*Gesamtsumme AfA = 165 + 55 = 220*  

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** aktiviert haben, würde die Anlage 15 AfA-Tage verlieren, weil die Stapelverarbeitung **AfA berechnen**, die am 30.09.00 ausgeführt wurde, die AfA vom 15.09.00 bis zum 30.09.00 berechnen würde. D. h., wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt würde, würde die folgende Berechnung erfolgen:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1395 Tage*  

*Der Buchwert ist (4800 + 480 - 100 - 15) = 5165*

*Der AfA-Betrag für September 2000: 5165 x 15 / 1395 = 55,54*  

*Gesamtsumme AfA = 100 + 15 + 55.54 = 170.54*

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

