---
title: Neue Debitoren durch Erstellen einer Debitorenkarte registrieren
description: Beschreibt, wie eine Debitorenkarte erstellt wird, um Informationen zu jedem neuen Debitor oder Clients zu erfassen, an die Sie verkaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 3d014015946f9202d59127d6e871aa5dd0ec90bd
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588982"
---
# <a name="register-new-customers"></a>Neue Debitoren registrieren

Debitoren sind die Herkunft Ihres Einkommens. Sie müssen jeden Debitor, an den Sie verkaufen, als Debitorenkarte anlegen. Debitorenkarten enthalten die Informationen, die für den Verkauf von Produkten an Debitoren erforderlich sind." Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Debitorenkarten ausfüllen. Weitere Informationen finden Sie unter [Einrichten von Verkäufen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Hinzufügen neuer Kunden
Sie können neue Debitoren manuell hinzufügen, indem Sie die Felder auf der Seite **Kundenkarte** ausfüllen, oder Sie können Vorlagen verwenden, die vordefinierte Informationen enthalten. Sie können zum Beispiel Vorlagen für verschiedene Arten von Kundenprofilen erstellen. Die Verwendung von Vorlagen spart Zeit beim Hinzufügen neuer Kunden und hilft sicherzustellen, dass die Informationen jedes Mal korrekt sind. Wenn Sie Vorlagen für mehr als eine Art von Kunden erstellen, können Sie die Vorlage auswählen, die Sie beim Hinzufügen eines Kunden verwenden möchten. Wenn Sie nur eine Vorlage erstellen, wird diese für alle neuen Kunden verwendet. Nachdem Sie eine Vorlage erstellt haben, können Sie die Aktion **Vorlage anwenden** verwenden, um sie auf einen oder mehrere ausgewählte Kunden anzuwenden. Um eine Vorlage zu erstellen, geben Sie auf der Seite Kundenkarte die Informationen ein, die Sie wiederverwenden möchten, und speichern sie dann als Vorlage. Weitere Informationen finden Sie unter [Speichern der Kundenkarte als Vorlage](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template)

> [!TIP]
> Es kann hilfreich sein, die Seite **Kundenvorlage** zu personalisieren, wenn Sie eine Vorlage erstellen. Zum Beispiel können Sie das Feld **Kreditlimit** zu einer Vorlage hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Sie können einen Debitor auch aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [So erstellen Sie einen Kontakt als Debitor, Kreditor , Mitarbeiter oder Bankkonto von einem Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Erstellen Sie eine neue Debitorenkarte

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Die Aktion **Preise und Rabatte** bietet Optionen zur Verwaltung von Sonderpreisen oder Rabatten für den Debitor, wenn eine Bestellung bestimmte Kriterien erfüllt. Kriterien sind beispielsweise, wann sie einen bestimmten Artikel kaufen, eine Mindestmenge bestellen oder vor einem bestimmten Datum kaufen, etwa wenn eine Kampagne endet. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.

Wenn Sie diese Debitorenkarte als Vorlage verwenden möchten, fahren Sie fort, um sie als Debitorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.  

### <a name="to-save-the-customer-card-as-a-template"></a>Um die Debitorenkarte als Vorlage zu speichern

1. Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Debitor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit der Vorlage erstellt wurden.  
5. Wenn Sie die neue Debitorenvorlage abgeschlossen haben, wählen Sie die Schaltfläche **OK**.

Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

## <a name="deleting-customer-cards"></a>Löschen von Debitorenkarten

Wenn Sie eine Transaktion für einen Debitor gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Prüfung erforderlich sind. Um Debitorenkarten mit Posten zu löschen, wenden Sie sich an Ihren Microsoft-Partner, um dies über einen Code durchzuführen.  

## <a name="managing-credit-limits"></a>Kreditlimits verwalten

Kreditlimits, Restbeträge und Zahlungsbedingungen ermöglichen [!INCLUDE [prod_short](includes/prod_short.md)] die Anwendung eine Kreditlimitwarnung oder eine Warnung bei einem überfälligen Saldo anzeigt, wenn Sie einen Verkaufsauftrag anlegen.  Außerdem ermöglichen Ihnen die Funktionen für Mahnungs- und Zinskonditionen die Fakturierung von Zinsen und/oder Gebühren.  

Das Feld **Kreditlimit** auf einer Debitorenkarte gibt den Höchstbetrag an, mit dem der Kunde den Zahlungssaldo überschreiten darf, bevor Warnungen ausgegeben werden. Wenn Sie dann Informationen in Journale, Angebote, Bestellungen und Rechnungen eingeben, testet [!INCLUDE [prod_short](includes/prod_short.md)] den Verkaufskopf und die einzelnen Verkaufszeilen, um festzustellen, ob das Kreditlimit überschritten wurde.

Sie können jedoch weiterhin Buchungen vornehmen, auch wenn das Kreditlimit überschritten wird. Wenn Sie das Feld leer lassen, verfügt der Debitor über ein unbegrenztes Kreditlimit.  

Sie können festlegen, dass keine Warnungen angezeigt werden, die darauf hinweisen, dass das Kreditlimit des Kunden überschritten wurde, und Sie können angeben, welche Arten von Warnungen angezeigt werden sollen.

### <a name="to-specify-credit-limit-warnings"></a>So legen Sie Kreditlimitwarnungen fest

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.

2. Wählen Sie im Inforegister **Allgemein** im Feld **Kreditlimitwarnung** die entsprechende Option aus, wie in der folgenden Tabelle beschrieben:

    |Option| Beschreibung|
    |------|------------|
    |**Beide Warnungen**| Die Felder **Kreditlimit** und **Fälliger Saldo** auf der Debitorenkarte werden überprüft, und eine Warnung wird ausgegeben, falls der Debitor sein Kreditlimit überschritten hat oder sich im Zahlungsrückstand befindet.|
    |**Kreditlimit**|Der Wert im Feld **Kreditlimit** der Debitorenkarte wird mit dem Saldo des Debitors verglichen, und eine Warnung wird angezeigt, falls der Saldo des Debitors diesen Betrag übersteigt.|
    |**Fälliger Saldo**|Das Feld **Fälliger Saldo** auf der Debitorenkarte wird geprüft, und eine Warnung wird angezeigt, wenn sich der Debitor im Zahlungsrückstand befindet.|
    |**Keine Warnung**|Keine Warnungen werden über den Status des Debitors angezeigt.|

## <a name="see-also"></a>Siehe auch

[Zahlungsformen definieren](finance-payment-methods.md)  
[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
