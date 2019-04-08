---
title: 'Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr.| Microsoft Docs'
description: Macht es für Debitoren einfacher, die Rechnungen durch Aktivierung des Zahlungsverkehrs zu bezahlen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: eac58a651989fff8b1d2cc6b6dbed2a380ae8ef8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "797930"
---
# <a name="enable-customer-payments-through-payment-services"></a>Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr
Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Microsoft Pay, Paypal oder WorldPay zu bezahlen.  

Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können. Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsdokument zu bezahlen. Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Debitor in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.  

Der Microsoft Pay, PayPal Payments Standard und die WorldPay Payments Standard-Erweiterungen werden installiert in [!INCLUDE[d365fin](includes/d365fin_md.md)] und stehen zur Aktivierung bereit.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungsverkehr** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Neu** aus.  
3. Wählen Sie die Zahlungsverkehr aus und schließen Sie dann die Seite.  
4. Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Einrichten** aus.  
5. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Schließen Sie die Seite.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsrechnung** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.  
3. Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.  

    > [!NOTE]  
    > Das Feld **Zahlungsverkehr** ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
