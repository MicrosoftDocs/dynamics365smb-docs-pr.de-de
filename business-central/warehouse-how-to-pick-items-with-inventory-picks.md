---
title: So kommissionieren Sie Artikel mit Lagerkommissionierungen
description: 'Erfahren Sie, wie Sie Lagerkommissionierungen verwenden, um Kommissionierungs- und Versandinformationen für Herkunftsbelege aufzuzeichnen und zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# <a name="pick-items-with-inventory-picks"></a><a name="pick-items-with-inventory-picks"></a>Artikel mit der Lagerkommissionierung kommissionieren

In [!INCLUDE[prod_short](includes/prod_short.md)] kommissionieren und versenden Sie Artikel wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden.

|Art|Ausgangsprozess|Kommissionierung erforderlich|Warenausgang erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Die Kommissionierung und den Versand aus der Auftragszeile buchen|||Keine dedizierte Lageraktivität.|  
|B|Die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg buchen|Aktiviert||Basis: Auftragsbezogene Logistik|  
|U|Die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg buchen||Aktiviert|Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg buchen|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).

Dieser Artikel bezieht sich auf die Methode B in der Tabelle.

Wenn Ihr Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen. Ausgehende Herkunftsbelege können Verkaufsaufträge, Einkaufsreklamationen und ausgehende Umlagerungsaufträge umfassen.

> [!NOTE]
> Produktions- und Montageauftragskomponentenbedarf stellt ebenfalls ausgehende Herkunftsbelege dar. Weitere Informationen über die Verarbeitung von Fertigungs- und Montageaufträge für interne Prozesse finden Sie unter [Designdetails: Interner Lagerfluss](design-details-internal-warehouse-flows.md).
>
> Obwohl Serviceaufträge auch ausgehende Herkunftsbelege sind, unterstützen sie nicht die grundlegende, auftragsbezogene Komplexitätsstufe.
>
> Bei der Kommissionierung und Lieferung von Verkaufszeilenmengen, die auftragsbezogen montiert werden, gibt es Regeln, die Sie einhalten müssen, wenn sie die Lagerkommissionierzeilen erstellen. Erfahren Sie mehr unter [Verarbeitung von Programmfertigung mit kommissionierten Bestandsartikeln](#handling-assemble-to-order-items-with-inventory-picks).  

Sie können eine Lagerkommissionierung auf drei Arten erstellen:

* Erstellen Sie die Lagerkommissionierung direkt vom Herkunftsbeleg aus.  
* Erstellen Sie Lagerkommissionierungen für mehrere Herkunftsbelege gleichzeitig, indem Sie einen Batchauftrag verwenden.
* Fordern Sie die Kommissionierung in zwei Schritten an, indem Sie zuerst den Herkunftsbeleg freigeben, die für die Logistik als ein Signal dient, dass der Herkunftsbeleg zum Kommissionieren bereitsteht.

Die Lagereinkommissionierung kann dann auf der Seite **Lagereinlagerung** erstellt werden, die auf dem Herkunftsbeleg basiert.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a><a name="to-create-an-inventory-pick-from-the-source-document"></a>Eine Lagerkommissionierung vom Herkunftsbeleg aus erstellen

1. Im Herkunftsbeleg, der ein Verkaufsauftrag, eine Einkaufsreklamation oder ein ausgehender Umlagerungsauftrag sein kann, klicken Sie auf die Aktion **Lagereinlagerung/Kommissionierung erstellen**.
2. Aktivieren Sie das Kontrollkästchen **Lagerkomm. erst.**.  
3. Wählen Sie die Schaltfläche **OK** aus. Eine neue Lagerkommissionierung wird erstellt.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a><a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Mehrere Lagerkommissionierungen mit einem Batchauftrag erstellen

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Erstelle Invt. Einlagern/Kommissionieren/Umlagern** ein, und wählen Sie dann den zugehörigen Link.  
2. Verwenden Sie im Inforegister **Erwartete Lagerbewegung** die Felder **Herkunftsbeleg** und **Herkunftsnr.**, um Filter auf bestimmte Arten von Belegen oder Bereiche von Belegnummern zu setzen. Beispielsweise können Sie Kommissionierungen nur für Verkaufsaufträge erstellen.  
3. Aktivieren Sie im Inforegister **Optionen** das Kontrollkästchen **Lagerkomm. erst.** aus.
4. Wählen Sie die Schaltfläche **OK**.

## <a name="to-create-the-pick-in-two-steps"></a><a name="to-create-the-pick-in-two-steps"></a>So erstellen Sie die Kommissionierung in zwei Schritten

### <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a><a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>So fordern Sie eine Lagerkommissionierung durch Freigabe des Herkunftsbelegs an

Bei Verkaufsaufträgen, Einkaufsreklamationen und ausgehenden Umlagerungsaufträgen erstellen Sie die erwartete Lagerbewegung, indem Sie den Auftrag freigeben. Durch die Freigabe des Auftrags werden die Artikel für die Kommissionierung verfügbar.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Verkaufsauftrag, den Sie freigeben möchten, und wählen Sie die **Freigeben** Aktion aus.

### <a name="to-create-an-inventory-pick-based-on-the-source-document"></a><a name="to-create-an-inventory-pick-based-on-the-source-document"></a>So erstellen Sie eine Lagerkommissionierung auf Grundlage des Herkunftsbelegs

Nachdem Sie einen Auftrag freigegeben haben, kann der Lagermitarbeiter eine Bestandskommissionierung erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Wählen Sie im Feld **Herkunftsbeleg** die Art des Belegs aus, auf dem die Kommissionierung basiert.  
4. Wählen Sie im Feld **Herkunftsnr.** den Herkunftsbeleg aus.  
5. Oder wählen Sie die Aktion **Herkunftsbeleg holen** aus, um eine Liste aller ausgehenden Herkunftsbelege zu erstellen, die zur Kommissionierung am Lagerort bereit sind.  
6. Wählen Sie die Schaltfläche **OK**, um die Kommissionierungszeilen gemäß den ausgewählten Herkunftsbelegen auszufüllen.  

## <a name="to-record-inventory-picks"></a><a name="to-record-inventory-picks"></a>So erfassen Sie Lagerkommissionierungen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie im Feld **Lagerplatzcode** auf den Kommissionierungszeilen wird der Lagerplatz der Kommissionierung entsprechend des Standardlagerplatzes des Artikels vorgeschlagen. Sie können – falls erforderlich – auf dieser Seite den Lagerplatz ändern.  
3. Führen Sie die Kommissionierung durch und geben Sie dann die Menge in das Feld **Bewegungsmenge** ein.

    Wenn Sie die Artikel für eine Zeile aus mehr als einem Lagerplatz kommissionieren müssen, beispielsweise, da sich die gesamte Menge nicht in dem Lagerplatz befindet, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.

4. Wählen Sie die Aktion **Buchen**.  

    * Buchen Sie den Versand der kommissionierten Herkunftsbelegzeilen.
    * Wenn der Lagerort Lagerplätze verwendet, erzeugt der Buchungsvorgang darüber hinaus Lagerplatzposten, um die Änderungen der Lagerplatzmenge zu buchen.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a><a name="handling-assemble-to-order-items-with-inventory-picks"></a>Verarbeiten von Auftragsmontageartikeln mit Lagerkommissionierungen

Sie können auch die Seite **Lagerkommissionierung** verwendet, um für Verkäufe zu kommissionieren und zu liefern, in denen Artikel montiert werden müssen, bevor sie geliefert werden können. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).

Auftragsmontageartikel sind erst dann tatsächlich in einem Lagerplatz vorhanden, wenn sie montiert und als Ausgabe für einen Lagerplatz gebucht wurden. Das Kommissionieren von Auftragsmontageartikeln aus einem Lagerplatz für Versand folgt einem speziellen Ablauf.

1. Von einem Lagerplatz bringen Lagermitarbeiter die Montageartikel zur Versandstelle und buchen dann die Lagerkommissionierung.
2. Die gebuchte Lagerkommissionierung bucht den Montageausstoß, den Komponentenverbrauch und die Verkaufslieferung.

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine automatische Lagerbestandsumlagerung zu erstellen, wenn die Lagerkommissionierung für die Montageartikel erstellt wird. Wählen Sie das Feld **Umlagerungen automatisch erstellen** auf der Seite **Montageeinrichtung** aus. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Lagerkommissionierzeilen für Verkaufsartikel werden je nachdem, ob keine, einige oder alle Verkaufspositionsmengen auf Bestellung gefertigt werden, auf unterschiedliche Weise erstellt. In Szenarien in denen ein Teil der Menge montiert und ein anderer Teil aus dem Lager kommissioniert wird, werden mindestens zwei Lagerkommissionierzeilen erstellt.

Bei Verkäufen, bei denen die gesamte Menge aus der Verkaufsauftragszeile montiert wird, wird eine Lagerkommissionierzeile für diese Menge erstellt. Der Wert im Feld **Menge für Montage** gleicht dem Wert im Feld **Zu liefern**. Das Feld **Auftragsmontage** wird in der Zeile ausgewählt.

Wenn ein Montageausgabefluss für den Lagerort eingerichtet ist, enthält das Feld **Lagerplatzcode** in der Lagerkommissionierzeile den Wert aus den folgenden Feldern in folgender Reihenfolge.

* ***LP-Code f. Prog.fert.lief.** <!-- not applicable for inv pick-->
* **Montage-Ausgangslagerplatzcode**

Wenn kein Lagerplatzcode in der Verkaufsauftragszeile angegeben wird und kein Montageausgabefluss für den Lagerort eingerichtet wird, bleibt das Feld **Lagerplatzcode** in der Lagerkommissionierzeile leer. Der Lagermitarbeiter muss die Seite **Lagerplatzinhalte** öffnen und den Lagerort auswählen, in dem die Montageartikel montiert werden.

In Szenarien in denen ein Teil der Menge zunächst montiert wird und ein anderer Teil aus dem Lager kommissioniert werden muss, werden mindestens zwei Kommissionierzeilen erstellt.

* Eine Kommissionierungszeile für die Auftragsmontagesmenge. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet die folgenden Felder in dieser Reihenfolge, um den Lagerplatzcode zu ermitteln: **Lagerplatzcode**, **Komp. Bin Code** und dann **Von-Assembly Bin Code**. Wenn diese Felder leer sind, muss der Lagermitarbeiter die Seite **Lagerplatzinhalte** öffnen und den Lagerort auswählen, in dem die Artikel montiert werden.  
* Die andere Kommissionierungszeile hängt davon ab, welche Lagerplätze die Restmenge erfüllen können. Wenn der Artikel in mehreren Lagerplätzen aufbewahrt wird, werden mehrere Zeilen erstellt. Die Entnahmezeile basiert auf der Menge im Feld **Zu liefern**.

> [!NOTE]  
> Wenn Artikel auf Bestellung montiert werden, führt die Lagerbestandskommissionierung für den verknüpften Verkaufsauftrag zu einer Lagerbestandsumlagerung für alle Montagekomponenten.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Exemplarische Vorgehensweise: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
