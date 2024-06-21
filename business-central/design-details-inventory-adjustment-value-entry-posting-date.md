---
title: Buchungsdatum auf Wertposten
description: 'Erfahren Sie wie die Stapelverarbeitung Lagerreg gekennzeichnet wird und ein Buchungsdatum auf Wertposten zugewiesen wird, der die Stapelverarbeitung erstellt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designdetails: Buchungsdatum auf Ausgleichs-Wertposten

Dieser Artikel enthält Anleitungen für Benutzer der Funktionalität der Bestandskalkulation in [!INCLUDE[prod_short](includes/prod_short.md)] und insbesondere für die Art und Weise, wie der Batchauftrag **Kosten kalkulieren – Element-Einträge** die Wert-Einträge, die der Batchauftrag erstellen soll, identifiziert und ihnen ein Buchungsdatum zuweist.

## Wie Buchungsdaten zugewiesen werden

Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** weist ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:  

1. Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.  

2. Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung überprüft.  

3. Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen. Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.  

Lassen Sie uns dieses Verfahren in der Praxis überprüfen. Angenommen, wir haben einen Artikelposten zum Verkauf. Der Artikel wurde am 5. September 2020 geliefert und er wurde am darauffolgenden Tag fakturiert.  

#### Artikelposten

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Postenart   | Belegnummer |Lagerortcode  |Menge  |Einstandsbetrag (tatsächl.)  |Fakturierte Menge  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Verkauf       |102033     |  Blau       | -1    |    -11     |-1     |    0     |

Nachfolgend finden Sie die zugehörigen Werteinträge:

- **Eintrag Nr. 379** stellt die Sendung dar und trägt dasselbe Buchungsdatum wie der übergeordnete Posten-Ledger-Eintrag.  
- **Eintrag Nr. 381** steht für die Rechnung.  
- **Eintrag Nr. 391** ist eine Anpassung des Rechnungswerts (Eintrag Nr. 381 oben).  

|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Artikelpostenart  |Postenart   |Belegnummer  |Artikelposten Lfd. Nr.  |Lagerortcode  |Artikelpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | Direkte Kosten   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    2020-09-10     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

Um das Buchungsdatum für **Eintrag Nr. 391** zuzuweisen, wurden die folgenden Schritte durchgeführt:

1. Dem zu erstellenden **Anpassungswert-Eintrag** (**Eintrag Nr. 391**) wird dasselbe **Buchungsdatum** zugewiesen wie dem Eintrag, den er anpasst.

2. Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung basiert.  

Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.  
  
#### Lagerbuchungsperioden

|Enddatum  |Name  |Geschlossen  |
|---------|---------|---------|
|2020-01-31     |2020. Januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |März 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |  Ja    |
|2020-08-31     |August 2020     |  Ja    |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |Dezember   2020   |         |

Das erste zugelassene Buchungsdatum ist der erste Tag der ersten offenen Periode, also der 1. September 2020.  

#### Finanzbuchhaltung Einrichtung

|Feld|Wert  |
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ-Code      |  

Das erste zulässige Buchungsdatum ist das in Feld **Buchungen zugel. ab** angegebene Datum: 10. September 2020. Wenn sowohl Lagerbuchungsperioden als auch erlaubte Buchungsdaten in **Hauptbuchhaltung-Einrichtung** definiert sind, definiert das spätere Datum von beiden den erlaubten Buchungsdatumsbereich.  

**Zuweisung eines erlaubten Buchungsdatums**  

Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht. Im zweiten Schritt stellt der Batchauftrag Lagerreg. fakt. Artikel-Einträge zugel. jedoch fest, dass das früheste zulässige Buchungsdatum der 10. September ist und ordnet somit den 10. September dem unten aufgeführten Eintrag für den Korrekturwert (**Eintrag Nr. 391**) zu.  


|Eingabenr.  |Artikelnr.  |Buchungsdatum  |Element Posten-Buchungsart  |Postenart   |Belegnummer  |Artikelposten Lfd. Nr.  |Lagerortcode  |Artikelpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Herkunftscode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | Direkte Kosten   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    **2020-09-10**     |    Verkauf     | Direkte Kosten   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

## Allgemeine Probleme mit dem „Lagerreg. fakt. Einst. Preise“-Batchauftrag

Es gibt zwei Szenarien, die dem Support-Team so häufig begegnen, dass sie einen eigenen Artikel zur Problemlösung rechtfertigen.

### Fehlermeldung: „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten...“

Wenn Sie auf diesen Fehler stoßen, müssen Sie die Daten anpassen, für die der Benutzer Buchungen zulassen darf. Weitere Informationen finden Sie unter [Fehlermeldung „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### Buchungsdatum der Korrekturwerteingabe gegenüber dem Buchungsdatum der Buchung, die die Korrektur verursacht, wie z.B. Neubewertung oder Artikel Zu-/Abschlag

Weitere Informationen finden Sie unter [Buchungsdatum der Korrekturwerteingabe im Vergleich zur Quellbuchung](design-details-inventory-adjustment-value-entry-source-entry.md).

## Weitere Informationen  

[Design Details: Kalkulation des Bestandes](design-details-inventory-costing.md)  
[Gestaltungsdetails: Element Anwendung](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
