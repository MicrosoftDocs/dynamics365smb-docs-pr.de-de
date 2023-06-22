---
title: Den Verbrauch über Stapelverarbeitung buchen
description: 'Wenn die Spülmethode Manuell ist, müssen Sie die Komponenten manuell buchen, indem Sie ein Verbrauchsjournal verwenden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="batch-post-production-consumption" />Produktionsverbrauch mit Stapelverarbeitung buchen

Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.  

> [!NOTE]
> Wenn Sie auf der Lagerortkarte im Feld **Kommissionierung erforderlich** ein Häkchen gesetzt haben, um anzugeben, dass für den Lagerort die Bearbeitung der Kommissionierung erforderlich ist, müssen Sie diese Stapelvearbeitung nicht ausführen. [!INCLUDE[prod_short](includes/prod_short.md)] übernimmt den Verbrauch, wenn Sie die Lagerkommissionierung buchen. Weitere Informationen finden Sie unter [Herausnehmen für die Produktion in grundlegenden Lagerort-Konfigurationen](warehouse-how-to-pick-for-production.md).  

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines" />Die Laufzeit für eine oder mehrere Verbrauchszeile buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verbrauchs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Verwenden Sie die Aktion **Verbrauch berechnen**, um Buch.-Blattzeilen von Fertigungsaufträgen basierend auf der Berechnung der Verbrauchsmenge auf der Ist-Menge (der Menge der fertig gestellten Artikel, die Sie ausgewertet haben) oder der Soll-Menge (der Menge von Artikeln, die Sie fertigen möchten) basiert.

    > [!NOTE]
    > Wenn Sie die Standortkarte so konfiguriert haben, dass eine Lagerentnahme erforderlich ist, können nur Mengen eingegeben werden, die bereits über eine Lageraktivität im Feld **Menge** auf der Seite **Verbrauchsjournal** kommissioniert wurden, keine berechnete Menge. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

3. Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus. Die damit verbundenen Bestände werden reduziert.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also" />Siehe auch

[Produktion](production-manage-manufacturing.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
