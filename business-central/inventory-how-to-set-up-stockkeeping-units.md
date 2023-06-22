---
title: Wie Sie Lagerhaltungsdaten-Einheiten festlegen
description: 'Verwenden sie Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerort oder eine bestimmte Variante zu speichern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
---

# <a name="set-up-stockkeeping-units" />Lagerhaltungseinheiten einrichten

Verwenden Sie Lagerhaltungsdaten (SKU), um Informationen zu Artikeln für einen bestimmten Lagerplatz oder eine Variante zu erfassen. Sie ermöglichen es Ihnen, verschiedene Informationen zu einem Artikel für einen bestimmten Lagerplatz hinzuzufügen, zum Beispiel:

* Ein Lager oder Verteilungszentrum
* Varianten, wie z. B. unterschiedliche Regalnummern und unterschiedliche Wiederbeschaffungsinformationen, für denselben Artikel  

## <a name="to-set-up-a-stockkeeping-unit" />Lagerhaltungsdaten einrichten:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerhaltungseinheiten** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Füllen Sie die Felder nach Bedarf aus. Die folgenden Felder sind obligatorisch: **Artikelnr.**, **Lagerortcode** und/oder **Variantencode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nachdem Sie die ersten Lagerhaltungsdaten für einen Artikel eingerichtet haben, ist das Kontrollkästchen **Lagerhaltungsdaten vorhanden** auf der **Artikel**-Karte ausgewählt.  

Um mehrere Lagerhaltungsdaten für einen Artikel anzulegen, verwenden Sie die Stapelverarbeitung **Lagerhaltungsdaten erstellen**. Mehr Informationen über Stapelverarbeitungsaufträge erhalten Sie unter [Verwenden Sie Aufgabenwarteschlangen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Die Informationen auf der **Lagerhaltungsdatenkarte** haben eine höhere Priorität als die auf der **Artikelkarte**.

> [!Warning]
> Wenn die Lagerhaltungsdaten nach Produktion angegeben sind, wird dieses Feld **Standardkosten** nicht verwendet, wenn die Ist-Kosten des gefertigten Artikels fakturiert und reguliert werden. Stattdessen verwendet [!INCLUDE [prod_short](includes/prod_short.md)] den Wert im Feld **Standardkosten** in der zugrunde liegenden Artikelkarte, und auftretende Abweichungen werden anhand der Kostenanteile dieses Artikels berechnet.<br><br>
> Obwohl Sie SKUs Fertigungsstücklisten und Arbeitsplänen zuweisen können, sind der Einstandspreis-Roll-up und die entsprechende Berechnung von Kosten für SKUs sind nicht verfügbar. Weitere Informationen zu den Standardkosten finden Sie unter [Informationen zur Berechnung der Standardkosten](finance-about-calculating-standard-cost.md)

## <a name="see-related-microsoft-trainingtrainingmodulescontrol-inventory-multiple-locations" />Siehe verwandte [Microsoft Schulungen](/training/modules/control-inventory-multiple-locations/)

## <a name="see-also" />Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Montageverwaltung](assembly-assemble-items.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
