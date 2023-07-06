---
title: Zuweisungsstatus und Reparaturstatus | Microsoft Docs
description: Kennenlernen des Verhältnisses zwischen dem Reparaturstatus der Serviceartikel und dem Zuordnungsstatus von Zuordnungen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocation-status-and-repair-status-of-service-items"></a><a name="allocation-status-and-repair-status-of-service-items"></a><a name="allocation-status-and-repair-status-of-service-items"></a>Zuordnungsstatus und Reparaturstatus von Serviceartikeln
Der Reparaturstatus der Serviceartikel und der Zuordnungsstatus von Zuordnungen für Serviceartikel stellen unter "Service" eine bestimmte Beziehung zueinander dar. Der Zuordnungsstatus ändert sich, wenn Sie den Reparaturstatus des Serviceartikels auf **Erledigt** oder **Unvollständig bearbeitet** setzen oder wenn Sie ein Serviceangebot in einen Serviceauftrag umwandeln. Der Reparaturstatus des Serviceartikels ändert sich, wenn Sie die Serviceartikelzuordnung stornieren oder den Serviceartikel einer anderen Ressource neu zuordnen. Sie können den Reparaturstatus der Serviceartikel auf der Seite **Serviceaufgaben** einsehen und ihn im Feld **Reparaturstatuscode** auf der Seite **Servicearbeitsblatt** aktualisieren. Sie können den Zuordnungsstatus im Feld **Status** der Seite **Ressourcenzuordnungen** einsehen.  
  
## <a name="changing-repair-status"></a><a name="changing-repair-status"></a><a name="changing-repair-status"></a>Ändern des Reparaturstatus
Wenn Sie den Reparaturstatus eines Serviceartikels in einer Serviceauftragszeile ändern, sucht die Anwendung nach einem entsprechenden Zuordnungseintrag für diesen Serviceartikel, der den Status **Aktiv** hat. Wenn eine solche Zuordnung gefunden wird, wird der Status dieser Zuordnung gemäß einer der folgenden Methoden aktualisiert:  
  
* Wenn Sie den Reparaturstatus auf **Erledigt** ändern, ändert die Anwendung den Zuordnungsstatus von **Aktiv** auf **Erledigt**.  
* Wenn Sie den Reparaturstatus auf **Unvollständig bearbeitet** (ein Teil des Services wurde durchgeführt) oder **Weitergeleitet** (es wurde noch kein Service durchgeführt) setzen, ändert die Anwendung den Zuordnungsstatus von **Aktiv** auf **Neuzuordnung notwendig**.  
* Wenn ein Serviceauftragszuordnung-Posten erstellt wird, der angibt, dass keine Ressourcen zugeordnet wurden, setzt die Anwendung das Feld **Status** auf der Seiten **Ressourcenzuordnungen** auf **Inaktiv**.  
* Die Anwendung legt den Status des Zuordnungspostens auf **Storniert** fest, wenn Sie den Serviceartikel, auf den im Serviceauftragszuordnungs-Posten verwiesen wird, erneut zuordnen und so angeben, dass die zugeordnete Ressource oder Ressourcengruppe mit der Serviceaufgabe noch nicht begonnen hat.  
  
Der Zuordnungsstatus gibt also an, wenn der Serviceprozess beendet ist, oder wenn eine andere Ressource nötig ist, um den Service an diesem Serviceartikel zu beenden.  
  
## <a name="converting-service-quotes-to-service-orders"></a><a name="converting-service-quotes-to-service-orders"></a><a name="converting-service-quotes-to-service-orders"></a>Vertragsangebote in Serviceaufträge umwandeln
Wenn Sie ein Serviceangebot in einen Serviceauftrag umwandeln, aktualisiert die Anwendung den Serviceauftrag, die Serviceartikel in dem Auftrag und deren Zuordnungsstatus auf die folgenden Arten:  
  
* Die Anwendung ändert den Reparaturstatus der Serviceartikel auf **Anfang**.  
* Der Serviceauftragsstatus ändert sich zu **Offen**.  
* Die Anwendung sucht nach Zuordnungen für alle Serviceartikel des Serviceauftrags mit dem Status **Aktiv**. Wenn solche Zuordnungen gefunden werden, wird der Zuordnungsstatus von **Aktiv** auf **Neuzuordnung notwendig** geändert.  
  
## <a name="canceling-allocations"></a><a name="canceling-allocations"></a><a name="canceling-allocations"></a>Zuordnungen stornieren
Wenn Sie die Zuordnung für einen Serviceartikel stornieren, aktualisiert [!INCLUDE[prod_short](includes/prod_short.md)] den Zuordnungsstatus des entsprechenden Zuordnungspostens von **Aktiv**auf **Neuzuordnung erforderlich**.

Der Reparaturstatus der Serviceartikel wird in dem Zuordnungsposten auf die folgenden Arten aktualisiert:  
  
* Steht der Reparaturstatus auf **Anfang**, ändert sich der Status in **Weitergeleitet** (es wurden noch keine Servicearbeiten durchgeführt).  
* Steht der Reparaturstatus auf **In Bearbeitung**, ändert sich der Status in **Nicht abgeschlossen** (einige Arbeiten wurden erledigt).  
  
## <a name="reallocating-an-active-allocation-entry"></a><a name="reallocating-an-active-allocation-entry"></a><a name="reallocating-an-active-allocation-entry"></a>Eine aktive Zuordnung neu zuordnen
Wenn Sie einen Serviceartikel neu zuordnen, der in einem Zuordnungsposten mit dem Status **Aktiv** enthalten ist, aktualisiert die Anwendung den Zuordnungsposten auf die folgenden Arten:  
  
* Wenn der Service begonnen wurde, als die Zuordnung **Aktiv** war (d. h. falls der Reparaturstatus des Serviceartikels in dem Posten auf **In Bearbeitung** geändert wurde), ändert die Anwendung den Zuordnungsstatus von **Aktiv** auf **Erledigt**.  
* Falls der Service nicht begonnen wurde, als die Zuordnung **Aktiv** war, ändert die Anwendung den Zuordnungsstatus von **Aktiv** auf **Storniert**.  
  
Die Anwendung aktualisiert den Reparaturstatus der Serviceartikel in dem Zuordnungsposten auf die gleiche Weise, als ob Sie die Zuordnung storniert hätten:  
  
* Steht der Reparaturstatus auf **Anfang**, ändert sich der Status in **Weitergeleitet** (es wurden noch keine Servicearbeiten durchgeführt).  
* Steht der Reparaturstatus auf **In Bearbeitung**, ändert sich der Status in **Nicht abgeschlossen** (einige Arbeiten wurden erledigt).  
  
Ein neuer Zuordnungsposten mit dem Zuordnungsstatus **Aktiv** wird erstellt, der die neue Ressource enthält.  
  
## <a name="reallocating-a-service-item"></a><a name="reallocating-a-service-item"></a><a name="reallocating-a-service-item"></a>Serviceaufgabenneu zuordnen
Wenn Sie einen Serviceartikel neu zuordnen, der in einem Zuordnungsposten mit dem Status **Neuzuordnung notwendig** enthalten ist, aktualisiert die Anwendung den Zuordnungsposten auf die folgenden Arten:  
  
* Wenn der Service begonnen wurde, als die Zuordnung **Aktiv** war (d. h. falls der Reparaturstatus des Serviceartikels in dem Posten auf **In Bearbeitung** geändert wurde), ändert die Anwendung den Zuordnungsstatus von **Neuzuordnung notwendig** auf **Erledigt**.  
* Falls der Service nicht begonnen wurde, als die Zuordnung **Aktiv** war, ändert die Anwendung den Zuordnungsstatus von **Neuzuordnung notwendig** auf **Storniert**.  
  
Ein neuer Zuordnungsposten mit dem Zuordnungsstatus **Aktiv** wird erstellt, der die neue Ressource enthält.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch
[Ressourcenzuweisung einrichten](service-how-setup-resource-allocation.md)  
[Ressourcen zuordnen](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
