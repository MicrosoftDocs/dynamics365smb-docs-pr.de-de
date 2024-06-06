---
title: Arbeitsplätze und Arbeitsplatzgruppen einrichten
description: 'Auf einer Arbeitsplatzgruppenkarte sind die konstanten Werte und Anforderungen der jeweiligen Fertigungsressource organisiert, und dadurch werden die Istmengen der Fertigung in dieser Arbeitsplatzgruppe gesteuert.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-work-centers-and-machine-centers"></a>Arbeitsplätze und Arbeitsplatzgruppen einrichten

Die Anwendung unterscheidet zwischen drei verschiedenen Arten von Kapazitätseinheiten. Diese sind hierarchisch angeordnet. Jede Ebene enthält die untergeordneten Ebenen.  

Die oberste Ebene ist die Abteilung. Arbeitsplatzgruppen werden den Abteilungen zugeordnet. Jede Arbeitsplatzgruppe gehört zu einer Abteilung.

Sie können unterschiedliche Arbeitsplätze zu einer Arbeitsplatzgruppe zusammenfassen. Ein Arbeitsplatz kann nur zu einer Arbeitsplatzgruppe gehören.  

Die geplante Kapazität einer Arbeitsplatzgruppe besteht aus der Verfügbarkeit der entsprechenden Arbeitsplätze und der zusätzlichen geplanten Verfügbarkeit der Arbeitsplatzgruppe. Die geplante Verfügbarkeit der Abteilung ist die Summe aller Verfügbarkeiten der entsprechenden Arbeitsplätze und Arbeitsplatzgruppen.  

Die Verfügbarkeit wird in Kalenderposten gespeichert.  

> [!IMPORTANT]
> Bevor Sie anfangen oder Arbeitsplätze einrichten, müssen Sie Betriebskalender einrichten. Weitere Informationen finden Sie unter [Erstellen von Betriebskalendern](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Um Arbeitsplatzgruppen einzurichten:

Nachfolgend ist beschrieben, wie ein alternativer Arbeitsplatzkalender eingerichtet wird. Die Schritte, um ein Arbeitsplatzkalenders einzurichten außer für das **Arbeitsplatz-Einrichtung** Inforegister.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsplatzgruppen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie im Feld **Abteilung** die übergeordnete Ebene, unter der sich die Arbeitsplatzgruppe befindet, sofern relevant. Wählen Sie aus der Dropdown-Liste die Aktion **Neu** aus.  
5. Wählen Sie im Feld **Alternativer Arbeitsplatz** den Arbeitsplatz aus, der verwendet werden soll, wenn dieser Arbeitsplatz nicht verfügbar ist oder wenn der Bedarf seine Kapazität übersteigt. Der alternative Arbeitsplatz dient nur zur Information und wird nicht automatisch in die Planungsprozesse einbezogen.
6. Wählen Sie das Feld **Gesperrt** aus, wenn Sie verhindern möchten, dass die Arbeitsplatzgruppe bei einer Verarbeitung verwendet wird. Das bedeutet, dass die Ausgabe für einen Artikel nicht gebucht werden kann, der für die Arbeitsplatzgruppe gefertigt wird. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-post-output-quantity.md).
7. Geben Sie im Feld **EK-Preis** die Kosten der Fertigung einer Einheit in dieser Arbeitsplatzgruppe ein, ausschließlich aller anderen Kostenelemente. Diese Kosten werden häufig als *direkte Arbeitskosten* bezeichnet.  
8. Geben Sie im Feld **Kosten %** die Gesamtkosten des Einsatzes der Arbeitsplatzgruppe als Prozentsatz des EK-Preises ein. Dieser prozentuale Betrag wird in der Berechnung des Einstandspreises zum EK-Preis addiert.  
9. Geben Sie im Feld **Gemeinkostensatz** die nicht mit dem eigentlichen Betrieb verbundenen Kosten für die Arbeitsplatzgruppe (z. B. Wartungsausgaben) als absoluten Betrag ein.  

    Das Feld **Einstandspreis** enthält den berechneten Einstandspreis für die Fertigung einer Einheit in der Arbeitsplatzgruppe, wobei alle Kostenelemente berücksichtigt sind.  

    Einstandspreis = EK-Preis + (EK-Preis x Kosten %) + Gemeinkostensatz.  

10. Legen Sie im Feld **Einstandspreisberechnung** fest, ob der obigen Berechnung die benötigte Zeitspanne (**Zeit**) oder die Anzahl der gefertigten Einheiten (**Einheiten**) zugrunde gelegt werden soll.  
11. Markieren Sie das Feld **Spezifische Stückkosten**, wenn Sie die Stückkosten des Arbeitsplatzes in der Arbeitsplanzeile, in der er verwendet wird, definieren wollen. Dies kann sich als unerlässlich bei Arbeitsgängen mit wesentlich abweichenden Kapazitätskosten erweisen, die normalerweise in dieser Arbeitsplatzgruppe verarbeitet werden.  
12. Wählen Sie im Feld **Buchungsmethode** aus, ob der Ausgabebuchung in dieser Arbeitsplatzgruppe manuell oder automatisch mit einer der folgenden Methoden berechnet und gebucht werden soll, indem eine der folgenden Methoden verwendet wird.

    |Option|Beschreibung|
    |------|-----------|
    |**Manuell**| Verwendete Zeit, Ausgabe und Ausschuss werden manuell im Ausgabe- oder Produktionsjournal gebucht.|
    |**"Vorwärts"**|Istmeldung wird automatisch berechnet und gebucht, wenn der Fertigungsauftrag freigegeben ist.|
    |**Rückwärts**|Istmeldung wird automatisch berechnet und gebucht, wenn der Fertigungsauftrag abgeschlossen ist.|

    > [!NOTE]
    > Gegebenenfalls kann die hier ausgewählte Buchungsmethode für einzelne Arbeitsgänge überschrieben werden, indem die Einstellungen für Arbeitsgänge geändert wird.

13. Geben Sie im Feld **Einheitencode** die Zeiteinheit ein, die bei der Kostenberechnung und der Kapazitätsplanung der Arbeitsplatzgruppe zugrunde gelegt werden soll.
    Um regelmäßig den Verbrauch erfassen zu können, müssen Sie zunächst die Buchungsmethode einrichten. Die Einheiten, die Sie eingeben, sind Basiseinheiten. Die Bearbeitungszeit wird z. B. in Stunden und Minuten gemessen.

    > [!NOTE]  
    > Beachten Sie bei der Verwendung von Tagen, dass 1 Tag 24 Stunden und nicht 8 (Arbeitsstunden) hat.

14. Geben Sie im Feld **Kapazität** an, ob in der Arbeitsplatzgruppe mehrere Personen bzw. Maschinen gleichzeitig eingesetzt werden. Wenn in der [!INCLUDE[prod_short](includes/prod_short.md)]-Installation das Element "Arbeitsplatz" nicht enthalten ist, muss in diesem Feld der Wert **1** festgelegt sein.  
15. Geben Sie im Feld **Effektivität** an, wie hoch die tatsächliche Effektivität der Arbeitsplatzgruppe prozentual hinsichtlich der erwarteten Standardeffektivität ist. Wenn Sie **100** eingeben, bedeutet dies, dass die Isteffektivität der Arbeitsplatzgruppe mit der Standardeffektivität übereinstimmt.  
16. Wählen Sie das Kontrollkästchen **Konsolidierter Kalender**, wenn Sie auch Arbeitsplätze verwenden. Dadurch ist sichergestellt, dass Kalenderposten oben aus den Arbeitsplatzkalendern ermittelt werden.  
17. Wählen Sie im Feld **Betriebskalender** einen Einkaufskalender. Weitere Informationen finden Sie unter [Erstellen von Betriebskalendern](production-how-to-create-work-center-calendars.md).  
18. Geben Sie im Feld **Warteschlangenzeit** eine feste Zeitspanne an, die ablaufen muss, bevor die zugewiesenen Arbeiten in dieser Arbeitsplatzgruppe begonnen werden können. 

> [!NOTE]
> Verwenden Sie Warteschlangenzeiten, um einen Puffer zwischen dem Eintreffen einer Komponente auf einer Maschine oder einem Arbeitsplatz und dem tatsächlichen Start des Vorgangs bereitzustellen. Beispielsweise wird ein Teil um 10:00 Uhr an ein Maschinenzentrum geliefert, die Montage an der Maschine dauert jedoch eine Stunde, sodass der Vorgang erst um 11.00 Uhr beginnt. Um diese Stunde zu berücksichtigen, würde die Wartezeit eine Stunde betragen. Der Wert des Feldes **Warteschlangenzeit** der speziellen Arbeitsplatzkarte oder Arbeitsplatzgruppenkarte plus die Summe der Werte in den Feldern **Einrichtungszeit**, **Ausführungszeit**, **Wartezeit** und **Transportzeit** der Arbeitsgänge des Artikels ergeben zusammen die Produktionsdurchlaufzeit des Artikels. Dies trägt zu genauen Gesamtproduktionszeiten bei.  

## <a name="considerations-about-capacity"></a>Überlegungen zur Kapazität

Die für ein Arbeits- und Maschinenzentrum vorgegebene Kapazität und Effizienz wirken sich nicht nur auf die verfügbare Kapazität aus. Sie wirken sich auch auf die Gesamtproduktionszeit aus, die sich aus der Rüstzeit und der Laufzeit zusammensetzt, die beide auf der Routinglinie definiert werden.  

Wenn eine bestimmte Arbeitsplanlinie einem Arbeitsplatz oder einem Maschinenzentrum zugewiesen wird, berechnet das System, wie viel Kapazität benötigt wird und wie lange es dauert, bis der Vorgang abgeschlossen ist.  

### <a name="run-time"></a>Bearbeitungszeit

Zur Berechnung der Laufzeit vergibt das System genau die Zeit, die im Feld **Laufzeit** der Routinglinie angegeben ist. Weder Effizienz noch Kapazität wirken sich auf die zugewiesene Zeit aus. Wenn die Laufzeit beispielsweise auf 2 Stunden festgelegt ist, beträgt die zugewiesene Zeit 2 Stunden, unabhängig von den Werten in den Feldern Effizienz und Kapazität im Arbeitsplatz.  

> [!NOTE]
> Die in den Berechnungen verwendete Kapazität ist der minimale Wert zwischen der Kapazität, die im Arbeitsplatz oder Maschinenzentrum definiert ist, und der gleichzeitigen Kapazität, die für die Arbeitsplanlinie definiert ist. Wenn ein Arbeitsplatz eine Kapazität von 100 hat, die gleichzeitige Kapazität für die Arbeitsplanzeile jedoch 2 beträgt, dann wird *2* in den Berechnungen verwendet.

Die *Dauer* einer Operation hingegen berücksichtigt sowohl die Effizienz als auch die Kapazität. Dauer wird berechnet als *Laufzeit / Effizienz / Kapazität*. Die folgende Liste zeigt einige Beispiele für die Berechnung der Dauer für die gleiche Laufzeit, die für die Routinglinie mit 2 Stunden definiert ist:

- Effizienz 80 % bedeutet, dass Sie 2,5 Stunden statt zwei Stunden benötigen  
- Effizienz 200 % bedeutet, dass Sie die Arbeit in einer Stunde erledigen können – Sie können das Loch zweimal schneller graben, wenn Sie einen Bagger haben, der doppelt so groß ist wie der kleinere.  

    Das gleiche Ergebnis erzielen Sie, wenn Sie statt eines großen zwei kleinere Bagger verwenden – verwenden Sie *2* als die Kapazität und *100 %* als die Effizienz  

Die fraktionale Kapazität ist knifflig, und wir werden sie später besprechen. 

### <a name="setup-time"></a>Rüstzeit

Die Zeitzuteilung für die Rüstzeit ist abhängig von der Kapazität und wird berechnet als *Einrichtungszeit * Kapazität*. Wenn die Kapazität beispielsweise auf *2* eingestellt ist, verdoppelt sich Ihre zugewiesene Rüstzeit, da Sie für den Betrieb zwei Maschinen einrichten müssen.  

*Dauer* der Rüstzeit ist effizienzabhängig und berechnet sich als *Einrichtungszeit / Effizienz*. 

- Effizienz 80 % bedeutet, dass Sie 2,5 Stunden statt zwei Stunden für die Einrichtung benötigen  
- Effizienz 200 % bedeutet, dass Sie die Einrichtung in 1 Stunde abschließen können statt in 2 Stunden, die in der Routinglinie definiert sind  

Die fraktale Kapazität ist nicht leicht zu erfassen und wird in sehr speziellen Fällen verwendet.

### <a name="work-center-processing-multiple-orders-simultaneously"></a>Arbeitsplatz, der mehrere Aufträge gleichzeitig bearbeitet

Nehmen wir als Beispiel eine Lackierkabine. Sie hat die gleiche Einrichtung und Laufzeit für jedes verarbeitete Los. Jedes Los kann jedoch mehrere Einzelaufträge enthalten, die gleichzeitig bemalt werden.  

In diesem Fall werden die Zeit und die Kosten, die den Aufträgen zugeordnet werden, durch die Rüstzeit und die gleichzeitige Kapazität verwaltet. Wir empfehlen, in den Routinglinien keine Laufzeit zu verwenden.  

Die zugewiesene Rüstzeit für jeden einzelnen Auftrag erfolgt in umgekehrter Reihenfolge der Anzahl gleichzeitig ausgeführter Aufträge (Mengen). Hier sind einige weitere Beispiele für die Berechnung der Rüstzeit, wenn diese als zwei Stunden für die Routinglinie definiert ist:

- Bei zwei Aufträgen sollte die gleichzeitige Kapazität in der Routinglinie auf 0,5 gesetzt werden.

    Daher beträgt die zugewiesene Kapazität jeweils eine Stunde, die Dauer für jeden Auftrag jedoch zwei Stunden.
- Bei zwei Aufträgen mit einer Menge von eins bzw. vier beträgt die gleichzeitige Kapazität für die Leitlinie des ersten Auftrags 0,2 und 0,8 für den zweiten.  

    Dadurch beträgt die zugeteilte Kapazität für den ersten Auftrag 24 min und für den zweiten 96 min. Die Dauer für beide Bestellungen bleibt zwei Stunden.  

In beiden Fällen beträgt die zugewiesene Gesamtzeit für alle Bestellungen zwei Stunden.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Effiziente Ressourcen können nur einen Teil ihrer Arbeitszeit der produktiven Arbeit widmen

> [!NOTE]
> Dies ist kein empfohlenes Szenario. Wir empfehlen, stattdessen Effizienz zu verwenden. 

Einer Ihrer Arbeitsplätze repräsentiert einen erfahrenen Arbeiter, der mit 100 % Effizienz an Aufgaben arbeitet. Aber sie können nur 50 % ihrer Arbeitszeit mit Aufgaben verbringen, weil sie die restliche Zeit administrative Aufgaben lösen. Während dieser Arbeiter in der Lage ist, eine zweistündige Aufgabe in genau zwei Stunden zu erledigen, müssen Sie im Durchschnitt weitere zwei Stunden warten, während die Person andere Aufgaben erledigt.  

Die zugewiesene Laufzeit beträgt zwei Stunden und die Dauer beträgt vier Stunden.  

Verwenden Sie für solche Szenarien keine Rüstzeit, da das System nur 50 % der Zeit zuweist. Wenn die Einrichtungszeit auf *2* eingestellt ist, dann beträgt die zugewiesene Einrichtungszeit eine Stunde und die Dauer beträgt zwei Stunden.

### <a name="consolidated-calendar"></a>Konsolidierter Kalender

Wenn das Feld **Konsolidierter Kalender** ausgewählt ist, hat der Arbeitsplatz keine eigene Kapazität. Stattdessen entspricht seine Kapazität der Summe der Kapazitäten aller Bearbeitungszentren, die dem Arbeitsplatz zugeordnet sind.  

> [!NOTE]
>  Die Effizienz des Bearbeitungszentrums wird auf die Kapazität des Arbeitsplatzes umgerechnet.

Wenn Sie beispielsweise zwei Bearbeitungszentren mit einer Effizienz von 80 bzw. 70 haben, hat der konsolidierte Kalendereintrag eine Effizienz von 100, eine Kapazität von 1,5 und eine Gesamtkapazität von 12 Stunden (eoithgt Stundenschicht * 1,5 Kapazität). 

> [!NOTE]
>  Verwenden Sie das Feld **Konsolidierter Kalender**, wenn Sie Ihre Arbeitspläne so strukturieren, dass Produktionsvorgänge auf Maschinenzentrumsebene und nicht auf Arbeitsplatzebene geplant werden. Wenn Sie den Kalender konsolidieren, werden die Seite **Arbeitsplatzbelastung** und Berichte zu einer Übersicht über die Gesamtbelastung in allen Bearbeitungszentren, die dem Arbeitsplatz zugeordnet sind.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Beispiel - unterschiedliche Arbeitsplätze, die einer Arbeitsplatzgruppe zugewiesen sind

Es ist wichtig zu planen, welche Kapazitätsarten die Gesamtkapazität ergeben, wenn Sie Arbeitsplatzgruppen und Arbeitsplätze einrichten.

Wenn unterschiedliche Arbeitsplätze (zum Beispiel 210 Packtisch 1, 310 Lackierkabine) einer Arbeitsplatzgruppe zugeordnet sind, ist die Betrachtung der einzelnen Kapazitäten entscheidend, da der Ausfall eines einzelnen Arbeitsplatzes den gesamten Fertigungsprozess unterbrechen kann. Die Arbeitsplatzgruppen können entsprechend ihrer Kapazität eingegeben werden, sie werden jedoch nicht in die Planung mit aufgenommen. Durch Deaktivieren des Feldes **Konsolidierter Kalender** wird nur die Kapazität der Arbeitsplatzgruppe, jedoch nicht die Kapazität der Arbeitsplätze, bei der Planung zugewiesen.

Wenn jedoch identische Arbeitsplätze (wie zum Beispiel 210 Packtisch 1 und 220 Packtisch 2) in einer Arbeitsplatzgruppe zusammengefasst werden, ist die Betrachtung der Arbeitsplatzgruppe als Summe der ihr zugeordneten Arbeitsplätze von Interesse. Daher wird die Arbeitsplatzgruppe selbst mit der Kapazität Null geführt. Durch Aktivierung des Feldes **Konsolidierter Kalender** wird die gemeinsame Kapazität der Arbeitsplatzgruppe zugewiesen.

Wenn die Kapazität von Arbeitsplätzen keinen Beitrag zur Gesamtkapazität leisten soll, können Sie dies mit der Effektivität = 0 erreichen.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>So wird ein in der Kapazität eingeschränkter Arbeitsplatz oder Arbeitsplatzgruppe eingerichtet

Sie müssen die Produktionsressourcen einrichten, die Sie als kritisch betrachten, damit diese nur eine Auslastung bis zu einer Kapazitätsgrenze annimmt, anstelle der Standardeinstellung ohne Kapazitätsgrenze, die andere Produktionsressourcen annehmen. Eine Ressource mit eingeschränkter Kapazität kann eine Arbeitsplatzgruppe oder ein Arbeitsplatz sein, den Sie als Flaschenhals erkannt haben und dessen Auslastung Sie deshalb begrenzen möchten.

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt keine ausführliche Fertigungsbereichssteuerung. Planung einer durchführbaren Nutzung von Ressourcen durch Bereitstellung eines Rohschnittzeitplans, jedoch keine automatische Erstellung und Verwaltung von detaillierten Plänen, die auf Prioritäten oder Optimierungsregeln basieren.

Auf der Seite **Ressourcen mit eingeschränkter Kapazität** können Sie ein Setup vornehmen, das eine Überladung bestimmter Ressourcen verhindert und sicherstellt, dass keine Kapazität unzugewiesen bleibt, wenn dies die Durchlaufzeit eines Fertigungsauftrags erhöhen könnte. Im Feld **Toleranz (% der gesamten Kapazität)** können Sie eine Toleranzperiode zu Ressourcen hinzufügen, um die Aufspaltung von Arbeitsgängen zu minimieren. Dies ermöglicht dem System, Auslastung am letzten möglichen Tag zu planen, indem es den kritischen Auslastungsprozentsatz etwas überschreitet, wenn dies die Anzahl der Arbeitsgänge verringern kann, die aufgeteilt werden.

Beim Planen mit eingeschränkter Kapazität stellt sicher das System sicher, dass keine Ressourcen oberhalb der definierten Kapazität (Grenzbelastung) geladen werden. Dies geschieht, indem jeder Arbeitsgang dem nächsten verfügbaren Zeitfenster zugewiesen wird. Wenn das Zeitfenster nicht ausreicht, um den gesamten Arbeitsgang abzuschließen, wird der Arbeitsgang in zwei Teile aufgeteilt, die in die nächsten verfügbaren Zeitfenster gesetzt werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Begrenzte Kapazitäten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die Felder je nach Bedarf aus.

> [!NOTE]
> Vorgänge auf Arbeitsplätzen oder Arbeitsplätzen, die als eingeschränkte Ressourcen eingerichtet wurden, werden immer seriell geplant. Das bedeutet, dass immer wenn eine eingeschränkte Ressource mehrere Kapazitäten hat, dann können diese Kapazitäten nur nacheinander und nicht nebeneinander geplant werden, wie es der Fall wäre, wenn der Maschinen- oder der Arbeitsplatz nicht als eingeschränkte Ressource eingerichtet wurde. In einer eingeschränkten Ressource ist das Feld Kapazität der Arbeitsplatzgruppe oder der Arbeitsplatz größer als 1.

> Im Falle der Teilung des Arbeitsgangs wird die Rüstzeit nur einmal zugeordnet, da davon ausgegangen wird, dass einige manuelle Ausgleiche vorgenommen werden, um den Plan zu optimieren.

## <a name="see-also"></a>Siehe auch

[Einkaufskalender einrichten](production-how-to-create-work-center-calendars.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
