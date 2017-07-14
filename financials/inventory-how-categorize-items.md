---
title: 'Vorgehensweise: Kategorisieren Sie Artikel| Microsoft Docs'
description: Beschreibt, wie man Artikel in Kategorien organisiert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 06f50a356ddc3a501c28fe34891213b55a12e3fd
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Artikel kategorisieren
<a id="how-to-categorize-items" class="xliff"></a>
Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.

Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen. Weitere Informationen finden Sie unter [So geht's: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).

## So erstellen Sie eine Artikelkategorie
<a id="to-create-an-item-category" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Artikel kategorisieren** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Fenster **Artikelkategorie** die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an. Weitere Informationen finden Sie im Abschnitt "So weisen Sie Artikelattribute Artikelkategorien zu" in [So geht's: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).

**Hinweis**: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.

**Hinweis**: Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.

## So ordnen Sie eine Artikelkategorie einem Artikel zu
<a id="to-assign-an-item-category-to-an-item" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.
3. Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus. Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es im Abschnitt "So erstellen Sie eine Artikelkategorie" erklärt wird.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Gewusst wie: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Vorgehensweise: Einen neuen Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

