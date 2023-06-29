---
title: Artikel montieren
description: Erfahren Sie mehr über Programmfertigung und Lagerfertigung in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items"></a><a name="assemble-items"></a>Artikel montieren

Wenn das Feld **Wiederbeschaffungssystem** auf der Artikelkarte den Wert **Montage** enthält, wird der Artikel standardmäßig gemäß einer Stückliste für die Montage und möglicherweise durch eine bestimmte Ressource bereitgestellt. Erfahren Sie mehr unter [Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md). Erfahren Sie mehr darüber, wie Sie ein Element für die Montage festlegen unter [Montage auf Bestellung und Montage auf Lager](assembly-assemble-to-order-or-assemble-to-stock.md).

Sie können Montageelemente für zwei Montageprozesse festlegen.

|Prozess  |Description  |
|---------|---------|
|Auf Lager montieren     | Elemente, die Sie für zukünftige Verkäufe montieren und auf Lager halten. Zum Beispiel Bausätze für eine bevorstehende Verkaufskampagne. Die Elemente sind nicht mit einem Verkaufsauftrag verknüpft, zumindest noch nicht. In der Regel sind diese Elemente nicht an Kundenwünsche angepasst.        |
|Montage auf Bestellung     | Elemente, die Sie nicht auf Lager haben möchten. Zum Beispiel, weil sie auf der Grundlage von Kundenbestellungen angepasst werden oder um die Kalkulation des Lagerbestands zu reduzieren. |
  
Dieser Artikel beschreibt die Standardeinstellungen für die Montage auf Lager. Vielleicht gibt es aber auch andere Möglichkeiten, die für Ihr Unternehmen besser geeignet sind. Erfahren Sie mehr unter [Verkauf von Lagerartikeln in Programmfertigungs Flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) und [Verkauf von Programmfertigungs- und Bestandsartikeln zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Montagekomponenten werden auf eine spezielle Art in den Basislagerkonfigurationen behandelt. Erfahren Sie mehr unter [Verarbeitung von Programmfertigung mit kommissionierten Bestandsartikeln](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock"></a><a name="to-assemble-an-item-to-stock"></a>So montieren Sie ein Element für den Bestand

Folgen Sie den Schritten in diesem Verfahren, um ein Element auf Lager zu montieren. Weitere Informationen zur Programmfertigung finden Sie unter [Verkauf von Elementen, die auf Bestellung gefertigt wurden](assembly-how-to-sell-items-assembled-to-order.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Montageaufträge** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus. Die Seite **Neuer Montageauftrag** wird geöffnet.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie im Feld **Element-Nr.** den Artikel aus, den Sie montieren möchten. Sie können Elemente auswählen, die für die Montage festgelegt sind und über eine Stückliste für die Montage verfügen, oder Elemente ohne eine Stückliste für die Montage. Letzteres ist nützlich für ungeplante Montagen oder Szenarien, in denen Sie die Umgliederung von Elementen verwenden und die Kosten verfolgen möchten.  
5. Geben Sie im Feld **Menge** ein wie viele Einheiten des Artikels Sie montieren möchten.  

    > [!NOTE]  
    >  Wenn eine oder mehrere Komponenten nicht verfügbar sind, um die Menge zum Fälligkeitsdatum zu erfüllen, öffnet sich die Seite **Montageverfügbarkeit**. Die Seite zeigt an, wie viele Montageelemente je nach Verfügbarkeit der Komponenten montiert werden können. Weitere Informationen finden Sie unter [Ansicht der Verfügbarkeit von Elementen](inventory-how-availability-overview.md). Wenn Sie die Seite schließen, wird der Montageauftrag erstellt, mit Verfügbarkeitswarnungen in den Zeilen für die betroffenen Komponenten.  

    Die Zeilen enthalten den Inhalt der Stückliste der Montage und die angegebenen Mengen.  

    > [!NOTE]  
    >  Wenn die Seite **Verfügbarkeit von Baugruppen** geöffnet wurde, als Sie den Kopf des Montageauftrags ausfüllten, enthält jede betroffene Zeile des Montageauftrags eine **Ja** im Feld **Verfügbar. Warnung** mit einem Link zu detaillierten Verfügbarkeitsinformationen. <!--check whether this field help is useful For more information, see Check Availability.--> Sie können ein Problem mit der Komponentenverfügbarkeit beheben, indem Sie:

    > * Verschieben Sie das Startdatum.
    > * Ersetzen Sie die Komponente durch ein anderes Element.
    > * Eine verfügbare Substitution auswählen, wenn eine solche definiert ist.  

6. Geben Sie in das Feld **Zu montierende Menge** ein, wie viele Einheiten des Montageartikels Sie beim nächsten POST des Montageauftrags als Ausgabe buchen möchten. Diese Menge kann unter dem Wert im Feld **Menge** liegen, um eine Teilbuchung anzuzeigen.  

    > [!NOTE]  
    >  Um sicherzustellen, dass die Buchung des Komponentenverbrauchs der Istmeldungsbuchung des Montageartikels entspricht, werden die Mengenfelder in den Montageauftragszeilen automatisch an den Wert angepasst, den Sie im Feld **Menge für Montage** eingeben.  
7. Geben Sie in Montageauftragszeilen vom Typ **Artikel** oder **Ressource** im Feld **Verbrauchsmenge** ein, wie viele Einheiten Sie als Verbrauch buchen möchten, wenn Sie den Montageauftrag das nächste Mal buchen.
8. Wenn Sie bereit sind, die Teil- oder die vollständige Buchung durchzuführen, wählen Sie die Aktion **Buchen**.  

    > [!NOTE]  
    >  Wenn in den Zeilen des Montageauftrags noch Warnungen vorhanden sind, können Sie den Auftrag nicht buchen. Eine Nachricht zeigt die Komponente(n) an, die sich nicht im Bestand befinden.  

Nach erfolgreicher Buchung wird der Montageartikel als Ausstoß für den Lagerortcode und den potenziellen Lagerplatzcode gebucht, die im Montageauftrag definiert sind. Für manuell erstellte Montageaufträge wird der Lagerplatz möglicherweise aus dem Einrichtungsfeld **Standardlagerort für Aufträge** kopiert. Für Auftragsmontageflüsse wird der Lagerortcode möglicherweise aus der Verkaufsauftragszeile kopiert.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe zugehörige [Microsoft Schulungen](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
