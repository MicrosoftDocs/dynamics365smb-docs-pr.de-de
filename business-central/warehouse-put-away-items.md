---
title: Einlagerung von Artikeln | Microsoft Docs
description: "Die Lageraktivität des Einlagerns von Artikeln nach ihrem Eingang oder ihrer Herstellung erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten."
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
ms.openlocfilehash: 5e732e27921f632c3e15b1d832d7295d32f4b8a2
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="putting-items-away"></a>Einlagerung von Artikeln
Die Lageraktivität des Einlagerns von Artikeln nach ihrem Eingang oder ihrer Herstellung erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Wenn Sie sich entscheiden, Ihre Einlagerungsaktivitäten mit Logistikbelegen zu organisieren und zu erfassen, setzen Sie ein Häkchen in das Feld **Einlagerung erforderlich** auf der Lagerortkarte. Dies zeigt an, dass Sie – wenn Sie Artikel haben, die Ihr Lager über einen eingehenden Herkunftsbeleg erreichen – möchten, dass die Einlagerung dieser Artikel durch die Anwendung gesteuert werden soll. Ein eingehender Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht.  

Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung erforderlich ist, jedoch nicht die Bearbeitung des Wareneingangs, verwenden Sie das Fenster **Lagereinlagerung**, um die Einlagerungsinformationen zu strukturieren, zu drucken, die Ergebnisse der tatsächlichen Einlagerung einzugeben und die Einlagerungsinformationen zu buchen, wodurch gleichzeitig die Wareneingangsinformationen im Herkunftsbeleg gebucht werden. Im Falle eines Fertigungsauftrags bucht der Buchungsvorgang die Istmeldung des Auftrags und beendet den Fertigungsauftrag.

Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist, Sie also Häkchen in die Felder **Wareneingang erforderlich** und **Einlagerung erforderlich** auf der Lagerortkarte gesetzt haben, weicht der Vorgang zum Einlagern von Artikeln ab. In diesem Falle verwenden Sie die **Einlagerung**, um das Einlagern von Artikeln abzuwickeln. Die Lagereinlagerungsfunktionen sind den Bestandseinlagerungsfunktionen ähnlich. Anstelle der Informationsbuchung wird die Einlagerung erfasst. Beachten Sie, dass bei der Registrierung der Einlagerung nicht der Eingang der Artikel gebucht wird. Es wird nur der Lagerplatzinhalt aktualisiert. Als Lagerbestandsmanager können Sie Einlagerungsvorschläge verwenden, um Einlagerungsinformationen zu organisieren, bevor Sie die individuellen Einlagerungsanweisungen erstellen.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Buchen Sie den Eingang von Artikeln direkt im Beleg des eingehenden Auftrags und Erfassen Sie dadurch die Einlagerung, da keine Lagerkonfiguration vorhanden ist.|[Empfangen von Artikeln](warehouse-how-receive-items.md)|  
|Lagern Sie Artikel auftragsweise ein, und buchen Sie bei einer Basis-Lagerkonfiguration den Eingang in derselben Aktivität.|[Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Lagern Sie Artikel für mehrere Aufträge in einer erweiterten Lagerkonfiguration ein.|[Einlagern von Artikeln mit Lagereinlagerungen](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Lagern Sie produzierte oder montierte Artikel in einer grundlegenden oder erweiterten Lagerkonfiguration ein.|[Einlagerung der fertiggestellten Produktion oder Montage](warehouse-how-to-put-away-production-output.md)|
|Planen Sie optimierte Einlagerungsanweisungen für eine Reihe gebuchter Lagereingänge, bevor Sie die Lagermitarbeiter die Wareneingänge direkt bearbeiten lassen.|[Planen von Einlagerungen in Arbeitsblättern](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Stellen Sie Artikel zurück, die im Prinzip intern kommissioniert wurden, z. B. für einen Produktionsauftrag, bei dem nicht die erwartete Menge verbraucht wurde.|[Wählen und setzen Sie die Einlagerung verwendet ohne Herkunftsbeleg](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Teilen Sie eine Einlagerungszeile auf, um einen Teil der Einlagerungsmenge an freien Lagerplätzen einzulagern, da der vorgesehene Lagerplatz aufgefüllt wird.|[Lageraktivitätszeilen aufzuteilen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Sie erhalten sofortigen Zugriff auf Einlagerungen, die Ihnen als Lagermitarbeiter zugewiesen sind.|[Suchen der Lagerzuweisungen](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

