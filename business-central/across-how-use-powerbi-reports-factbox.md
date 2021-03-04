---
title: Anzeigen benutzerdefinierter Power BI-Berichte für Business Central-Daten | Microsoft Docs
description: Sie können Power BI-Berichte verwenden, um einen zusätzlichen Einblick in Daten in Listen zu gewinnen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 069efcef517cd442539f13fad5e5a2c89e1533ff
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754467"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] enthält einen Infoboxregler in mehreren Schlüssellistenseiten, der zusätzliche Einblicke in die Daten in dieser Liste bereitstellt. Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert. Sie können benutzerdefinierte Berichte erstellen, die in diesem Steuerelement angezeigt werden. Dabei sind jedoch einige Regeln zu beachten, um sicherzustellen, dass die Berichte wie erwartet funktionieren.  

## <a name="prerequisites"></a>Voraussetzungen

- Ein Power BI-Konto.
- Power BI Desktop.

Weitere Informationen zu den ersten Schritten finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle nutzen](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definieren des Berichtsdatensatzes

Geben Sie die Datenquelle an, die die Daten enthält, die sich auf die Liste beziehen. Wenn Sie beispielsweise einen Bericht für die Verkaufsübersicht erstellen möchten, stellen Sie sicher, dass der Datensatz Informationen enthält, die mit Verkäufen verknüpft sind.  

## <a name="defining-the-report-filter"></a>Definieren des Berichtsfilters

Um die Daten für den ausgewählten Datensatz in der Liste zu aktualisieren, fügen Sie dem Bericht einen Filter hinzu. Der Filter muss ein Feld der Datenquelle enthalten, die als *Primärschlüssel* verwendet wird. In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.** Feld eingetragen.

Um einen Filter für den Bericht zu definieren, wählen Sie den Primärschlüssel aus der Liste der verfügbaren Felder und ziehen dann das Feld in den Abschnitt **Berichts-Filter**. Der Filter muss ein grundlegender Berichtsfilter sein, der für alle Seiten definiert ist. Es darf sich nicht um einen Seiten-, visuellen oder erweiterten Filter handeln.

![Den Berichtfilter für den Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Festlegen von Berichtsgröße und -farbe

Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden. Diese Größe gibt die richtige Skalierung des Berichts im verfügbaren Platz des Power BI-Infoboxreglers in [!INCLUDE[prod_short](includes/prod_short.md)] an. Um die Größe des Berichts zu definieren, den Fokus außerhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.

![Den Berichtfilter für die Breite und die Höhe des Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.

Wenn Sie möchten, dass sich der Hintergrund des Bericht an die Hintergrundfarbe des Power BI-Infoboxreglers anpasst, legen Sie die Berichtshintergrundfarbe auf *#FFFFFF* fest. 

## <a name="using-reports-with-multiple-pages"></a>Verwenden von Berichten mit mehreren Seiten

Mit Power BI können Sie einen einzelnen Bericht mit mehreren Seiten erstellen. Für Berichte, die mit Listenseiten angezeigt werden, empfehlen wir jedoch nicht, dass sie mehr als eine Seite umfassen. Die Power BI-Infobox zeigt nur die erste Seite Ihres Berichts an.

## <a name="naming-the-report"></a>Benennen des Berichts

Geben Sie dem Bericht einen Namen, der den Namen der dem Bericht zugeordneten Listenseite enthält. Wenn es sich beispielsweise um einen Bericht für die Listenseite **Verkäufer** handelt, sollte der Name das Wort *Verkäufer* enthalten.  

Diese Namenskonvention ist nicht zwingend erforderlich. Sie beschleunigt jedoch das Auswählen von Berichten in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn die Seite für die Berichtsauswahls von einer Listenseite aus geöffnet wird, wird sie automatisch anhand des Seitennamens gefiltert. Diese Filterung wird durchgeführt, um die Anzahl der angezeigten Berichte zu beschränken. Benutzer können den Filter entfernen, um eine vollständige Liste der in Power BI verfügbaren Berichte zu erhalten.  

## <a name="fixing-problems"></a>Probleme beheben

Dieser Abschnitt bietet eine Problemumgehung für die gängigsten Probleme, die beim Erstellen des Power BI-Berichts auftreten können.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Ein Bericht ist auf der Seite „Bericht auswählen“ nicht sichtbar

Vermutlich enthält der Name des Berichts nicht den Namen der Listenseite. Löschen Sie den Filter, um die vollständige Liste der verfügbaren Power BI-Berichte anzuzeigen.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Der Bericht wird zwar geladen, ist jedoch leer, wird nicht gefiltert oder falsch gefiltert

Vergewissern Sie sich, dass der Berichtsfilter den richtigen Primärschlüssel enthält. In den meisten Fällen handelt es sich hierbei um das Feld **Nr.**. In der Tabelle **Sachposten** beispielsweise müssen Sie jedoch das Feld **Postennr.** verwenden.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Der Bericht wird zwar geladen, zeigt jedoch nicht die erwartete Seite an

Vergewissern Sie sich, dass die Seite, die angezeigt werden soll, die erste Seite im Bericht ist.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Der Bericht wird mit einem unerwünschten grauen Rand angezeigt, ist zu klein oder zu umfangreich

Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird. Speichern Sie den Bericht, und aktualisieren Sie anschließend die Seite.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Erste Schritte](product-get-started.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzen](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]