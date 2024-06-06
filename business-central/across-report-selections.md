---
title: Berichtsauswahl in Business Central
description: 'Erfahren Sie, wie Sie die Berichte einrichten, mit denen Sie verschiedene Arten von Dokumenten in Business Central drucken.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Berichtsauswahl für Dokumente in Business Central

Sie können Standardberichte festlegen, die für den Druck von Verkaufs-, Kauf- und Service-Dokumenten wie Bestellungen, Angeboten und Rechnungen verwendet werden sollen. Wenn Sie beispielsweise ein bestimmtes Layout für Verkaufsrechnungen haben, können Sie diesen Bericht auf der Seite **Berichtsauswahl – Verkauf** definieren, damit sie zum Senden oder Drucken von Verkaufsrechnungen verwendet wird.  

## Verfügbare Berichtsauswahl

Die Seiten **Berichtsauswahl** geben an, welcher Bericht in verschiedenen Situationen gedruckt wird. [!INCLUDE [prod_short](includes/prod_short.md)] bietet Standardkonfigurationen, die Sie jedoch bei Bedarf ändern können. Zudem lassen sich auch weitere Berichte in das Fenster **Berichtsauswahl** aufnehmen, um gleichzeitig mehrere Berichte zu einer Belegart auszudrucken. 

In der folgenden Tabelle wird beschrieben, wo Sie Informationen zu den verschiedenen Seiten finden.  

|Bereich oder Aufgabe  |Weitere Informationen|
|--------------|----------|
|Beispiel für die Berichtsauswahl (Verkauf)|[Berichtsauswahl für Verkaufsdokumente](#example-report-selection-for-sales-documents) siehe unten|
|Standardlayout für E-Mails mit Verkaufs- und Kaufdokumenten  |[Wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Schecklayouts definieren     |[Ein Prüflayout auswählen](finance-how-define-check-layouts.md) |
|Definieren von Berichten für das Mehrwertsteuer-Reporting (Deutschland)|[Richten Sie Berichte für MwSt ein](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ihr [!INCLUDE [prod_short](includes/prod_short.md)] kann zusätzliche Seiten **Berichtsauswahl** enthalten, abhängig von Ihrem Standort und Ihrer Branche. Um Ihre Einrichtung zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Berichtsauswahl** ein und wählen Sie dann den entsprechenden Link.

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] enthält die folgenden Seiten **Berichtsauswahl**:

* **Berichtsauswahl - Verkauf**  
* **Berichtsauswahl - Einkauf**  
* **Berichtsauswahl - Lager**  
* **Berichtsauswahl - Cashflow**  
* **Berichtsauswahl – Lager**  
* **Berichtsauswahl - Bankkonto**  
* **Berichtsauswahl – Projekt**  
* **Berichtsauswahl - Service**

## Beispiel: Berichtsauswahl für Verkaufsbelege

Die Seite **Berichtsauswahl - Verkauf** bietet Standardberichte zur Verwendung in verschiedenen Szenarien für jede zugehörige Dokumentart. Wählen Sie im Feld **Verwendung** eine Dokumentenart aus und fügen Sie dann die Berichtsauswahl hinzu oder überprüfen Sie sie. Sie können mehr als einen Bericht festlegen und die Sequenz angeben, in der die Berichte gesendet oder gedruckt werden müssen.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Sie können nicht alle Dokumenttypen als E-Mail-Anhang versenden. Für diejenigen, die Sie versenden können, enthält die Seite **Berichtsauswahl** zusätzliche Felder.  

Auf den Seiten **Berichtsauswahl - Verkauf** und **Berichtsauswahl - Kauf** helfen Ihnen beispielsweise die folgenden Felder beim Festlegen der E-Mail:

|Name des Felds |Description  |
|-----------|-------------|
|**Für E-Mail-Text verwenden**| Fügen Sie zusammengefasste Informationen wie die Rechnungsnummer, das Fälligkeitsdatum oder einen Link zu einem Zahlungsservice in eine E-Mail ein.        |
|**Für E-Mail-Anhang verwenden**| Hängen Sie den zugehörigen Beleg an die E-Mail an.|
|**Layout-Beschreibung E-Mail-Text**|Geben Sie das zu verwendende E-Mail-Textlayout an. In der Regel handelt es sich um ein angepasstes Berichtslayout. |

## Siehe auch

[Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Ein Prüflayout auswählen](finance-how-define-check-layouts.md)  
[Einrichten von Berichten für MwSt. und Intrastat (Deutschland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md)  
[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Finanzberichte und Analysen in Business Central](finance-reports.md)  
[Debitorenberichte und Analysen in Business Central](receivables-reports.md)  
[Kreditoren-Berichte und -Analysen in Business Central](payables-reports.md)  
[Berichte und Analysen zu Anlagen in Business Central](fa-reports.md)  
[Projektberichte und Analysen in Business Central](project-reports.md)  
[Verkaufsberichte und Analysen in Business Central](sales-reports.md)  
[Einkaufsberichte und Analysen in Business Central](purchase-reports.md)  
[Bestands- und Lagerberichte und Analysen in Business Central](inventory-WMS-reports.md)  
[Montageberichte und Analysen in Business Central](assembly-reports.md)  
[Produktionsberichte und Analysen in Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
