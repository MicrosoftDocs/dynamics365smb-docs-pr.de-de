---
title: 'Eine Einkaufsanfrage erstellen, um ein Angebot anzufordern'
description: 'Beschreibt, wie Verkaufsangebote oder eine Anforderung erstellt wird, um Ihr Angebot zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 08/08/2022
ms.author: edupont
---
# <a name="request-quotes" />Angebotsanforderungen

Eine Einkaufsanfrage kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung umgewandelt werden.

## <a name="create-a-purchase-quote" />Erstellen Sie eine Einkaufsanfrage

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsanfragen** ein und wählen Sie dann den entsprechenden Link.
2. Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen. Erfahren Sie mehr unter [Einkäufe aufzeichnen](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order" />Konvertieren Sie eine Einkaufsanfrage in eine Einkaufsbestellung

Wenn Sie das Angebot akzeptiert haben, können Sie diese mit einer Einkaufsrechnung umwandeln, um den Einkauf zu verarbeiten.

1. Öffnen Sie eine Einkaufsanfrage, die Sie umzuwandeln möchten, und wählen Sie die **Bestellung erst.** Aktion aus.

Das Verkaufsangebot wird aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können und dann die Verkaufsrechnung buchen. In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags und der Rechnung, aus der sie erstellt wurde.

> [!NOTE]
> Es ist nicht möglich, ein Einkaufsangebot direkt in eine Einkaufsrechnung umzuwandeln, wie dies bei Verkaufsangeboten möglich ist. Einzelheiten zum Erstellen einer Einkaufsrechnung finden Sie unter [Erfassen Sie Einkäufe mit Einkaufsrechnungen](purchasing-how-record-purchases.md).

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-purchase-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
