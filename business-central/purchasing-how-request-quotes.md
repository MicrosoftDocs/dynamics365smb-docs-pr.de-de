---
title: 'Eine Einkaufsanfrage erstellen, um ein Angebot anzufordern'
description: 'Beschreibt, wie Verkaufsangebote oder eine Anforderung erstellt wird, um Ihr Angebot zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="request-quotes"></a>Angebote anfordern

Eine Einkaufsanfrage kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung umgewandelt werden.

## <a name="create-a-purchase-quote"></a>Erstellen Sie eine Einkaufsanfrage

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsanfragen** ein und wählen Sie dann den entsprechenden Link.
2. Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen. Erfahren Sie mehr unter [Einkäufe aufzeichnen](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Konvertieren Sie eine Einkaufsanfrage in eine Einkaufsbestellung

Wenn Sie das Angebot akzeptiert haben, können Sie diese mit einer Einkaufsrechnung umwandeln, um den Einkauf zu verarbeiten.

1. Öffnen Sie eine Einkaufsanfrage, die Sie umzuwandeln möchten, und wählen Sie die **Bestellung erst.** Aktion aus.

Das Verkaufsangebot wird aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können und dann die Verkaufsrechnung buchen. In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags und der Rechnung, aus der sie erstellt wurde.

> [!NOTE]
> Es ist nicht möglich, ein Einkaufsangebot direkt in eine Einkaufsrechnung umzuwandeln, wie dies bei Verkaufsangeboten möglich ist. Einzelheiten zum Erstellen einer Einkaufsrechnung finden Sie unter [Erfassen Sie Einkäufe mit Einkaufsrechnungen](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Belege per E-Mail senden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
