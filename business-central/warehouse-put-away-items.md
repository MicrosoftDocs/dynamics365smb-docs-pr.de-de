---
title: Einlagerung von Artikeln | Microsoft Docs
description: Die Lageraktivität des Einlagerns von Artikeln nach ihrem Eingang oder ihrer Herstellung erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d19486956fbaa0addb58a71c13849b0bb32c958a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771574"
---
# <a name="putting-items-away"></a>Einlagerung von Artikeln
Die Lageraktivität des Einlagerns von Artikeln nach ihrem Eingang oder ihrer Herstellung erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Wenn Sie sich entscheiden, Ihre Einlagerungsaktivitäten mit Logistikbelegen zu organisieren und zu erfassen, setzen Sie ein Häkchen in das Feld **Einlagerung erforderlich** auf der Lagerortkarte. Dies zeigt an, dass Sie – wenn Sie Artikel haben, die Ihr Lager über einen eingehenden Herkunftsbeleg erreichen – möchten, dass die Einlagerung dieser Artikel durch die Anwendung gesteuert werden soll. Ein eingehender Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht.  

Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung erforderlich ist, jedoch nicht die Bearbeitung des Wareneingangs, verwenden Sie die Seite **Lagereinlagerung**, um die Einlagerungsinformationen zu strukturieren, zu drucken, die Ergebnisse der tatsächlichen Einlagerung einzugeben und die Einlagerungsinformationen zu buchen, wodurch gleichzeitig die Wareneingangsinformationen im Herkunftsbeleg gebucht werden. Im Falle eines Fertigungsauftrags bucht der Buchungsvorgang die Istmeldung des Auftrags und beendet den Fertigungsauftrag.

Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist, Sie also Häkchen in die Felder **Wareneingang erforderlich** und **Einlagerung erforderlich** auf der Lagerortkarte gesetzt haben, weicht der Vorgang zum Einlagern von Artikeln ab. In diesem Falle verwenden Sie die Seite **Einlagerung**, um das Einlagern von Artikeln abzuwickeln. Die Lagereinlagerungsfunktionen sind den Bestandseinlagerungsfunktionen ähnlich. Anstelle der Informationsbuchung wird die Einlagerung erfasst. Beachten Sie, dass bei der Registrierung der Einlagerung nicht der Eingang der Artikel gebucht wird. Es wird nur der Lagerplatzinhalt aktualisiert. Als Lagerbestandsmanager können Sie Einlagerungsarbeitsblätter verwenden, um Einlagerungsinformationen zu organisieren, bevor Sie die individuellen Einlagerungsanweisungen erstellen.

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..   

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
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]