---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e66b50cec6d3f9e2606f3f698e12a06eccdd5cf6
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104172"
---
Die folgende Tabelle beschreibt einige der wichtigsten Berichte in der Kreditorenbuchhaltung.

| Bericht | Objekt-ID | Beschreibung |
|--|--|--|
| **Kreditor - Saldenrückblick** | 322|Zeigt überfällige Salden für Kreditoren in überfälligen Zeitintervallen an. Die überfälligen Beträge können je nach Bedarf nach Fälligkeitsdatum, Buchungsdatum oder nach Belegdatum angezeigt werden. Sie können wählen, ob Sie die Beträge in Hauswährung (LCY) anzeigen und Details zu den überfälligen Belegen drucken möchten. Die Zeitintervalle können Überschriften mit Datumsangaben oder mit der Anzahl der überfälligen Tage haben, bezogen auf die angegebene Fälligkeit nach Typ.<br>Dieser Bericht ist der Hauptbericht zum Abstimmen des Kreditor-Sachkontos mit dem Hauptbuch. Unter der Annahme, dass Sie die direkte Buchung auf die Konten, die im Sachkonto der Kreditorenbuchungsgruppen verwendet werden, nicht zugelassen haben, ist dieser Bericht eine Angabe der Beträge, die Sie im Hauptbuch finden.|
| **Kreditor – Saldo bis Datum** | 321 | Zeigt den Kreditorensaldo nach dem Enddatum des angegebenen Datumsbereichs an. Sie können wählen, ob der Kreditorensaldo in Ihrer lokalen Währung (LCY) angezeigt werden soll. Markieren Sie das Feld **Nicht angewandte Einträge einbeziehen**, um Einträge anzuzeigen, die bis zum Enddatum abgeschlossen wurden, aber zu einem späteren Zeitpunkt nicht angewandt (geöffnet) wurden. Wählen Sie das Feld **Einträge mit Nullsaldo anzeigen**, um Kreditoren mit einem Saldo von Null bis zum Enddatum des Datumsfilters anzuzeigen. Der Datumsfilter gilt für die detaillierten Sachkonto-Einträge für die Einträge im Bericht. Wenn Sie Zahlungen nach dem Enddatum haben, die auf Rechnungen innerhalb des Datumsbereichs angewendet wurden, erscheinen die Rechnungen im Bericht, da sie bis zum Enddatum noch nicht abgeschlossen sind. |
| **Kreditor – Test – Bilanz** | 329 | Zeigt die Nettoänderungen für Kreditoren für den im Datumsfilter angegebenen Zeitraum sowie die Nettoänderung von Jahr zu Jahr für das Geschäftsjahr, das dem gewählten Zeitraum entspricht. Der Bericht ist nach Kreditorenbuchungsgruppen gruppiert und bietet eine andere Ansicht des Kreditor-Sachkontos als der Bericht **Aktuelle Verbindlichkeiten**. **Hinweis**: Wenn Sie keine Buchhaltungsperiode festgelegt haben, weiß das System nicht, welches Geschäftsjahr zu verwenden ist und zeigt entweder Jahr-zu-Jahr ab dem zuletzt definierten Geschäftsjahr an oder wählt einfach die Periode aus, die vom Anfang eines Jahres sein kann oder auch nicht.|
| **Kreditor – Detail Test-Bilanz** | 304 | Zeigt alle Sachkonto-Einträge des Kreditors innerhalb des angegebenen Datumsfilters. Der Bericht zeigt die Anfangssalden des Kreditors relativ zum Datumsfilter. |
| **Einkaufsstatistik** |312 |[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]<br>Dieser Bericht kann auch in der Kreditorenbuchhaltung verwendet werden, da es einfacher ist, einen schnellen Blick auf gebuchte Zahlungen, Rabatte und andere Transaktionen für einen bestimmten Kreditor zu werfen.|
|**Kreditor – Zusammenfassung Fälligkeit**|305| Veralteter Bericht für gealterte Verbindlichkeiten a. LL. Wir empfehlen, dass Sie stattdessen den Bericht **Gealterte Verbindlichkeiten a. LL** verwenden. Sie können eine Periodenlänge und ein Datum wählen, das als festgelegtes *Überfälliges Datum* verwendet werden soll.|
|**Zahlungen im Rückstand**|319|Zeigt Kreditor-Sachkonto-Einträge, bei denen das Feld **Zurückgestellt** nicht leer ist.|
|**Kreditorenvorauszahlung Buch.-Blatt**|317|Zeigt die Erfassung des Zahlungsausgangs Buch.-Blatt mit Skonto- und Toleranzinformationen. Der Bericht kann verwendet werden, um Zahlungen zu prüfen, bevor Zahlungsausgangs Buch.-Blätter erstellt und das Journal gebucht wird. **Hinweis**: Der Bericht zeigt Zahlungsrabatte falsch an, wenn mehrere Gutschriften in einer Anwendung verwendet wurden. In diesem Fall wird der Zahlungsrabatt für die zusätzlichen Gutschriften als ein nicht angewandter Betrag angezeigt.|
|**Kreditor – Liste**|301|Zeigt verschiedene Arten von Basisinformationen für Kreditoren an, z.B. die Buchungsgruppe des Kreditors, Rabatt- und Zahlungsinformationen, die Prioritätsstufe und die Standardwährung des Kreditors sowie den aktuellen Saldo des Kreditors (in LCY). Der Report kann z.B. zur Pflege der Informationen in der Tabelle Kreditor verwendet werden.|
