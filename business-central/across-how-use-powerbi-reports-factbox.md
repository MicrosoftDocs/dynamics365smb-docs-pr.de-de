---
title: Benutzerdefinierte Power BI-Berichte anzeigen | Microsoft Docs
description: Sie können Power BI-Berichte verwenden, um einen zusätzlichen Einblick in Daten in Listen zu gewinnen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 15b9f17b0b7748df977eef3837fb75122eb8d1ae
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187844"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Anzeigen von Listendaten in Power BI-Berichten in Business Central

[!INCLUDE[prodlong](includes/prodlong.md)] enthält einen Infoboxregler in mehreren Schlüssellistenseiten, die zusätzliche Einblick in die Daten in dieser Liste bereitstellen. Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert. Sie können benutzerdefinierte Berichte erstellen, aber es gibt einige Regeln, die Sie beim Erstellen der Berichte befolgen müssen, um sicherzustellen, dass das gewünschte Verhalten geliefert wird.  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI haben. Um benutzerdefinierte Berichte zu erstellen, müssen Sie diese herunterladen [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Weitere Informationen finden Sie unter [Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Bericht Dataset
Wenn Sie den Bericht in Power BI Desktop erstellen, definieren Sie die Datenquelle oder den Webdienst, der die Daten enthält, die mit der Liste verknüpft sind, der Sie den Bericht zuordnen möchten. Wenn Sie beispielsweise einen Bericht für die Verkaufs-Liste erstellen möchten, stellen Sie sicher, dass das Dataset Informationen zu den entsprechenden Verkäufen enthält.  

Um Daten in Berichten zu filtern, basierend auf dem ausgewählten Datensatz der Listenseite, muss der primäre Schlüssel als Berichtsfilter verwendet werden. Die Primärschlüssel müssen Teil des Datasets sein, um die Berichte korrekt zu filtern. In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.** Feld  

## <a name="defining-the-report-filter"></a>Definiert den Berichts-Filter
Der Bericht wird benötigt, um einen grundlegenden Berichtsfilter (keinen Seiten- oder visuellen Filter und keinen erweiterten Filter), um in der Power BI-Infobox-Steuerung korrekt zu filtern. Der Filter, der zum Power BI-Bericht von jeder Listenseite übergeben wird, basiert auf dem Primärschlüssel, wie im vorherigen Abschnitt erläutert.  

Um einen Filter für den Bericht zu definieren, wählen Sie den Primärschlüssel aus der Liste der verfügbaren Felder und ziehen dann das Feld in den Abschnitt **Berichts-Filter**.  

![Den Berichtfilter für den Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Meldet Größe und Farbe
Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden. Dies ist für die Skalierung des Berichts im verfügbaren Platz erforderlich, der von der Power BI-Infobox-Steuerung zugelassen wird. Um die Größe des Berichts zu definieren, den Fokus außerhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.

![Den Berichtfilter für die Breite und die Höhe des Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.

Wenn Sie möchten, dass der Hintergrund des Bericht sich an die Hintergrundfarbe der Power BI-Infobox-Steuerung anpasst, definieren Sie eine benutzerdefinierte Berichtshintergrundfarbe von *E5E5E5*. Diese Angabe ist optional.  

## <a name="reports-with-multiple-pages"></a>Berichte mit mehrere Seiten
Mit Power BI können Sie einen einzelnen Bericht mit mehreren Seiten erstellen. Die grafischen Elemente, die Sie in den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Listenseiten einsehen möchten, müssen auf der ersten Seite des Berichts in Power BI sein.  

> [!NOTE]  
> Die Power BI-Infobox kann nur die ersten Seite des Berichts anzeigen; wenn Sie andere Seiten anzeigen möchten, müssen Sie den Bericht erweitern und Registerkarten im unteren Bereich des Berichts verwenden, um zu anderen Seiten zu navigieren.  

## <a name="saving-your-report"></a>Ihren Bericht speichern

Wenn Sie Ihren Bericht speichern, ist es üblich, dass der Name des Berichts den Namen der Liste enthält, die Sie im Bericht anzeigen möchten. Beispielsweise muss das Wort *Kreditor* im Namen des Berichts erscheinen, die Sie auf der Kreditorenliste zur Verfügung stellen möchten.  

Dies ist keine Anforderung; es macht aber den Prozess zur Auswahl der Berichte schneller. Wenn die Berichts-Auswahlseite in einer Listenseite geöffnet ist, werden sie in einen Filter basierend auf dem Seitennamen bereitgestellt, um die Anzahl der angezeigten Bericht zu begrenzen.  Sie können den Filter entfernen, um eine vollständige Liste von Berichten zu erhalten, die in Power BI verfügbar sind.  

## <a name="troubleshooting"></a>Problembehebung
Dieser Abschnitt bietet eine Problemumgehung für die typischsten Probleme, die auftreten können, wenn Sie den Power BI-Bericht erstellen.  

**Benutzer sieht keinen Bericht auf der ausgewählten Berichtseite** Wenn Sie keinen Bericht auswählen können, ist eine mögliche Lösung, den Namen des Berichts zu prüfen, um sicherzustellen, dass es den Namen der Seite enthält. Sie können auch den Filter entfernen, um eine vollständige Liste von verfügbaren Power BI-Berichten zu erhalten.  

**Bericht wird geladen ist aber leer, nicht gefiltert oder falsch gefiltert** Prüfen Sie, dass der Berichtsfilter den korrekten Primärschlüssel enthält. In den meisten Fällen ist dies das **Nr.** Feld, aber in der Tabelle **Sachposten** beispielsweise müssen Sie das Feld **Lfd. Nr.** verwenden.

**Bericht wird gebucht, aber er zeigt die Seite an, die Sie nicht erwartet haben** Überprüfen Sie, ob die Seite, die angezeigt werden sollen, die ersten Seite in Ihren Bericht ist.  

**Bericht erscheint mit unerwünschten grauen Rändern, ist zu klein oder zu umfangreich**

Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird. Speichern Sie den Bericht, und aktualisieren Sie anschließend die Seite.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Erste Schritte](product-get-started.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
