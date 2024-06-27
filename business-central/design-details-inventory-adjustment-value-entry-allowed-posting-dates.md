---
title: Fehlermeldung „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“
description: 'Beheben Sie den Fehler, der sich hinter der Nachricht „Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“ verbirgt, wenn Sie den Batchauftrag Anlagenbuchungen zugel. bis Einst. Preise ausführen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Fehlermeldung: „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten...“

Wenn Sie den Batchauftrag **Lagerreg. fakt. Einst. Preise** verwenden, kann die folgende Fehlermeldung auftreten:

**Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten**

Diese Meldung zeigt an, dass Sie für das eingegebene Datum keine Posten buchen dürfen. Sie können dieses Problem umgehen, indem Sie Ihre Benutzereinrichtung ändern.

## <a name="change-the-user-setup"></a>Ändern Sie die Benutzereinrichtung

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

In diesem Fall dürfen Sie im Zeitraum vom 11. bis 30. September Buchungen vornehmen. Eine Buchung des Regulierungswertposten mit einem Buchungsdatum vom 10. September ist allerdings nicht möglich.  

### <a name="overview-of-the-posting-date-setup"></a>Übersicht über die Einrichtung des Buchungsdatums

#### <a name="inventory-periods"></a>Lagerbuchungsperioden

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

#### <a name="general-ledger-setup"></a>Finanzbuchhaltung Einrichtung

|Feld|Wert|
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ-Code      |  

#### <a name="user-setup"></a>Benutzereinrichtung

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|BENUTZERNAME |  2020-09-10      |2020-09-30      |

Durch die Zuweisung eines breiteren zulässigen Buchungsdatumsbereichs auf der Seite **Lagerbuchungsperiode** oder der Seite **Finanzbuchhaltung Einrichtung** kann der Konflikt, der die Fehlermeldung verursacht, vermieden werden. Der weitere Bereich ermöglicht es Ihnen beispielsweise, den Regulierungswertposten mit einem Buchungsdatum vom 10. September zu buchen.
  
## <a name="see-also"></a>Siehe auch

[Designdetails: Buchungsdatum für Regulierungswertposten](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
