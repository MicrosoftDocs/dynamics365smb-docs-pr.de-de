---
title: Erzeugen von Produktionsaufträgen aus Verkaufsaufträgen
description: 'Lernen Sie verschiedene Möglichkeiten kennen, Produktionsaufträge für produzierte Artikel direkt aus Verkaufsaufträgen zu erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
ms.service: dynamics-365-business-central
---
# Erzeugen von Produktionsaufträgen aus Verkaufsaufträgen

In diesem Fenster können Sie direkt zum aktuellen Verkaufsauftrag einen Fertigungsauftrag erstellen.  

## Fertigungsaufträge aus Verkaufsaufträgen erstellen  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Verkaufsauftrag, für den Sie einen Fertigungsauftrag erstellen möchten.  
3. Wählen Sie die Aktion **Planung** aus. Die Seite **Verkaufsauftragsplanung** zeigt die Verfügbarkeit des Artikels.  
4. Wählen Sie die Aktion **Produktionsauftrag erstellen** aus.  
5. Wählen Sie den Status und die Auftragsart aus.  
6. Wählen Sie die Schaltfläche **Ja** aus, um einen oder mehrere Produktionsaufträge für die Zeilen zu erstellen, die **Fertigungsauftrag** im Feld **Beschaffungsmethode** haben.

    > [!NOTE]  
    > Bedarfszeilen, die **Prod. Auftrag** im Feld **Beschaffungsmethode** haben, stellen zugrunde liegende Fertigungsaufträge dar. Nachdem Sie diese Produktionsaufträge generiert haben, denken Sie daran, alle nicht erfüllten Komponentenanforderungen für sie zu identifizieren. Verwenden Sie die Seite **Auftragsplanung** oder die Aktion **Neu planen**, um unerfüllten Bedarf zu identifizieren.
    >
    > Wenn Sie Produktionsaufträge für Verkaufsaufträge mit der Seite Verkaufsauftragsplanung erstellen, werden Auftrag-zu-Auftrag-Verknüpfungen zwischen Nachfrage und Lieferung angewendet. Wenn Auftrag-zuAuftrag-Verknüpfungen vorhanden sind, umfasst das Planungssystem keinen verknüpften Lagerbestand in das Ausgleichsverfahren. Weitere Informationen zum Ausgleich finden Sie unter [Auftrag-zu-Auftrag-Verknüpfungen](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## Auftragsart  

In der folgenden Tabelle werden zwei Möglichkeiten zum Erstellen von Produktionsaufträgen beschrieben.

|Option|Beschreibung|
|------|-----------|
|Artikelauftrag|Ein Fertigungsauftrag wird für jeden Artikel erstellt, der durch eine Zeile auf der Seite **Verkaufsauftragsplanung** angegeben wird.|
|Projektauftrag|Ein Fertigungsauftrag mit mehreren Zeilen wird für alle Artikel erstellt, die durch Zeilen auf der Seite **Verkaufsauftragsplanung** angegeben werden. Wenn Sie Projektaufträge verwenden, enthält das Feld **Quellentyp** des Produktionsauftrags **Verkaufskopf**. Der Auftrag hat eine Zeile für jeden Artikel des Verkaufsauftrags, der produziert werden muss.|

## Weitere Informationen  

[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
