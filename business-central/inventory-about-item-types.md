---
title: Verstehen von Element-Typen
description: Sie können die Bestandsbewertung eines Elements mit der FIFO- oder Durchschnittskalkulation anpassen, wenn sich die Kosten des Elements aus anderen Gründen als Transaktionen ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 2541f509d02a584620c83903c3b92983aba1c2a8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6322794"
---
# <a name="about-item-types"></a>Info zu Elementtypen
Im Feld **Art** auf der Seite **Artikelkarte** können Sie auswählen, welche Artikel in Ihrer Unternehmung verwendet werden und deshalb im System verwaltet werden. Drei Optionen sind verfügbar:

|Option|Typischer Zweck|
|------|-----------|
|Bestand|Eine physikalische Einheit, wie z. B. Rennrad für volle Geschäftsunterstützung.|
|Kein Bestand|Eine physikalische Einheit, wie ein Bolzen, für begrenzte Geschäftsunterstützung beispielsweise da der Artikel nur intern verwendet wird und Basis Einstandspreis hat.|
|Service|Eine Arbeitszeiteinheit, wie eine Beratungsstunde, für begrenzte Geschäftsunterstützung.|

Die Art **Bestand** umfasst die vollständige Verfolgung der Lagermenge und des Wertes. Daher werden alle Artikeltransaktionstypen unterstützt, und Artikel der Art „Bestand“ können mit allen Artikelbehandlungsfunktionen verwendet werden.

Die Arten **Service** und **Kein Bestand** umfassen keine Nachverfolgung von Lagermengen und Werten. Daher werden nur die ausgewählten Geschäftsarten und Funktionen unterstützt.

Die drei Elementtypen unterstützen die folgenden Funktionen entsprechend.

|Artikelart|Verkauf|Einkauf|Job-Verbrauch|Serviceverbrauch|Verbrauch für Montage|Produktions-Verbrauch|Montageausstoß|Fertig produzierte Artikel (Istmeldungen)|Lagerortumlagerung|Physische Zählung|Bestandsneubewertung|Bestandskosten|Artikelverfolgung|Reservierung|Lagerhaus|Planung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Bestand|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Kein Bestand|Ja|Ja|Ja|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|
|Service|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|

## <a name="costing-methods-for-types-of-items"></a>Kalkulationsmethoden für Artikeltypen
Wenn Sie Lagerbuchungen vornehmen, werden die Mengen- und Wertänderungen des Bestands in den Artikelposten bzw. Wertposten erfasst. 

Für Lagerartikel werden die Kosten im Feld **Einstandsbetrag (tatsächl.)** auf der Seite **Wertposten** erfasst und bei der Abstimmung mit der Finanzbuchhaltung werden die Kosten im Feld **Gebuchte Lagerregulierung** angezeigt. Weitere Informationen finden Sie unter [Designdetails: Bestandskosten](design-details-inventory-costing.md).

Für Nicht-Bestands- und Serviceartikel werden die Kosten im Feld **Einst.-Betr. (lagerwertunabh.)** auf der Seite **Wertposten** erfasst. Für Nicht-Bestands- und Serviceartikel werden die Kosten in den Verkaufs-, Montage- und Produktionsbelegen und -buchungsblättern angegeben. Die Standardkosten können im Feld **Einstandspreis** auf den Seiten **Artikelkarte** und **Lagerhaltungsdaten** angegeben werden. Die Kosten für diese Arten von Artikeln werden nicht mit der Finanzbuchhaltung abgeglichen. 

## <a name="catalog-and-service-items"></a>Katalog- und Serviceartikel
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Katalogelemente sollen nicht mit regulären Artikel der Art Kein Bestand verwechselt werden. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

Die Artikel der Debitoren, die Sie im Service, wie z. B Drucker anbieten, werden Serviceartikel genannt. Serviceartikel haben nichts mit regulärem oder Katalogelementen zu tun. Aber Servicekomponenten können normale Artikel sein. Weitere Informationen finden Sie unter [Serviceartikelkomponenten und Serviceartikel einrichten](service-how-setup-service-items.md).

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand einrichten](inventory-setup-inventory.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]