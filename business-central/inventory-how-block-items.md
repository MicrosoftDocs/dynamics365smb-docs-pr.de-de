---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel für den Verkauf, den Einkauf oder alle Zwecke gesperrt werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798140"
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

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-posted"></a>So sperren Sie einen Artikel vor der Buchung
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  
