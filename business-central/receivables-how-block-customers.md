---
title: So blockieren Sie den Verkauf an Kunden
description: 'Bei Bedarf können Sie verhindern, dass ein Debitor in Verkaufsbelege und andere Verkaufstransaktionen aufgenommen wird.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="block-customers"></a>Kunden blockieren
Sie können einen Debitor beispielsweise wegen Insolvenz sperren, sodass dieser nicht in Verkaufsbelegen aufgenommen werden kann oder für den Debitor keine Umsätze gebucht werden können.

Zusätzlich zum Blockieren eines Debitors können Sie ausstehende Transaktionen festlegen, damit der Debitor in Verbindung mit Mahnungen ist. Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)   

Die drei Optionen zum Sperren von Debitoren werden in den folgenden Tabelle beschrieben.  

|Option|Beschreibung|  
|--------------------|------------|  
|**"Leer"**|Transaktionen sind für diesen Debitor zulässig.|
|**Lieferung**|Für diesen Kunden können keine neuen Bestellungen und neuen Lieferungen erstellt werden. Vorhandene Lieferungen, die noch nicht fakturiert wurden, können fakturiert werden.|  
|**Fakturieren**|Für diesen Kunden können keine neuen Bestellungen, neuen Lieferungen und neuen Rechnungen erstellt werden. Bestehende, noch nicht fakturierte Sendungen können nicht fakturiert werden. Sie können dem Debitor weiterhin Erinnerungen und Zinsrechnungen senden.|  
|**Alle**|Für diesen Debitor ist keine Transaktion zulässig, wozu auch Zahlungen gehören.|  

## <a name="to-block-a-customer"></a>Einen Debitor sperren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie einen Debitoren und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Feld **Gesperrt** aus, was gesperrt werden soll, wie in der obigen Tabelle beschrieben.

## <a name="see-also"></a>Siehe auch
[Neue Debitoren registrieren](sales-how-register-new-customers.md)  
[Restbeträge einziehen](receivables-collect-outstanding-balances.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
