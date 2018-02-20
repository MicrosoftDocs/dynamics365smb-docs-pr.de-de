---
title: 'Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand | Microsoft Docs'
description: "Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a>Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand
Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.  

 Deshalb betrachtet das Planungssystem es als einen Notfall, wenn ein zukünftiger Bedarf nicht aus dem voraussichtlichen Lagerbestand abgedeckt werden kann, oder anders ausgedrückt: wenn der voraussichtliche Lagerbestand negativ wird. Die Anwendung behandelt eine solche Ausnahme, indem es einen neuen Beschaffungsauftrag vorschlägt, um den Teil des Bedarf einzuhalten, der nicht durch Lagerbestand oder anderen Vorrat befriedigt werden kann. Die Auftragsgröße des neuen Beschaffungsauftrags berücksichtigt nicht den Höchstbestand oder die Wiederbeschaffungsmenge, und auch nicht die Auftragsmodifikatoren maximale Auftragsmenge, minimale Auftragsmenge und Auftragsvielfaches. Stattdessen spiegelt sie den genauen Mangel wider.  

 Die Planungszeile für diese Art von Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt, um den Benutzer über die Situation zu informieren..  

 In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

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

