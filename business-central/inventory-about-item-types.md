---
title: Artikel-Arten verstehen| Microsoft Docs
description: Sie können die Lagerbewertung eines Artikels anpassen, indem Sie die FIFO. oder " Standard "oder Durchschnittskostenmethode anwenden, z. B. wenn Artikelkosten für Gründe, die keine Transaktionen betreffen, ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab3da8450586928a02d17ccce14c704ed6d7c8fe
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182396"
---
# <a name="about-item-types"></a>Info zu Elementtypen
Im Feld **Art** auf der Seite **Artikelkarte** können Sie auswählen, welche Artikel in Ihrer Unternehmung verwendet werden und deshalb im System verwaltet werden. Drei Optionen sind verfügbar:

|Option|Typischer Zweck|
|------|-----------|
|Lagerbestand|Eine physikalische Einheit, wie z. B. Rennrad für volle Geschäftsunterstützung.|
|Nicht-Lager|Eine physikalische Einheit, wie ein Bolzen, für begrenzte Geschäftsunterstützung beispielsweise da der Artikel nur intern verwendet wird und Basis Einstandspreis hat.|
|Dienst|Eine Arbeitszeiteinheit, wie eine Beratungsstunde, für begrenzte Geschäftsunterstützung.|

Die **Lagerbestand** Art umfasst die vollständige Verfolgung der Lagermenge und des Wertes. Daher werden alle Artikeltransaktionstypen unterstützt, und Artikel der Art Lager können mit allen Artikelbehandlungsfunktionen verwendet werden.

Die Arten **Service** und **Nicht-Lager** umfassen keine Nachverfolgung von Lagermengen und Werten. Daher werden nur die ausgewählten Geschäftsarten und Funktionen unterstützt.

Die drei Elementtypen unterstützen die folgenden Funktionen entsprechend.

|Artikelart|Verkauf|Einkauf|Job-Verbrauch|Serviceverbrauch|Verbrauch für Montage|Produktions-Verbrauch|Montageausstoß|Fertig produzierte Artikel (Istmeldungen)|Lagerortumlagerung|Physische Zählung|Lagerbestandsneubewertung|Lagerkosten|Artikelverfolgung|Reservierung|Lagerhaus|Planung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagerbestand|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Nicht-Lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|
|Dienst|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nein|Nein|Nein|Nein|Nein|

> [!NOTE]
> Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Katalogelemente sollen nicht mit regulären Artikel der Art Nicht-Lager verwechselt werden. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Die Artikel der Debitoren, die Sie im Service, wie z.B Drucker anbieten, werden Serviceartikel genannt. Serviceartikel haben nichts mit regulärem oder Katalogelementen zu tun. Aber Dienstkomponenten können normale Artikel sein. Weitere Informationen finden Sie unter [Serviceartikelkomponenten und Serviceartikel einrichten](service-how-setup-service-items.md).

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand einrichten](inventory-setup-inventory.md)  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
