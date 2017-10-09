---
title: Einrichten von Vorauszahlungen | Microsoft Docs
description: "Vorauszahlungen sind Zahlungen, die vor der finalen Fakturierung fakturiert und auf einen Vorauszahlungsauftrag (Einkauf oder Verkauf) gebucht werden. Möglicherweise bestehen Sie auf einer Anzahlung, bevor Sie Artikel nach Maß fertigen, oder Sie bestehen auf einer Anzahlung, bevor die Artikel an den Debitor geliefert werden. Mithilfe der Vorauszahlungsfunktion können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten. Somit kann sichergestellt werden, dass alle Zahlungen mit einer Rechnung ausgeglichen werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11aef4cb4b1d40568b63662239a26993782201a3
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-prepayments"></a>Vorgehensweise: Einrichten von Vorauszahlungen
Wenn Sie von Ihren Kunden erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten oder wenn der Lieferant von Ihnen eine Vorauszahlung vor Lieferung erwartet, können Sie die Funktion "Vorauszahlung" verwenden. Mithilfe der Vorauszahlungsfunktion können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten, und um sicherzustellen, dass alle Teilzahlungen für eine Rechnung gebucht werden. Weitere Informationen finden Sie unter [Gewusst wie: Vorauszahlungsrechnungen erstellen](finance-how-to-create-prepayment-invoices.md).

Damit Vorauszahlungsrechnungen gebucht werden können, müssen in der Finanzbuchhaltung zunächst die Buchungskosten sowie die Nummernserien für Vorauszahlungsbelege eingerichtet werden.  

Sie können den Prozentsatz des zur Zahlung fakturierten Zeilenbetrags für einen Debitor, einen Kreditor, für alle Artikel oder für ausgewählte Artikel definieren. Nach dem Festlegen der Einstellungen können Vorauszahlungsrechnungen auf der Grundlage von Aufträgen und Bestellungen generiert werden. Sie können für jede Verkaufs- oder Einkaufszeile entweder die standardmäßigen Prozentsätze verwenden oder die Beträge der Rechnungen gemäß Ihren Anforderungen anpassen. So können Sie beispielsweise den Gesamtbetrag für den gesamten Auftrag angeben.  

Da der vorausgezahlte Betrag Eigentum des Käufers ist, bis dieser die Ware oder die Leistung erhalten hat, müssen Sie Sachkonten einrichten, auf denen die Vorauszahlungsbeträge bis zur Buchung der abschließenden Rechnung erfasst werden. Vorauszahlungen für Verkaufsaufträge müssen auf einem Verbindlichkeitskonto gebucht werden, bis die Artikel geliefert wurden. Vorauszahlungen für Bestellungen müssen auf einem Anlagenkonto erfasst werden, bis die Artikel eingegangen sind. Darüber hinaus müssen Sie ein separates Sachkonto für jedes MwSt.-Kennzeichen einrichten.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>So fügen Sie Vorauszahlungskonten zu "Buchungsmatrix Einrichtung" hinzu:  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Buchungsmatrix Einrichtung** ein und wählen dann den zugehörigen Link aus.
2. Im Fenster **Buchungsmatrix Einrichtung** müssen die folgenden Felder ausgefüllt werden:  

    - **Verkaufsvorauszahlungs-Konto**  
    - **Einkaufsvorauszahlungs-Konto**  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>So richten Sie Nummernserien für Vorauszahlungsbelege ein:  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debit&oren && Verkauf Einr.** ein und wählen dann den zugehörigen Link aus.
2. Füllen Sie im Feld **Debitoren & Verkauf Einr.** die folgenden Felder aus:  

   - **Geb. Vorauszahlungs-Rechnungsnr.**
   - **Geb. Vorauszahlungs-Gutschriftennr.**

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht  suchen")und geben **Kreditoren- und Debitoren-Einrichtung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie im Fenster **Kreditoren & Einkauf Einr.** die folgenden Felder aus:

    - **Geb. Vorauszahlungs-Rechnungsnr.**
    - **Geb. Vorauszahlungs-Gutschriftennr.**

> [!NOTE]  
>  Für Vorauszahlungsrechnungen und reguläre Rechnungen können dieselben oder unterschiedliche Nummernserien verwendet werden. Unterschiedliche Nummernserien dürfen sich nicht überschneiden, d. h. es darf keine Nummer in beiden Serien gleichzeitig vorhanden sein.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Einrichtung von Vorauszahlungsprozentsätze für Artikel, Debitoren und Kreditoren  
Für einen Artikel können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Debitoren, einen bestimmten Debitor oder eine Debitorenpreisgruppe einrichten.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie eien Artikel aus und wählen Sie dann die Aktion **Vorauszahlungsprozentsätze** aus.  
3. Füllen Sie im Fenster **Verkaufsvorauszahlungs-Prozentsätze** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Für einen Debitor oder Kreditor können Sie einen standardmäßigen Vorauszahlungsprozentsatz für alle Artikel und alle Arten von Verkaufszeilen einrichten. Dies geben Sie auf der Debitoren- oder Kreditorenkarte ein.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.
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
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

