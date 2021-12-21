---
title: Vorauszahlungen einrichten
description: Hier erfahren Sie, wie Sie Business Central so konfigurieren, dass Sie Vorauszahlungen verwenden können, um Rechnungen zu erstellen und Kautionen von Debitoren einzuziehen und Kautionen an Kreditoren zu überweisen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keyword: prepayment
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: a09f0cd35c62b65bf690fd785c0fc9a4b4b178d7
ms.sourcegitcommit: 4223484b0eeceb0258dae5abfd04e1a9a4a0990d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7889820"
---
# <a name="set-up-prepayments"></a>Vorauszahlungen einrichten

Wenn Sie von Ihren Debitoren erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten oder wenn der Kreditor von Ihnen eine Vorauszahlung vor Lieferung erwartet, können Sie die Funktion "Vorauszahlung" verwenden. Die Vorauszahlungsfunktionalität ermöglicht es Ihnen, von Debitoren geforderte Kautionen in Rechnung zu stellen und einzuziehen oder Kautionen an Kreditoren zu überweisen, um sicherzustellen, dass alle Teilzahlungen gegen eine Rechnung gebucht werden. Weitere Informationen finden Sie unter [Vorauszahlungsrechnungen erstellen](finance-how-to-create-prepayment-invoices.md).

Damit Vorauszahlungsrechnungen gebucht werden können, müssen in der Finanzbuchhaltung zunächst die Buchungskosten sowie die Nummernserien für Vorauszahlungsbelege eingerichtet werden. Sie müssen ein Konto für Vorauszahlungen im Zusammenhang mit Verkäufen und ein Konto für Vorauszahlungen im Zusammenhang mit dem Einkauf angeben. Sie können dieselben Buchungskonten angeben, die für alle Vorauszahlungen für alle allgemeinen Geschäftsbuchungsgruppen oder allgemeinen Produktbuchungsgruppen verwendet werden sollen, oder Sie können bestimmte Konten für bestimmte Buchungsgruppen für den Verkauf bzw. Einkauf angeben. Dies hängt von den Anforderungen Ihres Unternehmens zur Nachverfolgung von Vorauszahlungen ab.  

Sie können den Prozentsatz des zur Zahlung fakturierten Zeilenbetrags für einen Debitor, einen Kreditor, für alle Artikel oder für ausgewählte Artikel definieren. Nach dem Festlegen der Einstellungen können Vorauszahlungsrechnungen auf der Grundlage von Aufträgen und Bestellungen generiert werden. Sie können für jede Verkaufs- oder Einkaufszeile entweder die standardmäßigen Prozentsätze verwenden oder die Beträge der Rechnungen gemäß Ihren Anforderungen anpassen. So können Sie beispielsweise einen Gesamtbetrag für den gesamten Auftrag angeben.  

> [!NOTE]
> Wir empfehlen, in den folgenden Fällen keinen Vorauszahlungsprozentsatz von 100 % zu verwenden:
>
> * Wenn Sie sich in Nordamerika befinden. Aufgrund der Berechnung der Steuern kann ein Vorauszahlungsprozentsatz von 100 % zu Problemen mit Vorauszahlungsrechnungen führen.
> * In allen Regionen, wenn Sie manuell ein Skonto von der Rechnung abziehen. Bei einem Vorauszahlungsprozentsatz von 100 % verbleibt nicht automatisch ein Betrag, von dem das Skonto abgezogen werden kann. 

Da der vorausgezahlte Betrag Eigentum des Käufers ist, bis dieser die Ware oder die Leistung erhalten hat, müssen Sie Sachkonten einrichten, auf denen die Vorauszahlungsbeträge bis zur Buchung der abschließenden Rechnung erfasst werden. Vorauszahlungen für Verkaufsaufträge müssen auf einem Verbindlichkeitskonto gebucht werden, bis die Artikel geliefert wurden. Vorauszahlungen für Bestellungen müssen auf einem Anlagenkonto erfasst werden, bis die Artikel eingegangen sind. Darüber hinaus müssen Sie ein separates Sachkonto für jedes MwSt.-Kennzeichen einrichten.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>So fügen Sie Vorauszahlungskonten zu "Buchungsmatrix Einrichtung" hinzu:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Allgemeine Buchungsmatrixeinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Buchungsmatrix Einrichtung** müssen die folgenden Felder für die entsprechenden Zeilen ausgefüllt werden:  

    * **Verkaufsvorauszahlungs-Konto**  
    * **Einkaufsvorauszahlungs-Konto**  

> [!TIP]
> Wenn Sie die Felder auf der Seite **Buchungsmatrix einrichten** nicht sehen können, verwenden Sie die horizontale Bildlaufleiste am unteren Rand der Seite, um nach rechts zu scrollen.  

Wenn Sie das Sachkonto für Vorauszahlungen nicht bereits eingerichtet haben, können Sie dies auf der Seite **Sachkontenliste** vom relevanten Kontofeld aus tun.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>So richten Sie Nummernserien für Vorauszahlungsbelege ein:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie auf der Seite **Debitoren & Verkauf Einr.** im Inforegister **Nummernserie** die folgenden Felder aus.  

   * **Geb. Vorauszahlungs-Rechnungsnr.**
   * **Geb. Vorauszahlungs-Gutschriftennr.**

3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kredite und Einkauf Einr. ein** und wählen Sie dann den entsprechenden Link.
4. Füllen Sie auf der Seite **Kreditoren & Einkauf Einr.** im Inforegister **Nummernserie** die folgenden Felder aus:

    * **Geb. Vorauszahlungs-Rechnungsnr.**
    * **Geb. Vorauszahlungs-Gutschriftennr.**

> [!NOTE]  
> Für Vorauszahlungsrechnungen und reguläre Rechnungen können dieselben oder unterschiedliche Nummernserien verwendet werden. Unterschiedliche Nummernserien dürfen sich nicht überschneiden, d. h. es darf keine Nummer in beiden Serien gleichzeitig vorhanden sein.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Einrichtung von Vorauszahlungsprozentsätze für Artikel, Debitoren und Kreditoren

Für einen Artikel können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Debitoren, einen bestimmten Debitor oder eine Debitorenpreisgruppe einrichten. Wenn Sie nicht auf alle Debitoren denselben Vorauszahlungsprozentsatz anwenden möchten, müssen Sie angeben, für welche Debitoren oder für welche Debitorenpreisgruppen der Vorauszahlungsprozentsatz gilt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.
2. Wählen Sie eien Artikel aus und wählen Sie dann die Aktion **Vorauszahlungsprozentsätze** aus.  
3. Füllen Sie auf der Seite **Verkaufsvorauszahlungs-Prozentsätze** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Für einen Debitor oder Kreditor können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Artikel und alle Arten von Verkaufszeilen einrichten. Dies geben Sie auf der Debitoren- oder Kreditorenkarte ein. Das folgende Verfahren zeigt, wie Sie einen Vorauszahlungsprozentsatz für einen Debitor angeben, aber ähnliche Schritte gelten für Kreditoren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie eine Karte für einen Debitor.
3. Füllen Sie das Feld **Vorauszalung %** aus.
4. Wiederholen Sie die Schritte für die anderen Debitoren oder Kreditoren.  

> [!TIP]
> Sie können auch die Seite **Verkaufsvorauszahlungs-Prozentsätze** über die Debitoren- oder Kreditorenkarte aufrufen.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>So stellen Sie fest, welcher Vorauszahlungsprozentsatz die höchste Priorität hat:  

In einem Auftrag kann ein Vorauszahlungsprozentsatz im Auftragskopf und ein anderer Prozentsatz für die Artikel in den Zeilen angegeben werden. Um festzustellen, welcher Vorauszahlungsprozentsatz die höchste Priorität hat, sucht das System den Vorauszahlungsprozentsatz für jede Verkaufszeile in der nachstehenden Reihenfolge und wendet den ersten Standard an, der gefunden wird:  

1. Der Vorauszahlungsprozentsatz für den Artikel in der Zeile und den Debitor, der die Lieferung erhält.  
2. Der Vorauszahlungsprozentsatz für den Artikel in der Zeile und die Debitorenpreisgruppe, der der Debitor angehört.  
3. Der Vorauszahlungsprozentsatz für den Artikel in der Zeile für alle Debitoren.  
4. Der Vorauszahlungsprozentsatz im Einkaufs- oder Verkaufskopf.  

Anders ausgedrückt, der Vorauszahlungsprozentsatz auf der Debitorenkarte wird nur angewendet, wenn für den Artikel kein Vorauszahlungsprozentsatz eingerichtet wurde. Wenn Sie jedoch nach dem Erstellen der Zeilen den Inhalt des Felds **Vorauszahlung %** im Verkaufs- oder Einkaufskopf ändern, wird der Vorauszahlungsprozentsatz in allen Zeilen aktualisiert. So kann ungeachtet der Prozentsatzeinstellungen für Artikel auf einfache Weise ein Auftrag mit einem festen Vorauszahlungsprozentsatz erstellt werden.

## <a name="see-also"></a>Siehe auch  

[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Berechnen von Steuern für Waren und Dienstleistungen auf Vorauszahlungen in Australien](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Berechnen von Steuern für Waren und Dienstleistungen auf Vorauszahlungen in Neuseeland](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Verständnis der Fibu und des COA](finance-general-ledger.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]