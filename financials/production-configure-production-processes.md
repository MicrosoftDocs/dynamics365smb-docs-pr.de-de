---
title: Konfigurieren von Produktionsprozessen | Microsoft Docs
description: "Damit Material zu Fertigerzeugnissen verarbeitet werden kann, müssen im System Fertigungsressourcen wie Maschinisten und Maschinen eingerichtet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f2d95dbb6d0336286f0fb657028970ce8a04cfda
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-manufacturing"></a>Produktion einrichten
Damit Material zu Fertigerzeugnissen verarbeitet werden kann, müssen im System Fertigungsressourcen wie Maschinisten und Maschinen eingerichtet werden.

Maschinisten und Maschinen werden im System als Arbeitsplätze dargestellt, die in Form von Arbeitsplatzgruppen organisiert werden. Nachdem diese Ressourcen eingerichtet wurden, können sie gemäß der definierten  Material- und Verarbeitungsstruktur des Artikels und unter Berücksichtigung der Kapazität der Maschine oder des Arbeitsplatzes mit Arbeitsgängen geladen werden. Auch kann die Fertigungskapazität jeder einzelnen Ressource festgelegt werden. Die Kapazität wird durch die für die Arbeitsplätze und Arbeitsplatzgruppen verfügbare Arbeitszeit definiert und mithilfe von Kalendern für die einzelnen Ebenen gesteuert. In einem Arbeitsplatzgruppenkalender werden die Arbeitstage oder -stunden sowie Schichten, Feiertage und Fehlzeiten angegeben, anhand derer die verfügbare Bruttokapazität der Arbeitsplatzgruppe (üblicherweise gemessen in Minuten) bestimmt wird. All dies wird durch definierte Effizienz- und Kapazitätswerte festgelegt.  

Wenn Sie Produktion eingerichtet haben, können Sie Fertigungsaufträge berechnen und ausfüllen. Weitere Informationen finden Sie unter [Planung](production-planning.md) und [Produktion](production-manage-manufacturing.md).  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Konfigurieren der Produktionsfeatures, beispielsweise Definieren von Arbeitszeiten für den Fertigungsbereich und Auswählen von Planungsprinzipien|Öffnen Sie das **Produktion Einrichtung**-Fenster.|  
|Definieren einer Standardarbeitswoche mit Anfangs- und Endzeit der einzelnen Arbeitstage und der zugehörigen Schichten|[Einkaufskalender einrichten](production-how-to-create-work-center-calendars.md)|  
|Organisieren der festen Werte und des festen Bedarfs einer Fertigungsressource zum Steuern der fertig gestellten Mengen, die von einem Arbeitsplatz erstellt werden|[Arbeitsplätze und Arbeitsplatzgruppen einrichten](production-how-to-set-up-work-and-machine-centers.md)|
|Organisieren der Fertigungsarbeitsgänge im entsprechenden Auftrag und Zuordnen der Arbeitsplätze oder Arbeitsplatzgruppen mit den benötigten Arbeitsstunden.|[Routings erstellen](production-how-to-create-routings.md)|
|Organisieren der Produktionskomponenten oder Unterbaugruppen unter einem übergeordneten Artikel und gefertigten zertifizieren Sie die Stückliste für Bearbeitungs- in Arbeitsplatzgruppen.|[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)|
|Prüfen Sie, ob die rechte Teilmenge verfügbar ist, wenn Fertigungsartikel in Lager, aber in einer anderen Einheit gefertigt werden.|[Verwenden der Fertigungsloseinheit](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definieren von Fertigungsfamilien für Produkte mit ähnlichen Produktionsprozessen, um Verbrauch zu sparen. Beim Stanzen können vier Teile eines Artikels und 10 Teile eines anderen Artikels aus einem Blech zur gleichen Zeit gestanzt werden.|[Arbeiten mit Fertigungsfamilien](production-how-work-family.md)|
|Verwenden Sie einen Standardkatalog, die Erstellung von Arbeitsplänen zu vereinfachen, indem Sie weitere Informationen schnell wiederkehrende Arbeitsgänge zu verknüpfen.|[Einrichten von Aufgabenzeilen](production-how-set-up-standard-routing-lines.md)|  
|Vorbereiten von Arbeitsplatzgruppen und Arbeitspläne vor, zum Steuern vergebener Produktionsschritte darzustellen.|[Fertigung durch Fremdarbeitsvertrag](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Siehe auch
[Produktion](production-manage-manufacturing.md)    
[Planung](production-planning.md)   
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

