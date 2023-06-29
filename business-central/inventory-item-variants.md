---
title: Produktvarianten verwalten
description: 'Erfahren Sie, wie Sie nahezu identische Produkte, die sich in Farbe, Größe oder Material unterscheiden, als Artikelvarianten erfassen können.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# <a name="manage-product-variants"></a><a name="manage-product-variants"></a>Produktvarianten verwalten

Artikelvarianten sind eine großartige Möglichkeit, Ihre Produktliste unter Kontrolle zu halten. Das ist beispielsweise nützlich, wenn Sie eine große Anzahl fast identischer Artikel verwalten, die sich z. B. nur durch die Farbe unterscheiden. Sie können jede Variante als separaten Artikel definieren. Aber Sie entscheiden sich dafür, einen Artikel einzurichten und die verschiedenen Farben als Varianten des Artikels anzugeben.  

> [!TIP]
> Eine praktische Einführung in die Verwendung von Varianten in der Produktion finden Sie unter [Komplettlösung: Varianten](contoso-coffee/manufacturing/variants.md) für die Demodaten von Contoso Coffee.  

## <a name="add-variants-to-an-item"></a><a name="add-variants-to-an-item"></a>Varianten zu einem Artikel hinzufügen

Wenn sich Ihre Organisation für die Verwendung von Varianten entschieden hat, ist es ganz einfach, Varianten für einen Artikel zu definieren.  

### <a name="to-add-variants"></a><a name="to-add-variants"></a>Varianten hinzuzufügen

1. Öffnen Sie das entsprechende Artikel auf der [Seite **Artikelliste**](https://businesscentral.dynamics.com/?page=31).  
2. Auf der Seite **Artikel** wählen Sie die **Artikel** Aktion aus, und wählen Sie die **Varianten** Aktion aus.  
3. Listen Sie auf der Seite **Artikelvarianten** die Varianten auf.  

Wenn Sie dann einen Verkaufsbeleg erstellen und den Artikel hinzufügen, können Sie die Variante des Artikels im Feld **Variantencode** angeben. Gleiches gilt für Einkaufsbelege.  

## <a name="item-availability-by-variant"></a><a name="item-availability-by-variant"></a>Artikelverfügbarkeit nach Variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a><a name="require-use-of-variants"></a>Verwendung von Varianten erfordern

Ab dem Veröffentlichungszyklus 2, 2022 können Administratoren verlangen, dass Benutzer die Variante in Dokumenten und Journalen für Artikel mit Varianten angeben. Um die Funktion zu aktivieren, navigieren Sie zur Seite **Inventar einrichten**, und wählen Sie dann **Variante Obligatorisch, falls vorhanden**. Sie können diese globale Einstellung für bestimmte Elemente überschreiben.  

Auf Artikelkarten hat das Feld **Variante Obligatorisch, falls vorhanden** die folgenden Optionen:

|Feldwert |Description|
|---------|----|
|Standard| Die Einstellung von **Inventar einrichten** gilt für diesen Artikel.|
|Nein| Benutzer müssen für diesen Artikel keine Variante angeben.|
|Ja| Wenn der Artikel eine oder mehrere Varianten hat, müssen Benutzer die entsprechende Variante angeben. Wenn sie dies nicht tun, werden sie daran gehindert, die Transaktion zu buchen.|

> [!NOTE]
> Diese Einstellungen wirken sich nicht auf Artikel ohne Varianten aus.

Wenn die Funktion eingeschaltet ist, können Benutzer keinen Eintrag veröffentlichen, wenn die Variante nicht angegeben ist.

## <a name="categories-attributes-and-variants"></a><a name="categories-attributes-and-variants"></a>Kategorien, Attribute und Varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[So richten Sie allgemeine Lagerbestandsinformationen ein](inventory-how-setup-general.md)  
[Exemplarische Vorgehensweise: Varianten](contoso-coffee/manufacturing/variants.md)  
