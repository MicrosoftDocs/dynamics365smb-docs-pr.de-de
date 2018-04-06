---
title: "Definieren von Kostenstellen und Kostenträgern für Kontenpläne | Microsoft Docs"
description: "Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt das System nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5da3967e99bf8a1d5628159a542885ffd1113a02
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definieren von Kostenstellen und Kostenträgern für Kontenpläne
Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt [!INCLUDE[d365fin](includes/d365fin_md.md)] nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definieren von Standarddimensionswerten für Sachkonten  
Für jedes Sachkonto können Sie Standarddimensionswerte in der Tabelle **Standard-Dimensionen** definieren. Das folgende Beispiel zeigt, wie Sie definieren, dass es immer eine Kostenstelle ABTEILUNG, aber nie einen Kostenträger PROJEKT geben soll, wenn Sie auf ein Sachkonto buchen.  

|**Dimensionscode**|**Dimensionswertbuchung**|  
|------------------------------------------|-----------------------------------------|  
|Abteilung|Code notwendig|  
|Kostenträger|Kein Code|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definieren von Dimensionswerten für Gemeinkosten und direkte Kosten  
 Sie können Gemeinkosten an eine Kostenstelle und direkte Kosten an einen Kostenträger übertragen. In der folgenden Tabelle wird die optimale Kombination aus Dimensionseinrichtungswerten angezeigt.  

|Übertragen in|Kostenstellenbuchung|Kostenträgerbuchung|  
|-----------------|-------------------------|-------------------------|  
|Kostenstelle|Code notwendig|Kein Code|  
|Kostenträger|Kein Code|Code notwendig|  

> [!NOTE]  
>  Um sicherzustellen, dass die vordefinierte Kostenstelle und der vordefinierte Kostenträger, die bzw. den Sie im Sachkonto eingerichtet haben, automatisch in die Kostenrechnung übertragen werden, aktivieren Sie das Kontrollkästchen **Fibu-Buchung prüfen** im Fenster Kosenbuchungseinrichtung.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Kostenstellen einrichten](finance-how-to-set-up-cost-centers.md)   
[Einrichten von Kostenträgern](finance-how-to-set-up-cost-objects.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

