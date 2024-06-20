---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Wenn Sie Datums-/Uhrzeitangaben eingeben, die aus einem kombinierten Datum und einer Uhrzeit in einem Feld bestehen, müssen Sie ein Leerzeichen zwischen dem Datum und der Uhrzeit eingeben. Der Datumsteil kann nur Stellen in Form von den offiziellen Datumstrennzeichen Ihrer Regionseinstellung enthalten. Die Uhrzeit kann Stellen um die AM/AM-Angabe enthalten in relevanten regionalen Einstellungen.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

In der folgenden Tabelle finden Sie eine Übersicht über die Möglichkeiten zum Eingeben von Datums-/Uhrzeitangaben sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11.aktueller Monat.aktuelles Jahr 12:00:00|
|1112 12|11-12-aktuelles Jahr 12:00:00|
|"h" für heute|heutiges Datum 00:00:00|
|t Zeit|heutiges Datum aktuelle Zeit|
|h 10:30|heutiges Datum 10:30:00|
|h 3:3:3|heutiges Datum 03:03:03|
|"a" oder "Arbeitsdatum"|das Arbeitsdatum 00:00:00|
|"m" oder "Montag"|Montag der aktuellen Woche 00:00:00|
|"d" oder "Dienstag"|Dienstag der aktuellen Woche 00:00:00|
|"mi" oder "Mittwoch"|Mittwoch der aktuellen Woche 00:00:00|
|"do" oder "Donnerstag"|Donnerstag der aktuellen Woche 00:00:00|
|"f" oder "Freitag"|Freitag der aktuellen Woche 00:00:00|
|"s" oder "Sonnabend"|Samstag der aktuellen Woche 00:00:00|
|"so" oder "Sonntag"|Sonntag der aktuellen Woche 00:00:00|
|di 10:30|Dienstag der aktuellen Woche 10:30:00|
|di 3:3:3|Dienstag der aktuellen Woche 03:03:03|
|d23 h|Dienstag der Woche 23 des Jahres des Arbeitsdatums, aktuelle Uhrzeit|
|d23|Dienstag von Woche 23 des Arbeitsjahres|
|d 23|Heute 23:00:00|
|d-1|Dienstag von Woche 1 des Arbeitsjahres|


