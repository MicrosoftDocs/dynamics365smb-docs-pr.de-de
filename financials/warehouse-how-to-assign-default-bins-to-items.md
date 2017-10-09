---
title: "Vorgehensweise: Zuordnen der Vorgabelagerplätze zu Artikeln | Microsoft Docs"
description: "Wenn Sie in einem Lagerort Lagerplätze verwenden, kann das Zuordnen von Vorgabelagerplätzen zu Ihren Artikeln den Warenausgangs-, Wareneingangs- und Umlagerungsprozess wesentlich vereinfachen. Wenn einem Artikel ein Vorgabelagerplatz zugeordnet wurde, wird diesen Lagerplatz jedes Mal vorgeschlagen, wenn Sie eine Transaktion mit diesem Artikel starten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ae0d22fa5384edef167e5ba473977079c6473673
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-assign-default-bins-to-items"></a>Vorgehensweise: Zuordnen der Vorgabelagerplätze zu Artikeln
Wenn Sie in einem Lagerort Lagerplätze verwenden, kann das Zuordnen von Vorgabelagerplätzen zu Ihren Artikeln den Warenausgangs-, Wareneingangs- und Umlagerungsprozess wesentlich vereinfachen. Wenn einem Artikel ein Vorgabelagerplatz zugeordnet wurde, wird diesen Lagerplatz jedes Mal vorgeschlagen, wenn Sie eine Transaktion mit diesem Artikel starten. Vorgabelagerplätze werden im Fenster **Lagerplatzinhalt** definiert.  

## <a name="to-assign-a-default-bin-to-an-item"></a>So weisen Sie einen Standardlagerplatz einem Artikel zu
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Lagerplatzinh. Erst.-Vorschlag** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Geben Sie den Lagerplatzcode und die Artikelinformationen für jeden Lagerplatz ein, den Sie als Vorgabelagerplatz für einen Artikel einrichten möchten. Stellen Sie sicher, das das Feld **Standard** aktiviert ist.  
3.  Wählen Sie die **Lagerplatzinhalt erstellen** Aktion aus. Jetzt werden Ihrem Artikel Vorgabelagerplätze zugeordnet.  

> [!NOTE]  
>  Wenn ein Artikel eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, wird dem Artikel der Lagerplatz als Vorgabelagerplatz zugeordnet, in den der Artikel eingelagert wird.  

## <a name="to-change-the-default-bin-for-an-item"></a>So ändern Sie den Standardlagerplatz für einen Artikel  
Es kann sein, dass Sie die Zuordnung des Vorgabelagerplatzes für einen Artikel ändern oder einem neuen Artikel einen Vorgabelagerplatz zuordnen müssen.    
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Lagerplatzinhalt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Feld **Lagerortfilter** den geeigneten Lagerortcode aus.  
3.  Suchen Sie die aktuelle Zeile mit dem Vorgabewert des Artikels und deaktivieren Sie das Kontrollkästchen **Vorgabewert**.  
4.  Suchen Sie die Lagerplatzinhaltszeile des Lagerplatzes, den Sie als neuen Vorgabelagerplatz zuordnen möchten. Aktivieren Sie das Kontrollkästchen **Standardlagerplatz**.  

> [!NOTE]  
>  Wenn ein Artikel erstmalig eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, ordnet die Anwendung dem Artikel den Lagerplatz als Vorgabelagerplatz zu, in den der Artikel eingelagert wird.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

