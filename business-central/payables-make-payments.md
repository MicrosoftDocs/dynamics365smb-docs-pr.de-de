---
title: Überblick der Aufgaben zum Verwalten von Zahlungen an Kreditoren | Microsoft Docs
description: Gliederungen ihm eine Arbeit, um Zahlungen an Kreditoren oder zu den Gläubigern, einschließlich Buchungszahlungszeilen und das Anzeigen einer Übersicht über den fälligen Saldo zu verwalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 99da82d54a2e769c2ebbaf7d4c103791119517d9
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076462"
---
# <a name="making-payments"></a>Zahlungen vornehmen

Wenn Sie Zahlungen an Kreditoren oder Debitoren leisten oder Ihre Mitarbeiter entschädigen, buchen Sie die jeweiligen Zahlungszeilen auf der **Zahlungsausgangs Buch.-Blatt**-Seite. Das Buch.-Blatt ist ein Fibu Buch.-Blatt, das zum Anwenden von Zahlungen optimiert wird und enthält mehrere leistungsstarke Funktionen wie die **Zahlungsvorschlag** Funktion einfügen, welche Kreditorenzahlungen, die fällig sind und den **Kreditor - Saldo nach Perioden** Bericht findet, der einen Überblick über die fälligen Kreditorenzahlungen anzeigt.  

Sie können den Vorgang des Leistens der Zahlung aus Listen, den Karten und der Posten für Debitoren, Kreditoren und Mitarbeiter starten. Jede der Seiten hat eine Schaltfläche, die den Zahlungsstrom startet und die Ihnen dabei hilft, das Zahlungsausgangs Buch.-Blatt ausfüllen.  

Im Zahlungsausgangs Buch.-Blatt können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen. Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, dann müssen alle Posten für Schecks gedruckt werden, damit die Buch.-Blattzeilen gebucht werden können.

Wenn Zahlungen gebucht werden, exportieren Sie sie in eine Bankdatei für den Upload zu Ihrer Bank zur Verarbeitung.

Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in den entsprechenden offenen Kreditorenposten ausgleichen. Sie können dies manuell oder über den Import in eine Bankkontoauszugsdatei und das Automatische Ausgleichen der Zahlungen durchführen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| An | Siehe |
| --- | --- |
|Verwenden Sie die Seite **Zahlungsausgangs Buch.-Blatt**, das auf dem Fibu Buch.-Blatt basiert, um Zahlungen an Kreditoren oder für Mitarbeiter zu buchen.|[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)|
|Buchen Sie Zahlungen an Kreditoren oder Mitarbeiter und Erstattungen an Debitoren und wenden Sie optional die Zahlungen für die verwandten unbezahlten Rechnungen/Gutschriften an, um sie als bezahlt abzuschließen.|[Zahlungsbelege und Erstattungen](payables-how-post-payments-refunds.md)|
| Verwenden Sie die Funktion auf der Seite **Kreditorenzahlungen** um Kriterien, wie Fälligkeitsdatum, Skontoeignung und Ihrer Liquidität vorzuschlagen. |[Zahlungsvorschlag](payables-how-suggest-vendor-payments.md) |
| Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus. Annullieren Sie Schecks vor oder nach dem Buchen. |[Zahlung per Scheck machen](payables-how-work-checks.md) |
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Bezahlen Sie einen Kreditor bar oder mit Scheck und buchen Sie die Zahlung, wenn Sie die Rechnung buchen. |[Einkaufsrechnungen sofort ausgleichen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. |[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md) |

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
