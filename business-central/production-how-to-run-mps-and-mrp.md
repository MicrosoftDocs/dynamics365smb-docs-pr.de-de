---
title: "Wie die volle Programmplanung, MPS und MRP ausgeführt wird | Microsoft Docs"
description: "Die Begriffe \"Planungsvorschlag ausführen\" und \"Nettobedarf ausführen\" beziehen sich auf die Berechnung des Produktionsplans und der Materialbedarfe auf Basis des tatsächlichen und des geplanten Bedarfs. Das Planungssystem kann entweder die Prod.-Programmplanung (Master Planning Schedule, MPS) oder den Nettobedarf (Materialbedarfsplanung, Material Requirements Planning, MRP) auf Anforderung oder beides gleichzeitig berechnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4fe4c7eaf412bd6219b51a06f989c5a8508c4410
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="run-full-planning-mps-or-mrp"></a>Führen Sie eine vollständige Planung, Prod.-Programmplanung oder Nettobedarf aus
Die Begriffe "Planungsvorschlag ausführen" und "Nettobedarf ausführen" beziehen sich auf die Berechnung des Produktionsplans und der Materialbedarfe auf Basis des tatsächlichen und des geplanten Bedarfs. Das Planungssystem kann entweder die Prod.-Programmplanung (Master Planning Schedule, MPS) oder den Nettobedarf (Materialbedarfsplanung, Material Requirements Planning, MRP) auf Anforderung oder beides gleichzeitig berechnen.  

-   Prod.-Programmplanung ist die Berechnung eines Produktionsplans, der auf dem tatsächlichen Bedarf und der Absatzplanung basiert. Die Berechnung der Produktionsprogrammplanung wird für Endartikel mit einer Planung oder einer Verkaufsauftragszeile durchgeführt. Diese Artikel werden als „Prod.-Programmplanungsartikel” bezeichnet und werden dynamisch gekennzeichnet, wenn die Berechnung gestartet wird.  
-   Nettobedarf ist die Berechnung der Materialbedarfe auf Basis des tatsächlichen Bedarfs für Komponenten sowie der Absatzplanung auf Komponentenebene. Der Nettobedarf wird nur für Artikel berechnet, die keine Prod.-Programmplanungsartikel sind. Der Hauptzweck einer Nettobedarfsplanung besteht darin, terminierte formale Pläne je nach Artikeln aufzustellen, um den richtigen Artikel zur richtigen Zeit am richtigen Ort in der richtigen Menge bereitzustellen.  

Sowohl für die Prod.-Programmplanung (MPS) als auch für den Nettobedarf (MRP) wird derselbe Planungsalgorithmus verwendet. Der Planungsalgorithmus betrifft den Bestandsabgleich, die Wiederverwendung vorhandener Beschaffungsaufträge sowie die Ereignismeldungen. Der Planungssystemprozess untersucht, welche Mengen momentan oder zukünftig benötigt werden (Bedarf) und welche Mengen verfügbar sind oder erwartet werden (Vorrat). Wenn diese Mengen saldiert werden, gibt [!INCLUDE[d365fin](includes/d365fin_md.md)] Ereignismeldungen. Eine Ereignismeldung ist ein Vorschlag, einen neuen Auftrag zu erstellen, einen Auftrag zu ändern (Menge oder Datum) oder einen Auftrag zu stornieren. Der Begriff "Auftrag" umfasst Fertigungsaufträge, Einkaufsbestellungen, Herstellungsaufträge und Umlagerungsaufträge.

Die Links, die durch das Planungsmodul zwischen Bedarf und dem zugehörigen Bedarf erstellt werden, können im **Bedarfsverursacher** erzeugt werden. Weitere Informationen finden Sie unter [Titel-Beziehungen zwischen Bedarf und Vorrat nachverfolgen](production-how-track-demand-supply.md).   

Korrekte Planungsergebnisse hängen von der Einrichtung ab, die auf Artikelkarten, Montagestücklisten, Fertigungsstücklisten und Arbeitsplänen vorgenommen wurde.  

## <a name="methods-for-generating-a-plan"></a>Methoden zum Generieren eines Plans  

-   **Neuplanung berechnen:** Diese Funktion verarbeitet oder erneuert den gesamten Materialplan. Dieser Vorgang beginnt damit, dass alle momentan geladenen Beschaffungsaufträge gelöscht werden. Alle Artikel in der Datenbank werden neu geplant.  
-   **Änderungsplanung berechnen**: Diese Funktion verarbeitet eine Änderungsplanung. Artikel werden in einer Änderungsplanung von zwei Arten von Änderungen aus gesehen:  
    - **Bedarfs-/Vorratsänderungen**: Hierzu gehören Änderungen an Mengen für Verkaufsaufträge, Absatzplanungen, Montageaufträge oder Einkaufsbestellungen. Auch eine ungeplante Lagerbestandsänderung wird als Mengenänderung angesehen.  
    - **Planungsparameteränderungen**: Hierzu gehören Änderungen am Sicherheitsbestand, am Minimalbestand, am Arbeitsplan und an der Stückliste sowie Änderungen am Bestellzyklus oder an der Beschaffungszeit.  
-   **Aktionsmeldungen abrufen**: Diese Funktion fungiert als kurzfristiges Planungstool, indem sie Ereignismeldungen ausgibt, die den Benutzer über sämtliche Änderungen informieren, die seit der letzten Berechnung der Neuplanung oder der Änderungsplanung vorgenommen wurden.  

Bei jeder Planungsmethode generiert [!INCLUDE[d365fin](includes/d365fin_md.md)] Vorschlagsposten, wobei unbegrenzte Kapazität angenommen wird. Die Arbeitsplatz- und Arbeitsplatzgruppenkapazitäten werden nicht berücksichtigt, wenn Sie Schemata entwickeln.  

> [!IMPORTANT]  
>  Die Funktion Neuplanung errechnen ist der Prozess, der am häufigsten verwendet wird. Die Funktionen zum Berechnen und Ausführen von Ereignismeldungen können dagegen dazu verwendet werden, die Funktion "Änderungsplanungsvorgang berechnen" auszuführen.  
>   
>  Die Funktion "Ereignismeldungen abrufen" kann zwischen dem Ausführen einer Änderungsplanung und einer Neuplanung ausgeführt werden, um sofort sehen zu können, wie sich Planänderungen auswirken, ist aber nicht dazu vorgesehen, die Änderungsplanung oder Neuplanung zu ersetzen.  

## <a name="to-calculate-the-planning-worksheet"></a>Planungsvorschlag berechnen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Planungsvorschlag** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die **Neuplanung berechnen** Aktion aus, um das Fenster **Planung berechnen** zu öffnen.  
3.  Füllen Sie im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Wählen Sie diese Option aus, um die Berechnung eines Produktionsplans zu initiieren. Artikel, für die es offene Verkaufsaufträge und/oder Absatzplanungen gibt, werden in diesem Lauf berücksichtigt.|  
    |**MRP**|Wählen Sie diese Option aus, um die Berechnung der Materialbedarfsplanung zur initiieren. Artikel mit abhängigem Bedarf werden in diesem Lauf berücksichtigt. Normalerweise werden die Prod.-Programmplanung und der Nettobedarf gleichzeitig ausgeführt. Damit Prod.-Programmplanung und Nettobedarf gleichzeitig ausgeführt werden können, muss das Kontrollkästchen **Prod.-Prog.Pl./Nettobed. komb.** im Inforegister **Planung** im Fenster **Produktion Einrichtung** aktiviert sein.|  
    |**Startdatum**|Über dieses Datum wird die Lagerverfügbarkeit bewertet. Wenn die für einen Artikel verfügbare Menge unter dem Minimalbestand liegt (am Auftragsdatum), wird ab diesem Datum ein Beschaffungsauftrag vorausgeplant. Ist die Menge eines Artikels kleiner als dessen Sicherheitsbestand (am Auftragsdatum), wird ein Beschaffungsauftrag rückgesetzt, der am Auftragsstartdatum fällig ist.|  
    |**Enddatum**|Dies ist das Enddatum des Planungszeitraums. Nach diesem Datum wird weder Bedarf noch Vorrat berücksichtigt. Erstreckt sich der Bestellzyklus eines Artikels über das Enddatum hinaus, ist sich der effektive Planungszeitraum für diesen Artikel gleich Auftragsdatum + Bestellzyklus.<br /><br /> Der Planungszeitraum (-horizont) ist die Zeitspanne, über die sich der Plan erstreckt. Ist dieser Zeitraum zu kurz, werden Artikel mit längerer Beschaffungszeit nicht rechtzeitig bestellt. Ist dieser Zeitraum zu lang, wird zu viel Zeit mit dem Auswerten und Verarbeiten von Informationen verbracht, die sich wahrscheinlich geändert haben, bevor sie benötigt werden. Es ist möglich, einen Planungszeitraum für die Fertigung und einen längeren Planungszeitraum für Einkäufe festzulegen (dies ist aber nicht erforderlich). Ein Planungszeitraum für Einkäufe und Fertigung sollte so festgelegt sein, dass er die kumulierte Beschaffungszeit für Komponenten abdeckt.|  
    |**Abbrechen und ersten Fehler anzeigen**|Wählen Sie diese Option aus, wenn die Planung beendet werden soll, sobald ein Fehler auftritt. Gleichzeitig wird eine Meldung angezeigt, die Informationen zu dem ersten Fehler enthält. Gibt es einen Fehler, werden im Planungsvorschlag nur die Planungszeilen angezeigt, die vor dem Fehler erfolgreich erstellt wurden. Wenn Sie dieses Feld nicht auswählen, wird der Batchauftrag **Planung berechnen** vollständig ausgeführt, d. h., er wird nicht wegen Fehlern abgebrochen. Wenn Fehler vorliegen, wird nach dem Abschluss eine Meldung angezeigt und angegeben, wie viele Artikel betroffen sind. Danach wird das Fenster **Planungsfehlerprotokoll** angezeigt, in dem weitere Informationen zu den Fehlern sowie den Verknüpfungen für die betroffenen Artikelkarten bereitgestellt werden.|  
    |**Planung verwenden**|Wählen Sie eine Planung aus, die als Bedarf einbezogen werden soll, wenn Sie den Planungsbatchauftrag ausführen. Die Standardplanung wird im Inforegister **Planung** im Fenster **Produktion Einrichtung** eingerichtet.|  
    |**Planung vorher ausschließen**|Definieren Sie, welcher Umfang der ausgewählten Planung im Planungslauf berücksichtigt werden soll, indem Sie ein Datum eingeben, vor dem kein Planungsbedarf berücksichtigt wird. Auf diese Weise können Sie alte Informationen ausschließen.|  
    |**Planungsparameter für Ausnahmewarnungen berücksichtigen**|Dieses Feld ist standardmäßig ausgewählt.<br /><br /> Der Vorrat in Planungszeilen mit Warnungen wird normalerweise nicht gemäß den Planungsparametern geändert. Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken. Sie können jedoch bestimmte Planungsparameters festlegen, sodass Planungszeilen mit bestimmten Warnungen berücksichtigt werden können.<br /><br />|  

4.  Im Inforegister **Artikel** können Sie die Planungsroutinen auf Basis von Artikel, Artikelbeschreibung oder Lagerort filtern und ausführen.  
5.  Wählen Sie die Schaltfläche **OK** aus. Die Stapelverarbeitung wird ausgeführt, und anschließend werden die Planungszeilen in den Planungsvorschlag geschrieben.  

## <a name="to-perform-action-messages"></a>Ereignismeldungen ausführen  
1.  Im Fenster **Bestellauftrags-Arbeitsblatt** wählen Sie Aktion **Aktionsnachricht ausführen**.  
2.  Geben Sie im Inforegister **Optionen** an, wie die Lieferungen erstellt werden sollen. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Fertigungsauftrag**|Geben Sie an, wie Sie Fertigungsaufträge erstellen möchten. Sie können dies direkt von den Planungszeilenvorschlägen aus durchführen. Sie können entweder geplante oder fest geplante Fertigungsaufträge erstellen.|  
    |**Montageauftrag**|Geben Sie an, wie Sie Montageaufträge erstellen möchten. Sie können dies direkt von den Planungszeilenvorschlägen aus durchführen.|  
    |**Bestellung**|Geben Sie an, wie Sie Einkaufsbestellungen erstellen möchten. Sie können dies direkt von den Planungszeilenvorschlägen aus durchführen.<br /><br /> Wenn Sie die Planungszeilen Bestellvorschläge in das Anforderungsdatenblatt kopieren wollen, dann wählen Sie die Vorlagen und den Datenblattnamen aus.|  
    |**Umlagerungsauftrag**|Geben Sie an, wie Sie Umlagerungsaufträge erstellen möchten. Sie können dies direkt von den Planungszeilenvorschlägen aus durchführen.<br /><br /> Wenn Sie die Planungszeilen Umlagerungsvorschläge in das Anforderungsdatenblatt kopieren wollen, dann wählen Sie die Vorlagen und den Datenblattnamen aus.|  
    |**Umbuchungsaufträge zusammenfassen**|Wählen Sie diese Option aus, wenn Sie Umlagerungsaufträge kombinieren möchten.|  
    |**Abbrechen und ersten Fehler anzeigen**|Wählen Sie diese Option aus, wenn die Stapelverarbeitung **Ereignismeld. durchf.-Plan** beendet werden soll, sobald ein Fehler auftritt. Gleichzeitig wird eine Meldung angezeigt, die Informationen zu dem ersten Fehler enthält. Wenn ein Fehler vorliegt, werden nur aus den vor dem Auftreten des Fehlers verarbeiteten Planungszeilen Beschaffungsaufträge erstellt.|  

3.  Auf dem Inforegister **Planungszeile** können Sie Filter festlegen, um die durchzuführenden Ereignismeldungen zu beschränken.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

Die Stapelverarbeitung löscht die Zeilen im Planungsvorschlag, nachdem die Ereignismeldungen durchgeführt wurden. Die anderen Vorschlagszeilen bleiben im Planungsvorschlag, bis sie entweder akzeptiert oder zu einem späteren Zeitpunkt gelöscht werden. Sie können diese Zeilen auch manuell löschen.  

## <a name="action-messages"></a>Ereignismeldungen  
Ereignismeldungen werden vom Bedarfsverursachersystem ausgegeben, wenn im vorhandenen Auftragsnetzwerk kein Ausgleich möglich ist. Sie können als Vorschläge angesehen werden, wie Änderungen verarbeitet werden sollten, damit wieder ein Gleichgewicht zwischen Vorrat und Bedarf hergestellt werden kann.  

Die Generierung von Ereignismeldungen erfolgt jeweils für eine Ebene in Bezug auf die Stücklistenebene jedes Artikels. Dadurch ist sichergestellt, dass alle Artikel berücksichtigt werden, für die es Änderungen beim Vorrat oder Bedarf gegeben hat oder geben wird.  

Um kleine, überflüssige oder unwichtige Ereignismeldungen zu vermeiden, können Sie Toleranzen einrichten, die bewirken, dass die Generierung von Ereignismeldungen auf Änderungen beschränkt wird, durch die die definierte Menge oder Anzahl von Tagen überschritten wird.  

Nachdem Sie sich die Ereignismeldungen angesehen und durch Aktivieren oder Deaktivieren des Feldes **Ereignismeldung akzeptieren** festgelegt haben, welche der vorgeschlagenen Änderungen vorgenommen werden sollen, können Sie dann die Pläne entsprechend aktualisieren.  

> [!NOTE]  
>  Eine Ereignismeldung ist ein Vorschlag, eine neue Bestellung zu erstellen, eine Bestellung zu stornieren oder die Menge oder das Datum einer Bestellung zu ändern. Eine Bestellung ist eine Einkaufsbestellung, ein Umlagerungsauftrag oder ein Fertigungsauftrag.  

Als Reaktion auf gestörte Gleichgewichte von Vorrat und Bedarf werden die folgenden Ereignismeldungen generiert.  

|Ereignismeldung|Beschreibung|  
|--------------------|---------------------------------------|  
|**Neu**|Wenn sich ein Bedarf nicht dadurch erfüllen lässt, dass Ereignismeldungen für **Menge ändern**, **Neu berechnen**, oder **Neu berechnen Menge ändern** vorgeschlagen werden, wird eine Ereignismeldung der Art **Neu** generiert, die eine neue Bestellung vorschlägt. Eine Ereignismeldung der Art **Neu** wird auch ausgegeben, wenn es für den fraglichen Artikel keine Beschaffungsaufträge im Bestellzyklus gibt. Dieser Parameter bestimmt die Anzahl der Perioden vorwärts und rückwärts im Verfügbarkeitsprofil, wenn nach einer Bestellung gesucht wird, die neu geplant werden muss.|  
|**Menge ändern**|Wenn es für einen Bedarf, der mit einem Beschaffungsauftrag verknüpft ist, eine Mengenänderung gibt, wird eine Ereignismeldung der Art **Menge ändern** generiert, die darauf hinweist, dass der zugehörige Vorrat entsprechend der Änderung des Bedarfs angepasst werden sollte. Wenn ein neuer Bedarf vorliegt, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] nach dem nächsten vorhandenen und nicht reservierten Beschaffungsauftrag im Bestellzyklus suchen und für diesen Auftrag eine Ereignismeldung der Art "Vorgang ändern" ausgegeben.|  
|**Neu berechnen**|Wenn es für einen Beschaffungs- oder Bedarfsauftrag eine Datumsänderung gegeben hat, die ein Ungleichgewicht im Auftragsnetzwerk verursacht, wird eine Ereignismeldung der Art **Neu berechnen** ausgegeben. Gibt es eine Eins-zu-Eins-Beziehung zwischen dem Bedarf und dem Vorrat, wird eine Ereignismeldung ausgegeben, in der vorgeschlagen wird, den Beschaffungsauftrag entsprechend zu verschieben. Bezieht sich der Beschaffungsauftrag auf Bedarfe aus mehreren Verkaufsaufträgen, erfolgt die Neuberechnung des Beschaffungsauftrags bezogen auf das Datum des ersten Bedarfs.|  
|**Neu berechnen & Menge ändern**|Wenn sowohl die Datumsangaben als auch die Mengen einer Bestellung geändert wurden, müssen Sie den jeweilige Plan hinsichtlich beider Aspekte ändern. Bei der Generierung der Ereignismeldung werden beide Ereignisse in einer Meldung zusammengefasst **Neu berechnen Menge ändern**, damit sichergestellt ist, dass der Auftragsnetzwerk wieder ins Gleichgewicht gebracht wird.|  
|**Stornieren**|Wenn ein Bedarf, der auf einer Eins-zu-Eins-Basis gedeckt wird, gelöscht wurde, wird eine Ereignismeldung ausgegeben, die den zugehörigen Beschaffungsauftrag storniert. Ist die Beziehung nicht gleich "Eins-zu-Eins", wird eine Ereignismeldung der Art "Auftrag ändern" generiert, um den Vorrat zu verringern. Wenn zu dem Zeitpunkt, zu dem die Ereignismeldungen durch den Benutzer generiert werden, wegen anderer Faktoren kein Beschaffungsauftrag erforderlich ist, schlägt [!INCLUDE[d365fin](includes/d365fin_md.md)] in einer Ereignismeldung **Stornieren** im Arbeitsblatt vor.|  

## <a name="see-also"></a>Siehe auch  
[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

