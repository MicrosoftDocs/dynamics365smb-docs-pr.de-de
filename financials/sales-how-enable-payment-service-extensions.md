---
title: 'Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr.| Microsoft Docs'
description: "Macht es für Debitoren einfacher, die Rechnungen durch Aktivierung des Zahlungsverkehrs zu bezahlen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 769fd885e5c6070f8a4f6c9082900ea7f5f6ab8d
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr
<a id="how-to-enable-customer-payments-through-payment-services" class="xliff"></a>
Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Paypal oder WorldPay zu bezahlen.  

Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können. Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsdokument zu bezahlen. Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Kunde in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.  

Der Paypal-Zahlungs-Standard und die WorldPay-Zahlungsstandarderweiterungen werden erfasst in [!INCLUDE[d365fin](includes/d365fin_md.md)] und stehen zur Aktivierung bereit.  

## Einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren
<a id="to-enable-a-payment-service-in-included365finincludesd365finmdmd" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungsverkehr** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Neu** aus.  
3. Wählen Sie die Zahlungsverkehr aus und schließen Sie dann das Fenster.  
4. Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Einrichten** aus.  
5. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Schließen Sie das Fenster.  

## Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen
<a id="to-select-a-payment-service-on-a-sales-invoice" class="xliff"></a>
1. Auf der Startseite wählen Sie **Verkaufsrechnung** aus.  
2. Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.  
3. Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.  
  
    **Hinweis**: Das **Zahlungsverkehr** Feld ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.  

## Siehe auch
<a id="see-also" class="xliff"></a>  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Erweiterungen] (ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

