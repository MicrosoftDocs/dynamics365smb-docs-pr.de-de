---
title: So bearbeiten Sie Serviceaufgaben | Microsoft Docs
description: Nachdem Sie Serviceaufträge und Angebote angelegt, Serviceartikelzeilen erfasst und den Serviceartikeln im Auftrag oder Angebot Ressourcen zugeordnet haben, können Sie mit der Reparatur und Wartung der Serviceartikel beginnen.
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
ms.openlocfilehash: 5b153d68636e948a01a5ab2d514828710e413f3d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311644"
---
# <a name="work-on-service-tasks"></a>Mit Serviceaufgaben arbeiten
Nachdem Sie Serviceaufträge und Angebote angelegt, Serviceartikelzeilen erfasst und den Serviceartikeln im Auftrag oder Angebot Ressourcen zugeordnet haben, können Sie mit der Reparatur und Wartung der Serviceartikel beginnen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] verfügt über eine Seite **Serviceaufgaben**, in dem Sie einen Überblick über alle Serviceartikel erhalten, die zu beachten sind. Betrachten Sie das Fenster als Serviceeinsatzplanung - Sie erfahren, welche Aufträge ausstehen, können nach Ersatzteilen suchen und diese erfassen und den Lagerbestand auf dem aktuellen Stand halten.  

Verwenden Sie zum Verfolgen von Änderungen und zum Darstellen einer grafischen Ansicht des Servicegeschäfts das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Statistiktool, um schnelle und automatisch generierte Diagramme und Analysen zu erstellen.  

## <a name="to-work-on-a-service-task"></a>So bearbeiten Sie eine Serviceaufgabe  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufgaben** ein, und wählen dann den zugehörigen Link aus.
2. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die einer bestimmen Ressource oder Ressourcengruppe zugeordnet sind, füllen Sie die Felder **Ressourcenfilter** oder **Ressourcengruppenfilter** aus, und drücken Sie die Eingabetaste.  
3. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die ein bestimmtes "Reagieren bis (Datum)" haben oder deren "Reagieren bis (Datum)" in eine bestimmte Periode fällt, dann füllen Sie das Feld **Reagieren bis (Datum)** aus, und drücken Sie die Eingabetaste.  
4. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die einen bestimmen Zuordnungsstatus oder Reparaturstatus haben, füllen Sie die Felder **Zuordnungsfilter** oder **Reparaturstatusfilter** aus, und drücken Sie die Eingabetaste.  
5. Wählen Sie die Serviceaufgabe aus, die Sie bearbeiten möchten. Wählen Sie auf der Registerkarte **Navigieren** in der Gruppe **Serviceaufgaben** die Option **Servicearbeitsschein** aus. Die Seite **Servicearbeitsschein** wird geöffnet.  
6. Tragen Sie Standardtext, Ersatzteile, Arbeitsstunden und Kosten wie gewünscht ein, indem Sie die entsprechende Option im Feld **Art** verwenden: <Blank>, **Artikel**, **Ressource** und **Kosten**.  
7. Wählen Sie im Feld **Reparaturstatus** den geeigneten Status aus.  

   > [!NOTE]  
   >  Füllen Sie das Feld **Reparaturstatus** mit dem Status **Beendet** oder **Unvollständig bearbeitet**, wenn die Serviceartikel entweder vollständig bearbeitet wurden oder eine andere Ressource die Arbeiten fortführen wird. Der Status **Erledigt** oder **Neuzuordnung notwendig** wird automatisch für den Zuordnungsposten dieses Serviceartikels angegeben.  

## <a name="to-register-service-operations"></a>So erfassen Sie Servicearbeiten  
Wenn Sie eine Servicearbeit für einen Serviceauftrag ausführen, können Sie die Details erfassen, indem Sie die verwendeten Artikel, die angefallenen Kosten und den Zeitaufwand angeben. Die von Ihnen eingegebenen Daten werden auf der Seite **Servicearbeitsschein** gespeichert. Sie können die Daten bei Bedarf aktualisieren.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie den Serviceauftrag, für den der Service erfasst werden soll, und wählen Sie eine Artikelzeile aus.  
3. Wählen Sie **Aktionen**, **Zeile** und dann **Servicearbeitsschein** aus.  
4. Geben Sie in den Zeilen die verwendeten Artikel, die angefallenen Kosten und den Zeitaufwand für die Servicearbeit ein.  

   > [!NOTE]  
   >  Sie können die Servicearbeit auch direkt in den Servicezeilen erfassen, die mit dem Serviceauftrag verknüpft sind.  

## <a name="to-register-spare-parts"></a>So erfassen Sie Ersatzteile  
Wenn Sie in Serviceaufträgen mit Serviceartikeln arbeiten, können Sie im Service Ersatzteile verwenden. Der folgende Ablauf zeigt, wie Ersatzteile auf der Seite **Servicearbeitsschein** erfasst werden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufgaben** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Zeile aus, die den relevanten Serviceartikel enthält, und wählen die **Servicearbeitsschein** Aktion aus.  
3. Geben Sie eine neue Servicezeile ein.  
4. Wählen Sie im Feld **Art**die Option **Artikel** aus.  
5. Geben Sie im Feld **Nr.** die relevanten Ersatzteile ein.  
6. Geben Sie in dem Feld **Menge** die Menge der Artikel ein, die Sie verwenden möchten.  

 Sie können ähnlich vorgehen, um die Ersatzteile auf der Seite **Servicezeilen** zu erfassen, die Sie auf der Seite **Serviceauftrag** öffnen können.  

## <a name="to-register-spare-parts-from-a-service-order"></a>So erfassen Sie Ersatzteile aus einem Serviceauftrag  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie den Serviceauftrag, für den Sie Ersatzteile erfassen möchten.  
3. Wählen Sie die Zeile mit dem gewünschten Serviceartikel aus. Wählen Sie **Aktionen** , **Auftrag**, und klicken Sie anschließend auf **Servicezeilen**.  
4. geben Sie eine neue Servicezeile ein.  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a>So ersetzen Sie einen Serviceartikel oder eine Serviceartikelkomponente  
Wenn Sie einen Serviceartikel warten, der sich aus Komponenten zusammensetzt, können Sie fehlerhafte Teile durch neue ersetzen. Jedes Mal, wenn Sie ein Ersatzteil für einen Serviceartikel mit Komponenten eingeben, können Sie auswählen, ob Sie eine Komponente ersetzen oder eine neue Komponente erstellen möchten. Der neue Artikel wird nicht als Komponente des Serviceartikels erfasst, bis Sie die Servicezeile oder den Serviceauftrag buchen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufgaben** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Zeile aus, die den Serviceartikel enthält, und wählen die **Servicearbeitsschein** Aktion aus.  
3. Geben Sie eine neue Servicezeile ein.  
4. Wählen Sie im Feld **Art**die Option **Artikel** aus.  
5. Geben Sie im Feld **Nr.** die zu ersetzende Komponente ein.  
6. Drücken Sie die **EINGABETASTE**. Ein Dialogfenster mit drei Optionsfeldern wird geöffnet: **Komponente ersetzen**, **Neue Komponente** und **Ignorieren**. Die Optionen werden in der folgenden Tabelle beschrieben.  

    |Option | Description|  
    |----------------------------------|---------------------------------------|  
    |**Komponente ersetzen**|Ändern den Status der Komponente, die ersetzt wird, auf "Inaktiv". Sie wird in der Liste der ersetzten Komponenten des Serviceartikels angezeigt.|  
    |**Neue Komponente**|Fügt die neue Komponente in die Komponentenübersicht des Serviceartikels ein.|  
    |**Ignorieren**|Es erfolgt kein Eintrag in der Komponentenübersicht des Serviceartikels.|  

7. Klicken Sie auf **Komponente ersetzen**.  
8. Wählen Sie die zu ersetzende Komponente aus, und wählen Sie dann **OK** aus.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>So ändern Sie die Reaktionszeit für eine Serviceartikelzeile  
Wenn Sie eine Serviceartikelzeile in einem Serviceauftrag oder -angebot registrieren, wird die Reaktionszeit in Stunden automatisch eingegeben und das Reaktionsdatum wird entsprechend berechnet, je nach dem, ob der Serviceartikel zu einem Servicevertrag gehört. Die Reaktionszeit in Stunden und das "Reagieren bis (Datum)" können geändert werden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufträge** oder **Serviceangebote** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie den Serviceauftrag oder die -anfrage aus, um die Karte zu öffnen.  
3. Geben Sie auf der Serviceartikelzeile, für die Sie die Reaktionszeit ändern möchten, entweder im Feld **Reaktionszeit (Std.)** oder in die Felder **Reagieren bis (Datum)** und **Reagieren bis (Uhrzeit)** die neuen Daten ein.  

## <a name="to-register-faultresolution-codes"></a>So erfassen Sie Problem-/Lösungscodes  
Nachdem ein Serviceartikel repariert wurde, können Sie sowohl den Problemcode als auch den Lösungscode für den Artikel erfassen, indem Sie eine Kombination der bestehenden Problem-/Lösungszuordnung auswählen. Die ausgewählten Problem- und Lösungscodes erscheinen nun in den entsprechenden Feldern auf der Seite **Servicearbeitsschein**. Sie können die Codes auch direkt auf dieser Seite erfassen.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufgaben** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Zeile aus, die den relevanten Serviceartikel enthält, und wählen die **Servicearbeitsschein** Aktion aus.  
3. Auf der Seite **Servicearbeitsschein** wählen Sie **Problem/Resol. Code-Verhältnisse** aus. Die Seite **Problem-/Lösungszuordnungen** wird geöffnet.  

  >  [!NOTE]
  >  Filter werden auf die angezeigten Zuordnungen gesetzt, indem die Serviceartikelgruppe und die Problemcodes aus der Seite **Servicearbeitsschein** kopiert werden.  

4. Füllen Sie die Zeile aus. Wählen Sie die richtige Kombination von Problem- und Lösungscodes, und wählen Sie dann die Schaltfläche **OK**, um diese auf den Serviceartikel zu kopieren. Wenn keine geeignete Kombination gefunden wird, können Sie eine neue Kombination auf der Seite erstellen.  

## <a name="see-also"></a>Siehe auch  
[Einrichten der Fehlerberichte](service-how-setup-fault-reporting.md)
[Zuordnungsstatus und Reparaturstatus](service-allocation-status-and-repair-status.md)  
[Servicebuchung](service-service-posting.md)  
