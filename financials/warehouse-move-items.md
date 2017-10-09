---
title: Umlagern von Artikeln | Microsoft Docs
description: "Im Lagerbestand müssen Artikel möglicherweise zwischen Lagerplätzen umgelagert werden, um die täglichen Lageraktivitäten zu unterstützen, die für einen optimalen Lagerdurchlauf der Artikel verantwortlich sind. Einige Lagerplatzumlagerungen geschehen in der direkten Verknüpfung mit internen Vorgängen, wie einem Fertigungsauftrag, der die Lieferung von Komponenten benötigt, oder Endartikel, die eingelagert müssen. Andere Umlagerungen geschehen aus Gründen der Lagerplatzoptimierung oder als Ad-hoc-Lagerplatzumlagerungen zu und von Arbeitsgängen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f52353ec74b10983b0acfd04169d6b146c70eb84
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="moving-items"></a>Umlagern von Artikeln
Die Lageraktivität des Umlagerns von Artikeln innerhalb des Lagers erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

An einem Lagerort müssen Artikel möglicherweise zwischen Lagerplätzen umgelagert werden, um die täglichen Lageraktivitäten zu unterstützen, die für einen optimalen Lagerdurchlauf der Artikel verantwortlich sind. Einige Lagerplatzumlagerungen geschehen in der direkten Verknüpfung mit internen Vorgängen, wie einem Fertigungsauftrag, der die Lieferung von Komponenten benötigt, oder Endartikel, die eingelagert müssen. Andere Umlagerungen geschehen aus Gründen der Lagerplatzoptimierung oder als Ad-hoc-Lagerplatzumlagerungen zu und von Arbeitsgängen.

Das Umlagern von Artikeln an andere Lagerorte wirkt sich auf die Artikelposten aus und muss daher anhand eines Umlagerungsauftrags erfolgen. Weitere Informationen finden Sie unter [So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).  

Zusätzliche Umlagerungsaufgaben dienen der regelmäßigen Auffüllung von Kommissionierungslagerplätzen oder Fertigungsbereitstellungslagerplätzen und der Bearbeitung von Lagerplatzinhaltsinformationen.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Lagern Sie Artikel in den Basislagerkonfigurationen jederzeit und ohne Herkunftsbelege zwischen Lagerplätzen um.|[Vorgehensweise: Umlagern von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Verwenden Sie den Lagerplatzumlagerungsvorschlag, um Artikel für Herkunftsbelege und Ad-hoc in erweiterte Lagerkonfigurationen zu verschieben.|[Vorgehensweise: Umlagern von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Bringen Sie in den Basislagerkonfigurationen Komponenten zu den internen Vorgängen, wie von Herkunftsbelegen für diese Arbeitsgänge angefordert.|[Vorgehensweise: Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planen Sie, welche Lagerplätze gefüllt oder geleert werden sollen, um einen effizienten Ablauf zu gewährleisten, wie z. B. das Leeren eines Palettenlagerplatzes vor einem großen Wareneingang.|[Vorgehensweise: Planen von Umlagerungen in Vorschlägen](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Aktualisieren Sie aufgrund von Nachfrageschwankungen die Häufigkeit, mit der Lagerplätze, z. B. Kommissionierungslagerplätze, aufgefüllt werden müssen.|[Vorgehensweise: Lagerplatzauffüllung berechnen](warehouse-how-to-calculate-bin-replenishment.md)|
|Strukturieren Sie Ihr Lager mit neuen Lagerplatzcodes und neuen Lagerplatzeigenschaften neu und lagern Sie sie ggf. um.|[Vorgehensweise: Umstrukturieren von Lagern](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

