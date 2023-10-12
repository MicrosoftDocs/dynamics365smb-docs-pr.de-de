---
title: Lagerplätze erstellen
description: 'Erzeugen Sie Gruppen ähnlicher Lagerplätze im Lagerplatz-Erstellungs-Arbeitsblatt, erstellen Sie Lagerplätze einzeln auf der Standortkarte oder automatisch im Lagerplatz-Erstellungs-Arbeitsblatt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: bholtorf
---
# Lagerplätze erstellen

Die effektivste Art, die Lagerplätze Ihres Lagers zu erzeugen, ist, Gruppen von ähnlichen Lagerplätzen im Lagerplatz Erstellungsarbeitsblatt zu erstellen, Sie können Ihre Lagerplätze jedoch auch individuell aus der erzeugen Lagerortkarte erzeugen. Sie können eine Funktion auf der Seite **Lagerplatz Erst.-Arbeitsblatt** verwenden, um die Lagerplätze automatisch zu erstellen.  

## So erstellen einen Lagerplatz von der Lagerortkarte aus:

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie den zugehörigen Link.  
2.  Wählen Sie den Lagerort aus, aus dem Sie einen Lagerplatz erstellen möchten, und wählen Sie die Aktion **Lagerplätze** aus.  
3. Wählen Sie die Aktion **Neu**.
4. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Das dedizierte Feld

Das Feld **Dediziert** auf der Seite **Lagerplätze** gibt an, dass Mengen im Lagerplatz vor der Kommissionierung für andere Bedarfsanforderungen geschützt sind. Mengen in dedizierten Lagerplätzen können weiterhin reserviert werden. Entsprechend sind die Mengen in dedizierten Lagerplätzen im Feld **Total verfügbare Menge** auf der Seite **Reservierung** enthalten.

Das Einrichten eines Fert.-Bereitst.-Lagerplatzes/Fert.-Ausgangslagerplatzes stellt ähnliche Funktionen für die Verwendung von Lagerplatzarten zur Verfügung, die nur in erweiterten Lagerfunktionen verfügbar sind. Weitere Informationen finden Sie unter [Einrichten von Lagerplatzarten](warehouse-how-to-set-up-bin-types.md).

### Beispiel

Eine Arbeitsplatzgruppe mit einem Lagerplatzcode wird im Feld **Fert.-Bereitst.-Lagerplatzcode** eingerichtet. Komponentenzeilen in Fertigungsaufträgen mit diesem Lagerplatzcode erfordern, dass mit der Methode "Vorwärts" geleerte Komponenten dort platziert werden. Jedoch können, bis die Komponenten von diesem Lagerplatz verbraucht sind, Komponenten von diesem Lagerplatz durch andere Bedarfsanforderungen kommissioniert oder verbraucht werden, weil sie weiterhin als verfügbare Lagerplatzinhalte gelten. Um sicherzustellen, dass der Lagerplatzinhalt nur für den Komponentenbedarf verfügbar ist, der diesen Fert.-Bereitst.-Lagerplatzcode verwendet, müssen Sie das Feld **Dediziert** der Zeile für diesen Lagerplatzcode auf der Seite Lagerplätze auswählen, das Sie über die Lagerortkarte öffnen.

> [!Caution]
> Artikel in den Fert.-Bereitst.-Lagerplätzen/Fert.-Ausgangslagerplätzen werden nicht geschützt, wenn sie als Produktionskomponenten mit der **Lagerkommissionierungsseite** kommissioniert und verbraucht werden. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in der Grund-Lagerkonfiguration](warehouse-how-to-pick-for-production.md).

## So erstellen Sie Lagerplätze individuell im Lagerplatz-Erstellungsarbeitsblatt:

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Arbeitsblatt Lagerplatz Erst.-Arbeitsblatt** ein und wählen Sie den zugehörigen Link.  
2.  Füllen Sie in jeder Zeile die Felder aus, die erforderlich sind, um die Lagerplätze, die Sie erzeugen, zu benennen und zu charakterisieren.  
3.  Wählen Sie die Aktion **Lagerplätze erstellen** aus.  

## Um Lagerplätze automatisch im Lagerplatz Erst.-Arbeitsblatt zu erstellen:

Bevor Sie beginnen, Lagerplätze automatisch zu erstellen, sollten Sie die Art der Lagerplätze festlegen, die für Ihre Arbeit wichtig sind, sowie den sinnvollsten Warenfluss durch die physische Struktur Ihres Lagers.  

> [!NOTE]  
> Sobald Sie einen Lagerplatz verwenden, können Sie ihn nicht mehr löschen, es sei denn, er ist leer. Wenn Sie jedoch ein anderes System zur Benennung Ihrer Lagerplätze verwenden möchten, können Sie das Umlagerungs Buch.-Blatt verwenden, um Ihre Artikel in ein neues Lagerplatzsystem umzulagern. Dieser Prozess ist jedoch manuell und zeitaufwändig, so dass Sie am besten von Anfang an Ihre Lagerplätze richtig einrichten.  

Um mit der **Lagerplatz Erst.-Arbeitsblatt**-Seite zu arbeiten, müssen Sie als Lagermitarbeiter am Lagerort eingerichtet sein, in dem die Lagerplätze vorhanden sind. Weitere Informationen finden Sie unter [Lagermitarbeiter einrichten](warehouse-how-to-set-up-warehouse-employees.md)    

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerplatz Erst.-Arbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Lagerplätze berechnen** aus.
3. Wählen Sie auf der Seite **Lagerplätze berechnen** im Feld **Lagerplatzvorlagencode** aus, und wählen Sie die Lagerplatzvorlage, die Sie als Muster für die Lagerplätze verwenden möchten, die Sie gerade erstellen.
4.  Geben Sie eine Beschreibung für die Lagerplätze ein, die Sie gerade erstellen.  
5.  Um die Lagerplatzcodes zu erstellen, füllen Sie **Von Nr.** und **Bis Arbeitsgangnr** aus. Felder in den drei auf der Seite angezeigten Kategorien: **Regal**, **Abschnitt** und **Ebene** Der Lagerplatzcode kann bis zu 20 Zeichen umfassen.  

    > [!NOTE]  
    >  Die Anzahl der Zeichen, die Sie in den drei Kategorien für jedes Feld eingegeben haben, z. B. die Zeichen, die Sie in die drei Felder **Von Nr.** eingegeben haben plus die Feldtrennzeichen, wenn vorhanden, müssen 20 oder weniger sein.  

     Sie können im Code Buchstaben als identifizierende Kombination verwenden, der verwendete Buchstabe muss jedoch in den Feldern **Von No.** gleich sein. und **Bis Arbeitsgangnr** aus. Felder. Sie können z. B. den Regal-Teil des Codes als **Von Nr. A01** und **Nach Nr. A10** festlegen. Die Anwendung ist nicht so eingerichtet, dass sie Codes mit Buchstabensequenzen erzeugen kann, z. B. von A01 zu F05.  

6.  Wenn Sie ein Zeichen, z. B. einen Bindestrich, als Trennzeichen für die Kategoriefelder verwenden möchten, die Sie als Teil des Lagerplatzcodes definiert haben, tragen Sie dieses Zeichen in das Feld **Feldbegrenzung** ein.  
7.  Wenn Sie nicht möchten, dass die Anwendung eine Zeile für einen Lagerplatz erzeugt, wenn dieser bereits existiert, wählen das Feld **Auf vorh. Lagerplatz prüfen**.  
8. Wenn Sie mit dem Ausfüllen aller Zeilen fertig sind, wählen Sie die Schaltfläche **OK**.

    Die Anwendung erzeugt eine Zeile für jeden Lagerplatz im Arbeitsblatt. Sie können jetzt einige der Lagerplätze löschen, z. B. wenn Sie ein Regal haben, in dem es in einigen Säulen einen Durchgang durch die ersten beiden Ebenen gibt.  

9. Wenn Sie alle überflüssigen Lagerplätze gelöscht haben, wählen Sie die Aktion **Lagerplätze erstellen** und die Anwendung erstellt dann einen Lagerplatz für jede Zeile im Arbeitsblatt.  

Wiederholen Sie diesen Vorgang für die nächste Serie von Lagerplätzen, bis Sie alle Lagerplätze in Ihrem Lager erstellt haben.  

## Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
