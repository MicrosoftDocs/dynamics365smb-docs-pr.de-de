---
title: Wie Sie Zusteller festlegen
description: 'Erfahren Sie, wie Sie einen Code für jeden Ihrer Zusteller festlegen und beschreibende Informationen über jeden von ihnen und die von ihnen angebotenen Dienste eingeben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Zusteller einrichten
Sie können einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.  

Wenn Sie eine Internetadresse des Zustellers eingeben und der Zusteller die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen. Weitere Informationen finden Sie unter [Pakete nachverfolgen](sales-how-track-packages.md)

Wenn Sie Zusteller in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Zusteller anbietet.  
Für jeden Zusteller können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.  

Wenn Sie einer Verkaufsauftragszeile eine Zusteller Transportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt. Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).

## So richten Sie einen Zusteller ein  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Versand-Zusteller** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Wählen Sie die Aktion **Zustellertransportarten**.
4. In **Zustellertransportarten** füllen Sie die Felder wie notwendig aus.

> [!NOTE]  
>  Wenn Sie den Zusteller in der Auftragszeile löschen, wird auch der Zusteller Transportartcode gelöscht. Der Inhalt der Felder, die zum Teil auf der Zustellertransportart basierten, wird neu berechnet.  

## Siehe auch
[Lieferbedingungen einrichten](sales-how-set-up-shipment-methods.md)  
[Um Pakete zu verfolgen](sales-how-track-packages.md)    
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]