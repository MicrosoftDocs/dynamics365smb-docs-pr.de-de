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
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3ffd3b31dcef871ceb30eae6a041f68a4972b2cb
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="managing-receivables"></a>Debitoren verwalten
Ein regelmäßiger Schritt in jedem Finanzrhythmus ist, Bankkonten abzustimmen, die es erfordern, dass Sie Zahlungen mit Debitoren- oder Kreditorenposten ausgleichen, um Verkaufsrechnungen und - gutschriften zu schließen.  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist einer der schnellsten Arten, Zahlungen im Fenster **Zahlungsabstimmungsbuch.-Blatt** zu erfassen, indem Sie eine Bankauszugsdatei oder einen Feed erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten basierend auf Übereinstimmungen zwischen Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können die Suchergebnisse überprüfen und ändern, bevor Sie das Buch.-Blatt buchen, und schließen Bankposten für Posten, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Es gibt jedoch andere praktische Orte, um Zahlungen zu übernehmen und Bankkonten auszugleichen:  

* Im Fenster **Bankkontoabstimmung** können Sie ebenfalls Einträge prüfen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).  
* Das Fenster **Zahlungs-Registrierung**, indem Sie manuell Zahlungseingänge wie Kasse, Scheck oder Bankbuchung für eine generierte Liste der unbezahlten Verkaufsbelegen überprüfen können. Beachten Sie, dass diese Funktionen nur für Verkaufsbelege verfügbar sind.  
* Das Fenster **Zahlungseingangs Buch.-Blatt**, indem Sie manuell Belege der relevanten Sachkonten, Kunden oder anderer Konten durch Eingabe einer Zahlungsposition buchen können. In diesem Fall können Sie entweder den Wareneingang oder die Rückerstattung mit einem oder mehreren offenen Posten anwenden, bevor Sie das Zahlungseingangs Buch.-Blatt buchen, oder Sie können sie aus den erstellten Debitorenposten erstellen.  

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
## [!INCLUDE[d365fin](includes/training_link_md.md)]

