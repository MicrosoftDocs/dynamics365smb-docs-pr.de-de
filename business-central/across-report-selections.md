---
title: Berichtsauswahl in Business Central
description: Erfahren Sie, wie Sie die Berichte einrichten, mit denen Sie verschiedene Arten von Dokumenten in Business Central drucken.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 9106b1ac3f6b179e26c8dfb01212b88e92b694fe
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950199"
---
# <a name="report-selection-in-business-central"></a>Berichtsauswahl in Business Central

Sie können Standardberichte einrichten, die zum Drucken von Verkaufs- und Einkaufsbelegen wie Bestellungen, Angebote und Rechnungen verwendet werden. Wenn Sie beispielsweise ein bestimmtes Layout für Verkaufsrechnungen haben, können Sie diesen Bericht auf der Seite **Berichtsauswahl – Verkauf** definieren, damit sie zum Senden oder Drucken von Verkaufsrechnungen verwendet wird.  

Die Seiten **Berichtsauswahl** geben an, welcher Bericht in verschiedenen Situationen gedruckt wird. [!INCLUDE [prod_short](includes/prod_short.md)] bietet Standardkonfigurationen, die Sie jedoch bei Bedarf ändern können. Zudem lassen sich auch weitere Berichte in das Fenster **Berichtsauswahl** aufnehmen, um gleichzeitig mehrere Berichte zu einer Belegart auszudrucken.  

## <a name="available-report-selections"></a>Verfügbare Berichtsauswahl

[!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet verschiedene **Berichtsauswahl** Seiten für verschiedene Bereiche. In der folgenden Tabelle wird beschrieben, wo Sie Informationen zu den verschiedenen Seiten finden.  

|Bereich oder Aufgabe  |Weitere Informationen|
|--------------|----------|
|Beispiel für die Funktionsweise der Berichtsauswahl (Vertrieb)|[Berichtsauswahl für Verkaufsbelege](#example-report-selection-for-sales-documents)|
|Standardlayout für E-Mails mit Verkaufs- und Kaufdokumenten  |[Wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Schecklayouts definieren     |[Ein Prüflayout auswählen](finance-how-define-check-layouts.md) |
|Berichte für die Mehrwertsteuerberichterstattung definieren (Deutschland)|[Richten Sie Berichte für MwSt ein](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ihr [!INCLUDE [prod_short](includes/prod_short.md)] kann zusätzliche Seiten **Berichtsauswahl** enthalten, abhängig von Ihrem Standort und Ihrer Branche. Sie können Ihre Einrichtung jederzeit überprüfen, indem Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol wählen, **Berichtsauswahlen** eingeben und dann den entsprechenden Link wählen.

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet die folgende Seite **Berichtsabschnitt**:

* **Berichtsauswahl - Verkauf**  
* **Berichtsauswahl - Einkauf**  
* **Berichtsauswahl - Lager**  
* **Berichtsauswahl - Cashflow**  
* **Berichtsauswahl – Lager**  
* **Berichtsauswahl - Bankkonto**  
* **Berichtsauswahlen - Mahnung/Zinsrechnung**  
* **Berichtsauswahl – Projekt**  

## <a name="example-report-selection-for-sales-documents"></a>Beispiel: Berichtsauswahl für Verkaufsbelege

Die Seite **Berichtsauswahl – Verkauf** definiert die Standardberichte, die in verschiedenen Szenarien für jeden zugehörigen Dokumenttyp verwendet werden sollen. Wählen Sie einen Dokumenttyp im Feld **Verwendung** und fügen Sie dann die Berichtsauswahl hinzu oder überprüfen Sie sie. Sie können mehr als einen Bericht und die Reihenfolge festlegen, in der die Berichte gesendet oder gedruckt werden müssen.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Einige Belegtypen können als E-Mail-Anhänge gesendet werden, andere nicht. Wenn ein Belegtyp per E-Mail gesendet werden kann, enthält die Seite **Berichtsauswahl** zusätzliche Felder.  

Zum Beispiel helfen Ihnen die Seiten **Berichtsauswahl – Verkauf** und **Berichtsauswahl – Kauf** die folgenden Felder für die E-Mails einzurichten:

|Name des Felds |Description  |
|-----------|-------------|
|**Für E-Mail-Text verwenden**| Fügen Sie zusammengefasste Informationen wie Rechnungsnummer, Fälligkeitsdatum und Zahlungsservicelink in eine E-Mail ein.        |
|**Für E-Mail-Anhang verwenden**| Hängen Sie den zugehörigen Beleg an die E-Mail an.|
|**Layout-Beschreibung E-Mail-Text**|Geben Sie das zu verwendende E-Mail-Textlayout an. Das Layout ist in der Regel ein benutzerdefiniertes Berichtslayout. |

## <a name="see-also"></a>Siehe auch

[Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Ein Prüflayout auswählen](finance-how-define-check-layouts.md)  
[Einrichten von Berichten für MwSt. und Intrastat (Deutschland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md)  
[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Finanzberichte und Analysen in Business Central](finance-reports.md)  
[Debitorenberichte und Analysen in Business Central](receivables-reports.md) 
[Kreditorenberichte und Analysen in Business Central](payables-reports.md)  
[Berichte und Analysen zu Anlagen in Business Central](fa-reports.md)  
[Projektberichte und Analysen in Business Central](project-reports.md)  
[Verkaufsberichte und Analysen in Business Central](sales-reports.md)  
[Einkaufsberichte und Analysen in Business Central](purchase-reports.md)  
[Bestands- und Lagerberichte und Analysen in Business Central](inventory-WMS-reports.md)  
[Montageberichte und Analysen in Business Central](assembly-reports.md)  
[Produktionsberichte und Analysen in Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]