---
title: 'Vorgehensweise: Abstimmen von Kreditorenzahlungen manuell | Microsoft Docs'
description: 'Vorgehensweise: Manuelle Abstimmung vom Zahlungen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 929404a3385a7964136226ae1ee1a8775dd7a62a
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Manuelle Abstimmung vom Zahlungen
<a id="how-to-reconcile-customer-payments-manually" class="xliff"></a>
Wenn Sie einen Zahlungseingang von einem Debitor erhalten oder eine Barerstattung durchführen, müssen Sie entscheiden, ob die Zahlung oder die Rückerstattung mit einem oder mehreren offenen Soll- oder Habenposten ausgeglichen werden soll. Sie können den Betrag angeben, den Sie anwenden möchten. Beispielsweise können Sie Teilzahlungen für die Debitorenposten übernehmen. Schließende Debitorenposten stellen sicher, dass Informationen wie Debitorenstatistiken, Kontoauszüge und Zinsrechnungen korrekt sind.

**Hinweis**: Im Fenster **Debitorenposten** bedeutet die rote Schriftart, dass die entsprechende Zahlung nach dem Fälligkeitsdatum liegt.

Sie können Debitorenposten auf mehrere Arten übernehmen:

* Durch die Eingabe von Informationen in speziellen Fenstern, wie das **Barzahlungseingangsbuch.-Blatt** und das Fenster **Zahlungsabstimmungsbuch.-Blatt**.
* Aus den Verkaufsgutschriftsbelegen.
* Debitorenposten nach Verkaufsbelegen werden gebucht aber nicht angewendet.

**Hinweis**: Wenn das Feld **Ausgleichsmethode** auf der Debitorenkarte **Auf älteste anwenden** festgelegt ist, dann wird die Zahlung automatisch mit der ältesten offenen Rechnung abgeglichen, wenn Sie nicht explizit angeben, auf welchen Habenposten sie sich bezieht. Ist die Ausgleichsmethode eines Kreditors auf **Manuell** festgelegt, müssen die Posten immer manuell ausgeglichen werden.

Sie können Zahlungen automatisch im Fenster **Zahlungseingangsbuch.-Blatt** manuell verbuchen. Ein Zahlungseingangs Buch.-Blatt ist eine Art von Fibu Buch.-Blatt. Daher können Sie es verwenden, um Transaktionen auf Sach-, Bank-, Debitoren-, Kreditor- und Anlagenkonten zu buchen. Daher können Sie die Zahlungen beim Buchen auf einen oder mehrere Sollposten anwenden oder die gebuchten Posten später anwenden.

Sie können Debitorenzahlungen und Kreditorenzahlungen, im Fenster **Zahlungsabstimmungsbuch.-Blatt** mithilfe von Funktionalitäten für den Bankkontoauszugsimport, die automatische Anwendung und die Bankkontoabstimmung verwenden. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md). Alternativ können Sie Debitorenzahlungen auf einer Liste der unbezahlten Verkaufsbelegen im Fenster **Zahlungs-Registrierung** abstimmen. Weitere Informationen finden Sie unter [Vorgehensweise: Abstimmen von Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

## So füllen Sie ein Zahlungseingangs Buch.-Blatt aus und buchen dieses
<a id="to-fill-and-post-a-cash-receipt-journal" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditübertragungsjournale** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Wählen Sie im Feld **Buch.-Blattname** das relevante Buch.-Blatt aus.
4. Füllen Sie das Feld **Buchungsdatum** aus.  
5. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.

    Die **Dokumentennummer** Feld wird anhand der Nummernserie ausgefüllt, die dem Charge zugeordnet ist.  
6. **Externe Dokumentennummer** verwenden Verwenden Sie das Feld Externe Belegnummer, um eine Kennung wie die Schecknummer des Debitors zu speichern.
7. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
8. Wählen Sie im Feld **Kontonummer** Wählen Sie das entsprechende Sachkonto.
9. Falls Sie den Ausgleich gleichzeitig mit dem Buch.-Blatt buchen möchten, führen Sie einen der folgenden Schritte durch.
10. Wählen Sie im Feld **Gegenkontoart** das **Sachkonto** für Barzahlungen und das **Bankkonto** für sonstige Zahlungen aus.
11. Wählen Sie im Feld **Ausgleichskontonummer** das Barkonto für Barzahlungen oder das zutreffende Bankkonto für sonstige Zahlungen aus.
12. Buchen Sie das Buch.-Blatt.

## So gleichen Sie einen einzelnen Debitorenposten mit einer Zahlung aus:
<a id="to-apply-a-payment-to-a-single-customer-ledger-entry" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungseingangs-Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Wählen Sie im Feld **Ausgleich mit Belegnr.** Feld, wählen das Feld, um das Fenster **Debitorenposten anwenden**.
8. Wählen Sie im Fenster **Kreditorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
9. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand des Fensters **Benutzerdefinierter Eintrag anwenden** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
10. Wählen Sie die Schaltfläche **OK** aus. Das Fenster **Bahrzahlungseingangsbuch.-Blatt** zeigt nun die von Ihnen ausgewählten Einträge unter **Auf Dokumenttyp anwenden** und auf **Dokumenttyp anwenden**. Felder.
11. Buchen Sie das Zahlungseingangs-Buch.-Blatt.

## So gleichen Sie mehrere Debitorenposten mit einer Zahlung aus:
<a id="to-apply-a-payment-to-multiple-customer-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungseingangs-Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Geben Sie im Feld **Betrag** die vollständige Zahlung als negativen Betrag ein.
8. Wenn Sie die Zahlung bei der Buchung mit mehreren Kreditorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.
9. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.
10. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand des Fensters **Benutzerdefinierter Eintrag anwenden** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
11. Wählen Sie die Schaltfläche **OK** aus.
12. Buchen Sie das Zahlungseingangs-Buch.-Blatt.

## So gleichen Sie einen einzelnen Debitorenposten mit einer Gutschrift aus:
<a id="to-apply-a-credit-memo-to-a-single-customer-ledger-entry" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie bei der Buchung einen einzelnen Kreditorenposten durch die Gutschrift ausgleichen möchten, klicken Sie auf das Feld **Auf Dok.Nummer anwenden** und wählen den Posten aus, den Sie mit der Zahlung ausgleichen möchten.
4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.  

    Wenn Sie keinen Betrag eingeben, gleicht das Programm automatisch mit dem Höchstbetrag aus. Am unteren Rand des Fensters **Benutzerdefinierter Eintrag anwenden** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.    
5. Wählen Sie die Schaltfläche **OK** aus. Das Fenster **Verkaufsgutschrift** zeigt nun die von Ihnen ausgewählten Einträge unter **Auf Dokumenttyp anwenden** und auf **Dokumenttyp anwenden**. Felder. Und den Betrag der zu buchenden Gutschrift an, wobei mögliche Skonti berücksichtigt werden.
6. Buchen Sie die Gutschrift.

## So gleichen Sie mehrere Debitorenposten mit einer Gutschrift aus:
<a id="to-apply-a-credit-memo-to-multiple-customer-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie die Zahlung bei der Buchung mit mehreren Kreditorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.
4. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.
5. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand des Fensters **Benutzerdefinierter Eintrag anwenden** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
6. Wählen Sie die Schaltfläche **OK** aus. Das Fenster **Verkaufsgutschrift** zeigt nun den Betrag der zu buchenden Gutschrift an, wobei gegebenenfalls Skonto berücksichtigt wird.
7. Buchen Sie die Gutschrift.

## So gleichen Sie gebuchte Debitorenposten aus:
<a id="to-apply-posted-customer-ledger-entries" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Debitorenkarte für den Debitor mit den Posten, die Sie ausgleichen möchten.
3. Klicken Sie auf **Einträge** und wählen dann die Zeile mit dem Posten aus, den Sie ausgleichen möchten.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus. Im Fenster **Debitorenpostenausgleich** werden die offenen Posten für den Debitor angezeigt.
5. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**. Aktion
6. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand des Fensters **Debitorenpostenausgleich** wird im Feld **Ausgleichsbetrag** der spezifische Betrag angezeigt.  
7. Wählen Sie die Aktion **Ausgleich buchen** aus. Das Fenster **Ausgleich buchen** wird mit der Belegnummer des Ausgleichspostens und dem Buchungsdatum des Postens angezeigt, der das aktuellste Buchungsdatum aufweist.  
8. Klicken Sie auf die Schaltfläche **OK**, um den Ausgleich zu buchen.

    Wenn der gebuchte Ausgleich abgeschlossene Debitorenposten zur Folge hat, wird für diese Posten im Feld **Offen** kein Häkchen mehr angezeigt.    
9. Um die Verkaufsposten zu sehen wählen Sie in der oberen rechter Ecke das **Symbol Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus. Wechseln Sie zur Karte für den jeweiligen Debitor, um die Buchungsposten zu sehen.  

Sie können in der Liste der Posten sehen, dass„” „”i„”n der Zeile mit dem vollständig ausgeglichenen Posten das Feld **Offen** nicht aktiviert ist.  

**Hinweis**: Nachdem Sie im Fenster **Debitorenpostenausgleich** einen Posten oder mehrere Posten durch Festlegen der **Ausgleichs-ID** ausgewählt haben, enthält das Feld **Ausgleichsbetrag** die Summe der Restbeträge für die ausgewählten gebuchten Posten, es sei denn, das Feld enthält bereits Informationen. Wenn Sie **Auf Älteste Anwenden** im Feld **Anwendungsmethode** auf der Debitorenkarte auswählen, tritt die Anwendung automatisch auf.

## So gleichen Sie Debitorenposten in verschiedenen Währungen untereinander aus:
<a id="to-apply-customer-ledger-entries-in-different-currencies-to-one-another" class="xliff"></a>
Wenn Sie an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie dennoch die Rechnung mit der Zahlung ausgleichen.  

Wenn Sie einen Posten (Posten 2) in einer Währung mit einem Posten (Posten 1) in einer anderen Währung ausgleichen, wird das Buchungsdatum von Posten 1 verwendet, um den entsprechenden Wechselkurs zur Umrechnung der Beträge von Posten 2 zu ermitteln. Den Wechselkurs finden Sie im Fenster **Währungswechselkurse**.  

Das Ausgleichen von Debitorenposten in verschiedenen Währungen muss aktiviert sein. Weitere Informationen finden Sie unter [So geht's: Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungseingangs-Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie das gewünschte Buch.-Blatt, und füllen Sie unter Verwendung eines Währungscodes die erste Zeile aus.
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.
4. Klicken Sie auf die Zeile mit dem Posten, mit dem Sie den Posten im Zahlungsausgangs-Buch.-Blatt ausgleichen möchten. Klicken Sie dann auf **Ausgleichs-ID festlegen** und wählen Sie den auszugleichenden Posten aus.
5. Wählen Sie die Schaltfläche **OK**, um zum Barzahlungseingangsbuch zurückzukehren.
6. Buchen Sie das Verkaufs Buch.-Blatt.  

**Wichtig**: Wenn Sie Posten in verschiedenen Währungen miteinander ausgleichen, rechnet die Anwendung die Beträge in USD um. Selbst wenn der Wechselkurs fest ist, z. B. zwischen USD und EUR, kann es zu Rundungsdifferenzen kommen, wenn diese Fremdwährungsbeträge in USD umgerechnet werden. Diese Rundungsdifferenzen werden als Gewinne und Verluste auf die Konten gebucht, die in den Feldern **Kursgewinn realisiert** oder **Kursverlust realisiert** des Fensters **Währungen** angegeben sind. Außerdem werden die Beträge im Feld **Betrag (USD)** der entsprechenden Kreditorenposten angepasst.  

## So heben Sie den Ausgleich von Debitoren- oder Kreditorenposten auf
<a id="to-correct-an-application-of-customer-entries" class="xliff"></a>
Wenn Sie einen fehlerhaften Ausgleich aufheben, wird ein Korrekturposten (ein Posten, der mit dem ursprünglichen Posten identisch ist, im Betragsfeld allerdings ein umgekehrtes Vorzeichen aufweist) für alle Posten erstellt und gebucht, einschließlich aller aus dem Ausgleich abgeleiteten Fibu-Buchungen, z. B. Skonto und Währungsgewinne/-verluste. Die von der Anwendung geschlossenen Posten werden erneut geöffnet.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") . Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Debitorenkarte.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie den entsprechenden Posten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
5. Alternativ wählen Sie die Aktion **Detaillierte Posten** aus.
6. Wählen Sie den entsprechenden Ausgleichsposten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
7. Füllen Sie die Felder im Kopf aus, und wählen Sie dann die Aktion **Aufheben** aus.  

**Wichtig**: Wenn ein Posten durch mehrere Ausgleichsposten ausgeglichen wurde, müssen Sie zuerst den Ausgleich des letzten Ausgleichspostens aufheben.  

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

