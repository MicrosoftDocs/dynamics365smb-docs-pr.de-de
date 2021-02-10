---
title: Optionale Aktivitäten beispielsweise für Abschlussperioden | Microsoft Docs
description: In diesem Thema werden die optionalen Vorgänge und Aktivitäten Abschlussbuchhaltungsperioden in  Business Central dargelegt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 104f63e07e4bfd8945f73581a4fb7810f946304f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755567"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Überblick zu Aufgaben, Buchhaltungsperioden zu schließen
[!INCLUDE[prod_short](includes/prod_short.md)] zwingt Sie nicht, Perioden zu schließen, aber es gibt viele Aktivitäten am Periodenende (Monatsende), die Sie ausführen können. Dieses Thema zeigt eine Übersicht von optionalen Vorgängen und Aktivitäten für Perioden, die bereitstehen.  

## <a name="general-ledger"></a>Sachposten
* Geben Sie systemweite und benutzerspezifische Buchungsperioden an.  

    Dies gibt die Daten an, zwischen denen Buchungen zulässig sind. Je nach Geschäftsanforderungen empfiehlt es sich, die Buchungsdatumsbereiche für Benutzer zu Beginn des Periodenabschlusses einzugrenzen. Weitere Informationen finden Sie unter [Abschließen von Buchhaltungsperioden](finance-how-specify-posting-periods.md).  
* Führen Sie alle notwendigen Sachpostenregulierungen durch.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter.  
  <!--* Process Consolidations-->
* Führen Sie Kontenschemata wie folgt aus:  
  * Öffnen Sie die Seite **Kontenschema** und klicken Sie auf **Drucken**.  

## <a name="sales-and-receivables"></a>Debitoren und Verkauf
* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen werden gebucht.  
* Buchen Sie alle Barzahlungseingangs-Buch.-Blätter.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Debitoren und Verkauf beziehen.  
* Stimmen Sie die Debitoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Fakturierte Aufträge löschen** aus.  

## <a name="purchases-and-payables"></a>Kreditoren und Einkauf
* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen für Kreditoren werden gebucht.  
* Buchen Sie das Zahlungsausgangs Buch.-Blatt.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Kreditoren und Einkäufe beziehen.  
* Führen Sie den Bericht **Kreditor - Saldenrückblick** aus, und stimmen Sie die Kreditoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Erledigte fakturierte Bestellungen löschen** aus.  

Anlagen
* Alle Wartungskosten wurden über die Anlagen-Buch.-Blätter oder Rechnungen gebucht.
* Buchen Sie Regulierungen.
* Buchen Sie die Zuschreibung.
* Buchen Sie die Abschreibung.
* Aktualisieren und buchen Sie das Buch.-Blatt für wiederkehrende Anlagen

Intercompany
* Verarbeiten von Intercompanytransaktionen

## <a name="calculate-and-process-sales-tax"></a>Berechnen und erfassen Sie die MwSt.
* Schließen Sie Steuer-Abrechnungen ab.  

## <a name="see-also"></a>Siehe auch
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Schließen der Bücher](year-close-books.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
