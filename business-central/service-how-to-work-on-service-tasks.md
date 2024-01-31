---
title: Wie Sie Serviceaufgaben bearbeiten
description: 'Dieses Thema behandelt die verschiedenen Möglichkeiten, Serviceaufgaben zu bearbeiten. Die Seite Serviceaufgaben gibt einen Überblick über alle Elemente, die bearbeitet werden müssen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Mit Serviceaufgaben arbeiten
Nachdem Sie Serviceaufträge und Angebote angelegt, Serviceartikelzeilen erfasst und den Serviceartikeln im Auftrag oder Angebot Ressourcen zugeordnet haben, können Sie mit der Reparatur und Wartung der Serviceartikel beginnen.  

[!INCLUDE[prod_short](includes/prod_short.md)] verfügt über eine Seite **Serviceaufgaben**, in dem Sie einen Überblick über alle Serviceartikel erhalten, die zu beachten sind. Betrachten Sie das Fenster als Serviceeinsatzplanung - Sie erfahren, welche Aufträge ausstehen, können nach Ersatzteilen suchen und diese erfassen und den Lagerbestand auf dem aktuellen Stand halten.  

Verwenden Sie zum Verfolgen von Änderungen und zum Darstellen einer grafischen Ansicht des Servicegeschäfts das [!INCLUDE[prod_short](includes/prod_short.md)]-Statistiktool, um schnelle und automatisch generierte Diagramme und Analysen zu erstellen.  

## So bearbeiten Sie eine Serviceaufgabe  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"). Symbol. Geben Sie **Serviceaufgaben** ein und wählen Sie dann den zugehörigen Link.
2. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die einer bestimmen Ressource oder Ressourcengruppe zugeordnet sind, füllen Sie die Felder **Ressourcenfilter** oder **Ressourcengruppenfilter** aus, und wählen Sie die <kbd>Eingabetaste</kbd>.  
3. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die ein bestimmtes „Reagieren bis (Datum)“ haben oder deren „Reagieren bis (Datum)“ in eine bestimmte Periode fällt, dann füllen Sie das Feld **Reagieren bis (Datum)** aus, und wählen Sie die <kbd>Eingabetaste</kbd>.  
4. Wenn Sie eine Übersicht der Serviceaufgaben erhalten möchten, die einen bestimmen **Zuordnungsstatus** oder **Reparaturstatus** haben, füllen Sie die Felder Zuordnungsfilter oder Reparaturstatusfilter aus, und wählen Sie die <kbd>Eingabetaste</kbd>.  
5. Wählen Sie die Serviceaufgabe aus, die Sie bearbeiten möchten. Wählen Sie die Aktion **Artikel-Arbeitsblatt** aus. Die Seite **Servicearbeitsblatt** wird geöffnet.  
6. Tragen Sie Standardtext, Ersatzteile, Arbeitsstunden und Kosten wie gewünscht ein, indem Sie die entsprechende Option im Feld **Art** verwenden: \<Blank\>, **Artikel**, **Ressource** und **Kosten**.  
7. Wählen Sie im Feld **Reparaturstatus** den geeigneten Status aus.  

   > [!NOTE]  
   >  Füllen Sie das Feld **Reparaturstatus** mit dem Status **Beendet** oder **Unvollständig bearbeitet**, wenn die Serviceartikel entweder vollständig bearbeitet wurden oder eine andere Ressource die Arbeiten fortführen wird. Der Status **Erledigt** oder **Neuzuordnung notwendig** wird automatisch für den Zuordnungsposten dieses Serviceartikels angegeben.  

## So erfassen Sie Servicearbeiten  
Wenn Sie eine Servicearbeit für einen Serviceauftrag ausführen, können Sie die Details erfassen, indem Sie die verwendeten Artikel, die angefallenen Kosten und den Zeitaufwand angeben. Die von Ihnen eingegebenen Daten werden auf der Seite **Servicearbeitsblatt** gespeichert. Sie können die Daten bei Bedarf aktualisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Serviceauftrag, für den der Service erfasst werden soll, und wählen Sie eine Artikelzeile aus.  
3. Wählen Sie die Aktion **Servicearbeitsblatt**.  
4. Geben Sie in den Zeilen die verwendeten Artikel, die angefallenen Kosten und den Zeitaufwand für die Servicearbeit ein.  

   > [!NOTE]  
   >  Sie können die Servicearbeit auch direkt in den Servicezeilen erfassen, die mit dem Serviceauftrag verknüpft sind.  

## So erfassen Sie Ersatzteile  
Wenn Sie in Serviceaufträgen mit Serviceartikeln arbeiten, können Sie im Service Ersatzteile verwenden. Der folgende Ablauf zeigt, wie Ersatzteile auf der Seite **Servicearbeitsblatt** erfasst werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Serviceaufgaben** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile aus, die den relevanten Serviceartikel enthält, und wählen die **Servicearbeitsblatt** Aktion aus.  
3. Geben Sie eine neue Servicezeile ein.  
4. Wählen Sie im Feld **Art** die Option **Artikel** aus.  
5. Geben Sie im Feld **Nr.** die relevanten Ersatzteile ein.  
6. Geben Sie in dem Feld **Menge** die Menge der Artikel ein, die Sie verwenden möchten.  

 Sie können ähnlich vorgehen, um die Ersatzteile auf der Seite **Servicezeilen** zu erfassen, die Sie auf der Seite **Serviceauftrag** öffnen können.  

## So erfassen Sie Ersatzteile aus einem Serviceauftrag  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Serviceauftrag, für den Sie Ersatzteile erfassen möchten.  
3. Wählen Sie die Zeile mit dem gewünschten Serviceartikel aus. Wählen Sie **Aktionen** , **Auftrag**, und klicken Sie anschließend auf **Servicezeilen**.  
4. geben Sie eine neue Servicezeile ein.  

## So ersetzen Sie einen Serviceartikel oder eine Serviceartikelkomponente  
Wenn Sie einen Serviceartikel warten, der sich aus Komponenten zusammensetzt, können Sie fehlerhafte Teile durch neue ersetzen. Jedes Mal, wenn Sie ein Ersatzteil für einen Serviceartikel mit Komponenten eingeben, können Sie auswählen, ob Sie eine Komponente ersetzen oder eine neue Komponente erstellen möchten. Der neue Artikel wird nicht als Komponente des Serviceartikels erfasst, bis Sie die Servicezeile oder den Serviceauftrag buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 5.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Serviceaufgaben** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile aus, die den Serviceartikel enthält, und wählen die **Servicearbeitsblatt** Aktion aus.  
3. Geben Sie eine neue Servicezeile ein.  
4. Wählen Sie im Feld **Art** die Option **Artikel** aus.  
5. Geben Sie im Feld **Nr.** die zu ersetzende Komponente ein.  
6. Wählen Sie die <kbd>EINGABETASTE</kbd>. Ein Dialogfenster mit drei Optionsfeldern wird geöffnet: **Komponente ersetzen**, **Neue Komponente** und **Ignorieren**. Die Optionen werden in der folgenden Tabelle beschrieben.  

    |Option | Description|  
    |----------------------------------|---------------------------------------|  
    |**Komponente ersetzen**|Ändern den Status der Komponente, die ersetzt wird, auf "Inaktiv". Sie wird in der Liste der ersetzten Komponenten des Serviceartikels angezeigt.|  
    |**Neue Komponente**|Fügt die neue Komponente in die Komponentenübersicht des Serviceartikels ein.|  
    |**Ignorieren**|Es erfolgt kein Eintrag in der Komponentenübersicht des Serviceartikels.|  

7. Klicken Sie auf **Komponente ersetzen**.  
8. Wählen Sie die zu ersetzende Komponente aus, und wählen Sie dann **OK** aus.  

## So ändern Sie die Reaktionszeit für eine Serviceartikelzeile  
Wenn Sie eine Serviceartikelzeile in einem Serviceauftrag oder -angebot registrieren, wird die Reaktionszeit in Stunden automatisch eingegeben und das Reaktionsdatum wird entsprechend berechnet, je nach dem, ob der Serviceartikel zu einem Servicevertrag gehört. Die Reaktionszeit in Stunden und das "Reagieren bis (Datum)" können geändert werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 6.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** oder **Serviceangebote** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Serviceauftrag oder die -anfrage aus, um die Karte zu öffnen.  
3. Geben Sie auf der Serviceartikelzeile, für die Sie die Reaktionszeit ändern möchten, entweder im Feld **Reaktionszeit (Std.)** oder in die Felder **Reagieren bis (Datum)** und **Reagieren bis (Uhrzeit)** die neuen Daten ein.  

## So erfassen Sie Problem-/Lösungscodes  
Nachdem ein Serviceartikel repariert wurde, können Sie sowohl den Problemcode als auch den Lösungscode für den Artikel erfassen, indem Sie eine Kombination der bestehenden Problem-/Lösungszuordnung auswählen. Die ausgewählten Problem- und Lösungscodes erscheinen nun in den entsprechenden Feldern auf der Seite **Servicearbeitsblatt**. Sie können die Codes auch direkt auf dieser Seite erfassen.  

1. Wählen Sie die ![Glühbirne, die die Tell Me-Funktion öffnet 7.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Serviceaufgaben** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile aus, die den relevanten Serviceartikel enthält, und wählen die **Servicearbeitsblatt** Aktion aus.  
3. Auf der Seite **Servicearbeitsblatt** wählen Sie **Problem/Resol. Code-Verhältnisse** aus. Die Seite **Problem-/Lösungszuordnungen** wird geöffnet.  

  >  [!NOTE]
  >  Filter werden auf die angezeigten Zuordnungen gesetzt, indem die Serviceartikelgruppe und die Problemcodes aus der Seite **Servicearbeitsblatt** kopiert werden.  

4. Füllen Sie die Zeile aus. Wählen Sie die richtige Kombination von Problem- und Lösungscodes, und wählen Sie dann die Schaltfläche **OK**, um diese auf den Serviceartikel zu kopieren. Wenn keine geeignete Kombination gefunden wird, können Sie eine neue Kombination auf der Seite erstellen.  

## Siehe auch  
[Einrichten der Fehlerberichte](service-how-setup-fault-reporting.md)
[Zuordnungsstatus und Reparaturstatus](service-allocation-status-and-repair-status.md)  
[Servicebuchung](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]