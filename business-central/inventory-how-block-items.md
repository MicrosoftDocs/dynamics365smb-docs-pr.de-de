---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: "In Business Central kann ein Artikel für den Verkauf, den Einkauf oder alle Zwecke gesperrt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: de-de
ms.lasthandoff: 07/30/2018

---
# <a name="block-items-from-sales-or-purchasing"></a>Artikel vom Verkauf oder Einkauf sperren
Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.  

In der folgenden Tabelle wird dargestellt, was geschieht, wenn Artikel gesperrt werden.  

|Option|Description|  
|--------------------|------------|  
|**Vertrieb gesperrt**|Sie können den Artikel nicht in ein Verkaufs- oder Verkaufsartikelbuch.-Blatt eingeben.|  
|**Einkauf gesperrt**|Sie können den Artikel nicht in ein Einkaufsdokument, in einem Einkaufsartikel Buch.-Blatt oder in Einkaufsplanungsvorgänge eingeben.|  
|**Gesperrt**|Sie können diesen Artikel nicht für Artikeltransaktionen verwenden. Weitere Informationen zum Sperren eines Artikels für alle Zwecke finden Sie in der Artikelkarte.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-posted"></a>So sperren Sie einen Artikel vor der Buchung
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbest](inventory-manage-inventory.md)  

