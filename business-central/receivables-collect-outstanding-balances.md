---
title: Einziehen von Restbeträgen
description: 'Lernen Sie, wie Sie Ihre Debitor an ausstehende Zahlungen erinnern können. Senden Sie einen Debitor-Auszug, eine Mahnung oder eine Zinsrechnung.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 02/09/2022
ms.author: edupont
---
# <a name="collect-outstanding-balances"></a><a name="collect-outstanding-balances"></a>Einziehen von Restbeträgen

Im Rahmen der Debitorenverwaltung muss auch geprüft werden, ob fällige Beträge pünktlich bezahlt werden. Wenn Debitoren überfällige Zahlungen haben, können Sie damit beginnen, indem Sie den Bericht **Kontoauszug** als Mahnung senden. Sie können auch Mahnungen ausgeben.

Mithilfe von Mahnungen können Debitoren auf überfällige Beträge aufmerksam gemacht werden. Darüber hinaus können Mahnungen zum Berechnen von Zinsen oder Zuschlägen verwendet werden, die dann in die Mahnung aufgenommen werden. Verwenden Sie Zinsrechnungen, wenn Sie Debitoren Zinsen oder Zuschläge berechnen möchten, ohne die überfälligen Beträge anzumahnen.

## <a name="statements"></a><a name="statements"></a>Auszüge

Anhand der Kundenkarte können Sie einen Auszug mit den Transaktionen dieses Kunden mit Ihnen. Anschließend senden Sie dem Kunden die generierte PDF-Datei. Alternativ können Sie den Bericht **Kontoauszug** dazu verwenden, um Ihren Debitoren eine Übersicht über ihre Geschäftstätigkeit mit Ihnen senden. Der Kontoauszug kann zur weiteren Bearbeitung an Excel gesendet werden.  

### <a name="to-send-the-customer-statement-report"></a><a name="to-send-the-customer-statement-report"></a>Um den Kontoauszugsbericht zu senden

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 10.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontoauszug** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Unter **Ausgabeoptionen** wählen Sie aus, wie der Bericht an den Debitoren gesendet wird.

> [!NOTE]
> Wenn Sie mehrere Währungen verwenden, wird der Debitoren-Abrechnungsbericht immer in der Währung des Debitors gedruckt. Das Datum einer Abrechnungsperiode dient auch als Abrechnungsdatum und als Fälligkeitsdatum, wenn die Fälligkeit enthalten ist.

## <a name="reminders"></a><a name="reminders"></a>Mahnungen

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a><a name="finance-charges"></a>Finanzierungskosten

Hat ein Debitor nicht bis zum Fälligkeitsdatum gezahlt, können automatisch Zuschläge berechnet und zu den überfälligen Beträgen auf dem Debitorkonto addiert werden. Verwenden Sie Zinsrechnungen, um Debitoren über die Zuschläge zu informieren.  

> [!NOTE]  
> Mithilfe von Zinsrechnungen werden Zinsen und Zuschläge berechnet und Debitoren über die Zinsen und Zuschläge informiert, ohne die überfälligen Beträge anzumahnen. Alternativ können Zinsen auf überfällige Zahlungen auch bei der Mahnungserstellung berechnet werden.  

Bevor Sie Zinsrechnungen  erstellen können, müssen Sie Bestimmungen einrichten. Weitere Informationen finden Sie unter [Einrichten von Zinskonditionen](finance-setup-finance-charges.md).  

Sie können eine Zinsrechnung für einen bestimmten Debitor manuell erstellen und die Zeilen automatisch ausfüllen. Alternativ können Sie die Funktion **Zinsrechnungen erstellen** verwenden, um Zinsrechnungen für alle oder ausgewählte Debitoren mit überfälligem Saldo zu erstellen.  

Erstellte Zinsrechnungen können geändert werden. Der Text, der am Anfang und am Ende der Zinsrechnung erscheint, ist abhängig von den Zinskonditionen und wird in der jeweiligen Zeile in der Spalte **Beschreibung** angezeigt. Wurde in den Vor- oder Nachtext automatisch ein berechneter Betrag eingefügt, wird der Text beim Löschen von Zeilen nicht angepasst. Verwenden Sie in diesem Fall die Funktion **Zinsrech. Text aktualisieren**.  

Nach dem Erstellen von Zinsrechnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Zinsrechnungen versenden, in der Regel als E-Mail.

### <a name="to-create-a-finance-charge-memo-manually"></a><a name="to-create-a-finance-charge-memo-manually"></a>So erstellen Sie eine Zinsrechnung manuell

Eine Zinsrechnung ist ähnlich wie eine Rechnung. Sie können den Kopf manuell ausfüllen und die Zeilen ausfüllen lassen, oder Sie können Zinsrechnungen für alle Debitoren automatisch erstellen lassen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zinsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus.  
3. Wählen Sie **Zinsgebührmemo-Zeilen** vorschlagen.
4. Auf der Seite **Zinsrechnungszeile vorschlagen** setzen Sie auf dem Inforegister **Debitorenposten** einen Filter, wenn Sie nur für bestimmte Posten Zinsrechnungen erstellen möchten.

    > [!NOTE]
    > Obwohl sie aufgelistet sind, hat die Auswahl von **Zahlung** und **Gutschrift** als **Belegart**-Filter keine Wirkung, da die Funktion **Zinsrechnung** nur positive Beträge verarbeitet.
5.  Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.  

### <a name="to-update-finance-charge-memo-texts"></a><a name="to-update-finance-charge-memo-texts"></a>So aktualisieren Sie Zinsrechnungstexte:
In manchen Fällen möchten Sie möglicherweise den Vor- und Nachtext ändern, den Sie für die Zinskonditionen eingerichtet haben. Wenn Sie dies zu einem Zeitpunkt tun, an dem Sie Zinsrechnungen angelegt, aber noch nicht registriert haben, können Sie die Anwendung dazu veranlassen, die Zinsrechnungen mit den geänderten Texten zu aktualisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Finance Zinsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das Fenster, in dem Sie Text ändern möchten und wählen Sie die **Zinsrech. Text aktualisieren** Aktion aus.
3. Auf der Seite **Zinsrechnungskopf aktualisieren** können Sie einen Filter festlegen, wenn Sie mehrere Zinsrechnungen aktualisieren möchten.
4. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.  

### <a name="to-issue-finance-charge-memos"></a><a name="to-issue-finance-charge-memos"></a>Um Zinsrechnungen zu registrieren
Nach dem Erstellen von Zinsrechnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Zinsrechnungen registrieren.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben auf der Seite **Zinsgebühr** gebucht. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Die Seite **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten auf der Seite **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** auf der Seite **Zinsgebührbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten auf der Seite **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finance Zinsrechnungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das entsprechenden Memo aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie auf der Seite **Zinsgebührmemo ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Das Zinsgebührenmemo wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

### <a name="to-cancel-an-issued-finance-charge-memo"></a><a name="to-cancel-an-issued-finance-charge-memo"></a>Um die ausgestellte Zinsrechnung zu stornieren
Wenn fälschlicherweise Zinsrechnungen ausgegeben wurden, können Sie diese vor dem Versenden stornieren. Sie können dies entweder einzeln oder als Stapel ausführen.
1. Auf der Seite **Ausgestellte Zinsrechnung** wählen Sie mindestens eine Zeile für die Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie danach die Aktion **Löschen** aus.
2. Auf der Seite **Ausgestellte Zinsrechnungs-Memos stornieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a><a name="to-view-reminder-and-finance-charge-entries"></a>So zeigen Sie Mahnungs- und Zinsrechnungsposten an:
Wenn Sie eine Mahnung registrieren, wird für jede Mahnungszeile, die einen Debitorenposten enthält, ein Mahnungsposten auf der Seite **Mahnung/Zinsrechnung Posten** erstellt. Sie können sich einen Überblick über die erstellten Mahnungsposten für einen bestimmten Debitor anzeigen lassen.    
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 5.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Buchblatteinträge**.
3. Klicken Sie auf die Seite auf **Buch-Blatteinträge** und wählen Sie die Zeilen, die Sie anzeigen möchten, und klicken Sie dann auf **Posten, Mahnungs-/Zinsrechnungseinträge**.

## <a name="multiple-interest-rates"></a><a name="multiple-interest-rates"></a>Verschiedene Zinssätze

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Weitere Informationen finden Sie unter [Mehrere Zinssätze einrichten](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Einrichten von Mahnmethoden, Bestimmungen und Mahntext](finance-setup-reminders.md)  
[Konditionen für Finance-Belastungen festlegen](finance-setup-finance-charges.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
