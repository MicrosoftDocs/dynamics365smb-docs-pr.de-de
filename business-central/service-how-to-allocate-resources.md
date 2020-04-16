---
title: 'Gewusst wie: Ressourcen zuweisen | Microsoft Docs'
description: Sie können den Betrag "Zu fakturieren (Jahr)" des Servicevertrags oder Vertragsangebots ändern, um den jährlich fakturierten Betrag zu korrigieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0238a5fc1799ba78616aeb08aa8d84e089094e6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195006"
---
# <a name="allocate-resources"></a>Ressourcen zuordnen
Kernstück des Servicemanagements sind die Mitarbeiter, von denen der Service bereitgestellt wird. Sie können einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)], um die geeigneten Mitarbeiter den entsprechenden Projekten zuzuweisen. Zuweisungen können auf Servicebereichen basieren, in denen Mitarbeiter tätig sind, oder in denen der Service stattfindet. Zudem können Ressourcen beim Antworten auf Serviceanforderungen zusammengruppiert werden. Weitere Informationen finden Sie unter [Ressourcen zuweisen einrichten](service-how-setup-resource-allocation.md).

Sie können Ressourcen, z B. Techniker zuweisen, indem Sie **Einsatzplanung** oder einen Serviceauftrag verwenden. Sie können Ressourcenverfügbarkeit verwenden, um Ressourcen zuzuordnen, um die Aufgaben in Aufträgen und Angeboten auszuführen.

Sie können im Fenster Ressourcenzuordnungen allen Serviceartikeln in einem Serviceauftrag dieselbe Ressource, z. B. einen Techniker, oder dieselbe Ressourcengruppe zuordnen. Zuordnungsposten werden für die anderen Serviceartikel im Auftrag mit derselben Ressourcennummer und demselben Zuordnungsdatum wie in der Zeile erstellt, die bereits zugeordnet wurde. Die zugeordneten Stunden entsprechen den zuvor zugeordneten Stunden, dividiert durch die Anzahl der Serviceartikel im Auftrag. Das Feld **Status** wird automatisch auf **Aktiv** für alle Posten gesetzt, die erstellt wurden.

## <a name="to-see-an-overview-of-service-orders-and-service-quotes"></a>So zeigen Sie eine Übersicht der Serviceaufträge und -angebote an  
Sie benötigen u. U. eine Übersicht an Serviceaufträgen oder Serviceangeboten, die bestimmten Bedingungen entsprechen, um diese dann eine nach der anderen mit bestimmten Vorgehensweisen abzuarbeiten. Sie müssen z. B. Serviceaufträgen Ressourcen zuordnen, die zu einem bestimmten Debitor gehören.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Einsatzplanung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Feld **Belegartenfilter** die Belegart, die Sie sehen möchten.
3. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die einer bestimmten Ressource oder Ressourcengruppe zugeordnet sind, füllen Sie die Felder **Ressourcenfilter** und  **Ressourcengruppenfilter** aus und betätigen Sie Enter.  
4. Wenn Sie eine Übersicht der Belege erhalten möchten, die ein bestimmtes "Reagieren bis (Datum)" haben oder deren "Reagieren bis (Datum)" in eine bestimmte Periode fällt, dann füllen Sie das Feld **Reagieren bis (Datum)** aus und betätigen **Enter**.  
5. Wenn Sie eine Übersicht der Belege mit einem bestimmten Zuordnungsstatus/Belegstatus erhalten möchten, füllen Sie die Felder **Zuordnungsfilter/Statusfilter** aus und betätigen Sie **Enter**.  
6. Wenn Sie eine Übersicht der Belege erhalten möchten, die zu einem bestimmten Vertrag/Debitor/Servicegebiet gehören, füllen Sie die Felder **Vertragsfilter/Debitorenfilter/Servicegebietsfilter** aus und betätigen Sie **Enter**.  
7. Wählen Sie eine Zeile aus, die einem Serviceauftrag oder einem Serviceangebot entspricht, und wählen die **Beleg anzeigen** Aktion aus.  

    Die Seite **Serviceauftrag** oder **Serviceangebot** wird geöffnet, und Sie können den Beleg bearbeiten. Um zu der Seite **Einsatzplanung** zurückzukehren, wählen Sie **OK**.

## <a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a>So weisen Sie eine Ressource anhand der Ressource oder der Ressourcengruppenverfügbarkeit zu    
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Dispatch-Plan** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den relevanten Serviceauftrag, und wählen Sie die **Ressourcen zuweisen** Aktion aus.  
3. Wählen Sie den Posten mit der Serviceaufgabe aus, der Sie eine Ressource zuordnen möchten.  
4. Wählen Sie **Ressourcen verfügbar** oder **Res.Gruppe Verfügbar** Aktion aus.  
5. Auf der Seite **Res. Verfügbarkeit (Service)** wählen Sie **Matrix anzeigen** aus.  
6. Wählen Sie eine Ressource, die Sie zuweisen möchten. Sie können Ihre Auswahl darauf basieren, ob die Ressource für die Aufgabe qualifiziert ist, ob sie sich in der Nähe des Debitors befindet und/oder ob sie von diesem Debitor bevorzugt wird.  
7. Wählen Sie ein Datum aus, an dem die Ressource genügend verfügbare Zeit zur Erledigung der Aufgabe hat. Außerdem sollte das Datum nahe der Reaktionszeit des Serviceauftrags liegen.  
8. Geben Sie im Feld **Zuzuordnende Menge** die Anzahl der Stunden ein, die Sie der Ressource für die Serviceaufgabe zuordnen möchten.  
9. Wählen Sie die Aktion **Zuordnen**, um die ausgewählte Ressource zum ausgewählten Datum zuzuordnen.  

     Das Feld **Status** wird automatisch auf **Aktiv** gesetzt.  

 Wiederholen Sie diese Schritte für jedes Datum, dem Sie eine Ressource in der Serviceaufgabe zuordnen möchten.  

> [!NOTE]  
>  Für einen Serviceartikel in einem Serviceauftrag kann es nur eine **Aktiven** Für einen Serviceartikel in einem Serviceauftrag kann es nur eine aktive Serviceauftragszuordnung mit einer Ressource oder Ressourcengruppe geben.  

## <a name="to-allocate-a-resource-using-a-service-order"></a>So weisen Sie eine Ressource in einem Serviceauftrag zu  
Nachdem Sie einen Serviceauftrag oder ein Serviceangebot erstellt und ausgefüllt haben, können Sie Ressourcen wie z. B. Techniker zuweisen, die die im Beleg als Serviceartikelzeilen erfassten Serviceaufgaben ausführen sollen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie das Menü Bestellung, und wählen Sie dann **Bearbeiten**.  
3. Klicken Sie in die Serviceartikelzeile, die der Serviceaufgabe entspricht, der Sie eine Ressource zuordnen möchten.  
4. Wählen Sie **Ressourcenzuordnungen.**
5. Wählen Sie auf der Seite **Ressourcenzuordnungen** einen inaktiven Zuordnungseintrag mit der Serviceaufgabe, der Sie die Ressource zuordnen möchten. Wenn kein inaktiver Zuordnungseintrag vorhanden ist, können Sie einen **Neuen** erstellen.  
7. Geben Sie die Serviceaufgabe an, indem Sie im Feld **Serviceartikelnr.** in derselben Zeile ausfüllen.  
8. Wählen Sie im Feld **Ressourcennr.** die entsprechende Ressource aus. Falls die Ressource Mitglied einer Ressourcengruppe ist, wird die Nummer der Ressourcengruppe automatisch in das Feld **Res.-Gruppennr.** übernommen. Feld  
9. Füllen Sie die Felder **Zuordnungsdatum** und **Zugeordnete Stunden** aus. Das Feld **Status** wird auf **Aktiv** gesetzt. Damit ist die Ressource der Serviceaufgabe zugeordnet.  
10. Optional, um die Ressource für alle Artikel zuzuordnen, wählen Sie **Allen Serviceartikeln zuordnen** aus.

> [!NOTE]  
>  Für einen Serviceartikel in einem Serviceauftrag kann es nur einen aktiven Zuordnungsposten mit einer Ressource oder Ressourcengruppe gleichzeitig geben.

## <a name="to-reallocate-resources-on-a-service-order"></a>So ordnen Sie Ressourcen in einem Serviceauftrag neu zu  
Sie können Ressourcen direkt von einem Serviceauftrag oder Serviceangebot aus neu zuordnen. Der alte Posten ist noch vorhanden, aber sein Status wird folgendermaßen aktualisiert:  

* Wenn der Service begonnen wurde, während die Zuordnung **Aktiv** war, d. h. falls der Reparaturstatus des Serviceartikels in dem Posten auf **In Bearbeitung** geändert wurde, ändert sich der Zuordnungsstatus von **Neuzuordnung notwendig** in **Erledigt**.  
* Falls der Service nicht begonnen wurde, während die Zuordnung **Aktiv** war, ändert sich der Zuordnungsstatus von **Neuzuordnung notwendig** in **Storniert**.  
* Wenn Sie einen Serviceauftrag zuordnen, den Sie aus einem Angebot erstellt haben, ändert sich der Status der Zuordnungsposten in dem Angebot beim Zuordnen der Serviceartikel in dem Serviceauftrag immer in **Erledigt**.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den relevanten Serviceauftrag.  
3. Markieren Sie die Dienstleistungspositionszeile, die der Serviceaufgabe entspricht, der Sie eine Ressource zuordnen möchten, und wählen Sie dann die Aktion **Ressourcenzuordnungen**.  
4. Wählen Sie auf der Seite **Ressourcenzuordnungen** einen Zuordnungsposten mit der Serviceaufgabe aus, der Sie die Ressource zuordnen möchten. Wählen Sie im Feld **Ressourcennr.** die entsprechende Ressource aus. Die bereits im Feld vorhandene Ressourcennummer wird überschrieben.  
5. Drücken Sie die EINGABETASTE. Es wird ein Dialogfeld geöffnet, in dem Sie gefragt werden, ob Sie diesen Posten neu zuordnen möchten. Füllen Sie bei Bedarf das Feld **Ursachencode** aus, und klicken Sie zum Bestätigen auf **Ja**.  
6. Füllen Sie die Felder **Zuordnungsdatum** und **Zugeordnete Stunden** aus. Der Posten enthält jetzt die neue Ressource und der Status ist **Aktiv**.

## <a name="to-reallocate-a-resource-using-the-dispatch-board"></a>So ordnen Sie eine Ressource mithilfe der Einsatzplanung neu zu  
Wenn die der Serviceaufgabe zugewiesene Ressource die Arbeiten nicht zu Ende führen kann, muss die Serviceaufgabe neu zugeordnet werden. Normalerweise ordnen Sie ein Serviceaufgabe mithilfe der **Einsatzplanung** neu zu.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Einsatzplanung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Feld **Zuordnungsfilter** **Neuzuordnung notwendig**. Die Seite **Einsatzplanung** zeigt nun nur die Serviceaufträge mit Serviceaufgaben an, die eine Neuzuordnung benötigen.  
3. Markieren Sie den entsprechenden Serviceauftrag und wählen Sie dann die Aktion **Ressourcenzuordnungen**. Die Seite **Ressourcenzuordnungen** wird geöffnet.  
4. Wählen Sie den Zuordnungsposten, dem Sie eine Ressource neu zuordnen wollen.  
5. Wählen Sie im Feld **Ressourcennr.** die entsprechende Ressource aus. Die bereits im Feld vorhandene Ressourcennummer wird überschrieben.  
6. Drücken Sie die Eingabetaste. Das Dialogfeld **Eintragsneuzuordnungsgründe** wird geöffnet und Sie werden gefragt, ob Sie diesen Posten neu zuordnen möchten. Füllen Sie bei Bedarf das Feld **Ursachencode** aus, und klicken Sie zum Bestätigen auf **Ja**.  
7.  Füllen Sie die Felder **Zuordnungsdatum** und **Zugeordnete Stunden** aus. Der Posten enthält jetzt die neue Ressource, und der Status ist **Aktiv**.  

    > [!NOTE]  
    >  Der alte Posten ist noch vorhanden, aber der Status wird folgendermaßen aktualisiert:  
    >   
    >  * Wenn der Service begonnen wurde, während die Zuordnung **Aktiv** war, d. h. falls der Reparaturstatus des Serviceartikels in dem Posten auf **In Bearbeitung** geändert wurde, ändert sich der Zuordnungsstatus von **Neuzuordnung notwendig** in **Erledigt**.  
    > * Falls der Service nicht begonnen wurde, während die Zuordnung **Aktiv** war, ändert sich der Zuordnungsstatus von **Neuzuordnung notwendig** in **Storniert**.  
    > * Wenn Sie einen Serviceauftrag zuordnen, den Sie aus einem Angebot erstellt haben, ändert sich der Status der Zuordnungsposten in dem Angebot beim Zuordnen der Serviceartikel in dem Serviceauftrag immer in **Erledigt**.  

## <a name="to-register-resource-hours"></a>So erfassen Sie Ressourcenzeiten  
Wenn Sie in Serviceaufträgen mit Serviceartikeln arbeiten, müssen Sie die Ressourcenzeiten, die im Service verwendet werden, erfassen. Der folgende Ablauf zeigt, wie Ressourcenzeiten auf der Seite **Servicearbeitsschein** erfasst werden können.  

Sie können dieselbe Vorgehensweise verwenden, um die Stunden im Fenster **Servicezeilen** zu erfassen, das Sie auf der Seite "Serviceauftrag" öffnen können. Öffnen Sie die entsprechende Servicekarte und wählen Sie dann die Aktion **Servicereihen**.  

Wenn dieselbe Ressource an allen Serviceartikeln im Serviceauftrag arbeitet, erfassen Sie die gesamte Ressourcenzeit nur für einen Serviceartikel und teilen die Ressourcenzeile auf, um die Ressourcenzeiten den anderen Serviceartikeln zuzuordnen.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceaufgaben** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile aus, die den relevanten Serviceartikel enthält, und wählen die **Servicearbeitsschein** Aktion aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-resource-to-all-service-items-in-an-order"></a>So ordnen Sie allen Serviceartikeln in einem Serviceauftrag Ressourcen zu
Wenn dieselbe Ressource an allen Serviceartikeln im Serviceauftrag arbeitet, erfassen Sie die gesamten Ressourcenzeiten nur für einen Serviceartikel und teilen die Ressourcenzeile auf, um die Ressourcenzeiten auf die Ressourcenzeilen der anderen Serviceartikel zu verteilen.  

Der folgende Vorgang zeigt, wie Ressourcenzeilen auf der Seite **Servicerechnungszeilen** aufgeteilt werden können.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den relevanten Serviceauftrag.  
3. Wählen Sie auf der Registerkarte **Linien** FastTab die Aktion **Leistungszeilen**. Die Seite **Servicezeilen** wird geöffnet.  
4. Wählen Sie die Ressourcenzeile aus, die Sie aufteilen möchten. Der Inhalt des Feldes **Menge** wird auf alle Serviceartikel im Serviceauftrag aufgeteilt.  
5. Wählen Sie die Aktion **Ressourcenzeile teilen**. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.  

    Ressourcenzeilen für die anderen Serviceartikel im Auftrag werden mit der gleichen Ressourcennummer wie die aufgeteilte Zeile erstellt. Die Menge entspricht der Menge der Zeile, die aufgeteilt wurde, geteilt durch die Anzahl der Serviceartikel im Auftrag.  

## <a name="to-cancel-an-allocation"></a>So stornieren Sie eine Zuordnung  
Sie können Ressourcenzuordnungen für Serviceaufgaben stornieren, ohne die Aufgaben neu zuzuordnen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Einsatzplanung** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den relevanten Serviceauftrag, und wählen Sie die **Ressourcen zuweisen** Aktion aus.  
3. Wählen Sie den Zuordnungsposten mit der Serviceaufgabe aus, für die Sie die Zuordnung stornieren möchten.  
4. Wählen Sie die Aktion **Verteilung stornieren** aus.  
5. Wählen Sie im Feld **Ursachencode** den entsprechenden Code aus.  
6. Wählen Sie **Ja**, um die Stornierung zu bestätigen.  

    > [!NOTE]  
    > Die Anwendung wählt automatisch die Option **Neuzuordnung notwendig** in dem Feld **Status** aus. Falls der Reparaturstatus des Serviceartikels in dem Posten **Anfang** ist, wird der Reparaturstatus auf **Weitergeleitet** geändert (es wurden keine Servicearbeiten ausgeführt). Steht der Reparaturstatus auf **In Bearbeitung**, ändert sich der Status in **Nicht abgeschlossen** (einige Arbeiten wurden erledigt).

## <a name="see-also"></a>Siehe auch
[Ressourcenzuweisung einrichten](service-how-setup-resource-allocation.md)  
[Zuordnungsstatus und Reparaturstatus](service-allocation-status-and-repair-status.md)  
