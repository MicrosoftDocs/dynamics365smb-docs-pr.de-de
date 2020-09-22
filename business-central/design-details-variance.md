---
title: Designdetails - Abweichungen | Microsoft Docs
description: Abweichung wird als Differenz zwischen den Ist-Kosten und Einstandspreis (fest) definiert, wie in der folgenden Formel beschrieben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b86bc97ec6064ee1e4b8f56c444d03cdecc4cc4b
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787071"
---
# <a name="design-details-variance"></a>Designdetails: Abweichung
Abweichung wird als Differenz zwischen den Ist-Kosten und Einstandspreis (fest) definiert, wie in der folgenden Formel beschrieben.  

 tatsächliche Kosten – Standardkosten = Abweichung  

 Wenn sich die Ist-Kosten ändern, etwa, weil Sie an einem späteren Datum eine Artikeländerung buchen, wird die Abweichung entsprechend aktualisiert.  

> [!NOTE]  
>  Die Neubewertung hat keinen Einfluss auf die Abweichungsberechnung, da die Neubewertung nur den Bestandswert ändert.  

## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie die Abweichung für Einkaufsartikel berechnet wird. Die basiert auf dem folgenden Szenario:  

1.  Der Benutzer kauft einen Artikel zu MW 90,00 ein, aber der Standardpreis ist MW 100,00. Entsprechend ist die Einkaufsabweichung MW -10,00.  
2.  MW 10,00 wird dem Einkaufsabweichungskonto gutgeschrieben.  
3.  Der Benutzer erzeugt einen Artikel Zu-/Abschlag von MW 20,00. Entsprechend werden die Ist-Kosten auf MW 110,00 erhöht, und der Wert der Einkaufsabweichung wird MW 10,00.  
4.  MW 20,00 werden dem Einkaufsabweichungskonto belastet. Entsprechend wird die Nettoeinkaufsabweichung MW 10,00.  
5.  Der Benutzer bewertet den Artikel um von MW 100,00 auf MW 70,00. Dies hat keinen Einfluss auf die Abweichungsberechnung, nur auf den Bestandswert.  

 Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

 ![Einkaufsabweichungsberechnung](media/design_details_inventory_costing_11_purchase_variance.png "Einkaufsabweichungsberechnung")  

## <a name="determining-the-standard-cost"></a>Bestimmen der Standardkosten  
 Die Standardkosten werden verwendet, wenn die Abweichung und der zu nutzende Betrag berechnet werden. Da sich die Standardkosten aufgrund manueller Aktualisierungsberechnungen ändern können, benötigen Sie einen Zeitpunkt, an dem die Standardkosten für die Abweichungsberechnung fest sind. An diesem Punkt wird der Lagerzugang fakturiert. Für gefertigt oder montierte Artikel, ist der Zeitpunkt, an dem die Standardkosten bestimmt werden, der der Kostenanpassung.  

 Die nachstehende Tabelle zeigt, wie verschiedene Kostenanteile für produzierte und montierte Artikel berechnet werden, wenn Sie die Funktion zur Berechnung der Standardkosten verwenden.  

|Kostenanteil|Gekaufter Artikel|Erzeugter/Montierter Artikel|  
|----------------|--------------------|------------------------------|  
|**Einstandspreis (fest)**||Einstufige Materialkosten + Einstufige Kapazitätskosten + Einstufige Fremdarbeitskosten + Einstufige Kap.-Gemeinkosten + Einstufige Prod.-Gemeinkosten|  
|**Einstufige Materialkosten**|Einstandspreis|![Gleichung 1](media/design_details_inventory_costing_11_equation_1.png "Gleichung 1")|  
|**Einstufige Kapazitätskosten**|Nicht anwendbar|![Gleichung 2](media/design_details_inventory_costing_11_equation_2.png "Gleichung 2")|  
|**Einstufige Fremdarbeitskosten**|Nicht anwendbar|![Gleichung 3](media/design_details_inventory_costing_11_equation_3.png "Gleichung 3")|  
|**Einstufige Kap.-Gemeinkosten**|Nicht anwendbar|![Gleichung 4](media/design_details_inventory_costing_11_equation_4.png "Gleichung 4")|  
|**Einstufige Prod.-Gemeinkosten**|Nicht anwendbar|(Einstufige Materialkosten + Einstufige Kapazitätskosten + Einstufige Fremdarbeitskosten) * Indirekte Kosten %/100 + Gemeinkostensatz|  
|**Mehrstufige Materialkosten**|Einstandspreis|![Gleichung 5](media/design_details_inventory_costing_11_equation_5.png "Gleichung 5")|  
|**Mehrstufige Kapazitätskosten**|Nicht anwendbar|![Gleichung 6](media/design_details_inventory_costing_11_equation_6.png "Gleichung 6")|  
|**Mehrstufige Fremdarbeitskosten**|Nicht anwendbar|![Gleichung 7](media/design_details_inventory_costing_11_equation_7.png "Gleichung 7")|  
|**Mehrstufige Kapazitätsgemeinkosten**|Nicht anwendbar|![Gleichung 8](media/design_details_inventory_costing_11_equation_8.png "Gleichung 8")|  
|**Mehrstufige Prod.-Gemeinkosten**|Nicht anwendbar|![Gleichung 9](media/design_details_inventory_costing_11_equation_9.png "Gleichung 9")|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Kostenmethoden](design-details-costing-methods.md) [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
