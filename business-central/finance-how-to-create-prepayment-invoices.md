---
title: Vorauszahlungsrechnungen erstellen
description: 'Behandeln Sie Situationen, in denen Sie oder Ihr Kreditor eine Vorauszahlung verlangen. Verwenden Sie die voreingestellten Prozentsätze für jede Verkaufs- oder Kauf-Zeile oder passen Sie den Betrag nach Bedarf an.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 02/02/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a><a name="create-prepayment-invoices"></a>Vorauszahlungsrechnungen erstellen

Wenn Sie von Ihren Debitoren erwarten, dass diese vor der Lieferung eines Auftrags eine Zahlung leisten, können Sie die Funktion „Vorauszahlung“ verwenden. Dies gilt auch, wenn Ihr Verkäufer erwartet, dass Sie die Zahlung leisten, bevor er eine Bestellung an Sie versendet.  

Sie können den Vorauszahlungsprozess starten, wenn Sie eine Einkaufsbestellung oder einen Verkaufsauftrag erstellen. Der standardmäßige Vorauszahlungsprozentsatz für einen Artikel in der Bestellung oder für einen Debitor oder Kreditor wird dieser automatisch in die resultierende Vorauszahlungsrechnung aufgenommen. Sie können auch einen Vorauszahlungsprozentsatz für das gesamte Dokument angeben.

Nachdem Sie einen Auftrag oder eine Bestellung angelegt haben, können Sie eine Vorauszahlungsrechnung erstellen. Verwenden Sie entweder die voreingestellten Prozentsätze für jede Verkaufs- oder Kauf-Zeile oder passen Sie den Betrag nach Bedarf an. So können Sie beispielsweise einen Gesamtbetrag für den gesamten Auftrag angeben.  

Im Folgenden wird beschrieben, wie eine Vorauszahlung für einen Verkaufsauftrag fakturiert wird. Die Schritte sind für eine Bestellung ähnlich.  

## <a name="to-create-a-prepayment-invoice"></a><a name="to-create-a-prepayment-invoice"></a>So erstellen Sie eine Vorauszahlungsrechnung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neuen Verkaufsauftrag für den relevanten Debitor. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  

    Auf dem Inforegister **Vorauszahlung** gibt das Feld **Vorauszahlung %** den Prozentsatz an, der zur Berechnung des Vorauszahlungsbetrags verwendet werden soll. Wenn auf der Debitorenkarte ein standardmäßiger Vorauszahlungsprozentsatz angegeben ist, wird das Feld automatisch ausgefüllt. Sie können den Prozentsatz ändern. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Wählen Sie das Feld **Vorauszahlung komprimieren** aus, falls Sie auf der Vorauszahlungsrechnung Zeilen erstellen möchten, die Zeilen aus dem Kundenauftrag zusammenfassen, wenn folgende Bedingungen zutreffen:  

    - Es wird das gleiche Sachkonto für Vorauszahlungen verwendet, wie unter "Buchungsmatrix Einrichtung" festgelegt.  
    - Es werden die gleichen Dimensionen verwendet.  

    Wenn Sie eine Vorauszahlungsrechnung angeben möchten, die für jede Auftragszeile mit einem Vorauszahlungsprozentsatz eine Zeile enthält, wählen Sie nicht das Feld **Vorauszahlung komprimieren** aus.  

    Das Fälligkeitsdatum für die Vorauszahlung wird automatisch basierend auf dem Wert für **Zlg.-Bedingungscode Vorauszahlung** berechnet.

    > [!NOTE]
    > Wenn einige Zeilen auf einer Rechnung eine Vorauszahlung von 100 % erfordern und andere Positionen nicht, und das Vorauszahlungskonto Mehrwertsteuer enthält, kann der gerundete Betrag beim Erstellen einer Vorauszahlungsrechnung zu einem Fehler führen. Der Fehler tritt auf, weil der Vorauszahlungsrechnungsbetrag höher ist als die Beträge in den Belegzeilen. Um das Problem zu beheben, ändern Sie die Beträge auf einer oder allen Zeilen, für die eine Vorauszahlung von 100 % erforderlich ist. Durch die Änderung wird die Rundung des Mehrwertsteuerbetrags neu berechnet und die kumulierte Rundungsdifferenz in der letzten geänderten Zeile verwendet.
    >
    > Zwei weitere Möglichkeiten, das Problem zu beheben, sind:
    >
    > * Erstellen Sie eine separate MwSt.-Produktbuchungsgruppe und eine MwSt.-Buchungseinrichtung mit einer separaten MwSt.-Kennung und verwenden Sie diese für die Artikel oder Zeilen, die eine Vorauszahlung von 100 % erfordern. Die Rundung erfolgt für jedes MwSt.-Kennzeichen, sodass für Artikel, die der MwSt.-Produktbuchungsgruppe zugewiesen sind, eine separate Rundung durchgeführt wird.
    > * Verwenden Sie eine separate Rechnung für die Artikel oder Zeilen, die 100 % Vorauszahlungen erfordern und nicht.

3. Füllen Sie die Verkaufszeilen aus.  

    Wenn Sie einen standardmäßigen Vorauszahlungsprozentsatz für den Debitor oder auf dem Inforegister **Vorauszahlung** in diesem Dokument festgelegt haben, wird dieser Wert in jede Zeile kopiert. Sie können den Inhalt des Felds in der Zeile **Vorauszahlung %** ändern.  

    > [!TIP]
    > Wenn das Feld **Vorauszahlung %** nicht angezeigt wird, können Sie es durch Personalisierung hinzufügen.  Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

4. Um den gesamten Vorauszahlungsbetrag anzuzeigen, wählen Sie die Aktion **Statistik**.

    Wenn Sie den gesamten Vorauszahlungsbetrag für den Auftrag anpassen möchten, können Sie den Inhalt des Feldes **Vorauszahlungsbetrag** auf der Seite **Verkaufsauftragsstatistik** ändern.  

    Wenn das Feld **Preise inkl. MwSt** aktiviert ist, kann das Feld **Vorauszahlungsbetrag einschl. MwSt**. geändert werden.  

    Wenn Sie den Inhalt des Felds **Vorauszahlungsbetrag** ändern, wird der Betrag proportional auf alle Zeilen aufgeteilt, mit Ausnahme der Felder, bei denen im Feld **Vorauszahlung** der Wert **0** angegeben ist.  

5. Wählen Sie zum Drucken eines Testberichtes vor der Buchung der Vorauszahlungsrechnung die Aktion **Vorauszahlung** und dann die Aktion **Vorauszahlungstestbericht**.  
6. Wählen Sie zum Buchen der Vorauszahlungsrechnung die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung**.  

    Klicken Sie zum Buchen und Drucken der Vorauszahlungsrechnung die Aktion **Vorauszahlungsrechnung buchen und drucken**.  

Es können weitere Vorauszahlungsrechnungen für den Auftrag ausgegeben werden. Um eine andere Rechnung auszustellen, erhöhen Sie hierzu den Vorauszahlungsbetrag für eine oder mehrere Zeilen, passen Sie im Bedarfsfall das Belegdatum an, und buchen Sie die Vorauszahlungsrechnung. Für die Differenz zwischen den bisher fakturierten Vorauszahlungsbeträgen und dem neuen Vorauszahlungsbetrag wird eine neue Rechnung erstellt.  

> [!NOTE]  
> Wenn Sie in Nordamerika sind, können Sie den Prozentsatz nicht ändern, nachdem die Vorauszahlungsrechnung gebucht wurde. Dieses wird in der nordamerikanischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] verhindert, da die Berechnung der Verkaufssteuer ansonsten falsch ist.  

 Wenn Sie bereit zum Buchen des verbleibenden Rechnungsbetrags sind, buchen Sie diesen auf die gleiche Weise, wie Sie jede andere Rechnung buchen. Der Vorauszahlungsbetrag wird automatisch vom fälligen Betrag abgezogen.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a><a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Aktualisieren Sie den Status von vorausbezahlten Bestellungen und Rechnungen automatisch

Sie können die Auftrags- und Rechnungsverarbeitung beschleunigen, indem Sie Auftragswarteschlangeneinträge einrichten, die den Status dieser Dokumente automatisch aktualisieren. Wenn eine Vorauszahlungsrechnung bezahlt wird, können die Auftragswarteschlangeneinträge den Dokumentstatus automatisch von **Ausstehende Vorauszahlung** zu **Freigegeben** ändern. Wenn Sie die Jobwarteschlangeneinträge einrichten, müssen Sie folgende Codeunits verwenden: **383 Ausstehende Vorauszahlungsverkäufe aktualisieren** und **383 Ausstehende Vorauszahlungsbestellungen aktualisieren**. Wir empfehlen, die Einträge häufig auszuführen, z. B. jede Minute. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Beispielhafte Vorgehensweise: Verkaufsvorauszahlungen einrichten und in Rechnung stellen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
