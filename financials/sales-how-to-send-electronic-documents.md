---
title: Senden Sie elektronische Belege | Microsoft Docs
description: Erfahren Sie, wie man Rechnungen elektronisch sendet.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fae5e37b8f1fcca84a474b2eac2039f7fc6d8245
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="send-electronic-documents"></a>Elektronische Belege senden
Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Senden von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird. Ein Anbieter von Belegaustauschdiensten leitet elektronische Belege zwischen Handelspartnern weiter. Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.  

 In der allgemeinen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] ist ein vorkonfigurierter Belegaustauschdienst enthalten, der für Ihren Mandanten eingerichtet werden kann. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).  

 Um eine Verkaufsrechnung als elektronischen PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronischer Beleg** im Dialogfeld **Buchen und Senden** aus. Hier können Sie auch das standardmäßige Belegsendeprofil für den Debitor einrichten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [Einrichten von Senden und Empfangen von elektronischen Dokumenten](across-how-to-set-up-electronic-document-sending-and-receiving.md)in Elemente in der ausgehenden Dokumentdatei konvertiert werden.  

### <a name="to-send-an-electronic-sales-invoice"></a>So senden Sie eine elektronische Verkaufsrechnung  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.  

2.  Erstellen Sie eine neue Verkaufsrechnung.  

3.  Wenn die Verkaufsrechnung fakturiert werden kann, wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Buchung** die Option **Buchen und Senden** aus.  

     Wenn das Standardsendeprofil des Debitors **Elektronischer Beleg** lautet, wird es im Dialogfeld **Buchungs- und Sendebestätigung** angezeigt, und Sie müssen nur die Schaltfläche **Ja** auswählen, um die Rechnung im ausgewählten Format elektronisch zu buchen und zu senden.  

4.  Wählen Sie im Dialogfeld **Buchungs- und Sendebestätigung** die AssistEdit-Schaltfläche rechts vom Feld **Beleg senden an** aus.  

5.  Wählen Sie im Dialgofeld **Beleg senden an** im Feld **Elektronischer Beleg** die Option **Über Belegaustauschdienst** aus.  

6.  Wählen Sie im Feld **Format** die Option **PEPPOL** aus.  

7.  Wählen Sie die Schaltfläche **OK** aus. Das Dialogfeld **Buchungs- und Sendebestätigung** wird angezeigt. **Elektronischer Beleg (PEPPOL)** wird im Feld **Beleg senden an** hinzugefügt.  

8.  Wählen Sie die Schaltfläche **Ja** aus.  

     Die Verkaufsrechnung wird gebucht und als elektronischer Beleg im PEPPOL-Format an den Debitor gesendet.  

    > [!NOTE]  
    >  Sie können auch eine gebuchte Verkaufsrechnung als elektronischen Beleg senden. Dieser Vorgang ist derselbe wie im Thema für nicht gebuchte Verkaufsbelege beschrieben. Aktivieren Sie im Fenster **Gebuchte Verkaufsrechung** auf der Registerkarte **Aktionen** in der Gruppe **Allgemein** die Option **Aktivitätsprotokoll**, um den Status des elektronischen Belegs anzuzeigen. Weitere Informationen finden Sie unter **Aktivitätsprotokoll**  

## <a name="see-also"></a>Siehe auch  
[Verkaufsrechnung](sales-how-invoice-sales.md)  
[Belegsendeprofile einrichten](sales-how-setup-document-send-profiles.md)  
[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[So richten Sie einen Belegaustauschdienst ein](across-how-to-set-up-a-document-exchange-service.md)  
[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

