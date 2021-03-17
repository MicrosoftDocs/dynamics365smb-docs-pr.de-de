---
title: Einrichten von Prozessen in Financials | Microsoft Docs
description: Informationen zu Aufgaben, Finanzen in Ihrem Unternehmen einzurichten, um Ihrer Buchhaltung, oder Buchhaltungsanforderungen Prüfungen zu entsprechen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a659fd4edfcbeccf65204f30685ce5b3cf527399
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381931"
---
# <a name="setting-up-finance"></a>Finanzen einrichten
Bevor Sie mit der Geschäftstätigkeit beginnen können, müssen Sie Regeln und Standardeinstellungen für die Verwaltung der Finanzprozesse für dieses Unternehmen festlegen. Richten Sie zunächst den Kern der Buchhaltungsdatensätze des Mandanten ein, den Kontenplan. Anschließend werden Buchungsgruppen eingerichtet, um das Zuordnen von standardmäßigen Sachkontobuchungskonten zu Debitoren, Kreditoren und Artikeln effizienter zu gestalten.

Einige Finanzeinrichtungen können automatisch mit Hilfe der Anleitung für die unterstützte Einrichtung durchgeführt werden, andere müssen manuell durchgeführt werden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).

Sie können Dimensionen verwenden, um jeder Transaktion unterschiedliche Arten von Informationen hinzuzufügen. Sie können die grundlegenden Dimensionen Ihres Mandanten festlegen, wie Projekte und Abteilungen. Später können Sie weitere Dimensionen hinzufügen, wenn Sie sie benötigen, und Sie können temporäre Dimensionen für die Verwendung für einen begrenzten Zeitraum einrichten, beispielsweise in Verbindung mit einer Verkaufskampagne. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

Zwar müssen viele der Einrichtungsaufgaben ausgeführt werden, bevor Sie mit der Erfassung von Finanztransaktionen beginnen können, die meisten Einstellungen können jedoch zu einem späteren Zeitpunkt geändert werden. Einige der Einrichtungsaufgaben sind optional, beispielsweise richten Sie Intercompany-Buchungen und Konsolidierungen nur ein, wenn Sie mit mehreren Unternehmen arbeiten. Einige Einrichtungsaufgaben, wie das Angeben der Zeitraums, in dem das Buchen erlaubt ist, müssen möglicherweise in regelmäßigen Abständen wiederholt werden.  

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

| Aktion | Siehe |
| --- | --- |
| Geben Sie an, wie Sie von Kunden bezahlt werden möchten und wie Sie Ihre Lieferanten bezahlen möchten. |[Einrichten von Zahlungsformen](finance-payment-methods.md) |
| Definieren Sie Zahlungsbedingungen zum Verwalten von Fälligkeitsdaten sowie zum Berechnen von möglichem Skonto.|[Zahlungsbedingungen einrichten](finance-payment-terms.md) |
| Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten. |[Buchungsgruppen einrichten](finance-posting-groups.md)|
|Erstellen Sie Kontenschemata und definieren hiermit Kontengruppen, um den Inhalt aus Finanzdiagrammen und Berichte, wie den Bilanz- und GuV-Berichten zu definieren.|[Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Arbeiten mit Zahlungstoleranzen und Skontotoleranzen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Einrichten von Finanzzeiträumen |[Arbeiten mit Buchhaltungsperioden und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md) |
|Richten Sie Erinnerungsbedingungen ein, um überfällige Zahlungen einzutreiben.|[Einrichten von Mahnmethoden, Bestimmungen und Mahntext](finance-setup-reminders.md)|
| Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben. |[Mehrwertsteuer (MwSt.) einrichten](finance-setup-vat.md)|
|Vorbereitung für das Bearbeiten nicht realisierter MwSt. in Verbindung mit Einnahmen- und Ausgabenrechnungs-Methoden.|[Einrichten unrealisierter MwSt. für Einnahmen- und Ausgabenrechnung](finance-setup-unrealized-vat.md)|
| Einrichten Ihrer Verkaufs- und Einkaufsfunktionen, um Zahlungen in Fremdwährungen abzuwickeln.|[Den Ausgleich von Posten in unterschiedlichen Währungen zulassen:](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definieren Sie eine oder mehrere Währungen, so dass Beträge automatisch in Mandantenwährung sowie in Berichtswährung für jeden Sachposten und weitere Posten gebucht werden.|[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)|
|Passen Sie in regelmäßigen Abständen weitere Währungsentsprechungen an, um schwankende Wechselkurse wieder gutzumachen.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|
|Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet.|[Dient zum Einrichten mehrerer Zinssätze.](finance-how-to-set-up-multiple-interest-rates.md)|
|Gegebenenfalls müssen Rechnungsbeträge automatisch beim Erstellen von Rechnungen gerundet werden.|[Einrichten der Rechnungsrundung](finance-set-up-invoice-rounding.md)|
| Fügen Sie dem bestehenden Kontenplan neue Konten hinzu. |[Einrichten des Kontenplans](finance-setup-chart-accounts.md) |
| Einrichten Business Intelligence (BI)- Diagrammen, um Cashflow zu analysieren. |[Einrichten der Cashflowanalyse](finance-setup-cash-flow-analyses.md) |
|Aktivierung der Rechnungstellung für einen Debitoren, der nicht im System eingerichtet ist.|[BarDebitoren einrichten](finance-how-to-set-up-cash-customers.md)|
| Einrichtung von Intrastat-Berichten und Übermitteln des Berichts an eine Behörde | [Einrichten und Berichten von Intrastat](finance-how-setup-report-intrastat.md)|
|Stellen Sie sicher, dass ein Eintrag in einer Fibu Buch.-Blattzeile beim Buchen des Buch.-Blattes verschiedenen Konten zugewiesen wird, entweder Anzahl, Prozent oder Betrag.|[Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern](ui-how-use-allocation-keys-general-journals.md)|
|Einrichten von Herkunftscodes und Ursachencodes ein, mit denen Sie Audit-Trails verfolgen können|[Herkunftscodes und Ursachencodes für Audit Trails einrichten](finance-setup-trail-codes.md)|
|Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.|[Berichtsauswahl in Business Central](across-report-selections.md)|

> [!TIP]
> Abhängig von Ihrem geografischen Standort können einige Seiten Felder enthalten, die in den hier aufgeführten Artikeln nicht beschrieben sind, da sie für lokale Funktionen oder Anpassungen gelten. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]