---
title: Verschaffen Sie sich einen Überblick über die Verfügbarkeit| Microsoft Docs
description: Beschreibt, wie die Verfügbarkeit der Artikel über Lagerorte, pro Verkaufs- oder Einkaufsereignisse, nach einem Zeitraum oder der Position des Artikels in einer Montagestückliste angezeigt werden kann.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: f95544f2090185512d94e9a8ce10975304f0ec2f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324246"
---
# <a name="view-the-availability-of-items"></a>Artikelverfügbarkeit anzeigen
Vom Kontext einer Geschäftsaufgabe können Sie erweiterte Informationen darüber erhalten, wann und wo ein Artikel verfügbar ist, so als ob Sie mit einem Debitoren über ein Lieferdatum sprechen.

Sie können die Verfügbarkeit aller Artikel pro Lagerplatz anzeigen, und Sie können die Verfügbarkeit jedes Artikels nach Ereignis, nach Periode oder nach Lagerplatz anzeigen. Ein Ereignis ist jede beliebige geplante Artikeltransaktion, wie beispielsweise eine Verkaufslieferung oder ein eingehender Umlagerungseingang.

> [!NOTE]  
>   Die Verfügbarkeitsansichten nach Lagerplatz erfordern, dass Sie den Lagerbestand an mehr als einem Lagerplatz verwalten. Weitere Informationen finden Sie unter [Einrichten von Lagerorten](inventory-how-setup-locations.md).

Wenn Sie die Lagerfunktion verwenden, variiert die Verfügbarkeit je nach Zuordnungen auf Lagerplatzebene, wenn Lageraktivitäten wie Kommissionierungen und Lagerplatzumlagerungen auftreten, und wenn das Bestandsreservierungssystem Einschränkungen erforderlich macht, die einzuhalten sind. Ein komplexer Algorithmus prüft, ob alle Bedingungen erfüllt sind, bevor Mengen auf Kommissionierungen für ausgehende Ströme zugewiesen werden. Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).

In [!INCLUDE[d365fin](includes/d365fin_md.md)] werden Verfügbarkeitszahlen typischerweise in zwei verschiedenen Feldern angezeigt, jedes mit einer anderen Definition:

* Das Feld **verfügbare Menge** an einigen Stellen auch **Lagerbestand** genannt, zeigt die tatsächliche aktuelle Menge entsprechend den Sachkontoeinträgen.
* Das Feld **Verfügbarkeitssaldo** wird berechnet und zeigt den Lagerbestand sowie geplante Zugänge abzüglich des Bruttobedarfs an. (In [!INCLUDE[d365fin](includes/d365fin_md.md)] enthalten geplante Belege Mengen in Bestellungen und eingehenden Umlagerungsaufträgen. Bruttobedarf enthält Mengen der Verkaufsaufträge und ausgehenden Umlagerungsaufträge.)

> [!TIP]  
>   Der Verfügbarkeitssaldo ist insbesondere relevant zum Anzeigen in den Seiten **Artikelverfügb. nach Perioden** und **Artikelverfügbarkeit nach Ereignis**, da diese die Datumsdimension enthalten.  

> [!NOTE]  
>   Die folgenden Verfahren beschreiben, wie Sie erweiterte Verfügbarkeitsinformationen von der Artikelliste und Artikelkarte anzeigen können. Sie können auch auf die Informationen von Verkaufsbelegzeilen zugreifen, für den Artikel in der Zeile. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Um die Verfügbarkeit eines Artikels anzuzeigen gemäß dem, wann er erhalten oder gesendet wird
Sie zeigen die Verfügbarkeit eines Artikels gemäß geplanter Artikeltransaktionen auf der Seite **Verfügbarkeit nach Ereignis** an.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Ereignis** aus.

    Die Seite **Artikelverfügbarkeit nach Ereignis** zeigt an, wie sich die Lagermenge des Artikels im Zeitverlauf entsprechend der geplanten Lieferungs- und Zugangsereignisse entwickelt. Die Seite bietet eine verkürzte Darstellungsform, in der eine Zeile mit kumulierten Informationen pro Zeitintervall angezeigt wird, in dem sich Lagermengen ändern. Zeitintervalle, bei denen keine Ereignisse aufgetreten sind, werden nicht angezeigt. Sie können jede Zeile erweitern, um Einzelheiten zu dem Ereignis oder den Ereignissen anzuzeigen, die die kumulierte Menge in der Zeile verursacht haben.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>So zeigen Sie die Verfügbarkeit eines Artikels in verschiedenen Perioden an
Sie zeigen die Verfügbarkeit eines Artikels im Zeitverlauf für angegebene Zeitperioden auf der Seite **Artikelverfügbarkeit nach Perioden** an.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Periode** aus.

    Die Seite **Artikelverfügbarkeit nach Perioden** zeigt an, wie die Lagermenge des Artikels sich im Zeitverlauf entwickelt, angezeigt für eine Periode, die Sie auswählen, wie beispielsweise Tag, Woche oder Quartal.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>So zeigen Sie die Verfügbarkeit eines Artikels an den Lagerplätzen an, wo er gelagert wird
Sie zeigen auf der Seite **Artikelverfügbarkeit nach Lagerort** die Verfügbarkeit eines Artikels an verschiedenen Stellen an, wo er gelagert wird.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte eines Artikels, für den Sie die Verfügbarkeit anzeigen möchten.
3. Wählen Sie die Aktion **Artikelverfügbarkeit nach** aus, und wählen Sie dann die Aktion **Lagerplatz** aus.

    Die Seite **Artikelverfügbarkeit nach Lagerort** zeigt an, wie die Lagermenge des Artikels sich zukünftig entwickelt, angezeigt für jeden Lagerplatz, an dem er gelagert wird.
4. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten anzuzeigen, aus denen sich der Wert zusammensetzt.
5. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten oder offenen Belege anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>So zeigen Sie die Verfügbarkeit aller Artikel nach Lagerplatz an, wo sie gelagert werden
Sie zeigen die Verfügbarkeit aller Ihrer Artikel über alle Lagerplätze hinweg auf der Seite **Artikel nach Lagerort** an.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Artikel nach Lagerort** aus.

    Die Seite **Artikel nach Lagerort** zeigt für alle Ihre Artikel an, wie viele an jedem Lagerplatz verfügbar sind.
3. Wählen Sie den Wert im Feld **Verfügbarkeitssaldo**, um die Artikelposten anzuzeigen, aus denen sich der Wert zusammensetzt.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Um die Verfügbarkeit eines Artikels nach dessen Verwendung in den Montage- oder Produktionsstücklisten anzuzeigen
Wenn ein Artikel Teil von Montage- oder Produktionsstücklisten, entweder als übergeordneter Artikel oder als Komponente ist, können Sie anzeigen, wie viele Einheiten davon auf der Seite **Artikelverfügbarkeit nach Stücklistenebene** erforderlich sind. Die Seite zeigt Verfügbarkeitszahlen für Stücklistenartikel an, die angeben, wie viele Einheiten eines übergeordneten Artikels Sie auf Basis der Verfügbarkeit untergeordneter Elemente erstellen können. Jeder Artikel, der eine Montage- oder Produktionsstückliste hat, wird auf der Seite als reduzierbare Zeile angezeigt. Sie können diese Zeile erweitern, um die zugrunde liegenden Komponenten und Unterbaugruppen auf niedrigeren Ebenen mit ihren eigenen Stücklisten anzuzeigen.

Sie können anhand der Seite beispielsweise ermitteln, ob Sie einen Verkaufsauftrag für einen Artikel an einem bestimmten Datum ausführen können, indem Sie seine aktuelle Verfügbarkeit und die Mengen anzeigen, die von den Komponenten geliefert werden können. Sie können die Seite auch verwenden, um Engpässe in verknüpften Stücklisten zu identifizieren.

In jeder Zeile auf der Seite für übergeordnete und untergeordnete Elemente, geben folgende Schlüsselfelder die Verfügbarkeitszahlen an. Sie können diese Zahlen für Zusagen im Hinblick darauf verwenden, wie viele Einheiten eines übergeordneten Artikels Sie liefern können, wenn Sie mit der betreffenden Montage oder Fertigung beginnen.

|Feld|Beschreibung|
|------|-----------|
|**Festlegen als übergeord. Element möglich**|Zeigt, wie viele Einheiten einer beliebigen Unterbaugruppe im obersten Artikel Sie herstellen können. Das Feld gibt an, wie viele unmittelbare übergeordnete Einheiten Sie montieren oder fertigen können. Der Wert basiert auf der Verfügbarkeit des Artikels in der Zeile.|
|**Festlegen als übergeord. Artikel möglich**|Zeigt, wie viele Einheiten des obersten Artikels Sie herstellen können. Das Feld gibt an, wie viele Einheiten des Stücklistenartikels in der ersten Zeile Sie montieren bzw. fertigen können. Der Wert basiert auf der Verfügbarkeit des Artikels in der Zeile.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>So zeigen Sie die Verfügbarkeit eines Artikels gemäß des Bedarfs am übergeordneten Artikel an
Die Seite **Artikelverfügbarkeit nach Stücklistenebene** zeigt Informationen für den Artikel in der Karte oder der Belegzeile an, für die die Seite geöffnet wird. Der Artikel wird immer in der ersten Zeile angezeigt. Sie können Informationen für andere Artikel oder für alle Artikel anzeigen, indem Sie den Wert im Feld **Artikelfilter** ändern.

> [!NOTE]  
>   Standardmäßig zeigen Verfügbarkeitszahlen in den Zeilen die Gesamtverfügbarkeit aller Artikel unter dem obersten Artikel an. Diese Zahlen werden im Feld **Verfügbare Menge** angezeigt, wobei der Fokus auf dem obersten Artikel liegt. Jedoch können Informationen darüber, wie viele Unterbaugruppen Sie herstellen können, möglicherweise falsch sein. Um eine zutreffende Angabe darüber zu erhalten, wie viele der angezeigten Unterbaugruppen Sie herstellen können, müssen Sie das Kontrollkästchen **Gesamtverfügbarkeit anzeigen** deaktivieren und dann die Zahl im Feld **Festlegen als übergeord. Artikel möglich** anzeigen.

Das Feld **Engpass** gibt an, welcher Artikel in der Stücklistenstruktur verhindert, dass eine größere Menge als die im Feld **Festlegen als übergeord. Artikel möglich** angezeigte Menge hergestellt werden kann. Beispielsweise kann der Engpass-Artikel eine eingekaufte Komponente mit einem erwarteten Lieferdatum sein, die aber zu spät eintrifft, um zusätzliche Einheiten des Artikels bis zu dem Datum im Feld **Erforderlich bis Datum** herzustellen.

## <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>So zeigen Sie die Verfügbarkeit eines Artikels anhand dessen Einheiten an
Die Seite **Artikelverfügbarkeit nach Einheit** zeigt die Verfügbarkeit eines Artikels in den Maßeinheiten an, in denen er gespeichert ist.

> [!NOTE]  
> Um diese Informationen korrekt zu halten, müssen Sie Artikeleinheiten konvertieren. Wenn Sie beispielsweise einen Artikel in einer Maßeinheit kaufen, z. B. Kisten, und Artikel in einer anderen Maßeinheit verkaufen, z. B. Teile, müssen Sie eine Buch.-Blattzeile verwenden, um die Maßeinheiten zu konvertieren, oder Artikel „auspacken“. Sie können einen Artikel Buch.-Blattzeile für einen Abgang verwenden, um den Lagerbestand in der Einkaufsmaßeinheit, z. B. Kisten, zu reduzieren, und einen Zugang, um den Lagerbestand in der Verkaufsmengeneinheit, z. B. Stück, zu erhöhen. 

## <a name="assembly-availability-page"></a>Montageverfügbarkeitsseite
Die Seite **Montageverfügbarkeit** zeigt detaillierte Verfügbarkeitsinformationen für den Montageartikel an. Es wird geöffnet:

- Automatisch aus einer Verkaufsauftragszeile in Auftragsmontageszenarien, wenn Sie eine Menge eingeben, die ein Komponentenverfügbarkeitsproblem verursacht.
- Automatisch aus einem Montagesauftragskopf, wenn Sie im Feld Menge einen Wert eingeben, der ein Komponentenverfügbarkeitsproblem verursacht.
- Manuell, wenn aus einem Montageauftrag geöffnet. Klicken Sie auf der Registerkarte Aktionen in der Gruppe Funktion auf Verfügbarkeit anzeigen.

Die Registerkarte **Details** zeigt detaillierte Verfügbarkeitsinformationen für den Montageartikel an, einschließlich wie viel der Montageauftragsmenge bis zum Fälligkeitsdatum auf der Grundlage der Verfügbarkeit der benötigten Komponenten montiert werden kann. Dies wird im Feld Montage möglich im Inforegister Details angezeigt.

Der Wert im Feld **Montage möglich** wird in roten Schrift angezeigt, wenn die Menge geringer ist, als die Menge im Feld **Restmenge**, was anzeigt, dass es nicht genügend verfügbare Komponenten gibt, um die gesamte Liefermenge zu montieren.

Die Registerkarte **Positionen** zeigt detaillierte Verfügbarkeitsinformationen für die Montagekomponenten an.

Wenn eine oder mehrere Montagekomponenten nicht verfügbar sind, wird dies im Feld **Montage möglich** der jeweiligen Zeile angezeigt, dessen Menge kleiner ist als die Menge im Feld **Restmenge** im Inforegister **Details**.

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)    
[Einrichten von Lagerorten](inventory-how-setup-locations.md)  
[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  
[Produkte verkaufen](sales-how-sell-products.md)      
[Arbeiten mit Business Central](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)
