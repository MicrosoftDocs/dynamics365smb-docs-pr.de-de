---
title: FA-Benutzerdefinierte Abschreibungsmethode festlegen
description: 'In Business Central können Sie eine benutzerdefinierte Abschreibungsmethode anwenden, um die Abschreibungsmethode für Ihre Anlage auf der Seite Anlagekarte zu definieren.'
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
---

# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Festlegen von Anlagen mit benutzerdefinierten Abschreibungsmethoden

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, um die benutzerdefinierten Abschreibungsmethoden wie hier beschrieben festzulegen.

Für jede benutzerdefinierte Methode verwenden Sie die Seite **AfA-Tabellen**, wo Sie einen Abschreibungsprozentsatz für jede Periode (Monat, Quartal, Jahr oder Buchhaltungsperiode) eingeben müssen. Wenn Sie dann einem Anlagevermögen ein Abschreibungsbuch mit einer benutzerdefinierten Methode zuweisen, müssen Sie die Felder **Startdatum Normal-AfA** und **Abschreibungsbeginn** auf der Seite **Anlagen-AfA-Bücher** für das jeweilige Anlagevermögen festlegen.  

Die Formel zur Berechnung des AfA-Betrages ist:  

*AfA Betrag = (AfA % x Anzahl AfA Tage x AfA Basis) / (100 x 360)*


> [!NOTE]  
> Während das Datum im Feld **Erstes benutzerdefiniertes Depr. Date** verwendet wird, um die Zeitintervalle zu bestimmen, ist es das **Abschreibungsstartdatum**, das zur Bestimmung der Anzahl der Abschreibungstage verwendet wird. Wenn das **Erste benutzerdefinierte Depr. Datum** vor dem **Abschreibungs-Startdatum** liegt, wird der Prozentsatz für die erste Periode in der Abschreibungstabelle nur teilweise verwendet, wenn das Programm die erste Abschreibung berechnet. Das bedeutet, dass die Anlage bis zum Ende der letzten Periode nicht vollständig abgeschrieben ist.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>So ordnen Sie einer Anlage mit einer benutzerdefinierten Abschreibungsmethode ein Abschreibungsbuch zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie ein Anlagen-AfA-Buch einrichten möchten.
3. Wählen Sie die Aktion **Zuordnen**, dann **Anlage** und dann **AfA-Bücher**. Dies öffnet die Seite **FA Abschreibungs-Bücher**.

   Standardmäßig sind einige der Felder, die gemäß der folgenden Anleitung ausgefüllt werden müssen, ausgeblendet, sodass Sie sie einblenden müssen. Dazu müssen Sie die Seite personalisieren. Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Banner Personalisierung](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Wählen Sie im Feld **Abschreibungsmethode** die Option **Benutzerdefiniert**.
5. Wählen Sie im Feld **Abschreibungs-Tabellencode** die **Abschreibungs-Tabelle**, die Sie verwenden möchten.
6. Wählen Sie im Feld **Abschreibungsstartdatum** das Startdatum für die Abschreibungsberechnung.
7. Wenn Sie eine benutzerdefinierte Methode verwenden, muss das Feld **Erstes benutzerdefiniertes Depr. Date** auf ein Datum festgelegt werden, das gleich oder früher als das Feld **Abschreibungsstartdatum** ist. Wenn Sie in der Abschreibungstabelle einen Wert im Feld **Periodenlänge** gewählt haben, muss das Datum im Feld **Erste benutzerdefinierte Abschreibung Datum** muss das Anfangsdatum einer Buchhaltungsperiode sein.
8. Füllen Sie entweder das Feld **Anzahl Abschreibungsjahre** oder das Feld **Schreibungsenddatum** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>So richten Sie benutzerdefinierte AfA-Methoden ein

Auf der Seite **Abschreibungstabelle** können Sie benutzerdefinierte AfA-Methoden einrichten. Beispielsweise können Sie die Abschreibung basierend auf der Stückzahl einrichten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **AfA-Tabellen** ein, und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **AfA-Tabelle Übersicht** wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie auf der Seite **AfA-Tabellen-Karte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Verwenden Sie die Funktion **Dezimalstellen-Summentabelle erstellen** zum Definieren einer Abschreibungstabelle basierend auf der Methode *Summe der Ziffern*.

Mit der Methode *Summe der Ziffern* wird, wenn ein Anlagevermögen über einen Zeitraum von 4 Jahren abgeschrieben wird, die Abschreibung für jedes Jahr folgendermaßen berechnet:

Quersumme = 1 + 2 + 3 + 4 = 10 Abschreibungen:

* Jahr 1 = 4/10  
* Jahr 2 = 3/10  
* Jahr 3 = 2/10  
* Jahr 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Abschreibung basierend auf der Stückzahl

Diese benutzerdefinierte Methode kann auch verwendet werden, um eine Abschreibung nach der produzierten Stückzahl durchzuführen, zum Beispiel für Produktionsmaschinen, die eine von der Stückzahl abhängige Lebensdauer haben. Auf der Seite **AfA-Tabellen** können Sie die Stückzahl eingeben, die innerhalb einer Periode (Monat, Quartal, Jahr oder Buchhaltungsperiode) produziert werden kann.  

### <a name="example---user-defined-depreciation"></a>Beispiel - Benutzerdefinierte AfA

Sie verwenden eine Abschreibungsmethode, die es Ihnen erlaubt, Anlagen für steuerliche Zwecke schneller abzuschreiben.  

Sie könnten für steuerliche Zwecke die folgenden Sätze für eine Anlage mit einer Lebensdauer von drei Jahren verwenden:  

* Jahr 1: 25 %  
* Jahr 2: 38 %  
* Jahr 3: 37 %  

Die Anschaffungskosten betragen MW 100.000 und die Lebensdauer für die Abschreibung ist fünf Jahre. Die Abschreibung wird manuell berechnet.  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 12/31/20 |Abschreibungen |360 |-25.000,00 |75,000.00 |
| 12/31/21 |Abschreibungen |360 |-38.000,00 |37,000.00 |
| 12/31/22 |Abschreibungen |360 |-37.000,00 |0 |
| 12/31/23 |Abschreibungen |"Keine" |"Keine" |0 |
| 12/31/24 |Abschreibungen |"Keine" |"Keine" |0 |

Im vorherigen Beispiel würden die beiden Felder **Startdatum Benutzerdef. AfA** und **Startdatum Normal-AfA** auf 01/01/20 auf der Seite **Anlagen-AfA-Bücher** für das jeweilige Anlagevermögen festgelegt werden. Hätte das Feld **Startdatum Benutzerdef. AfA** jedoch den Wert "01/01/20" und das Feld **Startdatum Normal-AfA** den Wert "01/04/20" enthalten, wäre das Ergebnis folgendermaßen ausgefallen:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anschaffungskosten |(Startdatum Normal-AfA) |100,000.00 |100,000.00 |
| 12/31/20 |Abschreibungen |270 |-18.750,00 |81,250.00 |
| 12/31/21 |Abschreibungen |360 |-38.000,00 |42,250.00 |
| 12/31/22 |Abschreibungen |360 |-37.000,00 |6,250.00 |
| 12/31/23 |Abschreibungen |90 |-6.250,00 |0 |
| 12/31/24 |Abschreibungen |"Keine" |"Keine" |0 |


## <a name="see-also"></a>Weitere Informationen
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Richten Sie eine neue Anlagenkarte ein](fa-how-setup-depreciation.md)  
[Abschreibungsmethoden für Anlagen](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
