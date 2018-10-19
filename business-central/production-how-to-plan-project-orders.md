---
title: Projekt nach Projekt planen | Microsoft Docs
description: "Diese Planungsaufgabe beginnt mit einem Verkaufsauftrag im Fenster **Verkaufsauftragsplanung**. Nachdem ein Projektfertigungsauftrag erstellt wurde, kann die Planung im Fenster **Auftragsplanung** fortgeführt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 08cd8c323e8f5221bd6915618582441a739e77c8
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="plan-project-orders"></a>Projektaufträge planen
Diese Planungsaufgabe beginnt mit einem Verkaufsauftrag im Fenster **Verkaufsauftragsplanung**. Nachdem ein Projektfertigungsauftrag erstellt wurde, kann die Planung im Fenster **Auftragsplanung** fortgeführt werden.  

## <a name="to-create-a-project-production-order"></a>Projektfertigungsaufträge erstellen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Verkaufsauftrag, der für das Produktionsprojekt steht, und wählen die Aktion **Planung**.  
4.  Klicken Sie im Fenster  **Verkaufsauftragsplanung** auf  **Produktionsauftrag erstellen**.  
5.  Wählen Sie im Fenster **Auftrag aus Verkauf erstellen** im Feld **Auftragsart** die Option **Projektauftrag** aus.  
6.  Wählen Sie die Schaltfläche **Ja** aus.  
7.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Produktionsaufträge** ein, und wählen dann den zugehörigen Link aus.
8. Öffnen Sie den soeben erstellten Fertigungsauftrag.  

    Im Feld **Herkunftsart** des Fertigungsauftrags ist ein **Verkaufskopf** enthalten, und der Auftrag besteht aus mehreren Zeilen, eine pro zu fertigenden Verkaufszeilenartikel.  
9. Wählen Sie die Aktion **Planung** aus.
10. Klicken Sie im Fenster **Auftragsplanung** auf Funktionen und dann auf **Aktualisieren**, um den neuen Bedarf zu kalkulieren.  

Die Auftragskopfzeile für das Projekt wird angezeigt, wobei alle Zeilen für nicht erfüllten Bedarf darunter erweitert sind. Obwohl der Fertigungsauftrag Zeilen für mehrere gefertigte Artikel enthält, wird der Gesamtbedarf für alle Fertigungsauftragszeilen unter einer Auftragskopfzeile im Fenster **Auftragsplanung** aufgeführt, und der ursprüngliche Debitorenname wird angezeigt. Setzen Sie die Planung für den Bedarf so fort wie unter [Bedarf für neuen Auftrag nach Auftrag planen](production-how-to-plan-for-new-demand.md) beschrieben.  

> [!NOTE]  
>  Bedarfszeilen im projektbezogenen Produktionsauftrag, die **Prod. Auftrag** im Feld **Beschaffungsmethode** haben, stellen zugrunde liegende Fertigungsaufträge dar. Nachdem Sie diese Fertigungsaufträge erstellt haben, müssen Sie nochmals den Plan im Fenster **Auftragsplanung** berechnen, um sämtliche nicht befriedigte Nachfrage nach Komponenten für diese zu identifizieren. Dies bedeutet, dass die Projektbeziehung nicht mehr im Fenster sichtbar ist. Wenn Sie jedoch die Option "Auftragsverfolgung" verwenden, können Sie für alle Beschaffungsaufträge, die unter dem ursprünglichen Verkaufsauftrag erstellt wurden, eine Rück- und Vorschau ausführen.  

## <a name="see-also"></a>Siehe auch
[Planung](production-planning.md)   
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

