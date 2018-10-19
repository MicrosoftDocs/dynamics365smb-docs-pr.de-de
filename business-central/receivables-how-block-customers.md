---
title: "So sperren Sie Artikelverkäufe an den Debitoren vom Verkauf oder Einkauf"
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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

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

