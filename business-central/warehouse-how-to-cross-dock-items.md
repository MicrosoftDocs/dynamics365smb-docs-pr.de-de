---
title: Zuordnungselemente
description: 'Erfahren Sie, wie Sie Artikel empfangen und versenden, ohne sie einzulagern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a><a name="cross-dock-items"></a><a name="cross-dock-items"></a>Zuordnungselemente

Cross-Docking-Artikel sind Artikel, die Sie erhalten und versenden, ohne sie einzulagern. Die Einlagerungs- und Kommissionierungsprozesse erfordern eine begrenzte Handhabung von Artikeln. Sie können Artikel für den Warenausgang als auch für Fertigungsaufträge zuordnen.

## <a name="cross-dock-bins-and-zones"></a><a name="cross-dock-bins-and-zones"></a><a name="cross-dock-bins-and-zones"></a>Zuordnungslagerplätze und-zonen

Wenn Sie Lagerplätze verwenden, richten Sie mindestens einen Zuordnungslagerplatz ein und geben dann den Lagerplatz im Feld **Cross-Docking-Lagerplatzcode** an Ihren Lagerorten an. Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, richten SIe eine Zuordnungszone ein.

Wenn Sie einen Warenausgang vorbereiten oder Artikel für die Produktion kommissionieren und Sie Lagerplätze verwenden, kommissioniert die Anwendung automatisch die Artikel aus einem Zuordnungslagerplatz, bevor sie andere Lagerplätze berücksichtigt. Sie müssen im Zuordnungsbereich nachsehen, um festzustellen, ob die Artikel, die Sie benötigen, verfügbar sind, bevor Sie die Artikel aus ihrem normalen Lagerbereich holen.  

Wenn Sie Zuordnungsmengen berechnet haben, werden Einlagerungszeilen für den Zuordnungslagerplatz für Zuordnungsberechnungen erzeugt, wenn Sie den Wareneingang buchen. Andere Einlagerungszeilen werden wie üblich erzeugt.  

## <a name="cross-dock-select-lines-for-a-receipt"></a><a name="cross-dock-select-lines-for-a-receipt"></a><a name="cross-dock-select-lines-for-a-receipt"></a>Zuordnungsauswahlpositionen für einen Eingang

Wenn Sie die zugeordneten Artikel sofort buchen möchten, um sie für die Kommissionierung verfügbar zu machen, müssen Sie ebenfalls eine Einlagerung für die anderen Artikel aus der Wareneingangszeile, nämlich die, die eingelagert werden müssen, erfassen. Wenn nur einige der Artikel der Wareneingangszeile zugeordnet werden, müssen Sie sich daher bemühen, die anderen Artikel so schnell wie möglich einzulagern. Alternativ dazu kann Ihre Lagerpolitik so aussehen, dass Sie – wenn möglich – ganze Wareneingangszeilen zuordnen möchten.

Löschen Sie in der Einlagerungsanweisung die Entnahme- und Kommissionierungsanweisungszeilen für jede Wareneingangszeile für die einzulagernden Artikel. Sie können die Anweisungszeilen später als Einlagerungszeilen aus dem Einlagerungsarbeitsblatt oder dem gebuchten Wareneingang neu erzeugen. Nachdem Sie die Anweisungszeilen gelöscht haben, können Sie die Zeilen, für Zuordnungsartikel einlagern und registrieren.  

## <a name="about-the-put-away-worksheet-page"></a><a name="about-the-put-away-worksheet-page"></a><a name="about-the-put-away-worksheet-page"></a>Infos zur Einlagerungsarbeitsblattseite

Wenn Sie den Schalter **Einlagerungsarbeitsblatt verwenden** auf der Seite **Lagerortkarte** aktivieren und den Wareneingang mit berechneten Zuordnungen gebucht haben, werden alle Wareneingangszeilen im Arbeitsblatt verfügbar. Die Informationen zur Zuordnung sind verloren und können nicht wiederhergestellt werden. Um also die Zuordnungsfunktionalität zu nutzen, sollten Sie Zeilen in das Einlagerungsarbeitsblatt übertragen, indem Sie Einlagerungsanweisungen löschen, anstatt die automatische Übertragungsfunktion im Feld **Einlagerungsarbeitsblatt verwenden** zu nutzen.  

Wenn Sie den Wareneingang buchen, und der Schalter **Einlagerungsarbeitsblatt verwenden** deaktiviert ist, werden die Cross-Docking-Artikel zu einzelne Zeilen in der Einlagerungsanweisung. Das Feld **Cross-Dock-Informationen** auf jeder Einlagerungsposition zeigt an, ob die Zeile Folgendes enthält:

* Zuordnungsartikel.
* Alle Artikel einer Eingangs müssen gelagert werden.
* Einige Artikel aus einem Wareneingang müssen gelagert werden, und andere sollen Cross-Docking sein.

[!INCLUDE [prod_short](includes/prod_short.md)] führt keine separaten Aufzeichnungen für Cross-Docking-Artikel. Es registriert sie als gewöhnliche Einlagerungsanweisungen.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a><a name="to-set-up-the-warehouse-for-cross-docking"></a><a name="to-set-up-the-warehouse-for-cross-docking"></a>So richten Sie die Logistik für Zuordnungen ein:

1. Wenn Sie Lagerplätze verwenden, richten Sie mindestens einen Zuordnungslagerplatz ein. Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, richten SIe eine Zuordnungszone ein.  

    Bei einem Zuordnungslagerplatz ist das Feld **Zuordnungslagerplatz** ausgewählt, und es müssen die Lagerplatzarten **Wareneingang** und **Kommissionierung** ausgewählt sein. Weitere Informationen zu Behältern finden Sie unter [Behälter erstellen](warehouse-how-to-create-individual-bins.md) und [Ablagetypen einrichten](warehouse-how-to-set-up-bin-types.md).  

    Wenn Sie Zonen verwenden, erstellen Sie eine Zone für Ihre Zuordnungslagerplätze, und wählen Sie das Feld **Zuordnungslagerplatzzone** aus. Weitere Informationen zum Einrichten von Zonen finden Sie unter [Lagerorte mithilfe von Behältern einrichten](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerort** ein und wählen Sie dann den zugehörigen Link.  
3. Öffnen Sie die Seite **Lagerort**, und wählen Sie den Lagerort aus, den Sie für das Lager bezüglich Zuordnungen einrichten möchten, und wählen Sie die Aktion **Bearbeiten** aus.  
4. Aktivieren Sie im Inforegister **Lager** den Schalter **Zuordnung verwenden**, und tragen Sie im Feld **Zuord.-Fälligkeitsdatum ber.** die Zeit für die Suche nach Zuordnungsmöglichkeiten ein.

    Die Option **Zuordnung verwenden** ist nur verfügbar, wenn die Felder **Wareneingang erforderlich**, **Warenausgang erforderlich**, **Kommissionierung erforderlich** und **Einlagerung erforderlich** ausgewählt sind.  

5. Wenn Sie Lagerplätze verwenden, tragen Sie im Inforegister **Lagerplätze** in das Feld **Zuordnungslagerplatzcode** den Code des Lagerplatzes ein, der als Vorgabelagerplatz für Zuordnungen verwendet werden soll.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerhaltungsdaten Einheit** ein und wählen Sie den zugehörigen Link.  
7. Für jeden Artikel oder alle Lagerhaltungsdaten, die Sie zur Zuordnung verwenden möchten, wählen Sie den Artikel aus, und wählen Sie die **Bearbeiten** Aktion aus.
8. Auf der Seite **Lagerhaltungsdatenkarte** wählen Sie das Kontrollkästchen **Zuordnung verwenden** aus.  

> [!NOTE]  
>  Die Zuordnung ist nur möglich, wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a><a name="to-cross-dock-items-without-viewing-the-opportunities"></a><a name="to-cross-dock-items-without-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, ohne sich die Möglichkeiten anzeigen zu lassen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie Lagerbelege für einen Artikel, der angekommen ist und möglicherweise in Zuordnungen einbezogen werden kann. Weitere Informationen zu Eingängen finden Sie unter [Artikeleinkang](warehouse-how-receive-items.md).  
3. Füllen Sie das Feld **Menge akt. Lieferung** aus, und wählen Sie dann die Aktion **Zuordnung berechnen** aus.  

    Ausgehende Herkunftsbelege, die die Artikel benötigen und die das Lager innerhalb der Datumsformelperiode verlassen sollen, werden identifiziert. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet Mengen, damit Sie soviel wie möglich zuordnen und auf diese Art vermeiden können, Artikel einzulagern, ohne zu viele Artikel im Zuordnungsbereich anzusammeln. Der Wert im Feld **Menge für Zuordnung** ist die Summe aller ausgehenden Zeilen für den Artikel in der Vorausschauperiode abzüglich der Menge der Artikel, die bereits in den Zuordnungsbereich eingelagert wurden. Oder es ist der Wert im Feld **Menge akt. Lieferung** in der Lieferzeile, je nachdem, welcher geringer ist. Sie können nicht mehr zuordnen, als Sie erhalten haben.  

4. Wenn Sie die Menge wie vorgeschlagen zuordnen möchten, buchen Sie den Wareneingang. Sie können sich auch entscheiden, die zuzuordnende Menge auf einen höheren oder niedrigeren Wert zu setzen, und dann den Wareneingang zu buchen.  

    Die zuzuordnenden Mengen erscheinen jetzt als Zeilen in der Einlagerungsanweisung, vorausgesetzt, das Feld **Einlagerungsarbeitsblatt verwenden** ist deaktiviert. Die nicht zugeordneten Mengen werden auch Zeilen in der Einlagerungsanweisung.  

    Wenn Sie Lagerplätze verwenden, wurden die zugeordneten Artikel dem Vorgabe-Zuordnungslagerplatz zugeordnet, der auf der Artikelkarte festgelegt wurde.  

5. Löschen Sie die Zeilen **Entnahme** und **Einlagerung** für Artikel, die Sie nicht zuordnen möchten.  
6. Drucken Sie die Einlagerungsanweisungen für die übrigen Zeilen und lagern Sie die Mengen des Wareneingangs, die eingelagert werden sollen, in die jeweiligen Lagerplätze oder in einen geeigneten Bereich im Lager ein. Lagern Sie die zuzuordnenden Artikel in den Bereich oder Lagerplatz ein, der nach der Lagerpolitik für ihn vorgesehen ist. Es ist auch möglich, dass die Lagerrichtlinien vorsehen, dass Sie die Artikel einfach im Wareneingangsbereich lassen.  
7. Wenn Sie zugeordnete Artikel als eingelagert und zum Kommissionieren registrieren möchten, wählen Sie die Aktion **Registrieren** aus.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a><a name="to-cross-dock-items-after-viewing-the-opportunities"></a><a name="to-cross-dock-items-after-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, nachdem Sie die Verkaufschancen angezeigt haben:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie Lagerbelege für einen Artikel, der angekommen ist und möglicherweise in Zuordnungen einbezogen werden kann.  

    Sie können sich die Herkunftsbelegzeilen ansehen, die den Artikel anfordern, bevor Sie den Wareneingang buchen.  
3. Wählen Sie die Aktion **Zuordnung berechnen** aus.  

   Auf der Seite **Zuordnungsmöglichkeiten** können Sie die wichtigsten Details zu den Zeilen sehen, die den Artikel benötigen, wie z. B. die Belegart, die erforderliche Menge und das Fälligkeitsdatum. Diese Informationen können Ihnen bei der Entscheidung helfen, wo Sie die Artikel im Zuordnungsbereich einlagern und wie Sie sie gruppieren.  

4. Wählen Sie die Aktion **Menge für Zuordnung autom. ausfüllen** aus, um anzeigen zu lassen, wie die die Mengen in den Wareneingangszeilen berechnet werden. Wenn Sie die Anzahl der Artikel im Feld **Menge für Zuordnung** in den einzelnen Zeilen ändern, wird die Berechnung aktualisiert, während Sie Änderungen vornehmen. Die Aktualisierung bedeutet nicht, dass die Lieferung oder der Produktionsauftrag tatsächlich die Artikel erhält, die für das Cross-Docking vorgeschlagen werden. Das Feld dient nur zu Informationszwecken. Der Prozess kann jedoch informativ sein, wenn mehr als eine Einheit beteiligt ist.  
5. Um eine Menge von Artikel für eine Auftragszeile zu reservieren, wählen Sie die Aktion **Reservieren** aus. Reservieren Sie auf der Seite **Reservierung** die verfügbare Menge des Artikels. Die Reservierung ist wie jede andere Reservierung und hat keine höhere Priorität, weil sie im Zusammenhang mit einer Zuordnung erstellt wurde. Weitere Informationen zu Reservierungen finden Sie unter [Artikel reserrvieren](inventory-how-to-reserve-items.md).   
6. Wenn Sie mit der Neuberechnung oder der Reservierung fertig sind, wählen Sie **OK**, um die überprüfte Berechnung in das Feld **Menge für Zuordnung** in der Wareneingangszeile zu bringen, oder klicken Sie auf **Abbrechen**, wenn Sie zum Wareneingang zurückkehren möchten, wo Sie die Zuordnung noch einmal berechnen können, wenn Sie möchten.  
7. Buchen Sie den Wareneingang. Sie können mit der Einlagerungsanweisung fortfahren, wie in den Schritten 3 bis 7 im Abschnitt [Um Artikel zuzuordnen, ohne sich die Möglichkeiten anzeigen zu lassen](#to-cross-dock-items-without-viewing-the-opportunities) beschrieben.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > In der Einlagerung können Sie fortfahren, die Mengen zu ändern – falls notwendig –, die eingelagert oder zugeordnet werden sollen. Sie können sich z. B. entscheiden, eine zusätzliche Menge zuzuordnen, um die Zuordnungsregistrierung zu beschleunigen.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a><a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a><a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>So zeigen Sie zugeordnete Artikel in Warenausgängen oder Kommissionierarbeitsblättern an:

Wenn Sie Lagerplätze verwenden, können Sie jedes Mal, wenn Sie einen Warenausgang oder den Kommissioniervorschlag öffnen, eine aktualisierte Berechnung der Menge jedes Artikels in den Zuordnungslagerplätzen sehen. Wenn Sie sehen, dass der Artikel in einem Zuordnungslagerplatz verfügbar ist, können Sie schnell eine Kommissionierung für alle Artikel des Warenausgangs erstellen. Im Auswahlarbeitsblatt können Sie die Zeilen nach Bedarf bearbeiten.  

Wenn ein Fertigungsauftrag freigegeben wurde, sind die Zeilen im Kommissioniervorschlag verfügbar und Sie können im Feld **Menge in Zuord.-Lagerplätzen** sehen, ob die Artikel, auf die Sie warten, angekommen sind und in die zugeordneten Lagerplätze eingelagert wurden. Wenn Sie eine Entnahmeanweisung erstellen, schlägt [!INCLUDE [prod_short](includes/prod_short.md)] vor, dass Sie zuerst die Cross-Docked-Artikel auswählen. Anschließend werden Artikel in Lagerplätzen vorgeschlagen.  

Wenn Sie keine Lagerplätze verwenden, müssen Sie daran denken, den Zuordnungsbereich von Zeit zu Zeit zu überprüfen, oder Sie müssen sich auf die Nachrichten aus dem Wareneingang verlassen, dass die Artikel für die Produktion angekommen sind.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
