---
title: So sperren Sie Verkäufe an Debitoren
description: Bei Bedarf können Sie verhindern, dass ein Debitor in Verkaufsbelege und andere Verkaufstransaktionen aufgenommen wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781738"
---
# <a name="block-customers"></a>Debitoren sperren
Sie können Debitoren, zum Beispiel aufgrund von Zahlungsunfähigkeit sperren, so dass der Debitor nicht zu Verkaufsbelegen hinzugefügt werden kann, oder dass keine Transaktionen für den Debitor gebucht werden können.

Zusätzlich zum Blockieren eines Debitors können Sie ausstehende Transaktionen festlegen, damit der Debitor in Verbindung mit Mahnungen ist. Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)   

Die drei Optionen zum Sperren von Debitoren werden in den folgenden Tabelle beschrieben.  

|Option|Beschreibung|  
|--------------------|------------|  
|**"Leer"**|Transaktionen sind für diesen Debitor zulässig.|
|**Liefern**|Für diesen Debitor können keine neuen Aufträge und Lieferungen erstellt werden. Vorhandene Lieferungen, die noch nicht fakturiert wurden, können fakturiert werden.|  
|**Fakturieren**|Für diesen Debitor können keine neuen Aufträge, Lieferungen und Rechnungen erstellt werden. Vorhandene Lieferungen, die noch nicht fakturiert wurden, können nicht fakturiert werden. Sie können dem Debitor weiterhin Erinnerungen und Zinsrechnungen senden.|  
|**Alle**|Für diesen Debitor ist keine Transaktion zulässig, wozu auch Zahlungen gehören.|  

## <a name="to-block-a-customer"></a>Einen Debitor sperren  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen Debitoren und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Feld **Gesperrt** aus, was gesperrt werden soll, wie in der obigen Tabelle beschrieben.

## <a name="see-also"></a>Siehe auch  
[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  
[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]