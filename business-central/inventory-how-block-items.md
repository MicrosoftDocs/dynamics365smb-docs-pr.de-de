---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: Sie können verhindern, dass ein Artikel beispielsweise für Verkaufs- oder Einkaufsbelege verwendet wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87628f1983e0bafda9119ef3729dbb142c761b1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393124"
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
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-posted"></a>So sperren Sie einen Artikel vor der Buchung
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]