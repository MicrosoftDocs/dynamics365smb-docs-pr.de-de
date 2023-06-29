---
title: Wie Sie Artikel mit Lagereinlagerungen einlagern
description: 'Erfahren Sie, wie Sie Lagereinlagerungsbelege verwenden, um Datensätze und Eingangsinformationen zu erfassen und zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways"></a><a name="put-items-away-with-inventory-put-aways"></a>Artikel mit Lagereinlagerungen einlagern

In [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie Artikel und lagern sie, wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden ein.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

Dieser Artikel bezieht sich auf die Methode B in der Tabelle.

Wenn Ihr Lagerort so eingerichtet wurde, dass er Einlagerung erfordert, jedoch keinen Wareneingang, verwenden Sie den Beleg **Lagereinlagerung**, um die Wareneingangs- und Einlagerungsinformationen für Ihre Herkunftsbelege zu erfassen. Eingehende Herkunftsbelege können Einkaufsaufträge, Verkaufsreklamationen und eingehende Umlagerungsaufträge umfassen.

> [!NOTE]
> Produktions- und Montage-Ausgabe stellen auch eingehende Herkunftsbelege dar. Weitere Informationen über die Verarbeitung von Fertigungs- und Montage-Ausgabe für interne Prozesse finden Sie unter [Designdetails: Interner Lagerfluss](design-details-internal-warehouse-flows.md).

Sie können eine Lagereinlagerung auf drei Arten erstellen:  

* Erstellen Sie die Lagereinlagerung direkt vom Herkunftsbeleg aus.  
* Erstellen Sie für mehrere Herkunftsbelege gleichzeitig Lagereinlagerungen, indem Sie die eine Stapelverarbeitung verwenden.  
* Legen Sie die Einlagerung in zwei Schritten an, indem Sie zunächst den Herkunftsbeleg freigeben, um die Artikel für die Einlagerung verfügbar zu machen. Sie können die Lagereinlagerung basierend auf dem Herkunftsbeleg erstellen, indem Sie die Seite **Lagereinlagerung** verwenden.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a><a name="to-create-an-inventory-put-away-from-the-source-document"></a>Eine Lagereinlagerung vom Herkunftsbeleg aus erstellen

1. Im Herkunftsbeleg, der ein Einkaufsbestellung, eine Verkaufsreklamation oder ein eingehender Umlagerungsauftrag sein kann, klicken Sie auf die Aktion **Lagerbelege erstellen**.  
2. Aktivieren Sie das Kontrollkästchen **Lagerbelege erstellen**
3. Wählen Sie die Schaltfläche **OK** aus. Eine neue Lagereinlagerung wird erstellt.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a><a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>So erstellen Sie mehrere Lagereinlagerungen mit einer Stapelverarbeitung

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Erstelle Invt. Einlagern/Kommissionieren/Umlagern** ein, und wählen Sie dann den zugehörigen Link. 
2. Verwenden Sie im Inforegister **Erwartete Lagerbewegung** die Felder **Herkunftsbeleg** und **Herkunftsnr.**, um Filter auf bestimmte Arten von Belegen oder Bereiche von Belegnummern zu setzen. Beispielsweise können Sie Einlagerungen nur für Einkaufsaufträge erstellen.
3. Aktivieren Sie im Inforegister **Optionen** das Kontrollkästchen **Lagereinlag. erst.** aus.
4. Wählen Sie die Schaltfläche **OK**. Die angegebenen Lagereinlagerungen werden erstellt.

## <a name="to-create-the-put-away-in-two-steps"></a><a name="to-create-the-put-away-in-two-steps"></a>So erstellen Sie die Einlagerung in zwei Schritten

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a><a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>So fordern Sie eine Lagereinlagerung durch Freigabe des Herkunftsbelegs an

Wenn Sie Bestellungen, Verkaufsreklamationen und eingehende Umlagerungsaufträge freigeben, werden die Artikel auf den Bestellungen zum Einlagern verfügbar. In den folgenden Schritten wird beschrieben, wie Sie die Artikel einer Bestellung für die Einlagerung vorbereiten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Einkaufsbestellung, den Sie freigeben möchten, und wählen Sie die **Freigeben** Aktion aus.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a><a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Eine Lagereinlagerung vom Herkunftsbeleg aus erstellen

Ein Lagermitarbeiter kann basierend auf dem freigegebenen Herkunftsbeleg eine neue Lagereinlagerung erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagereinlagerungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Herkunftsbeleg** die Art des Herkunftsbelegs aus, auf dem die Einlagerung basiert.  
4. Wählen Sie im Feld **Herkunftsnr.** den Herkunftsbeleg aus.  
5. Oder wählen Sie die Aktion **Herkunftsbeleg holen** aus, um den Beleg aus einer Liste von eingehenden Herkunftsbelegen auszuwählen, die zur Einlagerung am Lagerort bereit sind.  
6. Wählen Sie die Schaltfläche **OK**, um die Einlagerungszeilen gemäß dem ausgewählten Herkunftsbeleg auszufüllen.  

## <a name="to-record-the-inventory-put-away"></a><a name="to-record-the-inventory-put-away"></a>So erfassen Sie die Lagereinlagerung

1. Öffnen Sie auf der Seite **Lagereinlagerungen** einen zuvor erstellten Einlagerungsbeleg.  
2. Im Feld **Lagerplatzcode** auf den Einlagerungszeilen werden der Lagerplätze, in die die Arikel eingelagert werden müssen, bnasiernd auf dem Standardlagerplatzes des Artikels vorgeschlagen. Sie können den Lagerplatz bei Bedarf ändern.  
3. Führen Sie die Einlagerung durch und geben Sie dann im Feld **Bewegungsmenge** die tatsächlich eingelagerte Menge ein.

    Wenn Sie die Artikel für eine Zeile in mehr als einem Lagerplatz platzieren müssen, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.  
4. Nachdem Sie die Artikel eingelagert haben, wählen Sie die **Buchen**-Aktion aus.  

    * Buchen Sie den Wareneingang der eingelagerten Herkunftsbelegen
    * Wenn der Lagerort Lagerplätze verwendet, erzeugt der Buchungsvorgang darüber hinaus Lagerplatzposten, um die Mengenänderungen in den Lagerplätzen zu buchen.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/receive-put-away-items/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
