---
title: Einrichten von Zahlungsformen
description: Sie können Zahlungsformen nutzen, z.B. Banküberweisung, Kasse oder Paypal, um festzulegen, wie eine Rechnung bezahlt wird.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1e836b43392cd915a77c5ee85d5a322753dcd5df
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773955"
---
# <a name="set-up-payment-methods"></a>Einrichten von Zahlungsformen

Zahlungsformen definieren die Art, wie Sie es vorziehen, dass Debitoren Sie zahlen und wie Sie den Kreditoren bezahlen können. Die Methode kann für jeden Debitor oder Kreditor variieren. Beispiele für typische Zahlungsformen sind **Bankkonten**, **Bargeld**, **Check** oder **Konto**.

Sie können eine Zahlungsform Debitoren und Kreditoren zuweisen, sodass dasselbe Verfahren immer auf Verkaufs- und Einkaufsbelegen verwendet wird, die Sie für sie einrichten. Bei Bedarf können Sie die Methode im Einkaufs- und Verkaufsbeleg ändern. Wenn Sie beispielsweise eine bestimmte Einkaufsrechnung in bar anstatt mit Scheck bezahlen möchten. Dies verändert nicht die standardmäßige Zahlungsform, die dem Kreditor zugeordnet ist.

Die gleichen Zahlungsformen werden für Einkaufs- und Verkaufsbelegen verwendet. Beispielsweise wird eine _cash_ Zahlungsform verwendet, wenn Sie Zahlungen leisten und wenn Sie den Wareneingang erhalten. [!INCLUDE[prod_short](includes/prod_short.md)] weiß, dass wenn Sie eine Verkaufsrechnung erstellen, Sie eine Zahlung erwarten und das Gegenteil der Einkaufsrechnungen ist.

Gutschriften für Reklamationen sind jedoch Ausnahmen, da Geld entgegengesetzt fließt, von Ihnen an Ihren Kunden und von Ihrem Lieferanten an Sie. Daher wird eine standardmäßige Zahlungsform nicht den Gutschriften zugeordnet. Es gibt eine Problemumgehung, wenn Sie Zahlungsfristen des Debitors oder Kreditors angegeben haben. Auch wenn das **Rechnungsrab. Zahl. Verk. im Zinsrechnung** Feld nicht für dies beabsichtigt ist, wenn Sie das Feld **Zahlungsbedingungen** auswählen, wird eine standardmäßige Zahlungsform hinzugefügt, wenn Sie eine Gutschrift erstellen. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>So richten Sie eine Zahlungsform ein

[!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Zahlungsformen, die Geschäfte häufig verwenden. Sie können so viele Zeilen hinzufügen, wie Sie benötigen.

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun"), geben Sie **Zahlungsformen** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Fügen Sie Ihren Zahlungsbedingungen optional Ihre Zahlungsform hinzu. Weitere Informationen finden Sie unter [Einrichten von Zahlungbedingungen](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>So weisen Sie einem Kreditor eine Zahlungsform zu

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Kunde** oder **Lieferant** ein und wählen Sie dann den entsprechenden Link.
2. Im **Zahlungsformcode** Feld wählen Sie die Methode, die Sie für den Debitor oder Kreditor standardmäßig verwenden möchten.

## <a name="see-also"></a>Siehe auch

[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  
[Zahlungsbedingungen einrichten](finance-payment-terms.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]