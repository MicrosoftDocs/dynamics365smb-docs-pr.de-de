---
title: Erstellen und Verwalten von Aritkel, die nicht am Lager sind | Microsoft Docs
description: "Beschreibt, wie lagerwertunabhängigen Artikel oder Artikel behandelt werden, die nicht in Ihrem Lagerbestand verwaltet werden."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cdfca33d0d9ea4b66b8e1c15cd66eaf9fa79b819
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-nonstock-items"></a>Arbeiten mit Katalogartikeln
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Wenn Sie damit beginnen wollen, solche Artikel im Lager zu verwalten, können Sie sie auf zwei Arten in normale Artikelkarten umwandeln.

* Erstellen Sie eine neue Artikelkarte aus der Katalogartikelkarte auf Basis einer Vorlage.
* Wählen Sie aus einer Auftragsposition des Typs **Artikel** mit einem leeren **Nummern**-Feld einen Artikel, der nicht an Lager ist. Eine Artikelkarte wird automatisch für den Artikel erstellt, der nicht an Lager ist.

> [!NOTE]  
>   Sie können im Fenster Verkaufsrechnung keine **Verkaufsrechungen**auswählen. Sie können Katalogartikel im Fenster **Verkaufschance** auswählen, aber der Katalogartikel wird nicht in einen normalen Artikel konvertiert, wenn Sie die Funktion **Auftrag erstellen** verwenden.

Ein Katalogartikel besitzt üblicherweise die Artikelnummer des Kreditoren, der diesen bereitstellt. Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst eingerichtet werden, wie die Kreditorenartikelnummerierung in Ihre eigene Artikelnummerierung umgewandelt wird.   

## <a name="to-create-a-nonstock-item"></a>So erstellen Sie einen Katalogartikel:
Katalogartikelkarten enthalten viel weniger Informationen als normale Artikelkarten, da Sie diese nur verwenden, um Angebote auf Anfragen oder auf andere Arten zu erstellen. Aus diesem Grund müssen sie in normale Artikelkarten konvertiert werden, bevor Sie Verkaufstransaktionen mit ihnen buchen können.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Nicht-Katalogartikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a>So richten Sie ein, wie Katalogartikelnummern in Ihrer eigenen Nummerierung erstellt werden
Um die Konvertierung einer Katalogartikelkarte in eine normale Artikelkarte zu aktivieren, muß zunächst festgelegt werden, wie die Kreditorenartikelnummerierung in Ihr eigenes Artikelnummernformat umgewandelt wird.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Nicht-Katalogartikel einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a>So konvertieren Sie einen Katalogartikel in einen normalen Artikel
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Nicht-Katalogartikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte für einen Katalogartikel, den Sie in einen normalen Artikel umwandeln wollen.
3. Wählen Sie im Fenster **Katalogartikelkarte** die Aktion **Artikel erstellen** aus.

Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt. Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a>So verkaufen Sie einen Katalogartikel und konvertieren ihn in einen normalen Artikel
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus. Füllen Sie die Felder auf dem Inforegister **Allgemein** für alle Verkaufsaufträge aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3. Auf einer neuen Verkaufszeile im Feld **Typ** wählen Sie **Artikel** und ignorieren die **Nr.**. leer lassen.
4. Wählen Sie die Aktion **Position** und dann die Aktion **Artikel nicht an Lager auswählen**.

    Der Katalogartikel ist nun in einen normalen Artikel umgewandelt. Eine neue Artikelkarte, die mit Informationen des Katalogartikels und einer Vorlage des entsprechenden Artikels ausgefüllt ist, wird erstellt.
5. Wählen Sie im Fenster **Katalogartikel** den Katalogartikel aus, den Sie verkaufen möchten, und klicken Sie anschließend auf **OK**.
6. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

Sie können dann die Felder in der neuen Artikelkarte nach Bedarf ausfüllen oder ändern. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

> [!NOTE]  
>   Für den Kreditor des Artikels wird automatisch ein Artikelreferenzdatensatz zwischen der Artikelnummer des Kreditors und Ihrer neuen Artikelnummer erstellt.

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Spezialaufträge erstellen](sales-how-to-create-special-orders.md)|  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

