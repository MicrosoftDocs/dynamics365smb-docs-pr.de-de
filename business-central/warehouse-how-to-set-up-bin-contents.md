---
title: Lagerplatzinhalt erstellen
description: 'Nachdem Sie Ihre Lagerplätze eingerichtet haben, können Sie die Artikel angeben, die Sie darin speichern möchten, und Regeln einrichten, die steuern, wie oft Lagerplätze nachgefüllt werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="create-bin-contents"></a>Lagerplatzinhalt erstellen

Nachdem Sie Ihre Lagerplätze eingerichtet haben, können Sie die Lagerplatzinhalte einrichten. Mit anderen Worten: Sie können die Artikel einrichten, die Sie in jedem beliebigen Lagerplatz lagern möchten, und Sie können die Regeln festlegen, die befolgt werden sollen, wenn sie den Lagerplatz mit einem bestimmten Artikel füllt. Sie können dies auf der Seite **Lagerplatzinhalt** oder automatisch mit der Seite **Erstellen Sie Lagerplatzinhalt-Arbeitsblatt erstellen** manuell tun.

## <a name="to-create-bin-content-manually"></a>So erstellen Sie Lagerplatzinhalt manuell

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Lagerort aus, an dem Sie Lagerplatzinhalte einrichten möchten, und wählen Sie dann die Aktion **Lagerplätze** aus.  
3. Wählen Sie den Lagerplatz aus, an dem Sie Lagerplatzinhalte einrichten möchten, und wählen Sie dann die Aktion **Inhalte** aus.  
4. Füllen Sie für jeden Artikel, den Sie in dem Lagerplatz lagern möchten, eine Zeile auf der Seite **Lagerplatzinhalt** mit den relevanten Informationen aus. Einige der Felder sind bereits mit Informationen über den Lagerplatz ausgefüllt.  
5. Füllen Sie als Erstes das Feld **Artikelnr.** aus und dann, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, die anderen Felder, wie z. B. **Einheitencode**, **Max. Menge** und **Min. Menge** aus.  

Wählen Sie bei Bedarf das Feld **Fix** aus. Wenn der Lagerplatz als Standardlagerplatz für den Artikel verwendet werden soll, wählen das Feld **Standardlagerplatz**.  

Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden und die richtigen Dimensionsinformationen auf der Artikelkarte zu den Einheiten jedes Artikels eingegeben haben, wird die Höchstmenge, die Sie auf der Seite **Lagerplatzinhalt** eingeben, gegen die physische Kapazität des Lagerplatzes geprüft. Dann werden die minimale und maximale Menge verwendet, wenn die Lagerplatzauffüllung berechnet und Einlagerungen vorgeschlagen werden.  

Wenn Sie das Feld **Fest** wählen, legen Sie diesen Lagerplatz für diesen Artikel fest. Das bedeutet, dass [!INCLUDE[prod_short](includes/prod_short.md)] versuchen wird, diesen Artikel in den Lagerplatz einzulagern, wenn dort Platz ist. Sie wird an dieser Festlegung sogar dann festhalten, wenn die Menge im Lagerplatz 0 ist. Andere Artikel können in den Lagerplatz eingelagert werden, obwohl ein bestimmter Artikel als Standard für den Lagerplatz festgelegt wurde. Andere Artikel können in den Lagerplatz eingelagert werden, obwohl ein bestimmter Artikel dem Lagerplatz fest zugewiesen wurde.  

> [!NOTE]  
> Auf der Seite **Lagerplatzinh. Erst.-Arbeitsblatt** können Sie mehrere Lagerplatzinhalte gleichzeitig einrichten.  

## <a name="to-create-bin-content-with-a-worksheet"></a>So erstellen Sie Lagerplatzinhalt in einem Arbeitsblatt

Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie den Lagerplatzinhalt, den Sie in jedem Lagerplatz haben möchten, im Lagerplatzinhalt Erstellungsarbeitsblatt generieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerplatzinhalt Erst.-Arbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Klicken Sie im Kopf des Arbeitsblatts in das Feld **Name** und wählen Sie das Arbeitsblatt des Lagerortes, für den Sie Lagerplatzinhalte erstellen möchten.  
3. Wählen Sie im Feld **Lagerplatzcode** den Code des Lagerplatzes, für den Sie den Lagerplatzinhalt definieren möchten.  

    Wenn Sie in diesem Lagerort die gesteuerte Einlagerung und Kommissionierung verwenden, werden automatisch die Felder ausgefüllt, die mit diesem speziellen Lagerplatz verknüpft sind, wie z. B. **Lagerplatzartencode**, **Lagerklassencode** und **Lagerplatzpriorität**. Dies sind Informationen, die Sie berücksichtigen müssen, wenn Sie den Lagerplatzinhalt definieren.  
4. Wählen Sie den Artikel, den Sie dem Lagerplatz zuordnen möchten, und füllen Sie die Felder aus, die sich auf den Lagerplatzinhalt beziehen. Wenn Sie die gesteuerte Einlagerung und Kommissionierung nutzen und die Funktion **Lagerplatz-Auffüllung berechnen** verwenden möchten, füllen Sie die Felder **Max. Menge** und **Min. Menge** aus.  

    Wenn Sie diesen Lagerplatz für den Artikel als bevorzugten Lagerplatz einrichten möchten, auch wenn die Menge am Lagerplatz **0** ist und alle anderen Einlagerungskriterien gleich sind, aktivieren Sie das Feld **Fix**.  
5. Wiederholen Sie die Schritte 3 bis 4 für jeden Artikel, den Sie einem Lagerplatz zuordnen möchten.  
6. Wählen Sie auf Aktion **Drucken** aus, um sich eine Seitenansicht der Lagerplatzinhalte anzusehen, die Sie im Arbeitsblatt eingegeben haben, oder um diese zu drucken. Überprüfen Sie den Lagerplatzinhalt so lange, bis Sie mit dem Ergebnis zufrieden sind.  
7. Wenn Sie bereit sind, wählen Sie die **Lagerplatzinhalt erstellen** Aktion aus.  

In diesem Arbeitsblatt können Sie mit einer Anzahl Lagerplatzinhaltszeilen für mehrere Lagerplätze arbeiten und dadurch einen guten Überblick darüber erhalten, was Sie in die verschiedenen Lagerplätze in einer vorgegebenen Zone, einem Gang oder Regal einlagern.  

## <a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
