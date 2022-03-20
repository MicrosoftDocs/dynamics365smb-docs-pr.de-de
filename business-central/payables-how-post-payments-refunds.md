---
title: Erfassen von Zahlungen und Rückerstattungen im Zahlungsausgangs Buch.-Blatt
description: Lesen Sie auf der Seite Zahlungsausgangs Buch.-Blätter nach, wie Sie Zahlungen an Kreditoren und Rückerstattungen an Debitoren erfassen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP
ms.search.form: 256, 233, 624, 1228
ms.date: 07/09/2021
ms.author: edupont
ms.openlocfilehash: fa43027481ba7b9eb970182eb62b5e2aa728fb06
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367255"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Erfassen von Zahlungen und Erstattungen im Zahlungsausgangs Buch.-Blatt

Auf der Seite **Zahlungsjournal** erfassen Sie Zahlungen and Kreditoren und Erstattungen an Debitoren. Wenn Sie eine Zlg Buch.-Blattzeile buchen, wird der zahlende Betrag angegebenen Systembankkonto erfasst. Sie müssen dann die Schritte unternehmen, um die tatsächliche Geldüberweisung aus dem entsprechenden Bankkonto vorzunehmen.  

Das Buch.-Blatt ist ein Fibu Buch.-Blatt, das zum Anwenden von Zahlungen optimiert wird. Sie können Zeilen schnell hinzufügen, können von Kreditorenzahlungen [!INCLUDE[prod_short](includes/prod_short.md)] vorschlagen lassen, und Sie können die Zahlung zu gebuchten Belege anwenden. Auch wenn Sie Zahlungen leisten, geben Sie einen positiven Betrag im Feld **Beleg-Betrag** Feld ein. Je nach Belegart für die Buch.-Blattzeile, wird dieser Betrag dann mit einem negativen Betrag in den zugrunde liegenden Transaktionen erstellt. Dieser Weg ist schneller, um Buch.-Blattzeilen manuell hinzufügen. Wenn Sie es vorziehen, negative Beträge einzugeben, können Sie das Buch.-Blatt personalisieren, um das Feld **Betrag** anzuzeigen,  

- Ausgleichen von Zahlungen mit Rechnungen oder Gutschriften

    Wenn Sie das Feld **Ausgleich mit Belegnr.** mit der Rechnung oder Gutschrift eingeben, die bezahlt oder erstattet werden muss, wird der entsprechende Beleg, der bezahlt wird festgelegt, wenn Sie das Buch.-Blatt buchen. Dies wird als Bündelung bezeichnet. Als Alternative zum Anwenden während der Zahlungsbuchung, können Sie die Seite **Kreditorenpostenausgleich** und **Debitorenpostenausgleich** verwenden, nachdem Sie die Zahlungsbuchung erstellt haben. Weitere Informationen finden Sie zum Beispiel unter [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).  

- Vorgeschlagener Zahlungen an Kreditoren oder für Mitarbeiter abrufen.

    Die Funktion **Zahlungsvorschlag** kann helfen **Buch.-Blattzeilen automatisch vorzuschlagen** und zwar entsprechend der Priorisierung automatisch auszufüllen. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md). Mit dieser Funktion wird das Feld **Ausgleich mit Belegnr.** ausgefüllt.  

- Drucken von Schecks und Buchen von Zahlungen elektronisch der Bank übermitteln.

    Zusätzlich zur Erfassung für die Leistung der Zahlung können Sie auch die Seite **Zahlungsausgangs Buch.-Blatt** verwenden, um die Zahlung für die weitere Verarbeitung von Ihrer Bank zu registrieren. Weitere Informationen finden Sie unter [Anwenden von Zahlungen](payables-how-work-checks.md) und [Debitoren-Zahlungen manuell ausgleichen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Um Zahlungen im Zahlungsausgangs Buch.-Blatt vornehmen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den Buch.-Blattnamen, der mit den Zahlungen dediziert ist.
3. Wenn Sie wissen, wer zu bezahlen ist, füllen Sie die Felder manuell aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um die Zahlung mit der entsprechenden Rechnung oder Gutschrift auch anzuwenden, aktivieren Sie **Felder Ausgleich. No.** Feld auf der Seite **Kreditorenpostenausgleich** wählen Sie die relevante Rechnung oder die Gutschrift und dann die Schaltfläche **OK** aus.

    Viele Felder, wie die Felder **Dokumentbetrag** und **Fälligkeitsdatum** werden nun mit Informationen aus dem ausgewählten Belegs ausgefüllt.
5. Alternativ nutzen Sie die **Zahlungsvorschlagfunktion**. Alle Informationen und Beträge werden dann auch auf die Buch.-Blattzeilen eingegeben. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

    Nachrichten leiten Sie, um die erforderlichen Felder korrekt auszufüllen.
6. Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.


## <a name="to-issue-a-refund-check"></a>So stellen Sie einen Scheck zur Rückerstattung aus

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsjournale** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Feld **Belegart** die Option **Rückerstattung**.  
3. Verwenden Sie im Feld **Externe Belegnummer** diese als Referenz für den Rückerstattungsscheck (z.B. Rücklieferungs-Bestellnummer).  
4. Wählen Sie im Feld **Kontoart** die Option **Debitor** aus.  
5. Wählen Sie im Feld **Konto-Nr.** die Kontonummer des Debitors, auf den der Scheck für die Rückerstattung ausgestellt wird.  
6. Geben Sie im Feld **Betrag** den zu erstattenden Betrag ein.  
7. Wählen Sie im Feld **Gegenkonto-Typ** die Option **Bankkonto**.  
8. Wählen Sie im Feld **Gegenkonto-Nr.** das Bankkonto aus, von dem der Scheck stammen soll.  
9. Wählen Sie im Feld **Gilt für Beleg. Nr.** wählen Sie die Belege aus, die eine Rückerstattung erfordern.  
10. Wenn alle Zeilen des Zahlungsausgangs Buch.-Blatt abgeschlossen sind, wählen Sie die Aktion **Buchen/Drucken**, dann die Aktion **Buchen und Drucken** und wählen **Ja**.  
  

## <a name="see-also"></a>Weitere Informationen
[Zahlung per Scheck machen](payables-how-work-checks.md)  
[Elektronische Zahlungen vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
