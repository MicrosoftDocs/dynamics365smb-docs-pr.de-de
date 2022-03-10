---
title: 'Vorgehensweise: Zuordnen von Artikeln | Microsoft Docs'
description: Die Zuordnungsfunktionalität ist verfügbar, wenn Sie Ihren Lagerort so eingerichtet haben, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 367dd6915a168b208432116439aa89b94bded649
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8128463"
---
# <a name="cross-dock-items"></a>Zuordnungselemente
Die Zuordnungsfunktionalität ist verfügbar, wenn Sie Ihren Lagerort so eingerichtet haben, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.  

Wenn Sie Artikel zuordnen, nehmen Sie sie an und liefern sie aus, ohne sie zwischendurch einzulagern, wodurch sich der Prozess der Einlagerung und Kommissionierung beschleunigt und die Bewegung der Artikel begrenzt wird. Sie können Artikel sowohl für den Warenausgang als auch für Fertigungsaufträge zuordnen. Wenn Sie einen Warenausgang vorbereiten oder Artikel für die Produktion kommissionieren und Sie Lagerplätze verwenden, kommissioniert die Anwendung automatisch die Artikel aus einem Zuordnungslagerplatz, bevor sie andere Lagerplätze berücksichtigt. Sie müssen im Zuordnungsbereich nachsehen, um festzustellen, ob die Artikel, die Sie benötigen, verfügbar sind, bevor Sie die Artikel aus ihrem normalen Lagerbereich holen.  

Wenn Sie Zuordnungsmengen berechnet haben, werden Einlagerungszeilen für den Zuordnungslagerplatz für Zuordnungsberechnungen erzeugt, wenn Sie den Wareneingang buchen. Andere Einlagerungszeilen werden wie üblich erzeugt.  

Wenn Sie die zugeordneten Artikel sofort buchen möchten, um sie für die Kommissionierung verfügbar zu machen, müssen Sie ebenfalls eine Einlagerung für die anderen Artikel aus der Wareneingangszeile, nämlich die, die eingelagert werden müssen, erfassen. Wenn nur einige der Artikel der Wareneingangszeile zugeordnet werden, müssen Sie sich daher bemühen, die anderen Artikel so schnell wie möglich einzulagern. Alternativ dazu kann Ihre Lagerpolitik so aussehen, dass Sie – wenn möglich – ganze Wareneingangszeilen zuordnen möchten.  

In der Einlagerungsanweisung können Sie zu Ihrem Vorteil Anweisungszeilen löschen (sowohl Zeilen der Art "Entnahme" als auch "Einlagerung" für jede Wareneingangszeile), die Wareneingänge betreffen, die vollständig eingelagert werden sollen. Diese Zeilen können später als Einlagerungszeilen aus dem Einlagerungsarbeitsblatt oder dem gebuchten Wareneingang erzeugt werden. Wenn sie gelöscht sind, können Sie die Zeilen, die Zuordnungsartikel betreffen, einlagern und registrieren.  

Wenn Sie das Feld **Einlagerungsarbeitsblatt verwenden** auf der Lagerortkarte ausgewählt und den Wareneingang mit berechneten Zuordnungen gebucht haben, werden alle Wareneingangszeilen im Arbeitsblatt verfügbar. Die Informationen zur Zuordnung sind verloren und können nicht wiederhergestellt werden. Wenn Sie daher die Zuordnungsfunktionalität nutzen möchten, sollten Sie Zeilen in das Einlagerungsarbeitsblatt übertragen, indem Sie Einlagerungsanweisungen löschen, anstatt die automatische Übertragungsfunktion im Feld **Einlagerungsarbeitsblatt verwenden** zu nutzen.  

Wenn Sie den Wareneingang buchen, und sich kein Häkchen im Feld **Einlagerungsarbeitsblatt verwenden** befindet, erscheinen die Artikel, die zugeordnet werden sollen, als einzelne Zeilen in der Einlagerungsanweisung. Das Feld **Zuordnungsinformation** in jeder Einlagerungszeile zeigt an, ob die Zeile zugeordnete Artikel, Artikel aus demselben Wareneingang, die alle eingelagert werden sollen, oder Artikel, die eingelagert werden sollen und aus einer Wareneingangszeile stammen, in der einige Artikel zugeordnet werden sollen, enthält. Mit diesem Feld können die Mitarbeiter schnell sehen, warum nicht die volle Menge eingelagert werden soll.  

Die Anwendung speichert keine eigenen Datensätze von Artikeln, die zugeordnet wurden, sondern erfasst sie als normale Einlagerungsanweisungen.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>So richten Sie die Logistik für Zuordnungen ein:  
1.  Richten Sie mindestens einen Zuordnungslagerplatz ein, wenn Sie Lagerplätze verwenden. Richten Sie eine Zuordnungszone ein, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden.  

    Bei einem Zuordnungslagerplatz ist das Feld **Zuordnungslagerplatz** ausgewählt, und es müssen die Lagerplatzarten **Wareneingang** und **Kommissionierung** ausgewählt sein. Weitere Informationen finden Sie unter [Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md) und [Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md).  

    Wenn Sie Zonen verwenden, erstellen Sie eine Zone für Ihre Zuordnungslagerplätze, und wählen Sie das Feld **Zuordnungslagerplatzzone** aus. Weitere Informationen finden Sie unter [Einrichten von Lagerplätzen](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerort** ein und wählen Sie dann den zugehörigen Link.  
3.  Öffnen Sie die Seite **Lagerort**, und wählen Sie den Lagerort aus, den Sie für das Lager bezüglich Zuordnungen einrichten möchten, und wählen Sie die Aktion **Bearbeiten** aus.  
4.  Wählen Sie im Inforegister **Lager** das Kontrollkästchen **Zuordnung verwenden** aus, und tragen Sie im Feld **Zuord.-Fälligkeitsdatum ber.** die Zeit für die Suche nach Zuordnungsmöglichkeiten ein.

    Die Option **Zuordnung verwenden** ist nur verfügbar, wenn die Felder **Wareneingang erforderlich**, **Warenausgang erforderlich**, **Kommissionierung erforderlich** und **Einlagerung erforderlich** ausgewählt sind.  

5.  Wenn Sie Lagerplätze verwenden, tragen Sie im Inforegister **Lagerplätze** in das Feld **Zuordnungslagerplatzcode** den Code des Lagerplatzes ein, der als Vorgabelagerplatz für Zuordnungen verwendet werden soll.  
6.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerhaltungsdaten Einheit** ein und wählen Sie den zugehörigen Link.  
7.  Für jeden Artikel oder alle Lagerhaltungsdaten, die Sie zur Zuordnung verwenden möchten, wählen Sie den Artikel aus, und wählen Sie die **Bearbeiten** Aktion aus.
8. Auf der Seite **Lagerhaltungsdatenkarte** wählen Sie das Kontrollkästchen **Zuordnung verwenden** aus.  

> [!NOTE]  
>  Die Zuordnung ist nur möglich, wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, ohne sich die Möglichkeiten anzeigen zu lassen:  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2.  Erstellen Sie Wareneingänge für einen Artikel, der angekommen ist und möglicherweise in Zuordnungen einbezogen werden kann. Weitere Informationen finden Sie unter [Entnahme von Artikeln](warehouse-how-receive-items.md).  
3.  Füllen Sie das Feld **Menge akt. Lieferung** aus, und wählen Sie dann die Aktion **Zuordnung berechnen** aus.  

    Ausgehende Herkunftsbelege, die die Artikel benötigen und die das Lager innerhalb der Datumsformelperiode verlassen sollen, werden identifiziert.  [!INCLUDE[prod_short](includes/prod_short.md)] berechnet Mengen, damit Sie soviel wie möglich zuordnen und auf diese Art vermeiden können, Artikel einzulagern, ohne zu viele Artikel im Zuordnungsbereich anzusammeln. Der Wert im Feld **Menge für Zuordnung** ist die Summe aller ausgehenden Zeilen, die den Artikel in der Vorausschauperiode benötigen, abzüglich der Menge der Artikel, die bereits in den Zuordnungsbereich eingelagert wurden. Oder es ist der Wert im Feld **Menge akt. Lieferung** in der Lieferzeile, je nachdem, welcher geringer ist. Sie können nicht mehr zuordnen, als Sie erhalten haben.  

4.  Wenn Sie die Menge wie vorgeschlagen zuordnen möchten, buchen Sie den Wareneingang. Sie können sich auch entscheiden, die zuzuordnende Menge auf einen höheren oder niedrigeren Wert zu setzen, und dann den Wareneingang zu buchen.  

    Die zuzuordnenden Mengen erscheinen jetzt als Zeilen in der Einlagerungsanweisung, vorausgesetzt, das Feld **Einlagerungsarbeitsblatt verwenden** ist deaktiviert. Die nicht zugeordneten Mengen werden auch Zeilen in der Einlagerungsanweisung.  

    Wenn Sie Lagerplätze verwenden, wurden die zugeordneten Artikel dem Vorgabe-Zuordnungslagerplatz zugeordnet, der auf der Artikelkarte festgelegt wurde.  

5.  Löschen Sie die Zeilen **Entnahme** und **Einlagerung** für Artikel, die nicht zugeordnet werden sollen.  
6.  Drucken Sie die Einlagerungsanweisungen für die übrigen Zeilen und lagern Sie die Mengen des Wareneingangs, die eingelagert werden sollen, in die jeweiligen Lagerplätze oder in einen geeigneten Bereich im Lager ein. Lagern Sie die zuzuordnenden Artikel in den Bereich oder Lagerplatz ein, der nach der Lagerpolitik für ihn vorgesehen ist. Es ist auch möglich, dass die Lagerrichtlinien vorsehen, dass Sie die Artikel einfach im Wareneingangsbereich lassen.  
7.  Wenn Sie zugeordnete Artikel als eingelagert und zum Kommissionieren registrieren möchten, wählen Sie die Aktion **Registrieren** aus.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, nachdem Sie die Verkaufschancen angezeigt haben:  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2.  Erstellen Sie Wareneingänge für einen Artikel, der angekommen ist und möglicherweise in Zuordnungen einbezogen werden kann. Weitere Informationen finden Sie unter [Entnahme von Artikeln](warehouse-how-receive-items.md).  

    Sie können sich die Herkunftsbelegzeilen ansehen, die den Artikel anfordern, bevor Sie den Wareneingang buchen.  
3.  Wählen Sie die Aktion **Zuordnung berechnen** aus.  

    Auf der Seite **Zuordnungsmöglichkeiten** können Sie die wichtigsten Details zu den Zeilen sehen, die den Artikel benötigen, wie z. B. die Belegart, die erforderliche Menge und das Fälligkeitsdatum. Diese Informationen können Ihnen bei der Entscheidung helfen, wo Sie die Artikel im Zuordnungsbereich einlagern und wie Sie sie gruppieren.  

4.  Wählen Sie die Aktion **Menge für Zuordnung autom. ausfüllen** aus, um anzeigen zu lassen, wie die die Mengen in den Wareneingangszeilen berechnet werden. Wenn Sie die Anzahl der Artikel im Feld **Menge für Zuordnung** in den einzelnen Zeilen ändern, wird die Berechnung aktualisiert, während Sie Änderungen vornehmen. Dies bedeutet nicht, dass der spezielle Warenausgang oder Fertigungsauftrag tatsächlich die Artikel, die für die Zuordnung vorgeschlagen wurden, erhalten wird, da diese Veränderungen nur zu Testzwecken vorgenommen werden. Der Prozess kann jedoch informativ sein, wenn mehr als eine Einheit beteiligt ist.  
5.  Wenn Sie eine Menge für den Artikel einer bestimmten Auftragszeile reservieren möchten, setzen Sie Ihren Cursor in diese Zeile und wählen Sie dann die Aktion **Reservieren** aus. Auf der Seite **Reservierung** können Sie jetzt eine verfügbare Menge des Artikels für diesen speziellen Auftrag reservieren. Diese Reservierung ist wie jede andere Reservierung und hat keine höhere Priorität, weil sie im Zusammenhang mit einer Zuordnung erstellt wurde. Weitere Informationen finden Sie unter [Entnahme von Artikeln](inventory-how-to-reserve-items.md).   
6.  Wenn Sie mit der Neuberechnung oder der Reservierung fertig sind, wählen Sie **OK**, um die überprüfte Berechnung in das Feld **Menge für Zuordnung** in der Wareneingangszeile zu bringen, oder klicken Sie auf **Abbrechen**, wenn Sie zum Wareneingang zurückkehren möchten, wo Sie die Zuordnung noch einmal berechnen können, wenn Sie möchten.  
7.  Buchen Sie jetzt den Wareneingang. Danach können Sie mit der Einlagerungsanweisung fortfahren, wie in den Schritten 3 bis 7 im Abschnitt "Um Artikel zuzuordnen, ohne sich die Möglichkeiten anzeigen zu lassen" beschrieben.  

> [!NOTE]  
>  In der Einlagerung können Sie fortfahren, die Mengen zu ändern – falls notwendig –, die eingelagert oder zugeordnet werden sollen. Sie können sich z. B. entscheiden, eine zusätzliche Menge zuzuordnen, um die Zuordnungsregistrierung zu beschleunigen.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>So zeigen Sie zugeordnete Artikel in Warenausgängen oder Kommissionierarbeitsblättern an:  
Wenn Sie Lagerplätze verwenden, können Sie jedes Mal, wenn Sie einen Warenausgang oder das Kommissionierarbeitsblatt öffnen, eine aktualisierte Berechnung der Menge jedes Artikels in den Zuordnungslagerplätzen sehen. Diese Information ist wertvoll, wenn Sie auf einen Artikel warten. Wenn Sie sehen, dass der Artikel in einem Zuordnungslagerplatz verfügbar ist, können Sie schnell eine Kommissionierung für alle Artikel des Warenausgangs erstellen. Im Kommissionierarbeitsblatt können Sie die Zeilen wie gewünscht ändern und dann eine Kommissionierung erstellen.  

Sie müssen die Artikel zuerst im Zuordnungsbereich suchen, wenn Sie Artikel für den Warenausgang kommissionieren. Wenn Sie sich beim Wareneingangsprozess die Herkunftsbelege notiert haben, die die Basis der Zuordnung waren, haben Sie einen besseren Überblick darüber, ob die Artikel im Zuordnungsbereich gefunden werden können oder nicht.  

Wenn ein Fertigungsauftrag freigegeben wurde, sind die Zeilen im Kommissionierarbeitsblatt verfügbar und Sie können dann im Feld **Menge in Zuord.-Lagerplätzen** sehen, ob die Artikel, auf die Sie warten, angekommen sind und in die zugeordneten Lagerplätze eingelagert wurden. Wenn Sie eine Kommissionieranweisung erstellen, schlägt die Anwendung vor, dass Sie zuerst die zugeordneten Artikel kommissionieren und erst dann in den festen Lagerplätzen nach weiteren Artikeln suchen.  

Wenn Sie keine Lagerplätze verwenden, müssen Sie daran denken, den Zuordnungsbereich von Zeit zu Zeit zu überprüfen, oder Sie müssen sich auf die Nachrichten aus dem Wareneingang verlassen, dass die Artikel für die Produktion angekommen sind.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]