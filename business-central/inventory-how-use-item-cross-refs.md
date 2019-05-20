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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244045"
---
# <a name="use-item-cross-references"></a>Artikelreferenzen verwenden
Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen Feld Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.

Die folgenden Verfahren beschreiben, wie Artikelreferenzen beim Einkauf verwendet werden. Die Schritte sind für den Verkauf ähnlich.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Eine Artikelreferenz zur Artikelbeschreibung des Kreditor einrichten
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte eines Artikels, für den Sie eine Referenz zur Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.
3. Wählen Sie die **Referenzen**-Aktion aus.
4. In einer neuen Zeile auf der Seite **Artikelreferenzposten** füllen Sie die Felder wie notwendig aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>So geben Sie die Artikelbeschreibung eines Kreditors auf einer Einkaufsbestellung ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.
2. Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.
3. Erstellen Sie eine Einkaufszeile für den Artikel, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.
4. Wählen Sie im Feld **Referenznr.** die Artikelreferenz aus, die Sie erstellt haben, und wählen Sie dann **OK** aus.

Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie im Artikelreferenzposten festgelegt.

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
