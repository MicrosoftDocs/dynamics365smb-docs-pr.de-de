---
title: Buchungsdatum auf Wertposten
description: Erfahren Sie wie die Stapelverarbeitung Lagerreg gekennzeichnet wird und ein Buchungsdatum auf Wertposten zugewiesen wird, der die Stapelverarbeitung erstellt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 31cfe9390e3f31253d60ba55a95f5507cdcac622
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436951"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designdetails: Buchungsdatum auf Ausgleichs-Wertposten
Dieser Artikel setzt Anleitung für Benutzer der Lager-Kostenberechnungsfunktionalität fest in [!INCLUDE[prod_short](includes/prod_short.md)]. Der spezifische Artikel informiert, wie die Stapelverarbeitung **Lagerreg. fakt. Einst.-Preise** kennzeichnet und ein Buchungsdatum auf Wertposten zuweist, die die Stapelverarbeitung erstellt.  

Zuerst wird der Begriff des Prozesses wiederholt, wie die Stapelverarbeitung das Buchungsdatum zuweist und Wertposten erstellt. Danach gibt es einige freigegebene Szenarien, auf die wir Support-Team gelegentlich stoßen und es gibt eine Zusammenfassung der Begriffe, die verwendet werden.  

## <a name="the-concept"></a>Das Konzept  
Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** weist ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:  

1.  Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.  

2.  Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung überprüft.  

3.  Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen. Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.  

 Lassen Sie uns dieses Verfahren in der Praxis überprüfen. Angenommen, wir haben einen Artikelposten zum Verkauf. Der Artikel wurde am 5. September 2013 geliefert und er wurde am darauffolgenden Tag fakturiert.  

![Status der Elemente-Sachkonto-Einträge im Szenario.](media/helene/TechArticleAdjustcost1.png "Zustand der Posten-Sachkonto-Einträge im Szenario")  

Unten zeigt der erste Wertposten (379) die Lieferung an und enthält dasselbe Buchungsdatum wie der Posten des übergeordneten Artikels.  

Der zweite Wertposten (381) zeigt die Rechnung an.  

 Der dritte Wertposten (391) ist eine Anpassung des Wertpostens Rechnungsstellung (381)  

 ![Status der Wertposten im Szenario.](media/helene/TechArticleAdjustcost2.png "Status der Wertposten im Szenario")  

 Schritt 1: Der zu erstellende Wertposten wird dem selben Buchungsdatum zugeordnet, wie der angepasste Eintrag, wie in oben durch Wertposten 391 angezeigt.  

 Schritt 2: Prüfung des zugewiesenen Buchungsdatums.  

Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung basiert.  

 Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.  

 Lagerbuchungsperioden:  

![Inventarisierungsperioden im Szenario.](media/helene/TechArticleAdjustcost3.png "Inventarisierungszeiträume im Szenario")

 Erster zugelassener Buchungszeitraum ist der erste Tag der ersten offenen Periode. 1. September 2013.  

 Finanzbuchhaltungs-Einrichtung:  

![G/L Einrichtung im Szenario.](media/helene/TechArticleAdjustcost4.png "Sachkonteneinrichtung im Szenario")

 Erster zugelassener Buchungszeitraum ist das Datum, das im Feld angezeigt wird, ab 10. September 2013.  

 Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem zugelassenen Ausgleichs-Wertposten zugeordnet.  

 Schritt 3: Zuweisung eines zugelassenen Buchungszeitraums;  

 Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht. Im zweiten Schritt erkennt die Stapelverarbeitung „Lagerreg. fakt. Einst.-Preise“ jedoch, dass das früheste zulässige Buchungsdatum der 10. September ist, und ordnet somit den 10. September dem unten stehenden Ausgleichs-Wertposten zu.  

 ![Status der Wertposten im Szenario 2.](media/helene/TechArticleAdjustcost5.png "Zustand der Wertposten im Szenario 2")

 Es haben jetzt das Vorgehen für das Zuweisen von Buchungsdaten für Wertposten wiederholt, durch die Stapelverarbeitung Lagerreg. fakt. Einst. Preise.  

 Lassen Sie uns fortfahren, um verschiedene Szenarien zu überprüfen, auf die wir im Support-Team gelegentlich stoßen, und zwar in Bezug auf ein Buchungsdatum in der Stapelverarbeitung Lagerreg und dem Zuordnen der zugehörigen Einrichtung.  

## <a name="scenarios"></a>Szenarien  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Szenario I: "Buchungsdatum liegt nicht innerhalb des zugelassenen Buchungszeitraums..."  
 Dies ist ein Szenario, in dem ein Benutzer eine Fehlermeldung erhält, wenn die Lagerreg. fakt. Einst. Preise Stapelverarbeitung ausgeführt wird.  

 Im vorherigen Abschnitt wird das Vorgehen für das Zuweisen des Buchungdatums beschrieben, die Absicht der Stapelverarbeitung Lagerreg. fakt. Einst. Preise ist es, einen Wertposten mit Buchungsdatum am 10. September zu erstellen.  

![Fehlermeldung zum Buchungsdatum.](media/helene/TechArticleAdjustcost6.png "Fehlermeldung zum Buchungsdatum")

 Wir nehmen die Benutzer Einrichtung nochmals auf:  

![Erlaubte Buchungsdaten des Benutzers einrichten.](media/helene/TechArticleAdjustcost7.png "Einrichtung der erlaubten Buchungsdaten der Benutzer")

 Der Anwender hat in diesem Fall einen Bereich des zugelassenen Buchungszeitraums vom 11. September bis zum 30. September und es wird dadurch nicht erlaubt, den Ausgleichs-Wertposten mit dem Buchungsdatum am 10. September zu buchen.  

![Übersicht der beteiligten Einrichtung des Buchungsdatums.](media/helene/TechArticleAdjustcost8.png "Übersicht über die Einstellung des beteiligten Buchungsdatums")

 Knowledge Base-Artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) erläutert weitere Szenarien, die mit erwähnter Fehlermeldung verknüpft sind.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Szenario II: Buchungsdatum auf Wertposten mit Buchungsdatum des Postens, der dem Ausgleich wie Neubewertung oder Artikel Zu-/Abschlag zugeordnet wird  

### <a name="revaluation-scenario"></a>Neubewertungsszenario:  
 Voraussetzungen:  

 Lagereinrichtung:  

-   Automatische Lagerbuchung = Ja  

-   Automatische Lagerregulierung = Immer  

-   Einst.-Pr.(durchschn.)Ber.-Art = Artikel  

-   Durchschnittskostenperiode= Tag  

 Finanzbuchhaltungs-Einrichtung:  

-   Zulassen Buchung von = am 1. Januar 2014  

-   Anlagenbuchungen zugel. bis= leer  

 Benutzereinrichtung:  

-   Zulassen Buchung von = 1. Dezember 2013.  

-   Anlagenbuchungen zugel. bis= leer  

##### <a name="to-test-the-scenario"></a>So führen Sie ein Testszenario aus  

1.  Artikel TEST erstellen:  

     Basismaßeinheit = PCS  

     Kostenberechnungsmethode = Durchschnitt  

     Wählen Sie Buchungsgruppen optional aus.  

2.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Buchungsdatum = 15. Dezember 2013  

     Artikel = TEST  

     Eink.-Posten ausgleichen = Einkauf  

     Menge = 100  

     Stückpreis = 10  

3.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Datum = 20. Dezember 2013  

     Artikel = TEST  

     Eingangsart = Negative Anpassung  

     Menge = 2  

4.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Datum = 15. Januar 2014  

     Artikel = TEST  

     Eingangsart = Negative Anpassung  

     Menge = 3  

5.  Buch.-Blatt Neubewertung öffnen und eine Zeile wie folgt erstellen und buchen:  

     Artikel = TEST  

     Auf Eintrag anwenden = Einkaufsposten auswählen, der unter Schritt 2 gebucht wurde. Das Buchungsdatum der Neubewertung ist derselbe, wie der Posten, der angepasst wird.  

     Einstandspreis neu bewertet = 40  

 Die folgenden Artikel- und Wertposten wurden gebucht:  

![Übersicht der resultierenden Elemente Sachkonto und Wertposten 1.](media/helene/TechArticleAdjustcost9.png "Übersicht der resultierenden Artikelposten- und Wertposten 1")

 ![Übersicht über das resultierende Element Sachkonto und die Wertposten 2.](media/helene/TechArticleAdjustcost10.png "Übersicht der resultierenden Artikelposten- und Wertposten 2")

 Die Stapelverarbeitung Lagerreg hat eine Änderung der Kosten realisiert und die negative Anpassung vorgenommen.  

 **Überprüfung Buchungsdatum des erstellten Ausgleichs-Wertposten:** Der früheste zugelassene Buchungszeitraum, den die Stapelverarbeitung Lagerreg verknüpft, ist am 1. Januar 2014, wie in der Finanzbuchhaltungs-Einrichtung festgelegt.  

 **Negative Anpassung in Schritt 3:** zugewiesenes Buchungsdatum ist am 1. Januar, wie von der Finanzbuchhaltung eingerichtet. Das Buchungsdatum des Wertpostens im Bereich für Ausgleich ist am 20. Dezember 2013. Entsprechend der Finanzbuchhaltungseinrichtung ist das Datum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums. Daher werden die Buchungsdaten, die im Feld Buchungen zulassen in der Finanzbuchhaltungs-Einrichtung festgelegt sind, den Ausgleichs-Wertposten zugeordnet.  

 **Abgang in Schritt 4:** weist Buchungsdatum 15. Januar auf. Der Wertposten im Bereich des Ausgleichs hat Buchungsdatum am 15. Januar, das innerhalb des Bereichs des zugelassenen Buchungszeitraums entsprechend der Finanzbuchhaltungseinrichtung ist.  

 Der Ausgleich, der für den Abgang in Schritt 3 geändert wird, verursacht Diskussionen. Das bevorzugte Buchungsdatum für den Ausgleichs-Wertposten wäre am 20. Dezember oder mindestens im Dezember während die Neubewertung eine Änderung im Lagerverbrauch verursacht, der im Dezember gebucht wurde.  

 Um den Ausgleich im Dezember im Feld Abgang in Schritt 3 zu erzielen, gestattet die Finanzbuchhaltungseinrichtung die Buchung aus dem Feld und es muss ein Datum im Dezember angegeben werden.  

 **Schlussfolgerung:**  

 Mit den Erfahrungen aus diesem Szenario sollten Sie bei der Überlegung, welche Einrichtung des zulässigen Buchungsdatumsbereichs für ein Unternehmen am besten geeignet ist, die folgenden Informationen berücksichtigen: Solange Sie zulassen, dass Bestandswertänderungen in einer Periode gebucht werden, in diesem Fall im Dezember, sollte die Einrichtung, die das Unternehmen für zulässige Buchungsdatumsbereiche verwendet, mit dieser Entscheidung in Einklang stehen. Buchung von zulassen in der Finanzbuchhaltungs-Einrichtung, in diesem Fall der 1. Dezember, würde die Neubewertung ermöglichen, die im Dezember erfolgte und an betroffene ausgehenden Posten in derselben Periode weitergeleitet werden.  

 Die Benutzergruppen, die nicht erlaubt sind, um im Dezember gebucht zu werden, sondern im Januar, sind wahrscheinlich durch die Finanzbuchhaltungseinrichtung in diesem Szenario beschränkt und sollten stattdessen über die Benutzereinrichtung adressiert werden.  

### <a name="item-charge-scenario"></a>Artikel-Zu-/Abschlagszuweisung  
 Voraussetzungen:  

 Lagereinrichtung:  

-   Automatische Lagerbuchung = Ja  

-   Automatische Lagerregulierung = Immer  

-   Einst.-Pr.(durchschn.)Ber.-Art = Artikel  

-   Durchschnittskostenperiode= Tag  

 Finanzbuchhaltungs-Einrichtung:  

-   Zulassen Buchung von = 1. Dezember 2013.  

-   Anlagenbuchungen zugel. bis= leer  

 Benutzereinrichtung:  

-   Zulassen Buchung von = 1. Dezember 2013.  

-   Anlagenbuchungen zugel. bis= leer  

##### <a name="to-test-the-scenario"></a>So führen Sie ein Testszenario aus  

1.  Artikel Zu-/Abschläge erstellen:  

     Basismaßeinheit = PCS  

     Kostenberechnungsmethode = Durchschnitt  

     Wählen Sie Buchungsgruppen optional aus.  

2.  Neue Bestellung erstellen  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 15. Dezember 2013  

     Kred.-Rechnungsnr.: 1234  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikel = ABSCHLAG  

     Menge = 1  

     Direkte Einheitskosten = 100  

     Lieferung und Rechnung buchen.  

3.  Einen neuen Verkaufsauftrag erstellen:  

     Verk. an Deb.-Nr.: 10000  

     Buchungsdatum = 16. Dezember 2013  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikel = ABSCHLAG  

     Menge = 1  

     VK-Preis = 135  

     Liefernung und Rechnung buchen.  

4.  Finanzbuchhaltungs-Einrichtung:  

     Zulassen Buchung von = am 1. Januar 2014  

     Anlagenbuchungen zugel. bis = leer  

5.  Neue Bestellung erstellen:  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 2. Januar 2014  

     Kred.-Rechnungsnr.: 2345  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikelkosten = FRACHT  

     Menge = 1  

     Direkte Einheitskosten = 3  

     Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.  

     Empfang und Rechnung buchen.  

     ![Übersicht über das resultierende Element Sachkonto und die Wertposten 3.](media/helene/TechArticleAdjustcost11.png "Übersicht der resultierenden Artikelposten- und Wertposten 3")

6.  Am Arbeitsdatum vom 3. Januar geht eine Einkaufsrechnung ein, die eine zusätzliche Belastung für den in Schritt 2 getätigten Einkauf enthält. Diese Rechnung hat ein Belegdatum vom 30. Dezember und wird daher mit Buchungsdatum am 30. Dezember 2013 gebucht.  

     Neue Bestellung erstellen:  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 30. Dezember 2013  

     Kred.-Rechnungsnr.: 3456  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikelkosten = FRACHT  

     Menge = 1  

     Direkte Einheitskosten = 2  

     Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.  

     Empfang und Rechnung buchen.  

   ![Übersicht über das resultierende Element Sachkonto und die Wertposten 4.](media/helene/TechArticleAdjustcost12.png "Übersicht der resultierenden Artikelposten- und Wertposten 4")

 Lager-Bewertungsbericht wird mit 31. Dezember 2013 gedruckt  

![Inhalt des Berichts „Bestandsbewertung“.](media/helene/TechArticleAdjustcost13.png "Inhalt des Berichts zur Inventarbewertung")

 **Zusammenfassung des Szenarios:**  

 Das oben beschriebene Szenario endet mit einem Lager-Bewertungsbericht und zeigt Menge = 0 an, während der Wert = 2 beträgt. Der Artikelzuschlag, der in Schritt 11 gebucht wird, ist ein Teil des Lagerzugangswerts vom Dezember, wohingegen der Lagerabgang derselben Periode nicht berücksichtigt wird.  

 Der Finanzbuchhaltungs-Einrichtung angeben, Buchungen ab dem 1. Januar zuzulassen, war für den ersten Artikel-Zu/Abschlag gut. Die Kosten des Lagerzugangs und des Feldes Abgang wurden in derselben Periode erfasst. Für den zweiten Artikel-Zu-/Abschlag verursachte die Finanzbuchhaltungseinrichtung jedoch die Änderung im Lagerverbrauch, der in der Periode danach erkannt wurde.  

 **Schlussfolgerung:**  

 Es ist eine Herausforderung, den Bestandbewertungsbericht zu haben, um Menge = O anzuzeigen, während der Wert<> Wert 0 ist. In diesem Fall ist es ebenfalls schwieriger, die optimalen Einstellungen zu finden, da Verkaufsrechnungen am gleichen Tag ankommen, jedoch verschiedene Perioden oder sogar Geschäftsjahre adressieren. Das Eindringen in ein neues Geschäftsjahr erfordert normalerweise eine Absatzplanung ist Teil der Einblicke der Stapelverarbeitung Lagerreg Artikelposten und muss berücksichtigt werden.  

 In diesem Szenario könnte eine Option sein, die Finanzbuchhaltung so einzurichten, dass das Feld Buchung zulassen von ein Datum im Dezember für einige Tage mehr definiert und die Buchung des Zuschlages des ersten Artikelpostens zurückgestellt wird, um die Kosten für die vorherige Periode/das vorherige Finanzjahr für die Periode zu ermöglichen, um alle Kosten dort zuzuweisen, wo sie zuerst erkannt wurden und dann die erlaubten Buchungsdaten in die neue Periode des \/ Steuerjahrs zu übertragen. Die Kosten des ersten Artikelpostens mit Buchungsdatum am 2. Januar dann gebucht werden.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Führen Sie die Stapelverarbeitung Lagerreg. fakt. Einst. Preise aus.  
 Unten finden Sie eine Zusammenfassung des Begriffs, der Buchungsdaten den Ausgleichs-Wertposten durch die Stapelverarbeitung „Lagerreg. fakt. Einst. Preise“ zuweist.  

### <a name="about-the-request-form-posting-date"></a>Informationen zum Veröffentlichungsdatum des Anfrageformulars:  
 Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss. Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum, das in das Anforderungsfenster eingegeben wird. Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen. vgl. Beschreibung des Konzepts oben.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Verlauf der Lagerkostenbuchung auf den Stapelverarbeitungseintrag  
 Die Stapelverarbeitung "Lagerregulierung buchen" ist mit der Stapelverarbeitung Lagerreg eng verwandt, warum die Historie dieser Stapelverarbeitung auch hier zusammengefasst und freigegeben wird.  
 
![Ist-Kosten gegenüber erwarteten Kosten.](media/helene/TechArticleAdjustcost14.png "Tatsächliche Kosten versus erwartete Kosten")

### <a name="about-the-posting-date"></a>Informationen zum Buchungsdatum
 Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss. Die Sachposten werden mit dem gleichen Buchungsdatum wie der verwandter Wertposten erstellt. Um die Stapelverarbeitung auszuführen, muss der mittlere des zugelassenen Buchungszeitraums das Buchungsdatum des erstellten Sachpostens erlauben. Wenn nicht, muss sich der Standort des zugelassenen Buchungszeitraums durch das Ändern oder Entfernen des festgelegten Datumsfilters Buchungen zugel und aus den Feldern der Finanzbuchhaltungseinrichtung vorübergehend erneut geöffnet werden. Um Abstimmungsprobleme zu vermeiden ist es notwendig, dass das Buchungsdatum des Sachpostens zum Buchungsdatum des Wertpostens entspricht.  

 Die Stapelverarbeitungsscans scannt Tabelle 5811 - Buchen von Wertposten mit Sachkonten, um die Wertposten im Bereich für die Buchung auf das Sachkonto zu identifizieren. Nach erfolgreicher Ausführung wird die Tabelle geleert.

## <a name="see-also"></a>Siehe auch  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
