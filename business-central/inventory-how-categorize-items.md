---
title: Kategorisieren Sie Artikel| Microsoft Docs
description: Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3959392048f4c130e6564160f9b2c6f5956ece8c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746241"
---
# <a name="categorize-items"></a>Artikel kategorisieren

Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.

Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>So erstellen Sie eine Artikelkategorie
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikelkategorien** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Artikelkategorien** die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an. Weitere Informationen finden Sie unter [So ordnen Sie ein Artikelattribut einer Artikelkategorie zu](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.

> [!NOTE]  
> Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.

Wenn Sie Ihre Meinung zu einer Artikelkategorie ändern, können Sie sie löschen. Wenn sie jedoch bereits einem Artikel zugewiesen wurde, müssen Sie diese Zuweisung entfernen, bevor Sie die Artikelkategorie löschen können.

## <a name="to-assign-an-item-category-to-an-item"></a>So ordnen Sie eine Artikelkategorie einem Artikel zu

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.
3. Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus. Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es unter [So erstellen Sie eine Artikelkategorie](inventory-how-categorize-items.md#to-create-an-item-category) erklärt wird.

## <a name="categories-attributes-and-variants"></a>Kategorien, Attribute und Varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
