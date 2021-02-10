---
title: Artikelreferenzen verwenden
description: Richten Sie Referenzen zwischen den Beschreibungen ein, die Sie und Ihr Kreditor für einen Artikel verwenden, damit Sie die Artikelbeschreibung des Kreditors in Einkaufsbelege einfügen können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013792"
---
# <a name="use-item-cross-references"></a>Artikelreferenzen verwenden
Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen Feld Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.

Die folgenden Verfahren beschreiben, wie Artikelreferenzen beim Einkauf verwendet werden. Die Schritte sind für den Verkauf ähnlich.

> [!NOTE]
> Für Artikelbezeichner wie z. B. GTINs oder GUIDs wird es immer üblicher, dass sie mindestens 30 Zeichen enthalten, was mehr ist. als die aktuelle Funktion für Artikelquerverweise handhaben kann. Wenn Sie Referenzen verwenden müssen, die mehr als 30 Zeichen enthalten, kann Ihr Administrator die Funktion **Längere Artikelreferenzen schreiben** auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren (der Link erfordert, dass Sie einen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten haben) aktivieren. Die Verwendung von Referenzen ändert sich nicht, aber die Namen von Dingen wie Seiten und Schaltflächen ändern sich. Aus der Seite **Artikelquerverweisposten** wird beispielsweise die Seite **Artikelreferenzposten**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Eine Artikelreferenz zur Artikelbeschreibung des Kreditor einrichten

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte eines Artikels, für den Sie eine Referenz zur Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.
3. Wählen Sie die **Referenzen**-Aktion aus.

     Wenn Sie die Aktion **Querverweise** nicht finden können, wählen Sie die Anzeige weiterer Optionen aus, und suchen Sie diese unter **Verknüpft** > **Artikel**.
  
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
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
