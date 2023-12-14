---
title: Neue Kapazität einrichten
description: 'Exemplarische Vorgehensweise, um zu erfahren, wie Sie einen neuen Arbeitsplatz mit einem Kapazitätskalender für eine einzelne Schicht in Business Central einrichten.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-new-capacity"></a>Exemplarische Vorgehensweise: Neue Kapazität einrichten

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee bei der Kapazitätsverwaltung.  

## <a name="scenario"></a>Szenario

Sie sind der Produktionsplaner bei Contoso Coffee. Als Reaktion auf Änderungen im Fertigungsbereich müssen Sie einen neuen Arbeitsplatz „Testabteilung“ einrichten. Das neue Arbeitszentrum hat ein Maschinenzentrum, „Test“. Die neuen Zentren müssen über einen Kapazitätskalender für eine Schicht von Montag bis Freitag von 08:00 Uhr bis 16:00 Uhr verfügen.  

## <a name="steps"></a>Schritte

1. Richten Sie die Arbeitsplatzgruppe ein.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsplatzgruppen** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Nr.** |700|
        |**Name** |Testabteilung|
        |**Abteilungscode** |1, Produktionsabteilung|
        |**EK-Preis**|3,25|
        |**Einstandspreisberechnung**|Zeit|
        |**Buchungsmethode**|Manuell|
        |**Produktbuchungsgruppe**|OHNE MWST</br></br>Beachten Sie, dass diese Auswahl von Ihrer Buchhaltungseinrichtung und Ihrem Land/Ihrer Region abhängt.|
        |**Einheitencode** |MINUTEN|
        |**Kapazität** |0|
        |**Effektivität** |90|
        |**Betriebskalendercode** |1|

        Im Feld **Betriebskalendercode** bedeutet die Einstellung 1 eine Schicht von Montag bis Freitag.

    3. Schließen Sie die Arbeitsplatzkarte.

2. Richten Sie die Arbeitsplätze ein.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsplätze** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Nr.** |760|
        |**Name** |Testen|
        |**Arbeitsplatzgruppennr.** |700, Testabteilung|
        |**EK-Preis**|3,25|
        |**Buchungsmethode**|Manuell|
        |**Produktbuchungsgruppe**|OHNE MWST</br></br>Beachten Sie, dass diese Auswahl von Ihrer Buchhaltungseinrichtung und Ihrem Land abhängt.|
        |**Kapazität** |1|
        |**Effektivität** |90|
    3. Erweitern Sie das Inforegister **Arbeitsplan Einrichtung**, und geben Sie dann in das Feld **Einrichtungszeit** den Wert *10* ein.  

3. Berechnen Sie die Arbeitsplatzkalenderkapazität.  

    1. Wählen Sie die Aktion **Kalender** aus.  

    2. Legen Sie auf der Seite **Arbeitsplatzkalender** auf dem Inforegister **Matrixoptionen** das Feld **Anzeigen nach** auf *Monat* fest.  

    3. Wählen Sie die Aktion **Matrix anzeigen** aus.  

    4. Klicken Sie auf der Seite **Arbeitsplatzkalender - Matrix** auf **Berechnen**.  

    5. Legen Sie auf der Seite **Arbeitsplatzkalender berechnen** auf dem Inforegister **Optionen** das Feld **Startdatum** auf *Januar 01* fest.  

    6. Stellen Sie das Feld **Enddatum** auf den 31. Dezember ein.  

    7. Füllen Sie auf dem Inforegister **Arbeitsplatz** das Filterfeld **Nr.** mit *760, Testen* aus.  

    8. Wählen Sie die Schaltfläche **OK**. Nachdem der Batch-Job abgeschlossen ist, kehrt er zur Seite **Arbeitsplatzkalender - Matrix** zurück.  

    9. Wählen Sie die Aktion **Aktualisieren** aus.  

    10. Führen Sie in der Zeile für den Arbeitsplatz 760, Test, einen Drilldown zum Wert in der Spalte Januar durch.  

Auf der **Kalendereinträge**-Seite sind die Tageskapazitätseinträge im **Kapazität (Gesamt)**-Feld 480 Minuten. Dies entspricht einer Acht-Stunden-Schicht für jeden Arbeitstag. Auch das **Kapazität (effektiv)**-Feld zeigt 432 Minuten. Dies spiegelt den 90-prozentigen Wirkungsgrad wider, den Sie dem Maschinenzentrum zugeschrieben haben.  

## <a name="see-also"></a>Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
