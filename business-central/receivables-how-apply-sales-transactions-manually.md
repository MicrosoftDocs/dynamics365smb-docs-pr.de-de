---
title: Abgleichen von Debitorenzahlungen mit dem Zahlungseingangsjournal oder mit Debitorenposten
description: Ordnen Sie Bareingänge oder Rückerstattungen von Kunden einem oder mehreren offenen Debitorenposten zu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Abgleichen von Debitorenzahlungen mit einem Zahlungseingangsjournal oder aus Debitorenposten

Wenn Sie von einem Kunden eine Barzahlung erhalten oder eine Rückerstattung in bar leisten, können Sie die Zahlung oder Rückerstattung zum Schließen offener Soll- oder Habenbeträge verwenden. Sie können den Betrag angeben, den Sie anwenden möchten. Beispielsweise können Sie Teilzahlungen für die Debitorenposten übernehmen. Der Abschluss von Kundenbucheinträgen hält Debitorenstatistiken, Kontoauszüge, Finanzierungskosten usw. auf dem neuesten Stand.

> [!TIP]  
> Auf der Seite **Debitorenposten** bedeutet die rote Schriftart, dass die entsprechende Zahlung nach dem Fälligkeitsdatum liegt. Wenn fällige Zahlungen ein Problem werden, können wir Ihnen dabei helfen, die Häufigkeit zu verringern. Sie können die Funktionen **Zahlungsverzug-Vorhersagen** Erweiterung aktivieren, die ein vorbestimmtes Modell verwendet, das wir in Azure Machine Learning erstellten, um die zeitliche Steuerung der Zahlungen vorauszusagen. Diese Vorhersagen helfen Ihnen, ausstehende Forderungen zu reduzieren und die Sammlungsstrategie abzustimmen. Wenn beispielsweise vorausgesagt wird, dass eine Zahlung zu spät erfolgen wird, können Sie sich entschieden, die Zahlungsfristen oder die Zahlungsform für den Debitor anzupassen. Weitere Informationen finden Sie unter [Vorhersage verspätete Zahlung](ui-extensions-late-payment-prediction.md).  

Sie können Debitorenposten auf mehrere Arten übernehmen:

* Geben Sie auf den folgenden Seiten Informationen ein:
   * Die Seite **Zahlungsabstimmungsbuch.-Blatt**. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).
   * Die Seite **Zahlungsregistrierung**. Weitere Informationen finden Sie unter [Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)
   * Die Seite  **Bargeldeingangsjournal** . Weitere Informationen finden Sie unter  [So füllen Sie ein Kassenbonjournal aus und buchen es](#to-fill-and-post-a-cash-receipt-journal).
* Durch das Ausfüllen des Felds **Ausgleich mit Belegnr.** in Verkaufsgutschriftsbelegen. Weitere Informationen finden Sie unter  [So wenden Sie eine Gutschrift auf einen einzelnen Debitorenposten an](#to-apply-a-credit-memo-to-a-single-customer-ledger-entry).
* Mit der **Ausgleichs-ID setzen**-Aktion in Debitorenposten. Weitere Informationen finden Sie unter  [So wenden Sie eine Zahlung auf einen einzelnen Debitorenposten an](#to-apply-a-payment-to-a-single-customer-ledger-entry).
* Indem Sie die Aktion **Buchungen zuweisen** auf der Seite **Bankeinzahlung** verwenden und dann die Rechnungsnummer in das Feld **Gilt für ID** eingeben. Weitere Informationen finden Sie unter [Bankeinzahlungen erstellen](bank-create-bank-deposits.md).

> [!NOTE]  
> Wenn das Feld **Ausgleichsmethode** auf der Debitorenkarte **Auf älteste anwenden** festgelegt ist, dann wird die Zahlung automatisch mit der ältesten offenen Rechnung abgeglichen, wenn Sie nicht explizit manuell einen Eintrag definieren. Ist die Ausgleichsmethode eines Debitors auf **Manuell** festgelegt, müssen die Posten immer manuell ausgeglichen werden.

## So füllen Sie ein Zahlungseingangs Buch.-Blatt aus und buchen dieses

Ein Zahlungseingangs Buch.-Blatt ist eine Art allgemeines Journal. Sie können damit Transaktionen auf Sach-, Bank-, Debitoren-, Kreditoren- und Anlagekonten buchen. Daher können Sie die Zahlungen beim Buchen auf einen oder mehrere Sollposten anwenden. Sie können sich auch später aus den veröffentlichten Einträgen bewerben.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungseingangs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Wählen Sie im Feld **Buch.-Blattname** das relevante Buch.-Blatt aus.
4. Füllen Sie das Feld **Buchungsdatum** aus.  
5. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.

    Das Feld **Belegnr.** wird anhand der Nummernserie ausgefüllt, die dem Buch.-Blatt zugeordnet wurde.  
6. Verwenden Sie das Feld **Externe Belegnummer**, um eine Kennung wie die Schecknummer des Debitors, zu speichern.

   > [!NOTE]
   > Standardmäßig ist das Feld „Externe Dokumentnummer“ ausgeblendet. Wenn dies der Fall ist und Sie es verwenden möchten, können Sie es mithilfe der Personalisierung hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsplatz](ui-personalization-user.md).

7. Wählen Sie im Feld **Kontoart** die Option **Debitor** aus.
8. Wählen Sie im Feld  **Kontonr.**  den Kunden aus.
9. Um die Anwendung gleichzeitig mit dem Journal zu buchen, füllen Sie die folgenden Felder aus:
   1. Wählen Sie im Feld **Gegenkontoart** das **Sachkonto** für Barzahlungen und das **Bankkonto** für sonstige Zahlungen aus.
   2. Wählen Sie im Feld **Gegenkontonr.** das Barkonto für Barzahlungen oder das zutreffende Bankkonto für sonstige Zahlungen aus.
10. Buchen Sie die Buch.-Blattzeile.

## So gleichen Sie einen einzelnen Debitorenposten mit einer Zahlung aus:

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie  **Barzahlungseingangsjournal** ein und wählen Sie den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Debitor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Im Feld **Ausgleich mit Belegnr.** wählen Sie das Feld aus, um die Seite **Debitorenpostenausgleich** zu öffnen.
8. Wählen Sie auf der Seite **Debitorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
9. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
10. Wählen Sie die Schaltfläche **OK**. Die Seite **Zahlungseingangsbuch.-Blatt** zeigt nun die Einträge unter **Ausgleich mit Belegart** und auf **Ausgleich mit Belegnr.**.
11. Buchen Sie das Zahlungseingangs Buch.-Blatt.

## So gleichen Sie mehrere Debitorenposten mit einer Zahlung aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungseingangs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Debitor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Geben Sie im Feld **Betrag** die vollständige Zahlung als negativen Betrag ein.
8. Wenn Sie die Zahlung bei der Buchung mit mehreren Debitorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.  
9. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.  
10. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
11. Wählen Sie die Schaltfläche **OK** aus.
12. Buchen Sie das Zahlungseingangs Buch.-Blatt.

## So gleichen Sie einen einzelnen Debitorenposten mit einer Gutschrift aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie beim Buchen einen einzelnen Debitorenposten mit einer Gutschrift ausgleichen möchten, klicken Sie auf das Inforegister **Anwendung im Feld** , und wählen Sie den Posten, den Sie mit der Zahlung ausgleichen möchten.
4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.  

    Wenn Sie keinen Betrag eingeben, wird die Anwendung automatisch mit dem Höchstbetrag angewendet. Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
5. Wählen Sie die Schaltfläche **OK**. Auf der Seite  **Verkaufsgutschrift**  wird jetzt der Eintrag angezeigt, den Sie in den Feldern  **Gilt für Belegtyp**  und  **Gilt für Belegnr.**  ausgewählt haben. Und den Betrag der zu buchenden Gutschrift an, wobei mögliche Skonti berücksichtigt werden.
6. Buchen Sie die Gutschrift.

## So gleichen Sie mehrere Debitorenposten mit einer Gutschrift aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie die Zahlung bei der Buchung mit mehreren Debitorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.
4. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.
5. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
6. Wählen Sie die Schaltfläche **OK** aus. Die Seite **Verkaufsgutschrift** zeigt nun den Betrag der zu buchenden Gutschrift an, wobei gegebenenfalls Skonto berücksichtigt wird.
7. Buchen Sie die Gutschrift.

## So gleichen Sie gebuchte Debitorenposten aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Debitorenkarte für den Debitor mit den Posten, die Sie ausgleichen möchten.
3. Wählen Sie die Aktion  **Hauptbucheinträge**  und anschließend die Zeile mit dem Eintrag aus, der der Ausgleichseintrag ist.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus. Auf der Seite **Debitorenpostenausgleich** werden die offenen Posten für den Debitor angezeigt.
5. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**. Aktion
6. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand der Seite **Debitorenpostenausgleich** wird im Feld **Ausgleichsbetrag** der spezifische Betrag angezeigt.  
7. Wählen Sie die Aktion **Ausgleich buchen** aus. Die Seite **Ausgleich buchen** wird mit der Belegnummer des Ausgleichspostens und dem Buchungsdatum des Postens angezeigt, der das aktuellste Buchungsdatum aufweist.  
8. Klicken Sie auf die Schaltfläche **OK**, um den Ausgleich zu buchen.

    Wenn der gebuchte Ausgleich geschlossene Debitorenposten zur Folge hatte, wird das Feld  **Offen**  für diese Posten gelöscht.  
9. Um die Sachkonto-Einträge zu sehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link. Wechseln Sie zur Karte für den jeweiligen Debitor, um die Buchungsposten zu sehen.  

Sie können in der Liste der Posten sehen, dass in der Zeile mit dem vollständig ausgeglichenen Posten das Feld **Offen** nicht aktiviert ist.  

> [!NOTE]  
> Nachdem Sie auf der Seite **Debitorenpostenausgleich** einen Posten oder mehrere Posten durch **Festlegen der Ausgleichs-ID** ausgewählt haben, enthält das Feld **Ausgleichsbetrag** die Summe der Restbeträge für die ausgewählten gebuchten Posten, es sei denn, das Feld enthält bereits Informationen. Wenn Sie **Auf Älteste Anwenden** im Feld **Anwendungsmethode** auf der Debitorenkarte auswählen, tritt die Anwendung automatisch auf.

## So gleichen Sie Debitorenposten in verschiedenen Währungen untereinander aus:

Wenn Sie an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie dennoch die Rechnung mit der Zahlung ausgleichen.  

Im Folgenden finden Sie ein Beispiel. Sie wenden Eintrag A in einer Währung auf Eintrag B in einer anderen Währung an. Das Buchungsdatum von Eintrag A wird verwendet, um den Wechselkurs zu ermitteln, der zum Umrechnen der Beträge von Eintrag B verwendet wird. Der Wechselkurs ist auf der Seite  **Wechselkurse**  zu finden.  

Das Ausgleichen von Debitorenposten in verschiedenen Währungen muss aktiviert sein. Weitere Informationen finden Sie unter [ Anwendung von Debitorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zlg.-Eing. Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie das gewünschte Buch.-Blatt, und füllen Sie unter Verwendung eines Währungscodes die erste Zeile aus.
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.
4. Klicken Sie auf die Zeile mit dem Posten, mit dem Sie den Posten im Zahlungsausgangs-Buch.-Blatt ausgleichen möchten. Klicken Sie dann auf **Ausgleichs-ID festlegen** und wählen Sie den auszugleichenden Posten aus.
5. Wählen Sie die Schaltfläche **OK**, um zum Barzahlungseingangsbuch zurückzukehren.
6. Buchen Sie das Verkaufs Buch.-Blatt.  

> [!IMPORTANT]  
>   Wenn Sie Posten in verschiedenen Währungen miteinander ausgleichen, rechnet die Anwendung die Beträge in USD um. Selbst wenn der Wechselkurs fest ist, z. B. zwischen USD und EUR, kann es zu Rundungsdifferenzen kommen, wenn diese Fremdwährungsbeträge in USD umgerechnet werden. Diese Rundungsdifferenzen werden als Gewinne und Verluste auf die Konten gebucht, die in den Feldern **Kursgewinn realisiert** oder **Kursverlust realisiert** der Seite **Währungen** angegeben sind. Außerdem werden die Beträge im Feld **Betrag (USD)** der entsprechenden Debitorenposten angepasst.  

## So heben Sie den Ausgleich von Debitorenposten auf
Wenn Sie einen Antrag korrigieren, werden Korrekturbuchungen für alle Buchungen erstellt und gebucht. Die Korrektureinträge sind die gleichen wie die Originale, haben aber ein entgegengesetztes Protokoll im **Menge**-Bereich. Die Korrekturbuchungen umfassen alle aus der Anwendung abgeleiteten Hauptbucheinträge. Zum Beispiel Skonto und Währungsgewinne/-verluste. Die von der Anwendung geschlossenen Einträge werden wieder geöffnet.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die relevante Debitorenkarte.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie den entsprechenden Posten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
5. Wählen Sie die Aktion **Detaillierte Posten** aus.
6. Wählen Sie den entsprechenden Ausgleichsposten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
7. Füllen Sie die Felder im Kopf aus, und wählen Sie dann die Aktion **Aufheben** aus.  

> [!IMPORTANT]  
>   Wenn ein Eintrag durch mehr als einen Anwendungseintrag angewendet wurde, müssen Sie den letzten Anwendungseintrag zuerst rückgängig machen.  

## Weitere Informationen
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]