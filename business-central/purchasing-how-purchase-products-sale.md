---
title: Einkaufs-Artikel für einen Verkauf durch das Erstellen von Einkaufsrechnungen | Microsoft Docs
description: Von einer Verkaufsrechnung um Produkte einzukaufen, können Sie eine Einkaufsrechnung für einen Kreditor oder Lieferanten einen erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1b723eaa62ef51fb6cacd42c29a4e2709a3228e6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312484"
---
# <a name="purchase-items-for-a-sale"></a>Einkauf von Artikeln für einen Verkauf
Bei Verkaufsaufträgen aus der Verkaufsrechnungen können Sie Funktionen verwenden, um für Einkaufsbelege Mengen des fehlenden Stücks schneller zu erstellen, die im Verkauf benötigt werden. Sie können zwei verschiedene Funktionen nutzen, abhängig von der Belegart, die verwendet wird.

> [!Note]
> Diese Funktionalität ist für das Füllen der Planung in Ihren eigenen Lager. Um Artikel für den Direktversand von Ihrem Kreditoren an Ihren Debitor zu kaufen, müssen Sie eine Direktlieferung erzeugen. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md)   

|Funktion|Description|
|--------|-----------|
|**Einkaufsbestellungen erstellen**|Bei einem Verkaufsauftrag erstellt diese Funktion eine Einkaufsbestellung für jeden Kreditor aus Artikeln des Verkaufsauftrags. Sie können die Abnahmemenge bearbeiten, bevor Sie die Bestellungen erstellen. Nur nicht verfügbare Verkaufsmengen werden vorgeschlagen.
|**Einkaufsrechnung erstellen**|Bei einem Verkaufsauftrag und einer Verkaufsrechnung, erstellt diese Funktion eine Einkaufsrechnung für einen ausgewählten Kreditor für alle Zeilen oder nur ausgewählte Zeilen des Verkaufsbelegs. Die verfügbare Verkaufsmenge wird vorgeschlagen.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Um eine oder mehrere Einkaufsbestellungen aus Verkaufsaufträgen zu erstellen
Um eine Bestellung für jede Artikelmenge von nichtverfügbaren Artikeln im Verkaufsauftrag zu erstellen, verwenden Sie die Funktion **Einkaufsbestellungen**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie kaufen möchten.
3. Wählen Sie die Aktion **Einkaufsbestellung erstellen**.

    Die Seite **Einkaufsbestellungen** wird geöffnet und zeigt eine Zeile für jeden anderen Artikel im Verkaufsauftrag. Zeilen für verfügbare und nicht verfügbare (abgeblendet) Verkaufsmengen werden standardmäßig angezeigt. Sie können die Funktionen **Anzeigen nicht verfügbar** Aktion auswählen, um Zeilen für nicht verfügbare Verkaufsmengen nur anzuzeigen.

    Das Feld **Einzukaufen Menge** enthält standardmäßig die nichtverfügbare Verkaufsmenge.
4. Um eine andere Menge als die nichtverfügbare Verkaufsmenge einzukaufen, ändern Sie den Wert im Feld **Einzukaufende Menge**.

    > [!NOTE]  
    >   Sie können das Feld **Einzukaufen Menge** in abgeblendeten Zeilen auch ändern, obwohl sie vollständig verfügbare Verkaufsmengen darstellen.
5. Wählen Sie die Schaltfläche **OK** aus.

    Ein Auftrag ist für jeden Kreditor der Artikel im Verkaufsauftrag, einschließlich alle Mengenänderungen erstellt, die Sie auf der Seite **Einkaufsbestellungen erstellen** durchgeführt haben.
7. Fahren Sie fort, die Einkaufsbestellungen zu verarbeiten, indem Sie beispielsweise Einkaufsbestellungszeilen bearbeiten oder hinzufügen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Eine Einkaufsrechnung aus einer Verkaufsbestellung erstellen
Eine einzelne Einkaufsrechnung für eine oder mehrere Zeilen in einem Verkaufsbeleg erstellen, indem Sie zuerst auswählen, von welchem Kreditor Sie die Funktion **Einkaufsr""echnung erstellen** verwenden.

> [!NOTE]  
>   Diese Funktion erstellt eine Einkaufsrechnung für die exakte Artikelmenge audf dem ausgewählten Verkaufsbeleg. Um die Abnahmemenge zu ändern, müssen Sie die Einkaufsrechnung bearbeiten nachdem sie erstellt wurde.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie einen Verkaufsrechnunung für Artikel, die Sie kaufen möchten.
3. Wählen Sie eine oder mehrere Rechnungszeilen aus, die Sie auf der Einkaufsrechnung verwenden möchten. Um alle Verkaufsrechnungszeilen zu verwenden, wählen Sie entweder alle oder keine Zeilen aus.
4. Wählen Sie die Aktion **Einkaufsrechnung erstellen**.
5. Wählen Sie entweder **Alle Posten** oder **Ausgewählte Posten**, und wählen Sie die **OK**-Schaltfläche.  
6. In der Kreditorenliste, die erscheint, wählen Sie den Kreditor, der die Artikel oder Dienstleistung liefert, und wählen Sie die Schaltfläche **OK**.

    Eine Einkaufsrechnung wird erstellt, die eine, mehrere oder alle Zeilen auf der Verkaufsrechnung enthält.
7. Fahren Sie fort, die Einkaufsrechnung zu verarbeiten, indem Sie beispielsweise Einkaufsrechnungszeilen bearbeiten oder hinzufügen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
