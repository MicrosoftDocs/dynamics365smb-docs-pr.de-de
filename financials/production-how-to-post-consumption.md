---
title: 'Vorgehensweise: Verbrauch mit Stapelverarbeitung buchen | Microsoft Docs'
description: "Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a>So wird's gemacht: Produktionsverbrauch mit Stapelverarbeitung buchen
Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.

Sie können das System so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Die Laufzeit für eine oder mehrere Verbrauchszeile buchen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Verbrauchs-Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Wenn der Lagerort, an dem sich die Komponenten befinden, so eingerichtet ist, dass Lagerplätze verwendet werden, die Bearbeitung der Kommissionierung jedoch nicht erforderlich ist, dann geben Sie in der Buch.-Blattzeile einen Lagerplatz ein, um festzulegen, von welchem Lagerplatz die Artikel aus dem Lager entnommen werden sollen. Weitere Informationen finden Sie unter [Vorgehensweise: Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md).  
3.  Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus. Die verknüpften Artikelposten werden verringert.

## <a name="see-also"></a>Siehe auch  
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

