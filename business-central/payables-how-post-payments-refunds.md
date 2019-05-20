---
title: Ausgleichen von Zahlungen mit den entsprechenden Belegen und diese buchen| Microsoft Docs
description: Beschreibt, wie man Zahlungen speichert, die Sie an Kreditoren und Erstattungen leisten, die Sie den Debitoren erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8be7de94b64cb89593df3ea028ab71dddd3d9541
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253976"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Erfassen von Zahlungen und Erstattungen im Zahlungsausgangs Buch.-Blatt

Auf der Seite **Zahlungsjournal** erfassen Sie Zahlungen and Kreditoren und Erstattungen an Debitoren. Wenn Sie eine Zlg Buch.-Blattzeile buchen, wird der zahlende Betrag angegebenen Systembankkonto erfasst. Sie müssen dann die Schritte unternehmen, um die tatsächliche Geldüberweisung aus dem entsprechenden Bankkonto vorzunehmen.  

Das Buch.-Blatt ist ein Fibu Buch.-Blatt, das zum Anwenden von Zahlungen optimiert wird. Sie können Zeilen schnell hinzufügen, können von Kreditorenzahlungen [!INCLUDE[d365fin](includes/d365fin_md.md)] vorschlagen lassen, und Sie können die Zahlung zu gebuchten Belege anwenden. Auch wenn Sie Zahlungen leisten, geben Sie einen positiven Betrag im Feld **Beleg-Betrag** Feld ein. Je nach Belegart für die Buch.-Blattzeile, wird dieser Betrag dann mit einem negativen Betrag in den zugrunde liegenden Transaktionen erstellt. Dieser Weg ist schneller, um Buch.-Blattzeilen manuell hinzufügen. Wenn Sie es vorziehen, negative Beträge einzugeben, können Sie das Buch.-Blatt personalisieren, um das Feld **Betrag** anzuzeigen,  

- Ausgleichen von Zahlungen mit Rechnungen oder Gutschriften

    Wenn Sie das Feld **Ausgleich mit Belegnr.** mit der Rechnung oder Gutschrift eingeben, die bezahlt oder erstattet werden muss, wird der entsprechende Beleg, der bezahlt wird festgelegt, wenn Sie das Buch.-Blatt buchen. Dies wird als Bündelung bezeichnet. Als Alternative zum Anwenden während der Zahlungsbuchung, können Sie die Seite **Kreditorenpostenausgleich** und **Debitorenpostenausgleich** verwenden, nachdem Sie die Zahlungsbuchung erstellt haben. Weitere Informationen finden Sie zum Beispiel unter [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).  

- Vorgeschlagener Zahlungen an Kreditoren oder für Mitarbeiter abrufen.

    Die Funktion **Zahlungsvorschlag** kann helfen **Buch.-Blattzeilen automatisch vorzuschlagen** und zwar entsprechend der Priorisierung automatisch auszufüllen. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md). Mit dieser Funktion wird das Feld **Ausgleich mit Belegnr.** ausgefüllt.  

- Drucken von Schecks und Buchen von Zahlungen elektronisch der Bank übermitteln.

    Zusätzlich zur Erfassung für die Leistung der Zahlung können Sie auch die Seite **Zahlungsausgangs Buch.-Blatt** verwenden, um die Zahlung für die weitere Verarbeitung von Ihrer Bank zu registrieren. Weitere Informationen finden Sie unter [Anwenden von Zahlungen](payables-how-work-checks.md) und [Debitoren-Zahlungen manuell ausgleichen](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>Um Zahlungen im Zahlungsausgangs Buch.-Blatt vornehmen

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungs-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Buch.-Blattnamen, der mit den Zahlungen dediziert ist.
3. Wenn Sie wissen, wie die Zahlung oder Rückerstattung erfolgt, füllen Sie die Felder manuell. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um die Zahlung mit der entsprechenden Rechnung oder Gutschrift auch anzuwenden, aktivieren Sie **Felder Ausgleich. No.** Feld auf der Seite **Kreditorenpostenausgleich** wählen Sie die relevante Rechnung oder die Gutschrift und dann die Schaltfläche **OK** aus.

    Viele Felder, wie die Felder **Dokumentbetrag** und **Fälligkeitsdatum** werden nun mit Informationen aus dem ausgewählten Belegs ausgefüllt.
5. Alternativ nutzen Sie die **Zahlungsvorschlagfunktion**. Alle Informationen und Beträge werden dann auch auf die Buch.-Blattzeilen eingegeben. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

    Nachrichten leiten Sie, um die erforderlichen Felder korrekt auszufüllen.
6.  Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Zahlung per Scheck machen](payables-how-work-checks.md)  
[Elektronische Zahlungen machen ](payables-how-export-payments-bank-file.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
