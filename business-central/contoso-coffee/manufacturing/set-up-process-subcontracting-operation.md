---
title: Fremdarbeitsvorgang einrichten und verarbeiten
description: 'Exemplarische Vorgehensweise, um zu erfahren, wie Sie einen Unterauftragsvorgang in Business Central einrichten und verarbeiten.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="set-up-and-process-a-subcontracting-operation"></a>Fremdarbeitsvorgang einrichten und verarbeiten

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee für Fremdarbeiten.

## <a name="scenario"></a>Szenario

Sie sind der Produktionsplaner bei Contoso Coffee. Aufgrund von Kapazitätsengpässen planen Sie, einen Subunternehmer mit der Produktion des Artikels **SP-SCM1009, Airpot** zu beauftragen.

Hier erstellen Sie mit Arbeitsplan – SP-SCM1009-SUB-2 einen neuen freigegebenen Produktionsauftrag für 12 Einheiten des Artikels SP-SCM1009, Airpot. Verwenden Sie das Unterauftragsarbeitsblatt, um eine Bestellung für die Produktion zu generieren, und schließen Sie dann den Vorgang ab, indem Sie die Bestellung erhalten und in Rechnung stellen.

## <a name="steps"></a>Schritte

1. Erstellen Sie einen neuen freigegebenen Produktionsauftrag für 12 Einheiten des Artikels SP-SCM1009, Airpot.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Freigegebener Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Herkunftsart** |Artikel|
        |**Herkunftsnr.** |SP-SCM1009|
        |**Menge** |100|
    3. Wählen Sie die Aktion **FA aktualisieren** aus.  

2. Ersetzen Sie den Arbeitsplan durch SP-SCM1009-SUB-2 in der Produktionsauftragsposition und aktualisieren Sie dann den Produktionsauftrag, aber nur für den Arbeitsplan.  

    1. Fügen Sie den Zeilen im freigegebenen Produktionsauftrag das Feld Produktionsarbeitsplannummer hinzu.<!--in code, this is marked as visible=false-->

    2. Ändern Sie das **Routing-Nr.**-Feld von *SP-SCM1009-SERIE* zu *SP-SCM1009-SUB-2*.  

    3. Wählen Sie die Aktion **FA aktualisieren** aus.  

    4. Auf der **Produktionsauftrag aktualisieren**-Anforderungsseite löschen Sie die Felder **Positionen** und **Komponentenbedarf**, sodass die Aufgabe nur für Routing ausgeführt wird, und wählen Sie dann die **OK**-Schaltfläche.

3. Verwenden Sie das Arbeitsblatt für Fremdarbeit, um eine Bestellung für den fremdvergebenen Arbeitsgang für den Produktionsauftrag zu generieren, den Sie in Schritt 2 erstellt haben.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Fremdarbeitenarbeitsblätter** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Fremdarbeit berechnen** aus.

    3. Wählen Sie das Feld **Aktionsnachricht akzeptieren** für die neue Position aus.

    4. Wählen Sie die Aktion **Aktionsnachricht austragen**.  

    5. Auf der **Ereignismeld. durchf. - Best.**-Anforderungsseite akzeptieren Sie alle Standardwerte und wählen Sie dann **OK**.

    6. Wählen Sie nach Abschluss des Batch-Jobs **OK** aus, um das Unterauftragsarbeitsblatt zu schließen.  

4. Die Bestellung entgegennehmen und fakturieren.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  

    2. In der Liste **Einkaufsbestellungen** suchen Sie nach der Bestellung des Kreditors 82000 Subunternehmer.

    3. Geben Sie im Feld **Kred.-Rechnungsnr** *542349* ein.

    4. Im **Positionen**-Inforegister wählen Sie die Zeile aus, und legen Sie dann das Feld **EK-Preis** auf *18* fest.

    5. Wählen Sie die Aktion **Buchen**.  

    6. Wählen Sie in der Anforderungsnachricht die Option **Lieferung und Rechnung** aus.  

Die Ausgabe des Artikels SP-SCM1009 Airpot ist jetzt registriert.

## <a name="see-also"></a>Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
