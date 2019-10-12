---
title: Definieren von Kostenstellen und Kostenträgern für Kontenpläne | Microsoft Docs
description: Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt das System nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 1a9178f80f6c16659509f1ae22b9225b1b6d2f70
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302428"
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
>  Um sicherzustellen, dass die vordefinierte Kostenstelle und der vordefinierte Kostenträger, die bzw. den Sie im Sachkonto eingerichtet haben, automatisch in die Kostenrechnung übertragen werden, aktivieren Sie das Kontrollkästchen **Fibu-Buchung prüfen** auf der Seite Kosenbuchungseinrichtung.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
