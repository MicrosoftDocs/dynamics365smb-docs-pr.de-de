---
title: Übersicht über die Aufgaben zum Einrichten von Einkäufen
description: 'Beschreibt die Aufgaben, um die Beschaffungsrichtlinien Ihres Mandanten festzulegen und Ihre Einkaufsprozesse einzurichten.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: edupont
---
# Einkauf einrichten

Bevor Sie Einkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Einkaufsrichtlinien des Mandanten definieren.

Sie müssen die allgemeine Einrichtung auf der Seite **Kreditoren und Einkauf Einr.** definieren, was in der Regel einmal während der anfänglichen Implementierung erfolgt. Erfahren Sie mehr im Abschnitt [Kreditoren und Einkauf Einr.](#purchases-and-payables-setup).

Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.

Einrichten von finanzbezogenen Einkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt. Erfahren Sie mehr unter [Einrichten von Finanzen](finance-setup-finance.md). Ähnlich verhält es sich mit der Einrichtung des Einkaufs, wie z. B. Einheiten und Artikelverfolgungscodes, die Sie im [Abschnitt „Lagereinrichtung“](inventory-setup-inventory.md) finden.

## Kreditoren und Einkauf Einr.

Bevor Sie mit Einkäufen und Verbindlichkeiten arbeiten, geben Sie auf der Seite **Kreditoren und Einkauf Einr.** wie Einkaufswerte gebucht werden und welche Nummernkreise für Kreditoren und Einkaufsbelege verwendet werden.

### Allgemeine Einstellungen

Auf dem Inforegister **Allgemein** geben Sie an, wie Rabatte berechnet und gebucht werden sollen und ob Sie Rechnungen runden möchten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Einige Felder erfordern besondere Aufmerksamkeit, wie **Rech.Rab. pro MwSt.Kennz. ber.**, das angibt, ob der Rechnungsrabatt nach der Steuerkennung oder der Rechnungssumme berechnet wird. Erfahren Sie mehr unter [Kombinieren Sie MwSt.-Produktbuchungsgruppen in der MwSt.-Einrichtung](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

Ebenso kann es im Feld **Währungsausgleich** zu kleinen Rundungsdifferenzen kommen, wenn Buchungen in unterschiedlichen Währungen aufeinander angewendet werden. Erfahren Sie mehr unter [Den Ausgleich von Posten in unterschiedlichen Währungen zulassen:](finance-how-enable-application-ledger-entries-different-currencies.md).

Außerdem ändern einige Felder ihr Verhalten oder hängen davon ab, wie andere Felder festgelegt sind. Zum Beispiel wird die Funktion **Vorauszahlung beim Buchen prüfen** wird dadurch beeinflusst, wie das Feld **Häufigkeit für automatische Aktualisierungen zu Vorauszahlungen** eingestellt ist, dass nach ausstehenden Vorauszahlungen gesucht wird.

Lesen Sie Details zu den Feldern [**Ext. Belegnr. erforderlich**](#external-document-number) und [**Einst.-Pr.-Rückverfolg. notw**](#exact-cost-reversing) unten.

### Einstellungen für Nummernkreise

Auf dem Inforegister **Nummernserie** müssen Sie die eindeutige Identifizierungscodes angeben, die für Kreditoren, Rechnungen und andere Einkaufsbelege verwendet werden sollen. Die Nummerierung ist nicht nur für interne Prozesse wichtig, sondern muss möglicherweise auch den örtlichen Vorschriften entsprechen. Es könnte also eine Überlegung wert sein, alle Serien auf der Seite **Nummernserie** vorher, anstatt neue auf der **Kreditoren & Einkauf Einr.** zu erstellen. Erfahren Sie mehr unter [Nummernserie erstellen](ui-create-number-series.md).

## Externe Belegnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Exakte Einstandspreisstornierung

Die **Einst.-Pr.-Rückverfolg. notw.** Funktion hilft sicherzustellen, dass zurückgegebene Waren zu den gleichen Kosten bewertet werden, zu denen sie ursprünglich aus dem Bestand entnommen wurden, indem eine feste Anwendung verwendet wird, anstatt einer Durchschnitts- oder First-in-First-out (FIFO)-Kalkulationsmethode zu folgen. Erfahren Sie mehr im Abschnitt [Designdetails: Feste Anwendung](design-details-item-application.md#fixed-application). Wird dem ursprünglichen Einkauf ein weiterer Preis hinzugefügt, dann wird der Wert der entsprechenden Einkaufsreklamation aktualisiert.

Mit der aktivierten Funktion kann eine Rücksendung erst gebucht werden, wenn die Artikelpostennummer im Feld **Anwendung für Artikeleintrag**in der Reklamationszeile eingegeben wird. Das Feld wird im Inforegister **Zeilen** standardmäßig nicht angezeigt. Erfahren Sie, wie Sie Felder zu Seiten hinzufügen im Abschnitt [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Weitere Einkaufskonfigurationen

| Bis | Siehe |
| --- | --- |
| Erstellen Sie eine Kreditorenkarte für jeden Kreditor, bei dem Sie einkaufen. |[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md) |
| Kreditoren priorisieren. |[Kreditoren priorisieren](purchasing-how-prioritize-vendors.md) |
| Geben Sie die Bankkontoinformationen,&mdash;einschließlich IBAN- und SWIFT-Codes, auf der Karte&mdash;Ihres Kreditors ein. | [Kreditoren-Bankkonto einrichten](purchasing-how-set-up-vendors-bank-accounts.md) |
| Richten Sie Einkäufer ein, weisen Sie ihnen Kreditoren und Codes zu, um Statistiken zu verfolgen. |[Einkäufer einrichten](purchasing-how-setup-purchasers.md) |
| Geben Sie die unterschiedlichen Rabatte und alternativen Preise ein, die vom Kreditor in Abhängigkeit des Artikels, der Menge und/oder des Datums gewährt werden. |[Erfassen von Einkaufspreisen, Skonti und Zahlungsvereinbarungen](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definieren Sie, was Sie für die von Ihrem Unternehmen gekauften Artikel und Dienstleistungen bezahlen.  | [Preise und Rabatte einrichten](across-prices-and-discounts.md) |
| Erstellen Sie Standardzeilen, die in Belege für wiederkehrende Kaufbelege eingefügt werden sollen. | [Wiederkehrende Bestellpositionen einrichten](purchasing-how-work-recurring-purchase-lines.md) |
| Erstellen Sie Aufgabensequenzen, um Prozesse zu verbinden, die von verschiedenen Benutzern ausgeführt werden, wie z. B. das Anfordern und Genehmigen von Bestellungen. | [Einkaufsgenehmigungsworkflows einrichten](across-set-up-workflows.md) |
| Verwalten Sie geschäftliche Interaktionen mit Ihren Kreditoren, importieren Sie empfangene Rechnungsbelege, und registrieren Sie neue Lieferanten mit dem Outlook-E-Mail-Client. | [Business Central-Add-in für Outlook einrichten](admin-outlook.md) |
| Überprüfen Sie Spesenbelege, wandeln Sie Papier- und elektronische Dokumente in Buchungsblattzeile um, und digitalisieren Sie Papierrechnungen von Kreditoren. | [Einrichten von eingehenden Belegen](across-how-setup-income-documents.md) |
| Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen. |[Berichtsauswahl in Business Central](across-report-selections.md)|
|Geben Sie an, ob Benutzer Einkaufsrechnungen buchen dürfen und ob sie diese zusammen mit einer Lieferung buchen müssen. |[Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer](admin-setup-invoice-posting-policy.md)|

## Siehe verwandte Schulungen unter [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Übersicht einrichten](setup.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
