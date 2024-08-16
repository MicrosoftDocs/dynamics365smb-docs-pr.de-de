---
title: Optionale Aktivitäten für die Schließzeiten
description: In diesem Artikel werden die optionalen Prozesse und Aktivitäten zum Schließen von Abrechnungszeiträumen in Business Central beschrieben.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/02/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="overview-of-tasks-to-close-accounting-periods"></a>Übersicht über die Aufgaben zum Abschluss von Abrechnungsperioden

[!INCLUDE[prod_short](includes/prod_short.md)] zwingt Sie nicht dazu, Zeiträume zu schließen. Es gibt jedoch zahlreiche Aktivitäten zum Zeitraumende (Monatsende), die Sie durchführen können. Dieser Artikel bietet einen Überblick über optionale Prozesse und Aktivitäten zum Abschluss von Perioden.  

## <a name="general-ledger"></a>Sachposten

* Geben Sie systemweite und benutzerspezifische Buchungsperioden an.  

    Dies gibt die Daten an, zwischen denen Buchungen zulässig sind. Abhängig von Ihrem Unternehmen möchten Sie möglicherweise Buchungen zu Beginn oder gegen Ende des Zeitraums zulassen. Erfahren Sie mehr unter [Buchungsperioden angeben](finance-how-specify-posting-periods.md).  
* Führen Sie alle notwendigen Sachpostenregulierungen durch.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter.  
  <!--* Process Consolidations-->
* Führen Sie Finanzberichte wie folgt aus:  
  * Öffnen Sie die Seite **Finanzberichte** und klicken Sie auf **Drucken**.  

## <a name="sales-and-receivables"></a>Debitoren und Verkauf

* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen werden gebucht.  
* Buchen Sie alle Barzahlungseingangs-Buch.-Blätter.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Debitoren und Verkauf beziehen.  
* Stimmen Sie die Debitoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Fakturierte Aufträge löschen** aus.  

## <a name="purchases-and-payables"></a>Kreditoren und Einkauf

* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen für Kreditoren werden gebucht.  
* Buchen Sie das Zahlungsausgangs Buch.-Blatt.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Kreditoren und Einkauf beziehen.  
* Führen Sie den Bericht **Kreditor - Saldenrückblick** aus, und stimmen Sie die Kreditoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Erledigte fakturierte Bestellungen löschen** aus.  

## <a name="fixed-assets"></a>Anlagen

* Alle Wartungskosten wurden über die Anlagen-Buch.-Blätter oder Rechnungen gebucht.
* Buchen Sie Regulierungen.
* Buchen Sie die Zuschreibung.
* Buchen Sie die Abschreibung.
* Aktualisieren und buchen Sie das Buch.-Blatt für wiederkehrende Anlagen

## <a name="intercompany"></a>Intercompany

* Verarbeiten von Intercompanytransaktionen.

## <a name="calculate-and-process-sales-tax"></a>Berechnen und erfassen Sie die MwSt.

* Schließen Sie Steuer-Abrechnungen ab.  

## <a name="see-also"></a>Siehe auch

[Jahres- und Periodenabschlüsse](year-close-years-periods.md)  
[Schließen der Bücher](year-close-books.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
