---
title: Debitoren verwalten | Microsoft Docs
description: Debitoren verwalten
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62d59546331a5faa5ecb7aea0f9bb8dedea719f9
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Debitoren verwalten
<a id="managing-receivables" class="xliff"></a>
Ein regelmäßiger Schritt in jedem Finanzrhythmus ist, Bankkonten abzustimmen, die es erfordern, dass Sie Zahlungen mit Debitoren- oder Kreditorenposten ausgleichen, um Verkaufsrechnungen und - gutschriften zu schließen.  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist einer der schnellsten Arten, Zahlungen im Fenster **Zahlungsabstimmungsbuch.-Blatt** zu erfassen, indem Sie eine Bankauszugsdatei oder einen Feed erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten basierend auf Übereinstimmungen zwischen Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können die Suchergebnisse überprüfen und ändern, bevor Sie das Buch.-Blatt buchen, und schließen Bankposten für Posten, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Es gibt jedoch andere praktische Orte, um Zahlungen zu übernehmen und Bankkonten auszugleichen:  

* Im Fenster **Bankkontoabstimmung** können Sie ebenfalls Einträge prüfen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).  
* Das Fenster **Zahlungs-Registrierung**, indem Sie manuell Zahlungseingänge wie Kasse, Scheck oder Bankbuchung für eine generierte Liste der unbezahlten Verkaufsbelegen überprüfen können. Beachten Sie, dass diese Funktionen nur für Verkaufsbelege verfügbar sind.  
* Das Fenster **Zahlungseingangs Buch.-Blatt**, indem Sie manuell Belege der relevanten Sachkonten, Kunden oder anderer Konten durch Eingabe einer Zahlungsposition buchen können. In diesem Fall können Sie entweder den Wareneingang oder die Rückerstattung mit einem oder mehreren offenen Posten anwenden, bevor Sie das Zahlungseingangs Buch.-Blatt buchen, oder Sie können sie aus den erstellten Debitorenposten erstellen.  

Eine andere Aufgabe, wenn Sie Forderungen verwalten ist es, offene Salden zu erfassen und Zinsrechnungen zu verwalten und Mahnungen auszugeben. [!INCLUDE[d365fin](includes/d365fin_md.md)] bietet Möglichkeiten, dies ebenfalls zu tun. Weitere Informationen finden Sie unter [Vorgehensweise: Offene Salden eintreiben](receivables-collect-outstanding-balances.md)  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

| Aufgabe | Siehe |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Ausgleichen von Zahlungen mit offenen Debitorenposten auf Grundlage der manuellen Eingabe in einer Liste von unbezahlten Verkaufsbelegen. |[Gewusst wie: Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Buchen Sie Zahlungseingänge oder Erstattungen für Debitoren im Zahlungseingangs Buch.-Blatt für Debitorenposten, entweder aus dem Buch.-Blatt oder von gebuchten Posten. |[Vorgehensweise: Manuelle Abstimmung vom Zahlungen](receivables-how-apply-sales-transactions-manually.md) |
| Erinnern von Debitoren an überfällige Beträge, Berechnen von Zinsen und Gebühren sowie Verwalten von Debitoren |[Vorgehensweise: Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md) |

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verkauf](sales-manage-sales.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

