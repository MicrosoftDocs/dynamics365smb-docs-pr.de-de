---
title: So lagern Sie Artikeln mit Lagereinlagerungen ein
description: 'Erfahren Sie mehr über die verschiedenen Möglichkeiten, Lagereinlagerungen zum Einlagern empfangener Artikel zu verwenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# Artikel mit Lagereinlagerungen einlagern

In [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie Artikel und lagern sie, wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden ein.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

Dieser Artikel bezieht sich auf Methode D in der Tabelle und geht davon aus, dass der Eingang bereits stattgefunden hat. Erfahren Sie mehr unter [Artikel empfangen](warehouse-how-receive-items.md).

Wenn ein Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, verwenden Sie Lagereinlagerungsbelege, um die zu steuern, wie Artikel eingelagert werden. Wenn Sie einen Wareneingang buchen, werden Herkunftsbelege wie Einkäufe, eingehende Umlagerungen oder Verkaufsreklamationen aktualisiert. Die eingegangene Menge wird in das Artikelbuch gebucht, und die Zeilen für die eingegangenen Artikel werden an die Einlagerungsfunktion im Lager gesendet.

Abhängig vom Wert im Feld **Einlagerungsarbeitsblatt verwenden** auf der **Lagerortskarte** werden die Zeilen entweder für das Einlagerungsarbeitsblatt zur Verfügung gestellt oder zur sofortigen Generierung von Einlagerungsbelegen verwendet. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).  

Zusätzlich zu den Standardoptionen für das Erstellen von Lagereinlagerungen, die in diesem Artikel beschrieben werden, können Sie Einlagerungen im zugehörigen gebuchten Wareneingang erstellen. Dies ist nützlich, wenn Sie die Einlagerungszeilen gelöscht haben, oder wenn Sie sich entschließen, das Einlagerungsarbeitsblatt nicht zu verwenden, da Sie Einlagerungsanweisungen aus gebuchte Wareneingangszeilen folgendermaßen erstellen oder wiedererstellen können.

## Zonen- und Lagerplatzcodes

An Lagerorten, die für die Verwendung der gesteuerten Einlagerung und Kommissionierung eingerichtet sind, sind die folgenden Einstellungen erforderlich, um den besten Ort für die Einlagerung dieser Artikel zu bestimmen.  

* So richten Sie eine Einlagerungsmethode ein: Weitere Informationen finden Sie unter [Einrichten von Aktivitätvorlagen](warehouse-how-to-set-up-put-away-templates.md).  
* Das Gewicht, Volumen und spezielle Lagerungsanforderungen des Artikels oder der Lagerhaltungsdaten werden festgelegt.
* Die Kapazität, der Lagerplatztyp und der Lagerplatzrang werden für die Lagerplätze definiert.  

Die Lagerplatzpriorität wird berücksichtigt, wenn mehr als ein Lagerplatz den Kriterien auf der Einlagerungsvorlage entspricht. Wenn für mehr als einen Lagerplatz die Kriterien der Einlagerungsvorlage und die Lagerplatzpriorität gleich sind, wird der Lagerplatz mit der höchsten Nummer ausgewählt.

## So erstellen Sie Einlagerungsbelege mit dem Einlagerungsarbeitsblatt in Masse  

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

Auf der Seite **Einlagerungsarbeitsblatt** können Sie Einlagerungsbelege für mehrere Belege gleichzeitig erstellen.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Einlagerungsarbeitsblätter** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die **Logistikbeleg holen** Aktion aus. Die Seite **Einlagerungsauswahl** wird geöffnet.  

    Die Liste enthält alle gebuchten Wareneingänge, die zur Einlagerung bereit sind, einschließlich derjenigen, für die bereits Einlagerungsanweisungen erstellt wurden. Belege mit Einlagerungszeilen, die bereits vollständig eingelagert und registriert wurden, werden in dieser Übersicht nicht angezeigt.  
3. Wählen Sie die Belege aus, die Sie bearbeiten möchten. Sie können gleichzeitig an Zeilen aus verschiedenen Belegen arbeiten.  

    > [!NOTE]  
    > Wenn Sie einen Beleg für einen Eingang oder eine interne Einlagerung auswählen, für den Sie bereits Anweisungen für alle Zeilen erstellt haben, informiert Sie [!INCLUDE[prod_short](includes/prod_short.md)]] darüber, dass es keine Mengen zu bewegen gibt.  

4. Füllen Sie das Feld **Sortiermethode** aus, um die Zeilen zu sortieren.  

    > [!NOTE]  
    > Die Art und Weise, wie die Zeilen im Arbeitsblatt sortiert sind, überträgt sich nicht automatisch auf die Einlagerungsanweisung. Es bestehen jedoch die gleichen Möglichkeiten zum Sortieren und Priorisieren der Lagerplätze. Sie können die Zeilenreihenfolge, die Sie im Arbeitsblatt planen, wiederherstellen, wenn Sie die Einlagerungsanweisungen sortieren.

5. Füllen Sie das Feld **Bewegungsmenge** aus. Wählen Sie die **Bewegungsmenge autom. ausfüllen** Aktion aus, oder füllen Sie die Felder manuell aus.  
6. Bearbeiten Sie diese Positionen bei Bedarf manuell. Sie können z. B. Zeilen löschen, wenn einige Artikel in einen Lagerplatz weit entfernt von den Lagerplätzen der anderen Artikel eingelagert werden müssen.  

    > [!NOTE]  
    > Wenn Sie Zeilen löschen, werden sie nur aus diesem Arbeitsblatt gelöscht. Sie werden nicht aus der Einlagerungsauswahl gelöscht.  

7. Wählen Sie die Aktion **Einlagerung erstellen** aus. Auf der Seite **Beleg erstellen**, das sich jetzt öffnet, können Sie weitere Informationen zu der Einlagerung hinzufügen, die Sie erstellen:  

    * Sie können die Einlagerung einem bestimmten Mitarbeiter zuordnen.  
    * Sie können die Einlagerungsanweisungszeilen so sortieren, wie Sie es im Arbeitsblatt getan haben oder nach Lagerplatzpriorität. Wenn Sie nach Lagerplatzrang sortieren, werden die *Entnahme*-Zeilen zuerst angezeigt, da die meisten Eingangslagerplätze einen Lagerplatzrang von 0 haben. Die *Ortszeilen* werden zuletzt angezeigt, beginnend mit den Lagerplätzen mit dem niedrigsten Lagerplatzrang. Wenn Sie Ihr Lager so strukturiert haben, dass sich Lagerplätze von ähnlicher Lagerplatzpriorität nebeneinander befinden, verkürzt eine auf diese Art durchgeführte Sortierung die Wege, die Lagermitarbeiter zurücklegen müssen.  
    * Sie können wählen, dass die Zeilen, die [!INCLUDE [prod_short](includes/prod_short.md)] erstellt hat, als es eine große Maßeinheit in kleinere Einheiten konvertiert hat, nicht eingeschlossen werden, indem Sie das Feld **Gebindeanbruchsfilter** festlegen wählen. Weitere Informationen zu Gebindeanbruch finden Sie unter [Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Sie können wählen, dass nicht automatisch das Feld **Bewegungsmenge** in den Einlagerungsanweisungen ausgefüllt wird.  
    * Sie können sich entscheiden, den Beleg sofort zu drucken.  

8. Wählen Sie **OK**, um die Einlagerung zu erstellen.  

## Um eine Einlagerung aus dem gebuchten Wareneingang zu erstellen

Wenn für einen Lagerort die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist und Sie die Einlagerungszeilen gelöscht haben, oder wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden und sich entschieden haben, den Einlagerungsvorschlag nicht zu verwenden, können Sie Einlagerungsanweisungen für gebuchte Wareneingangszeilen folgendermaßen erstellen oder wiedererstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Geb. Wareneingänge** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie eine einzulagernden gebuchten Eingang aus.  
3. Wählen Sie die Aktion **Karte** aus.  

    Wenn das Feld **Belegstatus** leer ist, wurde der Wareneingang noch nicht eingelagert. Sonst zeigt das Feld an, ob der Wareneingang teilweise oder komplett eingelagert wurde.  

4. Wenn der Wareneingang teilweise oder überhaupt nicht eingelagert wurde, wählen Sie die Aktion **Einlagerung erstellen** aus.  
5. Füllen Sie die Felder wie erforderlich aus, und wählen Sie **OK** aus.  

## So lagern Sie Artikel ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Geben Sie **Lagereinlagerungen** ein, und wählen Sie dann den zugehörigen Link.

2. Öffnen Sie die Wareneinlagerung, die für die Bearbeitung bereit ist.  
3. Geben Sie, sofern für Ihr Lager erforderlich ist, Ihre Benutzerkennung ein, wenn Sie mit der Arbeit an einer Einlagerung beginnen.  

    Sie können den Einlagerungszeilen nach verschiedenen Kriterien sortieren, beispielsweise nach Artikel, Regalnummer, Lagerplatz oder Fälligkeitsdatum. Die Sortierung kann helfen, den Einlagerungsprozess zu optimieren, zum Beispiel:

    * Wenn die Zeilen der Art Entnahme und Einlagerung einer Wareneingangszeile nicht direkt aufeinander folgen, Sie dies aber wünschen, sortieren Sie die Zeilen, indem Sie **Artikel** im Feld **Sortiermethode** auswählen.  
    * Wenn Lagerplatzränge das physische Layout des Lagers widerspiegeln, verwenden Sie die Sortiermethode **Lagerplatzrang**, um die Arbeit nach Lagerplatzlagerorten zu organisieren.

  > [!NOTE]  
  > Die Zeilen sind in der Reihenfolge der ausgewählten Kriterien aufsteigend sortiert. Wenn Sie nach Belegen sortieren, erfolgt die Sortierung zunächst nach Belegart basierend auf dem Feld **Quellbeleg der Lageraktivität**. Wenn Sie nach Lieferadresse sortieren, erfolgt die Sortierung zuerst nach Zieltyp basierend auf dem Feld **Lagerzieltyp**.

4. Führen Sie die Aktionen duch.

    Wenn ein Lagerplatzcode für die Lagerplätze obligatorisch ist, wird jede Wareneingangszeile wie folgt zu mindestens zwei Zeilen in der Lagereinlagerung.  

    * Die erste Zeile mit dem Feld **Entnahme** im Feld **Aktionsart** zeigt an, wo sich die Artikel im Wareneingangsbereich befinden. Sie können die Zone und den Lagerplatz in dieser Zeile nicht ändern.  
    * Die nächste Zeile, mit **Einlagerung** in der **Aktionsart** zeigt an, wo Sie die Artikel im Lager einlagern müssen. Wenn Sie eine große Menge an Artikeln in einer Wareneingangszeile erhalten, müssen Sie die Artikel möglicherweise in mehrere Lagerplätze einlagern und es gibt eine Zeile der Art Einlagerung für jeden Lagerplatz. 

    > [!NOTE]
    > Wenn Sie die Artikel für eine Zeile in mehr als einem Lagerplatz platzieren müssen, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.

5. Wenn Sie alle Artikel so in die Lagerplätze eingelagert haben, wie es die Anweisungen vorsehen, wählen Sie die Aktion **Einlagerung registrieren** aus.  

## Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
