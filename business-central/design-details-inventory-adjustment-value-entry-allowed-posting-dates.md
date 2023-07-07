---
title: Fehlermeldung „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“
description: Beheben Sie den Fehler, der sich hinter der Nachricht „Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“ verbirgt, wenn Sie den Batchauftrag Anlagenbuchungen zugel. bis Einst. Preise ausführen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 1694bc0267e32d2af4af1202b2dfd1ad4b46ba55
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139755"
---
# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Fehlermeldung: „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten...“

Wenn Sie den Batchauftrag **Kalkulation fakt. Einst. Preise anpassen** ausführen, kann die folgende Fehlermeldung auftreten:

**Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten**

Diese Nachricht zeigt an, dass der Benutzer keine Buchungen für das betreffende Datum zulassen darf. Dies kann durch eine Änderung der Benutzereinrichtung behoben werden.

## <a name="change-the-user-setup"></a>Ändern Sie die Benutzereinrichtung

|Benutzer ID  |Buchungen zugel. ab  | Buchungen zugel. bis  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

Der Benutzer in diesem Fall hat einen erlaubten Buchungsdatumsbereich vom 11. September bis zum 30. September und darf daher die Korrekturwertbuchung mit Buchungsdatum 10. September nicht buchen.  

### <a name="overview-of-involved-posting-date-setup"></a>Übersicht über die Einstellung des beteiligten Buchungsdatums

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

Durch die Zuweisung eines breiteren zulässigen Buchungsdatumsbereichs, wie in Lagerbuchungsperioden oder Finanzbuchhaltungs-Einrichtung, kann der Konflikt, der die Fehlermeldung verursacht, vermieden werden. Der Ausgleichs-Wertposten mit dem Buchungsdatum 10. September wird mit dieser Einrichtung erfolgreich gebucht.
  
## <a name="see-also"></a>Weitere Informationen

[Designdetails: Buchungsdatum auf Ausgleichs-Wertposten](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
