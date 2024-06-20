---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Wenn Sie eine Rechnung von einer Firma in einer Fremdwährung erhalten, ist es relativ einfach, den Wert der Rechnung in lokaler Währung (LCY) auf der Grundlage des heutigen Wechselkurses zu berechnen. Allerdings ist die Rechnung oft mit Zahlungsbedingungen versehen, sodass Sie die Zahlung auf ein späteres Datum verschieben können, was einen potenziell anderen Währungssatz impliziert. Dieses Problem in Kombination mit der Tatsache, dass die Bankwährungskurse immer von den offiziellen Währungskursen abweichen, macht es unmöglich, den genauen Betrag in lokaler Währung (LCY) vorherzusagen, der zur Deckung der Rechnung erforderlich ist. Wenn sich das Fälligkeitsdatum der Rechnung in den nächsten Monat erstreckt, müssen Sie möglicherweise auch den Betrag in Hauswährung (LCY) am Ende des Monats neu bewerten. Die Währungsanpassung ist notwendig, weil der neue LCY-Wert, der zur Deckung des Rechnungsbetrags erforderlich ist, anders sein könnte und sich die Schulden der Firma gegenüber dem Kreditor möglicherweise geändert haben. Der neue LCY-Betrag kann höher oder niedriger sein als der vorherige Betrag und stellt daher einen Gewinn oder einen Verlust dar. Da die Rechnung jedoch noch nicht bezahlt wurde, wird der Gewinn oder Verlust als *unrealisiert* betrachtet. Später wird die Rechnung bezahlt, und die Bank hat sich mit dem tatsächlichen Satz für die Zahlung zurückgemeldet. Erst jetzt wird der *realisierte* Gewinn oder Verlust berechnet. Dieser nicht realisierte Gewinn oder Verlust wird dann storniert und stattdessen wird der realisierte Gewinn oder Verlust gebucht.

Im folgenden Beispiel geht am 1. Januar eine Rechnung mit dem Währungsbetrag von 1000 ein. Zu diesem Zeitpunkt beträgt der Währungssatz 1,123.

|Datum|Aktion|Währungsbetrag|Belegkurs|MW-Betrag auf Beleg|Regulierungsrate|Unrealisierter Kursgewinn|Zahlungskurs|Realisierter Kursverlust|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturieren**|1000|1,123|1123|||||
|1/31|**Regulierung**|1000||1125|1,125|2|||
|2/15|**Anpassungsrücksetzung bei Zahlung**|1000||||-2|||
|2/15|**Zahlung**|1000||1120|||1,120|-3|

Am Ende des Monats wird eine Währungsanpassung durchgeführt, bei der der Anpassungswährungskurs auf 1,125 festgelegt wurde, was einen nicht realisierten Gewinn von 2 auslöst.

Zum Zeitpunkt der Zahlung weist der tatsächlich bei der Banktransaktion registrierte Währungskurs einen Währungskurs von 1,120 auf.

Hier liegt eine nicht realisierte Transaktion vor und wird daher mit der Zahlung storniert.

Abschließend wird die Zahlung registriert und der tatsächliche Verlust auf das realisierte Verlustkonto gebucht.
