---
title: 'Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand | Microsoft Docs'
description: Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: a49ad6e5c11820e5c0a68bd1d0749473bd3793a5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303532"
---
# <a name="design-details-handling-projected-negative-inventory"></a>Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand
Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.  

 Deshalb betrachtet das Planungssystem es als einen Notfall, wenn ein zukünftiger Bedarf nicht aus dem voraussichtlichen Lagerbestand abgedeckt werden kann, oder anders ausgedrückt: wenn der voraussichtliche Lagerbestand negativ wird. Die Anwendung behandelt eine solche Ausnahme, indem es einen neuen Beschaffungsauftrag vorschlägt, um den Teil des Bedarf einzuhalten, der nicht durch Lagerbestand oder anderen Vorrat befriedigt werden kann. Die Auftragsgröße des neuen Beschaffungsauftrags berücksichtigt nicht den Höchstbestand oder die Wiederbeschaffungsmenge, und auch nicht die Auftragsmodifikatoren maximale Auftragsmenge, minimale Auftragsmenge und Auftragsvielfaches. Stattdessen spiegelt sie den genauen Mangel wider.  

 Die Planungszeile für diese Art von Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt, um den Benutzer über die Situation zu informieren..  

 In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.  

 ![Notfallplanungsvorschlag, verhindern von negativem Lagerbestand](media/nav_app_supply_planning_2_negative_inventory.png "Notfallplanungsvorschlag, verhindern von negativem Lagerbestand")  

1.  Vorrat **A** anfänglicher voraussichtlicher Lagerbestand, liegt unter Minimalbestand.  
2.  Ein neuer voraus geplanter Vorrat wurde erstellt (**C**).  

     (Menge = Maximalbestand - Voraussichtlicher Lagerbestand)  
3.  Vorrat **A** wird durch Bedarf **B** geschlossen, der nicht vollständig abgedeckt wird.  

     (Bedarf **B** könnte versuchen, Zubehör C einzuplanen, dies erfolgt jedoch nicht aufgrund des Zeitrahmenkonzepts.)  
4.  Neuer Vorrat (**D**) wird erstellt, um die Restmenge auf Anfordung **B** zu decken.  
5.  Bedarf **B** ist geschlossen (eine Erinnerung für den voraussichtlichen Lagerbestand wird erstellt).  
6.  Das neue Vorrat **D** wird geschlossen.  
7.  Voraussichtlicher Lagerbestand wird geprüft; Minimalbestand wurde nicht überschritten.  
8.  Vorrat **C** ist geschlossen (kein Bedarf mehr vorhanden).  
9. Abschließende Prüfung: Keine ausstehenden Erinnerungen auf Bestandsebene sind vorhanden.  

> [!NOTE]  
>  Schritt 4 zeigt, wie das System in Versionen vor Microsoft Dynamics NAV 2009 SP1 reagiert.  

 Damit ist die Beschreibung der zentralen Prinzipien in Bezug auf Bestandsplanung basierend auf Wiederbeschaffungsverfahren abgeschlossen. Im nächsten Abschnitt werden die Eigenschaften der vier unterstützten Wiederbeschaffungsrichtlinien beschrieben.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
 [Designdetails: Planungsparameter](design-details-planning-parameters.md)   
 [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)
