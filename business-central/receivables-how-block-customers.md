---
title: So sperren Sie Verkäufe an Debitoren
description: Bei Bedarf können Sie verhindern, dass ein Debitor in Verkaufsbelege und andere Verkaufstransaktionen aufgenommen wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc8014cf0896db1ebbc5f0c5ea22e0f160c1b06d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926547"
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
[Registriert einen neuen Debitor.](sales-how-register-new-customers.md)  
[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
