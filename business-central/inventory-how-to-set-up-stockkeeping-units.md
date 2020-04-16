---
title: "So geht's: Eingehende Lagerhaltungseinheiten einrichten| Microsoft Docs"
description: Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 610939cb61c917d5319fc758e582c0d169d7f11b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182012"
---
# <a name="set-up-stockkeeping-units"></a>Lagerhaltungsdaten einrichten
Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.  

 Lagerhaltungsdaten sind eine Ergänzung zu Artikelkarten. Sie ersetzen sie nicht, obwohl sie mit ihnen verknüpft sind. Lagerhaltungsdaten ermöglichen Ihnen, Informationen über Artikel nach Lagerorten (wie z. B. Lagerhäuser und Vertriebsstellen) oder Varianten (wie z. B. unterschiedliche Regalnummern oder Informationen zur Wiederbestellung) zu unterscheiden.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Lagerhaltungsdaten einrichten:  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagermengeneinheiten** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie die Felder der Karte aus. Die folgenden Felder sind obligatorisch: **Artikelnr.**, **Lagerortcode** und/oder **Variantencode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nachdem Sie die ersten Lagerhaltungsdaten für einen Artikel eingerichtet haben, ist das Feld **Lagerhaltungsdaten vorhanden** auf der **Artikel**-Karte ausgewählt.  

Um mehrere Lagerhaltungsdaten für einen Artikel anzulegen, verwenden Sie die Stapelverarbeitung **Lagerhaltungsdaten erstellen**.  

> [!NOTE]  
>  Die Informationen auf der **Lagerhaltungsdatenkarte** haben eine höhere Priorität als die auf der **Artikelkarte**.

> [!Warning]
> Wenn die Lagerhaltungsdaten nach Produktion angegeben sind, wird dieses Feld **Standardkosten**nicht verwendet, wenn die Ist-Kosten des gefertigten Artikels fakturiert und reguliert werden. Stattdessen wird das Feld **Standardkosten** in der zugrunde liegenden Artikelkarte verwendet, und auftretende Abweichungen werden anhand der Kostenanteile dieses Artikels berechnet.<br /><br />
> Da Fertigungsstücklisten und Arbeitspläne nicht Lagerhaltungsdaten zugeordnet werden können, sind der Einstandspreis-Roll-up und die entsprechende Berechnung von Kosten für Lagerhaltungsdaten ebenfalls nicht verfügbar. Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
