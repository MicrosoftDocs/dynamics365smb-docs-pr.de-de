---
title: 'Vorgehensweise: Versandagenten | Microsoft Docs'
description: Sie können einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 27b362c9c9aabec842e28e631ca2b93c1515f2fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311980"
---
# <a name="set-up-shipping-agents"></a>Zusteller einrichten
Sie können einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.  

Wenn Sie eine Internetadresse des Zustellers eingeben und der Zusteller die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen. Weitere Informationen finden Sie unter [Pakete nachverfolgen](sales-how-track-packages.md)

Wenn Sie Zusteller in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Zusteller anbietet.  
Für jeden Zusteller können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.  

Wenn Sie einer Verkaufsauftragszeile eine Zusteller Transportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt. Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>So richten Sie einen Zusteller ein  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandagent** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Wählen Sie die Aktion **Zustellertransportarten**.
4. In **Zustellertransportarten** füllen Sie die Felder wie notwendig aus.

> [!NOTE]  
>  Wenn Sie den Zusteller in der Auftragszeile löschen, wird auch der Zusteller Transportartcode gelöscht. Der Inhalt der Felder, die zum Teil auf der Zustellertransportart basierten, wird neu berechnet.  

## <a name="see-also"></a>Siehe auch
[Liefermethoden einrichten](sales-how-set-up-shipment-methods.md)  
[Um Pakete zu verfolgen](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
