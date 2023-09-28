---
title: Versenden von Artikeln
description: 'Dieser Artikel beschreibt, wie Sie Artikel aus Ihrem Lager versenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# Liefern Sie Artikel mit einem Warenausgang

In [!INCLUDE[prod_short](includes/prod_short.md)] kommissionieren und versenden Sie Artikel wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden.

|Art|Ausgangsprozess|Kommissionierung erforderlich|Warenausgang erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Die Kommissionierung und den Versand aus der Auftragszeile buchen|||Keine dedizierte Lageraktivität.|  
|B|Die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg buchen|Aktiviert||Basis: Auftragsbezogene Logistik|  
|U|Die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg buchen||Aktiviert|Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg buchen|Aktiviert|Aktiviert|Erweitert|  

Mehr Informationen über den Versand von Artikeln finden Sie unter [Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).

Dieser Artikel bezieht sich auf die Methoden C und D in der Tabelle. In beiden Methoden starten Sie, indem Sie einen Warenausgangsbeleg aus einem Geschäftsherkunftsbeleg erstellen. Dann wählen Sie die angegebenen Artikel für den Versand aus.

Wenn ein Lagerort Warenausgänge erfordert, können Sie Artikel basierend auf Herkunftsbelegen versenden, die für das Lager freigegeben wurden. Durch die Freigabe von Herkunftsbelegen werden die darauf befindlichen Artikel für die Bearbeitung im Lager bereit gemacht. Es folgen Beispiele für Herkunftsbelege:

* Verkaufsaufträge
* Einkaufsreklamationen
* Umlagerungsaufträge
* Serviceaufträge

Sie können einen Warenausgang auf eine von zwei Arten erstellen:

* Im Push-Verfahren, wenn die Arbeit auftragsbezogen erledigt wird. Wählen Sie im Herkunftsbeleg die Aktion **Warenausgang erstellen** aus, um einen Warenausgang für den Beleg zu erstellen.
* In einem Pull-Verfahren, bei dem Sie die Aktion **Freigeben** im Herkunftsbeleg verwenden, um es an das Lager freizugeben. Ein Lagermitarbeiter erstellt einen **Warenausgang** für einen oder mehrere freigegebene Herkunftsbelege. Das folgende Verfahren beschreibt, wie Sie Warenausgänge in einem Pull-Verfahren erstellen.

## So liefern Sie Artikel mit einem Warenausgangsbeleg

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie **Neu** aus.  
3. Geben Sie im Feld **Nr.** die Nummernserie aus, die zum Erstellen einer ID für die Sendung verwendet werden soll.  
4. Wählen Sie im Feld **Lagerortcode** den Lagerort aus, von dem aus Sie versenden. 

    Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen aus dem Lagerort in jede Zeile kopiert.  
5. Wenn für den Lagerort Lagerplätze erforderlich sind, füllen Sie das Feld **Lagerplatzcode** aus. Je nach Einrichtung kann [!INCLUDE[prod_short](includes/prod_short.md)]] den Lagerplatzcode für Sie hinzufügen. Erfahren Sie mehr unter [Zone und Lagerplatzcodes](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Sie können den Herkunftsbeleg auf zwei Arten erhalten:

    * Wählen Sie die **Herkunftsbelege holen** Aktion aus. Die Seite **Herkunftsbelege - ausgehend** wird geöffnet. Hier können Sie einen oder mehrere an das Lager freigegebene Herkunftsbelege auswählen, die versendet werden müssen.
    * Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus. Die Seite **Filter zum Abrufen von Herkunftsbelegen.** wird geöffnet. Sie können den Herkunftsbelegfilter auswählen und anwenden. Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden auf der Seite **Warenausgang** hinzugefügt. Weitere Informationen finden Sie unter [So verwenden Sie Filter zum Abrufen von Herkunftsbelegen](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents)

    > [!NOTE]
    > Wenn Ihr Lagerort Crossdocking und Lagerplätze für jede Zeile benutzt, können Sie die Menge an Artikeln überprüfen, die in die Zuordnungslagerplätze eingelagert wurde. [!INCLUDE [prod_short](includes/prod_short.md)] berechnet die Mengen automatisch, wenn die Felder im Warenausgang aktualisiert werden. Wenn dies die Mengen auf dem Warenausgang sind, den Sie gerade vorbereiten, können Sie eine Kommissionierung für alle Artikel erstellen und dann den Warenausgang vervollständigen. Erfahren Sie mehr unter [Zuordnungselemente](warehouse-how-to-cross-dock-items.md).

7. Erstellen Sie eine Warenkommissionierung Wenn der Lagerort eine Kommissionierung erfordert, können Sie Kommissionierungsaktivitäten für Warenlagersendungen auf zwei Arten erstellen:

    * Im Push-Verfahren, bei dem Sie die Aktion **Kommissionierung erstellen** verwenden. Wählen Sie die zu entnehmenden Zeilen aus und geben Sie Informationen zu den Kommissionierungen an. Zum Beispiel, aus welchen Lagerplätzen entnommen und eingelagert werden soll und wie viele Einheiten bewegt werden sollen. Die Lagerplätze können für den Lagerort oder die Ressource vordefiniert werden.
    * Im Pull-Verfahren, bei dem Sie die Aktion **Freigeben** verwenden. Verwenden Sie auf der Seite **Kommissionierungsarbeitsblatt** die Aktion **Lagerdokumente abrufen**, um ihre zugewiesenen Kommissionierungen abzurufen. Wenn die Kommissionierungen vollständig erfasst sind, werden die Zeilen im **Kommissionierarbeitsblatt** gelöscht. Weitere Informationen finden Sie unter [Artikel für den Warenausgang kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)

    > [!TIP]
    > Für einen Lagerort, an dem keine Kommissionierung erforderlich ist, können Sie den Warenausgang ausdrucken und als Kommissionierungsliste verwenden.

8. Geben Sie die zu liefernde Menge an.  

    Für einen Lagerort, der kommissioniert werden muss, wird das Feld **Zu liefern** automatisch aktualisiert, wenn die Kommissionierung registriert wird. Andernfalls wird das Feld **Zu liefern** für jede Zeile mit der ausstehenden Menge für jede Zeile gefüllt, wenn die Warenausgangszeile erstellt wird.

    Sie können die Menge ändern, aber Sie können nicht mehr Artikel als die Anzahl im Feld **Restmenge** in der Zeile des Herkunftsbelegs oder dem Feld **Ausgewählte Menge** versenden, wenn eine Kommissionierung erforderlich ist.

    Um den Wert im Feld **Zu liefern** in allen Zeilen auf Null festzulegen, wählen Sie die Aktion **Menge zu liefern löschen** aus. Beispielsweise ist es hilfreich, die Mengen auf Null zu setzen, wenn Sie einen Barcode-Scanner verwenden, um die Versandmengen zu aktualisieren. Um die für den Versand verfügbare Menge hinzuzufügen, wählen Sie die Aktion **Menge zu liefern autom. ausfüllen**.

9. Buchen Sie die Lieferung.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## So verwenden Sie Filter zum Abrufen von Herkunftsbelegen

Aus einem Warenausgang können Sie die Seite **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die festlegen, welche Artikel geliefert werden sollen.

1. Wählen Sie im Lagerausgang die Aktion **Filter zum Holen von Herk.-Belegen verwenden.**. 
2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.

    Die Seite **Herkunftsbelegfilterkarte - ausgehend** wird geöffnet.

3. Verwenden Sie die Filter, um den Typ der abzurufenden Herkunftsbelegzeilen zu definieren. Beispielsweise können Sie Arten von Herkunftsbelegen auswählen, z. B. Verkaufs- oder Umlagerungsaufträge.
4. Wählen Sie **Ausführen** aus.  

Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden auf der Seite **Warenausgang** hinzugefügt, in der Sie die Filter festlegen.

Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Filter werden auf der Seite **Filter z. Holen v. Herk.-Bel.** gespeichert und sind das nächste Mal verfügbar, wenn sie benötigt werden. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

## Zonen- und Lagerplatzcodes

Wenn Lagerplätze am Lagerort obligatorisch sind, schlägt [!INCLUDE [prod_short](includes/prod_short.md)] eine Zone und einen Lagerplatzcode auf dem Warenausgangsbeleg vor.

* Bei erweiterten Konfigurationen, in denen ein Lagerort gezieltes Einlagern und Kommissionieren verwendet, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] den Lagerplatz, der im Feld **Warenausgangslagerplatzcode** auf der **Lagerortkarte** angegeben ist. Wenn kein **Warenausgangslagerplatzcode** angegeben ist, ist das Feld leer. Wenn der Artikel und der Lagerplatz nicht übereinstimmen, lässt [!INCLUDE [prod_short](includes/prod_short.md)] den Lagerplatz leer.
* In anderen Fällen verwendet [!INCLUDE [prod_short](includes/prod_short.md)] immer den Lagerplatz, der im Feld **Warenausgangslagerplatzcode** auf der **Lagerortkarte** zuerst angegeben ist. Wenn kein Warenausgangslagerplatzcode angegeben ist, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] den Lagerplatzcode aus dem Herkunftsbeleg.

## Verwenden von Auftragsmontageartikeln in Warenausgängen

Verwenden Sie in den Auftragsmontageszenarien das Feld **Zu liefern** in Warenausgangszeilen, um zu erfassen, wie viele Einheiten montiert werden. Die Menge wird als Montageausstoß gebucht, wenn Sie den Warenausgang buchen. Für andere Warenausgangszeilen ist der Wert im Feld **Zu liefern** Null.

Wenn Arbeiter einige oder alle Teile für die Auftragsmontagemenge montieren, erfassen sie die Menge im Feld **Zu liefern** in der Warenausgangszeile. Wählen Sie dann die Aktion **Warenausgang buchen** aus. Die Montage-Istmenge wird inklusive des Komponentenverbrauchs gebucht. Eine Verkaufslieferung für die Menge wird für den Verkaufsauftrag gebucht.

Vom Montageauftrag aus können Sie **Warenausgangszeile für Programmfertigung** wählen, um auf die Warenausgangszeile zuzugreifen.

Nachdem Sie den Warenausgang gebucht haben, werden verschiedene Felder in der Verkaufsauftragszeile aktualisiert, um den Status im Lager anzuzeigen. Die folgenden Felder werden auch aktualisiert, um anzuzeigen, wie viele Auftragsmontagemengen noch nicht montiert und geliefert wurden:

* **Auftragsmontage - Lagerrestbestellmenge**
* **Auftragsmontage - Lagerrestbestellmenge (Basis)**

> [!NOTE]
> In Kombinationsszenarien, in denen ein Teil der Menge montiert und ein anderer aus dem Lager geliefert werden muss, werden mindestens zwei Warenausgangszeilen erstellt. Eine für die Auftragsmontagemenge, und eine für die Lagermenge.
>
> Die Menge der Programmfertigung wird wie in diesem Artikel beschrieben gehandhabt. Die Lagerbestandsmenge wird als reguläre Warenausgangsposition gehandhabt. Weitere Informationen zu Kombinationsszenarien finden Sie unter [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).

## Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
