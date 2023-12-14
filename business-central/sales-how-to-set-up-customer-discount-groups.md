---
title: Debitorenrabattgruppen einrichten
description: 'Erfahren Sie, wie Sie Debitorenrabattgruppen festlegen und Verkaufszeilenrabatte für diese Gruppen erstellen.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: bholtorf
---
# <a name="set-up-customer-discount-groups"></a>Debitorenrabattgruppen einrichten

Sie können Verkaufszeilenrabatte für eine Gruppe von Debitoren definieren, anstatt sie einzeln anzuwenden.

**Debitorenrabattgruppen** funktionieren ähnlich wie [Debitorenpreisgruppen](sales-how-to-set-up-customer-price-groups.md), können jedoch mit Artikelrabattgruppen kombiniert werden, um für ausgewählte Debitoren schnell Zeilenrabatte für viele Artikel festzulegen.

## <a name="create-sales-line-discounts-for-a-customer-group"></a>Verkaufszeilenrabatte für eine Debitorgruppe erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol, geben Sie **Debitorenpreisgruppen** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Debitorenpreisgruppen** die Option **Neu** aus, um eine neue Rabattgruppe zu erstellen und ihr unter der Spalte **Code** einen Namen zu geben und eine Beschreibung hinzuzufügen.
3. Wählen Sie die Aktion **Navigieren** und die Option **Verkaufszeilenrabatte** aus.
4. Füllen Sie die Spalte **Verkaufscode** mit der Rabattgruppe aus, die auf der vorherigen Seite erstellt wurde.
5. Füllen Sie in den Zeilen die Felder mit **Typ** (Artikel oder Artikelrabattgruppe), **Code**, **Einheitencode** und **Zeilenrabatt %** aus.
6. Falls der Debitor eine bestimmte Menge kaufen muss, um den Rabattprozentsatz zu erhalten, füllen Sie das Feld **Mindestmenge** aus.
7. Geben Sie bei Bedarf das **Startdatum** und **Enddatum** für die Rabattgruppe ein.
8. Falls relevant, können Sie auch den **Währungscode** oder **Variantencode** nach dem [Personalisieren der Spalten](ui-personalization-user.md) festlegen.

Wiederholen Sie die Schritte 4 bis 8 für jeden Artikel oder für jede Artikelrabattgruppe, für die Sie einen Verkaufszeilenrabatt erstellen möchten.

## <a name="assign-a-customer-to-a-discount-group"></a>Einen Debitor einer Rabattgruppe zuweisen

Nachdem Sie die Debitorenrabattgruppen festgelegt haben, können Sie die Debitorenrabattgruppen-Codes auf den Debitorenkarten eingeben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Kunden** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die **Debitorenkarte** für einen Debitoren, der Teil einer Debitorenrabattgruppe sein soll.
3. Wählen Sie im Inforegister **Fakturierung** im Feld **Debitorenrabattgruppe** den Gruppencode aus.

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Erfassen von Sonderverkaufspreisen und Rabatten](sales-how-record-sales-price-discount-payment-agreements.md)  
[Einrichten von Debitorenpreisgruppen](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
