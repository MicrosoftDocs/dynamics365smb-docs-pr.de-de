---
title: Lager umstrukturieren
description: 'Erfahren Sie, wie Sie Ihr Lager mit neuen Lagerplatz-Codes und neuen Lagerplatz-Merkmalen umstrukturieren können, um einen effizienteren Vorgang zu erreichen oder beizubehalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '9813, 9814'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Lager umstrukturieren
Es kann sein, dass Sie Ihr Lager neu strukturieren und dabei neue Lagerplatzcodes und Eigenschaften von Zonen berücksichtigen möchten. Diese Art von Aktivität werden Sie nicht oft ausführen. Es können jedoch Situationen auftreten, in denen eine Neustrukturierung notwendig ist, um effektivere Arbeitsabläufe zu erreichen. Beispiel:  

- Sie möchten zu Lagerplatzcodes übergehen, die die Verwendung der mobilen Datenerfassung unterstützen, z. B. mit tragbaren Geräten.  
- Für das Lager wurde ein neues Regalsystem angeschafft, dass Ihnen neue Möglichkeiten der Lagerung bietet.  
- Das Unternehmen hat sein Artikelsortiment geändert und das Lager an einen neuen Ort verlagert, um sich diesen Veränderungen anzupassen.  

Wenn Ihr Lager so eingerichtet wurde, dass es Lagerplätze verwendet, aber keine gesteuerte Einlagerung und Kommissionierung, strukturieren Sie Ihr Lager neu, indem Sie die neuen Lagerplätze erstellen, die Sie zukünftig verwenden möchten.  

## Um ein Basislager neu zu strukturieren, das nur Lagerplätze verwendet  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2.  Setzen Sie im Inforegister **Logistik** das Feld **Vorg.-Lagerplatzauswahl** auf **Zuletzt verwendeter Lagerplatz**.  
3.  Lagern Sie alle Inhalte Ihrer aktuellen Lagerplätze in die neuen Lagerplätze um, die Sie gerade angelegt haben.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Artikel Umlagungs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link.  
    2.  Wählen Sie eine Buch.-Blattzeile aus, und wählen Sie die **Lagerplatzinhalt holen** Aktion aus.  
    3.  Legen Sie im Inforegister **Lagerplatzinhalt** in den Feldern **Lagerortcode**, **Lagerplatzcode** und **Artikelnr.** Filter fest, um den Inhalt anzugeben, den Sie umlagern möchten.  
    4.  Klicken Sie auf die Schaltfläche **OK**, um eine Buch.-Blattzeile zu füllen.  
    5.  Wählen Sie im Feld **Neuer Lagerplatzcode** den Lagerplatz aus, in den Sie die Artikel umlagern möchten.  
    6.  Wiederholen Sie die Schritte b bis e für alle Lagerplatzinhalte, die Sie umlagern möchten.  
    7.  Wählen Sie die Aktion **Buchen** aus.  

Sie haben jetzt die Lagerplätze geleert, an denen die Artikel bisher gelagert wurden. Die Standardlagerplätze Ihrer Artikel wurden jetzt in die neuen Lagerplätze geändert.  

## Um ein erweitertes Lager, das eine gesteuerte Einlagerung und Kommissionierung verwendet, neu zu strukturieren  

1.  Legen Sie die neuen Lagerplätze an, die Sie in Zukunft verwenden möchten. Weitere Informationen finden Sie unter [Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md).  
2.  Lagern Sie alle Inhalte Ihrer aktuellen Lagerplätze in die neuen Lagerplätze um, die Sie gerade angelegt haben.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Logistik Umlagerungs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
    2.  Für die Lagerplätze, bei denen keine tatsächliche Artikelumlagerung stattfindet, erstellen Sie eine Zeile für jeden der aktuellen Lagerplätze im **Logistik Umlagerungs Buch.-Blatt** mit dem alten Lagerplatzcode (**Von Lagerplatzcode**) und dem neuen Lagerplatzcode (**Nach Lagerplatzcode)**.  
    3.  Wenn einige der Umlagerungen tatsächliche physische Umlagerungen beinhalten, die die Lagermitarbeiter durchführen sollen, verwenden Sie den **Lagerplatzumlagerungsarbeitsblatt**, um die Umlagerungsanweisungen vorzubereiten, anstatt das Umlagerungs Buch.-Blatt zu verwenden. Weitere Informationen finden Sie unter [Umlagern von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Wenn die alten Lagerplätze geleert sind, buchen Sie diese als Lagerplätze vom Typ **QK** um, um sicherzustellen, dass sie nicht in den Artikelströmen enthalten sind.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
    2.  Wählen Sie die Zeile mit dem Lagerort aus und wählen Sie dann Aktion **Lagerplätze** aus.  
    3.  Geben Sie auf der Seite **Lagerplätze** im Feld **Lagerplatzartencode** für jeden der alten Lagerplätze, die Sie in Schritt 3 des vorherigen Verfahrens geleert haben, **QC** ein.  

Sie haben die Lagerplätze jetzt aus dem Warenfluss entfernt und sie als QC-Lagerplätze umgebucht. QC-Lagerplätze haben auf der Seite **Lagerplatzarten** keine ausgewählten Aktivitätenprotokollposten und werden daher durch den Warenfluss nicht berücksichtigt. Weitere Informationen finden Sie unter [Einrichten von Lagerplatzarten](warehouse-how-to-set-up-bin-types.md).  

## So löschen Sie einen Lagerplatz:  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie den Lagerort aus, an dem Sie Lagerplätze löschen möchten. Wählen Sie die **Lagerplätze** Aktion aus.  
3.  Wählen Sie die Zeilen für die zu löschenden Lagerplätze aus.  
4.  Wählen Sie die Aktion **Löschen** aus.  

Wenn Sie **Ja** wählen, wird der Lagerplatz für die zukünftige Verwendung gelöscht, der Lagerplatzcode in allen Lagerplatzposten bleibt jedoch derselbe.  

Wenn Sie einen Lagerplatz umbenennen möchten, so dass alle Datensätze zu diesem Lagerplatz ebenfalls umbenannt werden (die Datensätze umfassen Lagerplatzinhalte, Lageraktivitätszeilen, registrierte Lageraktivitätszeilen, Zeilen in Logistikarbeitsblättern, Wareneingangszeilen, gebuchte Wareneingangszeilen, Warenausgangszeilen, gebuchte Warenausgangszeilen sowie Lagerplatzposten), können Sie dies auf der Seite **Lagerplätze** tun.  

## So benennen Sie einen Lagerplatz um und ändern den Lagerplatzcode in allen Datensätzen:  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie den Lagerort aus, an dem Sie einen Lagerplatz umbenennen oder für den Sie den Lagerplatzcode ändern möchten, und wählen Sie dann die Aktion **Lagerplätze** aus.  
3.  Wählen Sie den Lagerplatz aus, den Sie ändern möchten, und geben Sie im Feld **Code** einen neuen Code für den Lagerort ein.  
4.  Wählen Sie die Schaltfläche **Ja** aus.  

> [!NOTE]  
>  Wenn Sie **Ja** wählen und es viele Datensätze zu diesem Lagerplatz gibt (z. B. weil Sie lange keine Logistikbelege mehr gelöscht haben), kann es einige Zeit dauern, bis die Anwendung alle Datensätze umbenannt hat. Wenn Sie diese Methode anwenden, sollten Sie den Batchauftrag **Registrierte Logistikbelege löschen** auszuführen, bevor Sie den Umbenennungsprozess starten. Beachten Sie darüber hinaus, dass die einzigen Belege, die durch diese Stapelverarbeitung gelöscht werden, Einlagerungen, Kommissionierungen und Lagerplatzumlagerungen sind.  
>   
>  Wenn Sie einen Wareneingangslagerplatz oder einen Warenausgangslagerplatz umbenennen, müssen alle gebuchten Wareneingänge oder Warenausgänge, die sich auf den jeweiligen Lagerplatz beziehen, umbenannt werden.  

## Weitere Informationen  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]