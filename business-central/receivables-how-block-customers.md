---
title: So sperren Sie Artikelverkäufe an den Debitoren vom Verkauf oder Einkauf
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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a2dee70270df135bc61ddef38e661758431b02a9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251354"
---
# <a name="block-customers"></a>Debitoren sperren
Sie können Debitoren, zum Beispiel aufgrund von Zahlungsunfähigkeit sperren, so dass der Debitor nicht zu Verkaufsbelegen hinzugefügt werden kann, oder dass keine Transaktionen für den Debitor gebucht werden können.

Zusätzlich zum Blockieren eines Debitors können Sie ausstehende Transaktionen festlegen, damit der Debitor in Verbindung mit Mahnungen ist. Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)   

Die drei Optionen werden in den folgenden Sperroptionen beschrieben.  

|Option|Description|  
|--------------------|------------|  
|**"Leer"**|Transaktionen sind für diesen Debitor zulässig.|
|**Liefern**|Für diesen Debitor können keine neuen Aufträge und Lieferungen erstellt werden. Vorhandene Lieferungen, die noch nicht fakturiert wurden, können fakturiert werden.|  
|**Fakturieren**|Für diesen Debitor können keine neuen Aufträge, Lieferungen und Rechnungen erstellt werden. Vorhandene Lieferungen, die noch nicht fakturiert wurden, können nicht fakturiert werden.|  
|**Alle**|Für diesen Debitor ist keine Transaktion zulässig, wozu auch Zahlungen gehören.|  

## <a name="to-block-a-customer"></a>Einen Debitor sperren  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie einen Debitoren und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Füllen Sie das Feld **Blockiert** mit einer der Optionen aus, wie sie oben beschrieben werden.

## <a name="see-also"></a>Siehe auch  
[Neue Debitoren registrieren.](sales-how-register-new-customers.md)  
[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
