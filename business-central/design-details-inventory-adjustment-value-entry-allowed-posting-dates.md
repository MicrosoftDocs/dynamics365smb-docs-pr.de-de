---
title: Fehlermeldung „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“
description: 'Beheben Sie den Fehler, der sich hinter der Nachricht „Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“ verbirgt, wenn Sie den Batchauftrag Anlagenbuchungen zugel. bis Einst. Preise ausführen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Fehlermeldung: „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten...“

Wenn Sie den Batchauftrag **Kalkulation fakt. Einst. Preise anpassen** ausführen, kann die folgende Fehlermeldung auftreten:

**Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten**

Diese Nachricht zeigt an, dass der Benutzer keine Buchungen für das betreffende Datum zulassen darf. Dies kann durch eine Änderung der Benutzereinrichtung behoben werden.

## Ändern Sie die Benutzereinrichtung  

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

Der Benutzer in diesem Fall hat einen erlaubten Buchungsdatumsbereich vom 11. September bis zum 30. September und darf daher die Korrekturwertbuchung mit Buchungsdatum 10. September nicht buchen.  

### Übersicht über die Einstellung des beteiligten Buchungsdatums

#### Lagerbuchungsperioden

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

#### Finanzbuchhaltung Einrichtung

|Feld|Wert|
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ-Code      |  

#### Benutzereinrichtung

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|BENUTZERNAME |  2020-09-10      |2020-09-30      |

Durch die Zuweisung eines breiteren zulässigen Buchungsdatumsbereichs, wie in Lagerbuchungsperioden oder Finanzbuchhaltungs-Einrichtung, kann der Konflikt, der die Fehlermeldung verursacht, vermieden werden. Der Ausgleichs-Wertposten mit dem Buchungsdatum 10. September wird mit dieser Einrichtung erfolgreich gebucht.
  
## Weitere Informationen  

[Designdetails: Buchungsdatum auf Ausgleichs-Wertposten](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
