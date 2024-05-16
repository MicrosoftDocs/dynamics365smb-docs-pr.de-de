---
title: E-Belege im Kaufprozess verwenden
description: 'Erfahren Sie, wie Sie die E-Beleg-Funktionalität im Zusammenhang mit Einkaufsrechnungen und Bestellungen nutzen.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-purchases-process"></a>E-Belege im Kaufprozess verwenden

Sie können konfigurierte elektronische Belege (E-Belege) mit den Einkaufsbelegen verwenden.

Die folgenden Einkaufsbelege können mit der E-Belege-Funktionalität verwendet werden:  

- Einkaufsrechnungen
- Bestellungen (ab Version 24.0)
- Einkaufsgutschriften
- Fibu Buch.-Blätter

> [!NOTE]
> Ab der [!INCLUDE[prod_short](includes/prod_short.md)] Version 24.0 können **Bestellungen** mit den empfangenen **E-Belegen** verknüpft werden.  

## <a name="e-documents-in-purchases"></a>E-Belege im Einkauf

Der Eingang von E-Belegen in Dynamics 365 Business Central kann als Batchauftrag oder manuell durchgeführt werden.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>So richten Sie Kreditoren für die Arbeit mit verschiedenen Einkaufsbelegen ein

Gehen Sie wie folgt vor, um Kreditoren so zu konfigurieren, dass sie mit eingehenden elektronischen Rechnungen richtig funktionieren: 

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus. 
2. Wählen Sie den Kreditor aus, den Sie konfigurieren möchten.   
3. Suchen Sie im Inforegister **Empfangen** das Feld **E-Beleg empfangen an**, um den Standardeinkaufsbeleg anzugeben, der aus dem empfangenen E-Beleg generiert werden soll. 

   > [!NOTE]
   > Im Feld **E-Beleg empfangen an** können Benutzende entweder eine **Einkaufsrechnung** oder eine **Bestellung** auswählen, je nachdem, was aus der empfangenen E-Rechnung erstellt werden soll. Diese Auswahl hat keine Auswirkungen auf die Erstellung von Korrekturbelegen. In beiden Fällen generiert das System eine **Gutschrift**.  

   > [!NOTE]
   > Wenn Benutzende die Option **Bestellung** im Feld **E-Beleg empfangen an** auswählen, versucht das System, eine der vorhandenen Bestellungen zu aktualisieren. Falls die Bestellung für einen Kreditor im empfangenen **E-Beleg** jedoch nicht existiert, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] eine neue **Bestellung** und verwendet dabei den gleichen Ansatz wie beim Erstellen der neuen **Einkaufsrechnungen**, der weiter unten auf dieser Seite erläutert wird.  

4. Wählen Sie eine der Optionen aus, die Sie für den ausgewählten Kreditor verwenden möchten. 
5. Schließen Sie die Seite.   

### <a name="to-work-with-purchase-invoices"></a>Um mit Einkaufsrechnungen zu arbeiten

#### <a name="run-the-batch-job"></a>Stapelverarbeitung ausführen

> [!NOTE]
> Diese Stapelverarbeitung dient der automatisierten Erfassung Ihrer eingehenden Rechnungen. Sie funktioniert nur in einem Land oder einer Region, in der die Funktionalität vorhanden ist.  

Jedes Mal, wenn eine **Aufgabenwarteschlange** ausgewählt wird und der externe Dienst über eingehende Rechnungen verfügt, die von Ihrem Kreditor gesendet wurden, sammelt und importiert das System diese Rechnungen. Gehen Sie wie folgt vor, um den Vorgang abzuschließen: 

1. Nachdem die Ausführung des Batchauftrags abgeschlossen ist, werden die neu importierten Rechnungen zusammen mit ihren grundlegenden detaillierten Informationen auf der Seite **E-Beleg** aufgelistet. 
2. Um weitere Details anzuzeigen, öffnen Sie einen bestimmten E-Beleg.   
3. Wenn im E-Beleg keine Fehler oder Probleme aufgetreten sind, ordnet das Feld **Datensatz** die Belegnummer der Einkaufsrechnung zu, wenn dies auf der Seite **Kreditorenkarte**, die das System automatisch erstellt hat, konfiguriert ist. Wählen Sie den Link aus, um den Beleg zu öffnen.
 
   > [!NOTE]
   > Dieser vom System erstellte Beleg ist nicht der gebuchte Beleg. 

4. Um direkt zum Einkaufsbeleg zu gelangen, wählen Sie das Feld **Datensatz** aus. Nachdem Sie die Seite **Einkaufsrechnung** geöffnet haben, überprüfen Sie den Beleg. Wenn alles korrekt ist, buchen Sie den Beleg.  
5. Wenn Sie den Einkaufsbeleg buchen, wird das Feld **Datensatz** auf dem **E-Beleg** von **Rechnung** auf **Einkaufsrechnung** aktualisiert und die Nummer des gebuchten Einkaufsbelegs ist verfügbar. Sie können die Nummer auswählen, um die gebuchte Einkaufsrechnung zu öffnen. 

Details zu Protokollen sind die gleichen wie im Verkaufsprozess für E-Belege.  

Da Fehler im Verkaufsprozess meist mit der Verfügbarkeit des Dienstes zusammenhängen, kann der eingehende Beleg mehrere Ursachen enthalten. Der häufigste Grund für einen Fehler ist, dass das System die Zeilen im E-Beleg, den Sie von Ihrem Kreditor erhalten haben, nicht erkennen kann. Daher können keine Zeilen in Ihre Einkaufsrechnung eingegeben werden. 

Es gibt zwei häufige Fehler:  

- Wenn Sie diese bestimmte Zeile aus Ihrer Kreditorenrechnung verwenden möchten, die direkt auf das Hauptbuchkonto (Sachkonto) gebucht wurde, müssen Sie den Wert **Zuordnungstext** korrekt konfiguriert haben. Um diesen Fehler zu umgehen, wenn Sie Sachkonten verwenden möchten, wählen Sie **Text zu Konto zuordnen** aus, um eine spezifische Zuordnung des Werts **Zuordnungstext** mit dem Wert **Sollkontonr.** zu erstellen, die Sie verwenden möchten. 
- Wenn Sie den Lagerbestand verfolgen und Zeilen aus Ihrer Kreditorenrechnung zum Ausfüllen der Artikel in Ihren Belegzeilen verwenden möchten, müssen Sie den Wert **Artikelreferenz-Nr.** korrekt konfiguriert haben. Um diesen Fehler zu umgehen, ordnen Sie den externen Artikel mithilfe der Artikelreferenzliste Ihren Artikelnummern zu. Weitere Informationen finden Sie unter [Artikelreferenzen verwenden](inventory-how-use-item-cross-refs.md). 

Nachdem Sie die Fehler und Warnungen behoben haben, können Sie manuell festlegen, wann das System basierend auf Ihren Einstellungen eine Einkaufsrechnung erstellen soll, indem Sie **Beleg erstellen** auswählen.   

#### <a name="manually-import-invoices"></a>Rechnungen manuell importieren

Um externe E-Belege manuell zu importieren, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol aus. Geben Sie **E-Beleg – Dienst** ein und wählen Sie dann den zugehörigen Link aus. 
2. Wählen Sie auf der Seite **E-Beleg – Dienst** den aktiven Dienst aus.   
3. Wählen Sie **Eingang** und laden Sie die E-Beleg-Datei hoch, die Sie vom Kreditor erhalten haben. 
4. Wenn eine Fehlermeldung auftritt, öffnen Sie den E-Beleg, um die Probleme zu beheben. 
5. Wenn Sie mit der Behebung der Probleme fertig sind, wählen Sie in der Gruppe **Manuell importieren** die Option **Beleg erstellen** aus.  
6. Nachdem der Beleg in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt wurde, ändert sich Ihre Anzeige durch die Verwendung eines Batchauftrags nicht. 

### <a name="e-documents-with-purchase-orders"></a>E-Belege mit Bestellungen

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>Um Bestellungen mit empfangenen E-Belegen zu verknüpfen

Wenn bei Ihrem **Kreditor** das Feld **E-Beleg empfangen an** für die Arbeit mit **Bestellungen** konfiguriert ist, tut [!INCLUDE[prod_short](includes/prod_short.md)] nach der Erstellung des elektronischen Belegs (manuell oder von einem externen Endpunkt aus) in [!INCLUDE[prod_short](includes/prod_short.md)] Folgendes:  

1. Wenn die **Bestellung** für diesen bestimmten Kreditor existiert und eine Bestellnummer in der empfangenen **E-Beleg**-Datei vorhanden ist, verknüpft [!INCLUDE[prod_short](includes/prod_short.md)] diesen **E-Beleg** automatisch mit der erwähnten **Bestellung**. Der **Belegstatus** dieses **E-Belegs** ist dann **In Bearbeitung** und der **Status des E-Belegs** auf der Unterseite **Dienststatus** ist **Bestellung verknüpft**. Diese Verknüpfung wird im Feld **Beleg** dieses speziellen **E-Belegs** angezeigt. Wenn Sie die automatisch verknüpfte **Bestellung** ändern müssen, können Sie dies mit der Aktion **Bestellungslink aktualisieren** tun und manuell eine der vorhandenen Bestellungen für diesen Kreditor auswählen. Dies ist nur möglich, bevor Sie die Zeilen zwischen **E-Beleg** und **Bestellung** abgleichen.  

2. Wenn die **Bestellung** für diesen bestimmten Kreditor existiert, es aber keine Bestellnummer in der eingangenen **E-Beleg**-Datei gibt, bietet [!INCLUDE[prod_short](includes/prod_short.md)] die Möglichkeit, eine der vorhandenen Bestellungen auszuwählen, falls Sie diesen Beleg manuell hochgeladen haben. Dadurch öffnet sich die Liste **Bestellungen** mit Bestellungen nur für den Kreditor, von dem Sie den **E-Beleg** erhalten haben. Sie müssen die gewünschte **Bestellung** und dann **OK** auswählen. Wenn Sie nicht die richtige **Bestellung** ausgewählt haben oder der **E-Beleg** automatisch von einem externen Endpunkt über die **Aufgabenwarteschlange** abgerufen haben, wird ein neuer **E-Beleg** mit keinem Einkaufsbeleg verknüpft. Der **Belegstatus** lautet dann **Fehler** und der **Status des E-Belegs** auf der Unterseite **Dienststatus** lautet ebenfalls **Fehler bei der Verarbeitung des importierten Belegs**. Um die Verknüpfung der **Bestellung** abzuschließen, wählen Sie die Aktion **Bestellungslink aktualisieren** und dann eine der vorhandenen Bestellungen für diesen Kreditor aus. 

3. Wenn die **Bestellung** für diesen bestimmten Kreditor bei der Erstellung des neuen **E-Belegs** noch nicht vorliegt, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] eine neue **Bestellung** und verwendet dabei dasselbe Erstellungsmodell wie für neue **Einkaufsrechnungen**. Der **Belegstatus** dieses **E-Belegs** ist dann **Verarbeitet** und der **Status des E-Belegs** auf der Unterseite **Dienststatus** lautet **Importierter Beleg erstellt**. Diese Verknüpfung wird im Feld **Beleg** dieses speziellen **E-Belegs** angezeigt.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Zeilen des empfangenen E-Belegs mit der Bestellung abgleichen

Sie können Ihre empfangenen elektronischen Belege von zwei verschiedenen Orten aus mit den Zeilen der Bestellungen abgleichen: von der Seite **E-Beleg** aus oder über die Seite **Bestellung**. Der einfachste Weg, die bereits verknüpften **Bestellungen** zu finden, ist die Kachel **Verknüpfte Bestellungen** unter den **E-Beleg-Aktivitäten**. Alle nicht verlinkten Belege finden Sie über die Kachel **Wartende E-Einkaufsrechnungen**. Hier finden Sie eine Liste von **E-Belegen**, die Sie durchgehen müssen.  

> [!NOTE]
> Die **E-Beleg-Aktivitäten** mit diesen beiden Kacheln finden Sie im folgenden **Rollencenter** : Bewertung durch Geschäftsführung, Geschäftsführung, Buchhaltung, Lagerverwaltung sowie Versand und Wareneingang.  

> [!NOTE]
> Wenn sich der Mehrwertsteuersatz zwischen dem eingehenden Beleg und dem Mehrwertsteuersatz des Unternehmens unterscheidet, kann der Abgleich von Belegen in einer Umgebung mit mehreren Ländern nicht verwendet werden.  

##### <a name="matching-lines-from-purchase-order"></a>Zeilen aus einer Bestellung abgleichen

Sie können die Zeilen aus der Liste **Bestellungen** oder aus einer der geöffneten **Bestellung** abgleichen. Gehen Sie wie folgt vor, um damit zu beginnen:  

1. Wählen Sie die Kachel **Verknüpfte Bestellungen** in Ihrem Rollencenter aus, wenn dort eine Nummer vorhanden ist. 
2. Entscheiden Sie sich für eine der beiden Möglichkeiten für den Abgleich: 

   - Wenn Sie die Zeilen aus der Liste **Bestellungen** abgleichen, wählen Sie die **Bestellzeile**, die Sie abgleichen möchten, und die Aktion **E-Belegzeilen zuordnen** aus.  
   - Wenn Sie zuerst die **Bestellung** öffnen wollen, öffnen Sie den Beleg und wählen Sie dann die Aktion **E-Belegzeilen zuordnen**. 

3. Da der Prozess für beide Optionen derselbe ist, öffnen Sie die Seite **Bestellabgleich** mit folgendem Inhalt: 

    1. In der Kopfzeile finden Sie folgende Angaben, die Ihnen das Zuordnen der Zeilen eventuell erleichtern: 

       |Name des Felds |Beschreibung |
       |--------|-----------------|
       |Kreditorenname |Gibt den Namen des Kreditors des elektronischen Belegs an. |
       |E-Beleg-Nr. |Gibt die Nummer des verknüpften elektronischen Belegs an. |
       |Datum des E-Belegs |Gibt das Datum des verknüpften elektronischen Belegs an.  |
       |E-Belegbetrag |Gibt den Gesamtbetrag des verknüpften E-Belegs ohne MwSt. an. |

    2. In den Zeilen finden Sie die importierten Zeilen aus der **E-Beleg**-Datei auf der linken Seite und die Zeilen aus den vorliegenden **Bestellungen** auf der rechten.  
    3. Alle Zeilen auf beiden Seiten enthalten Artikelnummern und Beschreibungen sowie den **EK-Preis** und den **Zeilenrabatt %**.  
    4. Auf der Seite **Importierte Zeilen** finden Sie außerdem das Feld **Menge** als Gesamtmenge aus der E-Rechnung und das Feld **Abgeglichene Menge**, das die Menge angibt, die bereits mit den Bestellzeilen übereinstimmt. 
    5. Auf der Seite **Bestellzeilen** finden Sie außerdem die **Verfügbare Menge** als die Menge, die dieser Zeile zugeordnet werden kann (erhaltene, aber nicht in Rechnung gestellte Menge) und die **Zu fakturierende Menge**, wobei es sich um die Menge handelt, die dieser Zeile bereits zugeordnet wurde. 
    6. Um Zeilen abzugleichen, wählen Sie auf beiden Seiten die Zeilen aus, die Sie abgleichen möchten, und wählen Sie dann die Aktion **Manuell abgleichen**. Die übereinstimmenden Zeilen werden grün markiert. 
    7. Es ist möglich, eins zu eins abzugleichen, es ist jedoch auch möglich, viele zu eins oder eins zu vielen abzugleichen, indem Sie mehrere Zeilen auf der einen oder anderen Seite auswählen, bevor Sie die Aktion **Manuell abgleichen** auswählen. 
    8. Sie können auch die Aktion **Automatisch abgleichen** auswählen, um alle Zeilen, bei denen **Typ**, **Nummer**, **VK-Preis**, **Rabatt** und **Maßeinheit** gleich sind, automatisch abzugleichen. 
    9. Wenn Ihnen ein Fehler unterläuft, können Sie die Aktion **Zuordnung entfernen** wählen, um die abgeglichenen Zeilen auf der Bestellseite zu entfernen, oder die Aktion **Zuordnung zurücksetzen**, um alle Zuordnungen zurückzusetzen. 
    10. Wenn Ihr **E-Beleg** viele Zeilen hat, können Sie während des Abgleichvorgangs die Aktion **Ausstehende Zeilen anzeigen** auswählen, um alle E-Belegzeilen zu entfernen, wenn sie bereits vollständig abgeglichen wurden. Wenn Sie alle Zeilen sehen müssen, können Sie jederzeit die Aktion **Alle Zeilen anzeigen** auswählen. 

4. Wenn Sie den Abgleich abgeschlossen haben, müssen Sie die Aktion **Auf Bestellung anwenden** auswählen.   
5. Nachdem Sie den Abgleich auf die **Bestellung** anwenden, aktualisiert [!INCLUDE[prod_short](includes/prod_short.md)] die folgenden Felder:

    1. Die **Kred.-Rechnungsnr.** und das **Belegdatum** im Belegkopf werden mit Werten aus dem elektronischen Beleg aktualisiert, den Sie erhalten und verknüpft haben. 
    2. Die **Zu fakturierende Menge** in den Zeilen wird mit den Werten aus der Spalte **Zu fakturierende Menge** der Seite **Bestellabgleich** aktualisiert, je nachdem, welchen Abgleich Sie vorgenommen haben. 
    3. Sie können den Beleg jetzt über die Aktion **Buchen** buchen.  
    4. Sobald Sie den Beleg buchen, ändert sich der Wert im Feld **Beleg** auf der Seite **E-Beleg** und bezieht sich dann auf die **Gebuchte Einkaufsrechnung**. 
    5. Schließen Sie die Seite.  

> [!IMPORTANT]
> Standardmäßig können Sie nur die Zeilen abgleichen, die in beiden Belegen den gleichen Gesamtbetrag aufweisen. Das bedeutet, dass der **EK-Preis** zusammen mit dem angewendeten **Zeilenrabatt %** gleich sein müssen, da in einem Beleg ein Betrag ohne Rabatt und in einem anderen ein Betrag mit Rabatt angegeben sein kann.  

Wenn Sie etwas Toleranz hinzufügen und Unterschiede zwischen den Zeilen in der **E-Rechnung** und der **Bestellung** zulassen möchten, gehen Sie wie folgt vor:   

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kredite und Einkauf Einr. ein** und wählen Sie dann den entsprechenden Link.  
2. Sie möchten im Feld **E-Beleg-Abgleichsdifferenz %** eine Toleranz zulassen und den maximal zulässigen Prozentsatz der Kostendifferenz beim Abgleich einer eingehenden **E-Belegzeile** mit der **Bestellzeile** angeben. 
3. Diese Einstellung gilt für alle übereinstimmenden Zeilen, berücksichtigt jedoch erneut die Toleranz für den Gesamtbetrag, wie für den **EK-Preis** zusammen mit dem angewandten **Zeilenrabatt %**.  
4. Schließen Sie die Seite.   

##### <a name="matching-lines-from-e-document"></a>Zeilen aus E-Belegen abgleichen

Sie können die Zeilen auf der Seite **E-Beleg** abgleichen. Gehen Sie wie folgt vor, um zu beginnen:  

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus. Geben Sie **E-Belege** ein und wählen Sie dann den zugehörigen Link aus. 
2. Wählen Sie die **E-Belege** aus, die Sie abgleichen möchten.   
3. Wählen Sie die Aktion **Bestellung abgleichen** um die Seite **Bestellabgleich** zu öffnen.  
4. Wiederholen Sie die Schritte, die Sie verwendet haben, als Sie mit dem Abgleichen von Bestellungen begonnen haben.

### <a name="e-document-matching-assistance-copilot"></a>Copilot zur Unterstützung beim Abgleich von E-Belegen

> [!NOTE]
> Derzeit befindet sich der Copilot **Unterstützung beim Abgleich von E-Belegen** in der Phase „Produktionsbereite Vorschauversion“ und ist weltweit außer in Kanada verfügbar. Er funktioniert nur auf Englisch. 

> [!NOTE]
> Copilot ist ein KI-gestützter Assistent, der Menschen in Ihrem Unternehmen hilft, ihre Kreativität zu entfalten und lästige Aufgaben zu automatisieren. Mithilfe des Copiloten zur **Unterstützung beim Abgleich von E-Belegen** können Benutzende ihre erhaltenen elektronischen Rechnungen problemlos mit vorhandenen Bestellzeilen abgleichen. Hierzu wird das große Sprachmodell zum Abgleichen von Zeilen zwischen zwei verschiedenen Belegen verwendet. 

#### <a name="to-activate-the-copilot"></a>So aktivieren Sie den Copiloten

Falls Sie den Copiloten zur **Unterstützung beim Abgleich von E-Belegen** nicht aktiviert haben, müssen Sie dies manuell tun. Um den Copiloten zur **Unterstützung beim Abgleich von E-Belegen** zu aktivieren, gehen Sie wie folgt vor: 

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Copilot- und KI-Funktionen** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie in der Liste der Funktionen **Unterstützung beim Abgleich von E-Belegen** und ändern Sie den Status auf **Aktiv**.  

Sobald der Copilot aktiviert ist, können Sie ihn verwenden.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Den Copilot zur Unterstützung beim Abgleich von E-Belegen verwenden

Wenn der Copilot aktiviert ist, erhalten die vorhandenen Aktionen **E-Belegzeilen zuordnen** auf Bestellungen und **Bestellung abgleichen** auf der Seite **E-Beleg** verschiedene Symbole, die für die KI-Fähigkeit stehen. Sie können diese Aktionen (die gleichen wie in den vorherigen Beispielen aus der Liste der Bestellungen) von einer der **Bestellungen** oder von einem **E-Beleg** aus ausführen. Alle Schritte zum Ausführen sind gleich, aber wenn Sie diese Aktion ausführen, sieht das Ergebnis anders aus und Sie müssen wie folgt vorgehen:  

1. Wählen Sie für bereits verknüpfte Belege die Aktion **E-Belegzeilen zuordnen** oder **Bestellung abgleichen**.  
2. Wie Sie sehen, funktioniert der Prompt **E-Belegsauftragszeilen mit Copilot abgleichen** und die Seite **Bestellabgleich** ist im Hintergrund. Das heißt, derselbe Prozess findet statt, allerdings mit der automatischen Unterstützung von **Copilot**, der den Abgleichsprozess anstatt Ihnen erledigt. 
3. Nach einigen Sekunden schlägt **E-Belegsauftragszeilen mit Copilot abgleichen** Zeilen zum Abgleichen mit einigen zusätzlichen Details vor: 

    1. In der Promptkopfzeile finden Sie die folgenden Informationen: 

       |Name des Felds |Beschreibung |
       |--------|-----------------|
       |Automatisch abgeglichen | Gibt die Anzahl der automatisch vorgeschlagenen Übereinstimmungen an. Diese basiert auf einem Zeichenfolgenvergleich. Wenn sich die Beschreibungen zu 80 % oder mehr überschneiden, gleicht das System diese Beschreibungen automatisch ab, ohne GPT-Funktionen zu verwenden. |
       |Copilot-Übereinstimmung | Gibt die Anzahl der von Copilot anhand von Zeichenfolgen- und semantischen Vergleichen vorgeschlagenen Übereinstimmungen an. |
       |E-Beleg-Nr. | Gibt die verknüpfte E-Belegnummer an. |
       |Gesamtrechnungsbetrag ohne MwSt. | Gibt den Gesamtrechnungsbetrag ohne MwSt. an. |
       |Abgeglichener Verkaufsbetrag inkl. MwSt. | Gibt den abgeglichenen Betrag einschließlich MwSt. an. |
    
    2. Wenn alle Zeilen übereinstimmen, wird in der oberen rechten Ecke dieser grüne Text angezeigt: **Alle Zeilen (100 %) wurden abgeglichen. Überprüfen Sie die Übereinstimmungsvorschläge**.  
    3. In den Zeilen **Zugeordneter Vorschlag** finden Sie die folgenden Informationen:  

       |Name des Felds |Description |
       |--------|-----------------|
       |E-Beleg-Zeilennr. | Gibt die Zeilennummer des E-Belegs an (aus der ursprünglichen E-Belegdatei). |
       |Beschreibung der E-Belegzeile | Gibt die Zeilenbeschreibung des E-Belegs an (aus der ursprünglichen E-Belegdatei). |
       |Abgeglichene Menge | Gibt die Menge an, die auf die Bestellzeile angewendet wird. |
       |Angebot | Gibt die von der KI vorgeschlagene Aktion an. Diese vorgeschlagenen Aktionen beziehen sich auf den Abgleich der Bestellzeilen. |

    4. Alle vollständig vorgeschlagenen und zugeordneten Zeilen sind grün markiert. Wenn ein Problem vorliegt, z. B. ein anderer Preis, der aber im zulässigen Preisbereich liegt, wird diese Zeile gelb markiert. Wenn zwischen den Beschreibungsfeldern eine Ähnlichkeit besteht, der Preisunterschied jedoch größer als zulässig ist, wird die Zeile rot markiert. 
    5. Wenn Sie mit einigen Vorschlägen nicht zufrieden sind, können Sie diese mithilfe der Aktion **Zeile löschen** entfernen.  
    6. Wenn Sie die vorgeschlagenen Zuordnungen sehen möchten, können Sie den Link in der Spalte **Vorschlag** verwenden, um die Seite **Details zum E-Dokument-Abgleich** zu öffnen. 
    7. Auf der Seite **Details zum E-Beleg-Abgleich** können Sie die Details aus dem **E-Beleg** und der **Bestellung** vergleichen, um die vorgeschlagene Übereinstimmung vor der Bestätigung zu überprüfen. 
    8. Schließen Sie die Seite nach der Überprüfung.   

4. Wenn Sie mit den meisten Vorschlägen nicht zufrieden sind oder das Feature **E-Belegsauftragszeilen mit Copilot abgleichen** nicht verwenden möchten, wählen Sie **Verwerfen** aus. Sie können dann wie bereits erklärt mit dem manuellen Abgleich fortfahren.  
5. Wenn Sie Vorschläge behalten möchten, wählen Sie die Schaltfläche **Behalten**. Das System speichert dann alle von **Copilot** gemachten Vorschläge.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] schließt den Copilot-Prompt und die Zeilen auf der Seite **Bestellabgleich** werden grün markiert, weil sie bereits abgeglichen wurden. 
7. Jetzt können Sie mit der Arbeit fortfahren, als würden Sie einen manuellen Abgleich durchführen. Das heißt, Sie können Zuordnungen entfernen, manuell abgleichen oder den Abgleich zurücksetzen. Wenn Sie keine Änderungen vornehmen möchten, wählen Sie einfach die Aktion **Auf Bestellung anwenden** und arbeiten Sie mit der **Bestellung** weiter. 

> [!NOTE]
> Sie können Sie die Aktion **Abgleich mit Copilot** auf der Seite **Bestellabgleich** erneut auswählen. In diesem Fall werden Sie jedoch gefragt, ob Sie die vorhandenen Zuordnungen überschreiben möchten, da alle Zeilen bereits abgeglichen wurden.  

> [!NOTE]
> Die Preis-/Kostenanalyse und die Prüfung der verfügbaren Menge gehören zur Vorverarbeitung dazu.   

## <a name="overview-of-e-document-statuses"></a>Übersicht über die Status von E-Belegen

Um einen besseren Überblick über alle E-Belege im Unternehmen zu erhalten, können Sie das **Buchhalter**-Rollencenter auswählen, in dem die Status des E-Belegs vorhanden sind. Dort finden Sie E-Beleg-Aktivitäten mit folgenden Status:

- **Eingehende E-Belege:**

    - Verarbeitet
    - In Bearbeitung
    - Fehler


## <a name="see-also"></a>Siehe auch

[E-Belege einrichten](finance-how-setup-edocuments.md)    
[E-Belege im Verkaufsprozess verwenden](finance-how-use-edocuments.md)   
[Erweiterung der E-Beleg-Funktionalität](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Finanzmanagement](finance.md)    
[Verkäufe fakturieren](sales-how-invoice-sales.md)    
[Einkäufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)    
[Arbeiten mit Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

