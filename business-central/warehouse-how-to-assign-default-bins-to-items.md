---
title: So weisen Sie Artikeln Standardlagerplätze zu
description: Wenn Sie in einem Lagerort Lagerplätze verwenden, kann das Zuordnen von Vorgabelagerplätzen zu Ihren Artikeln den Warenausgangs-, Wareneingangs- und Umlagerungsprozess wesentlich vereinfachen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 05d338234bbb4a6c578935c8aa29e32f9453f615
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445872"
---
# <a name="assign-default-bins-to-items"></a>Zuordnen der Vorgabelagerplätze zu Artikeln
Wenn Sie Lagerplätze an einem Lagerort verwenden, kann das Zuweisen von Standard-Lagerplätzen zu Ihren Artikeln den Prozess des Versands, des Empfangs und des Umzugs Ihrer Artikel erheblich vereinfachen. Wenn einem Artikel ein Vorgabelagerplatz zugeordnet wurde, wird diesen Lagerplatz jedes Mal vorgeschlagen, wenn Sie eine Transaktion mit diesem Artikel starten. Vorgabelagerplätze werden auf der Seite **Lagerplatzinhalt** definiert.  

## <a name="to-assign-a-default-bin-to-an-item"></a>So weisen Sie einen Standardlagerplatz einem Artikel zu
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerplatzinhalt Erst.-Arbeitsblatt** ein und wählen Sie den entsprechenden Link.  
2.  Geben Sie den Lagerplatzcode und die Artikelinformationen für jeden Lagerplatz ein, den Sie als Vorgabelagerplatz für einen Artikel einrichten möchten. Stellen Sie sicher, das das Feld **Standard** aktiviert ist.  
3.  Wählen Sie die **Lagerplatzinhalt erstellen** Aktion aus. Jetzt werden Ihrem Artikel Vorgabelagerplätze zugeordnet.  

> [!NOTE]  
>  Wenn ein Artikel eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, wird dem Artikel der Lagerplatz als Vorgabelagerplatz zugeordnet, in den der Artikel eingelagert wird.  

## <a name="to-change-the-default-bin-for-an-item"></a>So ändern Sie den Standardlagerplatz für einen Artikel  
Es kann sein, dass Sie die Zuordnung des Vorgabelagerplatzes für einen Artikel ändern oder einem neuen Artikel einen Vorgabelagerplatz zuordnen müssen.    
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerplatzinhalt** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie im Feld **Lagerortfilter** den geeigneten Lagerortcode aus.  
3.  Suchen Sie die aktuelle Zeile mit dem Vorgabewert des Artikels und deaktivieren Sie das Kontrollkästchen **Vorgabewert**.  
4.  Suchen Sie die Lagerplatzinhaltszeile des Lagerplatzes, den Sie als neuen Vorgabelagerplatz zuordnen möchten. Aktivieren Sie das Kontrollkästchen **Standardlagerplatz**.  

> [!NOTE]  
>  Wenn ein Artikel erstmalig eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, ordnet die Anwendung dem Artikel den Lagerplatz als Vorgabelagerplatz zu, in den der Artikel eingelagert wird.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]