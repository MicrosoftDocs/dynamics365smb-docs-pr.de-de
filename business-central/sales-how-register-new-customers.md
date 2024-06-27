---
title: Neue Debitoren durch Erstellen einer Debitorenkarte registrieren
description: 'Beschreibt, wie eine Debitorenkarte erstellt wird, um Informationen zu jedem neuen Debitor oder Clients zu erfassen, an die Sie verkaufen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 02/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Neue Debitoren registrieren

Debitoren sind Ihre Einkommensquelle. Sie müssen jeden Debitor, an den Sie verkaufen, als Debitorenkarte anlegen. Debitorenkarten enthalten die Informationen, die für den Verkauf von Produkten an Debitoren erforderlich sind. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](sales-how-invoice-sales.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie wählen können, wenn Sie Debitorenkarten ausfüllen. Erfahren Sie mehr unter [Einkauf einrichten](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## Neue Debitoren hinzufügen

Sie können neue Debitoren manuell hinzufügen, indem Sie die Seite **Kundenkarte** ausfüllen, oder Sie können Vorlagen verwenden, die vordefinierte Informationen enthalten. Sie können zum Beispiel eine Vorlage für verschiedene Arten von Kundenprofilen erstellen. Die Verwendung von Vorlagen spart Zeit beim Hinzufügen neuer Kunden und hilft sicherzustellen, dass die Informationen jedes Mal korrekt sind. 

Wenn Sie erstellen:
* Mehrere Vorlagen für mehr als eine Art von Kunden, können Sie die Vorlage auswählen, die Sie beim Hinzufügen eines Kunden verwenden möchten, können Sie eine passende Vorlage auswählen.
* Nur eine Vorlage, wird für alle diese neuen Debitoren verwendet. 

Nachdem Sie eine Vorlage erstellt haben, können Sie die Aktion **Vorlage anwenden** verwenden, um sie auf einen oder mehrere ausgewählte Kunden anzuwenden. Um eine Vorlage zu erstellen, geben Sie die Informationen, die Sie wiederverwenden möchten, auf der Seite **Kreditorenkarte** ein und speichern sie dann als Vorlage. Weitere Informationen finden Sie unter [Speichern der Debitorenkarte als Vorlage](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Es kann hilfreich sein, die Seite **Kundenvorlage** zu personalisieren, wenn Sie eine Vorlage erstellen. Zum Beispiel können Sie das Feld **Kreditlimit** zu einer Vorlage hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode).

Sie können einen Debitor auch aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [Erstellen eines Kunden, Kreditors, Mitarbeiters oder Bankkontos über einen Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### Erstellen Sie eine neue Debitorenkarte

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Die Aktion **Preise und Rabatte** bietet Optionen zur Verwaltung von Sonderpreisen oder Rabatten für einen Debitor, wenn eine Bestellung bestimmte Kriterien erfüllt. Beispiele für solche Kriterien sind wann sie einen bestimmten Artikel kaufen, eine Mindestmenge für die Bestellung oder der Kauf vor einem bestimmten Datum. Erfahren Sie mehr unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md).

Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.  

### Um die Debitorenkarte als Vorlage zu speichern

Sie können eine Debitorenkarte als Vorlage verwenden, wenn Sie neue Debitorenkarten erstellen.

1. Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Debitor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit dieser Vorlage erstellt wurden.  
5. Wenn Sie mit der neuen Debitorenvorlage fertig sind, wählen Sie **OK**.

Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, und Sie können diese verwenden, um neue Debitorenkarten zu erstellen.

## Debitorenkarten löschen

Wenn Sie eine Transaktion für einen Debitor buchen, können Sie die Debitorenkarte nicht löschen, da die Posten möglicherweise für die Prüfung erforderlich sind. Um Debitorenkarten mit Posten zu löschen, wenden Sie sich an Ihren Microsoft-Partner, um dies über einen Code durchzuführen.  

## Kreditlimits verwalten

Kreditlimits, Restbeträge und Zahlungsbedingungen ermöglichen [!INCLUDE [prod_short](includes/prod_short.md)] die Anwendung eine Kreditlimitwarnung oder eine Warnung bei einem überfälligen Saldo anzeigt, wenn Sie einen Verkaufsauftrag anlegen. Außerdem ermöglichen Ihnen die Funktionen für Mahnungs- und Zinskonditionen die Fakturierung von Zinsen und/oder extra Gebühren.  

Das Feld **Kreditlimit** auf einer Debitorenkarte gibt den Höchstbetrag an, mit dem der Kunde den Zahlungssaldo überschreiten darf, bevor Warnungen ausgegeben werden. Wenn Sie Informationen in Journale, Angebote, Bestellungen und Rechnungen eingeben, testet [!INCLUDE [prod_short](includes/prod_short.md)] den Verkaufskopf und die einzelnen Verkaufszeilen, um festzustellen, ob das Kreditlimit überschritten wurde.

Sie können jedoch weiterhin Buchungen vornehmen, wenn das Kreditlimit überschritten wird. Ein leeres Feld bedeutet, dass der Debitor über ein unbegrenztes Kreditlimit verfügt.  

Sie können festlegen, dass keine Warnungen angezeigt werden, wenn das Kreditlimit des Debitors überschritten wurde, und Sie können angeben, welche Arten von Warnungen angezeigt werden sollen.

### So legen Sie Kreditlimitwarnungen fest

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.

2. Wählen Sie im Inforegister **Allgemein** im Feld **Kreditlimitwarnung** die entsprechende Option aus, wie in der folgenden Tabelle beschrieben:

    |Option| Beschreibung|
    |------|------------|
    |**Beide Warnungen**| Die Felder **Kreditlimit** und **Fälliger Saldo** auf der Debitorenkarte werden überprüft, und eine Warnung wird ausgegeben, falls der Debitor sein Kreditlimit überschritten hat oder sich im Zahlungsrückstand befindet.|
    |**Kreditlimit**|Der Wert im Feld **Kreditlimit** der Debitorenkarte wird mit dem Saldo des Debitors verglichen, und eine Warnung wird angezeigt, falls der Saldo des Debitors diesen Betrag übersteigt.|
    |**Fälliger Saldo**|Das Feld **Fälliger Saldo** auf der Debitorenkarte wird geprüft, und eine Warnung wird angezeigt, wenn sich der Debitor im Zahlungsrückstand befindet.|
    |**Keine Warnung**|Keine Kreditwarnungen werden über den Status des Debitors angezeigt.|

## Verkaufenden zuweisen

Sie können Verkaufende der Lieferadresse des Debitoren statt der Rechnungsadresse zuweisen, sodass Ihre Verkaufsberichte die tatsächliche geografische Verteilung Ihrer Verkäufe widerspiegeln. Durch die Zuweisung eines Verkaufenden zur Lieferadresse eines Debitoren erhalten Sie präzisere Einblicke und können die Ressourcenzuweisung optimieren.

Beauftragen Sie einen Verkaufenden mit der **Kunden**-Kartenseite, indem Sie **Kunde** und dann **Lieferadressen** zum Öffnen der Seite **Liste der Lieferadressen**. Wählen Sie **Verwalten** und dann **Bearbeiten** zum Öffnen der Kartenseite **Lieferadresse**. Geben Sie ein oder wählen Sie einen **Verkäufercode** aus, um den Verkaufenden auszuwählen.

Wenn Sie die Option **Alternative Lieferadresse** als **Lief. an**-Standort auf einem Verkaufsbeleg auswählen, wird der **Verkäufercode** aktualisiert, damit er zum Verkaufenden aus **Lief. an** statt der **Rech. an**-Adresse passt. 

## Siehe auch

[Zahlungsformen definieren](finance-payment-methods.md)  
[Doppelte Datensätze zusammenführen](sales-how-merge-duplicate-records.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Teillieferungen mit Lieferavis aktivieren](sales-how-send-partial-shipments.md)  
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verwenden Sie Online-Karten, um Standorte und Wegbeschreibungen zu finden](across-online-maps.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
