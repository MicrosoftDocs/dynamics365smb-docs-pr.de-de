---
title: 'Designdetails: Kostenkomponenten | Microsoft Docs'
description: Kostenkomponenten sind unterschiedliche Arten von Kosten, die den Wert eines Lagerzugangs erhöhen oder vermindern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c44ca651417bb9f2b66c009bf3cd51f4f3dc5ca8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783872"
---
# <a name="design-details-cost-components"></a>Designdetails: Kostenkomponenten
Kostenkomponenten sind unterschiedliche Arten von Kosten, die den Wert eines Lagerzugangs erhöhen oder vermindern.  

 Die folgende Tabelle zeigt die verschiedenen Kostenkomponenten und alle untergeordneten Kostenkomponenten an, aus denen sie bestehen.  

|Kostenkomponenten|Unterstellte Kostenkomponente|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Direkte Kosten|Einstandspreis (Preis des direkten Kaufs)|Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.|  
|Direkte Kosten|Fracht Kosten (Artikelgebühren)|Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.|  
|Direkte Kosten|Versicherungskosten (Artikelgebühren)|Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.|  
|Indirekte Kosten||Kosten, die nicht auf ein Kostenobjekt zurückzuführen sind.|  
|Abweichung|Einkaufsabweichung|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Abweichung|Materialabweichung|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Abweichung|Kapazitätsabweichung|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Abweichung|Fremdarbeitskostenabweichung|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Abweichung|Abweichung Kapazitätsgemeinkosten|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Abweichung|Prod.-Gemeinkostenabw.|Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.|  
|Neubewertung||Eine Auf- oder Abwertung des aktuellen Lagerwerts.|  
|Rundung||Restbeträge, die durch die Berechnung von Bestandsminderungen entstehen.|  

> [!NOTE]  
>  Fracht- und Versicherungskosten sind Artikel-Gebühren, die jederzeit zu den Kosten des Artikels addiert werden können. Wenn Sie die Stapelverarbeitung **Artikeleintrag Kosten anpassen** ausführen, wird der Wert aller zugehörigen Lagerabgänge entsprechend aktualisiert.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Abweichungen](design-details-variance.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]