---
title: 'Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr.| Microsoft Docs'
description: "Macht es für Debitoren einfacher, die Rechnungen durch Aktivierung des Zahlungsverkehrs zu bezahlen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5853080ef39196e95c293415e9b81502ff03d5ed
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a>Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr
Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Microsoft Pay, Paypal oder WorldPay zu bezahlen.  

Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können. Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsdokument zu bezahlen. Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Kunde in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.  

Der Microsoft Pay, Paypal-Zahlungs-Standard und die WorldPay-Zahlungsstandarderweiterungen werden installiert in [!INCLUDE[d365fin](includes/d365fin_md.md)] und stehen zur Aktivierung bereit.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungsverkehr** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Neu** aus.  
3. Wählen Sie die Zahlungsverkehr aus und schließen Sie dann das Fenster.  
4. Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Einrichten** aus.  
5. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Schließen Sie das Fenster.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.  
2. Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.  
3. Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.  

    > [!NOTE]  
    > Das Feld **Zahlungsverkehr** ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

