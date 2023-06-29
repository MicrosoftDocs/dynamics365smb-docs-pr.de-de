---
title: Betriebskalender einrichten
description: 'Das Erstellen und Aktivieren eines Arbeitsplatzkalenders umfasst mehrere Aufgaben, einschließlich des Einrichtens von Betriebskalendern und des Erstellens von Arbeitsschichten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="set-up-shop-calendars"></a><a name="set-up-shop-calendars"></a>Betriebskalender einrichten

In einem Arbeitsplatzgruppenkalender werden die Arbeitstage/-stunden, Schichten, Feiertage und Fehlzeiten angegeben, die die verfügbare Bruttokapazität der Arbeitsplatzgruppe (zeitlich gemessen) entsprechend ihren definierten Effektivitäts- und Kapazitätswerten bestimmen.

Ein grundlegender Schritt beim Berechnen eines spezifischen Arbeitsplatzgruppenkalenders ist das Einrichten eines oder mehrerer allgemeiner Betriebskalender. In einem Betriebskalender wird eine Standardarbeitswoche gemäß den Anfangs- und Endzeit der einzelnen Arbeitstage und dem Plan der einzelnen Schichten definiert. Darüber hinaus werden im Betriebskalender die festen Feiertage im gesamten Jahr definiert.  

Nachfolgend ist beschrieben, wie ein alternativer Arbeitsplatzkalender eingerichtet wird. Die Schritte sind ähnlich, wenn Sie Arbeitsplatzkalender einrichten.  

## <a name="to-create-work-shifts"></a><a name="to-create-work-shifts"></a>Arbeitsschichten erstellen
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsschichten** ein und wählen Sie dann die entsprechende Verknüpfung.  
2.  Geben Sie in einer leeren Zeile eine Zahl im Feld **Code** ein, um die Schicht zu bestimmen, z. B. **1**.  
3.  Geben Sie im Feld **Beschreibung** eine Beschreibung der Schicht ein, z. B. **1. Schicht**.  
4.  Optional füllen Sie Zeilen für eine zweite oder dritte Schicht aus.  

Selbst wenn Ihre Arbeitsplatzgruppen nicht in verschiedenen Schichten arbeiten, geben Sie mindestens einen Schichtcode ein.  

## <a name="to-set-up-a-shop-calendar"></a><a name="to-set-up-a-shop-calendar"></a>Einen Betriebskalender einrichten
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Betriebskalender** ein und wählen Sie dann den zugehörigen Link.  
2.  Geben Sie in einer leeren Zeile eine Zahl im Feld **Code** ein, um den Betriebskalender zu bestimmen.  
3.  Geben Sie im Feld **Beschreibung** eine Beschreibung für den Betriebskalender ein.  
4.  Wählen Sie die **Arbeitstage** Aktion aus.
5.  Auf der Seite **Betriebskalenderarbeitstage** bestimmen Sie eine ganze Arbeitswoche mit den Start- und Endzeiten für jeden Tag.  

    Wählen Sie im Feld **Schichtcode** eine der Schichten aus, die Sie zuvor definierten. Fügen Sie eine Zeile für jeden Arbeitstag und jede Schicht hinzu. Beispiel:  

    Montag 07:00 15:00 1   
    Dienstag 07:00 15:00 1  

    Wenn Sie einen Betriebskalender mit zwei Schichten benötigen, nehmen Sie eine Eingabe wie im folgt vor:  

    Montag 07:00 15:00 1   
    Montag 15:00 23:00 2  
    Dienstag 07:00 15:00 1  
    Dienstag 15:00 23:00 2  

    Alle Wochentage, die nicht im Betriebskalender definiert sind, z. B. Samstag und Sonntag, werden einfach als Nicht-Werktage betrachtet, und sie weisen im Arbeitsplatzgruppenkalender keine verfügbare Kapazität auf.  

    Wenn alle Arbeitstage einer Woche definiert sind, können Sie die Seite **Betriebskalenderarbeitstage** schließen und mit der Eingabe von Feiertagen fortfahren:  

6.  Auf der Seite **Betriebskalender** wählen Sie den Betriebskalender, und wählen die **Feiertage** Aktion aus.
7. Auf der Seite **Betriebskalender-Feiertage** definieren Sie nun die Feiertage des Jahres, indem Sie Anfangsdatum und -uhrzeit sowie Enddatum und -uhrzeit sowie eine Beschreibung des jeweiligen Feiertags in einzelnen Zeilen eingeben. Beispiel. Beispiel:  

    04.07.14 0:00:00 23:59:00 Sommerurlaub  
    05.07.14 0:00:00 23:59:00 Sommerurlaub  
    06.07.14 0:00:00 23:59:00 Sommerurlaub  

Die definierten Feiertage weisen im Arbeitsgruppenkalender eine verfügbare Kapazität von Null auf.  

Der Betriebskalender kann nun einer Arbeitsplatzgruppe zugewiesen werden, um einen Arbeitsplatzgruppenkalender zu berechnen, anhand dessen die gesamte Arbeitsgangplanung für die Zeit dieser Arbeitsplatzgruppe erfolgt.  

## <a name="to-calculate-a-work-center-calendar"></a><a name="to-calculate-a-work-center-calendar"></a>Einen Arbeitsplatzgruppenkalender berechnen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsplatzgruppen** ein, und wählen Sie dann den zugehörigen Link.
2. öffnen Sie den Arbeitsplatz, den Sie aktualisieren möchten.  
3. Wählen Sie im Inforegister Planung im Feld **Betriebskalendercode** den Kalender aus, der in dieser Arbeitsplatzgruppe als Grundlage für einen Arbeitsplatzgruppenkalender verwendet werden soll.  
4. Wählen Sie die Aktion **Kalender** aus.  
5. Klicken Sie auf der Seite **Arbeitsplatzgruppenkalender** auf **Aktionen, Matrix anzeigen**.  

    Links auf der Matrixseite werden die eingerichteten Arbeitsplatzgruppen aufgelistet. Rechts befindet sich ein Kalender, in dem die verfügbaren Kapazitäten pro Arbeitstag in der definierten Einheit angegeben werden, z. B. **480** Minuten. Jede Zeile stellt den Kalender einer Arbeitsplatzgruppe dar.  

    > [!NOTE]  
    >  Sie können die Kapazitätswerte auch pro Woche oder Monat anzeigen, indem Sie die Auswahl im Feld **Anzeigen nach** auf dem Inforegister Matrixoptionen auf der Seite **Arbeitsplatzgruppenkalender** ändern.  

    Um den neuen Betriebskalender als eine Zeile in der ausgewählten Arbeitsgruppe widerzuspiegeln, muss er zunächst berechnet werden.  

6.  Wählen Sie die Aktion **berechnen** aus.  
7.  Auf dem Inforegister **Arbeitsplatzgruppe** können Sie einen Filter festlegen, sodass nur die Berechnung für eine Arbeitsplatzgruppe ausgeführt wird. Wenn kein Filter festgelegt wird, werden alle vorhandenen Arbeitsplatzgruppenkalender berechnet.  
8.  Legen Sie das Anfangs- und das Enddatum des zu berechnenden Kalenderzeitraums fest, z. B. ein Jahr vom 01.01.14 bis zum 31.12.14.
9. Klicken Sie auf die Schaltfläche **OK**, um die Kapazität zu berechnen.  

Kalenderposten werden nun erstellt bzw. aktualisiert und zeigen die verfügbare Kapazität pro Tag oder sonstiger Periode an, entsprechend den folgenden drei Sätzen von Stammdaten:  

- Die im zugewiesenen Betriebskalender definierten Arbeitstage und Schichten.  
- Der Wert im Feld **Kapazität** auf der Arbeitsplatzgruppenkarte.  
- Der Wert im Feld **Effektivität** auf der Arbeitsplatzgruppenkarte  

Der berechneten Arbeitsplatzgruppenkalender legt jetzt fest, wann und wie viel Kapazität in dieser Arbeitsplatzgruppe verfügbar ist. Dieses steuert die detaillierte Planung von Arbeitsgängen, die in der Arbeitsplatzgruppe ausgeführt werden.  

## <a name="to-record-work-center-absence"></a><a name="to-record-work-center-absence"></a>Fehlzeiten für Arbeitsplatzgruppen erfassen
1.  Klicken Sie auf der Seite **Arbeitsplatzgruppenkalender** auf **Aktionen, Matrix anzeigen**.
2. Wählen Sie auf der Seite **Arbeitsplatzgruppenkalendermatrix** die Arbeitsplatzgruppe und den Kalendertag aus, an dem die Fehlzeit aufgezeichnet werden soll, und klicken Sie anschließend auf **Verknüpfte Informationen, Planung, Fehlzeiten**.  
3.  Legen Sie auf der Seite Fenster **Fehlzeiten** die Anfangs- und die Endzeit für die Fehlzeiten an diesem Tag fest, und geben Sie eine Begründung an. Beispiel:  

    25.01.01 08:00 10:00 Wartung  

4.  Wählen Sie die **Aktualisieren** Aktion aus, und schließen Sie dann die Seite **Fehlzeiten**.  

Die Kapazität des ausgewählten Tages hat sich nun um die aufgezeichnete Fehlzeit verringert.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
[Basiskalender einrichten](across-how-to-assign-base-calendars.md)  
[Arbeitsplätze und Arbeitsplatzgruppen einrichten](production-how-to-set-up-work-and-machine-centers.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
