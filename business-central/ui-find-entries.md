---
title: Einträge suchen
description: Dieser Artikel beschreibt, wie Dokumente und Posten verknüpft sind
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
ms.openlocfilehash: 3c89d9f3044a8fd0d0fa7f811f1b2f01978e4302
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532376"
---
# <a name="finding-related-entries-for-posted-documents"></a>Suchen verwandter Posten für gebuchte Belege 

In diesem Artikel erfahren Sie, wie Sie Belege und Posten finden, die miteinander verwandt sind, basierend auf gemeinsamen Informationen, wie z. B.:

- Belegnummer oder Buchungsdatum
- Geschäftskontaktart, -nummer oder externe Belegnummer
- Seriennummer oder Chargennummer des Artikels

Diese Funktion ist nützlich, wenn Sie Posten finden möchten, die aus bestimmten Transaktionen resultierten. Wenn Sie anhand von einer Belegnummer suchen, können Sie die Zusammenfassung über den Bericht „Belegposten“ ausdrucken.

## <a name="get-started"></a>Erste Schritte

Die Funktion zum Suchen von Posten ist auf fast jeder Seite über die Tastenkombination STRG+ALT+Q verfügbar. Von Seiten, die speziell gebuchte Belege oder gebuchte Belegposten anzeigen, sowohl für Listen als auch für Karten, können Sie die Funktion auch durch Auswahl der Aktion **Posten suchen** öffnen.

Die Seite **Posten suchen** enthält alle verknüpften Belege und Posten basierend auf der Belegnr. und dem Buchungsdatum. Die Seite ist in drei Abschnitte unterteilt:

- Im oberen Abschnitt werden Felder und Aktionen angezeigt, die Sie zum Filtern Ihrer Suche verwenden.
- Im mittleren Bereich werden verwandte Belege basierend auf der Suche angezeigt.
- Im unteren Abschnitt werden Informationen über den Herkunftsbeleg angezeigt, der durch die Suche gefunden wurde.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Suche nach Posten

Sie können nach Posten suchen, basierend auf Informationen entweder über den Beleg, den Geschäftskontakt oder die Artikelreferenz. Um die Suche zu ändern, wählen Sie **Aktionen**, **Suchen nach** und dann eine der folgenden Aktionen aus:

|Aktion|Beschreibung|
|------|-----------|
|Nach Beleg suchen|Zeigen Sie Posten basierend auf einer bestimmten Belegnummer oder einem bestimmten Buchungsdatum an.|
|Geschäftskontakt |Zeigen Sie Posten basierend auf einer bestimmten Kontaktart, Kontaktnummer und/oder externer Belegnummer an. Sie können Beleginformationen eingeben, die von einem Kreditor oder einem Debitor zugewiesen wurden. Verwenden Sie die verfügbaren Felder, um nach Kreditorenbelegen zu suchen, indem Sie die Nummern verwenden, die der Kreditor den Belegen zugewiesen hat.|
|Artikelreferenz|Zeigen Sie Posten basierend auf einer Seriennummer oder Chargennummer an. Sie können die Chargennummer oder Seriennummer eingeben oder nach der Chargennummer oder Seriennummer filtern, nach der Sie suchen möchten. Mithilfe dieser Aktion kann festgestellt werden, ob eine bestimmte Artikelverfolgungsnummer verwendet wurde, von welchem Kreditor sie stammt oder an welchen Debitor der Artikel verkauft wurde.|

Nachdem Sie eine Auswahl getroffen haben, geben Sie die relevanten Suchinformationen in die Felder oben ein. Verwenden Sie die QuickInfos in den Feldern zur Hilfe. Wenn Sie fertig sind, wählen Sie **Suchen**, um die Suche zu starten. Wenn Sie eine der Filter ändern, müssen Sie **Suchen** erneut wählen.

> [!TIP]
> Unter [Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md) finden Sie einige Beispiele zur Verwendung von **Posten suchen**. <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Business Central](ui-work-product.md)  
[Fügen Sie Ihrem Rollencenter eine Seitenaktion hinzu](ui-bookmarks.md)  
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
