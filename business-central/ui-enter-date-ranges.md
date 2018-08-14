---
title: "Einstellungsgültigkeiten in Business Central  | Microsoft Docs"
description: "Erhalten von Informationen zum Anzeigen von Daten aus bestimmten Zeiträumen mithilfe von Business Central"
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: de-de
ms.lasthandoff: 07/09/2018

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

## <a name="using-date-formulas"></a>Verwenden von Datumsformeln
Bei einer Datumsformel handelt es sich um eine verkürzte Kombination aus Buchstaben und Zahlen, die zum Berechnen von Datumswerten verwendet wird. Datumsformeln können in verschiedenen Datumsberechnungsfeldern sowie in Felder vom Typ "Wiederholungsrate" (in wiederkehrenden Buch.-Blättern) eingeben werden.

> [!NOTE]
>  In allen Formelfeldern wird automatisch ein Tag aufgenommen, um den heutigen Tag als den Tag abzudecken, an dem die Periode beginnt. Wenn Sie beispielsweise **1W** eingeben, ist der Zeitraum tatsächlich acht Tage, da der aktuelle Tag (heute) eingeschlossen ist. Wenn Sie einen Zeitraum von sieben Tagen (genau eine Woche) angeben möchten, in der das Startdatum eingeschlossen ist, müssen Sie **6D** oder **1W\-1D** eingeben.

Nachfolgend finden Sie einige Verwendungsbeispiele für Datumsformeln:

-   In wiederkehrenden Buch.-Blättern wird anhand der Datumsformel im Feld "Wiederholungsrate" bestimmt, wie oft der Posten in der Buch.-Blattzeile gebucht werden soll.

-   Das Datumsformat im Feld **Frist** für eine bestimmte Erinnerungsstufe bestimmt den Zeitraum, der ab dem Fälligkeitsdatum (oder dem Fälligkeitsdatum der vorherigen Erinnerung) verstreichen muss, bevor eine Erinnerung erstellt wird.

-   Das Datumsformat im Feld **Berechnung des Fälligkeitsdatums** bestimmt, wie das Fälligkeitsdatum auf der Erinnerung berechnet wird.

Die Datumsberechnungsformel kann maximal 20 Zeichen (Buchstaben und Zahlen) enthalten. Für die Berechnungszeiträume können die folgenden Abkürzungen verwendet werden.

|  Brief  |  Zeitspezifikationen  |
|----------|----------------------|
|U|Aktuell|
|T|Tag\(e\)|
|W|Woche\(n\)|
|M|Monat\(e\)|
|Q|Quartal\(e\)|
|J|Jahr\(e\)|

Datumsformeln können auf drei Arten erstellt werden.

Im folgenden Beispiel wird veranschaulicht, wie Sie **C**, für aktuell und eine Zeiteinheit verwenden.

|  Ausdruck  |  Bedeutung  |
|--------------|-----------|
|LW|Laufende Woche|
|LM|Laufender Monat|

Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zahl und eine Zeiteinheit verwenden. Eine Zahl darf nicht größer sein als 9999.

|  Ausdruck  |  Bedeutung  |
|--------------|-----------|
|10T|10 Tage ab heute|
|2W|2 Wochen ab heute|

Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zeiteinheit und eine Zahl verwenden.

|  Ausdruck  |  Bedeutung  |
|--------------|-----------|
|T10|Der nächste 10. eines Monats|
|WT4|Der nächste 4. einer Woche \(Donnerstag\)|

Das folgende Beispiel zeigt, wie Sie diese drei Formulare nach Bedarf kombinieren können.

|  Ausdruck  |  Bedeutung  |
|--------------|-----------|
|CM\+10D|Aktueller Monat\+ 10 Tage|

Das folgende Beispiel zeigt, wie Sie ein Minuszeichen verwenden können, um anzugeben, dass es sich um ein Datum in der Vergangenheit handelt.

|  Ausdruck  |  Bedeutung  |
|--------------|-----------|
|-1J|Heute vor einem Jahr|

> [!IMPORTANT]
>  Wenn für den Lagerort einen Grundkalender verwendet, wird das Datumsformular, das Sie eingeben, zum Beispiel das Feld **Transportzeit**, entsprechend der Kalenderarbeitstage interpretiert. Zum Beispiel entspricht **1W** sieben Arbeitstagen.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)  
[Eingeben von Kriterien in Filtern](ui-enter-criteria-filters.md)  

