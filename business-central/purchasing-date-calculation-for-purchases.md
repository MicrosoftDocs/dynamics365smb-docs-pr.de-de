---
title: Daten für Einkäufe berechnen
description: In diesem Artikel wird beschrieben, wie Sie Daten für Einkäufe berechnen können.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase order, purchase, date, receipt, delivery, lead time
ms.search.forms: ''
ms.date: 02/06/2022
ms.author: bholtorf
ms.openlocfilehash: 779c2ac1b043cee6f2578f3a642a26a8bb3156c8
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079532"
---
# <a name="calculate-dates-for-purchases"></a>Daten für Einkäufe berechnen

Wenn sich Artikel zu einem bestimmten Datum im Lager befinden sollen, kann [!INCLUDE[prod_short](includes/prod_short.md)] das Datum berechnen, an dem Sie die Artikel bestellen müssen. 

Das Ergebnis ist das Datum, an dem Sie die bestellten Artikel kommissionieren können.  

Wenn Sie in einer Bestellposition ein gewünschtes Wareneingangsdatum angeben, ist das berechnete Bestelldatum das Datum, an dem Sie die Bestellung aufgeben müssen. Das Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen, wird im Feld **Erwartetes Eingangsdatum** angezeigt.  

Wenn Sie kein angefordertes Wareneingangsdatum angeben, basiert das Datum, an dem Sie den Eingang des Artikels erwarten, auf dem Bestelldatum in der Zeile. 

Das Wareneingangsdatum ist auch das Datum, an dem die Artikel zur Kommissionierung verfügbar sind.  

> [!TIP]
> Standardmäßig sind viele der in diesem Artikel erwähnten Datumsfelder in Bestellpositionen ausgeblendet. Wenn ein Feld nicht verfügbar ist, können Sie es hinzufügen, indem Sie die Seite personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a>Berechnung mit einem gewünschten Wareneingangsdatum

Falls ein gewünschtes Wareneingangsdatum in der Bestellzeile vorhanden ist, wird dieses Datum als Grundlage für die folgenden Berechnungen verwendet:  

- Gewünschtes Wareneingangsdatum – Beschaffungszeit = Bestelldatum  
- Gewünschtes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Wenn Sie ein angefordertes Wareneingangsdatum in einer Bestellposition angeben, wird dieses Datum neuen Positionen zugewiesen, wenn Sie sie erstellen. Das Datum in den Zeilen können bei Bedarf geändert oder entfernt werden.  

> [!NOTE]
> Wenn Ihr Prozess auf einer Rückwärtsberechnung basiert, wenn Sie beispielsweise das angeforderte Wareneingangsdatum verwenden, um das geplante Auftragsdatum zu erhalten, empfehlen wir, Datumsformeln mit fester Dauer zu verwenden, z. B. 5D für fünf Tage oder 1W für eine Woche. Datumsformeln ohne feste Dauer, wie „CW“ für die aktuelle Woche oder CM für den aktuellen Monat, können zu falschen Datumsberechnungen führen. Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Berechnung ohne ein gewünschtes Wareneingangsdatum

Wenn Sie eine Bestellzeile ohne ein gewünschtes Lieferdatum eingeben, zeigt das Feld **Bestelldatum** in der Zeile das Datum im Feld **Bestelldatum** im Bestellkopf an. Dieses Datum ist entweder das von Ihnen eingegebene Datum oder das Arbeitsdatum. Die Daten werden dann wie folgt für die Bestellzeile berechnet, wobei das Bestelldatum als Ausgangspunkt dient:  

- Bestelldatum + Beschaffungszeit = Geplantes Wareneingangsdatum  
- Geplantes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Wenn Sie das Bestelldatum auf der Zeile ändern, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] die anderen Daten neu.  

## <a name="default-values-for-lead-time-calculation"></a>Standardwerte für die Vorlaufzeitberechnung

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet das Datumsformular im Feld **Vorlaufzeitberechnung** in der Bestellzeile, um die Bestellung und die erwarteten Eingangsdaten zu berechnen.  

Sie können die Datumsformel manuell in Zeilen angeben. Andernfalls verwendet [!INCLUDE[prod_short](includes/prod_short.md)] die auf den folgenden Seiten definierten Formeln in der Reihenfolge der Priorität:

1. Artikel/Lieferanten Katalog
2. Artikelkarte
3. Lagerhaltungsdatenkarte
4. Kreditorenkarte

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Terminberechnung für Verkäufe](sales-date-calculation-for-sales.md)  
[Lieferterminzusagen-Daten berechnen](sales-how-to-calculate-order-promising-dates.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]