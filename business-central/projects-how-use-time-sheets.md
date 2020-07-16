---
title: Arbeitszeittabellen nutzen für Projekte| Microsoft Docs
description: Beschreibt, wie Sie eine Arbeitszeittabelle für ein Projekt erstellen, Planungszeilen kopieren, Arbeitstypen definieren, Arbeitszeittabellen ausfüllen und sie zur Genehmigung senden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/22/2020
ms.author: sgroespe
ms.openlocfilehash: 36405d80a021e6d3675a20c0283421c49aabd23b
ms.sourcegitcommit: 1ab077a024fa71d97ac70e4b36cc218b7ca66509
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "3499566"
---
# <a name="use-time-sheets-for-jobs"></a>Verwenden von Arbeitszeittabellen für Projekte

Verwenden Sie die Stapelverarbeitung **Arbeitszeittabellen erstellen**, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Sie müssen Berechtigungen haben, Arbeitszeittabellen zu erstellen.

Sie können Ihre Projektplanzeilen in die Arbeitszeittabelle kopieren und verwenden. Auf diese Art müssen Sie die Informationen immer nur an einer Stelle eingeben und die Zeileninformationen sind immer korrekt.

Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das entsprechende Projektjournal oder Ressourcen-Journal buchen.

Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie Informationen einrichten und einen Administrator und mindestens einen Genehmiger für Arbeitszeittabellen festlegen. Weitere Informationen finden Sie unter [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Arbeitszeittabellen erstellen

Sie können die Stapelverarbeitung **Arbeitszeittabellen erstellen** verwenden, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Nachdem eine Arbeitszeittabelle erstellt wurde, kann der Arbeitszeittabellenbesitzer sie öffnen und die Zeit aufzeichnen, die für eine Aufgabe benötigte wurde.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Arbeitszeittabellen-Liste** wählen Sie die Aktion **Arbeitszeittabellen erstellen** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Die Felder **Arbeitszeittabellen** verwenden und **Arbeitszeittabellenbesitzer-Benutzer-ID** müssen auf der Karte der Arbeitszeittabelle für die Ressource ausgefüllt werden.
4. Wählen Sie die Schaltfläche **OK** aus.  

Auf der Seite **Liste Arbeitszeittabelle** können Sie die erstellten Arbeitszeittabellen anzeigen.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>So kopieren Sie Projektplanzeilen in eine Arbeitszeittabelle:
Die folgende Vorgehensweise beschreibt, wie Projektplanzeilen einer Arbeitszeittabelle enfach hinzugefügt werden können.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Arbeitszeittabellen-Liste** wählen Sie eine Arbeitszeittabelle für den entsprechenden Zeitraum aus und wählen Sie dann die Aktion **Arbeitszeittabelle bearbeiten** aus.  
3. Wählen Sie die Aktion **Zeilen von Projektplanung erstellen** aus. Jegliche Projektplanzeilen im Arbeitszeittabellenzeitraum werden in die Arbeitszeittabelle für die Person oder die Maschine unter **Ressourcennummer** kopiert.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Um Arbeitstypen festzulegen und einer Arbeitszeittabelle hinzufügen
Sie können den Arbeitstyp für alle Arbeitszeittabellenzeilen für Projekte festlegen. Auf diese Art können Sie Informationen hinzufügen, die Sie benötigen, um dem Debitor unterschiedliche Arten von Arbeit zu berechnen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den entsprechenden Link.   
2. Öffnet die entsprechende Arbeitszeittabelle.
3. Wählen Sie das Feld **Beschreibung**.  
4. Auf der Seite **Arbeitszeittabellenzeilen-Projekt-Detail** wählen Sie das Feld **Arbeitstypencode** und wählen Sie einen Arbeitstyp aus der Liste aus, wie beispielsweise **Meilen**.  
5. Wenn keine Arbeitstypen vorhanden sind, wählen Sie die Aktion **Neu** aus.
6. Auf der Seite **Arbeitstypen** füllen Sie die notwendigen Felder aus.
7. Wiederholen Sie Schritt 4, um den neuen Arbeitstyp in der Arbeitszeittabelle einzugeben.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>So können Sie Arbeitszeittabellenzeilen in anderen Arbeitszeittabellen wiederverwenden
Falls die Arbeitszeittabelle Informationen von einem Zeitraum zum anderen gleich bleiben, können Sie Zeit sparen, indem Sie die Zeilen aus dem vorherigen Zeitraum kopieren. Tragen Sie dann einfach Ihren Zeitverbrauch für die neuen Periode ein.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die Arbeitszeittabelle für eine Periode nach der Periode für eine vorhandene Arbeitszeittabelle mit Zeilen.  
3. Wählen Sie die Aktion **Zeilen aus vorherigen Arbeitszeittabellen kopieren** aus.

Die Zeilen werden kopiert, einschließlich Informationen wie Art und Beschreibung. Wenn beispielsweise die Zeile mit einem Projekt verknüpft ist, wird die **Projektnr.** kopiert. Alle kopierten Zeilen haben den Status **Offen**. Sie können die benutzerdefinierten Zeilen jetzt bei Bedarf ändern.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>So können Sie Arbeitszeittabellenzeilen ausfüllen und zur Genehmigung senden
Die Arbeitszeittabellenregistrierung wird in Stunden verfolgt, der Standard-Basiseinheit für Ressourcen. Standardmäßig zeigt eine Arbeitszeittabelle die allgemeinen Arbeitstage von Montag bis Freitag an.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeittabellen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie eine Arbeitszeittabelle für den entsprechenden Zeitraum aus und wählen Sie dann die Aktion **Arbeitszeittabelle bearbeiten** aus.  
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. Geben Sie die Anzahl der Stunden ein, die von der Ressource an jedem Wochentag verwendet werden.

    > [!TIP]  
    >   Sie können die Summe der Arbeitszeittabellenstunden überprüfen, die Sie in die Infobox **Tatsächlich/Budgetiert Zusammenfassung** eingegeben haben.  
4. Wiederholen Sie Schritt 3 für weitere Arbeitstypen, die die Ressource ausführt.
5. Wählen Sie die Aktion **Übermitteln** aus und wählen Sie dann die Aktion **Alle offenen Zeilen**, um alle Zeilen zu senden oder **Nur ausgewählte Zeilen**, um nur die Zeilen zu übermitteln, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.  

    > [!NOTE]  
    >   ie können nur Arbeitszeitta‎bellenzeilen senden, für die Sie Zeit eingegeben haben.  
6. Um Informationen in einer Zeile zu ändern, die auf **Übermittelt** festgelegt wurde, wählen Sie die Zeile und wählen Sie dann die Aktion **Erneut öffnen** aus.

    > [!NOTE]  
    >   Ein Manager weist möglicherweise eine Arbeitszeittabellenzeile zurück, die zur Genehmigung eingesendet wird. Wenn eine Zeile den Status **Abgelehnt** hat, können Sie an der Zeile Änderungen vornehmen und dann erneut **Übermitteln** wählen.  
7. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-approve-or-reject-a-time-sheet"></a>So können Sie Arbeitszeittabellen genehmigen und ablehnen:
Eine Arbeitszeittabelle muss zur Genehmigung eingereicht werden, bevor Sie verwendet wird. Sie können einzelne Zeilen in der Arbeitszeittabelle genehmigen oder ablehnen und sie wieder an den Antragsteller für zusätzliche Aktion senden. Eine Arbeitszeittabelle kann auf zwei Arten genehmigt werden:

* Ein Arbeitszeittabellenadministrator kann jede Arbeitszeittabelle genehmigen.
* Die Person, die im Feld **Arbeitszeittabellen-Genehmiger Benutzer-ID** in einer Ressourcenkarte angegeben wird, kann die Arbeitszeittabellen dieser Ressource genehmigen. Weitere Informationen finden Sie unter [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeitnachweise für Manager** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie eine Arbeitszeittabelle aus der Liste aus.  
3. Wählen Sie auf der Seite **Arbeitszeittabelle** die Aktion **Genehmigen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen zu übermitteln oder **Nur ausgewählte Zeilen**, um nur jene Zeilen zu genehmigen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus.  
5. Wählen Sie die Aktion **Ablehnen** und führen Sie die Schritte 4 bis 5 aus.  

> [!TIP]  
>   Verwenden Sie die Infoboxen **Arbeitszeittabellenstatus** uns **Tatsächliche/Geplante Zusammenfassung** aus, um einen schnellen Überblick zu Arbeitszeittabelleninformationen zu erhalten.

Nachdem Sie eine Arbeitszeittabelle genehmigt oder abgelehnt haben, kann sie nicht mehr bearbeitet werden, außer wenn sie zuerst wieder geöffnet wird. Verwenden Sie das folgende Vorgehen, um eine genehmigte oder zurückgewiesene Arbeitszeittabelle erneut zu öffnen.

## <a name="to-reopen-a-time-sheet"></a>So öffnen Sie eine Arbeitszeittabelle erneut:
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeitnachweise für Manager** oder **Arbeitszeitnachweise** ein und wählen Sie dann den entsprechenden Link.
2. Öffnet eine Arbeitszeittabelle aus der Liste.  

    > [!NOTE]  
    >   Sie können Zeilen nur erneut öffnen, die den Status **Genehmigt** haben. Sie können keine Zeilen erneut öffnen, die den Status **Abgelehnt** haben. Sie können eine Arbeitszeittabelle nicht erneut öffnen, wenn diese gebucht wurde.  
3. Wählen Sie auf der Seite **Erneut öffnen** die Aktion **Genehmigen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen erneut zu öffnen oder **Nur ausgewählte Zeilen**, um nur jene Zeilen erneut zu öffnen, die auf der Seite **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus. Der Status der Arbeitszeittabellen, Zeile oder Zeilen wechselt auf **Übermittelt**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Buchen von Arbeitszeittabellenzeilen zu einem Ressourcen-Buch.-Blatt
Nachdem Sie Arbeitszeittabellenposten für eine Ressource genehmigt haben, können Sie sie in das entsprechende Ressourcen-Buch.-Blatt buchen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Ressourcen Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Ressourcen-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Buchen von Arbeitszeittabellenzeilen in einem Ressourcen-Buch.-Blatt
Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das Projektbuchungsblatt des entsprechenden Projekts buchen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Buch.-Blätter Projekt** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  

    > [!NOTE]  
    >   Informationen über den Arbeitstyp und darüber, ob die Arbeit fakturierbar ist, werden aus der Arbeitszeittabellenzeile kopiert. Bei Bedarf können Sie die Anzahl der Stunden reduzieren und eine Teilbuchung durchführen. Wenn Sie die Anzahl reduzieren, dann wird bei der nächsten Auswahl von **Zeilen anhand von Arbeitszeittabellen vorschlagen** eine Zeile mit der Restmenge der Stunden erstellt.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Die Seite **Projekt-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## <a name="to-archive-time-sheets"></a>So archivieren Sie Arbeitszeittabellen
Nachdem Sie Arbeitszeittabellen gebucht haben, können Sie diese für spätere Bezugnahme archivieren. Alle Arbeitszeittabellenzeilen müssen gebucht werden, bevor eine Arbeitszeittabelle archiviert werden kann.

> [!NOTE]  
>   Wenn Sie eine Arbeitszeittabelle archivieren, wird sie aus der Seite **Arbeitszeittabelle** und aus der Seite **Arbeitszeittabelle für Manager** entfernt.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Arbeitszeitnachweise in Archiv verschieben** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.  
3. Um archivierte Stundenzettel zu überprüfen, wählen Sie die Funktion ![Glühbirne, die das Symbol Tell Me feature](media/ui-search/search_small.png "Tell Me-Funktion") öffnet, geben Sie **Stundenzettel-Archive** oder **Manager-Stundenzettel-Archive** ein und wählen Sie dann den entsprechenden Link.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)    
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)     
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
