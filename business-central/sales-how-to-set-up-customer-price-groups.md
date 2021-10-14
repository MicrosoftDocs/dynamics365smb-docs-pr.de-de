---
title: Kundenpreisgruppen festlegen
description: Erfahren Sie, wie Sie Kundenpreisgruppen festlegen und Verkaufspreise für diese Gruppen erstellen.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer price groups, discounts, sales prices
ms.date: 09/30/2021
ms.author: a-jillk
ms.openlocfilehash: e00af84992274fd627735624b313940874966338
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589422"
---
# <a name="set-up-customer-price-groups"></a>Kundenpreisgruppen festlegen
  
Die Verkaufspreise können von den Kundengruppen, an die Sie verkaufen, abhängig gemacht werden. Diese werden als Debitorenpreisgruppen bezeichnet.

Bevor Sie Kundenpreisgruppen festlegen, müssen Sie entscheiden, wie viele Gruppen Sie haben möchten und welche Kunden zu den einzelnen Gruppen gehören werden.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>So erstellen Sie Verkaufspreise für eine Gruppe von Kunden  

Wenn Sie sich auf die Preise geeinigt haben, die die Gruppe von Kunden für bestimmte Artikel zahlen wird, registrieren Sie die Vereinbarung für die einzelnen Artikel in den Zeilen auf der Seite **Verkaufspreise**.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Um Verkaufspreise für eine Gruppe von Kunden zu erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Kundenpreisgruppen** ein und wählen Sie dann den entsprechenden Link.  

2. Wählen Sie die Zeile für die Kundenpreisgruppe aus. Wenn eine Zeile noch nicht vorhanden ist, können Sie eine neue Zeile erstellen. Wählen Sie **Neu**, um eine neue Entität zu erstellen und ihr einen Namen zu geben.  
    
    Überprüfen Sie für die ausgewählte Zeile den Inhalt der Felder **Zeile zulassen**, **Rechnung zulassen**, **Preis inkl. MwSt.** und **Steuer Bus. Posting Gr. (Preis)**. 
  
3. Wählen Sie die Aktion **Navigieren**, und wählen Sie **Verkaufspreise**. Die Seite **Verkaufspreise** wird geöffnet. Das Feld **Verkaufstyp** wird mit **Debitorenpreisgruppe** ausgefüllt.  
  
4. Füllen Sie das Feld **Verkaufscode** mit dem Verkaufscode aus, den Sie auf der vorherigen Seite ausgewählt haben.  
  
5. Füllen Sie die Felder in den Zeilen mit der **Artikel Nr.**, **Maßeinheit Code** und dem vereinbarten **Maßeinheitspreis** aus. Sie können auch die Spalte **Variantencode** einblenden und den **Variantencode** angeben, wenn es mehrere Varianten des Elements gibt.  
  
6. Wenn die Kundengruppe eine Mindestmenge kaufen muss, um den vereinbarten Preis zu erhalten, füllen Sie das Feld **Minimalmenge** aus.  

7. Geben Sie bei Bedarf das **Beginndatum** und **Ende-Datum** der Preisvereinbarung ein.  
  
8. Falls relevant, können Sie auch den **Währungscode** angeben.

Wiederholen Sie die Schritte 4 bis 8 für jedes Element, für das Sie einen Verkaufspreis erstellen möchten.

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>So geben Sie Debitorenpreisgruppen-Codes auf Kundenkarten ein  

Nachdem Sie die Kundenpreisgruppen festgelegt haben, können Sie die Kundenpreisgruppen-Codes auf den Kundenkarten eingeben.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Um Kundenpreisgruppen-Codes auf einer Kundenkarte einzugeben  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Kunden** ein und wählen Sie dann den entsprechenden Link.  

2. Öffnen Sie die entsprechende **Kundenkarte** für einen Kunden, der Teil einer Debitorenpreisgruppe sein soll.  

3. Wählen Sie auf dem Inforegister **Fakturierung** im Feld **Debitorenpreisgruppe** den Code **Debitorenpreisgruppe**.  


## <a name="see-also"></a>Weitere Informationen

[Spezielle Verkaufspreise und Rabatte aufzeichnen](sales-how-record-sales-price-discount-payment-agreements.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
