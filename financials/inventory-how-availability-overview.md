---
title: "Verschaffen Sie sich einen Überblick über die Verfügbarkeit| Microsoft Docs"
description: "Beschreibt, wie die Verfügbarkeit der Artikel über Lagerorte, pro Verkaufs- oder Einkaufsereignisse, nach einem Zeitraum oder der Position des Artikels in einer Montagestückliste angezeigt werden kann."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 83af1b6b3a234f67ccc26ee9bba7f5e3e6ff6d77
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-view-the-availability-of-items"></a>Vorgehensweise: Artikelverfügbarkeit anzeigen
Vom Kontext einer Geschäftsaufgabe können Sie erweiterte Informationen darüber erhalten, wann und wo ein Artikel verfügbar ist, so als ob Sie mit einem Kunden über ein Lieferdatum sprechen.

Sie können die Verfügbarkeit aller Artikel pro Lagerplatz anzeigen, und Sie können die Verfügbarkeit jedes Artikels nach Ereignis, nach Periode oder nach Lagerplatz anzeigen. Ein Ereignis ist jede beliebige geplante Artikeltransaktion, wie beispielsweise eine Verkaufslieferung oder ein eingehender Umlagerungseingang.

> [!NOTE]  
>   Die Verfügbarkeitsansichten nach Lagerplatz erfordern, dass Sie den Lagerbestand an mehr als einem Lagerplatz verwalten. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lagerplätzen](inventory-how-setup-locations.md).

In [Mithilfe [!INCLUDE[d365fin](includes/d365fin_md.md)] werden Verfügbarkeitszahlen in zwei verschiedenen Feldern angezeigt, jedes mit einer anderen Definition:

* Das Feld **Lagerbestand** zeigt die tatsächliche Menge heute entsprechend den Sachkontoeinträgen für gebuchte Artikel an.
* Das Feld **Verfügbarkeitssaldo** wird berechnet und zeigt den Lagerbestand sowie geplante Zugänge abzüglich des Bruttobedarfs an. (In [Mithilfe von [!INCLUDE[d365fin](includes/d365fin_md.md)] enthalten geplante Belege Mengen in Bestellungen und eingehenden Umlagerungsaufträgen. Bruttobedarf enthält Mengen der Verkaufsaufträge und ausgehenden Umlagerungsaufträge.)

> [!TIP]  
>   Der Verfügbarkeitssaldo ist insbesondere relevant zum Anzeigen in den Fenstern **Artikelverfügb. nach Perioden** und **Artikelverfügbarkeit nach Ereignis**, da diese die Datumsdimension enthalten.  

> [!NOTE]  
>   Die folgenden Verfahren beschreiben, wie Sie erweiterte Verfügbarkeitsinformationen von der Artikelliste und Artikelkarte anzeigen können. Sie können auch auf die Informationen von Verkaufsbelegzeilen zugreifen, für den Artikel in der Zeile. Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Um die Verfügbarkeit eines Artikels anzuzeigen gemäß dem, wann er erhalten oder gesendet wird
Sie zeigen die Verfügbarkeit eines Artikels gemäß geplanter Artikeltransaktionen im Fenster **Verfügbarkeit nach Ereignis** an.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Ereignis** aus.

    Das Fenster **Artikelverfügbarkeit nach Ereignis** zeigt an, wie sich die Lagermenge des Artikels im Zeitverlauf entsprechend der geplanten Lieferungs- und Zugangsereignisse entwickelt. Das Fenster bietet eine verkürzte Darstellungsform, in der eine Zeile mit kumulierten Informationen pro Zeitintervall angezeigt wird, in dem sich Lagermengen ändern. Zeitintervalle, bei denen keine Ereignisse aufgetreten sind, werden nicht angezeigt. Sie können jede Zeile erweitern, um Einzelheiten zu dem Ereignis oder den Ereignissen anzuzeigen, die die kumulierte Menge in der Zeile verursacht haben.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>So zeigen Sie die Verfügbarkeit eines Artikels in verschiedenen Perioden an
Sie zeigen die Verfügbarkeit eines Artikels im Zeitverlauf für angegebene Zeitperioden im Fenster **Artikelverfügbarkeit nach Perioden** an.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Periode** aus.

    Das Fenster **Artikelverfügbarkeit nach Perioden** zeigt an, wie die Lagermenge des Artikels sich im Zeitverlauf entwickelt, angezeigt für eine Periode, die Sie auswählen, wie beispielsweise Tag, Woche oder Quartal.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>So zeigen Sie die Verfügbarkeit eines Artikels an den Lagerplätzen an, wo er gelagert wird
Sie zeigen im Fenster **Artikelverfügbarkeit nach Lagerort** die Verfügbarkeit eines Artikels an verschiedenen Stellen an, wo er gelagert wird.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Lagerplatz** aus.

    Das Fenster **Artikelverfügbarkeit nach Lagerort** zeigt an, wie die Lagermenge des Artikels sich zukünftig entwickelt, angezeigt für jeden Lagerplatz, an dem er gelagert wird.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten anzuzeigen, aus denen sich der Wert zusammensetzt.
5. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>So zeigen Sie die Verfügbarkeit aller Artikel nach Lagerplatz an, wo sie gelagert werden
Sie zeigen die Verfügbarkeit aller Ihrer Artikel über alle Lagerplätze hinweg im Fenster **Artikel nach Lagerort** an.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Artikel nach Lagerort** aus.

    Das Fenster **Artikel nach Lagerort** zeigt für alle Ihre Artikel an, wie viele an jedem Lagerplatz verfügbar sind.
3. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-boms"></a>Um die Verfügbarkeit eines Artikels nach dessen Verwendung in den Montagestücklisten anzuzeigen
Wenn ein Artikel in den Montagestücklisten, entweder als übergeordneter Artikel oder als Komponente vorhanden ist, dann können Sie anzeigen, wie viele Einheiten davon im Fenster **Artikelverfügbarkeit nach Stücklistenebene** erforderlich sind. Das Fenster zeigt Verfügbarkeitszahlen für Stücklistenartikel an, die angeben, wie viele Einheiten eines übergeordneten Elements Sie auf Basis der Verfügbarkeit untergeordneter Elemente erstellen können. Jeder Artikel, der eine Montagestückliste hat, wird in dem Fenster als reduzierbare Zeile angezeigt. Sie können diese Zeile erweitern, um die zugrunde liegenden Komponenten und Unterbaugruppen auf niedrigeren Ebenen mit ihren eigenen Stücklisten anzuzeigen.

Sie können das Fenster verwenden, um zu ermitteln, ob Sie einen Verkaufsauftrag für einen Artikel an einem bestimmten Datum ausführen können, indem Sie seine aktuelle Verfügbarkeit und die Mengen anzeigen, die von den Komponenten geliefert werden können. Sie können das Fenster auch verwenden, um Engpässe in verknüpften Montagestücklisten zu identifizieren.

In jeder Zeile im Fenster für übergeordnete und untergeordnete Elemente, geben folgende Schlüsselfelder die Verfügbarkeitszahlen an. Sie können diese Zahlen für Zusagen im Hinblick darauf verwenden, wie viele Einheiten eines übergeordneten Artikels Sie liefern können, wenn Sie mit der betreffenden Montage oder Fertigung beginnen.

|Feld|Beschreibung|
|------|-----------|
|**Festlegen als übergeord. Element möglich**|Zeigt, wie viele Einheiten einer beliebigen Unterbaugruppe im obersten Artikel Sie herstellen können. Das Feld gibt an, wie viele unmittelbare übergeordnete Einheiten Sie montieren oder fertigen können. Der Wert basiert auf der Verfügbarkeit des Artikels in der Zeile.|
|**Festlegen als übergeord. Artikel möglich**|Zeigt, wie viele Einheiten des obersten Artikels Sie herstellen können. Das Feld gibt an, wie viele Einheiten des Stücklistenartikels in der ersten Zeile Sie montieren bzw. fertigen können. Der Wert basiert auf der Verfügbarkeit des Artikels in der Zeile.|

Das Fenster **Artikelverfügbarkeit nach Stücklistenebene** zeigt Informationen für den Artikel in der Karte oder der Belegzeile an, für die das Fenster geöffnet wird. Der Artikel wird immer in der ersten Zeile angezeigt. Sie können Informationen für andere Artikel oder für alle Artikel anzeigen, indem Sie den Wert im Feld **Artikelfilter** ändern.

> [!NOTE]  
>   Standardmäßig zeigen Verfügbarkeitszahlen in den Zeilen die Gesamtverfügbarkeit aller Artikel unter dem obersten Artikel an. Diese Zahlen werden im Feld **Verfügbare Menge** angezeigt, wobei der Fokus auf dem obersten Artikel liegt. Jedoch können Informationen darüber, wie viele Unterbaugruppen Sie herstellen können, möglicherweise falsch sein. Um eine zutreffende Angabe darüber zu erhalten, wie viele der angezeigten Unterbaugruppen Sie herstellen können, müssen Sie das Feld **Gesamtverfügbarkeit anzeigen** leeren und dann die Zahl im Feld **Festlegen als übergeord. Element möglich** betrachten.

Das Feld **Engpass** gibt an, welcher Artikel in der Stücklistenstruktur verhindert, dass eine größere Menge als die im Feld **Festlegen als übergeord. Artikel möglich** angezeigte Menge hergestellt werden kann. Beispielsweise kann der Engpass-Artikel eine eingekaufte Komponente mit einem erwarteten Lieferdatum sein, die aber zu spät eintrifft, um zusätzliche Einheiten des Artikels bis zu dem Datum im Feld **Erforderlich bis Datum** herzustellen.

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Vorgehensweise: Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)    
[So wird's gemacht: Standorte einrichten](inventory-how-setup-locations.md)  
[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  
[Gewusst wie: Produkte verkaufen](sales-how-sell-products.md)      
[Lieferkette](madeira-supply-chain.md)  
[Arbeiten mit Financials](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

