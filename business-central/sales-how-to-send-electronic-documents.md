---
title: Elektronische Belege senden
description: Erfahren Sie, wie man Rechnungen elektronisch sendet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 43f61682a1068a8e1652fd28421f83d5291c8fe8
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827068"
---
# <a name="send-electronic-documents"></a>Elektronische Belege senden

Die allgemeine Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das Senden von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, einem Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird. Ein Anbieter von Belegaustauschdiensten leitet elektronische Belege zwischen Handelspartnern weiter. Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.  

 In der allgemeinen Version von [!INCLUDE[prod_short](includes/prod_short.md)] ist ein vorkonfigurierter Belegaustauschdienst enthalten, der für Ihren Mandanten eingerichtet werden kann. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md). In einigen Fällen müssen Sie jedoch eine App installieren. Weitere Informationen finden Sie unter [Elektronische Rechnung FAQ](faq-electronic-invoicing.yml).  

 Um beispielsweise Verkaufsrechnungen als elektronischen PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronisches Dokument** im **Buchen und senden**-Dialogfeld aus. Dort können Sie außerdem das standardmäßige Belegsendeprofil für den Kunden vom Dialogfeld einrichten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [Einrichten von Senden und Empfangen von elektronischen Dokumenten](across-how-to-set-up-electronic-document-sending-and-receiving.md)in Elemente in der ausgehenden Dokumentdatei konvertiert werden.  

### <a name="to-send-an-electronic-sales-invoice"></a>So senden Sie eine elektronische Verkaufsrechnung

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun") aus, geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  

2. Erstellen Sie eine neue Verkaufsrechnung.  

3. Wenn die Verkaufsrechnung fakturierbar ist, wählen Sie die Aktion **Buchen und Senden**.  

     Wenn das Standard-Sendeprofil des Kunden lautet **Elektronisches Dokument**, dann wird es im Dialogfeld **Bestätigung buchen und senden** angezeigt. Auf diese Weise müssen Sie nur die Schaltfläche **Ja** zum Buchen und Versenden der Rechnung elektronisch im ausgewählten Format auswählen.  

4. Wählen Sie im Dialogfeld **Buchungs- und Sendebestätigung** die AssistEdit-Schaltfläche rechts vom Feld **Beleg senden an** aus.  

5. Wählen Sie im Dialgofeld **Beleg senden an** im Feld **Elektronischer Beleg** die Option **Über Belegaustauschdienst** aus.  

6. Wählen Sie im Feld **Format** die Option **PEPPOL** aus.  

7. Wählen Sie die Schaltfläche **OK** aus. Das Dialogfeld **Buchungs- und Sendebestätigung** wird angezeigt. **Elektronischer Beleg (PEPPOL)** wird im Feld **Beleg senden an** hinzugefügt.  

8. Wählen Sie die Schaltfläche **Ja** aus.  

     Die Verkaufsrechnung wird gebucht und als elektronischer Beleg im PEPPOL-Format an den Debitor gesendet.  

    > [!NOTE]  
    >  Sie können auch eine gebuchte Verkaufsrechnung als elektronischen Beleg senden. Dieser Vorgang ist derselbe wie im Thema für nicht gebuchte Verkaufsbelege beschrieben. Wählen Sie auf der Seite **gebuchte Verkaufsrechnung** die Aktion **Aktivitätsprotokoll**, um den Status des elektronischen Dokuments anzuzeigen.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Belegsendeprofile einrichten](sales-how-setup-document-send-profiles.md)  
[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[So richten Sie einen Belegaustauschdienst ein](across-how-to-set-up-a-document-exchange-service.md)  
[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Elektronische Rechnungsstellung FAQ](faq-electronic-invoicing.yml)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
