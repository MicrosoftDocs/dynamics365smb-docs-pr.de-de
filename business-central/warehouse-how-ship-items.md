---
title: Versenden von Artikeln
description: In diesem Artikel wird beschrieben, wie Sie Artikel aus Ihrem Lager abhängig von Ihrer Lagerkonfiguration für die Versandverarbeitung versenden können.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: b66a0a0a4cad12c4f41c53569b0007c51e846de7
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531215"
---
# <a name="ship-items"></a>Versenden von Artikeln

Wenn Sie Artikel von einem Lager liefern, das nicht für die Bearbeitung des Warenausgangs eingerichtet wurde, können Sie den Warenausgang einfach im zugehörigen Geschäftsdokument, wie einer Verkaufsauftrag, einer Serviceauftrag, eine Einkaufsreklamation oder ein ausgehender Umlagerungsauftrag, erfassen.

Wenn Sie Artikel aus einem Lager versenden, das für die Verarbeitung von Warensendungen festgelegt ist, können Sie nur Artikel auf der Basis von Quellbelegen versenden, die andere Einheiten der Firma zur Aktion an das Lager freigegeben haben.

> [!NOTE]
> Wenn Ihr Lager Crossdocking und Lagerplätze benutzt, können Sie für jede Zeile die Menge an Artikeln sehen, die in die Zuordnungslagerplätze eingelagert wurde. Die Anwendung berechnet dann diese Mengen automatisch, wenn die Felder im Warenausgang aktualisiert werden. Wenn dies die Mengen sind, die zu dem Warenausgang passen, den Sie gerade vorbereiten, können Sie eine Kommissionierung für alle Zeilen erstellen und dann den Warenausgang vervollständigen. Erfahren Sie mehr unter [Zuordnungselemente](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Liefern Sie Artikel mit einem Verkaufsauftrag

Nachfolgend wird erläutert, wie Artikel aus einem Verkaufsauftrag geliefert werden. Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie einen Auftrag oder erstellen Sie einen neuen. Erfahren Sie mehr unter [Produkte verkaufen](sales-how-sell-products.md).
3. Geben Sie in dem Feld **Zu liefern** die gelieferte Menge an.

    Der Wert im Feld **Menge geliefert** wird aktualisiert. Wenn dieses eine Teillieferung ist, ist der Wert niedriger als der Wert im Feld **Menge**. Erfahren Sie mehr unter [Teillieferungen verarbeiten](sales-how-send-partial-shipments.md).
4. Wählen Sie die Aktion **Buchen**.

> [!NOTE]
> Wenn Ihre Organisation keine Verkaufsaufträge verwendet, setzt [!INCLUDE [prod_short](includes/prod_short.md)] voraus, dass Sie die vollständige Menge versendet haben, wenn Sie die Verkaufsrechnung buchen. Wenn dies im Widerspruch zur Funktionsweise Ihrer Organisation steht, empfehlen wir Ihnen, Verkaufsaufträge zu verwenden und Sendungen zu registrieren, wie in diesem Artikel erläutert.

## <a name="ship-items-with-a-warehouse-shipment"></a>Liefern Sie Artikel mit einem Warenausgang

Zuerst erstellen Sie einen Warenausgangsbeleg von einem Geschäftsherkunftsbeleg. Dann wählen Sie die angegebenen Artikel für den Versand aus.

### <a name="create-a-warehouse-shipment"></a>Erstellen Sie einen neuen Warenausgang

Normalerweise erstellt der Mitarbeiter, der für die Lieferung verantwortlich ist, einen Warenausgang. Das folgende Verfahren beschreibt, wie Sie die Sendung in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] manuell erstellen. Ihre Organisation hat jedoch möglicherweise einen Teil des Prozesses automatisiert, z. B. durch die Verwendung von tragbaren oder montierten Scannern, die von externen Anbietern unterstützt werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie **Neu** aus.  

    Füllen Sie die Felder auf dem Inforegister **Allgemein** aus. Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen in jede Zeile kopiert.  

    Für Lagerkonfigurationen mit gesteuerter Einlagerung und Kommissionierung: Wenn der Lagerort eine Vorgabezone und einen Vorgabelagerplatz für Warenausgänge hat, werden die Felder **Zonencode** und **Lagerplatzcode** automatisch ausgefüllt, Sie können diese jedoch bei Bedarf ändern.  

    > [!NOTE]  
    > Wenn Sie Artikel mit Lagerklassen liefern möchten, die von den Lagerklassen der Lagerplätze im Feld **Lagerplatzcode** des Belegkopfes abweichen, müssen Sie den Inhalt des Feldes **Lagerplatzcode** des Kopfes löschen, bevor Sie die Herkunftsbelegzeilen der Artikel holen können.  
3. Wählen Sie die **Herkunftsbelege holen** Aktion aus. Die Seite **Herkunftsbelege** wird geöffnet.

    Aus einem neuen oder offenen Warenausgang können Sie die Seite **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die festlegen, welche Artikel geliefert werden sollen.

    1. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
    2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.  
    3. Legen Sie die Art von Herkunftsbelegzeilen fest, die Sie abrufen möchten, indem Sie die jeweiligen Filterfelder ausfüllen.  
    4. Wählen Sie die Aktion **Ausführen** aus.  

    Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden nun auf der Seite **Warenausgang** eingefügt, in dem Sie die Filterfunktion aktiviert haben.  

    Die Filterkombinationen, die Sie definieren, werden auf der Seite **Filter z. Holen v. Herk.-Bel.** gespeichert, bis das nächste Mal benötigt werden. Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

4. Wählen Sie die Herkunftsbelege, für die Sie Artikel liefern möchten, und bestätigen Sie dann mit **OK**.  

Die Zeilen der Herkunftsbelege werden auf der Seite **Warenausgang** angezeigt. Das Feld **Zu liefern** ist für jede Zeile gefüllt, Sie können die Menge jedoch bei Bedarf ändern. Wenn Sie den Inhalt des Feldes **Lagerplatzcode** m Inforegister **Allgemein** löschen, bevor Sie die Zeilen abrufen, muss in jeder Warenausgangszeile ein geeigneter Lagerplatzcode eingetragen werden.  

> [!NOTE]  
> Sie können nicht mehr Artikel liefern als die Anzahl im Feld **Restmenge** der Herkunftsbelegzeile. Um weitere Artikel zu liefern, rufen Sie mit der Filterfunktion einen weiteren Herkunftsbeleg ab, der eine Zeile für den Artikel enthält.  

Wenn Sie die Zeilen haben, die Sie ausliefern möchten, können Sie den Prozess starten, der die Zeilen an die Lagermitarbeiter zur Kommissionierung schickt.

### <a name="pick-and-ship"></a>Kommissionieren und ausliefern

In der Regel erstellt ein Lagermitarbeiter, der für das Kommissionieren zuständig ist, einen Kommissionierungsbeleg oder öffnet einen bereits erstellten Kommissionierbeleg.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Warenausgangslieferung aus, die Sie kommissionieren möchten, und wählen Sie die **Kommissionierung erstellen** Aktion aus.
3. Füllen Sie die Felder auf der Anforderungsseite aus, und wählen Sie dann **OK** aus. Der angegebene Kommissionierbeleg wird erstellt.

    Alternativ öffnen Sie einen vorhandenen Kommissionierungsbeleg.
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kommissionierungen** ein und wählen Sie dann den zugehörigen Link. Wählen Sie die Lagerkommissionierung aus, die Sie bearbeiten möchten.

    Wenn Ihr Lager für die Verwendung von Lagerplätzen eingerichtet wurde, wurden die Kommissionierzeilen in Aktionszeilen der Arten "Lagerentnahme" und "Einlagerung" umgewandelt.

    Sie können die Zeilen sortieren, der Kommissionierung einen Mitarbeiter zuordnen, einen Gebindeanbruchsfilter setzen, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, und die Kommissionieranweisungen drucken.

5. Führen Sie die eigentliche Kommissionierung von Artikeln aus und lagern Sie die Artikel in dem festgelegten Warenausgangslagerplatz ein, oder im Warenausgangsbereich, wenn Sie keine Lagerplätze haben.
6. Wählen Sie die Aktion **Auswahl registrieren**.

    Die Felder **Zu liefern** und **Belegstatus** im Kopf des Warenausgangsbelegs werden aktualisiert. Die Artikel, die Sie kommissioniert haben, stehen nicht mehr für Kommissionierungen für andere Warenausgänge oder für interne Arbeitsgänge zur Verfügung.
7. Drucken Sie die Lieferscheine, bereiten Sie die Pakete zur Lieferung vor und buchen Sie dann den Warenausgang.

Weitere Informationen zum Kommissionieren für Warenausgänge finden Sie unter [Kommissionieren von Artikeln für den Warenausgang](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Sie können den Kommissioniervorschlag auch verwenden, um mehrere Anweisungen in eine zu übernehmen (für mehrere Warenausgänge) und dadurch die Effizienz der Kommissionierung im Lager zu erhöhen. Erfahren Sie mehr unter [Kommissionierungen im Arbeitsblatt bearbeiten](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Wenn Sie auf den Empfang bestimmter Artikel warten, die im Lager ankommen sollen, und wenn Sie die Zuordnungsfunktionalität verwenden, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] in jeder Warenausgangs- oder Kommissionierarbeitsblattszeile die Menge des Artikels, die sich im Zuordnungslagerplatz befindet. Sie aktualisiert dieses Feld jedes Mal, wenn Sie den Warenausgangsbeleg oder das Arbeitsblatt verlassen und öffnen. Erfahren Sie mehr unter [Zuordnungselemente](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
