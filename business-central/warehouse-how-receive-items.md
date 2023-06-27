---
title: Empfangen von Artikeln
description: 'Dieser Artikel gibt einen Überblick über die verschiedenen Möglichkeiten, Artikel in einem Lager mit einem Wareneingang zu erhalten.'
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a>Empfangen Sie Artikel mit Wareneingängen

In [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie Artikel und lagern sie, wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden ein.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen zum Umgang mit eingehenden Artikeln finden Sie unter [Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

Der folgende Artikel bezieht sich auf die Methoden C und D in der vorherigen Tabelle.

## <a name="receive-items-with-a-warehouse-receipt"></a>Empfangen Sie Artikel mit einem Wareneingang

Wenn Artikel bei einem Lager ankommen, das für die Bearbeitung von Wareneingängen eingerichtet wurde, müssen Sie die Zeilen des freigegebenen Herkunftsbelegs abrufen, der dem Wareneingang ausgelöst hat. Wenn Sie Lagerplätze verwenden, können Sie entweder den Standardlagerplatz akzeptieren oder den Lagerplatz angeben, in dem die Artikel abgelegt werden sollen. Letzteres kann erforderlich sein, wenn Sie einen Artikel zum ersten Mal erhalten. Geben Sie dann die Mengen der Artikel eingeben, die Sie erhalten haben, und den Wareneingang buchen.  

Sie können einen Wareneingang auf eine von zwei Arten erstellen:

* Im Push-Verfahren, wenn die Arbeit auftragsbezogen erledigt wird. Wählen Sie die Aktion **Wareneingang erstellen** im Herkunftsbeleg, z. B. Bestellung, Verkaufsreklamation oder Umlagerungsauftrag, um den Wareneingang für einen Herkunftsbeleg zu erstellen.
* In einem Pull-Verfahren, bei dem Sie die Aktion **Freigeben** im Herkunftsbeleg verwenden, z. B. in einer Bestellung, einer Verkaufsreklamation oder einem Umlagerungsauftrag, um den Beleg an das Lager freizugeben. Ein Lagermitarbeiter erstellt einen **Wareneingang** für einen oder mehrere freigegebene Herkunftsbelege. Das folgende Verfahren beschreibt, wie Sie einen Wareneingang in einem Pull-Verfahren erstellen. Das folgende Verfahren beschreibt, wie Sie einen Wareneingang in einem Pull-Verfahren erstellen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  

    Füllen Sie das Feld **Lagerplatzcode** im Inforegister **Allgemein** aus. Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen in jede Zeile kopiert.

    Für einen Lagerort, der Lagerplätze erfordert, füllen Sie das Feld **Lagerplatzcode** aus. Je nach Einrichtung kann [!INCLUDE[prod_short](includes/prod_short.md)] den Lagerplatzcode für Sie hinzufügen. Erfahren Sie mehr unter [Zone und Lagerplatzcodes](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Sie können den Herkunftsbeleg auf zwei Arten erhalten:

    1. Wählen Sie die **Herkunftsbelege holen** Aktion aus. Die Seite **Herkunftsbelege - eingehend** wird geöffnet. Hier können Sie einen oder mehrere an das Lager freigegebene Herkunftsbelege auswählen, die empfangen werden müssen.
    2. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus. Die Seite **Filter zum Abrufen von Herkunftsbelegen - eingehend** wird geöffnet. Hier können Sie den Herkunftsbelegfilter auswählen und anwenden. Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden auf der Seite **Wareneingang** hinzugefügt. Weitere Informationen finden Sie unter [So verwenden Sie Filter zum Abrufen von Herkunftsbelegen](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents)

4. Stellen Sie die zu erhaltende Menge ein.

    Das Feld **Menge akt. Lieferung** enthält die für jede Zeile ausstehende Menge. Sie können die Menge jedoch bei Bedarf ändern. 

    Um den Wert im Feld **Menge akt. Lieferung** in allen Zeilen auf Null festzulegen, wählen Sie die Aktion **Menge akt. Lieferung löschen** aus. Beispielsweise ist es hilfreich, die Mengen auf Null zu setzen, wenn Sie einen Barcode-Scanner verwenden, um die Empfangsmengen zu aktualisieren. Um die Restmengen aus dem Herkunftsbeleg erneut hinzuzufügen, wählen Sie die Aktion **Menge akt. Lieferung autom. ausfüllen**.  

    Geben Sie einem Wareneingangsbeleg, bei dem die eingegangene Menge höher als die bestellte Menge ist, die tatsächlich eingegangene Menge in das Feld **Zu erhaltende Menge** ein. Wenn die Erhöhung innerhalb der durch einen zugeordneten Eingangsüberschusscode festgelegten Toleranz liegt, wird das Feld **Eingangsüberschussmenge** aktualisiert, um die Menge anzuzeigen, um die der Wert im Feld **Menge** überschritten wird. Wenn die Erhöhung über der Toleranz liegt, ist der Eingangsüberschuss nicht zulässig.

5. Buchen Sie den Wareneingang. Die Mengenfelder in den Herkunftsbelegen werden aktualisiert und die Artikel werden dem Lagerbestand hinzugefügt.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Wenn Sie die Lagereinlagerung verwenden, die sich auf Methode D in der Tabelle am Anfang dieses Artikels bezieht, werden die Artikel empfangen, können aber erst kommissioniert werden, wenn sie eingelagert wurden. Weitere Informationen zum Einlagern von Artikeln finden Sie unter [Einlagern von Artikeln mit Lagereinlagerungen](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Ziehen Sie andernfalls die Aktion **Buchen und drucken** in Betracht. Die Aktion bucht den Beleg und druckt ihn als Einlagerungsanweisung, die zeigt, wo der Artikel eingelagert werden soll.

    > [!NOTE]  
    > Wenn Ihr Lager Cross-Docking verwendet, können Sie prüfen, ob Sie Artikel Cross-Dock-fähig sind, ohne sie einzulagern. Weitere Informationen zum Cross-Docking finden Sie unter [Cross-Docking von Artikeln](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a>So verwenden Sie Filter zum Abrufen von Herkunftsbelegen

Aus einem Wareneingang können Sie die Seite **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die die zu empfangenden Artikel angeben.

1. Wählen Sie im Wareneingang die Aktion **Filter zum Holen von Herk.-Belegen verwenden.**.
2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.

    Die Seite **Herkunftsbelegfilterkarte - eingehend** wird angezeigt.

3. Verwenden Sie die Filter, um den Typ der abzurufenden Herkunftsbelegzeilen zu definieren. Beispielsweise können Sie Arten von Herkunftsbelegen auswählen, z. B. Einkaufs- oder Umlagerungsaufträge.
4. Wählen Sie **Ausführen** aus.  

Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden auf der Seite **Wareneingang** hinzugefügt, auf der Sie die Filter aktiviert haben.

Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Filter werden auf der Seite **Filter z. Holen v. Herk.-Bel.** gespeichert und sind das nächste Mal verfügbar, wenn sie benötigt werden. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

## <a name="zone-and-bin-codes"></a>Zonen- und Lagerplatzcodes

Um Artikel mit Lagerklassen anzunehmen, die von den Lagerklassen der Lagerplätze im Feld **Lagerplatzcode** des Belegkopfes abweichen, löschen Sie das Feld **Lagerplatzcode** des Kopfes, bevor Sie die Herkunftsbelegzeilen der Artikel holen können.  
<!-- TBD, table with comparison of various options-->

Wenn Lagerplätze für einen Lagerort obligatorisch sind, werden Zonen- und Lagerplatzcodes wie folgt zu Wareneingangsbelegen hinzugefügt:

* Für erweiterte Konfigurationen, die gezieltes Einlagern und Kommissionieren verwenden, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] den Eingangslagerplatzcode auf der Seite **Lagerortkarte** für den Lagerort. Wenn kein Lagerplatzcode angegeben ist, ist kein Lagerplatz angegeben. Wenn die Lagerplätze für Artikel und Belege nicht übereinstimmen, ist der Lagerplatzcode für Belege leer.
* Wenn in anderen Konfigurationen kein Eingangslagerplatzcode angegeben ist, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] den Lagerplatzcode aus dem Herkunftsbeleg.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
