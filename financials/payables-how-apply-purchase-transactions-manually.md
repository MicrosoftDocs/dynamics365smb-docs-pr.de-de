---
title: 'Vorgehensweise: Abstimmen von Kreditorenzahlunge manuell | Microsoft Docs'
description: 'Vorgehensweise: Manuelle Abstimmung von Debitorenzahlungen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 86f59b54f0261f9aa835dc35db6f31cbb55e5d04
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Manuelle Abstimmung von Debitorenzahlungen
<a id="how-to-reconcile-vendor-payments-manually" class="xliff"></a>
Wenn Sie eine Zahlung an einen Kreditor senden oder eine Erstattung von einem Kreditor erhalten, müssen Sie entscheiden, ob die Zahlung oder die Rückerstattung mit einem oder mehreren offenen Posten ausgeglichen werden soll. Sie können den genauen Betrag zum Ausgleichen der Zahlung oder der Rückerstattung angeben und dann die Kreditorenposten nur teilweise ausgleichen. Sie müssen alle Kreditorenposten ausgleichen, um eine korrekte Kreditorenstatistik und Berichte der Kontoauszüge und Zinsrechnungen zu erhalten.

**Hinweis**: Kreditoren erteilen gelegentlich eine Zahlungsrückerstattung anstelle einer Gutschrift, die mit zukünftigen Rechnungen verrechnet wird, insbesondere wenn bereits bezahlte Artikel zurückgeben werden oder ein zu hoher Betrag für eine Rechnung gezahlt wurde.

Sie können Kreditorenposten auf drei verschiedene Arten übernehmen:

* Durch die Eingabe von Informationen in speziellen Fenstern, wie das **Zahlungsausgangs Buch.-Blatt** und das Fenster **Zahlungsabstimmungsbuch.-Blatt**.
* Aus Einkaufsgutschriften.
* Kreditorposten nach Einkaufsbelegen werden gebucht aber nicht angewendet.

**Hinweis**: Wenn das Feld **Ausgleichsmethode** auf der Kreditorenkarte **Auf älteste anwenden** enthält, dann wird die Zahlung automatisch mit der ältesten offenen Rechnung abgeglichen, wenn Sie nicht explizit angeben, auf welchen Habenposten sie sich bezieht. Ist die Ausgleichsmethode eines Debitors auf **Manuell** festgelegt, müssen die Posten manuell ausgeglichen werden.

Sie können Kreditorenzahlungen manuell auf die entsprechenden Einkaufsbelege anwenden, wenn Sie die Zahlungen im **Zahlung Buch.-Blatt**-Fenster buchen. Informationen zum Ausfüllen des Zahlungsausgangs Buch.-Blattes, finden Sie in [Vorgehensweise: Anwenden von Zahlungen](payables-make-payments.md).

Sie können Kreditorenzahlungen und Debitorenzahlungen anwenden nachdem die Zahlungen als negative Banktransaktionen in Ihrer Bank erscheinen. Im **Zahlungs-Abstimmungs-Buch.-Blatt**-Fenster können Sie Funktionen für den Bankkontoauszugsimport, die automatische Anwendung und die Bankkontoabstimmung verwenden. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

## So gleichen Sie eine Zahlung mit einem einzelnen Kreditorenposten aus
<a id="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Zahlungsjournal** ein und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie im Fenster **Zahlung Buch.-Blatt** in der ersten Buchungsblattzeile die entsprechenden Informationen zu dem Zahlungsposten ein.
3. So gleichen Sie gebuchte Kreditorenposten aus:
   1. Wählen Sie im Feld **Ausgleich mit Belegnr.** das Feld aus, um das Fenster **Kreditorenposten anwenden** zu öffnen.
   2. Wählen Sie im Fenster **Debitorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
   3. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.
4. Oder gleichen Sie gebuchte Kreditorenposten aus:

   1. Wählen Sie die Aktion **Posten ausgleichen...** aus.
   2. Wählen Sie im Fenster **Kreditorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
   3. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.  
   4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

      Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand des Fensters **Kreditorenpostenausgleich** sehen Sie einen Betrag im Feld Ausgleichsbetrag. Sie sehen, ob die Buchung ausgeglichen ist.
5. Wählen Sie die Schaltfläche **OK** aus.
6. Wählen Sie die Aktion **Buchen**, um das Buch.-Blatt zu buchen.

## So gleichen Sie eine Gutschrift mit mehreren Kreditorenposten aus
<a id="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Einkaufsgutschriftsmemo** eingeben und den entsprechenden Link auswählen.
2. Öffnen Sie die Gutschrift, die Sie ausgleichen möchten.
3. Geben Sie die relevanten Informationen in der Kopfzeile ein.
4. Um einen einzelnen Kreditorenposten, im Inforegister **Anwendung**, **Ausgleich mit Belegnr.** ausgleichen Feld, wählen Sie den Posten aus, auf den die Gurtschrift anzuwenden ist, und wählen Sie dann im Feld **Ausgleichsbetrag** Feld eingeben, den Betrag, die für Posten ausgleichen möchten.
5. Oder gleichen Sie gebuchte Kreditorenposten aus:

   1. Wählen Sie die Aktion **Posten ausgleichen...** aus.
   2. Wählen Sie die Zeilen mit den Posten aus, auf die die Gutschrift anzuwenden ist.
   3. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.  
   4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

       Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand des Fensters **Kreditorenpostenausgleich** sehen Sie einen Betrag im Feld **Ausgleichsbetrag**. Sie sehen, ob die Buchung ausgeglichen ist.
6. Wählen Sie die Schaltfläche **OK** aus.  
   Das Fenster **Einkaufsgutschrift** zeigt den im Feld **Auf Dokumenttyp anwenden** und auf **Dokumenttyp anwenden** ausgewählten Eintrag an. Feld Das Fenster zeigt auch den Betrag der zu buchenden Gutschrift an, wobei gegebenenfalls Skonti berücksichtigt werden.
7. Wählen Sie die Schaltfläche **Buchen**, um die Gutschrift zu buchen.

## So gleichen Sie gebuchte Kreditorenposten aus
<a id="to-apply-posted-vendor-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie den relevanten Kreditor mit bereits gebuchten Posten.
3. Wählen Sie die **Posten**-Aktion aus, und wählen Sie dann die **Posten ausgleichen**-Aktion aus.
4. Im Fenster **Kreditorenpostenausgleich** werden die offenen Posten des Kreditors angezeigt.
5. Wählen Sie die Zeile mit dem Posten, den Sie ausgleichen möchten.
6. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.

    Das Feld **Ausgleichs-ID** zeigt drei Sternchen (***), wenn Sie in einem Einbenutzersystem arbeiten, oder Ihre Benutzer-ID, wenn Sie in einem Mehrbenutzersystem arbeiten.  
7. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

    Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand des Fensters **Kreditorenpostenausgleich** sehen Sie den Betrag im Feld **Ausgleichsbetrag**.
8. Wählen Sie die Aktion **Ausgleich buchen** aus.  

    Das Fenster **Ausgleich buchen** wird mit der Belegnummer des Ausgleichspostens und dem Buchungsdatum des Postens geöffnet, der das aktuellste Buchungsdatum aufweist.
9. Klicken Sie auf die Schaltfläche **OK**, um den Ausgleich zu buchen.

## So wenden Sie Kreditorenposten in unterschiedlichen Währungen aufeinander an
<a id="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another" class="xliff"></a>
Falls Sie Käufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit der Rechnung ausgleichen.

Wenn Sie einen Posten (Posten 2) in einer Währung mit einem Posten (Posten 1) in einer anderen Währung ausgleichen, wird das Buchungsdatum von Posten 1 verwendet, um den entsprechenden Wechselkurs zur Umrechnung der Beträge von Posten 2 zu ermitteln. Den Wechselkurs finden Sie im Fenster **Währungswechselkurse**. In diesem Fall müssen Sie die Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren. Weitere Informationen finden Sie unter [Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungsjournal** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie das gewünschte Buch.-Blatt, und füllen Sie unter Verwendung eines Währungscodes die erste Zeile aus.
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.
4. Klicken Sie auf die Zeile mit dem Posten, mit dem Sie den Posten im Zahlungsausgangs Buch.-Blatt. ausgleichen möchten. Klicken Sie dann auf **Ausgleichs-ID festlegen** und wählen Sie den auszugleichenden Posten aus.
5. Wählen Sie die Schaltfläche **OK**, um zum Zahlungsausgangsbuchungsblatt zurückzukehren.
6. Buchen Sie das Zahlungsausgangs Buch.-Blatt.

**Wichtig**: Wenn Sie Posten in verschiedenen Währungen miteinander ausgleichen, rechnet die Anwendung die Beträge in EUR um. Selbst wenn der Wechselkurs fest ist, z. B. zwischen USD und EUR, kann es zu Rundungsdifferenzen kommen, wenn diese Fremdwährungsbeträge in EUR umgerechnet werden. Diese Rundungsdifferenzen werden als Gewinne und Verluste auf die Konten gebucht, die in den Feldern **Kursgewinn realisiert** oder **Kursverlust realisiert** des Fensters **Währungen** angegeben sind. Außerdem werden die Beträge im Feld **Betrag (EUR)** der entsprechenden Kreditorenposten angepasst.

## So heben Sie den Ausgleich von Kreditorenposten auf
<a id="to-unapply-an-application-of-vendor-entries" class="xliff"></a>
Wenn Sie einen fehlerhaften Ausgleich aufheben, wird ein Korrekturposten (ein Posten, der mit dem ursprünglichen Posten identisch ist, im Betragsfeld allerdings ein umgekehrtes Vorzeichen aufweist) für alle Posten erstellt und gebucht, einschließlich aller aus dem Ausgleich abgeleiteten Fibu-Buchungen, z. B. Skonto und Währungsgewinne/-verluste. Die von der Anwendung geschlossenen Posten werden erneut geöffnet.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") . Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Kreditorenkarte.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie den entsprechenden Posten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
5. Alternativ wählen Sie die Aktion **Detaillierte Posten** aus.
6. Wählen Sie den entsprechenden Ausgleichsposten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
7. Füllen Sie die Felder im Kopf aus, und wählen Sie dann die Aktion **Aufheben** aus.

**Wichtig**: Wenn ein Posten durch mehrere Ausgleichsposten ausgeglichen wurde, müssen Sie zuerst den Ausgleich des letzten Ausgleichspostens aufheben.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

