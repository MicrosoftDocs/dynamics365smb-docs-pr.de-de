---
title: 'Vorgehensweise: Wareneingang von Artikeln | Microsoft Docs'
description: "Wenn Artikel bei einem Lager ankommen, das für die Bearbeitung des Wareneingangs eingerichtet wurde, müssen Sie die Zeilen des freigegebenen Herkunftsbelegs abrufen, der ihren Wareneingang ausgelöst hat."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: e56105cbd2410befea964c5445d8227021058d4f
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="receive-items"></a>Empfangen von Artikeln
Wenn Artikel bei einem Lager ankommen, das nicht für die Bearbeitung des Wareneingangs eingerichtet wurde, können Sie den Wareneingang einfach im zugehörigen Geschäftsdokument, wie einer Einkaufsbestellung, einer Verkaufsreklamation oder ein eingehender Umlagerungsauftrag, erfassen.

Wenn Artikel bei einem Lager ankommen, das für die Bearbeitung des Wareneingangs eingerichtet wurde, müssen Sie die Zeilen des freigegebenen Herkunftsbelegs abrufen, der ihren Wareneingang ausgelöst hat. Wenn Sie Lagerplätze nutzen, können Sie entweder den eingetragenen Standardlagerplatz akzeptieren oder, wenn der Artikel nie zuvor in diesem Lager verwendet wurde, tragen Sie den Lagerplatz ein, in den der Artikel eingelagert werden soll. Sie müssen dann die Mengen der Artikel eingeben, die Sie erhalten haben, und den Wareneingang buchen.  

## <a name="to-receive-items-with-a-purchase-order"></a>So empfangen Sie Artikel mit einer Einkaufsbestellung
Nachfolgend wird erläutert, wie Artikel mit einer Bestellung empfangen werden. Die Schritte für Verkaufsreklamationen und Umlagerungsaufträgen sind ähnlich.  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie eine bestehende Bestellung, oder erstellen Sie eine neue. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. Geben Sie in dem Feld **Menge akt. Lieferung** die empfangene Menge an.

    Der Wert im Feld **Bereits gelief. Menge** wird aktualisiert. Wenn dieses eine Teillieferung ist, ist der Wert niedriger als der Wert im Feld **Menge**.
4. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>So empfangen Sie Artikel mit einem Wareneingang
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Wareneingänge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  

    Füllen Sie die Felder auf dem Inforegister **Allgemein** aus. Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen in jede Zeile kopiert.  

    Für Lagerkonfigurationen mit gesteuerte Einlagerung und Kommissionierung: Wenn der Lagerort eine Vorgabezone und einen Vorgabelagerplatz für Wareneingänge hat, werden die Felder **Zonencode** und **Lagerplatzcode** automatisch ausgefüllt, Sie können diese jedoch bei Bedarf ändern.  

    > [!NOTE]  
    >  Wenn Sie Artikel mit Lagerklassen annehmen möchten, die von den Lagerklassen der Lagerplätze im Feld **Lagerplatzcode** des Belegkopfes abweichen, müssen Sie den Inhalt des Feldes **Lagerplatzcode** des Kopfes löschen, bevor Sie die Herkunftsbelegzeilen der Artikel holen können.  
3.  Wählen Sie die **Herkunftsbelege holen** Aktion aus. Die Seite **Herkunftsbelege** wird geöffnet.

    Aus einem neuen oder offenen Wareneingang können Sie die Seite **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die festlegen, welche Artikel erhalten oder geliefert werden sollen.

    1. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
    2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.  
    3. Legen Sie die Art von Herkunftsbelegzeilen fest, die Sie abrufen möchten, indem Sie die jeweiligen Filterfelder ausfüllen.  
    4. Wählen Sie die Aktion **Ausführen** aus.  

    Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden nun auf der Seite **Wareneingang** eingefügt, in dem Sie die Filterfunktion aktiviert haben.  

    Die Filterkombinationen, die Sie definieren, werden auf der Seite **Filter z. Holen v. Herk.-Bel.** gespeichert, bis das nächste Mal benötigt werden. Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

4.  Wählen Sie die Herkunftsbelege, für die Sie Artikel annehmen möchten, und bestätigen Sie dann mit **OK**.  

    Die Zeilen der Herkunftsbelege werden auf der Seite **Wareneingang** angezeigt. Das Feld **Menge akt. Lieferung** ist für jede Zeile gefüllt, Sie können die Menge jedoch bei Bedarf ändern. Wenn Sie den Inhalt des Feldes **Lagerplatzcode** m Inforegister **Allgemein** löschen, bevor Sie die Zeilen abrufen, muss in jeder Wareneingangszeile ein geeigneter Lagerplatzcode eingetragen werden.  

    > [!NOTE]  
    >  Um das Feld **Menge akt. Lieferung** in allen Zeilen mit Null auszufüllen, wählen Sie die Aktion **Menge akt. Lieferung löschen** aus. Um sie wieder mit den Restmengen auszufüllen, aktivieren Sie die Aktion **Menge akt. Lieferung autom. ausfüllen**.  

    > [!NOTE]  
    >  Sie können nicht mehr Artikel annehmen als die Anzahl im Feld **Restmenge** der Herkunftsbelegzeile. Um weitere Artikel anzunehmen, holen Sie einen weiteren Herkunftsbeleg, der eine Zeile für den Artikel enthält, indem Sie die Filterfunktion zum Holen von Herkunftsbelegen mit dem Artikel verwenden.  

5.  Buchen Sie den Wareneingang. Die Mengenfelder in den Herkunftsbelegen werden aktualisiert und die Artikel als Teil des Lagerbestands des Unternehmens gespeichert.  

Wenn Sie Einlagerungen verwenden, werden die Wareneingangszeilen zur Funktion "Wareneingang" gesendet. Die Artikel können, obwohl sie eingegangen sind, nicht kommissioniert werden, bis sie eingelagert wurden. Die eingegangenen Artikel werden nur dann als verfügbar betrachtet, wenn die Einlagerung gebucht wurde.  

Wenn Sie keine Einlagerungen verwenden, jedoch Lagerplätze, wird die Einlagerung der Artikel in dem Lagerplatz gespeichert, der in der Herkunftsbelegzeile angegeben wurde.  

> [!NOTE]  
>  Wenn Sie die Funktion **Buchen und drucken** verwenden, buchen Sie den Wareneingang und drucken eine Einlagerungsanweisung, die Ihnen zeigt, wo die Artikel eingelagert werden sollen.  
>   
>  Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet, wird die Einlagerungsvorlage genutzt, um den besten Platz für die Einlagerung der Artikel zu berechnen. Dieser wird dann auf der Einlagerungsanweisung ausgedruckt.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

