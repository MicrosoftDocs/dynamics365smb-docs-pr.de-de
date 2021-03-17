---
title: Terminberechnung für Einkäufe  | Microsoft Docs
description: Die Anwendung berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 03cdb942a088b27be5c89843da4a958d0e13f843
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388274"
---
# <a name="date-calculation-for-purchases"></a>Terminberechnung für Einkäufe

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.  

Wenn Sie ein gewünschtes Wareneingangsdatum in einem Einkaufsbestellkopf angeben, ist das berechnete Auftragsdatum das Datum, an dem die Bestellung erfolgen muss, um die Artikel an dem Datum zu erhalten, das Sie angefordert haben. Dann wird das Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen, im Feld **Erwartetes Eingangsdatum** berechnet und eingegeben.  

Wenn Sie kein gewünschtes Wareneingangsdatum angeben, wird das Bestelldatum in der Zeile als Ausgangspunkt zur Berechnung des Datums verwendet, an dem die Artikel eingehen sollen, und des Datums, an dem die Artikel für die Kommissionierung zur Verfügung stehen.  

## <a name="calculating-with-a-requested-receipt-date"></a>Berechnung mit einem gewünschten Wareneingangsdatum

Falls es ein gewünschtes Wareneingangsdatum in der Einkaufsbestellungszeile gibt, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.  

- Gewünschtes Wareneingangsdatum – Beschaffungszeit = Bestelldatum  
- Gewünschtes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Wenn Sie ein gewünschtes Wareneingangsdatum im Bestellkopf angegeben haben, wird dieses Datum in das entsprechende Feld in allen Zeilen kopiert. Sie können dieses Datum in den einzelnen Zeilen ändern oder entfernen.  

> [!NOTE]
> Wenn Ihr Prozess auf einer Rückwärtsberechnung basiert, wenn Sie beispielsweise das angeforderte Wareneingangsdatum verwenden, um das geplante Auftragsdatum zu erhalten, empfehlen wir, Datumsformeln mit fester Dauer zu verwenden, z. B. 5D für fünf Tage oder 1W für eine Woche. Datumsformeln ohne feste Dauer, wie „CW“ für die aktuelle Woche oder CM für den aktuellen Monat, können zu falschen Datumsberechnungen führen. Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Berechnung ohne ein gewünschtes Wareneingangsdatum

Wenn Sie eine Bestellzeile ohne ein gewünschtes Lieferdatum eingeben, füllt die Anwendung das Feld **Bestelldatum** in der Zeile mit dem **Bestelldatum** im Bestellkopf. Hierbei handelt es sich entweder um das Datum, das Sie eingegeben haben, oder um das Arbeitsdatum. Die folgenden Datumsangaben werden dann in der Einkaufsbestellungszeile berechnet, mit dem Bestelldatum als Ausgangspunkt.  

- Bestelldatum + Beschaffungszeit = Geplantes Wareneingangsdatum  
- Geplantes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Falls Sie das Bestelldatum in der Zeile ändern (z. B. weil die Artikel bei dem Kreditor erst zu einem späteren Datum verfügbar sind), werden die entsprechenden Datumsangaben in der Zeile automatisch neu berechnet.  

Wenn Sie das Bestelldatum im Kopf ändern, wird das Datum in allen Zeilen in das Feld  kopiert, und alle zugehörigen **Datumsfelder** werden neu berechnet.  

## <a name="default-values-for-lead-time-calculation"></a>Standardwerte für die Vorlaufzeitberechnung

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Wert aus dem Feld **Vorlaufzeitberechnung** in der Bestellzeile, um die Bestellung und die erwarteten Eingangsdaten zu berechnen.  

Sie können den Wert in der Zeile manuell angeben oder das Programm Werte verwenden lassen, die auf der Lieferantenkarte, der Artikelkarte, der Lagereinheitskarte oder dem Artikellieferantenkatalog definiert sind.
Der Wert für die Vorlaufzeit auf der Lieferantenkarte wird jedoch nur verwendet, wenn auf der Artikelkarte, der Karte der Lagereinheit oder dem Artikellieferantenkatalog für den Artikel keine Vorlaufzeit angegeben ist. Dies ist auch die eskalierende Prioritätsreihenfolge für diese Werte. Wenn alle angegeben sind, hat die Vorlaufzeit von der Lieferantenkarte die niedrigste Priorität, und die Vorlaufzeit aus dem Lieferantenkatalog des Artikels hat die höchste Priorität.  

## <a name="see-also"></a>Siehe auch

[Terminberechnung für Verkäufe](sales-date-calculation-for-sales.md)   
[Lieferterminzusagen-Daten berechnen](sales-how-to-calculate-order-promising-dates.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]