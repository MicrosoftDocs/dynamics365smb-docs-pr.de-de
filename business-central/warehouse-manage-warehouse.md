---
title: Lager-Aktivitäten verwalten
description: Nach dem Wareneingang und vor dem Versand der Waren findet eine Reihe von internen Lageraktivitäten statt, um einen effektiven Flow durch das Lager zu gewährleisten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 95e0655f863ea5559cad92f7bc0d89fc47a1b1c4
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074328"
---
# <a name="warehouse-management"></a>Logistik

Nach dem Eingang und vor der Lieferung von Waren finden einige interne Lageraktivitäten statt, um einen effektiven Ablauf im Lager zu gewährleisten und um den Lagerbestand des Unternehmens zu organisieren und zu verwalten.

Zu den typischen Lageraktivitäten gehören das Einlagern von Artikeln, das Umlagern von Artikeln in Lagern oder zwischen Lagern und die Kommissionierung von Artikeln für die Montage, Produktion oder Lieferung. Die Montage von Artikeln für Verkäufe oder Lager gilt auch als Lageraktivität, doch diese werden an anderer Stelle behandelt. Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md).  

In großen Lagern können diese unterschiedlichen Aufgaben nach Abteilungen getrennt sein und die Integration kann durch einen gesteuerten Workflow verwaltet werden. In einfacheren Installationen ist der Auftragsfluss weniger formalisiert und die Lageraktivitäten werden mit sogenannten Lagerbestandseinlagerungen und -kommissionierungen durchgeführt. Weitere Informationen über grundlegende und erweiterte Lagerkonfigurationen finden Sie unter [Designdetails: Logistik Übersicht](design-details-warehouse-overview.md).

Bevor Sie Lageraktivitäten ausführen können, müssen Sie das System für die relevante Komplexität der Lagerverarbeitung einrichten. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Die lagerbezogenen Aufgaben der Zählung, Anpassung und Umbuchung von Artikeln beinhaltet möglicherweise Lageraufgaben, die für Lagerplatzposten ausgeführt werden müssen, bevor sie mit den zugehörigen Artikelposten synchronisiert werden können. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md).

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.   

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Erfassung des Eingangs (einschließlich des Übereingangs) von Artikeln an Lagerstandorten, entweder nur mit einer Bestellung, bei einfachen Standorteinrichtungen, oder mit einem Lagerschein, im Falle einer halb- oder vollautomatischen Lagerabwicklung am Standort.|[Empfangen von Artikeln](warehouse-how-receive-items.md)|
|Umgehen Sie die Einlagerungs- und Kommissionierungsvorgänge, um einen Artikel direkt vom Wareneingang oder der Fertigung zum Versenden zu beschleunigen.|[Zuordnungselemente](warehouse-how-to-cross-dock-items.md)|
|Lagern Sie Artikel ein, die bei Einkäufen, Verkaufsrücksendungen, Umlagerungen oder Fertigerzeugnissen eingehen, gemäß dem konfigurierten Lageraktivitätsvorgang ein.|[Einlagerung von Artikeln](warehouse-put-away-items.md)|
|Lagern Sie Artikel zwischen Lagerplätzen in dem Lager um.|[Umlagern von Artikeln](warehouse-move-items.md)|
|Kommissionieren Sie Artikel, die geliefert, umgelagert oder bei der Montage bzw. Produktion verbraucht werden, gemäß dem konfigurierten Lageraktivitätsvorgang.|[Kommissionieren von Artikeln](warehouse-pick-items.md)|
|Erfassen Sie die Lieferung von Artikeln aus Lagerorten, entweder mit nur einem Verkaufsauftrag, in einfachen Lagerorteinrichtungen oder mit einem Warenausgang, im Falle von halb- oder vollautomatisierter Lagerverarbeitung am Lagerort.|[Versenden von Artikeln](warehouse-how-ship-items.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]