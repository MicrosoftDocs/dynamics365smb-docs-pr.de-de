---
title: Erstellen und Verwalten von Katalogaritkel | Microsoft Docs
description: Beschreibt, wie man den Artikel behandelt, der in der Übersicht der Artikel aber nicht in Ihrer persönlichen Artikelliste ist.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e4db83e4d2e3efffc1523fe3eadb65a14b431027
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781035"
---
# <a name="work-with-catalog-items"></a>Arbeiten mit Katalogartikeln
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Wenn Sie damit beginnen wollen, solche Artikel im Lager zu verwalten, können Sie sie auf zwei Arten in normale Artikelkarten umwandeln.

* Erstellen Sie eine neue Artikelkarte aus der Katalogartikelkarte auf Basis einer Vorlage.
* Wählen Sie aus einer Auftragsposition des Typs **Artikel** mit einem leeren **Nummern**Katalog-Feld einen Artikel, der nicht an Lager ist. Eine Artikelkarte wird automatisch für den Katalog-Artikel erstellt.

> [!NOTE]  
> Sie können auf der Seite Katalogartikel keine **Verkaufsrechungen**auswählen.<br /><br />
> Sie können Katalogartikel auf der Seite **Verkaufschance** auswählen, aber der Katalogartikel wird nicht in einen normalen Artikel konvertiert, wenn Sie die Funktion **Auftrag erstellen** verwenden.

Ein Katalogartikel besitzt üblicherweise die Artikelnummer des Kreditoren, der diesen bereitstellt. Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst eingerichtet werden, wie die Kreditorenartikelnummerierung in Ihre eigene Artikelnummerierung umgewandelt wird.   

> [!Important]
> Katalogelemente sollen nicht mit Nicht-Lagerartikeln beispielsweise verwechselt werden, die reguläre sind Artikel, die die Art **Nicht-Lager** gewährt werden, sie aus Verfügbarkeits- und Kostenberechnungsberechnungen B zu behalten, da sie nur intern verwendet und Basis Einstandspreis haben. Weitere Informationen zu diesen Arten finden Sie unter [über Einheitstypen](inventory-about-item-types.md)

## <a name="to-create-a-catalog-item"></a>So erstellen Sie einen Katalogartikel
Katalogartikelkarten enthalten viel weniger Informationen als normale Artikelkarten, da Sie diese nur verwenden, um Angebote auf Anfragen oder auf andere Arten zu erstellen. Aus diesem Grund müssen sie in normale Artikelkarten konvertiert werden, bevor Sie Verkaufstransaktionen mit ihnen buchen können.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Katalogartikel** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>So richten Sie ein, wie Katalogartikelnummern in Ihrer eigenen Nummerierung erstellt werden
Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst festgelegt werden, wie die Kreditorenartikelnummerierung in Ihr eigenes Artikelnummernformat umgewandelt wird.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Katalogartikel-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>So konvertieren Sie einen Katalogartikel in einen normalen Artikel
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Katalogartikel** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen Katalogartikel, den Sie in einen normalen Artikel umwandeln wollen.
3. Wählen Sie auf der Seite **Katalogartikelkarte** die Aktion **Artikel erstellen** aus.

Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt. Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>So verkaufen Sie einen Katalogartikel und konvertieren ihn in einen normalen Artikel
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus. Füllen Sie die Felder auf dem Inforegister **Allgemein** für alle Verkaufsaufträge aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3. Auf einer neuen Verkaufszeile im Feld **Typ** wählen Sie **Artikel** und ignorieren die **Nr.**. leer lassen.
4. Wählen Sie die Aktion **Position** und dann die Aktion **Artikel nicht an Lager auswählen**.

    Der Katalogartikel ist nun in einen normalen Artikel umgewandelt. Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt.
5. Wählen Sie auf der Seite **Katalogartikel** den Katalogartikel aus, den Sie verkaufen möchten, und klicken Sie anschließend auf **OK**.
6. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

> [!NOTE]  
>   Für den Kreditor des Artikels wird automatisch ein Artikelreferenzdatensatz zwischen der Artikelnummer des Kreditors und Ihrer neuen Artikelnummer erstellt. Weitere Informationen finden Sie unter [Verwenden von Artikelquerverweisen](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Spezialaufträge erstellen](sales-how-to-create-special-orders.md)|  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
