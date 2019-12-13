---
title: 'Exemplarische Vorgehensweise: Manuelle Beschaffungsplanung | Microsoft Docs'
description: In der folgenden exemplarischen Vorgehensweise wird die Planung von Beschaffungsaufträgen zum Erfüllen eines neuen Bedarfs beschrieben. Je nach Bedarfsart können Sie die Beschaffungsplanung in festen Intervallen, z. B. jeden Morgen oder jeden Montag, oder bei einer entsprechenden Benachrichtigung durch den Verkauf oder die Produktion initiieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0da12af6eb5a165c717cd112735a91aebe3ae85d
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876967"
---
# <a name="walkthrough-planning-supplies-manually"></a>Exemplarische Vorgehensweise: Manuelle Beschaffungsplanung

**Hinweis**: In dieser exemplarischen Vorgehensweise muss in einem Demomandanten mit der Option **Volle Auswertung - vollständige Beispieldaten** ausgeführt werden, die in der Sandboxumgebung verfügbar ist. Weitere Informationen finden Sie unter [Erstellen einer Sandbox-Umgebung](across-how-create-sandbox-environment.md).

In der folgenden exemplarischen Vorgehensweise wird die Planung von Beschaffungsaufträgen zum Erfüllen eines neuen Bedarfs beschrieben. Je nach Bedarfsart können Sie die Beschaffungsplanung in festen Intervallen, z. B. jeden Morgen oder jeden Montag, oder bei einer entsprechenden Benachrichtigung durch den Verkauf oder die Produktion initiieren. In dieser exemplarischen Vorgehensweise verwenden Sie die Seite **Auftragsplanung**, ein einfaches Tool für die Beschaffungsplanung, bei dem Entscheidungen manuell getroffen werden, anstatt die Planung automatisch anhand von Parametern durchzuführen.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
 In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Planen einer Bestellung für Produktionskomponenten  
-   Planen eines Umlagerungsauftrags zum Erfüllen des Verkaufsbedarfs  
-   Planen eines Fertigungsauftrags für einen Artikel mit mehreren Ebenen  

## <a name="roles"></a>Rollen  
 Die Aufgaben in dieser exemplarischen Vorgehensweise werden von den folgenden Benutzern ausgeführt:  

-   Produktionsplaner  
-   Einkäufer  
-   Verkaufsauftragsbearbeiter  

## <a name="prerequisites"></a>Voraussetzungen  
 Bevor Sie diese exemplarische Vorgehensweise beginnen können, müssen Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] einrichten. Die folgenden Änderungen müssen an der Datenbank vorgenommen werden:  

-   Löschen Sie alle vorhandenen Verkaufsaufträge für Tourenräder.  
-   Erstellen Sie einen Verkaufsauftrag für zehn Tourenräder am Standort BLAU.  
-   Löschen Sie alle geplanten und fest geplanten Fertigungsaufträge. Löschen Sie keine gestarteten Aufträge mit bereits gebuchten Posten.  

 Verwenden Sie grundsätzlich die vorgeschlagenen Daten in dieser exemplarischen Vorgehensweise. Diese Daten enthalten die erforderlichen Datensätze.  

## <a name="story"></a>Hintergrund  
 Jürgen, der Produktionsplaner eines kleinen Produktionsunternehmens, ist im Begriff, Fertigungsaufträge und Bestellungen zum Erfüllen eines neuen Verkaufsbedarfs zu planen.  

 Da die Produkte nur wenige Stücklistenebenen besitzen und der Auftragsfluss ebenfalls relativ wenige Stufen umfasst, verwendet Jürgen die Seite **Auftragsplanung** zum manuellen Erstellen von Beschaffungsaufträgen und arbeitet dabei nacheinander die einzelnen Produktebenen ab.  

 In einer komplexeren Produktionsumgebung wird der Planungsvorschlag verwendet, um die Beschaffung basierend auf Artikelparametern wie Neuplanungsperiode, Sicherheitszuschlag für die Beschaffungszeit und Minimalbestand sowie Stapelberechnungen des konsolidierten Bedarfs aller Produktebenen zu planen.  

## <a name="setting-up-the-sample-data"></a>Einrichten der Beispieldaten  
 Das standardmäßige Demounternehmen CRONUS verfügt derzeit über einen umfangreichen, nicht geplanten Bedarf. Während der unterschiedlichen Planungsphasen dieser exemplarischen Vorgehensweise ist eine Abweichung von einer realistischen Vorgehensweise erforderlich, da Bedarf mit unmittelbar bevorstehendem Fälligkeitsdatum ignoriert und stattdessen Bedarf mit einem späteren Fälligkeitsdatum verwendet wird.  

## <a name="using-the-order-planning-page"></a>Verwenden der Seite "Auftragsplanung"  

Die Seite **Auftragsplanung** kann von mehreren Standorten aus aufgerufen werden:  

-   Fertigung, Planung  
-   Vertrieb & Marketing, Auftragsabwicklung  
-   Einkauf, Planung  
-   Darüber hinaus können Sie diese Seite für einen bestimmten Fertigungsauftrag öffnen, indem Sie die Aktion **Planung** wählen.

### <a name="to-use-the-order-planning-page"></a>So verwenden Sie die Seite "Auftragsplanung"  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Auftragsplanung** ein, und wählen Sie dann den zugehörigen Link.  

     Beim erstmaligen Öffnen der Seite **Auftragsplanung** muss eine Planung berechnet werden, um den neuen Bedarf seit der letzten Berechnung anzuzeigen.  

2.  Wählen Sie die **Neuplanung berechnen** Aktion aus.  

     Das Planungssystem analysiert jeden neu erfassten Bedarf, z. B. neue Verkaufsaufträge und geänderte Verkaufs- oder Fertigungsaufträge.  

     Basierend auf der Gesamtverfügbarkeit wird die für jede Bedarfszeile benötigte Menge berechnet. Diese Berechnung erfolgt Auftrag für Auftrag. Folglich wird der Auftrag mit der Bedarfszeile mit dem frühesten Fälligkeitsdatum oder Warenausgangsdatum als Erstes berechnet. Danach werden weitere Bedarfszeilen in demselben Auftrag berechnet, unabhängig vom Fälligkeits- oder Warenausgangsdatum.  

3.  Maximieren Sie der Seite **Auftragsplanung**, und passen Sie die Größe der Spaltenfelder so an, dass alle standardmäßigen Feldnamen angezeigt werden.  

     Nach der Berechnung wird der nicht gedeckte Bedarf in Form von reduzierten Auftragskopfzeilen nach dem frühesten Bedarfsdatum sortiert auf der Seite angezeigt.  

     Für CRONUS liegen mehrere Aufträge mit nicht gedecktem Bedarf vor. Jede fett formatierte Planungszeile steht für einen Auftrag (Verkaufs- oder Fertigungsauftrag) und enthält mindestens eine Auftragszeile mit unzureichender Verfügbarkeit.  

4.  Wählen Sie im Feld **Bedarf anzeigen als** den Filter **Gesamtbedarf** aus.  

     Im Feld **Bedarfsart** können Sie die anzuzeigenden Auftragsarten auswählen.  

     Aufträge ohne Verfügbarkeitsprobleme werden nicht angezeigt. Falls bei der Berechnung einer Planung keine Aufträge vorhanden sind, wird eine Meldung eingeblendet, und es werden keine Planungszeilen angezeigt.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Planen einer Bestellung zum Erfüllen des Komponentenbedarfs  
 In diesem Verfahren erstellen Sie eine Bestellung für benötigte Produktionskomponenten.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>So planen Sie eine Bestellung zum Erfüllen des Komponentenbedarfs in der Produktion  

1.  Erweitern Sie die erste Zeile (klicken Sie auf das Pluszeichen +).  
2.  Wählen Sie die erste Bedarfszeile, mit Artikel **LSU-15**, und wählen Sie die **Beleg anzeigen** Aktion aus.  
3.  Schließen Sie den offenen Fertigungsauftrag, um zur Seite **Auftragsplanung** zurückzukehren.  
4.  Wählen Sie im Feld **Beschaffungsmethode** die Option **Einkauf** aus.  

     Der Standardwert ist die Artikelkarte (oder Lagerhaltungsdatenkarte), Sie können diesen Wert jedoch in eine der folgenden Optionen ändern:  

    -   **Einkauf** – Dient zum Erstellen einer Bestellung.  
    -   **Umlagerung** – Dient zum Erstellen eines Umlagerungsauftrags.  
    -   **Fert.-Auftrag** – Dient zum Erstellen eines Fertigungsauftrags.  

5.  Im Feld **Liefern von** müssen Sie entsprechend der ausgewählten Beschaffungsmethode eine der folgenden Optionen auswählen.  

    -   **Kreditor** – Für Einkäufe  
    -   **Lagerort** - für Umlagerungen  

     Wenn dieses Feld nicht ausgefüllt wird, wird beim Erstellen der Beschaffungsaufträge eine Fehlermeldung angezeigt.  

    > [!NOTE]  
    >  Falls auf den Artikelkarten eine Standardkreditorennummer für die Komponenten eingerichtet ist, sind in den Zeilen Werte voreingestellt.  

6.  Wählen Sie das Feld **Liefern von**  aus.  
7.  Klicken Sie auf der Seite **Artikel/Kreditoren-Katalog** auf **Neu**, und wählen Sie dann den Kreditoren **30000** aus.  
8.  Wählenen Sie die Schaltfläche **OK**, um zur Seite **Auftragsplanung** zurückzukehren.  
9. Kopieren Sie den Kreditor **30000** in die anderen Zeilen für Lautsprecherkomponenten für diesen Fertigungsauftrag.  

     Sie können jetzt eine Bestellung erstellen.  

10. Wählen Sie die **Auftrag erstellen** Aktion aus. Die Seite **Beschaffungsaufträge erstellen** wird geöffnet.  
11. Wählen Sie im Feld **Aufträge erstellen für** auf dem Inforegister **Auftragsplanung** die Option **Aktive Bestellung** aus.  
12. Wählen Sie auf dem Inforegister **Optionen** im Feld **Bestellung erstellen** die Option **Bestellungen erst.** aus.  
13. Klicken Sie auf **OK**, um Bestellungen für alle Komponenten des Auftrags zu erstellen.  

     Die Bestellungen werden erstellt und als die letzten Aufträge in der Liste der Bestellungen gespeichert.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Planen eines Umlagerungsauftrags zum Erfüllen des Verkaufsbedarfs  
 In diesem Verfahren erstellen Sie eine Planung für den Bedarf aus einem Verkaufsauftrag. Anders als beim Fertigungsbedarf, bei dem Bedarfszeilen Komponentenzeilen sind, stellen Bedarfszeilen hier Verkaufszeilen dar.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>So planen Sie einen Umlagerungsauftrag zum Erfüllen des Verkaufsbedarfs  

1.  Bewegen Sie den Mauszeiger in die Planungszeile für den Auftrag **2008**.  
2.  Erweitern Sie die Zeile, und bewegen Sie den Mauszeiger in die Bedarfszeile.  

     Die Verkaufsauftragsnummer **2008** ist ein Auftrag über zehn Lautsprecher vom Typ **LS-120**, bestellt von der Gilde Jupiter Versicherungs AG.  

     Die für den Artikel definierte Beschaffungsmethode sowie der Standardkreditor werden angezeigt.  

    > [!NOTE]  
    >  Im unteren Bereich der Seite befinden sich vier Informationsfelder. Dem Feld **Frühestes Verfügbarkeitsdatum** können Sie entnehmen, dass die benötigten zehn Stück neun Tage nach dem aktuellen Fälligkeitsdatum verfügbar sein werden (in einem eingehenden Beschaffungsauftrag). Falls dies für den Debitoren zu spät ist, können Sie im Feld **Verfügbar für Umlagerung** sehen, dass 13 Stück des Artikels an einem anderen Lagerort verfügbar sind. Sie verwenden diesen Bestand für die Planung.  

3.  Wählen Sie das Feld **Verfügbar für Umlagerung** aus, um die Seite **Alternativvorrat holen** zu öffnen.  
4.  Klicken Sie auf **OK**, um die zehn verfügbaren Artikel zu buchen.  

    > [!NOTE]  
    >  In der Bedarfszeile wurde der vorgeschlagene Einkauf gegen eine Umlagerung vom Standort GRÜN ausgetauscht. Mit der Funktion **Aufträge erstellen** wird somit ein Umlagerungsauftrag von GRÜN zum angeforderten Standort erstellt. Das Feld **Ersatzartikel vorhanden** funktioniert auf die gleiche Weise.  

5.  Wählen Sie die **Auftrag erstellen** Aktion aus. Die Seite **Beschaffungsaufträge erstellen** wird geöffnet.  
6.  Wählen Sie im Feld **Aufträge erstellen für** auf dem Inforegister **Auftragsplanung** die Option **Aktive Bestellung** aus.  
7.  Wählen Sie auf dem Inforegister **Optionen** im Feld **Umlagerungsauftrag erstellen** die Option **Umlag.-Aufträge erstellen** aus.  
8.  Klicken Sie auf **OK**, um den Umlagerungsauftrag für den Bedarf des Verkaufsauftrags zu erstellen.  

     Der Umlagerungsauftrag wird erstellt und als der letzte Auftrag in der Liste offener Umlagerungsaufträge gespeichert.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Planen eines Fertigungsauftrags mit mehreren Ebenen zum Erfüllen des Verkaufsbedarfs  
 In diesem Verfahren erstellen Sie eine Planung, um den Verkaufsbedarf für einen gefertigten Artikel mit mehreren Produktebenen zu erfüllen. Die Produktebenen des Artikels verursachen voneinander abhängigen Fertigungsbedarf.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>So planen Sie einen Fertigungsauftrag mit mehreren Ebenen zum Erfüllen des Verkaufsbedarfs  

1.  Wählen Sie die Planungszeile mit dem Verkaufsbedarf für Auftrag **1001** aus (wurde bei der Vorbereitung der Daten erstellt).  

     Dieser Bedarf ist eine Verkaufszeile, für den Artikel ist jedoch die Beschaffungsmethode **Fertigungsauftrag** festgelegt. Fügen Sie dem Komponentenbedarf für jedes Tourenrad eine zusätzliche Klingel hinzu.  

2.  Wählen Sie auf der Seite **Planungskomponenten** die Aktion **Komponenten** aus.  
3.  Ändern Sie in der Zeile für "Klingel" den Wert im Feld **Komponentenmenge** von **1** in **2**.  
4.  Überprüfen Sie auf der Seite **Auftragsplanung** die Planungsalternativen. In diesem Fall sind keine alternativen Beschaffungsmöglichkeiten verfügbar, d. h. weder Umlagerung noch Ersatzartikel oder spätere Lieferung. Sie müssen den vorgeschlagenen Beschaffungsauftrag, einen Fertigungsauftrag, erstellen.  
5.  Wählen Sie die Schaltfläche **Auftrag ausführen**, um den Fertigungsauftrag zu erstellen.  

     Auf der Seite **Auftragsplanung** können Sie sehen, dass die Planungszeile für den Verkaufsauftrag **1001** nicht mehr vorhanden ist und der ursprüngliche Verkaufsbedarf gedeckt wurde.  

6.  Schließen Sie die Seite **Auftragsplanung**.  

     Es wäre jetzt möglich, alle Planungsaufgaben in dieser Ansicht abzuschließen. Stattdessen übernehmen Sie nun die Rolle des Produktionsplaners, indem Sie zum soeben erstellten Fertigungsauftrag navigieren und die Seite **Auftragsplanung** öffnen.  

 Als Produktionsplaner müssen Sie jetzt einen spezifischen Fertigungsauftrag planen.  

### <a name="to-plan-a-specific-production-order"></a>So planen Sie einen spezifischen Fertigungsauftrag  

1.  Öffnen Sie den Fertigungsauftrag **101001** (für zehn Tourenräder), den Sie zuvor mit der Funktion **Aufträge erstellen** erstellt haben.  
2.  Öffnen Sie die Seite **FA-Komponenten**, um zu überprüfen, ob die zusätzliche Klingel über dem Fertigungsauftrag wiedergegeben wird.  
3.  Wählen Sie die Aktion **Planung** aus.  

     Die Seite **Auftragsplanung** wird geöffnet in einer Darstellungsform, die immer für den spezifischen Fertigungsauftrag gefiltert wird. Der Verkaufsbedarf wird nicht angezeigt. Sie müssen eine Planung berechnen, damit zusätzlicher Bedarf angezeigt wird.  

4.  Wählen Sie die **Neuplanung berechnen** Aktion aus.  

     Vier neue Fertigungsaufträge werden als vom Auftrag **101001** abgeleiteter nicht geplanter Fertigungsbedarf angezeigt. Die neuen Zeilen stellen den neuen Fertigungsbedarf für die benötigten Unterbaugruppen für den Auftrag dar.  

5.  Wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Alle aufklappen**, um sich einen Überblick über den gesamten Fertigungsbedarf für die Fertigungsaufträge zu verschaffen.  

     Um zusätzliche Informationen zu den Bedarfszeilen zu erhalten, sollten Sie die Felder **Bedarfsmenge** und **Verfügb. Bedarfsmenge** zur Ansicht hinzuzufügen.  

     Sie müssen jetzt zehn Stück von jeder Komponente beschaffen.  

     Beachten Sie, dass für vier der Bedarfszeilen ist die Beschaffungsmethode "Fertigungsauftrag" festgelegt ist. Diese vier Unterbaugruppen stellen die zweite Produktebene des Tourenrads dar.  

     Die standardmäßigen Beschaffungseinstellungen sind bereits angegeben, und Sie können mit dem Erstellen der Aufträge fortfahren.  

6.  Wählen Sie die **Auftrag erstellen** Aktion aus.  

     Lesen Sie den Text auf dem Inforegister **Auftragsplanung**, bevor Sie auf **OK** klicken. Dieser Text ist wichtig, da Sie wissen, dass die Produktstruktur des Tourenrads einige gefertigte Komponenten (Unterbaugruppen) enthält, für die zum Zeitpunkt der Auftragserstellung möglicherweise ein Bedarf vorliegt.  

7.  Wählen Sie auf der Seite **Beschaffungsaufträge erstellen** im Feld **Aufträge erstellen für** die Option **Alle Zeilen** aus, und wählen Sie dann die Schaltfläche **OK**, um Fertigungsaufträge für die zweite Produktebene des Auftrags zu erstellen.  

     Beachten Sie, dass der Fertigungsbedarf auf oberster Ebene für den Fertigungsauftrag 101001 nicht mehr vorhanden ist. Dies bedeutet, dass der ursprüngliche Fertigungsbedarf für Unterbraugruppen geplant wurde.  

     Auf der Seite **Auftragsplanung** berechnen Sie erneut eine Planung, um die Tourenradstruktur zu planen.  

8.  Wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Planung berechnen** aus, um die Planung entsprechend den Anweisungen im eingebetteten Hilfetext neu zu berechnen.  

     Die zwei neuen Zeilen stellen zusätzlichen Fertigungsbedarf dar, der von den in den vorhergehenden Schritten geplanten Unterbaugruppen abgeleitet wurde. Erstellen Sie zwei Fertigungsaufträge für die Beschaffung der Radnaben – einen für zehn Vorderrad- und einen für zehn Hinterradnaben.  

9. Wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Alle aufklappen**, um sich einen Überblick über die zwei Fertigungsaufträge zu verschaffen.  

     Die vorgeschlagene Beschaffungsplanung sieht vor, insgesamt vier Bestellungen für die Komponenten zu erstellen. Sie entscheiden sich, die vorgeschlagenen Aufträge zu erstellen.  

10. Wählen Sie die **Auftrag erstellen** Aktion aus.  
11. Wählen Sie im Feld **Aufträge erstellen für** die Option **Alle Zeilen** aus, und klicken Sie anschließend auf die Schaltfläche **OK**. Überprüfen Sie, ob zusätzlicher Bedarf für die Fertigung des übergeordneten Artikels besteht (das im Verkaufsauftrag 1001 verkaufte Tourenrad).  
12. Wählen Sie die **Neuplanung berechnen** Aktion aus.  

     Die Meldung zeigt an, dass alle erforderlichen Artikel geliefert werden. Prüfen Sie die fest geplanten Fertigungsaufträge, die erstellt wurden.  

13. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Feste geplante Fertigungsaufträge** ein, und wählen Sie dann den zugehörigen Link.  

     Überprüfen Sie auf der Seite **Fest geplante FA** , wie die Start- und Endzeiten der einzelnen Aufträge entsprechend der Produktstruktur geplant wurden. Die Komponenten auf der niedrigsten Ebene werden zuerst gefertigt. Daher ist es unumgänglich, die Planung von Aufträgen mit mehreren Ebenen wie in diesem Planungsworkflow gezeigt vorzunehmen.  

## <a name="see-also"></a>Siehe auch  
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)   
 [Exemplarische Vorgehensweise: Automatische Beschaffungsplanung](walkthrough-planning-supplies-automatically.md)
