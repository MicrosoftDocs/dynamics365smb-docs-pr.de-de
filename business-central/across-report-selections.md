---
title: Berichtsauswahl in Business Central
description: Erfahren Sie, wie Sie die Berichte einrichten, mit denen Sie verschiedene Arten von Dokumenten in Business Central drucken.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 16ad3480c10da544c7fdd3a6a299dc6d86cfce46
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134056"
---
# <a name="report-selection-in-business-central"></a>Berichtsauswahl in Business Central

Sie können Standardbereichte einrichten, die verwendet werden, um sie bei der Arbeit mit verschiedenen Einkaufs- und Verkaufsbelegen, wie Bestellungen, Angebote, Rechnungen und Gutschriften, drucken zu können. Wenn Sie beispielsweise ein bestimmtes Layout für Verkaufsrechnungen haben, können Sie diesen Bericht auf der Seite **Berichtsauswahl – Verkauf** definieren, damit sie zum Senden oder Drucken von Verkaufsrechnungen verwendet wird.  

Die Seiten **Berichtsauswahl** geben an, welcher Bericht in verschiedenen Situationen gedruckt wird. [!INCLUDE [prod_short](includes/prod_short.md)] enthält Standardkonfigurationen, aber Sie können diese Standardeinstellungen natürlich ändern. Zudem lassen sich auch weitere Berichte in das Fenster **Berichtsauswahl** aufnehmen, um gleichzeitig mehrere Berichte zu einer Belegart auszudrucken.  

## <a name="available-report-selections"></a>Verfügbare Berichtsauswahl

[!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet verschiedene **Berichtsauswahl** Seiten für verschiedene Bereiche. In den folgenden Tabellen wird beschrieben, wo Sie Informationen zu den verschiedenen Seiten finden.  

|Bereich oder Aufgabe  |Weitere Informationen|
|--------------|----------|
|Beispiel für die Funktionsweise der Berichtsauswahl (Vertrieb)|[Berichtsauswahl für Verkaufsbelege](#example-report-selection-for-sales-documents)|
|Standardlayout für E-Mails mit Verkaufs- und Kaufdokumenten  |[Richten Sie wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege ein](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Schecklayouts definieren     |[Ein Prüflayout auswählen](finance-how-define-check-layouts.md) |
|Berichte für die Mehrwertsteuerberichterstattung definieren (Deutschland)|[Richten Sie Berichte für MwSt ein](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ihr [!INCLUDE [prod_short](includes/prod_short.md)] kann zusätzliche Seiten **Berichtsauswahl** enthalten, abhängig von Ihrem Standort und Ihrer Branche. Sie können Ihre Einrichtung jederzeit überprüfen, indem Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun") Symbol wählen, **Berichtsauswahlen** eingeben und dann den entsprechenden Link wählen.

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet die folgende Seite **Berichtsabschnitt**:

* **Berichtsauswahl - Verkauf**  
* **Berichtsauswahl - Einkauf**  
* **Berichtsauswahl - Lager**  
* **Berichtsauswahl - Cashflow**  
* **Berichtsauswahl – Lager**  
* **Berichtsauswahl - Bankkonto**  
* **Berichtsauswahlen - Mahnung/Zinsrechnung**  

## <a name="example-report-selection-for-sales-documents"></a>Beispiel: Berichtsauswahl für Verkaufsbelege

Die Seite **Berichtsauswahl – Verkauf** definiert die Standardberichte, die in verschiedenen Szenarien für jeden zugehörigen Dokumenttyp verwendet werden sollen. Wählen Sie einen Dokumenttyp im Feld **Verwendung** und fügen Sie dann die Berichtsauswahl hinzu oder überprüfen Sie sie. Sie können mehr als einen Bericht und die Reihenfolge festlegen, in der die Berichte gesendet oder gedruckt werden müssen.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Einige Dokumenttypen können als E-Mail-Anhänge gesendet werden, andere nicht. Jede Seite **Berichtsauswahl** zeigt zusätzliche Felder an, wenn der Typ unterstützende E-Mail nicht sofort verfügbar ist.  

Zum Beispiel helfen Ihnen die Seiten **Berichtsauswahl – Verkauf** und **Berichtsauswahl – Kauf** die folgenden Felder für die E-Mails einzurichten:

|Name des Felds |Beschreibung  |
|-----------|-------------|
|**Für E-Mail-Text verwenden**| Gibt an, dass zusammengefasste Informationen, z. B. Rechnungsnummer, Fälligkeitsdatum und Zahlungsservicelink, in den Text der gesendeten E-Mail eingefügt werden.        |
|**Für E-Mail-Anhang verwenden**| Legt fest, dass der zugehörige Beleg an die E-Mail angehängt wird.|
|**Layout-Beschreibung E-Mail-Text**|Gibt das verwendete E-Mail-Textlayout an, normalerweise ein benutzerdefiniertes Berichtslayout. |

## <a name="see-also"></a>Siehe auch

[Richten Sie wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege ein](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Ein Prüflayout auswählen](finance-how-define-check-layouts.md)  
[Einrichten von Berichten für MwSt. und Intrastat (Deutschland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md)  
[Drucker einrichten](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]