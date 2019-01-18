---
title: Entnahme von Artikeln | Microsoft Docs
description: "Die Lageraktivität des Kommissionierens von Artikeln vor ihrer Lieferung oder ihrem Verbrauch erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität der [Einrichtung](../configure-warehouse-processes.md) reicht von keinen Lagerfunktionen über grundlegende Lagerfunktionen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 6a51a509ae1281d7c6bfe19e5276b516982a5fa5
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---
# <a name="pick-items"></a>Entnahme von Artikeln
Die Lageraktivität des Kommissionierens von Artikeln vor ihrer Lieferung oder ihrem Verbrauch erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Wenn Sie sich entscheiden, Ihre Kommissionieraktivitäten mit Lagerbelegen zu organisieren und zu erfassen, setzen Sie ein Häkchen in das Feld **Kommissionierung erforderlich** auf der Lagerortkarte. Dies zeigt an, dass Sie – wenn Sie Artikel haben, die für einen ausgehenden Herkunftsbeleg kommissioniert werden müssen – möchten, dass die Kommissionierung dieser Artikel durch die Anwendung gesteuert werden soll. Ein ausgehender Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, Serviceauftrag oder ein Fertigungsauftrag sein, dessen Komponenten kommissioniert werden sollen.

> [!NOTE]
> Obwohl die Einstellung **Kommissionierung erforderlich** genannt wird, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie dieses Kontrollkästchen aktivieren, buchen.

Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Kommissionierung erforderlich ist, jedoch nicht die Bearbeitung des Warenausgangs, verwenden Sie die Seite **Lagerkommissionierung**, um die Kommissionierungsinformationen zu strukturieren, zu drucken, die Ergebnisse der tatsächlichen Kommissionierung einzugeben und die Kommissionierungsinformationen zu buchen, wodurch gleichzeitig die Lieferung der Artikel gebucht werden. Im Falle der Kommissionierung von Komponenten für einen Fertigungsauftrag wird beim Buchen der Kommissionierung auch der Verbrauch gebucht.

Wenn Ihr Lagerort so eingerichtet ist, dass die Bearbeitung der Kommissionierung und des Warenausgangs erforderlich ist, Sie also Häkchen im Feld **Kommissionierung erforderlich** und **Warenausgang erforderlich** auf der Lagerortkarte gesetzt haben, verwenden Sie die Seite **Kommissionierung** für die Abwicklung der Kommissionierung. Die Kommissionierfunktionen sind ähnlich wie die Lagerkommissionierung, außer dass Sie anstatt die Kommissionierinformationen zu buchen, die Kommissionierung registrieren. Dieser Registrierungsprozess bucht nicht den Warenausgang, sondern stellt lediglich die Artikel für den Warenausgang zur Verfügung. Als Lagerbestandsmanager können Sie Kommissionierungsvorschläge verwenden, um Kommissionierungsinformationen zu organisieren, bevor Sie die individuellen Kommissionierungsanweisungen erstellen.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|
|------------|-------------|  
|Buchen Sie die Lieferung von Artikeln direkt im Beleg des ausgehenden Auftrags, da keine Lagerfunktionen vorhanden sind. (Funktioniert analog für Verkaufsaufträge, ausgehende Umlagerungsaufträge und Rücklieferungen.)|[Versenden von Artikeln](warehouse-how-ship-items.md)|  
|Kommissionieren Sie Artikel auftragsweise, und buchen Sie bei einer Basis-Lagerkonfiguration die Lieferung in derselben Aktivität.|[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Kommissionieren Sie Artikel für mehrere Aufträge in einer erweiterten Lagerkonfiguration.|[Artikel mit Kommissionierungen kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Kommissionieren Sie Komponenten für Produktion oder Montage in einer grundlegenden oder erweiterten Lagerkonfiguration.|[Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md)|  
|Planen Sie optimierte Kommissionierungsanweisungen für eine Reihe von Lieferungen, bevor Sie die Lagermitarbeiter die gebuchten Lieferungen direkt bearbeiten lassen.|[Kommissionierungen im Vorschlag bearbeiten](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Kommissionieren Sie Artikel für einen bestimmten Zweck, z. B. eine Produktion benötigt zusätzliche Komponenten. Dies geschieht technisch gesehen so, dass die Artikel das Lager nicht verlassen.|[Wählen und setzen Sie die Einlagerung verwendet ohne Herkunftsbeleg](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Die automatische Kommissionierung von Artikeln entsprechend ihres Ablaufdatums, beispielsweise begrenzt haltbare Lebensmittel, verstehen.|[Kommissionierung nach FEFO](warehouse-picking-by-fefo.md)|
|Teilen Sie eine Kommissionierungszeile in mehrere Zeilen auf, z. B., da es nicht genügend Artikel verfügbare sind, um sie aus dem festgelegten Lagerplatz zu entnehmen.|[Lageraktivitätszeilen aufzuteilen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Sie erhalten sofortigen Zugriff auf Kommissionierungen, die Ihnen als Lagermitarbeiter zugewiesen sind.|[Suchen der Lagerzuweisungen](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

