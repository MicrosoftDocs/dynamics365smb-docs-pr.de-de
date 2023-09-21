---
title: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren
description: 'In diesem Thema wird beschrieben, wie Sie Komponenten nach dem Ausgang des Vorgangs bündeln und welche anderen Bündelungsmethoden es gibt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# Komponenten nach Vorgangsausgabe bündeln
Sie können verschiedene Buchungsmethoden definieren, um die Registrierung des Verbrauchs von Komponenten zu automatisieren. 

Diese Funktionalität ist aus folgenden Ursachen nützlich:  

- **Lagerwert ermitteln**

    Wertposten für Istmeldungen und Verbräuche werden beim Fortschritt des Fertigungsauftrags erstellt. Ohne Verbindungscodes erhöht sich der Lagerwert, wenn Ausstoß registriert wird, und vermindert sich später, wenn der Wert des Komponentenverbrauchs zusammen mit dem beendeten FA gebucht wird.  
- **Lager - Verfügbarkeit**

    Mit allmählicher Verbrauchsbuchung wird die Verfügbarkeit von Komponenten aktueller, was wichtig ist, um die interne Balance zwischen Bedarf und Vorrat aufrechtzuerhalten. Ohne Verbindungscodenummern glauben möglicherweise andere, die Bedarf für die Komponente haben, dass sie verfügbar ist, solange eine verzögerte Verbrauchsbuchung dafür aussteht.  
- **Just-in-Time**

    Mit der Möglichkeit, Produkte an Debitorenanfragen anzupassen, können Sie Abfall minimieren, indem Sie sicherstellen, dass Arbeits- und Systemänderungen nur eintreten, wenn es erforderlich ist.  

- **Dateneingabe reduzieren**

    Durch die Möglichkeit, einen Arbeitsgang automatisch zu buchen, kann der gesamte Erfassungsprozess für Verbrauch und fertige Artikel automatisiert werden. Der Nachteil des automatischen Buchens besteht darin, dass Ausschuss möglicherweise nicht richtig oder sogar gar nicht erfasst wird.

## Methoden für das automatische Buchen des Verbrauchs  

- "Vorwärts"-Buchen des gesamten Auftrags  
- "Vorwärts"-Buchen pro Arbeitsgang  
- "Rückwärts"-Buchen pro Arbeitsgang  
- "Rückwärts"-Buchen des gesamten Auftrags  

### Automatisches Berichtswesen - "Vorwärts"-Buchen des gesamten Auftrags  
Wenn Sie den Fertigungsauftrag zu Beginn des Projekts mit der Methode "Vorwärts" buchen, verhält sich die Anwendung ähnlich wie bei einem manuellen Verbrauch. Der Hauptunterschied besteht darin, dass der Verbrauch automatisch auftritt.  

- Der gesamte Inhalt der Fertigungsstückliste wird zu dem Zeitpunkt verbraucht und dem Lagerbestand entnommen, zu dem der freigegebene Fertigungsauftrag aktualisiert wird.  
- Die Verbrauchsmenge entspricht der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Anzahl der übergeordneten Artikel, die gefertigt werden.  
- Es ist nicht erforderlich, irgendwelche Informationen im FA-Verbrauchs Buch.-Blatt zu erfassen, wenn für alle Artikel festgelegt ist, dass sie gebucht werden müssen.  
- Wenn Artikel aus dem Lagerbestand verbraucht werden, spielt es keine Rolle, wann die Einträge in das FA-Istmeldungs Buch.-Blatt vorgenommen werden, weil sich das FA-Istmeldungs Buch.-Blatt nicht auf diesen Modus des Buchens des Verbrauchs auswirkt.  
- Es können keine Verbindungscodes festgelegt werden.  

Das "Vorwärts"-Buchen eines gesamten Auftrags ist für Fertigungsumgebungen mit folgenden Eigenschaften geeignet:  

-   Es gibt nur wenige Defekte.  
-   Es gibt nur wenige Arbeitsgänge.  
-   Es gibt einen hohen Komponentenverbrauch in frühen Arbeitsgängen.  

### Automatisches Berichtswesen - "Vorwärts"-Buchen pro Arbeitsgang  
Buchen pro Arbeitsgang versetzt Sie in die Lage, den Lagerbestand zu aktualisieren, während ein bestimmter Arbeitsgang aus dem Arbeitsplan des übergeordneten Artikels ausgeführt wird. Die Materialien sind mit dem Arbeitsplan über Verbindungscodes verknüpft, die den Verbindungscodes entsprechen, die auf Komponenten in der Fertigungsstückliste angewendet werden.  

Die Buchung erfolgt, wenn der Arbeitsgang gestartet wurde, der denselben Verbindungscode hat. Gestartet bedeutet, dass mindestens eine Aktivität im FA-Istmeldungs Buch.-Blatt des Arbeitsgangs erfasst wurde. Diese Aktivität kann z. B. lediglich darin bestehen, dass eine Rüstzeit eingegeben wird.  

Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Anzahl der übergeordneten Artikel, die gefertigt werden (erwartete Menge).  

Diese Methode ist am besten geeignet, wenn es viele Arbeitsgänge gibt und bestimmte Komponenten erst spät im Fertigungsablauf benötigt werden. Tatsächlich kann es sein, dass bei einer JIT-Einrichtung (Just-in-Time) die Artikel noch nicht einmal verfügbar sind, wenn die Neuplanung des Fertigungsauftrags gestartet wird.  

Materialien können im Verlauf von Arbeitsgängen verbraucht werden, indem Verbindungscodes verwendet werden. Einige Komponenten werden möglicherweise erst bei den Endmontagearbeitsgängen benötigt und sollten bis dahin nicht aus dem Lager entnommen werden.  

### Automatisches Berichtswesen - "Rückwärts"-Buchen pro Arbeitsgang  
Beim "Rückwärts"-Buchen pro Arbeitsgang wird der Verbrauch erfasst, nachdem der Arbeitsgang im FA-Istmeldungs Buch.-Blatt gebucht wurde.  

Der Vorteil dieser Methode liegt darin, dass die Anzahl der übergeordneten Teile, die im Arbeitsgang fertig gestellt wurden, bekannt ist.  

Material in der Fertigungsstückliste ist über Verbindungscodes mit den Arbeitsplandatensätzen verbunden. Die "Rückwärts"-Buchung erfolgt, wenn ein Arbeitsgang mit einem bestimmten Verbindungscode zusammen mit einem fertigen Teil gebucht wird.  

Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Zahl der übergeordneten Artikel, die für diesen Arbeitsgang als fertig gestellte Menge gebucht wurden. Diese Mengenangabe kann von der erwarteten Menge unterscheiden.  

### Automatisches Berichtswesen - "Rückwärts"-Buchen des gesamten Auftrags  
Bei dieser Berichterstellungsmethode werden keine Verbindungscodes berücksichtigt.  

Komponenten werden erst entnommen, wenn sich der Status des freigegebenen Fertigungsauftrags in *Beendet* geändert hat. Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Zahl der übergeordneten Artikel, die fertig gestellt und in den Lagerbestand übernommen wurden.  

Soll ein gesamter Fertigungsauftrag nach der Methode "Rückwärts" gebucht werden, ist die gleiche Einrichtung wie für die Buchungsmethode "Vorwärts" erforderlich: Die Berichterstellungsmethode muss auf jeder Artikelkarte auf "Rückwärts" festgelegt sein, damit alle Artikel in der übergeordneten Stückliste bei der Berichterstellung berücksichtigt werden. Außerdem müssen alle Verbindungscodes aus der Produktionsstückliste entfernt worden sein. 



Wenn beispielsweise ein Fertigungsauftrag, 800 Meter zu produzieren, 8 Kilogramm einer Komponente benötigt, dann werden, wenn Sie 200 Meter buchen, wie ausgegeben, 2 Kilogramm automatisch als Verbrauch gebucht. Sie können dies durch Kombination der Rückwärtsbuchen und der Verbindungscodes erreichen, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität des abgeschlossenen Arbeitsgangs proportional ist. Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern. Wenn Sie auch Verbindungscodes definieren, dann erfolgt die Berechnung und Buchung, wenn jeder Arbeitsgang beendet ist, und die Menge, die tatsächlich im Arbeitsgang verbraucht wurde, wird gebucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

## Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Bearbeiten** aus.  
3.  Wählen Sie im Inforegister **Beschaffung** im Feld **Buchungsmethode** die Option **Rückwärts** aus.  

    > [!NOTE]  
    >  Wählen Sie **Kommiss. + Rückwärts** aus, wenn die Komponente in einem Lagerplatz verwendet wird, der für die gesteuerte Einlagerung und Kommissionierung eingerichtet ist.  

4.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  
5.  Definieren Sie Verbindungscodes für jeden Arbeitsgang, der die Komponente verbraucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Verwenden Sie nicht dieselbe Routing-Routing-Verbindung für verschiedene Vorgänge im Routing, da dies zur Registrierung des Verbrauchs von Komponenten für jeden verknüpften Vorgang führt.  
6.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Produktionsstückliste** ein und wählen Sie dann den zugehörigen Link.  
7.  Definieren Sie Verbindungscodes von jeder Instanz der Komponente zu dem Arbeitsgang, in dem sie verbraucht wird.

Der Verbrauch wird automatisch gebucht, wenn Sie die Ausgabe registrieren. Weitere Informationen finden Sie unter [Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen](production-how-to-post-output-quantity.md)

## Buchungsmethode

In der folgenden Tabelle werden die verfügbaren Optionen für die Buchungsmethode beschrieben, die Sie auf **Artikel**-Karten und **Lagerhaltungsdaten**-Karten festlegen.

|Option|Beschreibung|
|------------|-------------|  
|Manuell|Erfordert, dass Sie den Verbrauch manuell im FA-Verbrauchs Buch eingeben und buchen.|
|Vorwärts|Bucht Verbräuche automatisch entsprechend den Fertigungsauftragskomponentenzeilen. <br><br>Standardmäßig tritt die Buchung des Komponentenverbrauchs auf, wenn Sie den Status eines Fertigungsauftrags auf **Freigegeben** ändern. Wenn Sie jedoch das Feld **Verbindungscode** in den Fertigungsauftragskomponentenzeilen verwenden, dann erfolgt das Buchen pro Arbeitsgang, wenn der Arbeitsgang beginnt. Weitere Informationen finden Sie unter [Gewusst wie: Arbeitspläne erstellen](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Hinweis**<br>Für Vorausbuchung basiert die entsprechende Buchung, die Sie mit Verbindungscodes erhalten, auf der erwarteten Menge, die in der Komponentenzeile definiert ist. Informationen zu Arbeitsgang-spezifischen Buchungen basierend auf der Isteffektivität finden Sie in der Beschreibung für **Rückwärts** in diesem Thema.<br><br>Wenn der Lagerort oder die Ressourcen, für die diese Komponente verbraucht werden, mit einer Standardlagerplatzstruktur eingerichtet werden, wird der Artikel vom **Off. Fert.-Ber.-Lagerpl.-Code** verbraucht. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Wichtig** <br>Vorausbuchung tritt auch auf, wenn Sie auf **Aktualisieren** auf einem freigegebenen Fertigungsauftrag klicken, der von Grund auf neu erstellt wurde. In diesen direkt erstellten und freigegebenen Fertigungsaufträgen können Sie keine Lagerplatzinformationen ändern, da die Fertigungsauftragskomponentenzeilen generiert werden, wenn Sie den Auftrag aktualisieren, der Komponenten gleichzeitig vorwärts bucht. Wenn Sie Lagerplatzinformationen über Fertigungsauftragskomponentenzeilen ändern möchten, bevor die Vorausbuchung auftritt, muss dieser Auftrag mit dem *geplanten* oder *fest geplanten* Status erstellt werden.|
|Rückwärts|Berechnet und bucht Verbräuche automatisch entsprechend den Fertigungsauftragskomponentenzeilen.<br><br> Standardmäßig tritt die Berechnung und Buchung des Komponentenverbrauchs auf, wenn Sie den Status eines freigegebenen Fertigungsauftrags auf **Beendet** ändern. Wenn Sie jedoch das Feld **Verbindungscode** in den Fertigungsauftragskomponentenzeilen verwenden, dann erfolgt das Berechnen und Buchen beim Beenden jedes Arbeitsgangs.<br><br> **Hinweis** <br>Das Rückwärtsbuchen und die Verbindungscodes können zusammengefasst werden, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität dieses Arbeitsgangs proportional ist. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](#to-flush-components-according-to-operation-output).<br><br> Wenn der Lagerort oder der Arbeitsplatz, für die diese Komponente verbraucht werden, mit einer Standardlagerplatzstruktur eingerichtet werden, wird der Artikel vom **Off. Fert.-Ber.-Lagerpl.-Code** verbraucht.|
|Kommiss. + Vorwärts|Dasselbe wie für die Vorwärtsbuchungsmethode, außer dass es nur für Standorte funktioniert, die entweder eine erweiterte Lagerkonfiguration oder eine Basislagerkonfiguration mit obligatorischen Lagerplätzen verwenden.<br><br> Verbrauch wird aus dem Lagerort berechnet und gebucht, der im Feld **Fert.-Bereitst.-Lagerplatzcode** im Lagerplatz oder dem Arbeitsplatz definiert wird, nachdem die Komponente aus dem Lager kommissioniert wurde.<br><br> **Hinweis** <br>Wenn eine Komponente mit der Kommissionierungs- + Vorausbuchungsmethode eingerichtet wird, kann sie keinen Verbindungscode für einen Arbeitsgang haben, der mit der Vorausbuchungsmethode eingerichtet wurde. Die Komponente wird dann automatisch geleert, wenn der Arbeitsgang beginnt, was das Anfordern der Kommissionierungsaktivität unmöglich macht.|
|Kommiss. + Rückwärts|Dasselbe wie für die Rückwärtsbuchungsmethode, außer dass es nur für Standorte funktioniert, die entweder eine erweiterte Lagerkonfiguration oder eine Basislagerkonfiguration mit obligatorischen Lagerplätzen verwenden.<br><br> Verbrauch wird aus dem Lagerort berechnet und gebucht, der im Feld **Fert.-Bereitst.-Lagerplatzcode** im Lagerplatz oder dem Arbeitsplatz definiert wird, nachdem die Komponente aus dem Lager kommissioniert wurde.|

## Siehe auch

[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
