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
ms.date: 07/27/2021
ms.author: edupont
ms.openlocfilehash: 2a3d35672905094e714f85ac4758cbf39ec88cb6
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688314"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designdetails: Buchungsdatum auf Ausgleichs-Wertposten  

Dieser Artikel setzt Anleitung für Benutzer der Lager-Kostenberechnungsfunktionalität fest in [!INCLUDE[prod_short](includes/prod_short.md)]. Der spezifische Artikel informiert, wie die Stapelverarbeitung **Lagerreg. fakt. Einst.-Preise** kennzeichnet und ein Buchungsdatum auf Wertposten zuweist, die die Stapelverarbeitung erstellt.  

Zuerst wird der Begriff des Prozesses wiederholt, wie die Stapelverarbeitung das Buchungsdatum zuweist und Wertposten erstellt. Danach gibt es einige freigegebene Szenarien, auf die wir Support-Team gelegentlich stoßen und es gibt eine Zusammenfassung der Begriffe, die verwendet werden.  

## <a name="the-concept"></a>Das Konzept  

Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** weist ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:  

1.  Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.  

2.  Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung überprüft.  

3.  Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen. Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.  

 Lassen Sie uns dieses Verfahren in der Praxis überprüfen. Angenommen, wir haben einen Artikelposten zum Verkauf. Der Artikel wurde am 5. September 2020 geliefert und er wurde am darauffolgenden Tag fakturiert.  


**Artikelposten**  
Datumsformat JJJJ-MM-TT

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Postenart   | Belegnummer |Lagerortcode  |Menge  |Einstandsbetrag (tatsächl.)  |Fakturierte Menge  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Verkauf       |102033     |  Blau       | -1    |    -11     |-1     |    0     |

Unten zeigt der erste Wertposten (379) die Lieferung an und enthält dasselbe Buchungsdatum wie der Posten des übergeordneten Artikels.  
  
Der zweite Wertposten (381) zeigt die Rechnung an.  

Der dritte Wertposten (391) ist eine Anpassung des Wertpostens Rechnungsstellung (381).  
  

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Artikelpostenart  |Postenart   |Belegnummer  |Artikelposten Lfd. Nr.  |Lagerortcode  |Artikelpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | Direkte Kosten   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    2020-09-10     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

Das Buchungsdatum des Regulierungspostens wird zunächst auf das Buchungsdatum des zu regulierenden Postens gesetzt.

 Schritt 1: Der zu erstellende Wertposten wird dem selben Buchungsdatum zugeordnet, wie der angepasste Eintrag, wie in oben durch Wertposten 391 angezeigt.  
  
 Schritt 2: Prüfung des zugewiesenen Buchungsdatums.  

Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung basiert.  

Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.  
  
**Lagerbuchungsperioden**

|Enddatum  |Name  |Geschlossen  |
|---------|---------|---------|
|2020-01-31     |2020. Januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |März 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |   Ja   |
|2020-08-31     |August 2020     |   Ja   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |Dezember   2020   |         |

Erster zugelassener Buchungszeitraum ist der erste Tag der ersten offenen Periode. 1. September 2020.  

**Finanzbuchhaltungs-Einrichtung**

|Feld|Wert  |
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ-Code      |  

 Erster zugelassener Buchungszeitraum ist das Datum, das im Feld angezeigt wird, ab 1. September 2020.  
 Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem zugelassenen Ausgleichs-Wertposten zugeordnet.  

 Schritt 3: Zuweisung eines zugelassenen Buchungszeitraums;  

 Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht. Im zweiten Schritt erkennt die Stapelverarbeitung „Lagerreg. fakt. Einst.-Preise“ jedoch, dass das früheste zulässige Buchungsdatum der 10. September ist, und ordnet somit den 10. September dem unten stehenden Ausgleichs-Wertposten zu.  

   
|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Artikelpostenart  |Postenart   |Belegnummer  |Artikelposten Lfd. Nr.  |Lagerortcode  |Artikelpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | Direkte Kosten   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    **2020-09-10**     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

 Es haben jetzt das Vorgehen für das Zuweisen von Buchungsdaten für Wertposten wiederholt, durch die Stapelverarbeitung Lagerreg. fakt. Einst. Preise.  

 Lassen Sie uns fortfahren, um verschiedene Szenarien zu überprüfen, auf die wir im Support-Team gelegentlich stoßen, und zwar in Bezug auf ein Buchungsdatum in der Stapelverarbeitung Lagerreg und dem Zuordnen der zugehörigen Einrichtung.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Szenario I: "Buchungsdatum liegt nicht innerhalb des zugelassenen Buchungszeitraums..."  

 Dies ist ein Szenario, in dem ein Benutzer eine Fehlermeldung erhält, wenn die Lagerreg. fakt. Einst. Preise Stapelverarbeitung ausgeführt wird.  

 Im vorherigen Abschnitt wird das Vorgehen für das Zuweisen des Buchungdatums beschrieben, die Absicht der Stapelverarbeitung Lagerreg. fakt. Einst. Preise ist es, einen Wertposten mit Buchungsdatum am 10. September zu erstellen.  

![Fehlermeldung zum Buchungsdatum.](media/helene/TechArticleAdjustcost6.png "Fehlermeldung zum Buchungsdatum")

 Wir nehmen die Benutzer Einrichtung nochmals auf:  

**Benutzereinrichtung**  

Sortierung: Benutzer-ID  

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

 Der Anwender hat in diesem Fall einen Bereich des zugelassenen Buchungszeitraums vom 11. September bis zum 30. September und es wird dadurch nicht erlaubt, den Ausgleichs-Wertposten mit dem Buchungsdatum am 10. September zu buchen.  

### <a name="overview-of-involved-posting-date-setup"></a>Übersicht über die Einstellung des beteiligten Buchungsdatums:

**Lagerbuchungsperioden**  

|Enddatum  |Name  |Geschlossen  |
|---------|---------|---------|
|2020-01-31     |2020. Januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |März 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |   Ja   |
|2020-08-31     |August 2020     |   Ja   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |Dezember   2020   |         |  

**Finanzbuchhaltungs-Einrichtung**  

|Feld|Wert|
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ-Code      |  

**Benutzereinrichtung**    

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|<name> |  2020-09-11      |2020-09-30      |

 Durch Zuweisen eines größeren (oder gleichen) zulässigen Buchungsdatumsbereichs für den Benutzer wie in Lagerbuchungsperiode oder Finanzbuchhaltungs-Einrichtung wird der erwähnte Konflikt vermieden. Der Ausgleichs-Wertposten mit dem Buchungsdatum 10. September wird mit dieser Einrichtung erfolgreich gebucht.

Ein älterer Knowledge Base-Artikel [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) erläutert weitere Szenarien, die mit der erwähnten Fehlermeldung verknüpft sind.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Szenario II: Buchungsdatum auf Wertposten mit Buchungsdatum des Postens, der dem Ausgleich wie Neubewertung oder Artikel Zu-/Abschlag zugeordnet wird  

### <a name="revaluation-scenario"></a>Neubewertungsszenario:  

 Voraussetzungen:  

 Lagereinrichtung:  
ich
-   Automatische Lagerbuchung = Ja  

-   Automatische Lagerregulierung = Immer  

-   Einst.-Pr.(durchschn.)Ber.-Art = Artikel  

-   Durchschnittskostenperiode= Tag  

 Finanzbuchhaltungs-Einrichtung:  

-   Zulassen Buchung von = am 1. Januar 2021  

-   Anlagenbuchungen zugel. bis= leer  

 Benutzereinrichtung:  

-   Zulassen Buchung von = 1. Dezember 2020  

-   Anlagenbuchungen zugel. bis= leer  

### <a name="to-test-the-scenario"></a>So führen Sie ein Testszenario aus  

1.  Artikel TEST erstellen:  

     Basismaßeinheit = PCS  

     Kostenberechnungsmethode = Durchschnitt  

     Wählen Sie Buchungsgruppen optional aus.  

2.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Buchungsdatum = 15. Dezember 2020  

     Artikel = TEST  

     Eink.-Posten ausgleichen = Einkauf  

     Menge = 100  

     Stückpreis = 10  

3.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Datum = 20. Dezember 2020  

     Artikel = TEST  

     Eingangsart = Negative Anpassung  

     Menge = 2  

4.  Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:  

     Datum = 15. Januar 2021  

     Artikel = TEST  

     Eingangsart = Negative Anpassung  

     Menge = 3  

5.  Buch.-Blatt Neubewertung öffnen und eine Zeile wie folgt erstellen und buchen:  

     Artikel = TEST  

     Auf Eintrag anwenden = Einkaufsposten auswählen, der unter Schritt 2 gebucht wurde. Das Buchungsdatum der Neubewertung ist derselbe, wie der Posten, der angepasst wird.  

     Einstandspreis neu bewertet = 40  

Die folgenden **Artikelposten** und **Wertposten** wurden gebucht:  

**Artikelposten – Einkauf**:  
Datumsformat JJJJ-MM-TT  

|Postennummer  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Einkauf         |T00001         |100         |4000         |95        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Einkauf         |Direkte Kosten         |T00001         |100         |1 000,00          |1 000,00    |Nein         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Einkauf         |Neubewertung         |T04002         |0         |3 000,00         |3 000,00         |Nein         |0         |REVALINL         |

**Artikelposten – Abgang, Schritt 3**  

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Abgang  |T00002         |-2         |-80         | 0        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Abgang         |Direkte Kosten         |T00002         |-2         |-20          |-20    |Nein         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Abgang         |Direkte Kosten         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Artikelposten – Abgang, Schritt 4**  

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Abgang  |T00003         |-3         |-120         | 0        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Abgang         |Direkte Kosten         |T00003         |-3         |-30          |-30    |Nein         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Abgang         |Direkte Kosten         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Die Stapelverarbeitung Lagerreg hat eine Änderung der Kosten realisiert und die negative Anpassung vorgenommen.  

**Überprüfung Buchungsdatum des erstellten Ausgleichs-Wertposten:** Der früheste zugelassene Buchungszeitraum, den die Stapelverarbeitung Lagerreg verknüpft, ist am 1. Januar 2021, wie in der Finanzbuchhaltungs-Einrichtung festgelegt.  

**Negative Anpassung in Schritt 3:** zugewiesenes Buchungsdatum ist am 1. Januar, wie von der Finanzbuchhaltung eingerichtet. Das Buchungsdatum des Wertpostens im Bereich für Ausgleich ist am 20. Dezember 2020. Entsprechend der Finanzbuchhaltungseinrichtung ist das Datum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums. Daher werden die Buchungsdaten, die im Feld Buchungen zulassen in der Finanzbuchhaltungs-Einrichtung festgelegt sind, den Ausgleichs-Wertposten zugeordnet.  

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

-   Zulassen Buchung von = 1. Dezember 2020.  

-   Anlagenbuchungen zugel. bis= leer  

 Benutzereinrichtung:  

-   Zulassen Buchung von = 1. Dezember 2020.  

-   Anlagenbuchungen zugel. bis= leer  


### <a name="to-test-the-scenario"></a>So führen Sie ein Testszenario aus  

1.  Artikel Zu-/Abschläge erstellen:  

     Basismaßeinheit = PCS  

     Kostenberechnungsmethode = Durchschnitt  

     Wählen Sie Buchungsgruppen optional aus.  

2.  Neue Bestellung erstellen  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 15. Dezember 2020

     Kred.-Rechnungsnr.: 1234  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikel = ABSCHLAG  

     Menge = 1  

     Direkte Einheitskosten = 100  

     Lieferung und Rechnung buchen.  

3.  Einen neuen Verkaufsauftrag erstellen:  

     Verk. an Deb.-Nr.: 10000  

     Buchungsdatum = 16. Dezember 2020  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikel = ABSCHLAG  

     Menge = 1  

     VK-Preis = 135  

     Liefernung und Rechnung buchen.  

4.  Finanzbuchhaltungs-Einrichtung:  

     Zulassen Buchung von = am 1. Januar 2021  

     Anlagenbuchungen zugel. bis = leer  

5.  Neue Bestellung erstellen:  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 2. Januar 2021  

     Kred.-Rechnungsnr.: 2345  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikelkosten = FRACHT  

     Menge = 1  

     Direkte Einheitskosten = 3  

     Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.  

     Empfang und Rechnung buchen.  


**Status Artikelposten des Einkaufsschritts 2**:  
  
|Postennummer  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ABSCHLAG         |2020-12-15         |Einkauf         |107030         |1         |105         |0        |

**Wertposten**  

|Postennummer |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Artikelpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Lfd. Nr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ABSCHLAG|   2020-12-15    |324         |Einkauf         |Direkte Kosten         |108029         |         |1          |100    |100         |NEIN         |0         |
|399      |ABSCHLAG   |2021-01-02    |324         |Einkauf         |Direkte Kosten         |108009         |FRACHT         |0         |3         |3         |NEIN         |0         |


**Status Artikelposten Verkauf**:  
  
|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ABSCHLAG         |2020-12-16         |Verkauf         |102035         |-1         |-105         |0        |

**Wertposten**  

|Postennummer |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Artikelpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Lfd. Nr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ABSCHLAG|   2020-12-16    |325         |Verkauf         |Direkte Kosten         |109024         |         |-1          |-100    |-100         |NEIN         |0         |
|400      |ABSCHLAG   |2021-01-01    |325         |Verkauf         |Direkte Kosten         |109024         |         |0         |-3         |-3         |Ja         |398         |


6.  Am Arbeitsdatum vom 3. Januar geht eine Einkaufsrechnung ein, die eine zusätzliche Belastung für den in Schritt 2 getätigten Einkauf enthält. Diese Rechnung hat ein Belegdatum vom 30. Dezember und wird daher mit Buchungsdatum am 30. Dezember 2020 gebucht.  

     Neue Bestellung erstellen:  

     Eink. von Kred.-Nr.: 10000  

     Buchungsdatum = 30. Dezember 2020  

     Kred.-Rechnungsnr.: 3456  

     Lagerdurchlaufzeit der Einkaufsbestellung:  

     Artikelkosten = FRACHT  

     Menge = 1  

     Direkte Einheitskosten = 2  

     Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.  

     Empfang und Rechnung buchen.  


**Status Artikelposten des Einkaufs**:  

|Postennummer  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ABSCHLAG         |2020-12-15         |Einkauf         |107030         |1         |105         |0        |

**Wertposten**  

|Eingabenr. |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Artikelpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Lfd. Nr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ABSCHLAG   |2020-12-15    |324         |Einkauf         |Direkte Kosten         |108029         |            |1         |100    |100         |Nein         |0         |
|399      |ABSCHLAG   |2021-01-02    |324         |Einkauf         |Direkte Kosten         |108030         |FRACHT   |0         |3         |3         |Nein         |0         |
|401      |ABSCHLAG   |**2020-12-30**    |324         |Einkauf         |Direkte Kosten         |108031         |FRACHT   |0         |2         |2         |Nein         |0         |

**Status Artikelposten Verkauf**:  
  
|Postennummer  |Artikelnr.  |Buchungsdatum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ABSCHLAG         |2020-12-16         |Verkauf         |102035         |-1         |-105         |0        |

**Wertposten**  

|Eingabenr. |Artikelnr.  |Buchungsdatum  |Artikelposten Lfd. Nr.  |Artikelpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Artikelpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Lfd. Nr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ABSCHLAG   |2020-12-16        |325         |Verkauf         |Direkte Kosten         |103024         |            |-1         |-100       |-100         |Nein         |0         |
|400      |ABSCHLAG   |2021-01-01        |325         |Verkauf         |Direkte Kosten         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |ABSCHLAG   |**2021-01-01**    |325         |Verkauf         |Direkte Kosten         |103024         |            |0          |-2         |-2         |Ja         |398         |

Lager-Bewertungsbericht wird mit 31. Dezember 2020 gedruckt

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
