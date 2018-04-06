---
title: 'Vorgehensweise: Einrichten von Zuteilungsquellen und -zielen | Microsoft Docs'
description: Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d4dcf5f95d5fc44d4b8fb72b55d905c876989a56
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-allocation-source-and-targets"></a>Richten Sie die Zuteilungsquelle und Ziele ein
Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden.  

## <a name="to-set-up-cost-allocations"></a>So richten Sie Kostenzuordnungen ein  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kostenzuteilung** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Kostenzuteilung** die Aktion **Bearbeiten** aus.  
3.  Geben Sie eine ID für die Zuordnungsquelle in das Feld **ID** ein.  
4.  Definieren Sie eine **Ebene** als Zahl zwischen 1 und 99 im Feld . Die Verteilungsbuchung richtet sich nach der Reihenfolge der Stufen.  
5.  Geben Sie eine Kostenart ein, um festzulegen, welche Kostenarten im Feld **Kostenartbereich** zugeordnet werden. Wenn alle Kosten für eine Kostenart zugeordnet werden, wird kein Bereich definiert.  
6.  Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein.  
7.  Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein. Am häufigsten bleibt das Feld leer, da Kostenobjekte selten anderen Kostenträgern zugeordnet werden.  
8.  Geben Sie im Feld **Für Kostenart gutschreiben** eine Kostenart ein. Die Kosten, die zugeteilt werden, werden der ursprünglichen Kostenart gutgeschrieben. Die Kreditbuchung wird auf Kostenart gebucht, die hier angegeben ist.  
9. Definieren Sie im Inforegister **Zeilen** die Verteilungsziele. Geben Sie auf der ersten Zeile unter **Zielkostenart** eine Kostenart ein. So definieren Sie, unter welcher Kostenart die Zuordnung gebucht wird.  
10. Geben Sie in der ersten Zeile das erste Zuordnungsziel in das Feld **Zielkostenstelle** oder **Zielkostenobjekt** ein. Diese beiden Felder definieren, auf welche Kostenstelle oder welchen Kostenträger die Zuordnung gebucht wird. Sie können eines dieses Felder ausfüllen, aber nicht beide.  
11. Wiederholen Sie dieselben Schritte in der zweiten Zeile, um zusätzliche Zuordnungsziele einzurichten.  
12. Nach dem Einrichten der Zuordnungsziele und -quellen wählen Sie auf der Registerkarte Start in der Gruppe Prozess die Aktion **Verteilungsschlüssel berechnen** aus, um die gesamten Aktienwerte zu berechnen.  

> [!NOTE]  
>  Aktivieren Sie das Kontrollkästchen **Gesperrt**, um die Verteilungseinrichtung zu deaktivieren.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
 [Setzen von Filtern für dynamische Zuteilungsgrundlagen](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Szenario-Beispiel: Definieren von statischen Verteilungen basierend auf dem Verteilungsverhältnis](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)   
 [Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

