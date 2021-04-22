---
title: Umlagern von Artikeln | Microsoft Docs
description: Im Lagerbestand müssen Artikel möglicherweise zwischen Lagerplätzen umgelagert werden, um die täglichen Lageraktivitäten zu unterstützen, die für einen optimalen Lagerdurchlauf der Artikel verantwortlich sind. Einige Lagerplatzumlagerungen geschehen in der direkten Verknüpfung mit internen Vorgängen, wie einem Fertigungsauftrag, der die Lieferung von Komponenten benötigt, oder Endartikel, die eingelagert müssen. Andere Umlagerungen geschehen aus Gründen der Lagerplatzoptimierung oder als Ad-hoc-Lagerplatzumlagerungen zu und von Arbeitsgängen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66c2b9d191bc899de6ec2b6e6bbcd99d133448b7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784117"
---
# <a name="moving-items"></a>Umlagern von Artikeln
Die Lageraktivität des Umlagerns von Artikeln innerhalb des Lagers erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

An einem Lagerort müssen Artikel möglicherweise zwischen Lagerplätzen umgelagert werden, um die täglichen Lageraktivitäten zu unterstützen, die für einen optimalen Lagerdurchlauf der Artikel verantwortlich sind. Einige Lagerplatzumlagerungen geschehen in der direkten Verknüpfung mit internen Vorgängen, wie einem Fertigungsauftrag, der die Lieferung von Komponenten benötigt, oder Endartikel, die eingelagert müssen. Andere Umlagerungen geschehen aus Gründen der Lagerplatzoptimierung oder als Ad-hoc-Lagerplatzumlagerungen zu und von Arbeitsgängen.

Zusätzliche Umlagerungsaufgaben dienen der regelmäßigen Auffüllung von Kommissionierungslagerplätzen oder Fertigungsbereitstellungslagerplätzen und der Bearbeitung von Lagerplatzinhaltsinformationen.

Das Umlagern von Artikeln an andere Lagerorte wirkt sich auf die Artikelposten aus und muss daher anhand eines Umlagerungsauftrags erfolgen. Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).  

Die lagerbezogenen Aufgaben der Zählung, Anpassung und Umbuchung von Artikeln beinhaltet möglicherweise Lageraufgaben, die für Lagerplatzposten ausgeführt werden müssen, bevor sie mit den zugehörigen Artikelposten synchronisiert werden können. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md)  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Lagern Sie Artikel in den Basislagerkonfigurationen jederzeit und ohne Herkunftsbelege zwischen Lagerplätzen um.|[Umlagern von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Verwenden Sie den Lagerplatzumlagerungsarbeitsblatt, um Artikel für Herkunftsbelege und Ad-hoc in erweiterte Lagerkonfigurationen zu verschieben.|[Umlagerung von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Bringen Sie in den Basislagerkonfigurationen Komponenten zu den internen Vorgängen, wie von Herkunftsbelegen für diese Arbeitsgänge angefordert.|[So verschieben Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planen Sie, welche Lagerplätze gefüllt oder geleert werden sollen, um einen effizienten Ablauf zu gewährleisten, wie z. B. das Leeren eines Palettenlagerplatzes vor einem großen Wareneingang.|[Planen von Umlagerungen in Arbeitsblättern](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Aktualisieren Sie aufgrund von Nachfrageschwankungen die Häufigkeit, mit der Lagerplätze, z. B. Kommissionierungslagerplätze, aufgefüllt werden müssen.|[Lagerplatzauffüllung berechnen](warehouse-how-to-calculate-bin-replenishment.md)|
|Strukturieren Sie Ihr Lager mit neuen Lagerplatzcodes und neuen Lagerplatzeigenschaften neu und lagern Sie sie ggf. um.|[Lager umstrukturieren](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]