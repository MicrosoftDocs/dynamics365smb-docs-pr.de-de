---
title: Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten | Microsoft Docs
description: Kreditorenzahlungen oder Erstattungen manuell verarbeiten, abstimmen oder anpassen und den  Betrag mit einem oder mehreren offenen Kreditorenposten abgleichen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1e7d29d226c0c899a71188bc3ed1036e39939e67
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189987"
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten
Wenn Sie eine Zahlung an einen Kreditor senden oder eine Erstattung von einem Kreditor erhalten, müssen Sie entscheiden, ob die Zahlung oder die Rückerstattung mit einem oder mehreren offenen Posten ausgeglichen werden soll. Sie können den genauen Betrag zum Ausgleichen der Zahlung oder der Rückerstattung angeben und dann die Kreditorenposten nur teilweise ausgleichen. Sie müssen alle Kreditorenposten ausgleichen, um eine korrekte Kreditorenstatistik und Berichte der Kontoauszüge und Zinsrechnungen zu erhalten.

> [!NOTE]  
>   Kreditoren erteilen gelegentlich eine Zahlungsrückerstattung anstelle einer Gutschrift, die mit zukünftigen Rechnungen verrechnet wird, insbesondere wenn bereits bezahlte Artikel zurückgeben werden oder ein zu hoher Betrag für eine Rechnung gezahlt wurde.

Sie können Kreditorenposten auf drei verschiedene Arten übernehmen:

* Durch die Eingabe von Informationen auf speziellen Seiten, wie die Seite **Zahlungsausgangs Buch.-Blatt** und die Seite **Zahlungsabstimmungsbuch.-Blatt**.
* Aus Einkaufsgutschriften.
* Kreditorposten nach Einkaufsbelegen werden gebucht aber nicht angewendet.

> [!NOTE]  
>   Wenn das Feld **Ausgleichsmethode** auf der Kreditorenkarte **Auf älteste anwenden** enthält, dann wird die Zahlung automatisch mit der ältesten offenen Rechnung abgeglichen, wenn Sie nicht explizit angeben, auf welchen Habenposten sie sich bezieht. Ist die Ausgleichsmethode eines Debitors auf **Manuell** festgelegt, müssen die Posten manuell ausgeglichen werden.

Sie können Kreditorenzahlungen manuell auf die entsprechenden Einkaufsbelege anwenden, wenn Sie die Zahlungen auf der **Zahlung Buch.-Blatt**-Seite buchen. Informationen zum Ausfüllen des Zahlungsausgangs Buch.-Blattes, finden Sie in [Vorgehensweise: Anwenden von Zahlungen](payables-make-payments.md).

Sie können Kreditorenzahlungen und Debitorenzahlungen anwenden nachdem die Zahlungen als negative Banktransaktionen in Ihrer Bank erscheinen. Auf der **Zahlungs-Abstimmungs-Buch.-Blatt**-Seite können Sie Funktionen für den Bankkontoauszugsimport, die automatische Anwendung und die Bankkontoabstimmung verwenden. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>So gleichen Sie eine Zahlung mit einem einzelnen Kreditorenposten aus
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Zahlungsausgangs Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie auf der Seite **Zahlung Buch.-Blatt** in der ersten Buchungsblattzeile die entsprechenden Informationen zu dem Zahlungsposten ein.
3. So gleichen Sie gebuchte Kreditorenposten aus:
   1. Im Feld **Ausgleich mit Belegnr.** wählen Sie das Feld aus, um die Seite **Kreditorenpostenausgleich** zu öffnen.
   2. Wählen Sie auf der Seite **Kreditorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
   3. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.
4. Oder gleichen Sie gebuchte Kreditorenposten aus:

   1. Wählen Sie die Aktion **Posten ausgleichen...** aus.
   2. Wählen Sie auf der Seite **Kreditorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
   3. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.  
   4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

      Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand der Seite **Kreditorenpostenausgleich** sehen Sie einen Betrag im Feld Ausgleichsbetrag. Sie sehen, ob die Buchung ausgeglichen ist.
5. Wählen Sie die Schaltfläche **OK** aus.
6. Wählen Sie die Aktion **Buchen**, um das Buch.-Blatt zu buchen.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>So gleichen Sie eine Gutschrift mit mehreren Kreditorenposten aus
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Einkaufsgutschrift** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Gutschrift, die Sie ausgleichen möchten.
3. Geben Sie die relevanten Informationen in der Kopfzeile ein.
4. Um einen einzelnen Kreditorenposten, im Inforegister **Ausgleich**, im Feld **Ausgleich mit Belegnr.** Feld auszugleichen, wählen Sie den Posten aus auf den die Gurtschrift anzuwenden ist, und wählen Sie dann im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.
5. Oder gleichen Sie gebuchte Kreditorenposten aus:

   1. Wählen Sie die Aktion **Posten ausgleichen...** aus.
   2. Wählen Sie die Zeilen mit den Posten aus, auf die die Gutschrift anzuwenden ist.
   3. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.  
   4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

       Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand der Seite **Kreditorenpostenausgleich** sehen Sie einen Betrag im Feld **Ausgleichsbetrag**. Sie sehen, ob die Buchung ausgeglichen ist.
6. Wählen Sie die Schaltfläche **OK** aus.  
   Die Seite **Einkaufsgutschrift** zeigt den im Feld **Auf Dokumenttyp anwenden** und auf **Ausgleich mit Belegart** ausgewählten Eintrag an. Die Seite zeigt auch den Betrag der zu buchenden Gutschrift an, wobei gegebenenfalls Skonti berücksichtigt werden.
7. Wählen Sie die Schaltfläche **Buchen**, um die Gutschrift zu buchen.

## <a name="to-apply-posted-vendor-ledger-entries"></a>So gleichen Sie gebuchte Kreditorenposten aus
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den relevanten Kreditor mit bereits gebuchten Posten.
3. Wählen Sie die **Posten**-Aktion aus, und wählen Sie dann die **Posten ausgleichen**-Aktion aus.
4. Auf der Seite **Kreditorenpostenausgleich** werden die offenen Posten des Kreditors angezeigt.
5. Wählen Sie die Zeile mit dem Posten, den Sie ausgleichen möchten.
6. Wählen Sie die Aktion **Ausgleichs-ID setzen** aus.

    Das Feld **Ausgleichs-ID** zeigt drei Sternchen (***), wenn Sie in einem Einbenutzersystem arbeiten, oder Ihre Benutzer-ID, wenn Sie in einem Mehrbenutzersystem arbeiten.  
7. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.

    Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen. Am unteren Rand der Seite **Kreditorenpostenausgleich** sehen Sie den Betrag im Feld **Ausgleichsbetrag**.
8. Wählen Sie die Aktion **Ausgleich buchen** aus.  

    Die Seite **Ausgleich buchen** wird mit der Belegnummer des Ausgleichspostens und dem Buchungsdatum des Postens geöffnet, der das aktuellste Buchungsdatum aufweist.
9. Klicken Sie auf die Schaltfläche **OK**, um den Ausgleich zu buchen.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>So wenden Sie Kreditorenposten in unterschiedlichen Währungen aufeinander an
Falls Sie Käufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit der Rechnung ausgleichen.

Wenn Sie einen Posten (Posten 2) in einer Währung mit einem Posten (Posten 1) in einer anderen Währung ausgleichen, wird das Buchungsdatum von Posten 1 verwendet, um den entsprechenden Wechselkurs zur Umrechnung der Beträge von Posten 2 zu ermitteln. Den Wechselkurs finden Sie auf der Seite **Währungswechselkurse**. In diesem Fall müssen Sie die Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren. Weitere Informationen finden Sie unter [Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Zahlungsausgangs Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie das gewünschte Buch.-Blatt, und füllen Sie unter Verwendung eines Währungscodes die erste Zeile aus.
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.
4. Klicken Sie auf die Zeile mit dem Posten, mit dem Sie den Posten im Zahlungsausgangs Buch.-Blatt. ausgleichen möchten. Klicken Sie dann auf **Ausgleichs-ID festlegen** und wählen Sie den auszugleichenden Posten aus.
5. Wählen Sie die Schaltfläche **OK**, um zum Zahlungsausgangsbuchungsblatt zurückzukehren.
6. Buchen Sie das Zahlungsausgangs Buch.-Blatt.

> [!IMPORTANT]  
>   Wenn Sie Posten in verschiedenen Währungen miteinander ausgleichen, rechnet die Anwendung die Beträge in USD um. Selbst wenn der Wechselkurs fest ist, z. B. zwischen USD und EUR, kann es zu Rundungsdifferenzen kommen, wenn diese Fremdwährungsbeträge in EUR umgerechnet werden. Diese Rundungsdifferenzen werden als Gewinne und Verluste auf die Konten gebucht, die in den Feldern **Kursgewinn realisiert** oder **Kursverlust realisiert** der Seite **Währungen** angegeben sind. Außerdem werden die Beträge im Feld **Betrag (EUR)** der entsprechenden Kreditorenposten angepasst.

## <a name="to-unapply-an-application-of-vendor-entries"></a>So heben Sie den Ausgleich von Kreditorenposten auf
Wenn Sie einen fehlerhaften Ausgleich aufheben, wird ein Korrekturposten (ein Posten, der mit dem ursprünglichen Posten identisch ist, im Betragsfeld allerdings ein umgekehrtes Vorzeichen aufweist) für alle Posten erstellt und gebucht, einschließlich aller aus dem Ausgleich abgeleiteten Fibu-Buchungen, z. B. Skonto und Währungsgewinne/-verluste. Die von der Anwendung geschlossenen Posten werden erneut geöffnet.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die relevante Kreditorenkarte.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie den entsprechenden Posten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
5. Wählen Sie die Aktion **Detaillierte Posten** aus.
6. Wählen Sie den entsprechenden Ausgleichsposten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
7. Füllen Sie die Felder im Kopf aus, und wählen Sie dann die Aktion **Aufheben** aus.

> [!IMPORTANT]  
>   Wenn ein Posten durch mehrere Ausgleichsposten ausgeglichen wurde, müssen Sie zuerst den Ausgleich des letzten Ausgleichspostens aufheben.

## <a name="see-also"></a>Siehe auch
[Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
