---
title: Varianten
description: 'Exemplarische Vorgehensweise, um zu erfahren, wie die Bedarfsplanung für jede Variante eines Produkts in Business Central aktualisiert wird.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Exemplarische Vorgehensweise: Varianten

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee, um mehr über Varianten zu erfahren.

## Szenario

Sie sind der Produktionsplaner bei Contoso Coffee. Sie müssen die Bedarfsplanung für jede Variante des Artikels SP-SCM1006, AutoDripLite aktualisieren. Da sie unterschiedliche Farben haben, müssen Sie darauf achten, dass für jede Variante die richtige Stückliste (BOM) verwendet wird. Führen Sie das Planungsarbeitsblatt aus, um den Vorrat zu berechnen.  

## Schritte

1. Richten Sie die Lagerhaltungseinheiten für Artikel SP-SCM1006, AutoDripLite ein. Weisen Sie eine Stückliste für SKU mit den Varianten ROT und WEISS zu.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol einrichten möchten, geben Sie *Artikel* ein und wählen dann den entsprechenden Link.  

    2. Öffnen Sie den Artikel **SP-SCM1006, AutoDripLite**.

    3. Wählen Sie die **Lagerhaltungsdaten erstellen** Aktion aus.  

    4. Legen Sie das Feld **Erstellen pro** auf *Standort & Variante* fest.

    5. Legen Sie einen Filter für den Standort auf *MAIN* fest, und wählen Sie dann die **OK**-Taste aus.

    6. Wählen Sie die **Lagereinheiten**-Aktion aus.  

    7. Aktualisieren Sie die Produktionsstücklisten für die folgenden Lagereinheiten:

        1. ROT auf MAIN, SP-SCM1006-RED festlegen  

        2. WEISS auf MAIN, SP-SCM1006-WEISS festlegen  

        3. Lassen Sie die Produktionsstücklistennummer für SCHWARZ auf MAIN leer  

2. Aktualisieren Sie die Produktionseinrichtung und berücksichtigen Sie die Bedarfsplanung für Standorte und Varianten.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie *Produktionseinrichtung* ein, und wählen Sie dann den zugehörigen Link.  

    2. Schalten Sie das Feld **Planung an Lagerort verwenden** ein.

    3. Schalten Sie das Feld **Planung bei Variante verwenden** ein.

    4. Schließen Sie das **Produktionseinrichtung**-Fenster.

3. Erstellen Sie eine neue monatliche Bedarfsplanung, *AUTODRIP*. Filtern Sie sie nach dem Artikel SP-SCM1006 und dem Standort MAIN. Legen Sie die Nachfrage für Mai für jede Variante fest. 

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie *Bedarfsplanung* ein, und wählen Sie dann den zugehörigen Link.

    2. Erstellen Sie eine neue Bedarfsplanung mit dem Namen *AUTODRIP*.

    3. Wählen Sie die **Bedarfsplanung bearbeiten**-Aktion aus.

    4. Wählen Sie im Feld **Anzeigen nach** den Wert *Monat* aus.

    5. Wählen Sie im Feld **Artikelfilter** die Option *SP-SCM1006* aus.

    6. Schalten Sie das Feld **Planung an Lagerort verwenden** ein.

    7. Wählen Sie im Feld **Lagerortfilter** die Option *MAIN* aus.

    8. Schalten Sie das Feld **Planung bei Variante verwenden** ein.

    9. Für jede Zeile aktualisierte Werte in der Mai-Spalte

        1. ROT auf MAIN, 100 einstellen

        2. WEISS auf MAIN, 200 festlegen

        3. SCHWARZ auf MAIN, 300 festlegen

    10. Bedarfsprognose-Fenster schließen

4. Führen Sie den MPS-Plan im Mai für erstellte Bedarfsprognosen aus. Überprüfen Sie die Komponenten, um zu sehen, dass die Farbe des Artikels mit der Variante korreliert.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie *Planungsarbeitsblatt* ein und wählen Sie dann den zugehörigen Link.

    2. Wählen Sie die **Neuplanung berechnen** Aktion aus.

    3. Schalten Sie das **MPS**-Feld ein.

    4. Schalten Sie das **MPS**-Feld aus.

    5. Im **Startdatum**-Feld die Option *1. Mai* auswählen

    6. Im **Enddatum**-Feld die Option *31. Mai* auswählen

    7. Im **Prognose verwenden**-Feld die Option *AUTODRIP* auswählen

    8. Wählen Sie die Aktion **OK**.

    9. Wählen Sie für jede erstellte Zeile die **Komponenten**-Aktion aus und überprüfen Sie, welche Farbe verwendet wird.  

## Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
