---
title: 'Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:'
description: Lernen Sie die verschiedenen Möglichkeiten kennen, Produktionsaufträge für produzierte Artikel direkt aus Verkaufsaufträgen zu erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000883, 99000884
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 493d47e13d9ad1d7a2424dec4cd3691e92068d73
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973362"
---
# <a name="create-production-orders-from-sales-orders"></a>Erzeugen von Produktionsaufträgen aus Verkaufsaufträgen
In diesem Fenster können Sie direkt zum aktuellen Verkaufsauftrag einen Fertigungsauftrag erstellen.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Fertigungsaufträge aus Verkaufsaufträgen erstellen  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie den Verkaufsauftrag, für den Sie einen Fertigungsauftrag erstellen möchten.  
3.  Wählen Sie die Aktion **Planung** aus. Auf der Seite **Verkaufsauftragsplanung** können Sie die Verfügbarkeit des Verkaufsauftragsartikels anzeigen.  
4.  Wählen Sie die Aktion **Produktionsauftrag erstellen** aus.  
5.  Wählen Sie den Status und die Auftragsart aus.  
6.  Wählen Sie die Schaltfläche **Ja** aus, um einen oder mehrere Produktionsaufträge für die Zeilen zu erstellen, die **Fertigungsauftrag** im Feld **Beschaffungsmethode** haben.


> [!NOTE]  
> Bedarfszeilen im erstellten Produktionsauftrag, die **Prod. Auftrag** im Feld **Beschaffungsmethode** haben, stellen zugrunde liegende Fertigungsaufträge dar. Denken Sie daran, dass Sie nach der Erstellung dieser Fertigungsaufträge sämtliche nicht befriedigte Nachfrage nach Komponenten für diese auf der Seite **Auftragsplanung** oder mit der Funktion **Neu planen** aus erstellten Bestellungen identifizieren. 

## <a name="order-type"></a>Auftragsart  
Sie können zwischen zwei Methoden zur Erstellung von Produktionsaufträgen auswählen, wie in der folgenden Tabelle beschrieben.

|Option|Beschreibung|
|------|-----------|
|Artikelauftrag|Ein Fertigungsauftrag wird für jeden erforderlichen Fertigungsauftrag erstellt, der durch eine Zeile im Fenster **Verkaufsauftragsplanung** angegeben wird.|
|Projektauftrag|Ein Fertigungsauftrag wird für alle erforderlichen Fertigungsaufträge erstellt, die durch Zeilen im Fenster **Verkaufsauftragsplanung** angegeben werden. |

Wenn Sie Projektaufträge verwenden, enthält das Feld **Herkunftsart** des Fertigungsauftrags einen **Verkaufskopf** und der Auftrag besteht aus mehreren Zeilen, eine pro zu fertigenden Verkaufszeilenartikel.  


## <a name="see-also"></a>Siehe auch  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
