---
title: Angepasste Power BI-Berichte anzeigen
description: 'Sie können die Power BI-FactBox verwenden, um Power BI-Berichte anzuzeigen und zusätzliche Einblicke in die Datensätze in Schlüssellisten zu erhalten.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/11/2021
ms.author: jswymer
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-"></a>Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] umfasst ein Power BI-Infobox-Steuerelement auf mehreren Schlüssellistenseiten. Der Zweck dieser Infobox ist die Anzeige von Power BI-Berichten, die sich auf Datensätze in den Listen beziehen und zusätzlichen Einblick in die Daten bieten. Die Idee ist, dass, wenn Sie sich zwischen den Zeilen in der Liste bewegen, der Bericht für den ausgewählten Eintrag aktualisiert wird.

[!INCLUDE[prod_long](includes/prod_long.md)] kommt mit einigen dieser Berichte. Sie können auch eigene benutzerdefinierte Berichte erstellen, die in dieser Infobox angezeigt werden. Das Erstellen dieser Berichte ähnelt anderen Berichten. Es gibt jedoch einige Entwurfsregeln, die Sie befolgen müssen, um sicherzustellen, dass die Berichte wie erwartet angezeigt werden. Diese Regeln werden in diesem Artikel erläutert.

> [!NOTE]
> Allgemeine Informationen zum Erstellen und Veröffentlichen von Power BI-Berichten für Business Central finden Sie unter [Power BI-Berichte zum Anzeigen erstellen [!INCLUDE [prod_long](includes/prod_long.md)]-Daten](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Voraussetzungen

- Ein Power BI-Konto.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Einen Bericht für eine Listenseite erstellen

1. Starten Sie Power BI Desktop.
2. Wählen Sie **Daten abrufen** aus, und beginnen Sie mit der Auswahl der Datenquelle für den Bericht.

    Geben Sie die Business Central-Listenseiten an, die die Daten enthalten, die Sie im Bericht haben wollen. Um z.B. einen Bericht für die Liste **Verkaufsrechnungen** zu erstellen, schließen Sie die Seiten ein, die sich auf den Verkauf beziehen.

    Weitere Informationen finden Sie in den Anweisungen [[!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop hinzufügen](across-how-use-financials-data-source-powerbi.md#getdata).

3. Definieren Sie den Berichtsfilter.

    Um die Daten für den ausgewählten Datensatz in der Liste zu aktualisieren, fügen Sie dem Bericht einen Filter hinzu. Der Filter muss ein Feld der Datenquelle enthalten, mit dem jeder Datensatz in der Liste eindeutig identifiziert wird. In Bezug auf Entwickler ist dieses Feld der *Primärschlüssel*. In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.** Feld eingetragen.

    Führen Sie die folgenden Schritte aus, um den Filter einzustellen:

    1. Wählen Sie unter **Filter** das Primärschlüsselfeld aus der Liste der verfügbaren Felder aus.
    2. Ziehen Sie den Bereich **Filter** und legen Sie ihn in der Box **Filter auf allen Seiten** ab.
    3. Stellen Sie den **Filtertyp** auf **Grundfilterung**. Es darf sich nicht um einen Seiten-, visuellen oder erweiterten Filter handeln.

    ![Festlegen des Berichtsfilters für den Bericht „Verkaufsrechnungen Aktivitäten“.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Entwerfen Sie den Berichtslayout.

    Erstellen Sie das Layout, indem Sie Felder ziehen und Visualisierungen hinzufügen. Weitere Informationen finden Sie unter [Mit der Berichtsansicht in Power BI Desktop arbeiten](/power-bi/create-reports/desktop-report-view) in der Power BI-Dokumentation.

5. In den nächsten Abschnitten erfahren Sie, wie Sie die Größe des Berichts ändern und mehrere Seiten verwenden.

6. Speichern und benennen Sie den Bericht.

    Geben Sie dem Bericht einen Namen, der den Namen der mit dem Bericht verknüpften Listenseite enthält, wie er im Client steht. Bei dem Namen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Angenommen, der Bericht ist für die Listenseite **Verkaufsrechnungen**. In diesem Fall fügen Sie die Wörter **Verkaufsrechnungen** irgendwo im Namen ein, z. B. **Meine Verkaufsrechnungen.pbix** oder **Meine_Verkaufsrechnungen_liste.pbix**.

    Diese Namenskonvention ist nicht zwingend erforderlich. Sie beschleunigt jedoch das Auswählen von Berichten in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn die Berichtauswahlseite von einer Listenseite aus geöffnet wird, wird automatisch ein Filter auf der Basis des Seitennamens angewendet. Der Filter hat die Syntax: `@*<caption>*`, wie `@*Sales Invoices*`. Diese Filterung wird durchgeführt, um die Anzahl der angezeigten Berichte zu beschränken. Benutzer können den Filter entfernen, um eine vollständige Liste der in Power BI verfügbaren Berichte zu erhalten.

7. Wenn Sie fertig sind, veröffentlichen Sie den Bericht wie gewohnt.

    Weitere Informationen finden Sie unter [Veröffentlichen eines Berichts](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Testen Sie den Bericht.

    Sobald der Bericht in Ihrem Arbeitsbereich veröffentlicht wurde, sollte er in der FactBox Power BI auf der Listenseite in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sein.

    Führen Sie die folgenden Schritte aus, um es zu testen.

    1. Öffnen Sie [!INCLUDE[prod_short](includes/prod_short.md)], und gehen Sie zur Listenseite.
    2. Wenn Sie die Power BI-Infobox nicht sehen, wechseln Sie zur Aktionsleiste und wählen Sie **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus.
    3. Wählen Sie in der Power BI-Infobox **Berichte auswählen**, dann das Feld **Aktivieren** für den Bericht und **OK** aus.

    Bei korrekter Gestaltung wird der Bericht angezeigt.  

## <a name="set-the-report-size-and-color"></a>Berichtsgröße und ‑farbe festlegen

Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden. Diese Größe gibt die richtige Skalierung des Berichts im verfügbaren Platz des Power BI-Infoboxreglers in [!INCLUDE[prod_short](includes/prod_short.md)] an. Um die Größe des Berichts zu definieren, den Fokus außerhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.

![Festlegen der Berichtsbreite und -höhe für den Bericht „Verkaufsrechnungen Aktivität“.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.

Wenn Sie möchten, dass sich der Hintergrund des Bericht an die Hintergrundfarbe des Power BI-Infoboxreglers anpasst, legen Sie die Berichtshintergrundfarbe auf *#FFFFFF* (weiß) fest. 

> [!TIP]
> Verwenden Sie die [!INCLUDE [prod_short](includes/prod_short.md)]-Themendatei zum Erstellen von Berichten mit dem gleichen Farbstil wie die [!INCLUDE [prod_short](includes/prod_short.md)]-Apps. Weitere Informationen finden Sie unter [[!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema verwenden](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Berichte mit mehrere Seiten

Mit Power BI können Sie einen einzelnen Bericht mit mehreren Seiten erstellen. Für Berichte, die mit Listenseiten angezeigt werden sollen, empfehlen wir jedoch, dass sie nicht mehr als eine Seite haben. Die Power BI-Infobox zeigt nur die erste Seite Ihres Berichts an.

## <a name="fixing-problems"></a>Probleme beheben

In diesem Abschnitt wird erklärt, wie Sie Probleme beheben können, die auftreten können, wenn Sie versuchen, einen Power BI-Bericht für eine Listenseite in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen.  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>Sie können die Power BI-Infobox auf einer Listenseite nicht sehen

Standardmäßig ist die Power BI-Infobox nicht sichtbar. Um die Infobox auf einer Seite anzuzeigen, wählen Sie in der Aktionsleiste **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>Sie können den Bericht im Abschnitt „Bericht auswählen“ nicht sehen

Der Name des Berichts enthält nicht den Namen der Listenseite, die angezeigt wird. Löschen Sie den Filter, um die vollständige Liste der verfügbaren Power BI-Berichte anzuzeigen.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Der Bericht wird zwar geladen, ist jedoch leer, wird nicht gefiltert oder falsch gefiltert

Stellen Sie sicher, dass der Berichtsfilter den richtigen Primärschlüssel enthält. In den meisten Fällen handelt es sich hierbei um das Feld **Nr.**. In der Tabelle **Sachposten** beispielsweise müssen Sie jedoch das Feld **Postennr.** verwenden.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Der Bericht wird zwar geladen, zeigt jedoch nicht die erwartete Seite an

Vergewissern Sie sich, dass die Seite, die angezeigt werden soll, die erste Seite im Bericht ist.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Der Bericht wird mit einem unerwünschten grauen Rand angezeigt, ist zu klein oder zu umfangreich

Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird. Speichern Sie den Bericht, und aktualisieren Sie anschließend die Seite.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle verwenden](across-how-use-financials-data-source-powerbi.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzen](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
