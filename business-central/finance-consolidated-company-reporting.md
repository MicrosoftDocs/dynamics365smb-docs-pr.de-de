---
title: Daten von mehreren Firmen konsolidieren
description: 'In diesem Artikel wird erklärt, wie Sie die Hauptbuchhaltungsposten von zwei oder mehr separaten Firmen (Tochtergesellschaften) zu einer konsolidierten Firma konsolidieren können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidieren von Finanzdaten aus mehreren Unternehmen

Einige Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die den übergeordneten Organisationen Bericht erstatten müssen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet Buchhaltern Tools, die ihnen helfen, Hauptbucheinträge von zwei oder mehr Unternehmen (Tochtergesellschaften) in ein konsolidiertes Unternehmen zu übertragen.  

Jedes in eine Konsolidierung einbezogene Unternehmen wird als Konzernmandant bezeichnet. Die Gesellschaft, in der Sie die Daten zusammenfassen, wird als konsolidierte Gesellschaft bezeichnet.  

Sie können Finanzdaten von Tochtergesellschaften in das konsolidierte Unternehmen übertragen, auch wenn die Tochtergesellschaften [!INCLUDE [prod_short](includes/prod_short.md)] in unterschiedlichen Umgebungen verwenden. Weitere Informationen zum Herstellen einer Verbindung mit anderen Umgebungen finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md#busunit).

Wenn die Finanzauswertungen eines Konzernmandanten in einer anderen Währung als die des konsolidierten Unternehmen sind, müssen Sie Wechselkurse für die Konsolidierung einrichten. Weitere Informationen zu Wechselkursen für Konsolidierungen finden Sie unter [Firmenkonsolidierung einrichten](finance-consolidated-company-reporting-setup.md#exchrates).  

Konsolidierungen können wie folgt und für Folgendes durchgeführt werden:  

* Die Mandanten, die verschiedene Kontenpläne haben.  
* Unternehmen, die verschiedene Geschäftsjahre und verschiedene Währungen verwenden.  
* Entweder den vollständigen Betrag oder einen angegebenen Prozentsatz der Finanzdaten eines bestimmten Mandanten.
* Mittels der Wechselkurse der anderen Währung in den einzelnen Sachkonten.
* Unternehmen in anderen Buchhaltungs- und Geschäftsführungsprogrammen.
* Unternehmen in verschiedenen [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebungen.

Die Einrichtung des konsolidierten Unternehmens erfolgt auf die gleiche Weise wie die Einrichtung anderer Unternehmen. Der Kontenplan ist vom Kontenplan des Konzernmandanten unabhängig. Die Kontenpläne in den Geschäftsbereichen können voneinander abweichen. Weitere Informationen zum Einrichten einer Konsolidierung finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Die Konsolidierung von Finanzdaten kann insbesondere für unternehmensübergreifende Prozesse relevant sein. Weitere Informationen zu Intercompany-Funktionen finden Sie unter [Intercompany-Transaktionen verwalten](intercompany-manage.md).

## <a name="consolidate-data"></a>Daten konsolidieren

Vor der Konsolidierung empfiehlt es sich, Ihre Daten zu testen, bevor Sie sie an das konsolidierte Unternehmen übertragen. [!INCLUDE[prod_short](includes/prod_short.md)] So überprüfen Sie Unterschiede zwischen den Informationen in den Konzernmandanten und dem Konsolidierungsmandanten Beispielsweise ob Kontonummern oder Dimensionscodes abweichen. Korrigieren Sie alle Fehler, die Sie finden, bevor Sie den Bericht ausführen. Sie können die Datenbank prüfen oder, wenn Sie Daten einer XML-Datei importieren, die Datei.

### <a name="test-the-data-before-you-consolidate"></a>Prüfen von Datenbanken vor der Konsolidierung

1. Öffnen Sie den Konsolidierungsmandanten.  
2. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
3. Testen Sie die Datei und die Datenbank wie folgt:  

    * Um eine Datei zu testen, wählen Sie die **Datei prüfen** Aktion, geben Sie den Namen der Datei an zum Testen ein, und wählen Sie dann **Drucken** aus.  
    * Um die Datenbank zu testen, wählen Sie **Datenbank prüfen**.  

### <a name="run-the-consolidation"></a>Die Konsolidierung ausführen

Nachdem Sie Ihre Daten getestet haben, können Sie diese an den Konsolidierungsmandanten übertragen. Eine unterstützte Einrichtungsanleitung hilft Ihnen durch den Prozess.

> [!NOTE]
> Wenn Sie die Konsolidierung durchführen, können Sie die einzubeziehenden Unternehmen auswählen. Wenn Ihr konsolidiertes Unternehmen keinen Zugriff auf eine oder mehrere Tochtergesellschaften hat, können Sie im Leitfaden den Zugriff darauf gewähren.

1. Melden Sie sich im Konsolidierungsmandanten an.  
2. Wählen Sie auf der Seite **Konzernmandanten** die Aktion **Konsolidieren** aus.  
3. Füllen Sie die entsprechenden Felder aus.  

## <a name="use-the-consolidated-trial-balance-report"></a>Verwendet den Bericht Konsolidierte Rohbilanz

Der Bericht **Konsolidierte Rohbilanz** kann Ihnen einen Überblick über die allgemeine Finanzstärke Ihres Gesamtunternehmens geben. Der Bericht Sachposten kombiniert aus jedem Ihrer Mandanten in einem neuen Mandanten, den Sie erstellen, um die konsolidierten Daten zu berücksichtigen. Der Konsolidierungsmandant ist einfach ein Container für die konsolidierten Daten und hat keine Verbindung zu den aktuellen Geschäftsdaten. Die Unternehmen, die Sie im konsolidierten Unternehmen einschließen, wird zur **Geschäftseinheit** im Bericht. Wenn Sie vier Konzernmandanten oder weniger haben, können Sie auch den Bericht **Konsolidierte Rohbilanz (4)** verwenden.  

Der Bericht zeigt eine Zeile für jedes Konto und folgt der Struktur des Kontenplans. Ein Konto wird nicht angezeigt, wenn alle Beträge in der Zeile Null sind. Der Bericht zeigt die folgenden Informationen für jedes Konto an:

* Die Kontonummer und der Kontoname des Kontos
* Die Summen für das konsolidierte Unternehmen und für jede Geschäftseinheit. Endsummen können entweder als Bewegung oder als Saldo zum Datum angezeigt werden.
* Die im Konsolidierungsmandanten durchgeführten Eliminierungen. Eliminierungen werden immer für eine Periode entsprechend dem Geschäftsjahr des Konsolidierungsmandanten angezeigt.
* Die Endsumme für den Konsolidierungsmandanten nach Durchführung der Eliminierungen. Sie wird entweder als Bewegung oder als Saldo zum Datum angezeigt.

## <a name="eliminate-repeated-transactions"></a>Wiederholte Transaktionen verhindern

Nachdem sämtliche Mandanten konsolidiert wurden, müssen Sie alle Transaktionen suchen, die in mehreren Mandanten einmal aufgezeichnet wurden, und dann Eliminierungsposten buchen, um sie zu entfernen. Durchführen der Konsolidierungseliminierungen ist ein manuelles Verfahren.  

So verhindern Sie wiederholte Transaktionen:

1. Suchen Sie Transaktionen, die eventuell korrigiert werden müssen, und geben Sie Fibu Buch.-Blattzeilen ein, um sie zu beseitigen.
2. Führen Sie den Bericht **Konsolidierungseliminierungen** aus, um Ihnen zu helfen, die Auswirkungen der Fibu Buch.-Blattzeilen zu bewerten, bevor Sie buchen.
3. Buchen Sie die Regulierungstransaktionen.

Der **G/L-Konsolidierungseliminierungen**-Bericht zeigt eine vorläufige Probebilanz an, in der Sie die Folgen der Eliminierung von Buchungen simulieren können. Der Bericht vergleicht die Buchungen im Konsolidierungskreis mit den im Hauptbuch gebuchten Eliminierungen.

Bevor ein Konzernmandant in dem Bericht berücksichtigt werden kann, muss er auf der Seite **Konzernmandanten** eingerichtet werden. Stellen Sie sicher, dass Sie den Schalter **Konsolidieren** aktivieren.

Für jedes Konto wird eine eigenen Zeile entsprechend der Struktur im Kontenplan erstellt. Ein Konto wird nicht angezeigt, wenn alle Beträge in der Zeile Null sind. Der Bericht zeigt die folgenden Informationen für jedes Konto an:

* Kontonummer.
* Kontoname.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen oder mehrere Konzernmandantencodes angegeben haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der die gewählten Konzernmandanten und Eliminierungen nicht enthalten sind. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der nur die Eliminierungen nicht enthalten sind.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen Konzernmandantencode angegeben haben, wird eine Summe für die importierten Posten des Konzernmandanten angezeigt. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird eine Summe der gebuchten Eliminierungen des Konsolidierungsmandanten angezeigt.
* Die Endsumme für den Konsolidierungsmandanten mit allen Konzernmandanten und allen gebuchten Eliminierungen.
* Die im Konsolidierungsmandanten durchgeführten Eliminierungen. Das heißt, die Einträge im allgemeinen Journal, das auf der Anforderungsseite ausgewählt wird.
* Der aus dem Fibu Buch.-Blatt kopierte Buchungstext.
* Die Endsumme für den Konsolidierungsmandanten nach Durchführung der Eliminierungen, soweit diese gebucht wurden.

## <a name="export-and-import-consolidated-data-between-databases"></a>Konsolidierte Daten zwischen Datenbanken exportieren und importieren

Wenn sich Daten für einen Konzernmandant in einer anderen Datenbank befinden, können Sie eine manuelle dateibasierte Übertragung durchführen oder den Prozess mithilfe einer API automatisieren. Weitere Informationen zur API finden Sie unter [Nutzen Sie unsere API, um Daten automatisch Umgebungsübergreifend auszutauschen](#use-our-api-to-automatically-share-data-across-environments).

In diesem Abschnitt wird der manuelle, dateibasierte Prozess beschrieben.

Sie exportieren die Daten in eine Datei, bevor Sie sie in die Konsolidierung einbeziehen. Exportieren Sie jedes Unternehmen separat, indem Sie den Batchauftrag **Konsolidierung exportieren** verwenden.  

> [!TIP]
> Verwenden Sie denselben Prozess, um konsolidierte Daten zu exportieren, die Sie an Dynamics 365 Finance übermitteln müssen. Wenn es sich beispielsweise beim Konzernmandant um eine Tochtergesellschaft handelt und die Muttergesellschaft Dynamics 365 Finance verwendet.

Nachdem der Batchauftrag ausgeführt wurde, sind alle Posten in den einzelnen Sachkonten verarbeitet. Für jede Kombination aus ausgewählten Dimensionen und Datum wird der Inhalt des Felds **Betrag** der Posten summiert und exportiert. Die nächste Kombination der ausgewählten Dimensionen und des Datums mit derselben Kontonummer wird verarbeitet. Dann werden die Kombinationen in der nächsten Kontonummer verarbeitet und so weiter.  

Die exportierten Posten enthalten die folgenden Felder: **Kontonr.**, **Buchungsdatum** und **Betrag**. Wenn auch Dimensionsdaten exportiert wurden, sind ebenfalls Dimensionscodes und Dimensionswerte enthalten.  

1. Für jede exportierte Zeile wird, sofern die Summe des **Betrag**-Felds ein Sollbetrag ist, die im **Konsol. Sollkonto** des Konzernmandanten eingerichtete Kontonummer in die Zeile exportiert. Wenn die Summe ein Habenbetrag ist, wird die entsprechende Nummer im Feld **Konsol. Habenkonto** in die Zeile exportiert.  
2. Das für jede exportierte Zeile verwendete Datum ist entweder das Enddatum der Periode oder, wenn die Übertragung täglich erfolgt, das genaue Berechnungsdatum.  
3. Bei dem für den Posten exportierten Dimensionswert handelt es sich um den Dimensionswert des Konsolidierungsmandanten, der im Feld **Konsolidierungscode** für diesen Dimensionswert eingerichtet ist. Wurde im Feld **Konsolidierungscode** für diesen Dimensionswert kein Dimensionswert des Konsolidierungsmandanten eingerichtet, wird der Dimensionswert selbst in die Zeile exportiert.  
4. Die XML-Dateien enthalten auch die Währungswechselkurse innerhalb der Konsolidierungsperiode. Diese Wechselkurse sind in einem eigenen Abschnitt zu Beginn der Datei aufgeführt.  

## <a name="use-our-api-to-automatically-share-data-across-environments"></a>Nutzen Sie unsere API, um Daten automatisch Umgebungsübergreifend auszutauschen

[!INCLUDE [prod_short](includes/prod_short.md)] bietet eine API, mit der Sie den Prozess der Weitergabe von Finanzdaten von Konzernmandanten an das konsolidierte Unternehmen automatisieren können. Die API ist kostenlos nutzbar und einfach einzurichten. Sie können damit sogar Daten in [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebungen austauschen. Beispielsweise müssen Sie möglicherweise Umgebungsübergreifende Freigaben vornehmen, wenn sich Konzernmandanten nicht in denselben Azure-Regionen befinden. Weitere Informationen zur Verwendung der API zur Automatisierung des Konsolidierungsprozesses finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md#busunit).

## <a name="see-also"></a>Siehe auch

[Mandantenkonsolidierung einrichten](finance-consolidated-company-reporting-setup.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
