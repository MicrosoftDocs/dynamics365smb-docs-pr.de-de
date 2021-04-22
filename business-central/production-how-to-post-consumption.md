---
title: Den Verbrauch über Stapelverarbeitung buchen
description: Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787902"
---
# <a name="batch-post-production-consumption"></a>Produktionsverbrauch mit Stapelverarbeitung buchen

Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.  

>[!NOTE]
> Wenn Sie auf der Lagerortkarte im Feld **Kommissionierung erforderlich** ein Häkchen gesetzt haben, um anzugeben, dass für den Lagerort die Bearbeitung der Kommissionierung erforderlich ist, müssen Sie diese Stapelvearbeitung nicht ausführen. [!INCLUDE[prod_short](includes/prod_short.md)] übernimmt den Verbrauch, wenn Sie die Lagerkommissionierung buchen. Weitere Informationen finden Sie unter [Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations). 

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Die Laufzeit für eine oder mehrere Verbrauchszeile buchen

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Verbrauchs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Verwenden Sie die Aktion **Verbrauch berechnen**, um Buch.-Blattzeilen von Fertigungsaufträgen basierend auf der Berechnung der Verbrauchsmenge auf der Ist-Menge (der Menge der fertig gestellten Artikel, die Sie ausgewertet haben) oder der Soll-Menge (der Menge von Artikeln, die Sie fertigen möchten) basiert.

    > [!NOTE]
    > Wenn Sie die Standortkarte so konfiguriert haben, dass eine Lagerentnahme erforderlich ist, können nur Mengen eingegeben werden, die bereits über eine Lageraktivität im Feld **Menge** auf der Seite **Verbrauchsjournal** kommissioniert wurden, keine berechnete Menge. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

3.  Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus. Die damit verbundenen Bestände werden reduziert.



## <a name="see-also"></a>Siehe auch

[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
