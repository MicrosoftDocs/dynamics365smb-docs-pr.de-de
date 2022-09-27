---
title: Organisieren von Elementen in Kategorien (enthält Video) | Microsoft Dokumente
description: Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.search.form: 5730, 5733, 5401
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 72a88c90de9407bfe71486022085623b8e426087
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530216"
---
# <a name="categorize-items"></a>Artikel kategorisieren

Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.

Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>So erstellen Sie eine Artikelkategorie
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Artikelkategorien** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Artikelkategorien** die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an. Weitere Informationen finden Sie unter [So ordnen Sie ein Artikelattribut einer Artikelkategorie zu](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.

> [!NOTE]  
> Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.

Wenn Sie Ihre Meinung zu einer Artikelkategorie ändern, können Sie sie löschen. Wenn sie jedoch bereits einem Artikel zugewiesen wurde, müssen Sie diese Zuweisung entfernen, bevor Sie die Artikelkategorie löschen können.

## <a name="to-assign-an-item-category-to-an-item"></a>So ordnen Sie eine Artikelkategorie einem Artikel zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.
3. Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus. Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es unter [So erstellen Sie eine Artikelkategorie](inventory-how-categorize-items.md#to-create-an-item-category) erklärt wird.

## <a name="categories-attributes-and-variants"></a>Kategorien, Attribute und Varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
