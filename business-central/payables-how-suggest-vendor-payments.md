---
title: Lieferantenzahlungen vorschlagen
description: 'Verwenden Sie den Stapelverarbeitung „Zahlungsvorschlag“, um Zahlungszeilen für Ihre Kreditoren basierend auf Fälligkeitsterminen und Skonti zu erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 07/17/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="suggest-vendor-payments"></a>Lieferantenzahlungen vorschlagen

Auf der Seite **Zahlungsjournal** können Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungspositionen vorzuschlagen. Basierend auf Ihren Einstellungen, schlägt [!INCLUDE [prod_short](includes/prod_short.md)] Zeilen für Folgendes vor:

- Zahlungen, die bald fällig sind.
- Zahlungen, bei denen ein Skonto möglich ist.

Um aus vorgeschlagenen Zeilen voll zu profitieren, müssen Sie die Kreditoren priorisieren. Weitere Informationen zur Priorisierung von Kreditoren finden Sie unter [Kreditoren priorisieren](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Der Batchauftrag schließt Kreditorenposten aus, die **In der Warteschleife** sind oder die bereits angewendet werden und einen Wert im Feld **Ausgleichs-ID** haben.  

> [!IMPORTANT]  
> Wenn Sie Skonti nutzen möchten und einen verfügbaren Betrag eingegeben haben, wird der Rechnungsrabatt verwendet für:  
>
> * Priorisierte überfällige Kreditorenposten nach der Priorität.
> * Überfällige Kreditorenposten, die nicht berücksichtigt werden.  
> * Öffnen Sie die Kreditorenposten, die sich für Skonti qualifizieren. Die Einträge sind nach Kreditorennummer geordnet.  

## <a name="use-the-suggest-vendor-payments-action"></a>Die Zahlungsvorschlagsaktion verwenden

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das Buch.-Blatt und wählen Sie dann die Aktion **Zahlungsvorschlag**.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Das Fälligkeitsdatum als Buchungsdatum auf Zahlungs-Buch.-Blattzeilen einfügen

Wenn Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungszeilen für Ihre Kreditoren zu erstellen, können Sie zwei Felder ausfüllen, um sicherzustellen, dass die erzeugten Zeilen das Fälligkeitsdatum verwenden, um das Buchungsdatum zu berechnen. Diese Felder sind  **Buchungsdatum aus „Gilt für Dokument“-Fälligkeitsdatum berechnen**  und  **„Gilt für Dokument“-Fälligkeitsdatums-Offset**.  

> [!IMPORTANT]  
> Sie können das Feld  **Buchungsdatum aus Fälligkeitsdatum für Beleg berechnen**  nicht zusammen mit dem Feld  **Zahlungsrabatte suchen**  oder dem Feld  **Pro Lieferant zusammenfassen**  verwenden. Wenn das Buchungsdatum auf dem Fälligkeitsdatum liegt, werden einige Skonti möglicherweise nicht korrekt berechnet, da das Buchungsdatum nach dem Skontodatum liegt.  

Wenn das berechnete Buchungsdatum auch in der Vergangenheit liegt, wird das Buchungsdatum auf das Arbeitsdatum verschoben, und eine Warnung wird angezeigt.  

Sie können auch die Zahlungspositionen mithilfe des Fälligkeitsdatums manuell generieren, um das Buchungsdatum zu berechnen. Nachdem Sie Kreditorenposten ausgleichen, können Sie die Aktion **Buchungsdatum berechnen** verwenden, um das Buchungsdatum der Buch.-Blattzeile mit dem Fälligkeitsdatum der zugehörigen Einkaufsrechnung zu aktualisieren. Weitere Informationen zu diesem manuellen Prozess finden Sie unter [Einkaufstransaktionen manuell ausgleichen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Wenn die Einkaufsrechnung überfällig ist, wird das Buchungsdatum auf das Arbeitsdatum festgelegt, und die Schrift auf der Zeile wird zu rot geändert.  

## <a name="see-also"></a>Siehe auch

- [Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
- [Zahlungen vornehmen](payables-make-payments.md)  
- [Mit Fibu Buch.-Blättern arbeiten](ui-work-general-journals.md)  
- [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
