---
title: Element-Referenzen verwenden
description: Legen Sie Referenzen zwischen den Beschreibungen fest, die Sie und Ihr Kreditor für einen Artikel verwenden, um die Artikelbeschreibung des Lieferanten in Kaufbelege einzufügen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588601"
---
# <a name="use-item-references"></a>Element-Referenzen verwenden
Wenn Sie einen Bezug zwischen der Artikelbeschreibung, die Sie für einen Artikel verwenden, und der Beschreibung, die der Kreditor dieses Artikels verwendet, festlegen, wird die Artikelbeschreibung des Kreditors automatisch in die Belege des Kreditors eingefügt, wenn Sie das Feld **Artikelreferenznummer** ausfüllen. Feld eingetragen. Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.

Die folgenden Verfahren beschreiben, wie Sie Artikelreferenzen auf der Seite des Kaufs verwenden. Die Schritte sind für den Verkauf ähnlich.

> [!NOTE]
> Da nicht alle Firmen Artikelreferenzen verwenden, haben wir die zugehörigen Felder und Aktionen ausgeblendet, um das Durcheinander auf den Seiten zu minimieren. Wenn Sie sich entscheiden, sie zu verwenden, können Sie auf der Seite **Lagerbestandseinrichtung** die Option **Artikelreferenzen verwenden** aktivieren. Nachdem Sie die Artikelreferenzen aktiviert haben, sind die Felder und Aktionen auf den Seiten Artikelkarte, Lieferantenkarte und Kundenkarte sowie in Einkaufs- und Verkaufsbelegen verfügbar.

## <a name="to-start-using-item-references"></a>So beginnen Sie mit der Verwendung von Artikelreferenzen
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Aktivieren Sie das Kontrollkästchen **Artikelreferenzen verwenden**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Um einen Artikelverweis auf die Artikelbeschreibung eines Kreditors festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen Artikel, für den Sie einen Verweis auf die Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.
3. Wählen Sie die Aktion **Artikelverweise**.

     Wenn Sie die Aktion **Artikelverweise** nicht finden können, wählen Sie die Option zum Anzeigen weiterer Optionen und suchen Sie sie dann unter **Verwandt** > **Artikel**.
  
4. Füllen Sie in einer neuen Zeile auf der Seite **Element-Referenz-Einträge** die erforderlichen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>So geben Sie die Artikelbeschreibung eines Kreditors auf einer Einkaufsbestellung ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren einen Artikelbezug festgelegt haben.
3. Erstellen Sie eine Kauf-Zeile für den Artikel, für den Sie in der vorherigen Vorgehensweise einen Artikelbezug festgelegt haben.
4. Im Feld **Artikelreferenz-Nr.** wählen Sie den von Ihnen erstellten Artikelbezug aus und wählen dann die Schaltfläche **OK**.

Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie sie auf dem Eintrag für die Artikelreferenz festgelegt wurde.

## <a name="see-also"></a>Weitere Informationen
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]