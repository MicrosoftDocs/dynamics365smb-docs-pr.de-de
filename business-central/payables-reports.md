---
title: Verbindlichkeiten a. LL Berichte und Analysen
description: Sehen Sie, welche Berichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie den Überblick über Ihre Verbindlichkeiten behalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953384"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Berichte und Analysen zu Verbindlichkeiten a. LL in Business Central

Um Sie bei der Verwaltung Ihrer Verbindlichkeiten in [!INCLUDE [prod_short](includes/prod_short.md)] zu unterstützen, sind Standardberichte und Analysen integriert. Es geht über die herkömmlichen Berichtsbeschränkungen hinaus und hilft Ihnen, verschiedene Arten von Berichten effizient zu gestalten.  

## <a name="reports"></a>Berichte

Die folgende Tabelle beschreibt einige der wichtigsten Berichte in der Kreditorenbuchhaltung.

| Bericht | Objekt-ID | Beschreibung |
|--|--|--|
| **Kreditor - Saldenrückblick** | 322|Zeigt überfällige Salden für Kreditoren in überfälligen Zeitintervallen an. Die überfälligen Beträge können je nach Bedarf nach Fälligkeitsdatum, Buchungsdatum oder nach Belegdatum angezeigt werden. Sie können wählen, ob Sie die Beträge in Hauswährung (LCY) anzeigen und Details zu den überfälligen Belegen drucken möchten. Die Zeitintervalle können Überschriften mit Datumsangaben oder mit der Anzahl der überfälligen Tage haben, bezogen auf die angegebene Fälligkeit nach Typ.<br>Dieser Bericht ist der Hauptbericht zum Abstimmen des Kreditor-Sachkontos mit dem Hauptbuch. Unter der Annahme, dass Sie die direkte Buchung auf die Konten, die im Sachkonto der Kreditorenbuchungsgruppen verwendet werden, nicht zugelassen haben, ist dieser Bericht eine Angabe der Beträge, die Sie im Hauptbuch finden.|
| **Kreditor – Saldo bis Datum** | 321 | Zeigt den Kreditorensaldo nach dem Enddatum des angegebenen Datumsbereichs an. Sie können wählen, ob der Kreditorensaldo in Ihrer lokalen Währung (LCY) angezeigt werden soll. Markieren Sie das Feld **Nicht angewandte Einträge einbeziehen**, um Einträge anzuzeigen, die bis zum Enddatum abgeschlossen wurden, aber zu einem späteren Zeitpunkt nicht angewandt (geöffnet) wurden. Wählen Sie das Feld **Einträge mit Nullsaldo anzeigen**, um Kreditoren mit einem Saldo von Null bis zum Enddatum des Datumsfilters anzuzeigen. Der Datumsfilter gilt für die detaillierten Sachkonto-Einträge für die Einträge im Bericht. Wenn Sie Zahlungen nach dem Enddatum haben, die auf Rechnungen innerhalb des Datumsbereichs angewendet wurden, erscheinen die Rechnungen im Bericht, da sie bis zum Enddatum noch nicht abgeschlossen sind. |
| **Kreditor – Test – Bilanz** | 329 | Zeigt die Nettoänderungen für Kreditoren für den im Datumsfilter angegebenen Zeitraum sowie die Nettoänderung von Jahr zu Jahr für das Geschäftsjahr, das dem gewählten Zeitraum entspricht. Der Bericht ist nach Kreditorenbuchungsgruppen gruppiert und bietet eine andere Ansicht des Kreditor-Sachkontos als der Bericht **Aktuelle Verbindlichkeiten**. **Hinweis**: Wenn Sie keine Buchhaltungsperiode festgelegt haben, weiß das System nicht, welches Geschäftsjahr zu verwenden ist und zeigt entweder Jahr-zu-Jahr ab dem zuletzt definierten Geschäftsjahr an oder wählt einfach die Periode aus, die vom Anfang eines Jahres sein kann oder auch nicht.|
| **Kreditor – Detail Test-Bilanz** | 304 | Zeigt alle Sachkonto-Einträge des Kreditors innerhalb des angegebenen Datumsfilters. Der Bericht zeigt die Anfangssalden des Kreditors relativ zum Datumsfilter. |
| **Einkaufsstatistik** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Dieser Bericht kann auch in der Kreditorenbuchhaltung verwendet werden, da es einfacher ist, einen schnellen Blick auf gebuchte Zahlungen, Rabatte und andere Transaktionen für einen bestimmten Kreditor zu werfen.|
|**Kreditor – Zusammenfassung Fälligkeit**|305| Veralteter Bericht für gealterte Verbindlichkeiten a. LL. Wir empfehlen, dass Sie stattdessen den Bericht **Gealterte Verbindlichkeiten a. LL** verwenden. Sie können eine Periodenlänge und ein Datum wählen, das als festgelegtes *Überfälliges Datum* verwendet werden soll.|
|**Zahlungen im Rückstand**|319|Zeigt Kreditor-Sachkonto-Einträge, bei denen das Feld **Zurückgestellt** nicht leer ist.|
|**Kreditorenvorauszahlung Buch.-Blatt**|317|Zeigt die Erfassung des Zahlungsausgangs Buch.-Blatt mit Skonto- und Toleranzinformationen. Der Bericht kann verwendet werden, um Zahlungen zu prüfen, bevor Zahlungsausgangs Buch.-Blätter erstellt und das Journal gebucht wird. **Hinweis**: Der Bericht zeigt Zahlungsrabatte falsch an, wenn mehrere Gutschriften in einer Anwendung verwendet wurden. In diesem Fall wird der Zahlungsrabatt für die zusätzlichen Gutschriften als ein nicht angewandter Betrag angezeigt.|
|**Kreditor – Liste**|301|Zeigt verschiedene Arten von Basisinformationen für Kreditoren an, z.B. die Buchungsgruppe des Kreditors, Rabatt- und Zahlungsinformationen, die Prioritätsstufe und die Standardwährung des Kreditors sowie den aktuellen Saldo des Kreditors (in LCY). Der Report kann z.B. zur Pflege der Informationen in der Tabelle Kreditor verwendet werden.|

## <a name="see-also"></a>Siehe auch

[Analysieren von Finanzberichten in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Verwaltung von Anlagen](fa-manage.md)  
[Lokale Funktionen – Übersicht](about-localization.md)  
[Buchhalter-Erfahrung in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
