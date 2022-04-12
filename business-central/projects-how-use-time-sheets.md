---
title: Arbeitszeittabellen verwenden
description: Beschreibt, wie Sie eine Arbeitszeittabelle erstellen, Arbeitstypen definieren, Arbeitszeittabellen ausfüllen und sie zur Genehmigung senden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.search.form: 950, 951, 973
ms.date: 03/01/2022
ms.author: edupont
ms.openlocfilehash: 1ed54a63f3747d9ea5a1010206f4faac74fa90b0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510855"
---
# <a name="use-time-sheets"></a>Arbeitszeittabellen verwenden

Mit Arbeitszeittabellen in [!INCLUDE [prod_short](includes/prod_short.md)] können Sie Abwesenheit sowie Zeit und Ressourcen verfolgen, die für ein Projekt aufgewendet werden. Mit dem Zeitmanagement können Sie Probleme früh identifizieren und Verzögerungen oder Kostenüberschreitungen vermeiden. Mit Arbeitszeittabellen kann eine Ressource den Zeitverbrauch für eine Mitarbeiter oder einen Arbeitsplatz enfach melden, und ein Manager kann den Verbrauch und die Verteilung einfach überprüfen. In diesem Artiekl wird beschrieben, wie Sie eine Arbeitszeittabelle erstellen, Arbeitstypen definieren, Arbeitszeittabellen ausfüllen und sie zur Genehmigung senden.  

Sie können Ihre Projektplanzeilen in die Arbeitszeittabelle kopieren und verwenden. Auf diese Art müssen Sie die Informationen immer nur an einer Stelle eingeben und die Zeileninformationen sind immer korrekt.

Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das entsprechende Projektjournal oder Ressourcen-Journal buchen.

Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie Informationen einrichten und einen Administrator und mindestens einen Genehmiger für Arbeitszeittabellen festlegen. Weitere Informationen finden Sie unter [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).  

> [!TIP]
> Ab dem Veröffentlichungszyklus 2 von 2021 können Sie zugewiesene Arbeitszeittabellen auf einem mobilen Gerät verwalten. Ihr Administrator muss jedoch möglicherweise die Funktion **Funktionsupdate: Neue Erfahrung mit Arbeitszeittabellen** auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren, um diese Funktionalität nutzen zu können. Weitere Informationen finden Sie unter [Zeittabellen festlegen](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets"></a>So erstellen Sie Arbeitszeittabellen

Sie können die Stapelverarbeitung **Arbeitszeittabellen erstellen** verwenden, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Nachdem eine Arbeitszeittabelle erstellt wurde, kann der Arbeitszeittabellenbesitzer sie öffnen und die Zeit aufzeichnen, die für eine Aufgabe benötigte wurde. Sie können auch [die automatische Ausführung der Stapelverarbeitung planen](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Sie müssen Berechtigungen haben, Arbeitszeittabellen zu erstellen. Weitere Informationen finden Sie unter [Zeittabellen festlegen](projects-how-setup-time-sheets.md).

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Arbeitszeittabellen** die Aktion **Arbeitszeittabellen erstellen** aus.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Die Felder **Arbeitszeittabellen** verwenden und **Arbeitszeittabellenbesitzer-Benutzer-ID** müssen auf der Karte der Arbeitszeittabelle für die Ressource ausgefüllt werden.

    Wählen Sie optional die Aktion **Zeitplan** aus, um anzugeben, wie oft die Aufgabe automatisch ausgeführt werden soll. Um beispielsweise die Aufgabe so zu konfigurieren, dass sie vier Wochen lang wöchentlich ausgeführt wird, legen Sie das Feld **Datumsformel für nächste Ausführung** auf der Seite **Bericht planen – Arbeitszeittabelle erstellen** auf *4W* fest. Weitere Informationen finden Sie unter [Bericht für die Ausführung planen](ui-work-report.md#ScheduleReport).  
4. Wählen Sie die Schaltfläche **OK**.  

Auf der Seite **Arbeitszeittabellen** können Sie die erstellten Arbeitszeittabellen anzeigen. Jede Arbeitszeittabelle besteht aus mindestens einer Zeile, die die Zeit definiert, die Sie zur Genehmigung senden möchten. In der folgenden Tabelle werden die Zeilentypen beschrieben, die Sie der Arbeitszeittabelle hinzufügen können.

| **Feld** | **Beschreibung** |
|---|---|
| | Wird verwendet, um eine Notiz oder einen Marker im Feld **Beschreibung** der Arbeitszeittabellenzeile hinzuzufügen. Sie können dieses Feld beispielsweise verwenden, um Arbeitszeittabellenposten zu kategorisieren. Wenn Sie das Feld **Typ** in einer Arbeitszeittabelle leer lassen, können Sie keine Zeitwerte in den Wochentagsfeldern für diese Zeile eingeben. |
| Fehlzeit | Wird verwendet, um die Zeit zu erfassen, in der Sie in einer Arbeitswoche abwesend sind. Geben Sie die Art der Abwesenheit im Feld **Grund Abwesenheitscode** an, um die Informationen für die Zeile abzuschließen. |
| Montageauftrag | Wird verwendet, um die Zeit für Montageaufträge zu erfassen. Eine Arbeitszeittabelle wird beim Buchen von Montageauftragszeilen erstellt, für die die Ressource für die Verwendung von Arbeitszeittabellen eingerichtet wurde. Sie können eine Zeile dieses Typs nicht manuell auswählen. |
| Projekt | Wird verwendet, um den Verbrauch für ein Projekt zu erfassen. Geben Sie die Projektnummer und die Projektaufgabennummer an, für die Sie die Zeit registrieren möchten, um die Informationen für die Zeile abzuschließen. Sie können Zeit für Zeilen eintragen, die Sie nicht geplant haben.|
| Ressource | Wird verwendet, um den Verbrauch für eine Ressource zu erfassen. Erstellen Sie eine Beschreibung der Arbeit, um die Informationen für die Zeile abzuschließen. |
| Service | Wird verwendet, um die Bearbeitungszeit für einen Serviceauftrag oder eine Servicegutschrift zu erfassen. |

Wenn Sie beispielsweise eine Arbeitszeittabelle für eine Arbeitswoche einreichen möchten, in der Sie an den meisten Tagen mit Reinigungsaufgaben beschäftigt waren, aber aufgrund von Arztterminen einen freien Tag hatten, können Sie Zeilen wie in der folgenden Tabelle veranschaulicht hinzufügen.

| Typ | Beschreibung | Arbeitstypcode | Abwesenheitstypcode |
|--|--|--|--|
| Ressource | Arbeitszeit | Reinigung |  |
| Fehlzeit | Arbeitsfreie Zeit |  | Integrität |
|  | Ich musste am Dienstag wegen eines Arzttermins frei nehmen. |  |  |

In diesem hypothetischen Beispiel würden Sie dann die relevanten Stunden über die relevanten Tage hinweg in die Felder für jeden Wochentag eintragen.  

> [!TIP]
> In den meisten Fällen verfügt Ihr Unternehmen über vordefinierte Arbeitstypen für die verschiedenen Zeilentypen. In diesen Fällen wählen Sie einfach den entsprechenden Arbeitstyp aus der Liste aus und fügen dann Ihre eigene Beschreibung hinzu.  
>
> Wählen Sie den Arbeitstyp aus, indem Sie die Schaltfläche „:::image type="icon" source="media/assist-edit-icon.png" border="false":::“ im Feld **Beschreibung** und die Aktion **Aktivitätsdetails** auswählen und ihn dann auf der Seite angeben, die geöffnet wird, oder indem Sie ihn im Feld **Arbeitstypcode** bzw. im Feld **Abwesenheitstypcode** auswählen. In diesem Fall können Sie den Abschnitt [So definieren Sie Arbeitstypen und fügen sie einer Arbeitszeittabelle hinzu](#to-define-work-types-and-add-one-to-a-time-sheet) ignorieren.  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>So können Sie Arbeitszeittabellenzeilen in anderen Arbeitszeittabellen wiederverwenden

Falls die Arbeitszeittabelle Informationen von einem Zeitraum zum anderen gleich bleiben, können Sie Zeit sparen, indem Sie die Zeilen aus dem vorherigen Zeitraum kopieren. Tragen Sie dann einfach Ihren Zeitverbrauch für die neuen Periode ein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Arbeitszeittabelle für eine Periode nach der Periode für eine vorhandene Arbeitszeittabelle mit Zeilen.  
3. Wählen Sie die Aktion **Zeilen aus vorherigen Arbeitszeittabellen kopieren** aus.

Die Zeilen werden kopiert, einschließlich Informationen wie Art und Beschreibung. Wenn beispielsweise die Zeile mit einem Projekt verknüpft ist, wird die **Projektnr.** kopiert. Alle kopierten Zeilen haben den Status **Offen**. Sie können die benutzerdefinierten Zeilen jetzt bei Bedarf ändern.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>So kopieren Sie Projektplanzeilen in eine Arbeitszeittabelle:
Die folgende Vorgehensweise beschreibt, wie Projektplanzeilen einer Arbeitszeittabelle enfach hinzugefügt werden können.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Arbeitszeittabellen** eine Arbeitszeittabelle für den entsprechenden Zeitraum aus.  
3. Wählen Sie die Aktion **Zeilen von Projektplanung erstellen** aus. Jegliche Projektplanzeilen im Arbeitszeittabellenzeitraum werden in die Arbeitszeittabelle für die Person oder die Maschine unter **Ressourcennummer** kopiert.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Um Arbeitstypen festzulegen und einer Arbeitszeittabelle hinzufügen

Sie können den Arbeitstyp für alle Arbeitszeittabellenzeilen für Serviceaufträge, Projektaufträge und Ressourcen definieren. Auf diese Art können Sie Informationen hinzufügen, die Sie benötigen, um dem Debitor unterschiedliche Arten von Arbeit zu berechnen.  

1. Wählen Sie auf der Seite **Arbeitszeittabellen** die entsprechende Arbeitszeittabelle aus.
2. Wählen Sie in der ersten Zeile im Abschnitt **Zeilen** das Feld **Typ** und dann den entsprechenden Typ aus, z. B. *Ressource*.  
3. Wählen Sie das Feld **Beschreibung** aus, und füllen Sie anschließend die Felder auf der Seite **Arbeitszeittabellenzeile - Ressourcendetails** aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Wenn keine Arbeitstypen vorhanden sind, wählen Sie die Aktion **Neu** aus.
    2. Füllen Sie die Felder auf der Seite **Arbeitstypen** nach Bedarf aus, und kehren Sie dann zur Arbeitszeittabelle zurück.
4. Füllen Sie den Rest der Arbeitszeittabelle aus. Weitere Informationen finden Sie im Abschnitt [So füllen Sie Arbeitszeittabellen aus und senden sie zur Genehmigung](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Ähnliche Schritte gelten für die Definition von Abwesenheitscodes.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>So können Sie Arbeitszeittabellenzeilen ausfüllen und zur Genehmigung senden

Die Arbeitszeittabellenregistrierung wird in Stunden verfolgt, der Standard-Basiseinheit für Ressourcen. Standardmäßig zeigt eine Arbeitszeittabelle die allgemeinen Arbeitstage von Montag bis Freitag an.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein Arbeitszeitblatt für den entsprechenden Zeitraum aus.
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. Geben Sie die Anzahl der Stunden ein, die von der Ressource an jedem Wochentag verwendet werden.  

    In den meisten Fällen fügen Sie zum Verfolgen der Arbeit eine Zeile vom Typ *Ressource* hinzu und registrieren anschließend die täglich aufgewendeten Stunden. Wenn Sie Abwesenheit registrieren möchten, fügen Sie eine Zeile vom Typ *Abwesenheit* hinzu.  

    > [!TIP]  
    > Sie können die Summe der Arbeitszeittabellenstunden überprüfen, die Sie in die Infobox **Tatsächlich/Budgetiert Zusammenfassung** eingegeben haben.  
4. Wiederholen Sie Schritt 3 für weitere Arbeitstypen, die die Ressource ausführt.  

    Als nächstes müssen Sie entscheiden, ob Sie alle Zeilen der Arbeitszeittabelle oder einzelne Zeilen senden möchten.  

    * Wählen Sie die entsprechende Zeile und dann die Aktion **Übermitteln** aus, um den Stundenzettel für eine oder mehrere Zeilen zu übermitteln.

        Wählen Sie auf der Übermittlungsseite die Option **Nur ausgewählte Zeilen** aus. Die Zeile ändert den Status von *Offen* in *Übermittelt*.
    * Wählen Sie die Aktion **Übermitteln** oben auf der Seite **Arbeitszeittabelle** aus, um die Arbeitszeittabelle für alle offenen Zeilen zu übermitteln.  

        Sie werden aufgefordert, zu bestätigen, dass Sie alle offenen Zeilen in der aktuellen Arbeitszeittabelle übermitteln möchten.  

    > [!NOTE]  
    > ie können nur Arbeitszeitta‎bellenzeilen senden, für die Sie Zeit eingegeben haben.  
5. Um Informationen in einer Zeile zu ändern, die auf **Übermittelt** festgelegt wurde, wählen Sie die Zeile und wählen Sie dann die Aktion **Erneut öffnen** aus.

    > [!NOTE]  
    >   Ein Manager weist möglicherweise eine Arbeitszeittabellenzeile zurück, die zur Genehmigung eingesendet wird. Wenn eine Zeile den Status **Abgelehnt** hat, können Sie an der Zeile Änderungen vornehmen und dann erneut **Übermitteln** wählen.  
6. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-approve-or-reject-a-time-sheet"></a>So können Sie Arbeitszeittabellen genehmigen und ablehnen:
Eine Arbeitszeittabelle muss zur Genehmigung eingereicht werden, bevor Sie verwendet wird. Sie können einzelne Zeilen in der Arbeitszeittabelle genehmigen oder ablehnen und sie wieder an den Antragsteller für zusätzliche Aktion senden. Eine Arbeitszeittabelle kann auf zwei Arten genehmigt werden:

* Ein Arbeitszeittabellenadministrator kann jede Arbeitszeittabelle genehmigen.
* Die Person, die im Feld **Arbeitszeittabellen-Genehmiger Benutzer-ID** in einer Ressourcenkarte angegeben wird, kann die Arbeitszeittabellen dieser Ressource genehmigen. Weitere Informationen finden Sie unter [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen für Manager** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Arbeitszeittabelle aus der Liste aus.  
3. Führen Sie auf der Seite **Arbeitszeitblatt** die folgenden Schritte aus: 
    1. Wählen Sie die Aktion **Verarbeiten** und dann die Aktion **Genehmigen** aus.
    2. Wählen Sie die Aktion **Alle übermittelten Zeilen** aus, um alle Zeilen zu genehmigen, oder wählen Sie die Aktion **Alle offenen Zeilen** aus, um nur die Zeilen zu genehmigen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus.  
5. Wählen Sie die Aktion **Ablehnen** und führen Sie die Schritte 4 bis 5 aus.  

> [!TIP]  
>   Verwenden Sie die Infoboxen **Arbeitszeittabellenstatus** uns **Tatsächliche/Geplante Zusammenfassung** aus, um einen schnellen Überblick zu Arbeitszeittabelleninformationen zu erhalten.

Nachdem Sie eine Arbeitszeittabelle genehmigt oder abgelehnt haben, kann sie nicht mehr bearbeitet werden, außer wenn sie zuerst wieder geöffnet wird. Verwenden Sie das folgende Vorgehen, um eine genehmigte oder zurückgewiesene Arbeitszeittabelle erneut zu öffnen.

## <a name="to-reopen-a-time-sheet"></a>So öffnen Sie eine Arbeitszeittabelle erneut:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen für Manager** oder **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.
2. Öffnet eine Arbeitszeittabelle aus der Liste.  

    > [!NOTE]  
    >   Sie können Zeilen nur erneut öffnen, die den Status **Genehmigt** haben. Sie können keine Zeilen erneut öffnen, die den Status **Abgelehnt** haben. Sie können eine Arbeitszeittabelle nicht erneut öffnen, wenn diese gebucht wurde.  
3. Wählen Sie auf der Seite **Erneut öffnen** die Aktion **Genehmigen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen erneut zu öffnen oder **Nur ausgewählte Zeilen**, um nur jene Zeilen erneut zu öffnen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus. Der Status der Arbeitszeittabellen, Zeile oder Zeilen wechselt auf **Übermittelt**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>So zeigen Sie Arbeitszeittabellen nach Projekt an und genehmigen diese

Für ein Projekt können Sie eine Person bestimmen, die für das Projekt verantwortlich ist. Diese Information wird mit den Arbeitszeittabellenzeilen verknüpft und kann verwendet werden, um eine Liste der Arbeitszeittabellen bereitzustellen, die ein Projekt-Manager überprüfen und genehmigen muss. Beispielsweise ist der Team-Projekt-Manager möglicherweise für bestimmte Projekte in Ihrem Unternehmen verantwortlich. In diesem Fall sollte der Manager als die **Verantwortliche Person** auf der Projektkarte festgelegt sein. In dieser Ansicht der Arbeitszeittabelleninformationen, können Sie die Projektaufgaben sehen, die einem Projekt zugeordnet sind, und die verwendete Stundenmenge.

> [!NOTE]
> Um Arbeitszeittabellen im Fenster **Arbeitszeittabelle für Manager nach Projekt** genehmigen zu können, müssen Sie zuerst eine Option **Arbeitszeittabelle nach Projektgenehmigung** auf der Seite **Ressourceseinrichtung** auswählen. Weitere Informationen finden Sie unter [Ressourcen einrichten](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>So können Sie Arbeitszeittabellen nach Projekt genehmigen oder ablehnen

1. Geben Sie im Feld **Suchen** **Arbeitszeittabelle für Manager nach Projekt** ein, und wählen Sie dann den zugehörigen Link aus. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt eine Liste der Arbeitszeittabellezeilen an, die den Projekten zugeordnet sind, für die Sie verantwortlich sind.
2. Wählen Sie die Aktion **Genehmigen** und dann die Aktion **Alle übermittelten Zeilen** aus, um alle Zeilen zu genehmigen, oder wählen Sie die Aktion **Nur ausgewählte Zeilen** aus, um nur die Zeilen zu genehmigen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.

    > [!NOTE]
    > Sie können nur Arbeitszeittabellen genehmigen, die den Status **Übermittelt** haben.

3. Um zusätzliche Informationen zur Genehmigung oder Ablehnung anzugeben, wählen Sie die Aktion **Zugehörig**, dann **Kommentare** und anschließend **Zeilenkommentare** aus, und geben Sie Kommentare ein.
4. Wählen Sie die Schaltfläche **OK**.

> [!NOTE]
> Nachdem Sie eine Arbeitszeittabellenzeile nach Projekt genehmigt oder abgelehnt haben, kann sie im Fenster **Arbeitszeittabelle** nicht erneut geöffnet oder geändert werden.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Buchen von Arbeitszeittabellenzeilen zu einem Ressourcen-Buch.-Blatt
Nachdem Sie Arbeitszeittabellenposten für eine Ressource genehmigt haben, können Sie sie in das entsprechende Ressourcen-Buch.-Blatt buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie auf der Seite **Ressourcen Buch.-Blattzeilen vorschlagen** die Felder nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK**. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Ressourcen-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Buchen von Arbeitszeittabellenzeilen in einem Ressourcen-Buch.-Blatt
Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das Projektbuchungsblatt des entsprechenden Projekts buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie auf der Seite **Projekt Buch.-Blattzeilen vorschlagen** die Felder nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK**. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  

    > [!NOTE]  
    >   Informationen über den Arbeitstyp und darüber, ob die Arbeit fakturierbar ist, werden aus der Arbeitszeittabellenzeile kopiert. Bei Bedarf können Sie die Anzahl der Stunden reduzieren und eine Teilbuchung durchführen. Wenn Sie die Anzahl reduzieren, dann wird bei der nächsten Auswahl von **Zeilen anhand von Arbeitszeittabellen vorschlagen** eine Zeile mit der Restmenge der Stunden erstellt.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Projekt-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## <a name="to-archive-time-sheets"></a>So archivieren Sie Arbeitszeittabellen
Nachdem Sie Arbeitszeittabellen gebucht haben, können Sie diese für spätere Bezugnahme archivieren. Alle Arbeitszeittabellenzeilen müssen gebucht werden, bevor eine Arbeitszeittabelle archiviert werden kann.

> [!NOTE]  
>   Wenn Sie eine Arbeitszeittabelle archivieren, wird sie aus der Seite **Arbeitszeittabelle** und aus der Seite **Arbeitszeittabelle für Manager** entfernt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Arbeitszeittabellen in Archiv verschieben** aus.  
3. Füllen Sie auf der Seite **Arbeitszeittabellen in Archiv verschieben** die Felder nach Bedarf aus, und wählen Sie dann die Schaltfläche **OK** aus.  
4. Um archivierte Arbeitszeittabellen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus. Symbol. Geben Sie **Archiv für Arbeitszeittabellen** oder **Archiv für Arbeitszeittabellen für Manager** ein und wählen Sie dann den zugehörigen Link.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Projektmanagement einrichten](projects-setup-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]