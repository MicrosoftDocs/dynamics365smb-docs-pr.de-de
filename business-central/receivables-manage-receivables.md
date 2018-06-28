---
title: "Überblick der Aufgaben zum Verwalten von Debitoren | Microsoft Docs"
description: Zeigt auf, wie Debitoren verwaltet werden und ordnet Zahlungen einem Debitor oder Kreditorenposten zu.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 01a195130a6834256b30efea8c06841c88af354d
ms.contentlocale: de-de
ms.lasthandoff: 05/15/2018

---
# <a name="managing-receivables"></a>Debitoren verwalten
Ein regelmäßiger Schritt in jedem Finanzrhythmus ist, Bankkonten abzustimmen, die es erfordern, dass Sie Zahlungen mit Debitoren- oder Kreditorenposten ausgleichen, um Verkaufsrechnungen und - gutschriften zu schließen.

Da die meisten Debitoren in B2B-Umgebung einige Zeit nach der Lieferung bezahlen, lassen Sie die gebuchten Verkaufsrechnungen geöffnet für die Debitorenabteilung, um sie zu beenden, wenn die Zahlung erfolgt. Einige Verkaufsrechnungen können zum Beispiel mit Paypal sofort bezahlt werden. Solche Rechnungen werden sofort folgendermaßen als bezahlt angewendet, wenn sie gebucht werden und werden nicht als Zahlung in der Verarbeitung in AR angezeigt. Weitere Informationen finden Sie unter [Rechnungsverkaufsaktivitäten](sales-how-invoice-sales.md).  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist einer der schnellsten Arten, Zahlungen im Fenster **Zahlungsabstimmungsbuch.-Blatt** zu erfassen, indem Sie eine Bankauszugsdatei oder einen Feed erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten basierend auf Übereinstimmungen zwischen Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können die Suchergebnisse überprüfen und ändern, bevor Sie das Buch.-Blatt buchen, und schließen Bankposten für Posten, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Andere Fenster gibt es, wo Sie entweder Zahlungen anwenden oder Bankkonten abstimmen können:

* Das Fenster **Bankkontoabstimmung**, in dem Sie Bankkonten abstimmen, indem Sie Bankkontoauszugszeilen importierten mit Ihren Systembankposten. Hier können Sie auch Scheckzahlungen ausgleichen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md). Hier können Sie Zahlungen nicht übernehmen.
* Das Fenster **Zahlungs-Registrierung**, wo Sie manuell Zahlungseingänge wie Kasse, Scheck oder Bankbuchung für eine generierte Liste der unbezahlten Verkaufsbelegen überprüfen können. Beachten Sie, dass diese Funktionen nur für Verkaufsbelege verfügbar sind. Hier können Sie ausgehende Zahlungen nicht übernehmen, und Sie können keine Bankkonten abstimmen.
* Das Fenster **Zahlungseingangs Buch.-Blatt**, indem Sie manuell Belege der relevanten Sachkonten, Kunden oder anderer Konten durch Eingabe einer Zahlungsposition buchen können. In diesem Fall können Sie entweder den Wareneingang oder die Rückerstattung mit einem oder mehreren offenen Posten anwenden, bevor Sie das Zahlungseingangs Buch.-Blatt buchen, oder Sie können sie aus den erstellten Debitorenposten erstellen. Hier können Sie Bankkonten nicht ausgeglichen.  

Eine andere Aufgabe, wenn Sie Forderungen verwalten ist es, offene Salden zu erfassen und Zinsrechnungen zu verwalten und Mahnungen auszugeben. [!INCLUDE[d365fin](includes/d365fin_md.md)] bietet Möglichkeiten, dies ebenfalls zu tun. Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

| Aufgabe | Siehe |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Ausgleichen von Zahlungen mit offenen Debitorenposten auf Grundlage der manuellen Eingabe in einer Liste von unbezahlten Verkaufsbelegen. |[Debitoren-Zahlungen manuell aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Buchen Sie Zahlungseingänge oder Erstattungen für Debitoren im Zahlungseingangs Buch.-Blatt für Debitorenposten, entweder aus dem Buch.-Blatt oder von gebuchten Posten. |[Debitoren-Zahlungen manuell abstimmen](receivables-how-apply-sales-transactions-manually.md) |
| Erinnern von Debitoren an überfällige Beträge, Berechnen von Zinsen und Gebühren sowie Verwalten von Debitoren |[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md) |
|Stellen Sie sicher, dass Sie die Kosten der versandten Artikel kennen, indem Sie Artikelkosten wie Fracht, Verladen, Versicherung und Transport kennen, die Ihnen entstehen.|[Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Mit Zahlungstoleranzen und Skontotoleranzen arbeiten](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

