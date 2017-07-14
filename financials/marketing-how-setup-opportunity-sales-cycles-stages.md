---
title: "Vorgehensweise: Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen| Microsoft Docs"
description: "Beschreibt das Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen in Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# Vorgehensweise: Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen
<a id="how-to-set-up-opportunity-sales-cycles-and-cycle-stages" class="xliff"></a>
Damit die Verkaufschancen verwendet werden kann, müssen zunächst Verkaufsprozesse sowie Verkaufsprozess-Stufen eingerichtet werden. Ein Verkaufsprozess setzt sich aus einer Reihe von Schritten zusammen, die vom ersten Kontakt bis zu einem Verkaufsabschluss reichen. Jeder Stufe kann bestimmten Bedingungen haben, die erfüllen sein müssen (z. B. ein Verkaufsangebot), bevor eine Verkaufschance in die nächste Stufe gehen kann. Sie können auch festlegen, ob eine Stufe übersprungen werden kann. Verkaufsprozesse können in beliebiger Anzahl eingerichtet werden. Gleiches gilt auch für die Anzahl der Verkaufsprozess-Stufen, die innerhalb eines Verkaufsprozesses eingerichtet werden.

Das Implementieren des Verkaufsprozesses für Verkaufschancen umfasst das Einrichten des Verkaufsprozesscodes, das Definiert der verschiedenen Stufen des Zyklus, und das Zuweisen des Zyklus zu den Verkaufschancen.

## Einrichten eines Verkaufsprozesscodes
<a id="to-set-up-an-opportunity-sales-cycle-code" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Verkaufszyklen** ein und wählen Sie dann den entsprechenden Link aus. Das **Verkaufsprozesse**-Fenster wird geöffnet und führt alle vorhandenen Verkaufsprozesse auf.
2. Wählen Sie Aktion **Neu** aus, und füllen Sie die Felder aus.

Wiederholen Sie diese Schritte, um weitere Verkaufsprozesse einzurichten. Nachdem Sie Verkaufsprozesse für Verkaufschancen eingerichtet haben, können Sie die verschiedenen Stufen innerhalb jedes Prozesses einrichten.

## Verkaufsprozessstufe der Verkaufschance definieren
<a id="to-define-opportunity-sales-cycle-stages" class="xliff"></a>
1. Wählen Sie im Fenster **Verkaufsprozesse** den Verkaufsprozess für Verkaufschancen aus, für den Sie Stufen einrichten möchten, und wählen Sie dann die Aktion **Stufen**. Das Fenster **Verkaufsprozess-Stufen** wird geöffnet.
2. Klicken Sie auf **Neu**, um eine neue Stufe für den Verkaufsprozess einzugeben.

Wiederholen Sie diese Schritte, um beliebig viele Stufen innerhalb des Verkaufsprozesses einzurichten.

## Eine Verkaufsprozessstufe zu einer Verkaufschance zuordnen
<a id="to-assign-stage-cycle-to-an-opportunity" class="xliff"></a>
Nachdem Sie die Stufe des Verkaufprozesses hinzugefügt haben, können Sie Verkaufschancen hinzufügen und dann die Stufe des Verkaufprozesses zu Verkaufschancen hinzufügen, indem Sie das Feld **Verkaufsprozesscode** verwenden. Weitere Informationen finden Sie unter [Gewusst wie: Erstellen von Verkaufschancen](marketing-how-create-opportunities.md).

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verarbeiten von Verkaufschancen](marketing-processing-sales-opportunities.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeitend mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

