---
title: Datenbereich in Finance and Operations, Business edition  | Microsoft Docs einrichten
description: "Erhalten von Informationen zum Anzeigen von Daten aus bestimmten Zeiträumen mithilfe von Finance and Operations, Business edition"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0494a04e67803049df71cfefe779c831c9f31674
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a>Datenbereiche eingeben 
Sie können Filter mit einem Start- und Enddatum setzen, sodass lediglich die Daten angezeigt werden, die innerhalb eines bestimmten Datumsbereichs oder Zeitintervalls liegen. Für das Festlegen von Datumsbereichen gelten besondere Regeln. Als Beispiel nehmen wir die **Top 10 Debitoren**.

![Einen Datumsbereich auf der Anforderungsseite der Top 10 Debitorenliste festlegen](./media/ui-enter-date-ranges/customer-top10-list.png)

Hier können Sie den Bericht auf eine Gültigkeit wie den letzten 2 Wochen oder insgesamt 6 Wochen oder einen beliebigen Bereich einschränken. Um eine Gültigkeit festzulegen, geben Sie Daten ein und verwenden anschließend **..** oder **|**, um den Bereich zu ändern. Im vorliegenden Beispiel müssen Sie, um die ersten zwei Wochen des Mai für die Top 10 Debitoren anzuzeigen, den Datumsfilter auf *05 01 17..05 14 17* setzen.
Hier finden Sie einige andere Beispiele:

| Bedeutung | Beispiel | Enthaltene Posten |
|---|---|---|
|Ist gleich| 12 15 16 |Nur jene, die am 15. Deuzember 2016 gebucht wurden.|
|Intervall| 12 15 16..01 15 17<br /><br />..12 15 16|Jene, die zwischen dem 15. Dezember 2016 und dem 15. Januar 2017 (einschließlich) gebucht wurden.<br /><br />Jene, die bis zum 15. Dezember 2016 oder früher gebucht wurden.|
|Entweder/oder|12 15 16&#124;12 16 16|Entweder am 15. Dezember oder am 16. Dezember 2016 gebucht. Falls es Posten gibt, die an einem der beiden Tage gebucht wurden, werden diese angezeigt.|

Sie können auch die verschiedenen Formattypen miteinander kombinieren.

| Beispiel | Enthaltene Posten |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Posten, die am 15. Dezember 2016 oder zwischen dem 01. Dezember 2016 und 31. Mai 2017 (einschließlich) gebucht wurden. |
|..12 14 16&#124;12 30 16.. | Posten, die bis einschließlich zum 14. Dezember oder am bzw. nach dem 30. Dezember gebucht wurden. Mit diesem Filter können Sie alle Posten ausschließen, die zwischen den beiden angegebenen Tagen gebucht wurden. |

Beachten Sie, dass wir das US-Datumsformat MMDDYY hier verwendet haben. [!INCLUDE[d365fin](includes/d365fin_md.md)] wird verfügbar in anderen Märkten, Sie haben die Möglichkeit, die Formaten zu verwenden, die möchten.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Eingeben von Kriterien in Filtern](ui-enter-criteria-filters.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

