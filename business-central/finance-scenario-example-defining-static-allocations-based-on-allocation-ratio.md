---
title: "Definieren von statischen Verteilungen basierend auf dem Verteilungsverhältnis | Microsoft Docs"
description: "Die statische Verteilungsmethode basiert auf einem definierten Wert, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4."
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
ms.openlocfilehash: 036aa1f317c1b1de7fc1548e03d40eca8c25be89
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Szenario-Beispiel: Definieren von statischen Verteilungen basierend auf dem Verteilungsverhältnis
Die statische Verteilungsmethode basiert auf einem definierten Wert, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.  

In diesem Thema wird beschrieben, wie drei neue Verteilungsziel-Kostenträger für die Kostenstelle der Verteilungsquelle PROD mithilfe des eingerichteten Verteilungsverhältnisses 5:2:4 definiert wird. Die drei Zielkostenträger sind ZUBEHÖR, FARBE und EINRICHTUNG.  

> [!NOTE]  
>  Das Beispiel verwendet die Demodaten in [!INCLUDE[d365fin](includes/d365fin_md.md)]  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>So definieren die die Kostenstelle der Verteilungsquelle PROD auf dem Inforegister "Allgemein"  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenzuteilung** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Kostenzuteilung** die Aktion **Neu** aus.  
3.  Drücken Sie im Feld **ID** die EINGABETASTE, oder geben Sie eine ID ein.  
4.  Geben Sie in dem Feld **Menge** **1** ein.  
5.  In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.  
6.  Geben Sie im Feld **Kostenstellencode** **PROD** ein.  
7.  Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>So definieren Sie die Verteilungsziel-Kostenträger auf dem Inforegister "Zeilen"  

1.  Wählen Sie in der ersten Rechnungszeile in dem Feld **Zielkostenart** **9903** ein.  
2.  Wählen Sie in der ersten Rechnungszeile in dem Feld **Zielkosteobjekt** **ACCESSO**.  
3.  Wählen Sie in der ersten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
4.  Wählen Sie in der ersten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
5.  Geben Sie in der ersten Zeile im Feld **Aktie** das Verteilungsverhältnis **5**ein.  
6.  Wählen Sie in der zweiten Rechnungszeile in dem Feld **Zielkostenart** **9903**.  
7.  Wählen Sie in der zweiten Rechnungszeile in dem Feld **Zielkosteobjekt** **PAINT.**  
8.  Wählen Sie in der zweiten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
9. Wählen Sie in der zweiten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
10. Geben Sie in der zweiten Zeile im Feld **Aktie** das Verteilungsverhältnis **2**ein.  
11. Wählen Sie in der dritten Rechnungszeile in dem Feld **Zielkostenart** **9903** ein.  
12. Wählen Sie in der dritten Rechnungszeile in dem Feld **Zielkosteobjekt** **ACCESSO**.  
13. Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
14. Wählen Sie in der dritten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
15. Geben Sie in der dritten Zeile im Feld **Aktie** das Verteilungsverhältnis **4**ein.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet automatisch das Feld  unter Verwendung eines **Prozentsatzes**, der von allen drei Zuteilungsverhältnissen abhängt, die im Feld **Aktie** für alle drei Zeilen eingegeben werden.  

## <a name="see-also"></a>Siehe auch  
[Richten Sie die Zuteilungsquelle und Ziele ein](finance-how-to-set-up-allocation-source-and-targets.md)   
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)   
[Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)

