---
title: 'So gehts: Arbeiten mit Artikeln, die nicht an Lager sind| Microsoft Docs'
description: Beschreibt, wie man mit Artikel handelt, die nicht im Lagerbestand verwaltet werden
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae4710c0771d2b10c691f878ad6532e95f3b2912
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Arbeiten mit Katalogartikeln
<a id="how-to-work-with-nonstock-items" class="xliff"></a>
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Wenn Sie damit beginnen wollen, solche Artikel im Lager zu verwalten, können Sie sie auf zwei Arten in normale Artikelkarten umwandeln.

* Erstellen Sie eine neue Artikelkarte aus der Katalogartikelkarte auf Basis einer Vorlage.
* Wählen Sie aus einer Auftragsposition des Typs **Artikel** mit einem leeren **Nummern**-Feld einen Artikel, der nicht an Lager ist. Eine Artikelkarte wird automatisch für den Artikel erstellt, der nicht an Lager ist.

**Hinweis**: Sie können im Fenster **Verkaufsrechnung** keine Katalogartikel auswählen. Sie können Katalogartikel im Fenster **Verkaufschance** auswählen, aber der Katalogartikel wird nicht in einen normalen Artikel konvertiert, wenn Sie die Funktion **Auftrag erstellen** verwenden.

Ein Katalogartikel besitzt üblicherweise die Artikelnummer des Kreditoren, der diesen bereitstellt. Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst eingerichtet werden, wie die Kreditorenartikelnummerierung in Ihre eigene Artikelnummerierung umgewandelt wird.   

## So erstellen Sie einen Katalogartikel:
<a id="to-create-a-nonstock-item" class="xliff"></a>
Katalogartikelkarten enthalten viel weniger Informationen als normale Artikelkarten, da Sie diese nur verwenden, um Angebote auf Anfragen oder auf andere Arten zu erstellen. Aus diesem Grund müssen sie in normale Artikelkarten konvertiert werden, bevor Sie Verkaufstransaktionen mit ihnen buchen können.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Artikel nicht an Lager** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## So richten Sie ein, wie Katalogartikelnummern in Ihrer eigenen Nummerierung erstellt werden
<a id="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering" class="xliff"></a>
Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst festgelegt werden, wie die Kreditorenartikelnummerierung in Ihr eigenes Artikelnummernformat umgewandelt wird.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Artikel nicht an Lager einrichten** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.

## So konvertieren Sie einen Katalogartikel in einen normalen Artikel
<a id="to-convert-a-nonstock-item-to-a-normal-item" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Artikel nicht an Lager** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Karte für einen Katalogartikel, den Sie in einen normalen Artikel umwandeln wollen.
3. Wählen Sie im Fenster **Katalogartikelkarte** die Aktion **Artikel erstellen** aus.

Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt. Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).

## So verkaufen Sie einen Katalogartikel und konvertieren ihn in einen normalen Artikel
<a id="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Verkaufsauftrag** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus. Füllen Sie die Felder auf dem Inforegister **Allgemein** für alle Verkaufsaufträge aus. Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)
3. Auf einer neuen Verkaufszeile im Feld **Typ** wählen Sie **Artikel** und ignorieren die **Nr.**. leer lassen.
4. Wählen Sie die Aktion **Position** und dann die Aktion **Artikel nicht an Lager auswählen**.

    Der Katalogartikel ist nun in einen normalen Artikel umgewandelt. Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt.
5. Wählen Sie im Fenster **Katalogartikel** den Katalogartikel aus, den Sie verkaufen möchten, und klicken Sie anschließend auf **OK**.
6. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).

**Hinweis**: Für den Kreditor des Artikels wird automatisch ein Artikelreferenzdatensatz zwischen der Artikelnummer des Kreditors und Ihrer neuen Artikelnummer erstellt.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Vorgehensweise: Einen neuen Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

