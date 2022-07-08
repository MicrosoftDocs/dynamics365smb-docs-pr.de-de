---
title: Zahlungsformen festlegen (enthält Video)
description: Sie können Zahlungsformen nutzen, z.B. Banküberweisung, Kasse oder PayPal, um festzulegen, wie eine Rechnung bezahlt wird.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.search.form: 427
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5cf88736711667a18a43e75bc70533de5c924ad2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076591"
---
# <a name="set-up-payment-methods"></a>Einrichten von Zahlungsformen

Zahlungsformen definieren die Art, wie Sie es vorziehen, dass Debitoren Sie zahlen und wie Sie den Kreditoren bezahlen können. Die Methode kann für jeden Debitor oder Kreditor variieren. Beispiele für typische Zahlungsformen sind **Bankkonten**, **Bargeld**, **Check** oder **Konto**.

Sie können eine Zahlungsform Debitoren und Kreditoren zuweisen, sodass dasselbe Verfahren immer auf Verkaufs- und Einkaufsbelegen verwendet wird, die Sie für sie einrichten. Bei Bedarf können Sie die Methode im Einkaufs- und Verkaufsbeleg ändern. Wenn Sie beispielsweise eine bestimmte Einkaufsrechnung in bar anstatt mit Scheck bezahlen möchten. Dies verändert nicht die standardmäßige Zahlungsform, die dem Kreditor zugeordnet ist.

Die gleichen Zahlungsformen werden für Einkaufs- und Verkaufsbelegen verwendet. Beispielsweise wird eine _cash_ Zahlungsform verwendet, wenn Sie Zahlungen leisten und wenn Sie den Wareneingang erhalten. [!INCLUDE[prod_short](includes/prod_short.md)] weiß, dass wenn Sie eine Verkaufsrechnung erstellen, Sie eine Zahlung erwarten und das Gegenteil der Einkaufsrechnungen ist.

Gutschriften für Reklamationen sind jedoch Ausnahmen, da Geld entgegengesetzt fließt, von Ihnen an Ihren Kunden und von Ihrem Lieferanten an Sie. Daher wird eine standardmäßige Zahlungsform nicht den Gutschriften zugeordnet. Es gibt eine Problemumgehung, wenn Sie Zahlungsfristen des Debitors oder Kreditors angegeben haben. Auch wenn das **Rechnungsrab. Zahl. Verk. im Zinsrechnung** Feld nicht für dies beabsichtigt ist, wenn Sie das Feld **Zahlungsbedingungen** auswählen, wird eine standardmäßige Zahlungsform hinzugefügt, wenn Sie eine Gutschrift erstellen. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>So richten Sie eine Zahlungsform ein

[!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Zahlungsformen, die Geschäfte häufig verwenden. Sie können so viele Zeilen hinzufügen, wie Sie benötigen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsformen** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Fügen Sie Ihren Zahlungsbedingungen optional Ihre Zahlungsform hinzu. Weitere Informationen finden Sie unter [Einrichten von Zahlungbedingungen](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>So weisen Sie einem Kreditor eine Zahlungsform zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.
2. Im **Zahlungsformcode** Feld wählen Sie die Methode, die Sie für den Debitor oder Kreditor standardmäßig verwenden möchten.

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  
[Zahlungsbedingungen einrichten](finance-payment-terms.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]