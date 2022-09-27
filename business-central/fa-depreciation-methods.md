---
title: Abschreibungsmethoden für Anlagen
description: Erfahren Sie mehr über die verschiedenen integrierten Methoden zur Abschreibung von Anlagen in der Standardversion von Business Central, die acht Methoden enthält.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: 5629, 5633
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: f4f748e15a3bc3b911488cff74a7e51be4a75142
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535074"
---
# <a name="depreciation-methods-for-fixed-assets"></a>Abschreibungsmethoden für Anlagen

In der Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] stehen acht Abschreibungsmethoden zur Verfügung:  

* Linear  
* Degressiv 1  
* Degressiv 2  
* Degr1/Linear  
* Degr2/Linear  
* Tabelle  

  > [!NOTE]  
  > Geben Sie Ihre eigene Abschreibungsmethode an, indem Sie Abschreibungstabellen definieren. Informationen zur Anwendung einer benutzerdefinierten Abschreibungsmethode finden Sie unter [Benutzerdefinierte Abschreibungsmethode festlegen](fa-how-setup-user-defined-depreciation-method.md).
* Manuell  

  > [!NOTE]  
  > Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden z. B. Land. Sie müssen die Beschreibung im Anlagen Fibu Buch.-Blatt eingeben. Die Stapelverarbeitung **Abschreibung berechnen** berücksichtigt keine Anlagen mit dieser Abschreibungs-Methode.  
* US-Halbjahresregel  

  > [!NOTE]  
  > Wenn diese Methode verwendet wird, wird eine Anlage jedes Jahr mit dem gleichen Betrag abgeschrieben.  

## <a name="straight-line-depreciation"></a>Lineare Abschreibung

Wenn Sie die Methode "Linear" verwenden, müssen Sie eine der folgenden Optionen im Anlagen-AfA-Buch angeben:  

* Die Nutzungsdauer (in Jahren oder Monaten) oder das Enddatum der Nutzungsdauer.  
* Einen festen jährlichen Prozentsatz  
* Einen festen jährlichen Betrag  
* AfA Periode  

### <a name="depreciation-period"></a>AfA Periode

Falls Sie eine AfA Periode angeben (Anzahl der AfA Jahre, Anzahl der AfA Monate oder das Enddatum der Nutzungsdauer), verwendet die Anwendung die folgende Formel, um den AfA Betrag zu berechnen:  

*AfA Betrag = ((Buchwert – Restwert) x Anzahl AfA Tage) / Verbleibende AfA Tage*  

Die verbleibenden AfA-Tage werden als die Gesamtzahl der AfA-Tage minus der Anzahl der Tage zwischen dem Startdatum Normal-AfA und dem letzten Anlagen-Buchungsdatum berechnet.  

Der Buchwert kann durch gebuchte Zuschreibungen, AfA, benutzerdefinierter Beträge 1 oder 2 reduziert werden; abhängig davon, ob das Feld **In AfA-Berechnung enthalten** deaktiviert ist und ob das Feld **Teil d. Buchwerts** auf der Seite **Anlagenbuchungsart Einr.** aktiviert ist. Diese Berechnung stellt sicher, dass die Anlage zum angegebenen Enddatum vollständig abgeschrieben ist.  

### <a name="fixed-yearly-percentage"></a>Fester jährlicher Prozentsatz

Wenn Sie einen festen jährlichen Prozentsatz angeben, verwendet die Anwendung die folgende Formel für die Berechnung des AfA-Satzes.  

*AfA Betrag = (Linear % x AfA Basis x Anzahl AfA Tage) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a>Fester jährlicher Betrag

Wenn Sie einen festen jährlichen Betrag angeben, verwendet die Anwendung die folgende Formel, um den AfA-Satz zu berechnen:  

*AfA Betrag = (Fester AfA-Betrag x Anzahl AfA Tage) / 360*  

### <a name="example---straight-line-depreciation"></a>Beispiel – Lineare Abschreibung

Eine Anlage hat Anschaffungskosten von MW 100.000. Die erwartete Lebensdauer ist 8 Jahre. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Für dieses Beispiel sieht der Anlagenposten folgendermaßen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 06/30/20 |Abschreibungen |180 |-6.250,00 |93,750.00 |
| 12/31/20 |Abschreibungen |180 |-6.250,00 |87,500.00 |
| 06/30/21 |Abschreibungen |180 |-6.250,00 |81,250.00 |
| 12/31/21 |Abschreibungen |180 |-6.250,00 |75,000.00 |
| 06/30/27 |Abschreibungen |180 |-6.250,00 |6,250.00 |
| 12/31/27 |Abschreibungen |180 |-6.250,00 |0 |

## <a name="declining-balance-1-depreciation"></a>Abschreibungsmethode "1 % degressiv"

Hierbei handelt es sich um eine beschleunigte Abschreibungsmethode, bei der der größte Teil der Kosten einer Anlage in den ersten Jahren der Nutzungsdauer abgeschrieben wird. Wenn Sie diese Methode verwenden, müssen Sie einen festen jährlichen Prozentsatz eingeben.  

Die folgende Formel zur Berechnung des AfA-Betrages ist:  

*AfA Betrag = (Degressive AfA % * Anzahl AfA Tage * AfA Basis) / (100 * 360)*  

Die AfA Basis wird als der Buchwert minus der gebuchten AfA seit dem Startdatum des aktuellen Geschäftsjahres berechnet.  

Der gebuchte AfA-Betrag kann Posten mit verschiedenen Buchungsarten enthalten (erhöhte AfA, Sonder-AfA und benutzerdefinierte AfA), die seit dem Startdatum des aktuellen Geschäftsjahrs gebucht worden sind. Diese Buchungsarten sind in dem gebuchten AfA Betrag enthalten, wenn Häkchen in den Feldern **AfA-Art** und **Teil d. Buchwerts** auf der Seite **Anlagenbuchungsart Einr.** gesetzt sind.  

### <a name="example---declining-balance-1-depreciation"></a>Beispiel – Abschreibungsmethode "1 % degressiv"

Eine Anlage hat Anschaffungskosten von MW 100.000. Das Feld **Degressive AfA %** hat den Wert 25. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Die nachstehende Tabelle zeigt, wie die Anlagenposten-Einträge aussehen.  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 06/30/20 |Abschreibungen |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Abschreibungen |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Abschreibungen |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Abschreibungen |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Abschreibungen |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Abschreibungen |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Abschreibungen |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Abschreibungen |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Abschreibungen |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Abschreibungen |180 |-3.955,08 |23,730.46 |

Berechnungsmethode:  

* Jahr 1: *25 % von 100.000 = 25.000 = 12.500 + 12.500*

* Jahr 2: *25 % von 75.000 = 18.750 = 9.375 + 9.375*

* Jahr 3: *25 % von 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

Die Berechnung erfolgt bis der Buchwert gleich dem endgültigen Rundungsbetrag oder dem von Ihnen angegebenen Restwert ist.  

## <a name="declining-balance-2-depreciation"></a>Abschreibungsmethode "2 % degressiv"

Die Methoden Degressiv 1 und Degressiv 2 berechnen den gleichen Gesamt AfA-Betrag für jedes Jahr. Falls Sie die Stapelverarbeitung **AfA berechnen** mehr als einmal jährlich ausführen, resultiert die Methode "Degressiv 1" in gleichen AfA Beträgen für die einzelnen Perioden. Die Methode "Degressiv 2" hat in diesem Fall fallende Beträge in den einzelnen Perioden zur Folge.  

### <a name="example---declining-balance-2-depreciation"></a>Beispiel – Abschreibungsmethode "2 % degressiv"

Eine Anlage hat Anschaffungskosten von MW 100.000. Das Feld **Degressive AfA %** hat den Wert 25. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt. Die Anlagenposten sehen folgendermaßen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA)|100,000.00 |100,000.00 |
| 06/30/20 |Abschreibungen |180 |-13.397,46 |86,602.54 |
| 12/31/20 |Abschreibungen |180 |-11.602,54 |75,000.00 |
| 06/30/21 |Abschreibungen |180 |-10.048,09 |64,951.91 |
| 12/31/21 |Abschreibungen |180 |-8.701,91 |56,250.00 |

Berechnungsmethode:  

* *BW* = Buchwert  
* *AT* = Anzahl AfA-Tage  
* *DAP* = Degressive AfA Prozent  
* *P* = *DBP*/100  
* *D* = *ND*/360  

Die Formel zur Berechnung des AfA-Betrages ist:  

*DA* = *BV* x (1 – (1 –P)<sup>D</sup>)

Die Abschreibungswerte lauten:  

| Datum | Berechnung |
| --- | --- |
| 06/30/20 |DA = 100.000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 13.397,46 |
| 12/31/20 |DA = 86.602,54 x (1 -(1 - 0,25)<sup>0,5</sup>) = 11.602,54 |
| 06/30/21 |DA = 75.000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 10.048,09 |
| 12/31/21 |DA = 64.951,91 x (1 -(1 - 0,25)<sup>0,5</sup>) = 8.701,91 |

## <a name="db1sl-depreciation"></a>Degressiv/Lineare AfA 1

"Degr1/Linear" ist eine abgekürzte Kombination von "Degressiv 1" und "Linear". Die Berechnung erfolgt bis der Buchwert gleich dem endgültigen Rundungsbetrag oder dem von Ihnen angegebenen Restwert ist.  

Die Stapelverarbeitung **AfA berechnen** berechnet einen linearen Betrag und einen degressiven Betrag. Nur der größere dieser beiden Beträge wird in das Buch.-Blatt übertragen.  

Die Anwendung kann die degressiven Berechnungen unter der Verwendung von verschiedenen Prozentsätzen durchführen.  

Wenn Sie diese Methode verwenden, müssen Sie die geschätzte Nutzungsdauer und einen degressiven Prozentsatz auf der Seite **Anlagen-AfA-Bücher** eingeben.  

### <a name="example---db1-sl-depreciation"></a>Beispiel – Degressiv-Lineare AfA 1

Eine Anlage hat Anschaffungskosten von MW 100.000. Im Fenster **Anlagen-AfA-Bücher** enthält die Seite **Degressive AfA %** den Wert 25 und das Feld **Nutzungsdauer i. Jahren** den Wert 8. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Die Anlagenposten sehen folgendermaßen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 06/30/20 |Abschreibungen |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Abschreibungen |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Abschreibungen |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Abschreibungen |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Abschreibungen |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Abschreibungen |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Abschreibungen |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Abschreibungen |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Abschreibungen |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Abschreibungen |180 |-3.955,08 |23,730.46 |
| 06/30/25 |Abschreibungen |180 |-3.955,08 |19.775,38 Linear |
| 12/31/25 |Abschreibungen |180 |-3.955,08 |15.820,30 Linear |
| 06/30/26 |Abschreibungen |180 |-3.955,08 |11.865,22 Linear |
| 12/31/26 |Abschreibungen |180 |-3.955,07 |7.910,15 Linear |
| 06/30/27 |Abschreibungen |180 |-3.955,08 |3.955,07 Linear |
| 12/31/27 |Abschreibungen |180 |-3.955,07 |0,00 Linear |

`SL` nach dem Buchwert bedeutet, dass die lineare Abschreibung verwendet worden ist.  

Berechnungsmethode:  

* Jahr 1 (2020):  

    *Degressiv Betrag: 25% von 100.000 = 25.000=12.500+12.500*  

    *Linear Betrag = 100.000/8=12.500=6.250+6.250*  

    Es wird der degressive Betrag verwendet, da es sich um den größeren Betrag handelt.  

* Jahr 5 (2025):  

    *Degressiv Betrag: 25% von 23,730.46 = 4,943.85=2,471.92+2,471.92*  

    *Linear Betrag = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

    Es wird der lineare Betrag verwendet, da es sich um den größeren Betrag handelt.  

## <a name="half-year-convention-depreciation"></a>AfA 1 unter Verwendung der US-Halbjahresregel

Die US-Halbjahresregel wird nur dann angewendet, wenn Sie ein Häkchen auf der Seite **US-Halbjahresregel verwenden** im **Anlagen-AfA-Buch** gesetzt haben.  

Diese AfA-Methode kann im Zusammenhang mit folgenden AfA-Methoden in der Anwendung verwendet werden:  

* Linear  
* Degressiv 1  
* Degr1/Linear  

Wenn die Halbjahresregel angewendet wird, hat eine Anlage sechs AfA Monate in dem ersten Geschäftsjahr der Abschreibung, unabhängig vom Inhalt des Feldes **Abschreibungsdatum**.  

> [!NOTE]  
> Die Nutzungsdauer einer Anlage, die nach dem ersten Geschäftsjahr verbleibt, enthält immer ein halbes Jahr, wenn die US-Halbjahresregel verwendet wird. Damit die Halbjahresregel korrekt angewendet wird, muss dass Feld **Enddatum d. Nutzungsdauer** auf der Seite **Anlagen-AfA-Buch** immer ein Datum enthalten, das genau sechs Monate vor dem Enddatum des Geschäftsjahres liegt, in dem die Anlage vollständig abgeschrieben ist.  

### <a name="example---half-year-convention-depreciation"></a>Beispiel – AfA 1 unter Verwendung der US-Halbjahresregel

Eine Anlage hat Anschaffungskosten von MW 100.000. Das **Startdatum Normal-AfA** ist der 01.03.20. Die erwartete Lebensdauer ist fünf Jahre, daher muss das Feld **Enddatum d. Nutzungsdauer** den Wert 30.06.25 enthalten. Die Stapelverarbeitung **AfA berechnen** wird jährlich ausgeführt. Dieses Beispiel basiert auf einem Kalenderjahr als Geschäftsjahr.  

Die Anlagenposten sehen folgendermaßen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 03/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 12/31/20 |Abschreibungen |270 |-10.000,00 |90,000.00 |
| 12/31/21 |Abschreibungen |360 |-20.000,00 |70,000.00 |
| 12/31/22 |Abschreibungen |360 |-20.000,00 |50,000.00 |
| 12/31/23 |Abschreibungen |360 |-20.000,00 |30,000.00 |
| 12/31/24 |Abschreibungen |360 |-20.000,00 |10,000.00 |
| 12/31/25 |Abschreibungen |180 |-10.000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Beispiel – Degressiv/Lineare AfA 1 unter Verwendung der US-Halbjahresregel

Eine Anlage hat Anschaffungskosten von MW 100.000. Das **Startdatum Normal-AfA** ist der 11.01.20. Die erwartete Lebensdauer ist fünf Jahre, daher muss das Feld **Enddatum d. Nutzungsdauer** den Wert 30.06.25 enthalten. Auf der Seite **Anlagen-AfA-Bücher** enthält das Feld **Degressive AfA %** den Wert 40. Die Stapelverarbeitung **AfA berechnen** wird jährlich ausgeführt. Dieses Beispiel basiert auf einem Kalenderjahr als Geschäftsjahr.  

Die Anlagenposten sehen folgendermaßen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/11/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 12/31/20 |Abschreibungen |60 |-20.000,00 |80,000.00 |
| 12/31/21 |Abschreibungen |360 |-32.000,00 |48,000.00 |
| 12/31/22 |Abschreibungen |360 |-19.200,00 |28,800.00 |
| 12/31/23 |Abschreibungen |360 |-11.520,00 |17,280.00 |
| 12/31/24 |Abschreibungen |360 |-11.520,00 |5.760,00 Linear |
| 12/31/25 |Abschreibungen |180 |-5.760,00 |0,00 Linear |

`SL` nach dem Buchwert bedeutet, dass die lineare Abschreibung verwendet worden ist.  

Berechnungsmethode:  

* Jahr 1:  

    *Degressiv Betrag = Betrag des gesamten Jahres = 40% von 100.000 = 40.000.* Daher für ein halbes Jahr 40.000 / 2 = 20.000  

    *Linear Betrag = Betrag des gesamten Jahres = 100.000 / 5=20.000.* Daher für ein halbes Jahr = 20.000 / 2 =10.000  

    Es wird der degressive Betrag verwendet, da es sich um den größeren Betrag handelt.  

* Jahr 5 (2024):  

    *Degressiver Betrag = 40% von 17,280.00 = 6,912.00*  

    *Linearer Betrag = 28,800 / 1.5 = 11,520.00*  

    Es wird der lineare Betrag verwendet, da es sich um den größeren Betrag handelt.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Kopieren von Posten in weitere AfA-Bücher

Falls Sie über 3 AfA-Bücher B1, B2 und B3 verfügen und Sie Posten aus B1 in B2 und B3 kopieren möchten, können Sie ein Häkchen in dem Feld **Kopien ermöglichen** in der AfA-Buchkarte von B2 und B3 setzen. Dies kann hilfreich sein, wenn das AfA-Buch B1 in die Finanzbuchhaltung integriert ist und das Anlagen-Fibu Buch.-Blatt verwendet, während die AfA-Bücher B2 und B3 nicht in der Finanzbuchhaltung integriert sind und das Anlagen Buch.-Blatt verwenden.  

Wenn Sie einen Posten in B1 im Anlagen-Fibu Buch.-Blatt erstellen und dann ein Häkchen in dem Feld **Kopiervorgang aktivieren** gesetzt haben, kopiert die Anwendung den Posten in die Bücher B2 und B3 im Anlagen Buch.-Blatt, wenn Sie den Posten buchen.  

> [!NOTE]  
> Es ist nicht möglich in dem gleichen Buch.-Blatt und der gleichen Buch.-Blattvorlage zu kopieren, aus der Sie kopieren. Wenn Sie Posten im Fibu Buch.-Blatt buchen, können Sie diese über eine weitere Stapelverarbeitung in ein Anlagen Buch.-Blatt oder ein Anlagen Fibu Buch.-Blatt kopieren.  

> [!NOTE]  
> Es ist nicht möglich, im Anlagen Fibu Buch.-Blatt und im Anlagen Buch-Blatt dieselbe Nummernserie zu verwenden. Wenn Sie im Anlagen Fibu Buch.-Blatt Posten buchen, müssen Sie das Feld **Belegnr.** leer lasssen. Wenn Sie in das Feld eine Nummer eingeben, wird die Nummer im Anlagen Buch.-Blatt dupliziert. Sie müssen die Belegnummer manuell ändern, bevor Sie das Buch.-Blatt buchen können.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/configure-depreciation-books/)

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[Finanzen](finance.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
