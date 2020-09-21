---
title: Artikelreferenzen verwenden | Microsoft Docs
description: Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen Feld
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2c676af23e5a6e988ab5d89d07118b9ff1cce86b
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777961"
---
# <a name="use-item-cross-references"></a>Artikelreferenzen verwenden
Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen Feld Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.

Die folgenden Verfahren beschreiben, wie Artikelreferenzen beim Einkauf verwendet werden. Die Schritte sind für den Verkauf ähnlich.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Eine Artikelreferenz zur Artikelbeschreibung des Kreditor einrichten

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte eines Artikels, für den Sie eine Referenz zur Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.
3. Wählen Sie die **Referenzen**-Aktion aus.

     Wenn Sie die Aktion **Referenzen** nicht finden können, wählen Sie die Anzeige weiterer Optionen aus, und suchen Sie diese unter **Navigieren**, **Artikel**.
  
4. In einer neuen Zeile auf der Seite **Artikelreferenzposten** füllen Sie die Felder wie notwendig aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>So geben Sie die Artikelbeschreibung eines Kreditors auf einer Einkaufsbestellung ein

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.
2. Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.
3. Erstellen Sie eine Einkaufszeile für den Artikel, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.
4. Wählen Sie im Feld **Referenznr.** die Artikelreferenz aus, die Sie erstellt haben, und wählen Sie dann **OK** aus.

Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie im Artikelreferenzposten festgelegt.

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
