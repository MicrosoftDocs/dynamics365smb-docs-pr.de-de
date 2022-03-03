---
title: Drucken einer Liste zur Lagerkommissionierung aus einem Verkaufsauftrag
description: Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftrag, Verkaufsbeleg, Rechnungsbeleg und anderen ausgehenden Verkaufsauftragsbelegen drucken.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e42008912079eafeaa037f7759a50a2c76393edb
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130098"
---
# <a name="print-the-picking-list"></a>Kommissionierliste drucken

Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftrag und anderen Belegen drucken, die den Versand von Artikeln einleiten.

Dieser Bericht wird normalerweise in Unternehmen ohne dedizierte Funktionen für die Lagerverwaltung verwendet, sodass ein Lagerarbeiter die Kommissionierliste einfach über den zugehörigen Verkaufsbeleg aufrufen oder drucken kann. In Unternehmen mit höherem Volumen oder komplexeren Prozessen wird die Kommissionierung in dedizierten Lagerdokumenten geplant und durchgeführt. Weitere Informationen finden Sie unter [Artikel kommissionieren](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>So drucken Sie eine Kommissionierliste aus einem Verkaufsauftrag

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle anderen Belege ähnlich, mit denen der Versand von Artikeln eingeleitet werden kann, z. B. ein Umlagerungsauftrag.

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Verkaufsauftrag, für den Sie Artikel auswählen möchten.  
3. Wählen Sie die Aktion **Bericht** und dann die Aktion **Kommissionierliste nach Bestellung** aus.  
4. Wählen Sie die Schaltfläche **Drucken** aus, um die Kommissionierliste zu drucken, oder die Schaltfläche **Vorschau**, um sie auf dem Bildschirm anzuzeigen.

Sie können die Kommissionierliste auch als Dokument speichern, um sie beispielsweise an jemanden zu senden oder dem Verkaufsauftrag als Anhang hinzuzufügen. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten](ui-how-add-link-to-record.md).

> [!NOTE]
> Wenn Sie die Funktion **Stückliste explodieren** auf dem Verkaufsauftrag verwendet haben, werden im Bericht nur die Komponenten des zugehörigen Montageartikels angezeigt. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Siehe auch

[Lagerbestand](inventory-manage-inventory.md)  
[Entnahme von Artikeln](warehouse-pick-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]