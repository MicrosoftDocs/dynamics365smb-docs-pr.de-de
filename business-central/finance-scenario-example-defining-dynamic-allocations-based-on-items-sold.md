---
title: 'Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel | Microsoft Docs'
description: Dieses Thema zeigt ein Beispiel für das Definieren von Zuordnungen mithilfe der Methode der dynamischen Verteilung.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 7219e1d56129da66e802aa0b4ea5df946dc34e04
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239590"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel
Dieses Thema zeigt ein Beispiel für das Definieren von Zuordnungen mithilfe der Methode der dynamischen Verteilung. In dem Beispiel ändern Sie die dynamische Verteilung der Kosten für die VERKAUF-Kostenstelle, sodass der neue Kostenträger COMPUTERAUSSTATTUNG unterstützt wird. COMPUTERAUSSTATTUNG-Pakete haben Artikelnummern im Bereich von 8904-W bis 8924-W. Sie verwenden die Verkaufszahlen des Vorjahres, um den Anteil zu berechnen. Die Verteilung wird auf die helfende Kostenart 9903 gebucht.  

> [!NOTE]  
>  Das Beispiel verwendet die Demodaten in [!INCLUDE[d365fin](includes/d365fin_md.md)]  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>So definieren Sie dynamische Zuteilungen auf der Basis der im Vorjahr verkauften Artikel  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenzuteilung** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Kostenzuteilung** die Aktion **Neu** aus.  
3.  Drücken Sie im Feld **ID** die EINGABETASTE, oder geben Sie eine ID ein.  
4.  Geben Sie in dem Feld **Menge** **1** ein.  
5.  In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.  
6.  Geben Sie im Feld **Kostenstellencode** **VERKAUF** ein.  
7.  Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  
8.  Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  
9. Wählen Sie im Feld **Zielkostenobjekt** die Option **Neu** aus, um einen neuen Kostenträger COMPUTERAUSSTATTUNG zu erstellen, und füllen Sie ggf. Felder aus. Wählen Sie **COMPUTERAUSSTATTUNG** aus. Lassen Sie das Feld **Zielkostenstelle** leer.  
10. Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
11. Wählen Sie im Feld **Basis** die Verteilungsgrundlage **Verkaufte Artikel (Betrag)** aus.  
12. Geben Sie im Feld **Nummernfilter** den Wert **8904-W..8924-W** ein.  
13. In dem Feld **Datumsfiltercode** geben Sie **Vorjahr** ein.  
14. Damit der Vorschlag berechnet wird, klicken Sie auf Aktionen **Fremdarbeit berechnen**.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet die Verkaufszahlen der Vorjahre, um einen Anteil von 1596,50 MW mit 100 Prozent für die COMPUTERAUSSTATTUNG-Pakete zu berechnen. Das bedeutet, dass alle Artikel, die letztes Jahr verkauft wurden, dem Kostenträger COMPUTERAUSSTATTUNG zugeordnet werden.  

## <a name="see-also"></a>Siehe auch  
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)  
[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)   
[Informationen zur Kostenrechnung](finance-about-cost-accounting.md)
