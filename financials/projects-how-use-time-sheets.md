---
title: "Vorgehensweise: Arbeitszeittabellen nutzen für Projekte| Microsoft Docs"
description: Beschreibt, wie Arbeitszeittabellen verwendet werden, um Projekte zu verwalten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1796436b964f5e1e4220f885e97713848d94bdfb
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Verwenden von Arbeitszeittabellen für Projekte
<a id="how-to-use-time-sheets-for-jobs" class="xliff"></a>
Verwenden Sie die Stapelverarbeitung **Arbeitszeittabellen erstellen**, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Sie müssen Berechtigungen haben, Arbeitszeittabellen zu erstellen.

Sie können Ihre Projektplanzeilen in die Arbeitszeittabelle kopieren und verwenden. Auf diese Art müssen Sie die Informationen immer nur an einer Stelle eingeben und die Zeileninformationen sind immer korrekt.

Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das entsprechende Projektjournal oder Ressourcen-Journal buchen.

Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie Informationen einrichten und einen Administrator und mindestens einen Genehmiger für Arbeitszeittabellen festlegen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

**Hinweis**: Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen].

## Arbeitszeittabellen erstellen
<a id="to-create-a-time-sheet" class="xliff"></a>
Sie können die Stapelverarbeitung **Arbeitszeittabellen erstellen** verwenden, um Arbeitszeittabellen für eine bestimmte Anzahl von Perioden oder Wochen einzurichten. Nachdem eine Arbeitszeittabelle erstellt wurde, kann der Arbeitszeittabellenbesitzer sie öffnen und die Zeit aufzeichnen, die für eine Aufgabe benötigte wurde.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen** eingeben und den entsprechenden Link auswählen.
2. Im Fenster **Arbeitszeittabellen-Liste** wählen Sie die Aktion **Arbeitszeittabellen erstellen** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Notiz**: Die Felder **Arbeitszeittabellen verwenden** und **Arbeitszeittabellenbesitzer-Benutzer-ID** müssen auf der Karte der Arbeitszeittabelle für die Ressource ausgefüllt werden.

1. Wählen Sie die Schaltfläche **OK** aus.  

Im Fenster **Liste Arbeitszeittabelle** können Sie die erstellten Arbeitszeittabellen anzeigen.

## So kopieren Sie Projektplanzeilen in eine Arbeitszeittabelle:
<a id="to-copy-job-planning-lines-to-a-time-sheet" class="xliff"></a>
Die folgende Vorgehensweise beschreibt, wie Projektplanzeilen einer Arbeitszeittabelle enfach hinzugefügt werden können.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen** eingeben und den entsprechenden Link auswählen.  
2. Im Fenster **Arbeitszeittabellen-Liste** wählen Sie eine Arbeitszeittabelle für den entsprechenden Zeitraum aus und wählen Sie dann die Aktion **Arbeitszeittabelle bearbeiten** aus.  
3. Wählen Sie die Aktion **Zeilen von Projektplanung erstellen** aus. Jegliche Projektplanzeilen im Arbeitszeittabellenzeitraum werden in die Arbeitszeittabelle für die Person oder die Maschine unter **Ressourcennummer** kopiert. Feld auf der Arbeitszeittabelle.

## Um Arbeitstypen festzulegen und einer Arbeitszeittabelle hinzufügen
<a id="to-define-work-types-and-add-one-to-a-time-sheet" class="xliff"></a>
Sie können den Arbeitstyp für alle Arbeitszeittabellenzeilen für Projekte festlegen. Auf diese Art können Sie Informationen hinzufügen, die Sie benötigen, um dem Debitor unterschiedliche Arten von Arbeit zu berechnen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen** eingeben und den entsprechenden Link auswählen.   
2. Öffnet die entsprechende Arbeitszeittabelle.
3. Wählen Sie das Feld **Beschreibung**.  
4. Im Fenster **Arbeitszeittabellenzeilen-Projekt-Detail** wählen Sie das Feld **Arbeitstypencode** und wählen Sie einen Arbeitstyp aus der Liste aus, wie beispielsweise **Meilen**.  
5. Wenn keine Arbeitstypen vorhanden sind, wählen Sie die Aktion **Neu** aus.
6. Im Fenster **Arbeitstypen** füllen Sie die notwendigen Felder aus.
7. Wiederholen Sie Schritt 4, um den neuen Arbeitstyp in der Arbeitszeittabelle einzugeben.

## So können Sie Arbeitszeittabellenzeilen in anderen Arbeitszeittabellen wiederverwenden
<a id="to-reuse-time-sheet-lines-in-other-time-sheets" class="xliff"></a>
Falls die Arbeitszeittabelle Informationen von einem Zeitraum zum anderen gleich bleiben, können Sie Zeit sparen, indem Sie die Zeilen aus dem vorherigen Zeitraum kopieren. Tragen Sie dann einfach Ihren Zeitverbrauch für die neuen Periode ein.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen** eingeben und den entsprechenden Link auswählen.  
2. Öffnen Sie die Arbeitszeittabelle für eine Periode nach der Periode für eine vorhandene Arbeitszeittabelle mit Zeilen.  
3. Wählen Sie die Aktion **Zeilen aus vorherigen Arbeitszeittabellen kopieren** aus.

Die Zeilen werden kopiert, einschließlich Informationen wie Art und Beschreibung. Wenn beispielsweise die Zeile mit einem Projekt verknüpft ist, wird die **Projektnr.** kopiert. Alle kopierten Zeilen haben den Status **Offen**. Sie können die benutzerdefinierten Zeilen jetzt bei Bedarf ändern.

## So können Sie Arbeitszeittabellenzeilen ausfüllen und zur Genehmigung senden
<a id="to-fill-in-a-time-sheet-lines-and-submit-for-approval" class="xliff"></a>
Die Arbeitszeittabellenregistrierung wird in Stunden verfolgt, der Standard-Basiseinheit für Ressourcen. Standardmäßig zeigt eine Arbeitszeittabelle die allgemeinen Arbeitstage von Montag bis Freitag an.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie eine Arbeitszeittabelle für den entsprechenden Zeitraum aus und wählen Sie dann die Aktion **Arbeitszeittabelle bearbeiten** aus.  
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. Geben Sie die Anzahl der Stunden ein, die von der Ressource an jedem Wochentag verwendet werden.

    **Hinweis**: Sie können die Summe der Arbeitszeittabellenstunden überprüfen, die Sie in die Infobox **Tatsächlich/Budgetiert** eingegeben haben.  
4. Wiederholen Sie Schritt 3 für weitere Arbeitstypen, die die Ressource ausführt.
5. Wählen Sie die Aktion **Übermitteln** aus und wählen Sie dann die Aktion **Alle offenen Zeilen**, um alle Zeilen zu senden oder **Nur ausgewählte Zeilen**, um nur die Zeilen zu übermitteln, die im Fenster **Arbeitszeittabelle** ausgewählt wurden.  

    **Hinweis**: Sie können nur Arbeitszeitta‎bellenzeilen senden, für die Sie Zeit eingegeben haben.  
6. Um Informationen in einer Zeile zu ändern, die auf **Übermittelt** festgelegt wurde, wählen Sie die Zeile und wählen Sie dann die Aktion **Erneut öffnen** aus.

    **Hinweis**: Ein Manager weist möglicherweise eine Arbeitszeittabellenzeile zurück, die zur Genehmigung eingesendet wird. Wenn eine Zeile den Status **Abgelehnt** hat, können Sie an der Zeile Änderungen vornehmen und dann erneut **Übermitteln** wählen.  
7. Wählen Sie die Schaltfläche **OK** aus.

## So können Sie Arbeitszeittabellen genehmigen und ablehnen:
<a id="to-approve-or-reject-a-time-sheet" class="xliff"></a>
Eine Arbeitszeittabelle muss zur Genehmigung eingereicht werden, bevor Sie verwendet wird. Sie können einzelne Zeilen in der Arbeitszeittabelle genehmigen oder ablehnen und sie wieder an den Antragsteller für zusätzliche Aktion senden. Eine Arbeitszeittabelle kann auf zwei Arten genehmigt werden:

* Ein Arbeitszeittabellenadministrator kann jede Arbeitszeittabelle genehmigen.
* Die Person, die im Feld **Arbeitszeittabellen-Genehmiger Benutzer-ID** in einer Ressourcenkarte angegeben wird, kann die Arbeitszeittabellen dieser Ressource genehmigen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen Manager** eingeben und den entsprechenden Link auswählen.
2. Wählen Sie eine Arbeitszeittabelle aus der Liste aus.  
3. Wählen Sie im Fenster **Arbeitszeittabelle** die Aktion **Genehmigen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen zu übermitteln oder **Nur ausgewählte Zeilen**, um nur jene Zeilen zu genehmigen, die im Fenster **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus.  
5. Alternativ wählen Sie die Aktion **Ablehnen** und führen Sie die Schritte 4 bis 5 aus.  

**Hinweis**: Verwenden Sie die Infoboxen **Arbeitszeittabellenstatus** uns **Tatsächliche/Geplante Zusammenfassung** aus, um einen schnellen Überblick zu Arbeitszeittabelleninformationen zu erhalten.

Nachdem Sie eine Arbeitszeittabelle genehmigt oder abgelehnt haben, kann sie nicht mehr bearbeitet werden, außer wenn sie zuerst wieder geöffnet wird. Verwenden Sie das folgende Vorgehen, um eine genehmigte oder zurückgewiesene Arbeitszeittabelle erneut zu öffnen.

## So öffnen Sie eine Arbeitszeittabelle erneut:
<a id="to-reopen-a-time-sheet" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Arbeitszeittabellen Manager** oder **Arbeitszeittabelle** ein und wählen den entsprechenden Link aus.
2. Öffnet eine Arbeitszeittabelle aus der Liste.  

    **Hinweis**; Sie können Zeilen nur erneut öffnen, die den Status **Genehmigt** haben. Sie können keine Zeilen erneut öffnen, die den Status **Abgelehnt** haben. Sie können eine Arbeitszeittabelle nicht erneut öffnen, wenn diese gebucht wurde.  
3. Wählen Sie im Fenster **Arbeitszeittabelle** die Aktion **Erneut öffnen** aus, und wählen Sie die Aktion **Alle übermittelten Zeilen**, um alle Zeilen erneut zu öffnen oder **Nur ausgewählte Zeilen**, um nur jene Zeilen zu öffnen, die im Fenster **Arbeitszeittabelle** ausgewählt wurden.
4. Wählen Sie die Schaltfläche **OK** aus. Der Status der Arbeitszeittabellen, Zeile oder Zeilen wechselt auf **Übermittelt**.  

## Buchen von Arbeitszeittabellenzeilen zu einem Ressourcen-Buch.-Blatt
<a id="to-post-time-sheet-lines-in-a-resource-journal" class="xliff"></a>
Nachdem Sie Arbeitszeittabellenposten für eine Ressource genehmigt haben, können Sie sie in das entsprechende Ressourcen-Buch.-Blatt buchen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Ressourcenjournal** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Das Fenster **Ressourcen-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## Buchen von Arbeitszeittabellenzeilen in einem Ressourcen-Buch.-Blatt
<a id="to-post-time-sheet-lines-in-a-job-journal" class="xliff"></a>
Nachdem Sie Arbeitszeittabellenposten für ein Projekt genehmigt haben, können Sie sie in das Projektbuchungsblatt des entsprechenden Projekts buchen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Jobjournal** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Aktion **Zeilen von Arbeitszeittabellen vorschlagen** aus.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus. Einträge für Verbrauch werden im Ressourcen Buch.-Blatt erstellt, in dem Sie die Informationen ändern können.  

    **Hinweis**: Informationen über den Arbeitstyp und ob die Arbeit fakturierbar ist, werden aus der Arbeitszeittabellenzeile kopiert. Bei Bedarf können Sie die Anzahl der Stunden reduzieren und eine Teilbuchung durchführen. Wenn Sie die Anzahl reduzieren, dann wird bei der nächsten Auswahl von **Zeilen anhand von Arbeitszeittabellen vorschlagen** eine Zeile mit der Restmenge der Stunden erstellt.  
5. Wählen Sie die Aktion **Buchen** aus.  
6. Um die Buchung zu überprüfen, wählen Sie die Aktion **Sachposten** aus. Das Fenster **Projekt-Buch.-Blatt** öffnet die Anzeige des Ergebnisses der Buchung des Ressourcen Buch.-Blattes.

## So archivieren Sie Arbeitszeittabellen
<a id="to-archive-time-sheets" class="xliff"></a>
Nachdem Sie Arbeitszeittabellen gebucht haben, können Sie diese für spätere Bezugnahme archivieren. Alle Arbeitszeittabellenzeilen müssen gebucht werden, bevor eine Arbeitszeittabelle archiviert werden kann.

**Hinweis**: Wenn Sie eine Arbeitszeittabelle archivieren, wird sie aus der Liste **Arbeitszeittabelle** und aus der Liste **Arbeitszeittabelle für Manager** entfernt.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Arbeitszeittabellen in das Archiv verschieben** eingeben und den entsprechenden Link auswählen.  
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.  
3. Um die archivierten Arbeitszeittabellen anzusehen, wählen Sie in der oberen rechter Ecke das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Arbeitszeittabellen Archiv** oder **Manager Arbeitszeittabelle Archiv** ein und wählen den entsprechenden Link aus.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Projektmanagement](projects-manage-projects.md)  
[Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)    
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)     
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

