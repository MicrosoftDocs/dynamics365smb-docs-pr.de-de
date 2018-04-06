---
title: "Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs"
description: "Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bc804db29ec89904101f48b625770f730abb13d9
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Einrichten von Status für Serviceaufträge und Reparaturen
Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln. Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.  

Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen. Die vier Prioritäten lauten: "Hoch" und "Sehr Hoch", "Sehr Gering" und "Gering".  
  
Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert. Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft. Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.  

## <a name="to-set-up-a-repair-status"></a>So richten Sie einen Reparaturstatus ein  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Reparaturstatus** ein. Wählen Sie dann den zugehörigen Link aus. 2. Erstellen Sie einen neuen Reparaturstatus.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll. Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.  
5. Wählen Sie einen Reparaturstatus aus. Sie können nur einen auswählen.  
6. Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.  
7. Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.  
8. Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen**und **Status Warten zulassen** auf die gleiche Weise aus.
  
## <a name="to-set-up-service-status-priorities"></a>So richten Sie Servicestatusprioritäten ein  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceauftragsstatus** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.  
3. Wählen Sie im Feld **Priorität**die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten. Wiederholen Sie diesen Schritt für jeden Status.  
  
## <a name="see-also"></a>Siehe auch  
[Serviceauftragsstatus und Reparaturstatus]()  
[Einrichten der Serviceverwaltung](service-setup-service.md)  

