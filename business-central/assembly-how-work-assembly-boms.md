---
title: Arbeiten mit Montage-Stücklisten
description: 'Sie erstellen eine Montagestückliste, um die Komponenten anzugeben, die für den Zusammenbau des Elements, das die Stückliste darstellt, erforderlich sind.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 09/26/2022
ms.author: edupont
---
# <a name="work-with-assembly-boms" />Arbeiten mit Montage-Stücklisten

Sie verwenden Montagestücklisten, um übergeordnete Elemente zu strukturieren, die aus Komponenten mit geringem oder gar keinem Ressourceneinsatz zusammengesetzt werden müssen. Eine Montagestückliste kann z.B. dazu verwendet werden, ein übergeordnetes Element als Bausatz zu verkaufen, der aus Komponenten besteht.

Montageaufträge werden für die Produktion von Endartikeln aus Komponenten in einem einfachen Prozess verwendet, der mit einer oder mehreren grundlegenden Ressourcen, die keine Maschinen oder Arbeitsplatzgruppen sind, oder ganz ohne Ressourcen durchgeführt werden kann. Beispielsweise könnte ein Montagevorgang lauten, zwei Weinflaschen und ein Paket Kaffee zu kommissionieren und sie als Geschenkartikel zu verpacken.  

Eine Montagestückliste liefert die Masterdaten, die festlegen, welche Komponentenartikel in einen montierten Endartikel enthalten sind und welche Ressourcen verwendet werden, um den Montageartikel zu montieren. Wenn Sie im Kopf eines neuen Montageauftrags den Montageartikel und die Menge eingeben, werden die Montageauftragszeilen automatisch aus der Montagestückliste übernommen und pro Komponente oder Ressource als eine Montageauftragszeile dargestellt. Erfahren Sie mehr unter [Montage Management](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt auch Fertigungsstücklisten. Fertigungsstücklisten unterscheiden sich von Montagestücklisten dadurch, dass sie komplexere Verfahren beinhalten, einschließlich der Ressourcennutzung, des Produktionsroutings und der Arbeits- oder Maschinenzentren. Erfahren Sie mehr über die Unterschiede unter [Arbeiten mit Stücklisten](inventory-how-work-BOMs.md) und [Erstellen von Fertigungsstücklisten](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom" />So erstellen Sie eine Montagestückliste

Um einen übergeordneten Artikel zu definieren, der aus anderen Artikeln und möglicherweise Ressourcen besteht die benötigt werden, um die übergeordnete Baugruppe zusammenzufügen, müssen Sie eine Montagestückliste erstellen.  

Montagestücklisten enthalten normalerweise Artikel, können jedoch auch eine oder mehrere Ressourcen enthalten, die die Montageartikel ausführen.

Montagestücklisten können mehrstufig sein, was bedeutet, dass eine Komponente in der Montagestückliste selbst ein Montageartikel sein kann. In diesem Fall lautet das Feld **Montagestückliste** in der Montagestücklistenzeile **Ja**.

Für Elemente auf Stücklisten für die Montage gelten besondere Anforderungen an die Verfügbarkeit. Erfahren Sie mehr unter [Die Verfügbarkeit eines Elements anhand seiner Verwendung in Stücklisten für die Montage anzeigen](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Es gibt zwei Schritte zum Erstellen einer Montagestückliste:

- Einrichten einer neuen Artikelkarte
- Gibt die Beschreibung des Montageartikels an.

1. Richten Sie einen neuen Artikel ein. Erfahren Sie mehr unter [Registrieren Sie neue Artikel](inventory-how-register-new-items.md).

   Fahren Sie fort, um Komponenten oder Ressourcen in der Montagestückliste einzugeben.  
2. Wählen Sie auf der Seite **Artikelkarte** für einen Montageartikel die Aktion **Montage** und dann die Aktion **Montagestückliste**.
3. Füllen Sie auf der Seite **Montagestückliste** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Für Montage-Elemente können Sie wie für jedes andere Element verschiedene Varianten auf [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, damit die Liste der verfügbaren Produkte kürzer bleibt. Erfahren Sie mehr über diese Funktion unter [Produktvarianten verwalten](inventory-item-variants.md).

## <a name="to-edit-assembly-boms" />So bearbeiten Sie Montagestücklisten

Sie können die Zeilen in einer Montagestückliste jederzeit bearbeiten. Beachten Sie jedoch, dass die Stückliste möglicherweise bei laufenden Verkäufen oder Baugruppen des übergeordneten Unternehmens verwendet wird, die von der Änderung betroffen sein können. Wählen Sie das die Aktion **Artikelverwendungsübersicht** aus, um zu sehen, in welchen Artikeln es verwendet wird und dann ob Verkaufs- oder Montageaufträge betroffen sein können.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Wert **Ja** in der Spalte **Montagestückliste** aus.
3. Wählen Sie auf der Seite **Montagestückliste** die Aktion **Liste bearbeiten** und ändern Sie dann ein beliebiges Feld nach Bedarf.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure" />So werden Komponenten und Ressourcen angezeigt, eingerückt gemäß der Stücklistenstruktur

Auf der Seite **Montagestückliste** können Sie ein separates Fenster öffnen, in dem die Komponenten sowie jegliche Ressourcen angezeigt werden, die gemäß ihrer Stücklistenposition unter den Montageartikel eingerückt werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für ein Element der Montage. (Das Feld **Montagestückliste** auf der Seite **Positionen** enthält **Ja**.)
3. Wählen Sie auf der Seite **Elementkarte** die Aktion **Montage** und dann die Aktion **Montagestückliste**.
4. Wählen Sie auf der Seite **Montagestückliste** die Aktion **Stückliste anzeigen** aus.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines" />Um den Montageartikel von den Komponenten in Belegzeilen ersetzen

von beliebigen Verkaufs- und Einkaufsbeleg aus, die einen Montageartikel enthalten, können Sie eine spezielle Funktion verwenden, um die Zeile für den Montageartikel durch neue Zeilen für Komponenten zu ersetzen. Diese Funktion kann beispielsweise dann nützlich sein, wenn Sie die Komponenten als Kit verkaufen möchten, das den Montageartikel darstellt.

Die Aktion **Stückliste auflösen** steht auch auf der Seite **Montagestückliste** zur Verfügung, um die Elemente der Unterbaugruppe in einer Montagestückliste anzuzeigen.

> [!CAUTION]  
> Wenn Sie die Funktion **Stückliste entfalten** verwendet haben, können Sie sie nicht einfach rückgängig machen. Um die Aktion rückgängig zu machen, müssen Sie die Verkaufsauftragszeilen, die die Komponenten darstellen, löschen und dann erneut eine Verkaufsauftragszeile für den Montageartikel eingeben.

Das folgende Verfahren basiert auf einer Verkaufsrechnung. Die gleichen Schritte gelten für andere Verkaufsbelege und alle Kaufbelege.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine Verkaufsrechnung, die eine Zeile für einen Montageartikel enthält.
3. Wählen Sie die Zeile für ein Element der Montage und dann die Zeilenaktion **Stückliste auflösen**.

Alle Felder in der Verkaufsrechnungszeile für den Montageartikel werden außer für den **Artikel** **Beschreibung** gelöscht. Vollständige Verkaufsrechnungszeilen werden für die Komponenten und möglichen Ressourcen eingefügt, aus denen der Montageartikel besteht.

> [!NOTE]
> Der Bericht **Kommissionierliste nach Bestellung** wird ebenfalls geändert, um nur die Komponenten anzuzeigen. Dies bedeutet, dass ein Lagerarbeiter, der den übergeordneten Artikel, den Montageartikel, auswählt, diesen nicht in der Kommissionierliste sieht. Erfahren Sie mehr unter [Drucken der Kommissionierliste](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item" />So berechnen Sie den festen Einstandspreis von Montagestücklisten

Sie berechnen den Einstandspreis eines Montageartikels, indem Sie den Einstandspreis jeder Komponente und Ressource in der Montagestückliste des Artikels ermitteln.

Sie können den Einstandspreis (fest) für eine oder mehrere Artikel auf der Seite **Einst.-Preis (fest) Arbeitsblatt** auch berechnen und aktualisieren. Erfahren Sie mehr unter [Standardkosten aktualisieren](finance-how-to-update-standard-costs.md).  

Der Einstandspreis einer Montagestückliste entspricht immer der Summe der Einstandspreise der Komponenten, Artikel und aller Ressourcen.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für ein Element der Montage. (Das Feld **Montagestückliste** auf der Seite **Positionen** enthält **Ja**.)
3. Wählen Sie auf der Seite **Elementkarte** die Aktion **Montage** und dann die Aktion **Montagestückliste**.
4. Auf der Seite **Montagestückliste** wählen Sie die **Calc. Einstandspreis (fest)** Aktion aus.
5. Wählen Sie eine der folgenden Optionen aus und klicken Sie dann auf die Schaltfläche **OK**.

|Option |Description |
|-------|------------|
|**Oberste Ebene**|Berechnet den festen Einstandspreis des Montageartikels als Gesamtkosten aller gekauften oder gefertigten Artikel dieser Montagestückliste, unabhängig von evtl. zugrunde liegenden Montagestücklisten.|
|**"Alle Ebenen"**|Berechnet den festen Einstandspreis des Montageartikels als Summe folgender Komponenten: 1) Der berechneten Kosten aller zugrunde liegenden Montagestücklisten in der Montagestückliste. 2) Die Kosten aller gekauften Artikel in der Montagestückliste.|

Die Einstandspreise der Artikel, aus denen die Montagestückliste besteht, werden anhand der Artikelkarten der Komponenten kopiert. Die Kosten jedes Artikels wird mit der Menge multipliziert und die Summe der Kosten wird auf der Montageartikelkarte im Feld **Einheitskosten** angezeigt.

## <a name="see-related-microsoft-training" />Siehe die zugehörige [Microsoft Schulung](/training/modules/set-up-assembly-items-dynamics-365-business-central/).

## <a name="see-also" />Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Verwalten von Produktvarianten](inventory-item-variants.md)  
[Die Verfügbarkeit von Elementen anzeigen](inventory-how-availability-overview.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
