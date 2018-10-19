---
title: "Vorgehensweise: Erstellen von Lagerplätzen | Microsoft Docs"
description: "Die effektivste Art, die Lagerplätze Ihres Lagers zu erzeugen, ist, Gruppen von ähnlichen Lagerplätzen im Lagerplatz Erstellungsvorschlag zu erstellen, Sie können Ihre Lagerplätze jedoch auch individuell erzeugen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7d5b2ce28f1eaebfca26c2db3801b44ff5278e78
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-bins"></a>Lagerplätze erstellen
Die effektivste Art, die Lagerplätze Ihres Lagers zu erzeugen, ist, Gruppen von ähnlichen Lagerplätzen im Lagerplatz Erstellungsvorschlag zu erstellen, Sie können Ihre Lagerplätze jedoch auch individuell aus der erzeugen Lagerortkarte erzeugen. Sie können eine Funktion im Fenster **Lagerplatz Erst.-Vorschlag** verwenden, um die Lagerplätze automatisch zu erstellen.  

## <a name="to-create-a-bin-from-the-location-card"></a>So erstellen einen Lagerplatz von der Lagerortkarte aus:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerorte** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Lagerort aus, aus dem Sie einen Lagerplatz erstellen möchten, und wählen Sie die Aktion **Lagerplätze** aus.  
3. Wählen Sie die Aktion **Neu** aus.
4. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>So erstellen Sie Lagerplätze individuell im Lagerplatz-Erstellungsvorschlag:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzvorschlag** ein, und wählen den zugehörigen Link aus.  
2.  Füllen Sie in jeder Zeile die Felder aus, die erforderlich sind, um die Lagerplätze, die Sie erzeugen, zu benennen und zu charakterisieren.  
3.  Wählen Sie die Aktion **Lagerplätze erstellen** aus.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Um Lagerplätze automatisch im Lagerplatz Erst.-Vorschlag zu erstellen:  
Bevor Sie beginnen, Lagerplätze automatisch zu erstellen, sollten Sie die Art der Lagerplätze festlegen, die für Ihre Arbeit wichtig sind, sowie den sinnvollsten Warenfluss durch die physische Struktur Ihres Lagers.  

> [!NOTE]  
>  Sobald Sie einen Lagerplatz verwenden, können Sie ihn nicht mehr löschen, es sei denn, er ist leer. Wenn Sie jedoch ein anderes System zur Benennung Ihrer Lagerplätze verwenden möchten, können Sie das Umlagerungs Buch.-Blatt verwenden, um Ihre Artikel in ein neues Lagerplatzsystem umzulagern. Dieser Prozess ist jedoch manuell und zeitaufwändig, so dass Sie am besten von Anfang an Ihre Lagerplätze richtig einrichten.  

Um mit dem **Lagerplatz Erst.-Vorschlag**-Fenster zu arbeiten, müssen Sie als Lagermitarbeiter am Lagerort eingerichtet sein, in dem die Lagerplätze vorhanden sind. Weitere Informationen finden Sie unter [Lagermitarbeiter einrichten](warehouse-how-to-set-up-warehouse-employees.md)    

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzvorschlag** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Lagerplätze berechnen** aus.
3. Wählen Sie im Fenster **Lagerplätze berechnen** im Feld **Lagerplatzvorlagencode** aus, und wählen Sie die Lagerplatzvorlage, die Sie als Muster für die Lagerplätze verwenden möchten, die Sie gerade erstellen.
4.  Geben Sie eine Beschreibung für die Lagerplätze ein, die Sie gerade erstellen.  
5.  Um die Lagerplatzcodes zu erstellen, füllen Sie **Von Nr.** und **Bis Arbeitsgangnr** aus. Felder in den drei im Fenster angezeigten Kategorien: **Regal**, **Abschnitt** und **Ebene** Der Lagerplatzcode kann bis zu 20 Zeichen umfassen.  

    > [!NOTE]  
    >  Die Anzahl der Zeichen, die Sie in den drei Kategorien für jedes Feld eingegeben haben, z. B. die Zeichen, die Sie in die drei Felder **Von Nr.** eingegeben haben plus die Feldtrennzeichen, wenn vorhanden, müssen 20 oder weniger sein.  

     Sie können im Code Buchstaben als identifizierende Kombination verwenden, der verwendete Buchstabe muss jedoch in den Feldern **Von No.** gleich sein. und **Bis Arbeitsgangnr** aus. Felder. Sie können z. B. den Regal-Teil des Codes als **Von Nr. A01** und **Nach Nr. A10** festlegen. Die Anwendung ist nicht so eingerichtet, dass sie Codes mit Buchstabensequenzen erzeugen kann, z. B. von A01 bis F05.  

6.  Wenn Sie ein Zeichen, z. B. einen Bindestrich, als Trennzeichen für die Kategoriefelder verwenden möchten, die Sie als Teil des Lagerplatzcodes definiert haben, tragen Sie dieses Zeichen in das Feld **Feldbegrenzung** ein.  
7.  Wenn Sie nicht möchten, dass die Anwendung eine Zeile für einen Lagerplatz erzeugt, wenn dieser bereits existiert, wählen Feld **Auf vorh. Lagerplatz prüfen**.  
8. Wenn Sie mit dem Ausfüllen aller Zeilen fertig sind, wählen Sie die Schaltfläche **OK**.

    Die Anwendung erzeugt eine Zeile für jeden Lagerplatz im Vorschlag. Sie können jetzt einige der Lagerplätze löschen, z. B. wenn Sie ein Regal haben, in dem es in einigen Säulen einen Durchgang durch die ersten beiden Ebenen gibt.  

9. Wenn Sie alle überflüssigen Lagerplätze gelöscht haben, wählen Sie die Aktion **Lagerplätze erstellen** und die Anwendung erstellt einen Lagerplatz für jede Zeile im Vorschlag.  

Wiederholen Sie diesen Vorgang für die nächste Serie von Lagerplätzen, bis Sie alle Lagerplätze in Ihrem Lager erstellt haben.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

