---
title: Auftragsplanung zum Erstellen und Reservieren von Lieferungen verwenden
description: 'Exemplarische Vorgehensweise, um zu erfahren, wie Sie die Auftragsplanung verwenden, um den erforderlichen Produktionsauftrag für die Lieferung in Business Central zu erstellen.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Exemplarische Vorgehensweise: Auftragsplanung zum Erstellen und Reservieren von Lieferungen verwenden

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee für Auftragsplanung.

## Szenario

Sie sind der Produktionsplaner bei Contoso Coffee. Sie haben einen Produktionsauftrag für 100 Einheiten des Artikels **SP-SCM1009, Airpot** erstellt, und Sie möchten Unterbaugruppen für diesen Auftrag planen. Mit der Auftragsplanung legen Sie den erforderlichen Fertigungsauftrag für die Versorgung an. Da Sie den Produktionsauftrag erstellen, um die Anforderungen eines bestimmten Auftrags zu erfüllen, entscheiden Sie sich, die Ausgabe des Produktionsauftrags zu reservieren.  

## Schritte

1. Erstellen Sie einen neuen freigegebenen Produktionsauftrag für 100 Einheiten des Artikels **SP-SCM1009, Airpot**.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Freigegebener Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Herkunftsart** |Artikel|
        |**Herkunftsnr.** |SP-SCM1009|
        |**Menge** |100|
    3. Wählen Sie die Aktion **FA aktualisieren** aus.  

    Achten Sie auf die Nummer des veröffentlichten Fertigungsauftrags.

2. Öffnen Sie die **Auftragsplanung**-Seite und berechnen Sie einen neuen Plan.

    1. Wählen Sie die Aktion **Planung** aus.  

    2. Klicken Sie auf der Seite **Auftragsplanung** auf Funktionen und dann auf **Planung berechnen**.  

    3. Scrollen Sie nach unten zur Bedarfszeile, die den freigegebenen Produktionsauftrag darstellt, den Sie zuvor erstellt haben.  

    4. Erweitern Sie die Positionen, um die Details für die Bedarfszeile anzuzeigen. Bestätigen Sie, dass es sich um einen Vorschlag für einen Produktionsauftrag von 100 Einheiten von Artikel 1001 handelt.  

3. Erstellen Sie einen neuen Produktionsauftrag für 100 Artikeleinheiten von **SP-BOM2000, Behälterbaugruppe**, und reservieren Sie die Ausgabe dieses Produktionsauftrags für den zugehörigen übergeordneten Auftrag.  

    1. Aktivieren Sie das Kontrollkästchen im Feld **Reservieren** in der Bedarfszeile für die 100 Einheiten des Artikels SP-BOM2000.

    2. Wählen Sie die **Auftrag erstellen** Aktion aus.  

    3. Legen Sie das Feld **Aufträge erstellen für** auf *die aktive Zeile* fest.  

    4. Stellen Sie das **Produktionsauftrag erstellen**-Feld auf *Fest geplant* ein.

    5. Wählen Sie die Schaltfläche **OK**, um den Fertigungsauftrag zu erstellen.

    6. Auf der **Auftragsplanung**-Seite bestätigen Sie, dass die Bedarfszeile für die 100 Einheiten von Artikel 1001 entfernt wurde.

Das war's für die Auftragsplanung in [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
[Info zu Fertigungsaufträgen](../../production-about-production-orders.md)  
