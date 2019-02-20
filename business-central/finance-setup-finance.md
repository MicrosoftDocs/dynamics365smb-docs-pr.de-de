---
title: Einrichten von Prozessen in Financials | Microsoft Docs
description: "Informationen zu Aufgaben, Finanzen in Ihrem Unternehmen einzurichten, um Ihrer Buchhaltung, oder Buchhaltungsanforderungen Prüfungen zu entsprechen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 377e7f8eb3cb78adf68e3f4167a215d8f027f972
ms.contentlocale: de-de
ms.lasthandoff: 12/19/2018

---
# <a name="setting-up-finance"></a>Finanzen einrichten
Damit Sie sich rasch zurechtfinden, enthält [!INCLUDE[d365fin](includes/d365fin_md.md)] Standardkonfigurationen für die meisten Finanzprozesse. Wenn Sie die Konfiguration ändern müssen, um Ihrem Geschäft zu entsprechen, tun Sie es. Sei können vom Rollencenter auf eine unterstützte Einrichtung zugreifen, die Sie bespielsweise dabei unterstützt, Verkaufssteuer abhängig von Ihrem Standort einzurichten.  

Es gibt jedoch mehrere Elemente, die Sie selber einrichten müssen. Wenn Sie Dimensionen als Grundlage für Business Intelligence verwenden möchten.  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| Aufgabe | Siehe |
| --- | --- |
| Wählen Sie aus, wie Sie Ihre Kreditoren bezahlen. |[Zahlungsformen definieren](finance-payment-methods.md) |
| Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten. |[Buchungsgruppen einrichten](finance-posting-groups.md)|
|Erstellen Sie Kontenschemata und definieren hiermit Kontengruppen, um den Inhalt aus Finanzdiagrammen und Berichte, wie den Bilanz- und GuV-Berichten zu definieren.|[Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Mit Zahlungstoleranzen und Skontotoleranzen arbeiten](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Einrichten von Finanzzeiträumen |[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md) |
| Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben. |[Methoden für die Berechnung und Buchung von Mehrwertsteuer einrichten](finance-setup-vat.md)|
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
|Konsolidierten Rohbilanzberichts für das Buchhalter Rollen-Center vorbereiten, um eine finanzielle Übersicht in mehreren Mandanten zu erhalten.|[Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md)|
|Stellen Sie sicher, dass ein Eintrag in einer Fibu Buch.-Blattzeile beim Buchen des Buch.-Blattes verschiedenen Konten zugewiesen wird, entweder Anzahl, Prozent oder Betrag.|[Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

