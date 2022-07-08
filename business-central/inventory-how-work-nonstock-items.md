---
title: Erstellen und Verwalten von Katalogartikeln
description: Beschreibt, wie Sie Elemente verkaufen können, die Sie nicht in Ihrer Artikelliste führen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: c12eb256d4e7f1e211e28dacf4c403406dba3d85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077007"
---
# <a name="work-with-catalog-items"></a>Arbeiten mit Katalogartikeln

Katalogartikel sind Elemente, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] erst dann verwalten, wenn Sie sie verkaufen. Wenn Sie die Aktion **Katalogelement auswählen** verwenden, um ein Katalogelement zu einer Zeile in einem Verkaufsauftrag oder einem Angebot hinzuzufügen, wird das Katalogelement in einen regulären Artikel umgewandelt.

> [!NOTE]  
> Sie können auf der Seite Katalogartikel keine **Verkaufsrechungen** auswählen.

Ein Katalogartikel besitzt üblicherweise die Artikelnummer des Kreditoren, der diesen bereitstellt. Bevor Sie ein Katalogelement in ein normales Element umwandeln können, müssen Sie festlegen, wie die Artikelnummern der Lieferanten in Ihre Artikelnummern umgewandelt werden sollen. Weitere Informationen finden Sie unter [Angeben, wie Katalogartikelnummern in Ihre eigene Nummerierung umgewandelt werden](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogelemente sollen nicht mit Nicht-Lagerartikeln beispielsweise verwechselt werden, die reguläre sind Artikel, die die Art **Nicht-Lager** gewährt werden, sie aus Verfügbarkeits- und Kostenberechnungsberechnungen B zu behalten, da sie nur intern verwendet und Basis Einstandspreis haben. Weitere Informationen zu diesen Arten finden Sie unter [über Einheitstypen](inventory-about-item-types.md)

## <a name="create-a-catalog-item"></a>Einen Katalogartikel erstellen

Katalogartikelkarten enthalten viel weniger Informationen als normale Artikelkarten, da Sie diese nur verwenden, um Angebote auf Anfragen oder auf andere Arten zu erstellen. Aus diesem Grund müssen sie in normale Artikelkarten konvertiert werden, bevor Sie Verkaufstransaktionen mit ihnen buchen können.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Katalogartikel** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Legen Sie fest, wie Katalogartikelnummern in Ihre eigene Nummerierung umgewandelt werden

Bevor Sie ein Katalogelement in ein normales Element umwandeln können, müssen Sie festlegen, wie die Artikelnummern der Lieferanten in Ihre Artikelnummern umgewandelt werden sollen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Katalogartikel – Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Ein Element aus dem Katalog in ein normales Element umwandeln

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Katalogartikel** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für einen Katalogartikel, den Sie in einen normalen Artikel umwandeln wollen.
3. Wählen Sie auf der Seite **Katalogartikelkarte** die Aktion **Artikel erstellen** aus.

Es wird eine neue Artikelkarte erstellt, die mit Informationen aus dem Katalogartikel und einer entsprechenden Artikelvorlage vorausgefüllt ist. Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>So verkaufen Sie einen Katalogartikel und konvertieren ihn in einen normalen Artikel

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus. Füllen Sie die Felder auf dem Inforegister **Allgemein** für alle Verkaufsaufträge aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3. Auf einer neuen Verkaufszeile im Feld **Typ** wählen Sie **Artikel** und ignorieren die **Nr.**. leer lassen.
4. Wählen Sie die Aktion **Position** und dann die Aktion **Artikel nicht an Lager auswählen**.

    Der Katalogartikel ist nun in einen normalen Artikel umgewandelt. Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt.
5. Wählen Sie auf der Seite **Katalogartikel** den Katalogartikel aus, den Sie verkaufen möchten, und klicken Sie anschließend auf **OK**.
6. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

> [!NOTE]  
> Zwischen der Artikelnummer des Kreditors und Ihrer neuen Artikelnummer wird automatisch eine Artikelreferenz eingefügt. Weitere Informationen finden Sie unter [Verwendung von Element-Referenzen](inventory-how-use-item-cross-refs.md).

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Spezialaufträge erstellen:](sales-how-to-create-special-orders.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
