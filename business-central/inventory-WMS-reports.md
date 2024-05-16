---
title: Bestands- und Lagerberichte und -analysen
description: 'Sehen Sie, welche Bestands- und Lagerberichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihr Unternehmen im Auge behalten können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Bestands- und Lagerberichte und -analysen

Die Bestands- und Lagerberichterstattung in [!INCLUDE [prod_short](includes/prod_short.md)] gibt Bestands- und Geschäftsfachleuten Einblicke und Statistiken über aktuelle und vergangene Bestands- und Lageraktivitäten.  

## <a name="reports"></a>Berichte

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Aufgaben

In den folgenden Artikeln werden einige der wichtigsten Aufgaben zur Analyse des Status Ihres Unternehmens beschrieben:

* [Analyseberichte erstellen](bi-how-create-analysis-views-reports.md)  
* [Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Barcodes drucken und scannen

Die Verwendung von Barcodes kann dazu beitragen, Ihre Eingangs-, Ausgangs- und internen Lagerprozesse zu optimieren. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Nachdem Sie die App installiert haben, können Sie die Aktion **Etikett drucken** verwenden, um 1D- und 2D-Barcodes von den in der folgenden Tabelle aufgeführten Seiten zu drucken.

|Seite  |Feldwerte, die Barcodes enthalten können  |
|---------|---------|
|Artikel, Artikelkarte     |Artikel-Nr., Beschreibung und GTIN         |
|Artikelreferenzliste, Artikelreferenz     |Artikel-Nr., Beschreibung, Einheit und Referenznummer         |
|Chargennr.-Informationsliste, Chargennummern-Etikett     |Artikelnummer, Beschreibung und Chargennummer       |
|Seriennummern-Etikett     |Nr., Beschreibung und Seriennummer         |

> [!NOTE]
> Manche Drucker und Barcode-/QR-Codeformate erfordern eine spezielle Implementierung. Möglicherweise müssen Sie eine andere Word-Vorlage hochladen oder den Bericht klonen, um Ihre eigene angepasste Version zu erstellen.


## <a name="explore-inventory-reports-with-report-explorer"></a>Bestandsberichte mit dem Berichts-Explorer kennenlernen

Um einen Überblick über die für den Bestand verfügbaren Berichte zu erhalten, wählen Sie auf Ihrer Homepage **Alle Berichte** aus. Dadurch öffnet sich der Rollen-Explorer, der nach den Features in der Option **Bericht und Analyse** gefiltert ist. Wählen Sie unter der Überschrift **Verkauf und Marketing** die Option **Erkunden** aus.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Beispiel zu Berichten im Finanzrollencenter." lightbox="media/report-explorer-sales.png":::

Weitere Informationen finden Sie unter [Mit dem Rollen-Explorer nach Berichten suchen](ui-role-explorer.md).


## <a name="see-also"></a>Siehe auch

[Ad-hoc-Analyse von Bestandsdaten](ad-hoc-analysis-inventory.md)  
[Übersicht über die Bestandsanalyse](inventory-analytics-overview.md)   
[Bestand einrichten](inventory-setup-inventory.md)  
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
