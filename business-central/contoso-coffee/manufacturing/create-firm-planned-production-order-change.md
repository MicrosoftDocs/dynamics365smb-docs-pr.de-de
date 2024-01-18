---
title: Fest geplante Fertigungsaufträge erstellen und ändern
description: 'Exemplarische Vorgehensweise für einen Produktionsplaner bei Contoso Coffee, der einen fest geplanten Produktionsauftrag erstellen und ihn dann ändern möchte.'
ms.date: 12/12/2023
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Exemplarische Vorgehensweise: Neuen fest geplanten Produktionsauftrag erstellen und ändern

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee, um mit Fertigungsaufträgen zu arbeiten.  

## Szenario

Eduardo, der Produktionsplaner bei Contoso Coffee, muss einen neuen Produktionsauftrag für 10 Einheiten des Artikels **SP-SCM1009, Flughafen** erstellen, der am 28. April fällig ist. Eduardo plant diesen rückwärts und überprüft, ob er den Auftrag am 27. April starten kann.  

Kurz nachdem er diese Aufgabe erledigt hat, wird Eduardo gebeten, die Bestellung auf 50 Einheiten zu erhöhen. Wenn er dies tut, verschiebt die Rückwärtsterminierungsfunktion das Startdatum des Auftrags auf einen zu frühen Zeitpunkt. Also plant Eduardo den Auftrag für den 23. April voraus, um ein realistischeres Fertigstellungsdatum zu ermitteln.  

## Schritte

1. Erstellen Sie den ersten Fertigungsauftrag für 10 Einheiten des Artikels **SP-SCM1009, Airpot**.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") , geben Sie **Geplante Prod. Aufträge** ein, und wählen Sie dann den zugehörigen Link aus.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Herkunftsart** |Artikel|
        |**Herkunftsnr.** |SP-SCM1009|
        |**Menge** |10|
        |**Fälligkeitsdatum**|April 28  |

    3. Wählen Sie die Aktion **FA aktualisieren** aus.  

    4. Akzeptieren Sie auuf der Seite **FA aktualisieren** alle Standardwerte, und wählen Sie dann die Schaltfläche **OK** aus, um den Vorgang zu starten.  

        In der aktuellen Einrichtung verwendet dieser Prozess die Rückwärtsterminierung. In der neuen Zeile des Fertigungsauftrags ist das Startdatum der 26. April.  

2. Ändern Sie die Menge des Fertigungsauftrags in 50 Einheiten, und planen Sie den Auftrag.  

    1. Wählen Sie im Inforegister **Zeilen** die **Fertigungsstückliste** aus, wählen Sie die kürzlich hinzugefügte Zeile aus, und geben Sie dann im Feld **Menge** den Wert *50* ein.  

3. Wählen Sie die Aktion **FA aktualisieren** aus.  

    Das Startdatum wurde nun auf den 20. April verschoben. Dieses Datum ist für Eduardo nicht akzeptabel.

4. Lösen Sie eine Vorwärtsterminierung des Fertigungsauftrags aus.

    1. Legen Sie im Inforegister **Zeitplan** das Feld **Anfangsdatum** auf *23. April* fest.

    Das Startdatum des Auftrags ist jetzt der 25. April und das Enddatum ist der 2. Mai. Das Fälligkeitsdatum für den Auftrag ist auf den Folgetag, den 3. Mai, festgelegt. Eduardo weiß jetzt, dass es bis zum 3. Mai dauern wird, die erhöhte Auftragsmenge zu liefern.

> [!NOTE]
> Wenn ein Auftrag durch Ändern des Start- oder Enddatums geändert wird, ist der Batchauftrag **Fertigungsauftrag aktualisieren** nicht erforderlich, da alle Daten automatisch neu berechnet werden.

Der neue Fertigungsauftrag ist nun eingerichtet und Eduardos Anforderungen sind erfüllt.  

## Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
