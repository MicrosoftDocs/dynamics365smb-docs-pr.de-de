---
title: Einrichten und Verwenden von Standardzeilen für Wiederverkäufe und -einkäufe| Microsoft Docs
description: Sie können Verkaufszeilen und Einkaufszeilen einrichten, die Sie häufig machen und diese dann in Verkaufs- und Einkaufsbelegen einfügen, um die Zeilen mit Standardinformationen schnell auszufüllen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e85d870c73a4c7e5baec449c63f80cc5a4dadf5e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195267"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen
Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufs- und Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.  

Der folgende Ablauf zeigt, wie man Standardverkaufszeilen in einer Verkaufsrechnung einrichtet. Das funktioniert ähnlich bei allen anderen Verkaufsbelegen und Einkaufsbelegen.  

## <a name="to-set-up-recurring-sales-lines"></a>So richten Sie wiederkehrende Verkaufszeilen ein  
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Wiederkehrende Verkaufszeilen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Wiederkehrende Verkaufszeilen** die Aktion **Neu**.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.  

> [!NOTE]
> Sie können keine Preise für wiederkehrende Verkaufszeilen definieren, da Preise, Rabatte usw. auf den tatsächlichen Verkaufsbelegen berechnet werden, nachdem Sie die wiederkehrenden Verkaufszeilen eingefügt haben.

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>So weisen Sie einem Debitor wiederkehrende Verkaufszeilen zu
Ordnen Sie einem Debitor eine oder mehrere wiederkehrende Verkaufszeilen zu, so dass sie zum Einfügen in Verkaufsbelege für diesen Debitor zur Verfügung stehen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen entsprechendes Debitor.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie Codes für die wiederkehrenden Verkaufszeilen aus, die Sie auf den Verkaufsbelegen für den Debitor einfügen können möchten.
5. Füllen Sie die weiteren Felder aus, um festzulegen, wann, wie und wo die wiederkehrenden Verkaufszeilen verwendet werden sollen.
6. In den vier Feldern, in denen Sie angeben, wie die Zeilen auf vier Belegarten eingefügt werden, wählen Sie eine der folgenden Optionen aus:

|Option|Beschreibung|
|-|-|
|**Manuell**|Sie müssen eine wiederkehrende Verkaufszeile, die bereits für den Debitor vorhanden ist, manuell suchen.|
|**Automatisch**|Wenn wiederkehrende Verkaufszeilen für den Debitor vorhanden sind, erhalten Sie eine Benachrichtigung, in der Sie auswählen können, welche eingefügt werden soll. Wenn nur eine wiederkehrende Verkaufszeile existiert, wird sie automatisch eingefügt.<br /><br />Beachten Sie, dass dies nur funktioniert, wenn das neue Dokument aus einer Dokumentenliste erstellt wurde, z. B. durch Auswahl der Aktion **Neu** auf der Seite **Kundenaufträge**. Dies funktioniert nicht, wenn das Dokument beispielsweise aus einer Debitorenkarte erstellt wurde.|
|**Immer bestätigen**|Eine Benachrichtigung erscheint und alle vorhandenen wiederkehrenden Verkaufszeilen werden angezeigt, sodass Sie eine auswählen können.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Um auf einer wiederkehrenden Verkaufsrechnung Standardverkaufszeilen einfügen
Wenn für den Debitor wiederkehrende Verkaufszeilen vorhanden sind, können Sie diese in alle Arten von Verkaufsbelegen einfügen oder einfügen lassen, z. B. in eine Verkaufsrechnung. Wenn Sie die Optionen **Immer fragen** aktiviert haben, werden Sie informiert, wenn wiederkehrende Verkaufszeilen vorhanden sind.
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Rechnungen** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.

    > [!NOTE]
    > Um wiederkehrenden die Verkaufszeilen zu verwenden, die bei der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** festgelegt werden, müssen Sie die Felder **Gültig ab-Datum** und **Gültig bis-Datum** auf der Seite **Wiederkehrende Verkaufszeilen** ausfüllen. Weitere Informationen finden Sie unter [Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines)

5. Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen
Sie können mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** die Verkaufsrechnungen gemäß Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.

> [!NOTE]
> Auf der Seite **Wiederkehrende Verkaufszeilen** können Sie auch eine Einzugsmethode und ein Lastschrift-Mandat angeben. Die Verkaufsrechnungen, die mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen** erstellt werden, enthalten dann Informationen, die für den Einzug der Zahlungen für die Verkaufsrechnungen per SEPA-Lastschrift benötigt werden. Weitere Informationen finden Sie unter [Zahlungen mit SEPA-Lastschrift einziehen](finance-collect-payments-with-sepa-direct-debit.md).

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Wiederkehrende Verkaufsrechnungen erstellen** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie auf der Seite **Wiederkehrende Verkaufsrechnung** die Felder wie benötigt aus.
3. In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
