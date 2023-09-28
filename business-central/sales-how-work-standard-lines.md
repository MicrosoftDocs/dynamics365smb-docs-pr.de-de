---
title: Wiederkehrende Standard-Verkaufszeilen
description: 'Legen Sie häufig verwendete Verkaufszeilen fest, um sie in Verkaufsbelege einzufügen und die Zeilen schnell mit Standardinformationen zu füllen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 07/06/2022
ms.author: bholtorf
---
# Wiederkehrende Verkaufsrechn. erstellen

Wenn Sie häufiger Verkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.  

## Wiederkehrende Verkaufszeilen einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Wiederkehrende Verkaufszeilen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Wiederkehrende Verkaufszeilen** die Aktion **Neu**.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.  

> [!NOTE]
> Sie können keine Preise für wiederkehrende Verkaufszeilen definieren, da Preise, Rabatte usw. auf den tatsächlichen Verkaufsbelegen berechnet werden, nachdem Sie die wiederkehrenden Verkaufszeilen eingefügt haben.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Wiederkehrende Verkaufszeilen einem Debitor zuweisen

Ordnen Sie einem Debitor eine oder mehrere wiederkehrende Verkaufszeilen zu, so dass sie zum Einfügen in Verkaufsbelege für diesen Debitor zur Verfügung stehen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen entsprechendes Debitor.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie Codes für die wiederkehrenden Verkaufszeilen aus, die Sie auf den Verkaufsbelegen für den Debitor einfügen können möchten.
5. Füllen Sie die anderen Felder aus, um festzulegen, wann, wie und wo die wiederkehrenden Verkaufszeilen verwendet werden sollen.  

    Wenn Sie die wiederkehrenden Verkaufszeilen, die zusammen mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** festgelegt werden, verwenden Sie die Felder **Gültig ab-Datum** und **Gültig bis-Datum**, um die Verwendung der wiederkehrenden Verkaufszeilen zur Erstellung von Rechnungen zeitlich zu beschränken. Weitere Informationen finden Sie unter [Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufszeilen erstellen](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines)

    Sie können auch eine Einzugsmethode und ein Lastschrift-Mandat angeben. Die Verkaufsrechnungen, die mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** erstellt werden, enthalten dann die Informationen, die für den Einzug der Zahlungen für die Verkaufsrechnungen per SEPA-Lastschrift benötigt werden. Weitere Informationen finden Sie unter [Zahlungen mit SEPA-Lastschrift einziehen](finance-collect-payments-with-sepa-direct-debit.md).

6. In den vier Feldern, in denen Sie angeben, wie die Zeilen auf vier Belegarten eingefügt werden, wählen Sie eine der folgenden Optionen aus:

|Option|Beschreibung|
|------|-----------|
|**Manuell**|Sie müssen eine wiederkehrende Verkaufszeile, die bereits für den Debitor vorhanden ist, manuell suchen.|
|**Automatisch**|Wenn wiederkehrende Verkaufszeilen für den Debitor vorhanden sind, erhalten Sie eine Benachrichtigung, in der Sie auswählen können, welche eingefügt werden soll. Wenn nur eine wiederkehrende Verkaufszeile existiert, wird sie automatisch eingefügt.<br /><br />Dies funktioniert nur, wenn das neue Dokument aus einer Dokumentenliste erstellt wurde, z. B. durch Auswahl der Aktion **Neu** auf der Seite **Kundenaufträge**. Dies funktioniert nicht, wenn das Dokument beispielsweise aus einer Debitorenkarte erstellt wurde.|
|**Immer bestätigen**|Eine Benachrichtigung erscheint und alle vorhandenen wiederkehrenden Verkaufszeilen werden angezeigt, sodass Sie eine auswählen können.

## Wiederkehrende Verkaufszeilen auf einer Verkaufsrechnung einfügen

Wenn für den Debitor wiederkehrende Verkaufszeilen vorhanden sind, können Sie diese in alle Arten von Verkaufsbelegen einfügen oder einfügen lassen, z. B. in eine Verkaufsrechnung. Wenn Sie die Option **Immer fragen** aktiviert haben, während Sie Debitoren wiederkehrende Verkaufszeilen hinzufügen, werden Sie informiert, wenn wiederkehrende Verkaufszeilen vorhanden sind.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.
5. Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.

## Mehrere Verkaufsrechnungen basierend auf wiederkehrenden Verkaufszeilen erstellen

Sie können mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** die Verkaufsrechnungen gemäß Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wiederkehrende Verkaufsrechnungen erstellen** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Wiederkehrende Verkaufsrechnung** die Felder wie benötigt aus.
3. In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.

## Siehe auch

[Verkauf](sales-manage-sales.md)  
[Verkäufe einrichten](sales-setup-sales.md)  
[Wiederkehrende Einkaufszeilen erstellen](purchasing-how-work-recurring-purchase-lines.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
