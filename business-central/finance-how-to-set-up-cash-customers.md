---
title: 'Vorgehensweise: Einrichten von BarDebitoren | Microsoft Docs'
description: Dieses Thema beschreibt die Schritte, um Debitoren einzurichten, der in bar bezahlt.
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
ms.openlocfilehash: d122eaf5e7f898f2497b3cc0848309fb36fa62c1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "933955"
---
# <a name="set-up-cash-customers"></a>BarDebitoren einrichten
Sie können keine Rechnung ohne Debitorennummer erstellen. Dies trifft auch zu, wenn Sie einen Barverkauf tätigen und kein Debitorenkonto aktualisieren müssen.  

## <a name="to-set-up-a-cash-customer"></a>So richten Sie Bargelddebitoren ein:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.  
2.  Erstellen Sie eine neue Karte **Debitor**. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).
3.  Geben Sie im Feld **Nr.** Geben Sie beispielsweise **Bar** ein.  
4.  Geben Sie in dem Feld **Name** z. B. **BARVERKAUF** ein.  
5.  Füllen Sie auf dem Inforegister **Fakturierung** die Felder **Debitorenbuchungsgruppe** und **Geschäftsbuchungsgruppe** aus.  

 Sie haben jetzt einen neuen Debitor und die notwendigen Informationen für die Fakturierung eingerichtet.  

> [!NOTE]  
>  Es kann sein, dass Sie eine Buchungsgruppe gewählt haben, die auch für inländische Kreditverkäufe verwendet wird. Falls Sie gesonderte Daten für Barverkäufe benötigen, z. B. mit einem Verkaufs- oder Sammelkonto, können Sie zu diesem Zweck eine gesonderte Buchungsgruppe einrichten.  
>   
>  Sie müssen in dieser Buchungsgruppe die Nummer für ein Sammelkonto angeben, obwohl der Saldo auf diesem Konto immer 0 sein wird, nachdem Sie die Rechnung gebucht haben.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Neue Debitoren registrieren](sales-how-register-new-customers.md)    
[Finanzen](finance.md)  

