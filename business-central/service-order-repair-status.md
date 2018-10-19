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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 366bf200b78e4927b1c202340dd84af09d32c1a5
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Einrichten von Status für Serviceaufträge und Reparaturen
Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln. Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.  

Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen. Die vier Prioritäten lauten: "Hoch" und "Sehr Hoch", "Sehr Gering" und "Gering".  

Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert. Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft. Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.  

## <a name="to-set-up-a-repair-status"></a>So richten Sie einen Reparaturstatus ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Reparaturstatus** ein, und wählen dann den zugehörigen Link aus.
2. Erstellen Sie einen neuen Reparaturstatus.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll. Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.  
5. Wählen Sie einen Reparaturstatus aus. Sie können nur einen auswählen.  
6. Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.  
7. Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.  
8. Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen**und **Status Warten zulassen** auf die gleiche Weise aus.
  
## <a name="to-set-up-service-status-priorities"></a>So richten Sie Servicestatusprioritäten ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceauftragsstatus** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.  
3. Wählen Sie im Feld **Priorität**die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten. Wiederholen Sie diesen Schritt für jeden Status.  

## <a name="see-also"></a>Siehe auch  
[Serviceauftragsstatus und Reparaturstatus](service-service-order-status-and-repair-status.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  

