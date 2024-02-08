---
title: 'Vollständige Planung, Prod.-Programmplanung oder Nettobedarf ausführen'
description: 'Das Planungssystem kann auf Wunsch entweder den Master Production Schedule (MPS) oder die Materialbedarfsplanung (MRP) berechnen, oder beides gleichzeitig.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: andreipa
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="run-full-planning-mps-or-mrp"></a>Vollständige Planung, Prod.-Programmplanung oder Nettobedarf ausführen

Die Begriffe „Planungsvorschlag ausführen“ und „Nettobedarf ausführen“ beziehen sich auf die Berechnung des Produktionsplans und der Materialbedarfe. Die Berechnung basiert auf dem tatsächlichen und prognostizierten Bedarf. Das Planungssystem kann auf Wunsch entweder den Master Production Schedule (MPS) oder die Materialbedarfsplanung (MRP) berechnen, oder beides gleichzeitig.  

- Prod.-Programmplanung ist die Berechnung eines Produktionsplans, der auf dem tatsächlichen Bedarf und der Absatzplanung basiert. Die Berechnung der Produktionsprogrammplanung wird für Endartikel mit einer Planung oder einer Verkaufsauftragszeile durchgeführt. Diese Artikel werden als „Prod.-Programmplanungsartikel“ bezeichnet und werden dynamisch gekennzeichnet, wenn die Berechnung gestartet wird.  
- Nettobedarf ist die Berechnung der Materialbedarfe auf Basis des tatsächlichen Bedarfs für Komponenten sowie der Absatzplanung auf Komponentenebene. Der Nettobedarf wird nur für Artikel berechnet, die keine Prod.-Programmplanungsartikel sind. Der Hauptzweck einer Nettobedarfsplanung besteht darin, terminierte formale Pläne je nach Artikeln aufzustellen, um den richtigen Artikel zur richtigen Zeit, am richtigen Ort und in der richtigen Menge bereitzustellen.  

Für die Prod.-Programmplanung und den Nettobedarf wird derselbe Planungsalgorithmus verwendet. Der Algorithmus betrifft den Bestandsabgleich, die Wiederverwendung vorhandener Beschaffungsaufträge sowie die Ereignismeldungen. Der Planungssystemprozess untersucht, was momentan oder zukünftig benötigt wird (Bedarf) und was verfügbar ist oder erwartet wird (Vorrat). Wenn Sie diese Mengen saldieren, gibt [!INCLUDE[prod_short](includes/prod_short.md)] Ereignismeldungen zurück. Eine Ereignismeldung ist ein Vorschlag, einen neuen Auftrag zu erstellen, einen Auftrag zu ändern (Menge oder Datum) oder einen Auftrag zu stornieren. Der Begriff „Auftrag“ umfasst Fertigungsaufträge, Einkaufsbestellungen, Herstellungsaufträge und Umlagerungsaufträge.

Sie können die Links, die das Planungsmodul zwischen Bedarf und Vorrat auf der Seite **Bedarfsverursacher** erstellt, nachverfolgen. Weitere Informationen finden Sie unter [Titel-Beziehungen zwischen Bedarf und Vorrat nachverfolgen](production-how-track-demand-supply.md).

Korrekte Planungsergebnisse hängen von der Einrichtung ab, die auf Artikelkarten, Montagestücklisten, Fertigungsstücklisten und Arbeitsplänen vorgenommen wurde.  

## <a name="methods-for-generating-a-plan"></a>Methoden zum Generieren eines Plans

- **Neuplanung berechnen:** den Materialplan verarbeiten oder erneut generieren. Dieser Vorgang beginnt damit, dass alle momentan geladenen Beschaffungsaufträge gelöscht werden. Alle Artikel in der Datenbank werden neu geplant.  
- **Änderungsplanung berechnen**: eine Änderungsplanung verarbeiten. Artikel werden in einer Änderungsplanung von zwei Arten von Änderungen aus gesehen:  
   - **Bedarfs-/Vorratsänderungen**: Hierzu gehören Änderungen an Mengen für Verkaufsaufträge, Absatzplanungen, Montageaufträge oder Einkaufsbestellungen. Auch eine ungeplante Lagerbestandsänderung wird als Mengenänderung angesehen.  
   - **Planungsparameteränderungen**: Hierzu gehören Änderungen am Sicherheitsbestand, am Meldebestand, am Arbeitsplan und an der Stückliste sowie Änderungen am Bestellzyklus oder an der Beschaffungszeit.  
- **Aktionsmeldungen abrufen**: Fungiert als kurzfristiges Planungstool, indem sie Ereignismeldungen ausgibt, die den Benutzenden über Änderungen informieren, die seit Ihrer letzten Berechnung der Neuplanung oder der Änderungsplanung vorgenommen wurden.  

Bei jeder Planungsmethode generiert [!INCLUDE[prod_short](includes/prod_short.md)] Arbeitsblattposten, wobei unbegrenzte Kapazität angenommen wird. Die Arbeitsplatz- und Arbeitsplatzgruppenkapazitäten werden nicht berücksichtigt, wenn Sie Pläne entwickeln.  

> [!IMPORTANT]  
> „Neuplanung berechnen“ ist der Prozess, der am häufigsten verwendet wird. Die „Planung berechnen“ und „Ereignismeldungen durchführen“ können dagegen dazu verwendet werden, den Prozess „Änderungsplanung berechnen“ auszuführen.  
>
> Sie können „Aktionsmeldungen abrufen“ zwischen Ausführungen der Neu- und Änderungsplanung ausführen, um einen sofortigen Überblick über die Auswirkungen von Planänderungen zu erhalten. Es ist jedoch nicht dazu gedacht, die vollständigen Neu- oder Änderungsplanungsprozesse zu ersetzen.  

## <a name="to-calculate-the-planning-worksheet"></a>Planungsarbeitsblatt berechnen
  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Planungsarbeitsblätter** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die **Neuplanung berechnen** Aktion aus, um die Seite **Planung berechnen** zu öffnen.  
3. Füllen Sie im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Berechnen Sie eine Produktions-Programmplanung. Artikel, für die es offene Verkaufsaufträge und/oder Absatzplanungen gibt, werden in diesem Lauf berücksichtigt. <br/>Wenn für solche Artikel auch andere Bedarfe bestehen, beispielsweise Sicherheitsbestand, Meldebestand oder offene Fertigungskomponentenzeilen, werden diese Bedarfe in die Berechnung der Produktions-Programmplanung einbezogen, um sicherzustellen, dass das Planungssystem das vollständige Bestandsprofil berücksichtigt.  |  
    |**MRP**|Berechnen Sie eine Materialbedarfsplanung. Artikel mit abhängigem Bedarf werden in diesem Lauf berücksichtigt. Normalerweise werden die Prod.-Programmplanung und der Nettobedarf gleichzeitig ausgeführt. Damit Prod.-Programmplanung und Materialbedarfsplanung gleichzeitig ausgeführt werden können, muss das Kontrollkästchen **Prod.-Prog.Pl./Nettobedarf komb.** im Inforegister **Planung** auf der Seite **Produktion Einrichtung** aktiviert sein.|  
    |**Startdatum**|Bewerten Sie die Lagerverfügbarkeit. Wenn die für einen Artikel verfügbare Menge unter dem Minimalbestand liegt (am Auftragsdatum), wird ab diesem Datum ein Beschaffungsauftrag vorausgeplant. Ist die Menge eines Artikels kleiner als dessen Sicherheitsbestand (am Auftragsdatum), wird ein Beschaffungsauftrag rückgesetzt, der am Auftragsstartdatum fällig ist.|  
    |**Enddatum**|Das Enddatum des Planungszeitraums. Nach diesem Datum wird weder Bedarf noch Vorrat berücksichtigt. Erstreckt sich der Bestellzyklus eines Artikels über das Enddatum hinaus, ist sich der effektive Planungszeitraum für diesen Artikel gleich Auftragsdatum plus Bestellzyklus.<br/><br/> Der Planungszeitraum (-horizont) ist die Zeitspanne, über die sich der Plan erstreckt. Ist dieser Zeitraum zu kurz, werden Artikel mit längerer Beschaffungszeit nicht rechtzeitig bestellt. Ist dieser Zeitraum zu lang, wird zu viel Zeit mit dem Auswerten und Verarbeiten von Informationen verbracht, die sich wahrscheinlich geändert haben, bevor sie benötigt werden. Sie können einen Planungszeitraum für die Fertigung und einen längeren Planungszeitraum für Einkäufe festlegen, dies ist aber nicht erforderlich. Ein Planungszeitraum für Einkäufe und Fertigung sollte so festgelegt sein, dass er die gesamte Beschaffungszeit für Komponenten abdeckt.|  
    |**Abbrechen und ersten Fehler anzeigen**|Wählen Sie diese Option aus, wenn die Planung beendet werden soll, sobald ein Fehler auftritt. Es wird eine Meldung angezeigt, die Informationen zu dem Fehler enthält. Gibt es einen Fehler, werden im Planungsarbeitsblatt nur die Planungszeilen angezeigt, die vor dem Fehler erfolgreich erstellt wurden. Wenn Sie das Feld nicht auswählen, wird die Batchauftrag **Planung berechnen** weiterhin bis zum Abschluss durchgeführt. Fehler unterbrechen die Stapelverarbeitung nicht. Wenn Fehler vorliegen, wird nach dem Abschluss eine Meldung angezeigt und angegeben, wie viele Artikel betroffen sind. Danach wird die Seite **Planungsfehlerprotokoll** angezeigt, in dem weitere Informationen zu den Fehlern sowie den Verknüpfungen für die betroffenen Artikelkarten bereitgestellt werden.|  
    |**Planung verwenden**|Wählen Sie eine Planung aus, die einbezogen werden soll, wenn Sie den Planungsbatchauftrag ausführen. Die Standardplanung wird auf der Seite **Produktion Einrichtung** auf dem Inforegister **Planung** eingerichtet.|  
    |**Planung vorher ausschließen**|Definieren Sie, wie viel der gewählten Planung in den Planungslauf einbezogen werden soll, indem Sie ein Datum eingeben, vor dem kein Planungsbedarf einbezogen wird.|  
    |**Planungsparameter für Ausnahmewarnungen berücksichtigen**|Dieses Feld ist standardmäßig ausgewählt.<br/><br/> Der Vorrat in Planungszeilen mit Warnungen wird normalerweise nicht gemäß den Planungsparametern geändert. Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken. Sie können jedoch bestimmte Planungsparameters festlegen, sodass Planungszeilen mit bestimmten Warnungen berücksichtigt werden können.<br/><br/>|  

4. Im Inforegister **Artikel** können Sie die Planungsroutinen auf Basis von Artikel, Artikelbeschreibung oder Lagerort filtern und ausführen.  
5. Wählen Sie die Schaltfläche **OK**. Der Batchauftrag wird ausgeführt und Planungszeilen werden in das Planungsarbeitsblatt hinzugefügt.  

## <a name="to-perform-action-messages"></a>Ereignismeldungen ausführen
  
1. Auf der Seite **Planungsarbeitsblatt** wählen Sie **Aktionsnachricht ausführen**.  
2. Geben Sie im Inforegister **Optionen** an, wie die Lieferungen erstellt werden sollen. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Fertigungsauftrag**|Geben Sie an, wie die Fertigungsaufträge erstellt werden sollen. Sie können dies direkt von den Planungszeilenvorschlägen aus durchführen. Sie können entweder geplante oder fest geplante Fertigungsaufträge erstellen.|  
    |**Montageauftrag**|Geben Sie an, wie Montageaufträge erstellt werden sollen. Sie können dies direkt von den Planungszeilenvorschlägen aus tun.|  
    |**Bestellung**|Geben Sie an, wie Einkaufsbestellungen erstellt werden sollen. Sie können dies direkt von den Planungszeilenvorschlägen aus tun.<br/><br/> Wenn Sie die Planungszeilen Bestellarbeitsblätter in das Anforderungsarbeitsblatt kopieren wollen, dann wählen Sie die Vorlagen und den Arbeitsblattnamen aus.|  
    |**Umlagerungsauftrag**|Geben Sie an, wie Umlagerungsaufträge erstellt werden sollen. Sie können dies direkt von den Planungszeilenvorschlägen aus tun.<br/><br/> Wenn Sie die Planungszeilen Umlagerungsvorschläge in das Anforderungsarbeitsblatt kopieren wollen, dann wählen Sie die Vorlagen und den Arbeitsblattnamen aus.|  
    |**Umlagerungsaufträge kombinieren**|Wählen Sie aus, ob Umlagerungsaufträge kombiniert werden sollen.|  
    |**Abbrechen und ersten Fehler anzeigen**|Wählen Sie diese Option aus, wenn der Batchauftrag **Ereignismeld. durchf.-Plan** beendet werden soll, sobald er einen Fehler findet. Eine Meldung mit Informationen zu dem Fehler wird angezeigt. Wenn ein Fehler vorliegt, werden nur aus den vor dem Auffinden des Fehlers verarbeiteten Planungszeilen Beschaffungsaufträge erstellt.|  

3. Auf dem Inforegister **Planungszeile** können Sie Filter festlegen, um die durchzuführenden Ereignismeldungen zu beschränken.  
4. Wählen Sie die Schaltfläche **OK** aus.  

Die Stapelverarbeitung löscht die Zeilen im Planungsarbeitsblatt, nachdem die Ereignismeldungen durchgeführt wurden. Die anderen Vorschlagszeilen bleiben im Planungsvorschlag, bis sie entweder akzeptiert oder zu einem späteren Zeitpunkt gelöscht werden. Sie können diese Zeilen auch manuell löschen.  

## <a name="action-messages"></a>Ereignismeldungen
  
Ereignismeldungen werden vom Bedarfsverursachersystem ausgegeben, wenn im vorhandenen Auftragsnetzwerk kein Ausgleich möglich ist. Diese Meldungen können als Vorschläge angesehen werden, wie Änderungen verarbeitet werden sollten, damit wieder ein Gleichgewicht zwischen Vorrat und Bedarf hergestellt werden kann.  

Die Generierung von Ereignismeldungen erfolgt jeweils für eine Ebene in Bezug auf die Stücklistenebene jedes Artikels. Dadurch ist sichergestellt, dass alle Artikel berücksichtigt werden, für die es Änderungen beim Vorrat oder Bedarf gegeben hat oder geben wird.  

Um kleine, nicht benötigte oder unwichtige Ereignismeldungen zu vermeiden, können Sie Toleranzen festlegen, die bewirken, dass die Generierung von Ereignismeldungen auf Änderungen beschränkt wird, durch welche die festgelegte Menge oder der Anzahl von Tagen überschritten wird.  

Nachdem Sie die Ereignismeldungen durchgesehen und bestimmt haben, ob Sie einige oder alle der vorgeschlagenen Änderungen akzeptiert haben, wählen Sie das Feld **Ereignismeldung akzeptieren** aus. Aktualisieren Sie als Nächstes die Zeitpläne entsprechend.  

> [!NOTE]  
> Eine Ereignismeldung ist ein Vorschlag, eine neue Bestellung zu erstellen, eine Bestellung zu stornieren oder die Menge oder das Datum einer Bestellung zu ändern. Eine Bestellung ist eine Einkaufsbestellung, ein Umlagerungsauftrag oder ein Fertigungsauftrag.  

Als Reaktion auf gestörte Gleichgewichte von Vorrat und Bedarf werden die folgenden Ereignismeldungen generiert.  

|Ereignismeldung|Beschreibung|  
|--------------------|---------------------------------------|  
|**Neu**|Wenn sich ein Bedarf nicht dadurch erfüllen lässt, dass Ereignismeldungen für **Menge ändern**, **Neu planen** oder **Neu planen und Menge ändern** vorgeschlagen werden, wird eine Ereignismeldung der Art **Neu** generiert, um eine neue Bestellung zu generieren. Die Meldung der Art **Neu** wird auch ausgegeben, wenn es für den Artikel keine Beschaffungsaufträge im Bestellzyklus gibt. Diese Option bestimmt die Anzahl der Perioden vorwärts und rückwärts im Verfügbarkeitsprofil, wenn nach einer Bestellung gesucht wird, die neu geplant werden muss.|  
|**Menge ändern**|Wenn sich die Menge für einen Bedarf ändert, der mit einem Beschaffungsauftrag verknüpft ist, wird die Ereignismeldung **Menge ändern** generiert. Die Meldung gibt an, dass der zugehörige Vorrat entsprechend der Änderung im Bedarf geändert werden soll. Wenn ein neuer Bedarf vorliegt, wird [!INCLUDE[prod_short](includes/prod_short.md)] nach dem nächsten vorhandenen und nicht reservierten Beschaffungsauftrag im Bestellzyklus suchen und für diesen Auftrag eine Ereignismeldung der Art „Vorgang ändern“ ausgegeben.|  
|**Neu planen**|Wenn eine Datumsänderung für einen Beschaffungs- oder Bedarfsauftrag zu einem Ungleichgewicht im Auftragsnetzwerk führt, wird eine Ereignismeldung der Art **Neu planen** ausgegeben. Gibt es eine 1:1-Beziehung zwischen dem Bedarf und dem Vorrat, wird eine Ereignismeldung ausgegeben, die vorschlägt, dass Sie den Beschaffungsauftrag verschieben. Bezieht sich der Beschaffungsauftrag auf Bedarfe aus mehreren Verkaufsaufträgen, erfolgt die Neuberechnung des Beschaffungsauftrags bezogen auf das Datum des ersten Bedarfs.|  
|**Neu planen & Menge ändern**|Wenn sich sowohl die Datumsangaben als auch die Mengen einer Bestellung ändern, müssen Sie die Pläne im Hinblick auf beides ändern. Bei der Generierung der Ereignismeldung werden beide Ereignisse in einer Meldung zusammengefasst **Neu berechnen Menge ändern**, damit sichergestellt ist, dass der Auftragsnetzwerk wieder ins Gleichgewicht gebracht wird.|  
|**Stornieren**|Wenn ein Bedarf, der auf einer Eins-zu-eins-Basis gedeckt wird, gelöscht wurde, wird eine Ereignismeldung ausgegeben, die den zugehörigen Beschaffungsauftrag storniert. Handelt es sich nicht um eine Beziehung auf Eins-zu-eins-Basis, wird eine Ereignismeldung generiert, um die Auftrag zu ändern und so den Vorrat zu verringern. Wenn zu dem Zeitpunkt, wenn Sie die Ereignismeldungen generieren, wegen anderer Faktoren kein Beschaffungsauftrag erforderlich ist, schlägt [!INCLUDE[prod_short](includes/prod_short.md)] eine **Stornieren**-Ereignismeldung im Arbeitsblatt vor.|  

## <a name="see-also"></a>Siehe auch

[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Fertigung](production-manage-manufacturing.md)    
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
