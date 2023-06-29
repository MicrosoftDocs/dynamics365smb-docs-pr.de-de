---
title: Daten von mehreren Firmen konsolidieren
description: 'In diesem Artikel wird erklärt, wie Sie die Hauptbuchhaltungsposten von zwei oder mehr separaten Firmen (Tochtergesellschaften) zu einer konsolidierten Firma konsolidieren können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# <a name="consolidating-financial-data-from-multiple-companies"></a><a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidieren von Finanzdaten aus mehreren Unternehmen

Einige Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die den übergeordneten Organisationen Bericht erstatten müssen. In beiden Fällen verwenden die Buchhalter integrierte Tools, um die Finanzdaten leichter zu konsolidieren.  

Die Sachposten von zwei oder mehreren getrennten Unternehmen (Niederlassungen) können Sie einem konsolidierten Unternehmen konsolidieren. Jedes in eine Konsolidierung einbezogene einzelne Unternehmen wird als Konzernmandant bezeichnet. Das kombinierte Unternehmen wird konsolidiertes Unternehmen genannt.  

In das konsolidierte Unternehmen können Daten aus anderen Unternehmen im selben [!INCLUDE [prod_short](includes/prod_short.md)]-Mandant, aus Mandanten oder aus Dateien importiert werden.  

Wenn die Finanzauswertungen eines Konzernmandanten in einer anderen Währung als die des konsolidierten Unternehmen sind, müssen Sie Wechselkurse für die Konsolidierung einrichten.  

Konsolidierungen können wie folgt und für Folgendes durchgeführt werden:  

* Die Mandanten, die verschiedene Kontenpläne haben.  
* Unternehmen, die verschiedene Geschäftsjahre und verschiedene Währungen verwenden.  
* Entweder den vollständigen Betrag oder einen angegebenen Prozentsatz der Finanzdaten eines bestimmten Mandanten
* Mittels der Wechselkurse der anderen Währung in den einzelnen Sachkonten
* Unternehmen in anderen Buchhaltungs- und Geschäftsführungsprogrammen

Die Einrichtung des konsolidierten Unternehmens erfolgt auf die gleiche Weise wie die Einrichtung anderer Unternehmen. Der Kontenplan ist vom Kontenplan des Konzernmandanten unabhängig. Die Kontenpläne in den Geschäftsbereichen können voneinander abweichen. Sie richten eine Liste von Unternehmen ein, um die Buchhaltungsdaten vor der Konsolidierung zu konsolidieren und zu überprüfen, aus Dateien oder Datenbanken zu importieren und Konsolidierungsberichte zu generieren. Weitere Informationen finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Die Konsolidierung von Finanzdaten kann insbesondere in Verbindung mit Intergesellschaftsvorgängen relevant sein. Weitere Informationen finden Sie unter [Verwaltung von Intercompany-Transaktionen](intercompany-manage.md).

## <a name="use-the-consolidated-trial-balance-report"></a><a name="use-the-consolidated-trial-balance-report"></a>Verwendet den Bericht Konsolidierte Rohbilanz

Der Bericht **Konsolidierte Rohbilanz** kann Ihnen einen Überblick über die allgemeine Finanzstärke Ihres Gesamtunternehmens geben. Der Bericht Sachposten kombiniert aus jedem Ihrer Mandanten in einem neuen Mandanten, den Sie erstellen, um die konsolidierten Daten zu berücksichtigen. Dieses Unternehmen wird in der Regel als *Konsolidiertes Unternehmen* bezeichnet. Der Konsolidierungsmandant ist einfach ein Container für die konsolidierten Daten und hat keine Verbindung zu den aktuellen Geschäftsdaten. Die Unternehmen, die Sie im konsolidierten Unternehmen einschließen, wird zur **Geschäftseinheit** im Bericht. Weitere Informationen finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md). Wenn Sie vier Konzernmandanten oder weniger haben, können Sie auch den Bericht **Konsolidierte Rohbilanz (4)** verwenden.  

Der Bericht zeigt eine Zeile für jedes Konto und folgt der Struktur des Kontenplans. Ein Konto wird nicht angezeigt, wenn alle Beträge in der Zeile Null sind. Der Bericht zeigt die folgenden Informationen für jedes Konto an:

* Die Kontonummer und der Kontoname des Kontos
* Die Summen für das konsolidierte Unternehmen und für jede Geschäftseinheit. Endsummen können entweder als Bewegung oder als Saldo zum Datum angezeigt werden.
* Die im Konsolidierungsmandanten durchgeführten Eliminierungen. Eliminierungen werden immer für eine Periode entsprechend dem Geschäftsjahr des Konsolidierungsmandanten angezeigt.
* Die Endsumme für den Konsolidierungsmandanten nach Durchführung der Eliminierungen. Sie wird entweder als Bewegung oder als Saldo zum Datum angezeigt.

## <a name="consolidate-data"></a><a name="consolidate-data"></a>Daten konsolidieren

Die Übertragung der Zahlen aus den Konzernmandanten in das konsolidierte Unternehmen ist die tatsächliche *Konsolidierung*. Bevor Sie konsolidieren, sollten Sie prüfen, ob es Unterschiede zwischen den grundlegenden Informationen in den Konzernmandanten und im konsolidierten Unternehmen gibt. Es gibt zwei Berichte, die Sie verwenden können, um die Datenbank und die Datei zu testen.

### <a name="to-test-the-data-before-you-consolidate"></a><a name="to-test-the-data-before-you-consolidate"></a>Prüfen von Datenbanken vor der Konsolidierung

Testen Sie Ihre Daten, bevor Sie sie an den Konsolidierungsmandanten übertragen. [!INCLUDE[prod_short](includes/prod_short.md)] So überprüfen Sie Unterschiede zwischen den Informationen in den Konzernmandanten und dem Konsolidierungsmandanten Beispielsweise ob Kontonummern oder Dimensionscodes abweichen. Sie müssen Fehler korrigieren, bevor Sie den Bericht ausführen können. Sie können die Datenbank prüfen oder, wenn Sie Daten einer XML-Datei importieren, können Sie die Datei testen.  

1. Öffnen Sie den Konsolidierungsmandanten.  
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
3. Testen Sie die Datei und die Datenbank wie folgt:  

    * Um eine Datei zu testen, wählen Sie die **Datei prüfen** Aktion, geben Sie den Namen der Datei an zum Testen ein, und wählen Sie dann **Drucken** aus.  
    * Um die Datenbank zu testen, wählen Sie **Datenbank prüfen**.  

### <a name="run-the-consolidation"></a><a name="run-the-consolidation"></a>Die Konsolidierung ausführen

Nachdem Sie Ihre Daten getestet haben, können Sie diese an den Konsolidierungsmandanten übertragen.  

1. Melden Sie sich im Konsolidierungsmandanten an.  
2. Im Feld **Buchhalter-Rollencenter** wählen Sie Rollencenter **Konsolidierung ausführen** Aktion aus.  
3. Füllen Sie die entsprechenden Felder aus.  
4. Legen Sie im Abschnitt Filter einen Filter für den jeweiligen Konzernmandanten oder Unternehmensnamen fest.  
5. Optional planen Sie den Bericht so, dass er zu einer günstigen Zeit ausgeführt wird.  

## <a name="eliminate-repeated-transactions"></a><a name="eliminate-repeated-transactions"></a>Wiederholte Transaktionen verhindern

Nachdem sämtliche Mandanten konsolidiert wurden, müssen Sie alle Transaktionen suchen, die in mehreren Mandanten einmal aufgezeichnet wurden, und dann Eliminierungsposten buchen, um sie zu entfernen. Durchführen der Konsolidierungseliminierungen ist ein manuelles Verfahren.  

So verhindern Sie wiederholte Transaktionen:

1. Suchen Sie Transaktionen, die eventuell korrigiert werden müssen, und geben Sie Fibu Buch.-Blattzeilen ein, um sie zu beseitigen.
2. Führen Sie den Bericht **Konsolidierungseliminierungen** aus, um Ihnen zu helfen, die Auswirkungen der Fibu Buch.-Blattzeilen zu bewerten, bevor Sie buchen.
3. Buchen Sie die Regulierungstransaktionen.

Der **G/L-Konsolidierungseliminierungen**-Bericht zeigt eine vorläufige Probebilanz an, in der Sie die Folgen der Eliminierung von Buchungen simulieren können. Der Bericht vergleicht die Buchungen im Konsolidierungskreis mit den im Hauptbuch gebuchten Eliminierungen.

Bevor ein Konzernmandant in dem Bericht berücksichtigt werden kann, muss er auf der Seite **Konzernmandanten** eingerichtet werden. Das Feld **Konsolidieren** muss ausgewählt werden.

Für jedes Konto wird eine eigenen Zeile entsprechend der Struktur im Kontenplan erstellt. Ein Konto wird nicht angezeigt, wenn alle Beträge in der Zeile Null sind. Folgende Informationen werden für jedes Konto angegeben:

* Kontonummer.
* Kontoname.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen oder mehrere Konzernmandantencodes angegeben haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der die gewählten Konzernmandanten und Eliminierungen nicht enthalten sind. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der nur die Eliminierungen nicht enthalten sind.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen Konzernmandantencode angegeben haben, wird eine Summe für die importierten Posten des Konzernmandanten angezeigt. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird eine Summe der gebuchten Eliminierungen des Konsolidierungsmandanten angezeigt.
* Die Endsumme für den Konsolidierungsmandanten mit allen Konzernmandanten und allen gebuchten Eliminierungen.
* Die im Konsolidierungsmandanten durchgeführten Eliminierungen. Das heißt, die Einträge im allgemeinen Journal, das auf der Anforderungsseite ausgewählt wird.
* Der aus dem Fibu Buch.-Blatt kopierte Buchungstext.
* Die Endsumme für den Konsolidierungsmandanten nach Durchführung der Eliminierungen, soweit diese gebucht wurden.

## <a name="export-and-import-consolidated-data-between-databases"></a><a name="export-and-import-consolidated-data-between-databases"></a>Konsolidierte Daten zwischen Datenbanken exportieren und importieren

Wenn sich ein Konzernmandant in einer anderen Datenbank befindet, müssen Sie die Konsolidierungsdaten in eine Datei exportieren, bevor diese konsolidiert werden können. Jeder Mandant muss separat konsolidiert werden. Zu diesem Zweck wird in der Anwendung die Stapelverarbeitung **Konsolidierung exportieren** verwendet.  

> [!TIP]
> Verwenden Sie denselben Prozess, um konsolidierte Daten zu exportieren, die an Dynamics 365 Finance übermittelt werden müssen, wie z. B. wenn der aktuelle Konzernmandant eine Niederlassung ist und das übergeordnete Unternehmen Dynamics 365 Finance nutzt.

Nachdem der Batchauftrag ausgeführt wurde, sind alle Posten in den einzelnen Sachkonten verarbeitet. Für jede Kombination aus ausgewählten Dimensionen und Datum wird der Inhalt des Felds **Betrag** der Posten summiert und exportiert. Die nächste Kombination der ausgewählten Dimensionen und des Datums mit derselben Kontonummer wird verarbeitet. Dann werden die Kombinationen in der nächsten Kontonummer verarbeitet und so weiter.  

Die exportierten Posten enthalten die folgenden Felder: **Kontonr.**, **Buchungsdatum** und **Betrag**. Wenn auch Dimensionsdaten exportiert wurden, sind ebenfalls Dimensionscodes und Dimensionswerte enthalten.  

1. Für jede exportierte Zeile wird, sofern die Summe des **Betrag**-Felds ein Sollbetrag ist, die im **Konsol. Sollkonto** des Konzernmandanten eingerichtete Kontonummer in die Zeile exportiert. Wenn die Summe ein Habenbetrag ist, wird die entsprechende Nummer im Feld **Konsol. Habenkonto** in die Zeile exportiert.  
2. Das für jede exportierte Zeile verwendete Datum ist entweder das Enddatum der Periode oder, wenn die Übertragung täglich erfolgt, das genaue Berechnungsdatum.  
3. Bei dem für den Posten exportierten Dimensionswert handelt es sich um den Dimensionswert des Konsolidierungsmandanten, der im Feld **Konsolidierungscode** für diesen Dimensionswert eingerichtet ist. Wurde im Feld **Konsolidierungscode** für diesen Dimensionswert kein Dimensionswert des Konsolidierungsmandanten eingerichtet, wird der Dimensionswert selbst in die Zeile exportiert.  
4. Die XML-Dateien enthalten auch die Währungswechselkurse innerhalb der Konsolidierungsperiode. Diese Wechselkurse sind in einem eigenen Abschnitt zu Beginn der Datei aufgeführt.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
