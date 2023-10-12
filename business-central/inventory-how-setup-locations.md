---
title: Eine Standortkarte festlegen und Umlagerungsrouten definieren (enthält ein Video)
description: 'Wenn Sie Artikel an mehr als einem Ort kaufen, lagern oder verkaufen, können Sie jeden Ort als Standort einrichten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
---
# <a name="set-up-locations"></a>Einrichten von Lagerorten

Standorte sind Orte wie z.B. Lager, an denen Sie Artikel kaufen, lagern oder verkaufen. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet Standorte, um den Bestand sowohl in einfachen als auch in komplexen Lagerprozessen im Auge zu behalten.

Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lagerortkarten

Auf der Seite **Standortkarte** geben Sie Informationen über einen Standort an, z.B. ein Lager oder ein Vertriebszentrum. Sie vergeben für jeden Lagerort einen Namen und einen Code, der den Lagerort darstellt. Sie können dann den Lagerortcode auch in anderen Bereichen des Programms angeben, wenn Sie die Transaktionen für einen bestimmten Lagerort speichern möchten.  

Sie können Informationen zu Lagerplätzen und Lagerrichtlinien für jeden Lagerort eingeben. Basierend auf Ihren Lagerrichtlinien können Sie die Optionen im Inforegister **Lagerplätze** zum Angeben der standardmäßig für Transaktionen zu verwendenden Lagerplätze verwenden. Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, verwenden Sie die meisten Optionen im Inforegister **Lagerplatzrichtlinien**, um festzulegen, wie Sie die zahlreichen erweiterten Logistikfunktionen verwenden möchten.  

Einige Optionsfelder hängen von den Einstellungen auf der Seite **Standortkarte** ab, um nicht unterstützte Einrichtungskombinationen einzuschränken.  

Wählen Sie die Aktionen **Zonen** oder **Lagerplätze**, um Informationen über Zonen und Lagerplätze anzuzeigen, die für den Standort definiert sind.

### <a name="to-set-up-a-location"></a>So legen Sie einen Ort fest

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.

> [!NOTE]  
> Viele Felder auf der Seite Standortkarte stehen im Zusammenhang mit der Verarbeitung von Artikeln in eingehenden und ausgehenden Lagerprozessen. Diese Felder sind für Firmen, die keine komplexen Lagerfunktionen benötigen, nicht relevant. Weitere Informationen unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

Sie können die Konfiguration eines Standorts ändern, solange er keine Artikelposten enthält.  

Wenn Sie mehrere Standorte haben, können Sie Umlagerungsrouten zwischen den Standorten definieren. Weitere Informationen zu Übertragungsrouten finden Sie unter [So erstellen Sie eine Übertragungsroute](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>So erstellen Sie eine Umlagerungsroute

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umlagerungsrouten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
4. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern. Um mehr über Übertragungen zu erfahren, gehen Sie zu [Inventar zwischen Standorten übertragen](inventory-how-transfer-between-locations.md).

## <a name="bins"></a>Lagerplätze

Lagerplätze stellen die grundlegende Lagerstruktur dar und können vorschlagen, wo Artikel abgelegt werden sollen. Ihre Lagerplätze können Inhalt haben oder schwimmende Lagerplätze ohne bestimmten Inhalt sein.

Um die Lagerplatz-Funktionalität an einem Standort zu nutzen, aktivieren Sie die Funktionalität auf der Seite **Standortkarte**, indem Sie das Feld **Lagerplätze obligatorisch** auf dem Inforegister **Lager** auswählen. Sie können den Artikelfluss am Standort gestalten, indem Sie in den Feldern für die Lagerprozesse auf der Lagerplatzcodes in den Inforegistern **Lagerplätze** und**Lagerplatzrichtlinien** angeben.

> [!NOTE]
> Bevor Sie Lagerplätze auf einem Platz angeben können, müssen Sie Lagerplatzcodes erstellen. Weitere Informationen zu Behältern finden Sie unter [Behälter erstellen](warehouse-how-to-create-individual-bins.md) und [Ablagetypen einrichten](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zonen

Wenn Sie Ihre Lagerplätze nach Zonen strukturieren möchten, haben Sie auf der Seite **Zonen** dazu die Möglichkeit. Wenn Sie Lagerplätzen eine Zone zuweisen, kopiert [!INCLUDE [prod_short](includes/prod_short.md)] Informationen aus der Zone in die Lagerplätze. Sie können sich auch dafür entscheiden, eine Zone einzurichten und nur Lagerplätze zu verwenden, um Ihr Lager zu organisieren. Weitere Informationen zu Zonen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standarddimensionen für Standorte

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie mit verschiedenen Berichterstattungstools verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welcher Abteilung oder aus welchem Projekt ein Eintrag kommt. Die Verwendung von Standardabmessungen hilft Menschen, Fehler zu vermeiden und Abmessungen auf Transaktionsebene manuell eingeben zu müssen, wenn alle Waren von einem einzigen Standort und einer einzigen Abteilung stammen.

Sie legen Standarddimensionen für einen Standort auf der Seite **Standortkarte** fest, indem Sie **Dimensionen** auswählen. Anschließend werden den folgenden Dokumenten die Standardabmessungen des Standorts zugewiesen, wenn Sie den Standort in einer Zeile auswählen.

* Umlagerungsaufträge
* Physische Lageraufträge
* Lagerabgänge
* Lagerzugänge
* Artikel-Blätter

Bei Bedarf können Sie die Dimensionen in der Zeile löschen oder ändern. Im Feld **Wertbuchung** können Sie verlangen, dass Personen Dimensionen für bestimmte Standorte angeben, bevor sie einen Eintrag veröffentlichen können. Wenn Sie Personen erlauben möchten, nur bestimmte Dimensionswerte auszuwählen, können Sie diese im Feld **Zulässige Wertefilter** angeben. Sie können auch Standortdimensionswerte auf der Seite **Standarddimensionsprioritäten** und für Kombinationen aus Prioritäts- und Dimensionsregeln auf der Seite **Dimensionskombinationen** einbeziehen.

Da sich Transportauftragsbelege und Umgliederungserfassungen auf mehr als einen Standort beziehen, ist die Reihenfolge der Dateneingabe wichtig. Standardabmessungen werden aus dem letzten Standortfeld kopiert (der Transitstandort wird ignoriert).

### <a name="example-of-default-dimensions-on-locations"></a>Beispiel einer Standarddimensionen für Standorte

Die folgenden Beispiele veranschaulichen, wie die Standarddimension verwendet wird.

Sie haben ein Szenario mit den folgenden Dimensionseinstellungen:

* Lagerort OST. Abteilungsdimension ist ADM
* Lagerort WEST. Abteilungsdimension ist PROD

Sie geben den Standort auf einem Transportauftrag wie folgt an:

1. Von Standort = OST
2. Nach Lagerort = WEST

Die PROD-Dimension wird vom Standort WEST kopiert.

Füllen Sie die Felder in der umgekehrten Reihenfolge wie folgt aus:

1. Nach Lagerort = WEST
2. Von Standort = OST

Die ADM-Dimension wird vom Standort EAST kopiert.

## <a name="see-also"></a>Siehe auch

[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  
[Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md)  
[Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md)  
[Warehouse Management einrichten](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
