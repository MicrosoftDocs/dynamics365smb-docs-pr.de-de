---
title: "Vorgehensweise: Mit Stücklisten arbeiten| Microsoft Docs"
description: "Sie erstellen eine Montagestückliste oder eine Fertigungsstückliste, um die Komponenten und Ressourcen anzuzeigeb, die benötigt werden, um den Artikel zusammenzufügen, die die Stückliste darstellt."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f27160f551a002d1d19fa64b86aa637d8fadcf8a
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-bills-of-material"></a>Mit Fertigungsstücklisten arbeiten
Verwenden Sie Stücklisten (BOMs), um beispielsweise Oberartikel zu strukturieren, die nach Ressourcen oder Arbeitsplätze aus Komponenten montiert oder gefertigt werden müssen. Eine Montagestückliste kann auch verwendet werden, um den übergeordneten Artikel als Kit zu verkaufen, das aus den Komponenten bestehet.

## <a name="assembly-boms-or-production-boms"></a>Montagestücklisten oder Fertigungsstücklisten
Montageaufträge werden für die Produktion von Endartikeln aus Komponenten in einem einfachen Prozess verwendet, der mit einer oder mehreren grundlegenden Ressourcen, die keine Maschinen oder Arbeitsplatzgruppen sind, oder ganz ohne Ressourcen durchgeführt werden kann. Beispielsweise könnte ein Montagevorgang lauten, zwei Weinflaschen und einen Sack Kaffee zu kommissionieren und sie als Geschenkartikel zu verpacken.  

Eine Montagestückliste liefert die Masterdaten, die festlegen, welche Komponentenartikel in einen montierten Endartikel enthalten sind und welche Ressourcen verwendet werden, um den Montageartikel zu montieren. Wenn Sie im Kopf eines neuen Montageauftrags den Montageartikel und die Menge eingeben, werden die Montageauftragszeilen automatisch aus der Montagestückliste übernommen und pro Komponente oder Ressource als eine Montageauftragszeile dargestellt. Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md).

Montagestücklisten werden in diesem Thema beschrieben.

Fertigungsaufträge werden für die Produktion von Endartikeln aus Komponenten in einem komplexen Prozess verwendet, für den ein FA-Arbeitsplan und Arbeitsplätze oder Arbeitsplatzgruppen erforderlich sind, die Fertigungskapazitäten darstellen. Ein Fertigungsvorgang könnte beispielsweise darin bestehen, Stahlplatten in einem Arbeitsgang zuzuschneiden, sie im folgenden Arbeitsgang zu schweißen und den Endartikel im letzten Arbeitsgang zu lackieren. Weitere Informationen finden Sie unter [Produktion](production-manage-manufacturing.md)  

Eine Fertigungsstückliste liefert die Masterdaten, die einen Fertigungsartikel und die enthaltenen Komponenten definieren, die in diese einfließen. für Montageartikel muss die Fertigungsstückliste zertifiziert und dem Fertigungsartikel zugeordnet werden, bevor sie in einem Fertigungsauftrag verwendet werden kann. Wenn Sie den Fertigungsartikel entweder manuell in einer FA-Zeile eingeben oder indem Sie den Auftrag aktualisieren, wird der Inhalt der Fertigungsstückliste zu den Fertigungsauftragskomponenten. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-create-production-boms.md).  

Das Ressourcenkonzept ist in der Produktion weitergehender als in der Montageverwaltung. Arbeitsplatzgruppen und Arbeitsplätze arbeiten als Ressourcen und Produktionsschritte werden durch Arbeitsgänge dargestellt, die Ressourcen in den Arbeitsplänen zugeordnet sind. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).

Montageaufträge und Fertigungsaufträge können direkt mit Verkaufsaufträgen verknüpft sein. Sie können jedoch nur Montageaufträge nutzen, um den Endartikel direkt für eine Debitorenanfrage im Verkaufsauftrag anzupassen.

## <a name="to-create-an-assembly-bom"></a>So erstellen Sie eine Montagestückliste
Um einen übergeordneten Artikel zu definieren, der aus anderen Artikeln und möglicherweise Ressourcen besteht die benötigt werden, um die übergeordnete Baugruppe zusammenzufügen, müssen Sie eine Montagestückliste erstellen.  

Montagestücklisten enthalten normalerweise Artikel, können jedoch auch eine oder mehrere Ressourcen enthalten, die die Montageartikel ausführen.

Montagestücklisten können mehrstufig sein, was bedeutet, dass eine Komponente in der Montagestückliste selbst ein Montageartikel sein kann. In diesem Fall lautet das Feld **Montagestückliste** in der Montagestücklistenzeile **Ja**.

Spezielle Anforderungen gelten für Artikel auf Montagestücklisten in Bezug auf die Verfügbarkeit. Weitere Informationen finden Sie im Abschnitt "Verfügbarkeit eines Artikels nach dessen Verwendung in den Montagestücklisten anzeigen [Vorgehensweise: Verschaffen Sie sich eine Übersicht zur Verfügbarkeit](inventory-how-availability-overview.md)".

Es gibt zwei Schritte zum Erstellen einer Montagestückliste:
- Einrichten einer neuen Artikelkarte
- Gibt die Beschreibung des Montageartikels an.

1. Richten Sie einen neuen Artikel ein. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

    Fahren Sie fort, um Komponenten oder Ressourcen in der Montagestückliste einzugeben.  
2. Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.
3. Füllen Sie im Fenster **Montagestückliste** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Um die Komponenten eines Montageartikels anzuzeigen gemäß der Stücklistenstruktur
Im Fenster **Montagestückliste** können Sie ein separates Fenster öffnen, in dem die Komponenten sowie jegliche Ressourcen angezeigt werden, die gemäß ihrer Stücklistenposition unter den Montageartikel eingerückt werden.

1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie das Kartenfenster für den Montageartikel. (Das Feld **Montagestückliste** im Fenster **Artikel** enthält **Ja**.)
3. Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.
4. Wählen Sie im Fenster **Montagestückliste** die Aktion **Stückliste anzeigen** aus.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Um den Montageartikel von den Komponenten in Belegzeilen ersetzen
von beliebigen Verkaufs- und Einkaufsbeleg aus, die einen Montageartikel enthalten, können Sie eine spezielle Funktion verwenden, um die Zeile für den Montageartikel durch neue Zeilen für Komponenten zu ersetzen. Diese Funktion kann beispielsweise dann nützlich sein, wenn Sie die Komponenten als Kit verkaufen möchten, das den Montageartikel darstellt.

**Vorsicht**: Wenn Sie die Funktion **Stückliste entfalten** verwendet haben, können Sie sie einfach nicht rückgängig machen. Um die Aktion rückgängig zu machen, müssen Sie die Verkaufsauftragszeilen, die die Komponenten darstellen, löschen und dann erneut eine Verkaufsauftragszeile für den Montageartikel eingeben.

Das folgende Verfahren basiert auf einer Verkaufsrechnung. Die gleichen Schritte gelten auch für andere Verkaufs- und Einkaufsbelege.

1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** aus und geben Sie **Verkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie eine Verkaufsrechnung, die eine Zeile für einen Montageartikel enthält.
3. Wählen Sie die Zeile für einen Montageartikel und dann **Stückliste entfalten** Zeilenaktion aus.

Alle Felder in der Verkaufsrechnungszeile für den Montageartikel werden außer für den **Artikel** **Beschreibung** gelöscht. Vollständige Verkaufsrechnungszeilen werden für die Komponenten und möglichen Ressourcen eingefügt, aus denen der Montageartikel besteht.

**Hinweis**: Die entfaltete Stücklistenfunktion ist im Fenster **Montagestückliste** verfügbar.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>So berechnen Sie den festen Einstandspreis von Montagestücklisten
Sie berechnen den Einstandspreis eines Montageartikels, indem Sie den Einstandspreis jeder Komponente und Ressource in der Montagestückliste des Artikels ermitteln.

Sie können den Einstandspreis (fest) für eine oder mehrere Artikel im Fenster **Einst.-Preis (fest) Vorschlag** auch berechnen und aktualisieren. Weitere Informationen zum Erstellen von Erfassungen finden Sie unter [Standard-Buch.-Blätter aktualisieren](finance-how-to-update-standard-costs.md).  

Der Einstandspreis einer Montagestückliste entspricht immer der Summe der Einstandspreise der Komponenten, Artikel und aller Ressourcen.

1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie das Kartenfenster für den Montageartikel. (Das Feld **Montagestückliste** im Fenster **Artikel** enthält **Ja**.)
3. Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.
4. Im Fenster **Montagestückliste** wählen Sie die **Calc. Einstandspreis (fest)** Aktion aus.
5. Wählen Sie eine der Optionen aus, und klicken Sie auf **OK**.

|Option |Description |
|-------|------------|
|**Oberste Ebene**|Berechnet den festen Einstandspreis des Montageartikels als Gesamtkosten aller gekauften oder gefertigten Artikel dieser Montagestückliste, unabhängig von evtl. zugrunde liegenden Montagestücklisten.|
|**"Alle Ebenen"**|Berechnet den festen Einstandspreis des Montageartikels als Summe folgender Komponenten: 1) Der berechneten Kosten aller zugrunde liegenden Montagestücklisten in der Montagestückliste. 2) Die Kosten aller gekauften Artikel in der Montagestückliste.|



Die Einstandspreise der Artikel, aus denen die Montagestückliste besteht, werden anhand der Artikelkarten der Komponenten kopiert. Die Kosten jedes Artikels wird mit der Menge multipliziert und die Summe der Kosten wird auf der Montageartikelkarte im Feld **Einheitskosten** angezeigt.

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)     
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

