---
title: Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs
description: Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 4c28fcfbc2cbc7493ba183812383225754fd3dfa
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389649"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Einrichten von Status für Serviceaufträge und Reparaturen

Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln. Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.  

Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen. Die vier Prioritäten lauten: **Hoch** und **Sehr Hoch**, **Sehr Gering** und **Gering**.  

Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert. Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft. Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.  

Bevor Sie einen Reparaturstatus einrichten können, müssen Sie die Prioritäten für den Servicestatus festlegen.

## <a name="to-set-up-service-status-priorities"></a>So richten Sie Servicestatusprioritäten ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceauftragsstatus** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.  
3. Wählen Sie im Feld **Priorität** die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten.  

Wiederholen Sie die Schritte 2 und 3, bis Sie für jede der vier Statusoptionen eine Priorität festgelegt haben:  **Offen**, **In Bearbeitung**, **Erledigt** und **Warten** .  

## <a name="to-set-up-a-repair-status"></a>So richten Sie einen Reparaturstatus ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Reparaturstatus** ein und wählen Sie dann den entsprechenden Link.
2. Erstellen Sie einen neuen Reparaturstatus.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll. Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.  
5. Wählen Sie einen Reparaturstatus aus. Sie können nur einen auswählen. Ein Reparaturstatus kann nicht mit mehr als einer Reparaturstatusoption verknüpft sein.  
6. Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.  
7. Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.  
8. Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen** und **Status Warten zulassen** auf die gleiche Weise aus.

Wiederholen Sie diese Schritte für jede Reparaturstatusoption, die Sie erstellen möchten.

## <a name="see-also"></a>Siehe auch

[Serviceauftragsstatus und Reparaturstatus](service-service-order-status-and-repair-status.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]