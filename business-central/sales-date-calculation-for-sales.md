---
title: Terminberechnung für Verkäufe
description: Die Anwendung berechnet automatisch das Datum, an dem Sie ein Element bestellen müssen, damit es zu einem bestimmten Datum im Bestand ist und zur Kommissionierung zur Verfügung steht.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 401deb016122100f86142cb2314c18e3b481bccd
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077866"
---
# <a name="date-calculation-for-sales"></a>Terminberechnung für Verkäufe

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.

Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.

Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.

## <a name="calculating-a-requested-delivery-date"></a>So berechnen Sie ein gewünschtes Wareneingangsdatum:

Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum dann als Ausgangspunkt für die folgenden Berechnungen verwendet.

- Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum

Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden. Andernfalls wird eine Bestandswarnung angezeigt.

> [!Note]
> Wenn Ihr Prozess auf einer Rückwärtsberechnung basiert, wenn Sie beispielsweise das angeforderte Lieferdatum verwenden, um das geplante Versanddatum zu erhalten, empfehlen wir, Datumsformeln mit fester Dauer zu verwenden, z. B. 5D für fünf Tage oder 1W für eine Woche. Datumsformeln ohne feste Dauer, wie „CW“ für die aktuelle Woche oder CM für den aktuellen Monat, können zu falschen Datumsberechnungen führen. Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>So berechnen Sie das frühestmögliche Lieferdatum:

Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet. Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.

- Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

 [Datumsberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)  
 [Lieferterminzusagen-Daten berechnen](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]