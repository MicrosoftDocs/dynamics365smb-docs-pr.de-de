---
title: Unternehmenskonsolidierung einrichten
description: Erfahren Sie, wie Sie konfigurieren können, wie Daten von verschiedenen Unternehmen in Business Central an ein Konsolidierungsunternehmen gemeldet werden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 453cebcddb1fdfd2f3127fd08548deccc8fe1876
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512204"
---
# <a name="set-up-company-consolidation"></a>Unternehmenskonsolidierung einrichten

Bevor Sie die Sachposten von zwei oder mehr getrennten Unternehmen (Niederlassungen) in ein konsolidiertes Unternehmen zusammenführen können, müssen Sie die Kontenpläne und das Konsolidierungsunternehmen vorbereiten.  

Je nach Komplexität Ihrer Unternehmen, gibt es zwei Arten, die Konsolidierung einzurichten:

* Wenn Sie nicht erweiterte Einstellungen benötigen, wie Einschließen eines Unternehmens, dessen Sie nur ein Teil anlegen, können Sie die Felder **Mandanten-Konsolidierung** unterstützer Setup um raschen Einrichten einer Konsolidierung nutzen. Der Leitfaden führt Sie durch die grundlegenden Schritte durch.
* Wenn Sie erweitertere Einstellungen benötigen, können Sie den Konsolidierungsmandanten und die Konzernmandanten einrichten.
  * In jedem Konzernmandanten geben Sie an, welche Sachkonten in die Konsolidierung einzubeziehen sind und geben Sie die Konsolidierungsumrechnungsmethode für jedes Konto an.
  * Richten Sie im Konsolidierungsunternehmen eine Konzernmandantenkarte für jedes Unternehmen ein, das in die Konsolidierung einbezogen werden soll. Auf der Konzernmandantenkarte befinden sich Informationen wie Datumswerte für das Geschäftsjahr des Konzernmandanten und der Prozentsatz jedes Kontos, das in die Konsolidierung einbezogen werden muss.

## <a name="simple-consolidation-setup"></a>Einfache Konsolidierungseinrichtung

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Wenn die Konsolidierung einfach ist, weil Sie beispielsweise die Geschäftseinheit als Ganzes besitzen, führt Sie der unterstützte Setup **Mandanten-Konsolidierung** durch die folgenden Schritte:

* Wählen Sie aus, ob einen neuen Konsolidierungsmandanten erstellen oder ob die Daten in einem Mandanten konsolidiert werden, den Sie bereits für die Konsolidierung erstellt haben. Der Mandant sollte keine Transaktionen beinhalten.
* Ergebnisse in Vorschau anzeigen. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, dass die Masterdaten und die Transaktionen in den Konsolidierungsmandanten erfolgreich übertragen werden können.

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermaßen vor:

1. Im Feld **Buchhalter** wählen Sie Rollencenter **Unterstützte Einrichtung** Aktion aus.
2. Wählen Sie **Einrichten Konsolidierungsberichterstellung** und schließen Sie dann jeden Schritt im unterstützten Setup ab.

## <a name="advanced-consolidation-setup"></a>Erweiterte Konsolidierungseinrichtung

Wenn Sie erweitertere Einstellungen für die Konsolidierung benötigen, können Sie die Konsolidierung manuell einrichten. Wenn Sie Unternehmen haben, die Sie nur teilweise besitzen, oder Sie haben Mandanten, die nicht in der Konsolidierung enthalten sein soll.  

### <a name="set-up-the-consolidated-company"></a>Das konsolidierte Unternehmen einrichten

Zuerst müssen Sie das konsolidierte Unternehmen einrichten. Die Einrichtung des konsolidierten Unternehmens erfolgt auf die gleiche Weise wie die Einrichtung anderer Unternehmen. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).  

Die folgende Liste veranschaulicht wichtige Aspekte des konsolidierten Unternehmens.

1. Die Kontenpläne einrichten

    Weitere Informationen finden Sie unter [Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md).  

    Die Kontenpläne können in einem gesamten Konzernmandanten und dem konsolidierten Unternehmen identisch sein, oder das konsolidierte Unternehmen kann einen anderen Kontenplan haben. Wenn sich der Kontenplan eines Konzernmandanten von dem des konsolidierten Unternehmens unterscheidet, müssen Sie die Zuordnung zwischen Konten in den Konten im Konzernmandanten angeben. Weitere Informationen finden Sie im Abschnitt [Sachkonten für die Konsolidierung vorbereiten](#glacc).

2. Konzernmandanten hinzufügen

    Um die Finanzdaten mehrerer Mandanten in einem konsolidierten Unternehmen zu konsolidieren, müssen Sie Informationen über die Niederlassung als Konzernmandanten eingeben und darüber, in welchem Umfang ihre Zahlen einbezogen werden.

    Weitere Informationen finden Sie im Abschnitt [Konzernmandanten hinzufügen](#busunit).
3. Sie können Wechselkurse angeben, wenn die Finanzauswertungen von Konzernmandanten konsolidiert werden, wenn die Finanzauswertungen in einer Fremdwährung vorliegen.

    Die drei benutzten Wechselkurse sind **Durchschnittskurs (manuell)**, **Ultimokurs** und **Letzter Ultimokurs**. Weitere Informationen finden Sie im Abschnitt [Wechselkurse für Konsolidierungen angeben](#exchrates).
4. Sie können Dimensionsinformationen und Sachkonten konsolidieren.

    Weitere Informationen finden Sie im Abschnitt [Dimensionen ein- oder ausschließen](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Konzernmandanten hinzufügen

[!INCLUDE[prod_short](includes/prod_short.md)] ermöglicht es Ihnen, eine Liste zu konsolidierender Konzernmandanten einzurichten, die Buchhaltungsdaten zu überprüfen, bevor Sie diese konsolidieren, Dateien zu importieren und Konsolidierungsberichte zu generieren.  

1. Melden Sie sich im Konsolidierungsmandanten an.
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie Aktion **Neu** aus, und füllen Sie die relevanten Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Wenn Sie die Felder **Startdatum** und **Enddatum** ausfüllen, stellen Sie sicher, in die GAAP-Regeln zu Abrechnungszeiträumen des Konzernmandanten gegenüber der Muttergesellschaft einzuwilligen.
4. Wiederholen Sie Schritt 3 für jeden weiteren Konzernmandanten

Wenn der Konzernmandant eine Fremdwährung verwendet, müssen Sie den Wechselkurs angeben, der in der Konsolidierung verwendet werden soll. Sie müssen auch Konsolidierungdaten über die Sachkonten der Konzernmandanten angeben. In den folgenden Abschnitten werden diese Prozesse erläutert.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Sachkonten für die Konsolidierung vorbereiten

Der Kontenplan eines Unternehmens, das konsolidiert wird, muss Konten für die Konsolidierung angeben. Für jedes Buchungssachkonto in jedem Unternehmen müssen Sie das Sachkonto in dem konsolidierten Unternehmen angeben, auf das der Saldo bei der Konsolidierung übertragen wird. Mit dieser Zuordnung können Unternehmen mit unterschiedlichen Kontenplänen zusammen konsolidiert werden.

Wenn der Kontenplan des Konzernmandanten aus dem Konsolidierungsmandanten abweicht, müssen Sie die Sachkonten vorbereiten für die Konsolidierung. Sie können Konten definieren, um Soll- und Habenposten zu buchen und die Methode festlegen, die verwendet wird, um Währungen im Konsolidierungsmandanten zu übersetzen. Dies ist beispielsweise dann nützlich, wenn Sie häufig den Bericht ausführen.

1. Wählen Sie in der [!INCLUDE [prod_short](includes/prod_short.md)] jeder Einheit die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für das Konto, und füllen Sie dann die Felder im Inforegister **Konsolidierung** aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Wechselkurse für Konsolidierungen angeben

Richten Sie Wechselkurse für die Konsolidierung ein, wenn für die Finanzauswertungen eines Konzernmandanten nicht die Währung des konsolidierten Mandanten verwendet wird. Für jedes Konto bestimmt der Inhalt des Feldes **Konsol. Umrechnungsmethode** den Wechselkurses. Im konsolidierten Unternehmen auf jeder Konzernmandantenkarte im Feld **Währungswechselkurstabelle** geben Sie an, ob bei der Konsolidierung Wechselkurse des Konzernmandanten oder des konsolidierten Unternehmens verwendet werden. Bei Verwendung von Wechselkursen des konsolidierten Mandanten können die Wechselkurse für einen Konzernmandanten geändert werden. Enthält bei einer Geschäftseinheit das Feld **Wechselkurstabelle** (auf der Konzernmandantenkarte) den Wert **Lokal**, kann der Wechselkurs auf der Konzernmandantenkarte geändert werden. Zwar werden die Wechselkurse aus der Tabelle **Währungswechselkurs** kopiert, Sie haben jedoch die Möglichkeit, diese Wechselkurse vor der Konsolidierung zu ändern.

Die folgende Tabelle beschreibt die Wechselkursmethoden, die Sie für Konten verwenden können.

|Wechselkurs | Typische Nutzung |
|---|---|
|Durchschnittskurs (manuell) | Der Durchnittskurs für den zu konsolidierenden Zeitraum berechnen Sie manuell. Sie berechnen den Durchschnitt entweder als arithmetisches Mittel oder als bestmögliche Schätzung und geben ihn für jeden Konzernmandanten ein. Für GuV-Konten verwendet.|
|Ultimokurs | Für Kontenschema für Bilanz verwendet.|
|Letzter Ultimokurs | Schlusskurs: Der Schlusskurs am Devisenmarkt für den Tag, für den die Bilanz oder Gewinn- und Verlustrechnung erstellt wird. Sie geben diesen Kurs für jeden Konzernmandanten ein. Für Kontenschema für Bilanz verwendet.|
|Historischer Kurs | Der Wechselkurs, der galt, als die Transaktion erfolgte.|
|Gemischter Wechselkurs | Mischkurs: Die Beträge der laufenden Periode werden zum Durchschnittskurs umgerechnet und zum zuvor erfassten Saldo für den konsolidierten Mandanten addiert. Diese Methode wird meistens für Gewinn- und Verlustkonten verwendet, da diese Beträge aus unterschiedlichen Perioden umfassen und daher mit verschiedenen Umrechnungskursen bestimmte Beträge vereinen.|
|Eigenkapitalkurs | Dieses ist ähnlich wie der **Mischkurs**. Differenzen werden gebucht, um Sachkonten zu trennen.|

Um Wechselkurse für Konzernmandanten anzugeben, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Konzernmandantenübersicht** wählen Sie die Konzernmandanten aus, und wählen Sie die **Durchschnittskurs (manuell)** Aktion aus.  
3. Der Inhalt des Felds **Bezug auf Wechselkursbetrag** (im Fenster **Wechselkurs ändern**) wurde aus der Tabelle **Währungswechselkurs** kopiert, kann jedoch geändert werden. Schließen Sie die Seite.  
4. Wählen Sie die **Ultimokurs**-Aktion aus.  
5. In dem Feld **Relationaler Wechselkursbetrag** geben Sie den Wechselkurs ein.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Dimensionen ein- oder ausschließen

Sie können Dimensionsinformationen und Sachkonten konsolidieren.

* Machen Sie bei den relevanten Dimensionen Angaben im Feld **Konsolidierungscode** oder lassen Sie es leer
  * Um eine Dimension in der Konsolidierung auszuschließen, lassen Sie das Feld **Konsolidierungscode** bei der Dimension leer, und wählen Sie keine Dimensionen in den Feldern **Dimensionen kopieren** in irgendwelchen Konsolidierungsfunktionen oder Berichten.
  * Lassen Sie das Feld **Konsolidierungscode** leer, um Dimensionsinformationen in die Konsolidierung aufzunehmen. Die Konsolidierung wird jedoch nur dann funktionieren, wenn die Dimensionswerte in dem Konzernmandanten genau mit denen des konsolidierten Unternehmens übereinstimmen.
  * Um den Dimensionswertcode im Konzernmandanten mit einem anderen Dimensionswertcode im konsolidierten Unternehmen zu konsolidieren, füllen Sie das Feld **Konsolidierungscode** bei den relevanten Dimensionen aus.  
* Fügen Sie die relevanten Dimensionen zu den relevanten Sachkonten hinzu

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Ein Unternehmen aus der Konsolidierung ausschließen

Wenn Sie keinen Konzernmandanten in die Konsolidierung einbeziehen, können Sie sie ausschließen. Um das zu tun, wechseln Sie zur Konzernmandantenkarte, und löschen Sie das Kontrollkästchen **Konsolidieren**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Schließen Sie Unternehmen in die Konsolidierung ein, das teilweise im Besitz ist

Wenn Sie nur einen Teil des Unternehmen anlegen, können Sie einen Prozentsatz jeder Transaktion einschließen, der dem Prozentsatz des Mandanten entspricht, den Sie besitzen. Wenn beispielsweise 70% des Unternehmen anlegen, enthält $70 Konsolidierung einer Rechnung für $100. Um den Prozentsatz des Unternehmens anzugeben, den Sie anlegen, wechseln Sie zur Konzernmandantenkarte, und geben Sie den Prozentsatz im Feld **Konsolidierung %** ein.  

## <a name="see-also"></a>Siehe auch

[Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]