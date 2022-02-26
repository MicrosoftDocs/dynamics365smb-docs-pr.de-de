---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: Sie können verhindern, dass Artikel in Zeilen von Verkaufs- oder Kaufbelegen eingegeben oder in einer Transaktion gebucht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 744d19675fe3ae95bcbaa56d6e8555ac734180e6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441168"
---
# <a name="block-items-from-sales-or-purchasing"></a>Artikel vom Verkauf oder Einkauf sperren
Sie können einen Artikel sperren, damit er nicht in Zeilen von Verkaufs- oder Einkaufsbelegen eingegeben und in einer Transaktion nicht gebucht werden kann. Dies ist beispielsweise nützlich, wenn ein Artikel einen bekannten Fehler aufweist. Wenn jemand in einem Verkaufs- oder Einkaufsbeleg einen gesperrten Artikel auswählt, wird er durch eine Nachricht darüber informiert, dass der Artikel gesperrt ist.

In der folgenden Tabelle wird beschrieben, was geschieht, wenn Artikel gesperrt sind.  

|Option|Beschreibung|  
|--------------------|------------|  
|**Vertrieb gesperrt**|Sie können den Artikel nicht in ein Verkaufs- oder Verkaufsartikelbuch.-Blatt eingeben.|  
|**Einkauf gesperrt**|Sie können den Artikel nicht in ein Einkaufsdokument, in einem Einkaufsartikel Buch.-Blatt oder in Einkaufsplanungsvorgänge eingeben.|  
|**Gesperrt**|Sie können diesen Artikel nicht für Artikeltransaktionen verwenden.|  

> [!NOTE]
> Blockierte Artikel können zurückgesendet werden. Das bedeutet, dass keine der obigen Einstellungen gilt, wenn der Artikel für Reklamationen und Gutschriften verwendet wird.

Wenn Sie die Funktion **Aus Dokument kopieren** verwenden, um neue Dokumente auf der Grundlage vorhandener Dokumente zu erstellen, werden Sie benachrichtigt, wenn Positionen in den Zeilen des Quelldokuments blockiert sind. Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-posted"></a>So sperren Sie einen Artikel vor der Buchung
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]