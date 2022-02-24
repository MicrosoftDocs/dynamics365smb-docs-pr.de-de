---
title: Überblick der Aufgaben zum Verwalten von Debitoren | Microsoft Docs
description: Zeigt auf, wie Debitoren verwaltet werden und ordnet Zahlungen einem Debitor oder Kreditorenposten zu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4d9431ba233f1fa304fab589a3dc85e831e53217
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191907"
---
# <a name="managing-receivables"></a>Debitoren verwalten
Ein regelmäßiger Schritt in jedem Finanzrhythmus ist, Bankkonten abzustimmen, die es erfordern, dass Sie Zahlungen mit Debitoren- oder Kreditorenposten ausgleichen, um Verkaufsrechnungen und - gutschriften zu schließen.

Da die meisten Debitoren in B2B-Umgebung einige Zeit nach der Lieferung bezahlen, lassen Sie die gebuchten Verkaufsrechnungen geöffnet für die Debitorenabteilung, um sie zu beenden, wenn die Zahlung erfolgt. Einige Verkaufsrechnungen können zum Beispiel mit Paypal sofort bezahlt werden. Solche Rechnungen werden sofort folgendermaßen als bezahlt angewendet, wenn sie gebucht werden und werden nicht als Zahlung in der Verarbeitung in AR angezeigt. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist einer der schnellsten Arten, Zahlungen auf der Seite **Zahlungsabstimmungsbuch.-Blatt** zu erfassen, indem Sie eine Bankauszugsdatei oder einen Feed erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten basierend auf Übereinstimmungen zwischen Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können die Suchergebnisse überprüfen und ändern, bevor Sie das Buch.-Blatt buchen, und schließen Bankposten für Posten, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Andere Seiten gibt es, wo Sie entweder Zahlungen anwenden oder Bankkonten abstimmen können:

* Die Seite **Bankkontoabstimmung**, in dem Sie Bankkonten abstimmen, indem Sie Bankkontoauszugszeilen importierten mit Ihren Systembankposten. Hier können Sie auch Scheckzahlungen ausgleichen. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md). Hier können Sie Zahlungen nicht übernehmen.
* Die Seite **Zahlungs-Registrierung**, wo Sie manuell Zahlungseingänge wie Kasse, Scheck oder Bankbuchung für eine generierte Liste der unbezahlten Verkaufsbelegen überprüfen können. Beachten Sie, dass diese Funktionen nur für Verkaufsbelege verfügbar sind. Hier können Sie ausgehende Zahlungen nicht übernehmen, und Sie können keine Bankkonten abstimmen.
* Die Seite **Zahlungseingangsbuch.-Blatt**, indem Sie manuell Belege der relevanten Sachkonten, Debitoren oder anderer Konten durch Eingabe einer Zahlungsposition buchen können. In diesem Fall können Sie entweder den Wareneingang oder die Rückerstattung mit einem oder mehreren offenen Posten anwenden, bevor Sie das Zahlungseingangs Buch.-Blatt buchen, oder Sie können sie aus den erstellten Debitorenposten erstellen. Hier können Sie Bankkonten nicht ausgeglichen.

Die Seiten **Zahlungsabstimmungsbuch.-Blatt** und **Bankkontoabstimmung** verwenden eine automatische Abgleichslogik, die Sie auf der Seite **Zahlungsausgleichsvorschriften** einrichten können. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md).

Andere Aspekte der Verwaltung von Forderungen umfassen die Erfassung offener Salden, einschließlich Zinsrechnungen und Mahnungen und die Einrichtung von Bankkonten, damit Zahlungen von Debitoren automatisch von ihren Konten abgehoben werden können.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

| Aufgabe | Siehe |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Wenden Sie Zahlungen auf offene Debitorenposten basierend auf einer Liste der unbezahlten Verkaufsbelege auf der Seite **Zahlungs-Registrierung** an. |[Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Buchen Sie Zahlungseingänge oder Erstattungen für Debitoren im Zahlungseingangs Buch.-Blatt für Debitorenposten, entweder aus dem Buch.-Blatt oder von gebuchten Posten. |[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md) |
| Erinnern von Debitoren an überfällige Beträge, Berechnen von Zinsen und Gebühren sowie Verwalten von Debitoren |[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md) |
|Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden nur in europäischen Währung einziehen.|[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Sperren Sie einen Debitor, so dass er nicht in Belege oder für das Buchen eingegeben werden kann, zum Beispiel aufgrund von Zahlungsunfähigkeit.|[Debitoren sperren](receivables-how-block-customers.md)|
|Stellen Sie sicher, dass Sie die Kosten der versandten Artikel kennen, indem Sie Artikelkosten wie Fracht, Verladen, Versicherung und Transport kennen, die Ihnen entstehen.|[Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Arbeiten mit Zahlungstoleranzen und Skontotoleranzen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Sagen Sie voraus, wenn Zahlungen für Verkaufsbelege zu spät geleistet werden. | [Die Erweiterung zur Vorhersage verspäteter Zahlungen](ui-extensions-late-payment-prediction.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
