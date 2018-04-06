---
title: "Vorgehensweise: Buchen von Kapazitäten | Microsoft Docs"
description: "Im Kapazitäts Buch.-Blatt buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6114149372b786c20ee7edbe13022abe688ed9a2
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a>Kapazität buchen
Im Kapazitäts Buch.-Blatt buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.  

## <a name="to-post-capacities"></a>Kapazitäten buchen  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Kapazität Journal** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.  
3.  Geben Sie in das Feld **Art** die Art der Kapazität entweder **Arbeitsplatz** oder **Arbeitsplatzgruppe** ein, die Sie buchen möchten.  
4.  Geben Sie im Feld **Nr.** Geben Sie die Nummer des Arbeitsplatzes oder der Arbeitsplatzgruppe ein.  
5.  Geben Sie in den anderen Feldern die entsprechenden Daten, wie zum Beispiel **Startzeit**, **Endzeit**, **Menge** und **Ausschuss** ein.  
6.  Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-view-work-center-ledger-entries"></a>Um sich die Arbeitsplatzgruppeneinträge anzeigen zu lassen:  
In den Fenstern **Arbeitsplatzgruppenkarte** und **Arbeitsplatzkarte** können Sie gebuchte Kapazität aufgrund der Informationen zu beendeten Fertigungsaufträgen anzeigen.    
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Schichten** ein und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die relevante Karte **Arbeitsplatzgruppe** aus der Liste, und wählen Sie die **Kapazitätsposten** Aktion aus.  

Im Fenster **Kapazitätsposten** werden die gebuchten Posten der Arbeitsplatzgruppe in der Reihenfolge der Buchungen angezeigt.   

## <a name="see-also"></a>Siehe auch  
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

