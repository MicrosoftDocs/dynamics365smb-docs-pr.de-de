---
title: Arbeitszeittabellen verwenden
description: 'Erfahren Sie, wie Sie Arbeitszeittabellen für Ressourcen, Projekte und Dienste erstellen, übermitteln, genehmigen und veröffentlichen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 02/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Arbeitszeittabellen verwenden

Dieser Artikel beschreibt, wie Sie Arbeitszeittabellen zur Nachverfolgung von Abwesenheit sowie von Zeit und Ressourcen verwenden, die für ein Projekt aufgewendet werden. Die Zeiterfassung hilft Ihnen, Probleme frühzeitig zu erkennen und Verzögerungen oder Kostenüberschreitungen zu vermeiden. Arbeitszeittabellen erleichtern es einer Ressource, die Zeitverwendung für eine Person oder eine Maschine zu melden, so dass Vorgesetzte die Verwendung und deren Zuordnung überprüfen können.

Sie können Ihre Projektplanzeilen in die Arbeitszeittabelle kopieren und verwenden. Auf diese Art müssen Sie die Informationen immer nur an einer Stelle eingeben und die Zeileninformationen sind immer korrekt. Weitere Informationern finden Sie unter [So kopieren Sie Projektplanzeilen in eine Arbeitszeittabelle](#copy-project-planning-lines-to-a-time-sheet).

Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das entsprechende Projekt- oder Ressourcen-Buch.-Blatt buchen. Weitere Informationen finden Sie unter [Buchen von Arbeitszeittabellenzeilen in einem Projektbuchungsblatt](#post-time-sheet-lines-in-a-project-journal) und [Buchen von Arbeitszeittabellenzeilen zu einem Ressourcen-Buch.-Blatt](#post-time-sheet-lines-in-a-resource-journal).

Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie Informationen einrichten und einen Administrator und mindestens einen Genehmiger für Arbeitszeittabellen festlegen. Weitere Informationen zum Einrichten von Arbeitszeittabellen finden Sie unter [Arbeitszeittabellen einrichten](projects-how-setup-time-sheets.md).  

> [!TIP]
> Sie können Arbeitszeittabellen auf einem mobilen Gerät verwenden. Dazu müssen Sie möglicherweise den Schalter **Neue Arbeitszeittabellenumgebung verwenden** auf der Seite [Ressourcen-Setup](https://businesscentral.dynamics.com/?page=462) aktivieren.

## Arbeitszeittabellen erstellen

Sie können die Seite **Arbeitszeittabellen erstellen** verwenden, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Nachdem eine Arbeitszeittabelle erstellt wurde, kann der Arbeitszeittabellenbesitzer sie öffnen und die Zeit aufzeichnen, die für eine Aufgabe benötigte wurde. Sie können auch [die automatische Ausführung des Stapelprojekts planen](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Sie müssen berechtigt sein, Arbeitszeittabellen zu erstellen. Um mehr über Berechtigungen zu erfahren, gehen Sie zu [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Arbeitszeittabellen erstellen** ein und wählen Sie dann den zugehörigen Link.

    > [!TIP]
    > Sie können die Aktion **Arbeitszeittabellen erstellen** auch auf der **Ressourcen**-Listenseite und der **Ressourcenkarte**-Seite verwenden.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Bevor Sie Stundenzettel für eine Ressource erstellen, stellen Sie sicher, dass die Felder **Arbeitszeitnachweis** und **Benutzer-ID des Arbeitszeittabellenbesitzers** aktiviert sind für auf der Seite **Ressourcenkarte** angegeben sind.

    Wählen Sie optional die Aktion **Zeitplan** aus, um anzugeben, wie oft die Aufgabe automatisch ausgeführt werden soll. Um beispielsweise die Aufgabe so zu konfigurieren, dass sie vier Wochen lang wöchentlich ausgeführt wird, legen Sie das Feld **Datumsformel für nächste Ausführung** auf der Seite **Bericht planen – Arbeitszeittabelle erstellen** auf **4W** fest. Weitere Informationen zur Planung von Berichten finden Sie unter [Bericht für die Ausführung planen](ui-work-report.md#ScheduleReport).  

Erstellen Sie auf der Seite **Arbeitszeittabellen** die erstellten Arbeitszeittabellen anzeigen. Jede Arbeitszeittabelle besteht aus mindestens einer Zeile, die die Zeit definiert, die Sie zur Genehmigung senden möchten. In der folgenden Tabelle werden die Zeilentypen beschrieben, die Sie der Arbeitszeittabelle hinzufügen können.

| **Feld** | **Beschreibung** |
|---|---|
| | Wird verwendet, um eine Notiz oder einen Marker im Feld **Beschreibung** der Arbeitszeittabellenzeile hinzuzufügen. Sie können dieses Feld beispielsweise verwenden, um Arbeitszeittabellenposten zu kategorisieren. Wenn Sie das Feld **Typ** in einer Arbeitszeittabelle leer lassen, können Sie keine Zeitwerte in den Wochentagsfeldern für diese Zeile eingeben. |
| Fehlzeit | Wird verwendet, um die Zeit zu erfassen, in der Sie in einer Arbeitswoche abwesend sind. Geben Sie die Art der Abwesenheit im Feld **Grund Abwesenheitscode** an, um die Informationen für die Zeile abzuschließen. |
| Montageauftrag | Wird verwendet, um die Zeit für Montageaufträge zu erfassen. Eine Arbeitszeittabelleposition wird beim Buchen von Montageauftragspositionen erstellt, für welche die Ressource für die Verwendung von Arbeitszeittabellen eingerichtet wurde. Sie können eine Zeile dieses Typs nicht manuell auswählen. |
| Projekt | Wird verwendet, um den Verbrauch für ein Projekt zu erfassen. Geben Sie die Projektnummer und die Projektaufgabennummer an, für die Sie die Zeit registrieren möchten, um die Informationen für die Zeile abzuschließen. Sie können Zeit für Zeilen eintragen, die Sie nicht geplant haben.|
| Ressource | Wird verwendet, um den Verbrauch für eine Ressource zu erfassen. Erstellen Sie eine Beschreibung der Arbeit, um die Informationen für die Zeile abzuschließen. |
| Service | Wird verwendet, um die Bearbeitungszeit für einen Serviceauftrag oder eine Servicegutschrift zu erfassen. |

Sie möchten beispielsweise eine Arbeitszeittabelle für eine Woche einreichen, in der Sie Reinigungsaufgaben erledigt haben und einen freien Tag für einen Arzttermin hatten. Die folgende Tabelle zeigt, wie Sie Zeilen zum Arbeitszeitnachweis hinzufügen würden.

| Typ | Description | Arbeitstypencode | Abwesenheitstypcode |
|--|--|--|--|
| Ressource | Arbeitszeit | Reinigung |  |
| Fehlzeit | Arbeitsfreie Zeit |  | Integrität |
|  | Ich musste am Dienstag wegen eines Arzttermins frei nehmen. |  |  |

In diesem hypothetischen Beispiel können Sie dann die relevanten Stunden über die relevanten Tage hinweg für die einzelnen Wochentage eintragen.  

> [!TIP]
> In den meisten Fällen verfügt Ihr Unternehmen über vordefinierte Arbeitstypen für die verschiedenen Zeilentypen. In diesen Fällen wählen Sie einfach den entsprechenden Arbeitstyp aus der Liste aus und fügen dann Ihre eigene Beschreibung hinzu.  
>
> Wählen Sie den Arbeitstyp aus, indem Sie die Schaltfläche :::image type="icon" source="media/assist-edit-icon.png" border="false"::: im Feld **Beschreibung** und die Aktion **Aktivitätsdetails** auswählen und ihn dann auf der Seite angeben, die geöffnet wird, oder indem Sie ihn im Feld **Arbeitstypcode** bzw. im Feld **Abwesenheitstypcode** auswählen. In diesem Fall können Sie den Abschnitt [So definieren Sie Arbeitstypen und fügen sie einer Arbeitszeittabelle hinzu](#define-work-types-and-add-one-to-a-time-sheet) ignorieren.  

## So können Sie Arbeitszeittabellenzeilen in anderen Arbeitszeittabellen wiederverwenden

Falls die Arbeitszeittabelleninformationen von einem Zeitraum zum nächsten gleich bleiben, kopieren Sie die Zeilen aus dem vorherigen Zeitraum, um Zeit zu sparen. Tragen Sie dann einfach Ihren Zeitverbrauch für den neuen Zeitraum ein.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Arbeitszeittabelle für eine Periode nach der Periode für eine vorhandene Arbeitszeittabelle mit Zeilen.  
3. Wählen Sie die Aktion **Zeilen aus vorherigen Arbeitszeittabellen kopieren** aus.

Die Zeilen werden kopiert, einschließlich Informationen wie Art und Beschreibung. Wenn beispielsweise die Zeile mit einem Projekt verknüpft ist, wird die **Projektnr.** kopiert. Alle kopierten Zeilen haben den Status **Offen**. Sie können die benutzerdefinierten Zeilen jetzt bei Bedarf ändern.

## Projektplanzeilen in eine Arbeitszeittabelle kopieren

Die folgende Vorgehensweise beschreibt, wie Projektplanzeilen einer Arbeitszeittabelle schnell hinzugefügt werden können.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Arbeitszeittabellen** eine Arbeitszeittabelle für den entsprechenden Zeitraum aus.  
3. Wählen Sie die Aktion **Zeilen anhand der Projektplanung erstellen** aus. Jegliche Projektplanzeilen im Arbeitszeittabellenzeitraum werden in die Arbeitszeittabelle für die Person oder die Maschine unter **Ressourcennummer** kopiert.

## Um Arbeitstypen festzulegen und einer Arbeitszeittabelle hinzufügen

Sie können den Arbeitstyp für alle Arbeitszeittabellenzeilen für Serviceaufträge, Projektaufträge und Ressourcen definieren. Auf diese Art können Sie Informationen hinzufügen, die Sie benötigen, um dem Debitor unterschiedliche Arten von Arbeit zu berechnen.  

1. Wählen Sie auf der Seite **Arbeitszeittabellen** die entsprechende Arbeitszeittabelle aus.
2. Wählen Sie in der ersten Zeile im Abschnitt **Zeilen** das Feld **Typ** und dann den entsprechenden Typ aus, z. B. *Ressource*.  
3. Wählen Sie das Feld **Beschreibung** aus, und füllen Sie anschließend die Felder auf der Seite **Arbeitszeittabellenzeile - Ressourcendetails** aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Wenn keine Arbeitstypen vorhanden sind, wählen Sie die Aktion **Neu** aus.
    2. Füllen Sie die Felder auf der Seite **Arbeitstypen** nach Bedarf aus, und kehren Sie dann zur Arbeitszeittabelle zurück.
4. Füllen Sie den Rest der Arbeitszeittabelle aus. Weitere Informationen finden Sie im Abschnitt [So füllen Sie Arbeitszeittabellen aus und senden sie zur Genehmigung](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Sie können ähnlich vorgehen, um Abwesenheitscodes festzulegen.

## So können Sie Arbeitszeittabellenzeilen ausfüllen und zur Genehmigung senden

Die Arbeitszeittabellenregistrierung wird in Stunden verfolgt, der Standard-Basiseinheit für Ressourcen. Standardmäßig zeigt eine Arbeitszeittabelle die allgemeinen Arbeitstage von Montag bis Freitag an.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein Arbeitszeitblatt für den entsprechenden Zeitraum aus.
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. Geben Sie die Anzahl der Stunden ein, die von der Ressource an jedem Wochentag verwendet werden.  

    In den meisten Fällen fügen Sie zum Nachverfolgen der Arbeit eine Zeile vom Typ *Ressource* hinzu und erfassen anschließend die täglich aufgewendeten Stunden. Wenn Sie Abwesenheit erfassen möchten, fügen Sie eine Zeile vom Typ *Abwesenheit* hinzu.  

    > [!TIP]  
    > Sie können die Summe der Arbeitszeittabellenstunden überprüfen, die in die Infobox **Zusammenfassung tatsächlich/budgetiert** eingetragen sind.  
4. Wiederholen Sie Schritt 3 für weitere Arbeitstypen, die die Ressource ausführt.  

    Entscheiden Sie im nächsten Schritt, ob Sie alle oder ausgewählte Zeilen in der Arbeitszeittabelle einreichen möchten.  

    * Wählen Sie die entsprechende Zeile und dann die Aktion **Übermitteln** aus, um den Stundenzettel für eine oder mehrere Zeilen zu übermitteln.

        Wählen Sie auf der Übermittlungsseite die Option **Nur ausgewählte Zeilen** aus. Die Zeile ändert den Status von **Offen** in **Übermittelt**.
    * Wählen Sie die Aktion **Übermitteln** oben auf der Seite **Arbeitszeittabelle** aus, um die Arbeitszeittabelle für alle offenen Zeilen zu übermitteln.  

        Bestätigen Sie, dass Sie alle offenen Zeilen der aktuellen Arbeitszeittabelle übermitteln möchten.  

    > [!NOTE]  
    > ie können nur Arbeitszeitta‎bellenzeilen senden, für die Sie Zeit eingegeben haben.  
5. Um Informationen in einer Zeile zu ändern, die auf **Übermittelt** festgelegt wurde, wählen Sie die Zeile und wählen Sie dann die Aktion **Erneut öffnen** aus.

    > [!NOTE]  
    > Ein Manager weist möglicherweise eine Arbeitszeittabellenzeile zurück, die zur Genehmigung eingesendet wird. Wenn eine Zeile den Status **Abgelehnt** hat, können Sie an der Zeile Änderungen vornehmen und dann erneut **Übermitteln** wählen.  
6. Wählen Sie die Schaltfläche **OK**.

## Arbeitszeittabellen genehmigen oder ablehnen

Eine Arbeitszeittabelle muss zur Genehmigung eingereicht werden, bevor Sie verwendet wird. Sie können einzelne Zeilen in der Arbeitszeittabelle genehmigen oder ablehnen und sie wieder an den Antragsteller senden. Eine Arbeitszeittabelle kann auf zwei Arten genehmigt werden:

* Ein Arbeitszeittabellenadministrator kann jede Arbeitszeittabelle genehmigen.
* Die Person, die im Feld **Arbeitszeittabellen-Genehmiger Benutzer-ID** in einer Ressourcenkarte angegeben wird, kann die Arbeitszeittabellen dieser Ressource genehmigen. Weitere Informationen zum Einrichten von Genehmigungen finden Sie unter [Arbeitszeittabellen einrichten](projects-how-setup-time-sheets.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen für Manager** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Arbeitszeittabelle aus der Liste aus.  
3. Führen Sie auf der Seite **Arbeitszeitblatt** die folgenden Schritte aus: 
    1. Wählen Sie die Aktion **Verarbeiten** und dann die Aktion **Genehmigen** aus.
    2. Wählen Sie die Aktion **Alle übermittelten Zeilen** aus, um alle Zeilen zu genehmigen, oder wählen Sie die Aktion **Alle offenen Zeilen** aus, um nur die Zeilen zu genehmigen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus.  
5. Wählen Sie die Aktion **Ablehnen** und führen Sie die Schritte 4 bis 5 aus.  

> [!TIP]  
> Verwenden Sie die Infoboxen **Arbeitszeittabellenstatus** uns **Tatsächliche/Geplante Zusammenfassung** aus, um einen schnellen Überblick zu Arbeitszeittabelleninformationen zu erhalten.

Nachdem Sie eine Arbeitszeittabelle genehmigt oder abgelehnt haben, kann sie nicht mehr bearbeitet werden, wenn sie nicht zuerst wieder geöffnet wird. Verwenden Sie das folgende Vorgehen, um eine genehmigte oder zurückgewiesene Arbeitszeittabelle erneut zu öffnen.

## Eine Arbeitszeittabelle erneut öffnen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen für Manager** oder **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.
2. Öffnet eine Arbeitszeittabelle aus der Liste.  

    > [!NOTE]  
    > Sie können Zeilen nur erneut öffnen, die den Status **Genehmigt** haben. Sie können keine Zeilen erneut öffnen, die den Status **Abgelehnt** haben oder gebucht wurden.  
3. Wählen Sie auf der Seite **Erneut öffnen** die Aktion **Genehmigen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen erneut zu öffnen oder **Nur ausgewählte Zeilen**, um nur jene Zeilen erneut zu öffnen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus. Der Status der Arbeitszeittabellen, Zeile oder Zeilen wechselt auf **Übermittelt**.  

## Arbeitszeittabellen nach Projekt anzeigen und diese genehmigen

Für ein Projekt können Sie eine Person bestimmen, die für das Projekt verantwortlich ist. Diese Informationen sind mit Stundenzettelzeilen verknüpft. Über den Link erhalten Projektmanager eine Liste der zu genehmigenden Stundennachweise. Beispielsweise ist der Team-Projekt-Manager möglicherweise für bestimmte Projekte in Ihrem Unternehmen verantwortlich. In diesem Fall sollte der Manager als die **Verantwortliche Person** auf der Projektkartenseite festgelegt sein. In dieser Ansicht der Arbeitszeittabelleninformationen, können Sie die Projektaufgaben sehen, die einem Projekt zugeordnet sind, und die verwendete Stundenmenge.

> [!NOTE]
> Um Arbeitszeittabellen auf der Seite **Arbeitszeittabelle für Manager nach Projekt** genehmigen zu können, müssen Sie zuerst eine Option **Arbeitszeittabelle nach Projektgenehmigung** auf der Seite **Ressourceseinrichtung** auswählen. Weitere Informationen zu Genehmigungen für Ressourcen finden Sie unter [Ressourcen einrichten](projects-how-setup-resources.md).

### Arbeitszeittabellen nach Projekt genehmigen oder ablehnen

1. Geben Sie im Feld **Suchen** **Arbeitszeittabelle für Manager nach Projekt** ein, und wählen Sie dann den zugehörigen Link aus. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt eine Liste der Arbeitszeittabellezeilen an, die den Projekten zugeordnet sind, für die Sie verantwortlich sind.
2. Wählen Sie die Aktion **Genehmigen** und dann die Aktion **Alle übermittelten Zeilen** aus, um alle Zeilen zu genehmigen, oder wählen Sie die Aktion **Nur ausgewählte Zeilen** aus, um nur die Zeilen zu genehmigen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.

    > [!NOTE]
    > Sie können nur Arbeitszeittabellen mit dem Status **Übermittelt** genehmigen.

3. Um zusätzliche Informationen zur Genehmigung oder Ablehnung anzugeben, wählen Sie die Aktion **Zugehörig**, dann **Kommentare** und anschließend **Zeilenkommentare** aus.
4. Wählen Sie die Schaltfläche **OK**.

> [!NOTE]
> Nachdem Sie eine Arbeitszeittabellenzeile nach Projekt genehmigt oder abgelehnt haben, können Sie sie auf der Seite **Arbeitszeittabelle** nicht wieder öffnen oder ändern.

## Buchen von Arbeitszeittabellenzeilen zu einem Ressourcen-Buch.-Blatt

Nachdem Sie Arbeitszeittabellenposten für eine Ressource genehmigt haben, können Sie sie in das entsprechende Ressourcen-Buch.-Blatt buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie auf der Seite **Ressourcen Buch.-Blattzeilen vorschlagen** die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Wählen Sie die Schaltfläche **OK**. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Ressourcen-Buch.-Blatt** öffnet sich und die Ergebnisses der Buchung des Ressourcen Buch.-Blattes werden angezeigt.

## Buchen von Arbeitszeittabellenzeilen zu einem Projekt-Buch.-Blatt

Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das entsprechende Projekt-Buch.-Blatt buchen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekterfassungen** ein und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie auf der Seite **Projekt Buchungsblattzeilen vorschlagen** die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Wählen Sie die Schaltfläche **OK** aus. Einträge für Verbrauch werden im Projekt-Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  

    > [!NOTE]  
    > Informationen über den Arbeitstyp und darüber, ob die Arbeit fakturierbar ist, werden aus der Arbeitszeittabellenzeile kopiert. Bei Bedarf können Sie die Anzahl der Stunden reduzieren und eine Teilbuchung durchführen. Wenn Sie die Anzahl reduzieren, dann wird bei der nächsten Auswahl von **Zeilen anhand von Arbeitszeittabellen vorschlagen** eine Zeile mit der Restmenge der Stunden erstellt.  
5. Wählen Sie die Aktion **Buchen**.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Projektposten** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen-Buch.-Blattes.

## Arbeitszeitnachweise archivieren

Nachdem Sie Arbeitszeittabellen gebucht haben, können Sie diese für spätere Bezugnahme archivieren. Sie müssen alle Zeilen auf einer Arbeitszeittabelle buchen, bevor Sie sie archivieren können.

> [!NOTE]  
> Wenn Sie eine Arbeitszeittabelle archivieren, wird sie aus der Seite **Arbeitszeittabelle** und aus der Seite **Arbeitszeittabelle für Manager** entfernt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Arbeitszeittabellen in Archiv verschieben** aus.  
3. Füllen Sie auf der Seite **Arbeitszeittabellen in Archiv verschieben** die Felder nach Bedarf aus, und wählen Sie dann die Schaltfläche **OK** aus.  
4. Um archivierte Arbeitszeittabellen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus. Symbol. Geben Sie **Archiv für Arbeitszeittabellen** oder **Archiv für Arbeitszeittabellen für Manager** ein und wählen Sie dann den zugehörigen Link.

## Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Einrichten des Projektmanagements](projects-setup-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]