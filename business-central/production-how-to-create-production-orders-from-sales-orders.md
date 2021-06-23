---
title: 'Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:'
description: Sie können Fertigungsaufträge aus Verkaufsaufträgen erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115236"
---
# <a name="create-production-orders-from-sales-orders"></a>Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:
In diesem Fenster können Sie direkt zum aktuellen Verkaufsauftrag einen Fertigungsauftrag erstellen.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Fertigungsaufträge aus Verkaufsaufträgen erstellen  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den entsprechenden Link aus.  
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
