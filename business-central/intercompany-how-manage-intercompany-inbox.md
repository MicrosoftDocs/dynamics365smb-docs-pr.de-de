---
title: Intercompany-Ein- und -Ausgangstransaktionen verwalten
description: 'Intercompanytransaktionen, die Sie von Intercompanypartnern empfangen, werden im IC-Eingang aufgelistet, in dem Sie sie manuell oder automatisch bearbeiten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# Intercompany-Ein- und -Ausgangstransaktionen verwalten

Die Intercompanytransaktionen, die Sie auf elektronischem Wege von Intercompanypartnern empfangen, werden im **Intercompanyeingang** aufgelistet. Um zu erfahren, wie Sie eingehende Intercompany-Transaktionen verarbeiten, gehen Sie zu [Eingehende Intercompany-Transaktionen verarbeiten](#process-incoming-intercompany-transactions). Die Intercompanytransaktionen, die Sie auf elektronischem Wege von Intercompanypartnern empfangen, werden auf der Seite **Intercompanyausgang** aufgelistet. Um zu erfahren, wie Sie ausgehende Intercompany-Transaktionen verarbeiten, gehen Sie zu [Ausgehende Intercompany-Transaktionen verarbeiten](#to-process-outgoing-intercompany-transactions).

Abhängig von Ihrer Intercompany-Einrichtung werden einige Transaktionen jedoch automatisch verarbeitet. Sie können das Quellunternehmen und die Partnerunternehmen so einrichten, dass sie automatisch Belege und Journale erstellen, die Transaktionen entsprechen, die Partner über das Intercompany-Hauptbuch buchen. Um mehr über die Verwendung von Intercompany-Journalen zu erfahren, gehen Sie zu [Intercompany-Journal ausfüllen und buchen](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## Strukturieren des Eingangs  

Mit Hilfe der Filterfelder im oberen Bereich der Seite Eingang können Sie festlegen, welche Transaktionen auf der Seite angezeigt werden. Wenn Sie beispielsweise nur die von einem bestimmten Partner erstellten Transaktionen anzeigen möchten, können Sie die entsprechenden Filterkriterien in den Feldern **Transaktionsursprung** und **Intercompanypartnercode** verwenden.  

### Transaktionsursprung  

Welche Möglichkeiten Sie bei der Verwendung einer Transaktion haben, ist davon abhängig ob es sich dabei um eine Transaktion handelt, die:  

* Vom intercompanypartner erstellt oder  
* Vom intercompanypartner abgelehnt und an Sie zurückgesandt wurde.  

Das Feld **Transaktionsursprung anzeigen** kann zum Filtern der Transaktionen im Fenster **Intercompany-Eingangstransaktionen** verwendet werden, damit auf dieser Seite nur Transaktionen des festgelegten Typs angezeigt werden. Darüber hinaus können Sie nach Intercompanypartner oder nach dem Inhalt des Feldes **Zeilenaktion** filtern.  

#### Vom Intercompanypartner erstellt  

 Wenn Sie eine neue Transaktion empfangen, die vom Partner erstellt wurde, haben Sie folgende Möglichkeiten:

* Transaktion akzeptieren  
* Transaktion ablehnen (an Partner zurücksenden)  
* Transaktion abbrechen (löschen, ohne sie an den Partner zurückzusenden)  

#### Von Intercompanypartner zurückgesendet  

Wenn Ihr Intercompanypartner eine Transaktion ablehnt, können Sie sie nur im Eingang abbrechen. Anschließend müssen Sie Korrekturzeilen erstellen oder das Buch.-Blatt oder den Beleg im Unternehmen stornieren.  

## Neuerstellen von Eingangsposten  

Wenn Sie eine Transaktion im Eingang akzeptiert, anschließend aber den Beleg oder das Buch.-Blatt gelöscht haben, statt diese zu buchen, können Sie den Eingangsposten neu erstellen und erneut akzeptieren.  

## Eine Übersicht über die Intercompanytransaktionen eines bestimmten Zeitraums erhalten  

Die Intercompanytransaktionen, die Sie in einem bestimmten Zeitraum empfangen oder versendet haben, können in einer Übersicht angezeigt werden. Im Bericht **Intercompanytransaktionen** werden alle Intercompanysachposten, Debitorenposten und Kreditorenposten aufgelistet.

> [!NOTE]  
> Wenn sich die Intercompanypartner in derselben Datenbank befinden, können die Partner Transaktionen automatisch akzeptieren. Gehen Sie dann direkt zu den Seiten **Abgewickelte unternehmensinterne Posteingangstransaktionen** und **Abgewickelte unternehmensinterne Ausgangstransaktionen** . Weitere Informationen zum automatischen Akzeptieren von Transaktionen finden Sie unter [Transaktionen von Intercompany-Partnern automatisch akzeptieren](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Aktivieren Sie für den Synchronisationspartner auf der Seite **Unternehmensübergreifende Einrichtung** die Umschaltung **Automatisch. Senden-Transaktionen**.
> * Aktivieren Sie für Partnerunternehmen auf der Seite **Intercompany-Partner** die Umschaltung **Transaktionen automatisch annehmen**.  

## Intercompanytransaktionen aus einer Datei importieren

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Wenn einer der Intercompanypartner sich nicht in derselben Datenbank wie das eigene Unternehmen befindet, können die Intercompanytransaktionen von diesem Partner in einer XML-Datei empfangen werden. Anschließend werden die Transaktionen in den Eingang importiert.  

1. Speichern Sie die Datei in dem Verzeichnis, das Sie im Feld **Intercompanyeingangsdetails** angegeben haben, als Sie Intercompany eingerichtet haben.  
2. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompany-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.
3. Wählen Sie auf der Seite **Intercompany-Eingangstransaktionen** die **Transaktionsdatei importieren**-Aktion aus.  
4. Wählen Sie auf der angezeigten Seite die XML-Datei mit den Transaktionen aus, und wählen Sie dann **Öffnen**.  

Die Transaktionen werden in den Eingang importiert und können nun verarbeitet werden.

## Eingehende Intercompanytransaktionen verarbeiten  

Wenn Intercompanypartner Intercompanytransaktionen an Sie senden, werden diese Transaktionen im Intercompanyeingang abgelegt. Sie müssen die einzelnen Transaktionen im Eingang bewerten und entsprechend verarbeiten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompany-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intercompany-Eingangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Akzeptieren** aus, um die Zeile zu verarbeiten.
3. Füllen Sie auf der Seite **IC-Eingangsvorgang abschl.** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK**.  

Für Zeilen, die bei der Aktion akzeptieren verarbeitet wurden, werden Beleg- oder Buch.-Blattzeilen in Ihrem Unternehmen erstellt. Öffnen Sie die Belege oder Buch.-Blätter, nehmen Sie die erforderlichen Änderungen vor, und buchen Sie sie anschließend.  

Positionen, die Sie ablehnen und an Ihren Partner zurücksenden, werden an Ihren Intercompany-Ausgang weitergeleitet, wo Sie sie an Ihren Partner senden können.

Für Zeilen, die ein Partner zurückgewiesen und an Sie zurückgesendet hat, müssen Sie nun eine Korrektur in die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.

## So verarbeiten Sie ausgehende Intercompanytransaktionen  

Wenn Sie Intercompany-Buch.-Blätter oder -Belege buchen oder Intercompanybestellbestätigungen senden, werden die Transaktionen an den Intercompanyausgang gesendet. Damit sie an die Intercompanypartner gesendet werden, müssen Sie den Ausgang öffnen und die Transaktionen verarbeiten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompany-Ausgangstransaktionen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intercompany-Ausgangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Zurück in Eingang** aus, um die Zeile zu verarbeiten.

Verwenden Sie die **An Intercompanypartner senden**-Aktion verarbeiten, um die Zeilen an den Eingang des Partners zu senden.

Zeilen, die Sie mit der **Zurück in Eingang**-Aktion verarbeiten, werden in den Eingang verschoben, wo Sie sie akzeptieren können, um Belege oder Buch.-Blattzeilen in Ihrem Unternehmen zu erstellen.  

Wenn Sie die Aktion **Abbrechen** verwenden, müssen Sie nun eine Korrektur für die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.  

## So erstellen Sie Intercompanyeingangstransaktionen neu  

Gelegentlich sollten Sie eine Transaktion im Ein- oder Ausgang neu erstellen. Wenn Sie z. B. eine Transaktion im Eingang akzeptiert, den Beleg oder das Buch.-Blatt anschließend jedoch statt zu buchen gelöscht haben, können Sie den Eingangsposten erneut erstellen und akzeptieren.  

In der folgenden Schrittfolge wird beschrieben, wie Eingangstransaktionen neu erstellt werden. Bei Ausgangstransaktionen wird jedoch gleichermaßen verfahren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Bearbeitete IC-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Bearbeitete IC-Eingangstrans.** die Zeile mit der Transaktion aus, die im Eingang neu erstellt werden soll, und wählen Sie dann die Aktion **Eingangstransaktion neu erstellen** aus.  

## Siehe auch

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
