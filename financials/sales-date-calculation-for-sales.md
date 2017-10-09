---
title: "Terminberechnung für Verkäufe  | Microsoft Docs"
description: "Das Programm berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e8bc9e8b99db8afda83edb4aff13f5daf9f5a31
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-sales"></a>Terminberechnung für Verkäufe
[!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.

Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.

Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.

## <a name="calculating-a-requested-delivery-date"></a>So berechnen Sie ein gewünschtes Wareneingangsdatum:
Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.

- Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum

Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden.

Falls die Artikel am Lieferdatum nicht zur Kommissionierung zur Verfügung stehen, erscheint eine Warnmeldung die auf diesen Umstand hinweist.

## <a name="calculating-the-earliest-possible-delivery-date"></a>So berechnen Sie das frühestmögliche Lieferdatum:
Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet. Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.

- Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum


## <a name="see-also"></a>Siehe auch  
 [Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)   
 [So wird's gemacht: Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

