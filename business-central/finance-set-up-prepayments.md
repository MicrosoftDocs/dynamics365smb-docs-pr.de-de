---
title: Einrichten von Vorauszahlungen | Microsoft Docs
description: "Vorauszahlungen sind Zahlungen, die vor der finalen Fakturierung fakturiert und auf einen Vorauszahlungsauftrag (Einkauf oder Verkauf) gebucht werden. Möglicherweise bestehen Sie auf einer Anzahlung, bevor Sie Artikel nach Maß fertigen, oder Sie bestehen auf einer Anzahlung, bevor die Artikel an den Debitor geliefert werden. Mithilfe der Vorauszahlungsfunktion können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten. Somit kann sichergestellt werden, dass alle Zahlungen mit einer Rechnung ausgeglichen werden."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 12/04/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 3f158d7ed56445d6d2acf2ef8e5e9ab8e7487531
ms.openlocfilehash: 3038fc256ec45b8eb51abe3f71b7fcc7d273b353
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-prepayments"></a>Vorauszahlungen einrichten
Wenn Sie von Ihren Debitoren erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten oder wenn der Kreditor von Ihnen eine Vorauszahlung vor Lieferung erwartet, können Sie die Funktion "Vorauszahlung" verwenden. Mithilfe der Vorauszahlungsfunktion können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten, und um sicherzustellen, dass alle Teilzahlungen für eine Rechnung gebucht werden. Weitere Informationen finden Sie unter [Vorauszahlungsrechnungen erstellen](finance-how-to-create-prepayment-invoices.md).

Damit Vorauszahlungsrechnungen gebucht werden können, müssen in der Finanzbuchhaltung zunächst die Buchungskosten sowie die Nummernserien für Vorauszahlungsbelege eingerichtet werden.  

Sie können den Prozentsatz des zur Zahlung fakturierten Zeilenbetrags für einen Debitor, einen Kreditor, für alle Artikel oder für ausgewählte Artikel definieren. Nach dem Festlegen der Einstellungen können Vorauszahlungsrechnungen auf der Grundlage von Aufträgen und Bestellungen generiert werden. Sie können für jede Verkaufs- oder Einkaufszeile entweder die standardmäßigen Prozentsätze verwenden oder die Beträge der Rechnungen gemäß Ihren Anforderungen anpassen. So können Sie beispielsweise den Gesamtbetrag für den gesamten Auftrag angeben.  

Da der vorausgezahlte Betrag Eigentum des Käufers ist, bis dieser die Ware oder die Leistung erhalten hat, müssen Sie Sachkonten einrichten, auf denen die Vorauszahlungsbeträge bis zur Buchung der abschließenden Rechnung erfasst werden. Vorauszahlungen für Verkaufsaufträge müssen auf einem Verbindlichkeitskonto gebucht werden, bis die Artikel geliefert wurden. Vorauszahlungen für Bestellungen müssen auf einem Anlagenkonto erfasst werden, bis die Artikel eingegangen sind. Darüber hinaus müssen Sie ein separates Sachkonto für jedes MwSt.-Kennzeichen einrichten.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>So fügen Sie Vorauszahlungskonten zu "Buchungsmatrix Einrichtung" hinzu:  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeine Buchungseinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Buchungsmatrix Einrichtung** müssen die folgenden Felder ausgefüllt werden:  

    - **Verkaufsvorauszahlungs-Konto**  
    - **Einkaufsvorauszahlungs-Konto**  

Wenn Sie das Sachkonto für Vorauszahlungen nicht bereits eingerichtet haben, können Sie dies auf der Seite **Sachkontenliste** tun.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>So richten Sie Nummernserien für Vorauszahlungsbelege ein:  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren & Verkauf einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie auf der Seite **Debitoren & Verkauf Einr.** die folgenden Felder aus:  

   - **Geb. Vorauszahlungs-Rechnungsnr.**
   - **Geb. Vorauszahlungs-Gutschriftennr.**

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Käufe und Verkäufe einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie auf der Seite **Kreditoren & Einkauf Einr.** die folgenden Felder aus:

    - **Geb. Vorauszahlungs-Rechnungsnr.**
    - **Geb. Vorauszahlungs-Gutschriftennr.**

> [!NOTE]  
>  Für Vorauszahlungsrechnungen und reguläre Rechnungen können dieselben oder unterschiedliche Nummernserien verwendet werden. Unterschiedliche Nummernserien dürfen sich nicht überschneiden, d. h. es darf keine Nummer in beiden Serien gleichzeitig vorhanden sein.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Einrichtung von Vorauszahlungsprozentsätze für Artikel, Debitoren und Kreditoren  
Für einen Artikel können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Debitoren, einen bestimmten Debitor oder eine Debitorenpreisgruppe einrichten.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie eien Artikel aus und wählen Sie dann die Aktion **Vorauszahlungsprozentsätze** aus.  
3. Füllen Sie auf der Seite **Verkaufsvorauszahlungs-Prozentsätze** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Für einen Debitor oder Kreditor können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Artikel und alle Arten von Verkaufszeilen einrichten. Dies geben Sie auf der Debitoren- oder Kreditorenkarte ein.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie eine Karte für einen Debitor.
3. Füllen Sie das Feld **Vorauszalung %** aus.
4. Wiederholen Sie die Schritte für die anderen Debitoren oder Kreditoren.  

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
[Verständis der Fibu und des Kontoplans](finance-general-ledger.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

