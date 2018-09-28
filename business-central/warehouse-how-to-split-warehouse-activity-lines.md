---
title: "Vorgehensweise: Aufteilen von Lageraktivitätszeilen | Microsoft Docs"
description: "In Einlagerungen, Lagerplatzumlagerungen oder Kommissionierungen und in Lagereinlagerungen und Lagerkommissionierungen werden Lagerplätze für das Kommissionieren oder Einlagern von Artikeln vorgeschlagen. Die tatsächliche Menge im Lagerplatz, die von der Anwendung vorgeschlagen wird, ist möglicherweise nicht ausreichend, oder in dem vorgeschlagenen Lagerplatz ist nicht genügend Platz, um die erforderliche Menge einzulagern. In diesen Fällen müssen Sie die Zeile aufteilen, so dass die Artikel für eine Zeile entweder aus mehr als einem Lagerplatz entnommen oder in mehr als einen Lagerplatz eingelagert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dfb633ef874b77a3cf6060311f0bcbbf66e05102
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="split-warehouse-activity-lines"></a>Lageraktivitätszeilen aufzuteilen
In Einlagerungen, Lagerplatzumlagerungen oder Kommissionierungen und in Lagereinlagerungen und Lagerkommissionierungen werden Lagerplätze für das Kommissionieren oder Einlagern von Artikeln vorgeschlagen. Die tatsächliche Menge im Lagerplatz, die von der Anwendung vorgeschlagen wird, ist möglicherweise nicht ausreichend, oder in dem vorgeschlagenen Lagerplatz ist nicht genügend Platz, um die erforderliche Menge einzulagern. In diesen Fällen müssen Sie die Zeile aufteilen, so dass die Artikel für eine Zeile entweder aus mehr als einem Lagerplatz entnommen oder in mehr als einen Lagerplatz eingelagert werden.  

Die folgende Vorgehensweise gilt für Logistikbelege, z. B. Einlagerungs-, Umlagerungs- und Kommissionierzeilen, oder Lagereinlagerungs-, Umlagerungs- und Kommissionierzeilen.  

## <a name="to-split-warehouse-activity-lines"></a>Um Lageraktivitätszeilen aufzuteilen  
1.  Öffnen Sie eine Lageraktivitätszeile, in der Sie versuchen, eine nicht ausreichende Menge zu bearbeiten.  
2.  Geben Sie im Feld **Bewegungsmenge** die reduzierte Menge ein, die Sie bearbeiten können.  
3.  Wählen Sie im Inforegister **Zeilen** die Aktion **Aktionen**, dann die Aktion **Funktionen** und die Aktion **Zeile aufteilen** aus. Eine neue Zeile wird angezeigt, bei der es sich um eine Kopie der Originalzeile handelt. Einziger Unterschied: Das Feld **Bewegungsmenge** enthält die Menge, die aus der ursprünglichen Zeile entfernt wurde.  
4.  Ordnen Sie dieser neuen Zeile einen geeigneten Lagerplatz zu, und eine Zone, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, oder setzen Sie das Aufteilen der Zeile so lange fort, wie es erforderlich ist, um geeignete Lagerplätze für die gesamte Menge zu finden.  

> [!NOTE]  
>  Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und Sie die Zeilen aufteilen, müssen Sie sich mit dem Lager auskennen und in der Lage sein, einen Lagerplatz auszuwählen, der den Lageranforderungen des Artikels und den allgemeinen Anforderungen des Logistikbelegs entspricht. Sie würden z. B. nicht eine Zeile eines Kommissionierbelegs aufteilen und einige der Artikel in den Palettenlagerplätzen einlagern.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

