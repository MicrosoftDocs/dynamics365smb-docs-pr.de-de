---
title: Konsolidieren Sie Daten aus mehreren Unternehmen | Microsoft Docs
description: Rufen Sie eine Zusammenfassungsansicht der Finanzstärke über Ihre Konzernmandanten hinweg ab.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2be133009314b714d7b86e6257f642f13720b5e8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774329"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidieren von Finanzdaten aus mehreren Unternehmen

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

Die Einrichtung des konsolidierten Unternehmens erfolgt auf die gleiche Weise wie die Einrichtung anderer Unternehmen. Der Kontenplan ist unabhängig vom Kontenplan in anderen Konzernmandanten, und der Kontenplan in den einzelnen Konzernmandanten kann sich von einem anderen unterscheiden. Sie richten eine Liste von Unternehmen ein, um die Buchhaltungsdaten vor der Konsolidierung zu konsolidieren und zu überprüfen, aus Dateien oder Datenbanken zu importieren und Konsolidierungsberichte zu generieren. Weitere Informationen finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Die Konsolidierung von Finanzdaten kann insbesondere in Verbindung mit Intergesellschaftsvorgängen relevant sein. Weitere Informationen finden Sie unter [Verwaltung von Intercompany-Transaktionen](intercompany-manage.md).

## <a name="trial-balance"></a>Rohbilanz

Wenn Sie mehr als ein Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] haben , kann der **konsolidierte Rohbilanz**-Bericht Ihnen einen Überblick über die Finanzstärke Ihres Gesamtunternehmens geben.  

Der Bericht Sachposten (Fibu) kombiniert aus jedem Ihrer Mandanten in einem neuen Mandanten, den erstellen, um die konsolidierten Daten zu berücksichtigen. Dieses Unternehmen wird in der Regel als "konsolidiertes Unternehmen" bezeichnet. Der Konsolidierungsmandant ist einfach ein Container für die konsolidierten Daten und hat keine Verbindung zu den aktuellen Geschäftsdaten. Die Unternehmen, die Sie im konsolidierten Unternehmen einschließen, wird zur **Geschäftseinheit** im Bericht. Weitere Informationen finden Sie unter [Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md).  

## <a name="consolidate-data"></a>Daten konsolidieren

Der Prozess der Übertragung der Zahlen aus den Konzernmandanten in das konsolidierte Unternehmen ist die tatsächliche *Konsolidierung*. Bevor Sie das tun, sollten Sie prüfen, ob es Unterschiede zwischen den grundlegenden Informationen in den Konzernmandanten und im konsolidierten Unternehmen gibt. Es gibt zwei Berichte, die Sie verwenden können, um die Datenbank und die Datei zu testen.

### <a name="to-test-the-data-before-you-consolidate"></a>Prüfen von Datenbanken vor der Konsolidierung

Sie können Ihre Daten testen, bevor Sie sie an den Konsolidierungsmandanten übertragen. [!INCLUDE[prod_short](includes/prod_short.md)] So überprüfen Sie Unterschiede zwischen den Informationen in den Konzernmandanten und dem Konsolidierungsmandanten Beispielsweise ob Kontonummern oder Dimensionscodes abweichen. Sie müssen Fehler korrigieren, bevor Sie den Bericht ausführen können. Sie können prüfen, die Datenbank oder, wenn Sie Daten einer XML-Datei importiert, können Sie testen die Datei.  

1. Öffnen Sie den Konsolidierungsmandanten.  
2. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Geschäftseinheiten** ein und wählen Sie dann den entsprechenden Link.  
3. Führen Sie einen der folgenden Schritte aus:  

    * Um eine Datei zu testen, wählen Sie die **Datei prüfen** Aktion, geben Sie den Namen der Datei an zum Testen ein, und wählen Sie dann **Drucken** aus.  
    * Um die Datenbank zu testen, wählen Sie **Datenbank prüfen**.  

### <a name="run-the-consolidation"></a>Die Konsolidierung ausführen

Nachdem Sie Ihre Daten geteste haben, können Sie diese an den Konsolidierungsmandanten übertragen.  

1. Melden Sie sich im Konsolidierungsmandanten an.  
2. Im Feld **Buchhalter-Rollencenter** wählen Sie Rollencenter **Konsolidierung ausführen** Aktion aus.  
3. Füllen Sie die entsprechenden Felder aus.  
4. Legen Sie im Abschnitt Filter einen Filter für den jeweiligen Konzernmandanten oder Unternehmensnamen fest.  
5. Optional planen Sie den Bericht so, dass er zu einer günstigen Zeit ausgeführt wird.  

## <a name="eliminate-repeated-transactions"></a>Wiederholte Transaktionen verhindern

Nachdem sämtliche Mandanten konsolidiert wurden, müssen Sie alle Transaktionen suchen, die in mehreren Mandanten einmal aufgezeichnet wurden, und dann Eliminierungsposten buchen, um sie zu entfernen.

Durchführen der Konsolidierungseliminierungen ist ein manuelles Verfahren.  

So verhindern Sie wiederholte Transaktionen:

1. Suchen Sie Transaktionen, die eventuell korrigiert werden müssen, und geben Sie Fibu Buch.-Blattzeilen ein, um sie zu beseitigen.
2. Führen Sie den Bericht **Konsolidierungseliminierungen** aus, um Ihnen zu helfen, die Auswirkungen der Fibu Buch.-Blattzeilen zu bewerten, bevor Sie buchen.
3. Buchen Sie die Regulierungstransaktionen.

Der Bericht **Konsolidierungseliminierungen** enthält eine vorläufige Rohbilanz, d. h., er zeigt eine Simulation der aus der Eliminierung der Posten hervorgegangenen Ergebnisse. Hierzu werden die Posten des Konsolidierungsmandanten mit den Eliminierungen verglichen, die in das Fibu Buch.-Blatt eingegeben wurden, in dem sie nachfolgend gebucht werden.

Bevor ein Konzernmandant in dem Bericht berücksichtigt werden kann, muss er auf der Seite **Konzernmandanten** eingerichtet werden und das Feld **Konsolidieren** muss ausgewählt werden.

Jedes Konto erscheint in einer eigenen Zeile entsprechend der Struktur im Kontenplan. Ein Konto wird nicht angezeigt, wenn alle Beträge in der Zeile Null sind. Folgende Informationen werden für jedes Konto angegeben:

* Kontonummer
* Kontoname.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen oder mehrere Konzernmandantencodes angegeben haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der die gewählten Konzernmandanten und Eliminierungen nicht enthalten sind. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird für den Konsolidierungsmandanten eine Summe angezeigt, in der nur die Eliminierungen nicht enthalten sind.
* Wenn Sie im Feld **Konzernmandantencode** auf der Anforderungsseite einen Konzernmandantencode angegeben haben, wird eine Summe für die importierten Posten des Konzernmandanten angezeigt. Wenn Sie das Feld **Konzernmandantencode** nicht ausgefüllt haben, wird eine Summe der gebuchten Eliminierungen des Konsolidierungsmandanten angezeigt.
* Die Endsumme für den Konsolidierungsmandanten mit allen Konzernmandanten und allen gebuchten Eliminierungen.
* Die Eliminierungen, die im Konsolidierungsmandanten durchgeführt werden müssen. Das sind die Posten des Fibu Buch.-Blattes, das auf der Anforderungsseite ausgewählt wurde.
* Der aus dem Fibu Buch.-Blatt kopierte Buchungstext.
* Die Endsumme für den Konsolidierungsmandanten nach Durchführung der Eliminierungen, soweit diese gebucht wurden.

## <a name="export-and-import-consolidated-data-between-databases"></a>Konsolidierte Daten zwischen Datenbanken exportieren und importieren

Wenn sich ein Konzernmandant in einer anderen Datenbank befindet, müssen Sie die Konsolidierungsdaten in eine Datei exportieren, bevor diese konsolidiert werden können. Jeder Mandant muss separat konsolidiert werden. Zu diesem Zweck wird in der Anwendung die Stapelverarbeitung **Konsolidierung exportieren** verwendet.  

> [!TIP]
> Verwenden Sie denselben Prozess, um konsolidierte Daten zu exportieren, die an Dynamics 365 Finance übermittelt werden müssen, wie z. B. wenn der aktuelle Konzernmandant eine Niederlassung ist und das übergeordnete Unternehmen Dynamics 365 Finance nutzt.

Nachdem der Batchauftrag ausgeführt wurde, sind alle Posten in den einzelnen Sachkonten verarbeitet. Für jede Kombination aus ausgewählten Dimensionen und Datum wird der Inhalt des Felds **Betrag** der Posten summiert und exportiert. Die nächste Kombination aus ausgewählten Dimensionen und Datum mit derselben Kontonummer verarbeitet, danach die Kombinationen in der nächsten Kontonummer, usw.  

Die exportierten Posten enthalten die folgenden Felder: **Kontonr.**, **Buchungsdatum** und **Betrag**. Wenn auch Dimensionsdaten exportiert wurden, sind ebenfalls Dimensionscodes und Dimensionswerte enthalten.  

1. Für jede exportierte Zeile wird, sofern die Summe des **Betrag**-Felds ein Sollbetrag ist, die im **Konsol. Sollkonto** des Konzernmandanten eingerichtete Kontonummer in die Zeile exportiert. Wenn die Summe ein Habenbetrag ist, wird die entsprechende Nummer im Feld **Konsol. Habenkonto** in die Zeile exportiert.  
2. Das für jede exportierte Zeile verwendete Datum ist entweder das Enddatum der Periode oder, wenn die Übertragung täglich erfolgt, das genaue Berechnungsdatum.  
3. Bei dem für den Posten exportierten Dimensionswert handelt es sich um den Dimensionswert des Konsolidierungsmandanten, der im Feld **Konsolidierungscode** für diesen Dimensionswert eingerichtet ist. Wurde im Feld **Konsolidierungscode** für diesen Dimensionswert kein Dimensionswert des Konsolidierungsmandanten eingerichtet, wird der Dimensionswert selbst in die Zeile exportiert.  
4. Die XML-Dateien enthalten auch die Währungswechselkurse innerhalb der Konsolidierungsperiode. Diese Wechselkurse sind in einem eigenen Abschnitt zu Beginn der Datei aufgeführt.  

## <a name="see-also"></a>Siehe auch

[Unternehmenskonsolidierung einrichten](finance-consolidated-company-reporting-setup.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]