---
title: "Überblick der Aufgaben zum Verwalten von Zahlungen an Debitoren | Microsoft Docs"
description: "Gliederungen ihm eine Arbeit, um Zahlungen an Kreditoren oder zu den Gläubigern, einschließlich Buchungszahlungszeilen und das Anzeigen einer Übersicht über den fälligen Saldo zu verwalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 6cd7b9922f047d05a2cc37a9157de47221f67a7f
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="making-payments"></a>Zahlungen vornehmen
Wenn Sie Zahlungen an Kreditoren leisten, buchen Sie die jeweiligen Zahlungszeilen im **Zahlungsausgangs Buch.-Blatt**-Fenster. Verwenden Sie zum Suchen fälliger Zahlungen im Zahlungsausgangs Buch.-Blatt die Funktion **Zahlungsvorschlag**. Darüber hinaus können Sie sich mithilfe des Berichts **Kreditor - Saldo nach Perioden** einen Überblick über die fälligen Zahlungen verschaffen.

Im Zahlungsausgangs Buch.-Blatt können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen. Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, dann müssen alle Posten für Schecks gedruckt werden, damit die Buch.-Blattzeilen gebucht werden können.

Wenn Zahlungen gebucht werden, exportieren Sie sie in eine Bankdatei für den Upload zu Ihrer Bank zur Verarbeitung.

Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in den entsprechenden offenen Kreditorenposten ausgleichen. Sie können dies manuell oder über den Import in eine Bankkontoauszugsdatei und das Automatische Ausgleichen der Zahlungen durchführen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

| Aufgabe | Siehe |
| --- | --- |
|Verwenden Sie das Fenster **Zahlungsausgangs Buch.-Blatt**, das auf dem Fibu Buch.-Blatt basiert, um Zahlungen an Kreditoren oder für Mitarbeiter zu buchen.|[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)|
| Verwenden Sie die Funktion, um Kreditorenzahlungen entsprechend gewählten Kriterien, wie Fälligkeitsdatum, Skontoeignung und Ihrer Liquidität vorzuschlagen. |[Vorgehensweise: Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md) |
|Erstatten Sie Mitarbeitern persönliche Ausgaben für die Geschäftsaktivitäten zurück, indem Sie Zahlung zu dem Bankkonto vornehmen.|[Vorgehensweise: Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen](finance-how-record-reimburse-employee-expenses.md)|
| Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus. Annullieren Sie Schecks vor oder nach dem Buchen. |[So gehts: Arbeiten mit Schecks](payables-how-work-checks.md) |
| Bezahlen Sie den Kreditor bar oder mit Scheck und buchen Sie die Zahlung, wenn Sie die Rechnung buchen. |[Vorgehensweise: Sofortiges Ausgleichen von Einkaufsrechnungen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. |[Erneuter Positive Pay-Export in Datei](finance-how-positive-pay.md) |
|Exportzahlungen aus dem **Zahlungsausgangs Buch.-Blatt** in eine Bank archivieren, das Sie für Ihre Bank für das Verarbeiten hochladen, einschließlich EFT (elektronischer Geldtransfer) in Nordamerika. |[Vorgehensweise: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md)|
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|    

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

