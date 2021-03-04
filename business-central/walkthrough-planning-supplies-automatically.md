---
title: Walkthrough - Vorräte automatisch planen | Microsoft Docs
description: Die Begriffe Planung ausführen oder Nettobedarf ausführen beziehen sich auf die Berechnung der Produktions-Programmplanung und des Materialbedarfsplans anhand des tatsächlichen und geplanten Bedarfs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 04483a81793f21a6011c142433b830f678adf85d
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035706"
---
# <a name="walkthrough-planning-supplies-automatically"></a>Exemplarische Vorgehensweise: Automatische Beschaffungsplanung

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Die Begriffe Planung ausführen oder Nettobedarf ausführen beziehen sich auf die Berechnung der Produktions-Programmplanung und des Materialbedarfsplans anhand des tatsächlichen und geplanten Bedarfs.  

-   Prod.-Programmplanung ist die Berechnung eines Produktionsplans, der auf dem tatsächlichen Bedarf und der Absatzplanung basiert. Die Berechnung der Produktionsprogrammplanung wird für Endartikel mit einer Planung oder einer Verkaufsauftragszeile durchgeführt. Diese Artikel werden als "Prod.-Programmplanungsartikel" bezeichnet und werden dynamisch gekennzeichnet, wenn die Berechnung gestartet wird.  
-   Nettobedarf ist die Berechnung der Materialbedarfe auf Basis des tatsächlichen Bedarfs für Komponenten sowie der Absatzplanung auf Komponentenebene. Der Nettobedarf wird nur für Artikel berechnet, die keine Prod.-Programmplanungsartikel sind. Der Hauptzweck eines Nettobedarfs besteht darin, terminierte formale Pläne (nach Artikeln) aufzustellen, um den richtigen Artikel zur richtigen Zeit am richtigen Ort in der richtigen Menge bereitzustellen.  

 Sowohl für die Prod.-Programmplanung (MPS) als auch für den Nettobedarf (MRP) wird derselbe Planungsalgorithmus verwendet. Die Planungsalgorithmen arbeiten mit Aufrechnung, Wiederverwendung vorhandener Beschaffungsaufträge und Ereignismeldungen. Der Planungssystemprozess untersucht, welche Mengen momentan oder zukünftig benötigt werden (Bedarf) und welche Mengen verfügbar sind oder erwartet werden (Vorrat). Wenn diese Mengen gegeneinander aufgerechnet werden, werden Ereignismeldungen im Planungsvorschlag angezeigt. Ereignismeldungen sind Vorschläge für das Erstellen eines neuen Beschaffungsauftrags, Ändern eines Beschaffungsauftrags (Menge oder Datum) oder Stornieren eines vorhandenen Beschaffungsauftrags. Bei Beschaffungsaufträgen kann es sich um Fertigungsaufträge, Bestellungen und Umlagerungsaufträge handeln. Weitere Informationen finden Sie unter [Designdetails: Beschaffungsplanung](design-details-supply-planning.md)  

 Das Planungsergebnis wird zum Teil aus den Bedarf-Bestand-Sätzen in der Datenbank und zum Teil durch die Einrichtung von Lagerhaltungsdatenkarten oder Artikelkarten, Fertigungsstücklisten und Arbeitsplänen berechnet.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
 In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie das Beschaffungsplanungssystem verwenden, um alle Bestellungen und Fertigungsaufträge automatisch zu planen, die erforderlich sind, um 15 Tourenräder zu produzieren, die in verschiedenen Verkaufsaufträgen angefordert wurden. Um eine klare und realistische exemplarische Vorgehensweise zu bieten, wurde die Anzahl der Planungszeilen begrenzt, indem alle anderen Nachfrage-Angebots-Sätze im Demounternehmen CRONUS AG außer dem Verkaufsbedarf am Standort OST herausgefiltert wurden.  

 In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Erstellen des Verkaufsauftrags und Berechnen eines vollständigen Beschaffungsplans  
-   Anzeigen der Planungsparameter und Bedarfsverursacherposten der Planungszeilen  
-   Automatisches Erstellen der vorgeschlagenen Beschaffungsaufträge  
-   Erstellen eines neuen Verkaufsbedarfs und entsprechende Neuplanung  

## <a name="roles"></a>Rollen  

-   Produktionsplaner  
-   Einkäufer  

## <a name="prerequisites"></a>Voraussetzungen  
 Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

-   Das Demounternehmen CRONUS AG.  
-   Ändern Sie, wie im Abschnitt Vorbereiten der Beispieldaten dieser exemplarischen Vorgehensweise beschrieben, verschiedene Artikelkonfigurationswerte.  

## <a name="story"></a>Hintergrund  
 Der Debitor, Cannon Group PLC, bestellt fünf Rennräder mit Liefertermin am 05.02.2021 (5. Februar).  

 Jürgen, der Produktionsplaner, führt die routinemäßige Beschaffungsplanung für die erste Woche im Februar 2021 aus. Er filtert nach seinem eigenen Standort, OST, und gibt als Planungsintervall 23.01.2021 bis 07.02.2021 ein, bevor er den ersten Beschaffungsplan berechnet.  

 In dieser Woche ist nur für den Verkaufsauftrag der Möbel-Meller KG ein Bedarf vorhanden. Jürgen sieht, dass für keine der Planungszeilen Warnungen vorliegen, und fährt mit der Erstellung von Beschaffungsaufträgen für die vorgeschlagenen Planungszeilen ohne Änderungen fort.  

 Am nächsten Tag (noch bevor die anfänglichen Beschaffungsaufträge gestartet oder gebucht wurden) wird Jürgen benachrichtigt, dass ein anderer Debitor zehn Rennräder mit Liefertermin am 12.02.2021 bestellt hat. Er führt eine Neuberechnung aus, um den Beschaffungsplan entsprechend dem geänderten Bedarf anzupassen. Die Neuberechnung ergibt eine Änderungsplanung, in der Änderungen der Zeit und Menge einiger Beschaffungsaufträge aus dem ersten Berechnungslauf vorgeschlagen werden.  

 Während der verschiedenen Planungsschritte überprüft Jürgen die relevanten Aufträge. Er verwendet die Funktion "Bedarfsverursacher", um festzustellen, welcher Bedarf von welchem Bestand abgedeckt wird.  

## <a name="preparing-sample-data"></a>Vorbereiten der Beispieldaten  
 Erstellen Sie Lagerhaltungsdaten für das Rennrad und all seine Komponenten, Artikelnummern 1001 bis 1300. (Einige Komponenten werden abgezogen, um den Vorgang zu vereinfachen.) Passen Sie die Planungsparameter der kommissionierten Komponenten an, um ein transparenteres Planungsergebnis zu erhalten.  

### <a name="to-create-stockkeeping-units"></a>So erstellen Sie Lagerhaltungsdaten  

1.  Öffnen Sie die Artikelkarte für Artikel 1001, Rennrad.  
2.  Wählen Sie die **Lagerhaltungsdaten erstellen** Aktion aus.  
3.  Übernehmen Sie auf der Seite **Lagerhaltungsdaten erstellen** alle Optionen und Filter, und klicken Sie dann auf **OK**.  
4.  Wiederholen Sie die Schritte 1 bis 3 für alle Artikel im Nummernbereich 1100 bis 1300.  

### <a name="to-change-selected-planning-parameters"></a>Ausgewählte Planungsparameter ändern  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagermengeneinheiten** ein, und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie die OST Lagerhaltungsdatenkarte für Artikel 1100, Vorderrad.  
3.  Füllen Sie im Inforegister **Planung** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Wiederbeschaffungsverfahren|Sicherheitsbestand|Loskumulierungsperiode|Neuplanungsperiode|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Los-für-Los|Leer|2W|2W|  

4.  Wiederholen Sie die Schritte 2 und 3 für alle SKUs im Nummernbereich 1100 bis 1300.  

 Damit ist die Vorbereitung der Beispieldaten für die exemplarische Vorgehensweise abgeschlossen.  

## <a name="creating-a-regenerative-supply-plan"></a>Erstellen einer Beschaffungsneuplanung  
 Als Antworten auf einen neuen Verkaufsauftrag für fünf Rennräder, beginnt Andreas mit dem Planungsprozess, indem er Optionen und Filter setzt und das Planungsintervall festlegt, um jeden anderen Bedarf auszuschließen, mit Ausnahme des Bedarfs der ersten Woche vom Februar am Standort OST. Er berechnet als Erstes eine Produktions-Programmplanung (MPS) und berechnet dann einen vollständigen Beschaffungsplan für den gesamten Bedarf auf untergeordneter Ebene (Materialbedarfsplan).  

### <a name="to-create-the-sales-order"></a>Den Verkaufsauftrag erstellen  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie auf der Seite **Verkaufsauftrag** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Verk. an Debitorname|Warenausg.-Datum|Artikelnr.|Lagerort|Menge|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Möbel-Meller|05.02.2014|1001|OST|5|  

4.  Akzeptieren Sie die Verfügbarkeitswarnung und klicken Sie auf **Ja**, um die neue Bedarfsmenge zu erfassen.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>So erstellen Sie eine Neuplanung, um den Bedarf am Standort OST zu erfüllen  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Planungsarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die **Neuplanung berechnen** Aktion aus.  
3.  Auf der Seite **Arbeitsplan - Plan berechnen** füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Planung berechnen|Startdatum|Enddatum|Ergebnisse anzeigen:|Summenberechnung einschränken auf|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Nein|01-23-2021<br /><br /> (Arbeitsdatum)|02-07-2021|1001..1300|Lagerortfilter = OST|  

4.  Klicken Sie auf die Schaltfläche **OK**, um die Planungsausführung zu starten.  

     Es wird eine Planungszeile erstellt, in der vorgeschlagen wird, einen geplanten Fertigungsauftrag für die Produktion der zehn Rennräder, Artikel 1001, zum 05.02.2021 (Warenausgangsdatum des Verkaufsauftrags) zu registrieren.  

     Als Nächstes stellen Sie mithilfe der Funktion **Bedarfsverursacher** sicher, dass sich diese Planungszeile auf den Verkaufsauftrag der Möbel-Meller KG bezieht. Diese Funktion verknüpft den Bedarf dynamisch mit der geplanten Beschaffung.  

5.  Wählen Sie die neue Planungszeile aus und klicken Sie dann auf **Bedarfsverursacher**.  
6.  Auf der Seite **Verkaufsnachverfolgung** wählen Sie die Aktion **Anzeigen** aus.  

     Der Verkaufsauftrag über den Versand von fünf Rennrädern für die Debitorennummer 10000 am 05.02.2021 wird nun angezeigt.  

7.  Schließen Sie die Seite **Verkaufsauftrag** und **Bedarfsverursacher**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Nettobedarf berechnen, um den Bedarf zugrunde liegender Komponenten einzuschließen  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Planungsarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die **Neuplanung berechnen** Aktion aus.  
3.  Auf der Seite **Arbeitsplan - Plan berechnen** füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Berechnen|Startdatum|Enddatum|Ergebnisse anzeigen:|Summenberechnung einschränken auf:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|01-23-2021|02-07-2021|1001..1300|Lagerortfilter = OST|  

4.  Klicken Sie auf die Schaltfläche **OK**, um die Planungsausführung zu starten.  

     Es werden insgesamt 14 Planungszeilen erstellt, in denen Beschaffungsaufträge für den gesamten Bedarf des Rennradauftrags am Standort OST vorgeschlagen werden.  

## <a name="analyzing-the-planning-result"></a>Analysieren des Planungsergebnisses  
 Zum Analysieren der vorgeschlagenen Mengen führt Jürgen ein Drilldown in ausgewählten Planungszeilen aus, um Bedarfsverursacher und Planungsparameter anzuzeigen.  

 Beachten Sie, dass dann auf der Seite **Planungsvorschlag** in der Spalte **Fälligkeitsdatum** die vorgeschlagenen Beschaffungsaufträge rückwärts vom Fälligkeitsdatum des Verkaufsauftrags (05.02.2021) geplant werden. Die Zeitleiste beginnt auf der obersten Planungszeile mit dem Fertigungsauftrag zur Produktion der fertigen Rennräder. Die Zeitleiste endet in der untersten Planungszeile mit der Bestellung für einen der Artikel auf unterster Ebene, 1255 (Laufbuchse hinten), fällig am 30.01.2021. Wie die Planungszeile für den Artikel 1251, wird Achsen-Hinterrad, steht diese Zeile für eine Bestellung für Komponenten, die am Startdatum seines gefertigten übergeordneten Elements, Unterbaugruppenartikel 1250 fällig sind, das wiederum am 02-03-2014 fällig ist. In diesem Vorschlag können Sie sehen, dass alle zugrunde liegenden Artikel im Startdatum ihrer Elemente fällig sind.  

 In der Planungszeile für den Artikel 1300 (Kette komplett) werden zehn Stück vorgeschlagen. Dies weicht von den vorgeschlagenen fünf Stück ab, von denen wir erwarten, dass sie erforderlich sind, um den Verkaufsauftrag zu erfüllen. Fahren Sie fort, um die Bedarfsverursacherposten anzuzeigen.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>So zeigen Sie Bedarfsverursacher für Artikel 1300 an  

1.  Wählen Sie die Planungszeile für den Artikel 1300 aus, und klicken Sie dann auf **Auftragsnachverfolgung**.  

     Die beiden Zeilen auf der Seite **Bedarfsverursacher** zeigen, dass für fünf Stück die Bedarfsverursacher von der Planungszeile (erste Bedarfsverursacherzeile) zum Verkaufsauftrag 1001 (zweite Bedarfsverursacherzeile) zurückverfolgt werden können. Die letzten vorgeschlagenen fünf Stück beziehen sich nicht auf Belegzeilen, sondern auf einen Planungsparameter, Planungsposten oder Rahmenauftragsposten. Solche nicht nachverfolgten Mengen werden im Feld **Menge ohne Bedarfsverursacher** im Kopf der Seite **Bedarfsverursacher** summiert.  

2.  Wählen Sie das Feld **Menge ohne Bedarfsverursacher** aus.  

     Der Seite **Planungselement ohne Bedarfsverursacher** können Sie entnehmen, dass für den Artikel 1300 ein Planungsparameter "Minimale Losgröße" von 10,00 Stück verwendet wird. Daher beträgt die Summe der Planungszeile zehn Stück, von denen nur fünf Stück zu einem Bedarfsverursacher nachverfolgt werden können. Die letzten fünf Stück sind eine Menge ohne Bedarfsverursacher und werden aufgrund des Planungsparameters angezeigt. Fahren Sie fort, die Planungsparameter zu prüfen.  

### <a name="to-check-the-planning-parameter"></a>Den Planungsparameter prüfen  

1.  Wählen Sie auf der Seite **Planungselemente ohne Bedarfsverursacher** die Bedarfsverursacherzeile für Artikel 1300 aus.  
2.  Wählen Sie das Feld **Artikelnr.** und dann **Erweitert** aus.  
3.  Wählen Sie auf der Seite **Artikelkarte** die Aktion **Lagerhaltungseinheit** aus.  
4.  Öffnen Sie auf der Seite **Lagerhaltungsdatenübersicht** die Lagerhaltungsdatenkarte OST.  
5.  Aud dem Inforegister **Planung** achten Sie darauf, dass das Feld **Mindestbestellmenge** zehn enthält.  
6.  Schließen Sie alle Seiten außer der Seite **Planungsvorschlag**.  

### <a name="to-view-more-order-tracking-entries"></a>Weitere Bedarfsverursacher anzeigen  

1.  Wählen Sie die Planungszeile für den Artikel 1110, Rim aus, und klicken Sie dann auf **Auftragsnachverfolgung**.  

     Der Seite **Bedarfsverursacher** können Sie entnehmen, dass fünf Kanten für jeden Fertigungsauftrag für Vorder- und Hinterräder benötigt werden.  

     Der gleiche Bedarfsverursache gilt die Planungszeilen für Artikel 1120, 1160 und 1170. Für Artikel 1120 ist das Feld **Komponentenmenge** der Fertigungsstückliste jedes Radartikels 50 Stück, die eine gesamte Anforderung von 100 hat.  

     Die Planungszeile für den Artikel 1150 für sechs Stück erscheint unregelmäßig. Fahren Sie fort, um zu analysieren.  

2.  Wählen Sie die Planungszeile für den Artikel 1150 und klicken Sie dann auf **Auftragsnachverfolgung**.  

     Der Seite **Bedarfsverursacher** können Sie entnehmen, dass fünf Einheiten zum Vorderrad erzeugt wurden, und eine Einheit ohne Bedarfsverursacher ist. Fahren Sie fort, die Menge ohne Bedarfsverursacher anzuzeigen.  

3.  Wählen Sie das Feld **Menge ohne Bedarfsverursacher** aus.  

     Der Seite **Planungselemente ohne Bedarfsverursacher** können Sie entnehmen, dass der Artikel 1150 einen Planungsparameter, Losgrößenrundungsfaktor von 2,00 verwendet, der angibt, dass der Artikel bestellt wird, er muss in eine Menge sein, die durch 2 teilbar ist. Die fünf am nächsten liegende durch zwei teilbare Zahl ist sechs.  

     Der gleiche Bedarfsverursacher gilt für die Planungszeilen für die vorderen Hubkomponenten, Artikel 1151 und 1155, außer dass jeder Bedarf durch den Prozentsatzes des Ausschusses multipliziert wird, der für Artikel 1150 im Feld **Ausschuss Prozent** auf der Artikelkarte definiert ist.  

 Damit ist die Analyse des anfänglichen Beschaffungsplans abgeschlossen. Beachten Sie, dass das Kontrollkästchen **Aktionsnachricht akzeptieren** in allen Planungszeilen aktiviert ist. Dadurch wird angegeben, dass sie nun in Beschaffungsaufträge übernommen werden können.  

## <a name="carrying-out-action-messages"></a>Durchführen von Ereignismeldungsaktionen  
 Als Nächstes wandelt Jürgen die vorgeschlagenen Planungszeilen mithilfe der Funktion **Ereignismeldung durchführen** in Beschaffungsaufträge um.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>So erstellen Sie automatisch die vorgeschlagenen Beschaffungsaufträge  

1.  Wählen Sie das Kontrollkästchen **Aktionsnalchricht akzeptieren** auf der Planungszeile mit der Warnung Ausnahmetyp.  
2.  Wählen Sie die **Ereignismeldung durchführen** Aktion aus.  
3.  Füllen Sie auf der Seite **Ereignismeld. durchf. - Plan.** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Fertigungsauftrag|Bestellung|Umlagerungsauftrag|  
    |----------------------|--------------------|--------------------|  
    |Fest geplant|Bestellungen erst.|Umlag.-Aufträge erstellen|  

4.  Klicken Sie auf **OK**, um alle vorgeschlagenen Beschaffungsaufträge automatisch zu erstellen.  
5.  Schließen Sie die leere Seite **Planungsvorschlag**.  

 Damit ist die erste Berechnung, Analyse und Erstellung eines Beschaffungsplans für den Bedarf am Standort OST in der ersten Februarwoche abgeschlossen. Im folgenden Abschnitt bestellt ein weiterer Debitor zehn Rennräder und Jürgen muss neu planen.  

## <a name="creating-a-net-change-plan"></a>Erstellen eines Änderungsplans  
 Am nächsten Tag (noch bevor Beschaffungsaufträge gestartet oder gebucht wurden) geht ein neuer Verkaufsauftrag von Libros S.A. für zehn Rennräder mit Liefertermin am 12.02.2021 ein. Jürgen wird über den neuen Bedarf benachrichtigt und beginnt mit der Neuplanung, um den aktuellen Beschaffungsplan anzupassen. Jürgen verwendet die Funktion "Änderungsplanung", um nur die Änderungen zu berechnen, die seit dem letzten Planungslauf am Bedarf oder Bestand vorgenommen wurden. Zudem verlängert er den Planungszeitraum bis zum 14.02.2021, um das zweite Bedarfsdatum (12.02.2014) einzuschließen.  

 Das Planungssystem berechnet, wie der Bedarf für diese beiden identischen Produkte am besten gedeckt werden kann. Zu diesem Zweck werden einige Bestellungen und Fertigungsaufträge konsolidiert, andere Aufträge neu geplant und bei Bedarf neue Aufträge erstellt.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>So erstellen Sie den neuen Verkaufsbedarf und führen eine entsprechende Neuplanung durch  

1.  Wählen Sie die Aktion **Neu** aus.  
2.  Füllen Sie auf der Seite **Verkaufsauftrag** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Verk. an Debitorname|Warenausg.-Datum|Artikelnr.|Lagerort|Menge|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.a.|02-12-2021|1001|OST|10|  

3.  Akzeptieren Sie die Verfügbarkeitswarnung und klicken Sie auf **Ja**, um die Bedarfsmenge zu erfassen.  
4.  Als Nächstes führen Sie die Neuplanung durch, um den aktuellen Beschaffungsplan anzupassen.  
5.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Planungsarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
6.  Wählen Sie die **Nettoveränderung berechnen** Aktion aus.  
7.  Auf der Seite **Arbeitsplan - Plan berechnen** füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Planung berechnen|Startdatum|Enddatum|Ergebnisse anzeigen:|Summenberechnung einschränken auf|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|01-23-2021|02-14-2021|1001..1300|Lagerortfilter = OST|  

8.  Klicken Sie auf die Schaltfläche **OK**, um die Planungsausführung zu starten.  

 Insgesamt werden 14 Planungszeilen erstellt. Beachten Sie, dass auf der ersten Planungszeile das Feld **Aktionsnachricht** **Neu** enthält, das Feld **Menge** 10 anzeigt, und das Feld **Fälligkeitsdatum** 12.02.2021 enthält. Diese neue Zeile für den obersten übergeordneten Artikel, 1001, Rennrad, wird erstellt, weil der Artikel ein Wiederbeschaffungsverfahren aus **Auftrag** verwendet, d.h., dass er in einer Eins-zu-Eins-Beziehung zu dem Bedarf geliefert werden muss, dem Verkaufsauftrag von zehn Stück.  

 Die nächsten beiden Planungszeilen enthalten die Fertigungsaufträge für die Rennradräder. Jede bestehende Menge von 5 im Feld **Originalmenge** wird mit 15 erhöht im Feld **Menge**. Beide Fertigungsaufträge haben unverändert Fälligkeitsdaten, wie im **Aktionsnachricht**-Feld, das **Menge ändern** enthält. Dies ist auch der Fall für die Planungszeile für Artikel 1300, außer seinem Losgrößenrundungsfaktor mit 10,00 Rundungen, der Nachfrageverfolgung von 15 Stück bis zu 20 Stück.  

 Alle anderen Planungszeilen enthalten die Ereignismeldung **Neu berechnen & Menge ändern**. Das bedeutet, dass neben der Erhöhung der Menge die Fälligkeitsdaten in Bezug auf den Beschaffungsplan verschoben werden, damit die zusätzliche Menge in der verfügbaren Fertigungszeit (Kapazität) berücksichtigt wird. Eingekaufte Komponenten werden neu geplant und erhöht, um die Fertigungsaufträge zu erzeugen. Fahren Sie fort, um den neuen Plan zu analysieren.  

## <a name="analyzing-the-changed-planning-result"></a>Analysieren des geänderten Planungsergebnisses  
 Da alle Charge-für-Charge-geplanten Artikel innerhalb des Filters, 1100 und 1300, eine Neuplanungsperiode von zwei Wochen haben, werden ihre Beschaffungsaufträge alle geändert, um dem neuen Bedarf zu entsprechen, der innerhalb der angegebenen zwei Wochen auftritt.  

 Einige Planungszeilen werden einfach mit drei multipliziert, um 15 Rennräder anstelle 5 bereitzustellen, und die Fälligkeitsdaten sind rückdatiert, um die erhöhten Mengen bis zum Lieferdatum des Verkaufsauftrags für Möbel-Meller KG bereitzustellen. Für diese Planungszeilen können alle Mengen zurückverfolgt werden. Die verbleibenden Planungszeilen werden durch zehn Stück, sowie durch das Verschieben ihrer Fälligkeitsdaten erhöht. Für diese Planungszeilen sind ein Teil der Mengen, aufgrund von verschiedenen Planungsparametern, ohne Bedarfsverursacher. Fahren Sie fort, um einige dieser Bedarfsverursacherposten anzuzeigen.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>So zeigen Sie Bedarfsverursacher für Artikel 1250 an  

1.  Wählen Sie die Planungszeile für den Artikel 1250 aus, und klicken Sie dann auf **Auftragsnachverfolgung**.  

     Die sieben Zeilen auf der Seite **Bedarfsverursacher** zeigen, dass fünf und zehn Stück durch das Hinterrad zu den Tourenrädern in den beiden Verkaufsaufträgen zurückverfolgt werden können.  

     Die letzten fünf Stück sind ohne Bedarfsverursacher. Fahren Sie fort, um zu analysieren.  

2.  Wählen Sie das Feld **Menge ohne Bedarfsverursacher** aus.  

     Der Seite **Planungselement ohne Bedarfsverursacher** können Sie entnehmen, dass für den Artikel 1250 ein Planungsparameter "Minimale Losgröße" von 10,00 Stück verwendet wird. Daher wurde die Planungszeile für 20 Stück, insgesamt um den tatsächlichen Bedarf auf die nächste Zahl gerundet, die durch 10 teilbar ist. Die letzten fünf Stück sind eine Menge ohne Bedarfsverursacher und werden aufgrund des Planungsparameters angezeigt.  

3.  Schließen Sie alle Seiten außer der Seite **Planungsvorschlag**.  

### <a name="to-view-an-existing-order"></a>Bestehenden Auftrag anzeigen  

1.  Klicken Sie in der Planungszeile für den Artikel 1250 auf das Feld **Ref.Auftragsnr.** Feld  
2.  Öffnen Sie die Seite **Fest geplanter Auftrag** für Nabe hinten. Der bestehende Auftrag über zehn Stück wird geöffnet, den Sie in der ersten Planung erstellt haben.  
3.  Schließen Sie die fest geplanten Fertigungsaufträge.  

 Damit ist die exemplarische Vorgehensweise zur Verwendung des Planungssystems zum automatischen Erkennen von Bedarf, Berechnen der entsprechenden Beschaffungsaufträge für den Bedarf und die Planungsparameter und anschließenden automatischen Erstellen unterschiedlicher Beschaffungsauftragsarten mit den jeweiligen Daten und Mengen abgeschlossen.  

## <a name="see-also"></a>Siehe auch  
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)   
 [Exemplarische Vorgehensweise: Manuelle Beschaffungsplanung](walkthrough-planning-supplies-manually.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]