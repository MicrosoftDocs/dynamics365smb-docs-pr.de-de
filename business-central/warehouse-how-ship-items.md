---
title: 'So geht''s: Artikel versenden | Microsoft Docs'
description: "Abhängig von Ihrer Lagerkonfiguration können Sie entweder Lieferung im zugehörigen ausgehenden Geschäftsdokument, wie einem Verkaufsauftrag, direkt buchen, oder Sie können einen der Warenausgangsbelege verwenden, die einen Workflow berücksichtigen und in verschiedene Lageraktivitäten integriert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54f554e2e0acf657fdf77caa863ff4e028734418
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="ship-items"></a>Versenden von Artikeln
Wenn Sie Artikel von einem Lager liefern, das nicht für die Bearbeitung des Warenausgangs eingerichtet wurde, können Sie den Warenausgang einfach im zugehörigen Geschäftsdokument, wie einer Verkaufsauftrag, einer Serviceauftrag, eine Einkaufsreklamation oder ein ausgehender Umlagerungsauftrag, erfassen.

Wenn Sie Artikel aus einem Lagerort liefern, der so eingerichtet wurde, dass die Bearbeitung des Warenausgangs erforderlich ist, können Sie den Warenausgang nur auf der Basis von Herkunftsbelegen erfassen, die andere Abteilungen Ihres Unternehmens für die Bearbeitung freigegeben haben.

> [!NOTE]
> Wenn Ihr Lager Crossdocking und Lagerplätze benutzt, können Sie für jede Zeile die Menge an Artikeln sehen, die in die Zuordnungslagerplätze eingelagert wurde. Die Anwendung berechnet diese Mengen automatisch, wenn die Felder im Warenausgang aktualisiert werden. Wenn dies die Mengen sind, die zu dem Warenausgang passen, den Sie gerade vorbereiten, können Sie eine Kommissionierung für alle Zeilen erstellen und dann den Warenausgang vervollständigen. Weitere Informationen finden Sie unter [Zuordnen von Artikeln](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>So liefern Sie Artikel mit einem Verkaufsauftrag
Nachfolgend wird erläutert, wie Artikel mit einer Bestellung empfangen werden. Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus, geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie einen Auftrag oder erstellen Sie einen neuen. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3. Geben Sie in dem Feld **Zu liefern** die empfangene Menge an.

    Der Wert im Feld **Menge geliefert** wird aktualisiert. Wenn dieses eine Teillieferung ist, ist der Wert niedriger als der Wert im Feld **Menge**.
4. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>So liefern Sie Artikel mit einem Warenausgang
Zuerst erstellen Sie einen Warenausgangsbeleg von einem Geschäftsherkunftsbeleg. Dann wählen Sie die angegebenen Artikel für den Versand aus.

### <a name="to-create-a-warehouse-shipment"></a>So erstellen Sie einen neuen Warenausgang.
Normalerweise erstellt der Mitarbeiter, der für die Lieferung verantwortlich ist, einen Warenausgang.
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Warenausgänge** ein und wählen den zugehörenden Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  

    Füllen Sie die Felder auf dem Inforegister **Allgemein** aus. Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen in jede Zeile kopiert.  

    Für Lagerkonfigurationen mit gesteuerte Einlagerung und Kommissionierung: Wenn der Lagerort eine Vorgabezone und einen Vorgabelagerplatz für Warenausgänge hat, werden die Felder **Zonencode** und **Lagerplatzcode** automatisch ausgefüllt, Sie können diese jedoch bei Bedarf ändern.  

    > [!NOTE]  
    >  Wenn Sie Artikel mit Lagerklassen liefern möchten, die von den Lagerklassen der Lagerplätze im Feld **Lagerplatzcode** des Belegkopfes abweichen, müssen Sie den Inhalt des Feldes **Lagerplatzcode** des Kopfes löschen, bevor Sie die Herkunftsbelegzeilen der Artikel holen können.  
3.  Wählen Sie die **Herkunftsbelege holen** Aktion aus. Das Fenster **Herkunftsbelege** wird geöffnet.

    Aus einem neuen oder offenen Warenausgang können Sie das Fenster **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die festlegen, welche Artikel geliefert werden sollen.

    1. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
    2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.  
    3. Legen Sie die Art von Herkunftsbelegzeilen fest, die Sie abrufen möchten, indem Sie die jeweiligen Filterfelder ausfüllen.  
    4. Wählen Sie die Aktion **Ausführen** aus.  

    Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden nun im Fenster **Warenausgang** eingefügt, in dem Sie die Filterfunktion aktiviert haben.  

    Die Filterkombinationen, die Sie definieren, werden im Fenster **Filter z. Holen v. Herk.-Bel.** gespeichert, bis das nächste Mal benötigt werden. Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

4.  Wählen Sie die Herkunftsbelege, für die Sie Artikel liefern möchten, und bestätigen Sie dann mit **OK**.  

Die Zeilen der Herkunftsbelege werden im Fenster **Warenausgang** angezeigt. Das Feld **Zu liefern** ist für jede Zeile gefüllt, Sie können die Menge jedoch bei Bedarf ändern. Wenn Sie den Inhalt des Feldes **Lagerplatzcode** m Inforegister **Allgemein** löschen, bevor Sie die Zeilen abrufen, muss in jeder Warenausgangszeile ein geeigneter Lagerplatzcode eingetragen werden.  

> [!NOTE]  
>  Sie können nicht mehr Artikel liefern als die Anzahl im Feld **Restmenge** der Herkunftsbelegzeile. Um weitere Artikel zu liefern, holen Sie einen weiteren Herkunftsbeleg, der eine Zeile für den Artikel enthält, indem Sie die Filterfunktion zum Holen von Herkunftsbelegen mit dem Artikel verwenden.  

Wenn Sie die Zeilen haben, die Sie ausliefern möchten, können Sie den Prozess starten, der die Zeilen an die Lagermitarbeiter zur Kommissionierung schickt.

### <a name="to-pick-and-ship"></a>So können Sie kommissionieren und ausliefern:
In der Regel erstellt ein Lagermitarbeiter, der für das Kommissionieren zuständig ist, einen Kommissionierungsbeleg oder öffnet einen bereits erstellten Kommissionierbeleg.
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Warenausgänge** ein und wählen den zugehörenden Link aus.
2. Wählen Sie die Warenausgangslieferung aus, die Sie kommissionieren möchten, und wählen Sie die **Kommissionierung erstellen** Aktion aus.
3. Füllen Sie die Felder im Anforderungsfenster aus, und wählen Sie dann die Schaltfläche **OK** aus. Der angegebene Kommissionierbeleg wird erstellt.

    Alternativ öffnen Sie eine vorhandene Kommissionierung.
4. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben Sie **Auswahl** ein und wählen dann den zugehörigen Link aus. Wählen Sie die Lagerkommissionierung aus, die Sie bearbeiten möchten.

    Wenn Ihr Lager für die Verwendung von Lagerplätzen eingerichtet wurde, wurden die Kommissionierzeilen in Aktionszeilen der Arten "Lagerentnahme" und "Einlagerung" umgewandelt.

    Sie können die Zeilen sortieren, der Kommissionierung einen Mitarbeiter zuordnen, einen Gebindeanbruchsfilter setzen, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, und die Kommissionieranweisungen drucken.

5. Führen Sie die eigentliche Kommissionierung von Artikeln aus und lagern Sie die Artikel in dem festgelegten Warenausgangslagerplatz ein, oder im Warenausgangsbereich, wenn Sie keine Lagerplätze haben.
6. Wählen Sie die Aktion **Kommissionierung registrieren** aus.

    Die Felder **Zu liefern** und **Belegstatus** im Kopf des Warenausgangsbelegs werden aktualisiert. Die Artikel, die Sie kommissioniert haben, stehen nicht mehr für Kommissionierungen für andere Warenausgänge oder für interne Arbeitsgänge zur Verfügung.
7. Drucken Sie die Lieferscheine, bereiten Sie die Pakete zur Lieferung vor und buchen Sie dann den Warenausgang.

Weitere Informationen zum Kommissionieren für Warenausgänge finden Sie unter: [Kommissionieren von Artikeln für den Warenausgang](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Sie können den Kommissioniervorschlag auch verwenden, um mehrere Anweisungen in eine zu übernehmen (für mehrere Warenausgänge) und dadurch die Effizienz der Kommissionierung im Lager zu erhöhen. Weitere Informationen finden Sie unter [Kommissionierungen im Vorschlag bearbeiten](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Wenn Sie auf bestimmte Artikel warten, die im Lager ankommen sollen, und wenn Sie die Zuordnungsfunktionalität verwenden, berechnet [!INCLUDE[d365fin](includes/d365fin_md.md)] in jeder Warenausgangs- oder Kommissioniervorschlagszeile die Menge des Artikels, die sich im Zuordnungslagerplatz befindet. Sie aktualisiert dieses Feld jedes Mal, wenn Sie den Warenausgangsbeleg oder den Vorschlag verlassen und öffnen. Weitere Informationen finden Sie unter [Zuordnen von Artikeln](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

