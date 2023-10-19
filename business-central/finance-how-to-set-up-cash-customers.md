---
title: BarDebitoren einrichten
description: 'Dieses Thema beschreibt die Schritte, die erforderlich sind, um die Rechnung mit einer Kundennummer für Debitoren, die in bar bezahlen, festzulegen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-cash-customers"></a>BarDebitoren einrichten

Sie können keine Rechnung ohne Debitorennummer erstellen. Dies trifft auch zu, wenn Sie einen Barverkauf tätigen und kein Debitorenkonto aktualisieren müssen.  

## <a name="to-set-up-a-cash-customer"></a>So richten Sie Bargelddebitoren ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kunde** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Karte **Debitor**. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).
3. Geben Sie im Feld **Nr.** Geben Sie beispielsweise **Bar** ein.  
4. Geben Sie in dem Feld **Name** z. B. **BARVERKAUF** ein.  
5. Füllen Sie auf dem Inforegister **Fakturierung** die Felder **Debitorenbuchungsgruppe** und **Geschäftsbuchungsgruppe** aus.  

 Sie haben jetzt einen neuen Debitor und die notwendigen Informationen für die Fakturierung eingerichtet.  

> [!NOTE]  
> Es kann sein, dass Sie eine Buchungsgruppe gewählt haben, die auch für inländische Kreditverkäufe verwendet wird. Falls Sie gesonderte Daten für Barverkäufe benötigen, z. B. mit einem Verkaufs- oder Sammelkonto, können Sie zu diesem Zweck eine gesonderte Buchungsgruppe einrichten.  
>
> Sie müssen in dieser Buchungsgruppe die Nummer für ein Sammelkonto angeben, obwohl der Saldo auf diesem Konto immer 0 sein wird, nachdem Sie die Rechnung gebucht haben.  

## <a name="see-also"></a>Siehe auch

[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Neue Kunden registrieren](sales-how-register-new-customers.md)
[Finance](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
