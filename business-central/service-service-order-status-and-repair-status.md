---
title: Serviceauftragsstatus und Reparaturstatus | Microsoft Docs
description: Das Feld "Status" auf der Seite "Serviceauftrag" und das Feld "Reparaturstatuscode" (der Serviceartikelreparaturstatus) auf der Seite "Serviceauftrag stellen" im Service eine bestimmte Beziehung zueinander dar. Der Serviceauftragsstatus spiegelt den Reparaturstatus aller Serviceartikel des Serviceauftrags wider.
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
ms.openlocfilehash: f55e33490bb70fae2b37eda6fe0b43f982fe8493
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311596"
---
# <a name="service-order-status-and-repair-status"></a>Serviceauftragsstatus und Reparaturstatus
Das Feld **Status** auf der Seite **Serviceauftrag** und das Feld **Reparaturstatuscode** (der Serviceartikelreparaturstatus) auf der Seite **Serviceauftrag stellen** im Service eine bestimmte Beziehung zueinander dar. Der Serviceauftragsstatus spiegelt den Reparaturstatus aller Serviceartikel des Serviceauftrags wider.  

> [!NOTE]  
>  Die beiden Felder sind nicht mit dem Feld **Freigabestatus** des Serviceauftragskopfs verbunden, der den Lagerdurchlauf von Serviceartikeln steuert.  

 Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Auftragsstatus aktualisiert. Um den gesamten Reparaturstatus einzelner Serviceartikel anzuzeigen, müssen Sie Folgendes angeben:  

* Den Serviceauftragsstatus, mit dem jeder Reparaturstatus verknüpft ist. Weitere Informationen finden Sie unter Serviceauftrag einrichten.  
* Die Prioritätsstufe jeder Serviceauftragsstatus Option. Weitere Informationen finden Sie unter Priorität  

 Wenn Sie ein Serviceangebot in einen Serviceauftrag umwandeln, wird der Reparaturstatus der einzelnen Serviceartikel in dem Serviceauftrag in **Anfang** und der Serviceauftragsstatus in **Offen** geändert.  

## <a name="specifying-service-order-status-for-repair-status"></a>Serviceauftragsstatus für Reparaturstatusoptionen festlegen  
Jeder Reparaturstatus ist mit einem bestimmten Serviceauftragsstatus verknüpft. Die Optionen für den Serviceauftragsstatus sind **Offen**, **In Bearbeitung**, **Warten** und **Erledigt**. Die Optionen für den Reparaturstatus sind **Anfangsstatus**, **Angebot erstellt**, **Ersatzteil bestellt**, **Ersatzteil erhalten**, **Service ist erledigt**, **Service in Bearbeitung**, **Unvollständig bearbeitet**, **Warten auf Debitor** und **Weitergeleitet**.  

### <a name="pending"></a>"Offen"  
Der Serviceauftragsstatus **Offen** gibt an, dass der Service jederzeit beginnen oder fortgesetzt werden kann. Aus diesem Grunde können die vier Reparaturstatusoptionen **Anfang**, **Weitergeleitet**, **Unvollständig bearbeitet** und **Ersatzteil erhalten** mit diesem Serviceauftragsstatus verknüpft werden.  

### <a name="in-process"></a>"In Bearbeitung"  
Der Serviceauftragsstatus **In Bearbeitung** gibt an, dass der Service in Bearbeitung ist. Aus diesem Grunde können die zwei Reparaturstatusoptionen **In Bearbeitung** und **Ersatzteil bestellt** mit diesem Serviceauftragsstatus verknüpft werden. Wenn Sie den Status **Ersatzteil bestellt** mit dem Serviceauftragsstatus **In Bearbeitung** verknüpfen, müssen Sie auch den Status **Ersatzteil erhalten** mit diesem Serviceauftragsstatus verknüpfen.  

### <a name="on-hold"></a>Warten  
Der Serviceauftragsstatus **Warten** gibt an, dass der Service zeitweilig gesperrt ist, da Sie auf die Antwort eines Debitors oder auf Ersatzteile warten, bevor der Service gestartet werden kann. Aus diesem Grunde können die drei Reparaturstatusoptionen **Angebot erstellt**, **Ersatzteil bestellt** und **Warten auf Debitor** mit diesem Serviceauftragsstatus verknüpft werden.  

### <a name="finished"></a>"Erledigt"  
Der Serviceauftragsstatus **Erledigt** gibt an, dass der Service abgeschlossen wurde. Deshalb wird der Reparaturstatus **Erledigt** mit diesem Status verknüpft.  

## <a name="assigning-priority-to-service-order-status"></a>Einem Serviceauftragsstatus eine Priorität zuordnen  
Wenn der Reparaturstatus eines Serviceartikels geändert wird, werden die Serviceauftragsstatusoptionen, die mit den verschiedenen Reparaturstatusoptionen aller Serviceartikel des Auftrags verknüpft sind, identifiziert. Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.  

Sie müssen entscheiden, welcher Serviceauftragsstatus die wichtigsten Informationen über den Status des Serviceauftrages enthält und diesen Status mit der höchsten Priorität verbinden usw.  

### <a name="example"></a>Beispiel  
Eine typische Zuordnung von Prioritätsstufen könnte folgendermaßen aussehen:  

* "In Bearbeitung" - Sehr hoch  
* "Offen" - Hoch  
* "Warten" - Niedrig  
* "Erledigt" - Sehr niedrig  

Wenn ein Serviceartikel z. B. den Status **Anfang** hat (verbunden mit dem Serviceauftragsstatus **Warten**), einer den Reparaturstatus **In Bearbeitung** (verbunden mit dem Serviceauftragsstatus **In Bearbeitung**) und ein dritter den Reparaturstatus **Ersatzteil bestellt** (verbunden mit dem Serviceauftragsstatus **Warten**), ist der Auftragsstatus dann **In Bearbeitung**, weil er die höchste Priorität hat.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Status für Serviceaufträge und Reparaturen](service-order-repair-status.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
