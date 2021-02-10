---
title: Ändern oder Löschen einer gebuchten Verkaufsrechnung
description: Beschreibt, wie eine gebuchte Verkaufsrechnung korrigiert, rückgängig gemacht oder eine Gutschrift angewendet wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 01/11/2021
ms.author: edupont
ms.openlocfilehash: 7b52b3bd2acadc965b4b7ee25bc66f3f8f511bd5
ms.sourcegitcommit: 5d5451ee618f122c926e3189290f3765052f7077
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/11/2021
ms.locfileid: "4846315"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Ändern oder Löschen einer unbezahlten Verkaufsrechnung

Sie können eine nicht bezahlte Buchung korrigieren oder stornieren, sofern sie nicht vollständig versendet wurde. Dies ist nützlich, wenn Ihnen ein Fehler unterläuft, oder wenn der Debitor eine Änderung vornimmt, bevor die Sendung komplett ist. In allen anderen Szenarien empfehlen wir, dass Sie direkt eine korrigierende Verkaufsgutschrift erstellen. Weitere Informationen finden Sie unter [So erstellen Sie eine Verkaufsgutschrift aus einer gebuchten Verkaufsrechnung](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Nachdem eine gebuchte Verkaufsrechnung teilweise oder vollständig gezahlt wurde, können Sie die Nummer aus der gebuchten Verkaufsrechnung selbst nicht korrigieren oder stornieren. Stattdessen müssen Sie eine Verkaufsgutschrift manuell erstellen, um den Verkauf zu stornieren und den Debitor zurückzuerstatten. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Der Unterschied zwischen dem Stornieren oder Korrigieren einer gebuchten Verkaufsrechnung, die nicht bezahlt oder versendet wurde, wird in der folgenden Tabelle beschrieben.

| Aktion | Beschreibung |
| --- | --- |
| **Abbrechen** |Die gebuchte Verkaufsrechnung ist storniert. Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. In der ursprünglich gebuchten Verkaufsrechnung werden die Kontrollkästchen **Storniert** und **Bezahlt** aktiviert. |
| **Korrigiereh** |Die gebuchte Verkaufsrechnung ist storniert. Eine neue Kundenrechnung mit denselben Informationen wird erstellt, es sei denn, der gebuchte Kundenauftrag wurde aus einem Kundenauftrag gebucht. In diesem Fall empfehlen wir Ihnen, stattdessen die gebuchte Verkaufsrechnung zu stornieren, die Korrektur vorzunehmen und den Verkaufsprozess vom ursprünglichen Kundenauftrag aus fortzusetzen. <br/><br/>Die neue Verkaufsrechnung hat eine andere Nummer als die erste Verkaufsrechnung. Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. In der ursprünglich gebuchten Verkaufsrechnung werden die Kontrollkästchen **Storniert** und **Bezahlt** aktiviert. |

Wenn Sie eine gebuchte Verkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Verkaufsrechnung gebucht wurde. Dadurch wird die gebuchte Verkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrekturverkaufsgutschrift für Ihr Protokoll.  

> [!TIP]
> Wenn Sie eine Vorauszahlungsrechnung für eine Verkaufsrechnung gebucht haben, die Sie dann korrigieren oder stornieren, müssen Sie auch die Vorauszahlung korrigieren oder stornieren. Weitere Informationen finden Sie unter [Vorauszahlungen korrigieren](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Gebuchte Verkaufsrechnung stornieren

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die gebuchte Verkaufsrechnung, die Sie stornieren möchten.

    > [!NOTE]  
    >   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Auf der Seite **Gebuchte Verkaufsrechnung** wählen Sie **Abbrechen** aus.

    Eine Verkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. Das Feld **Storniert** am Anfang gebuchten Verkaufsrechnung wird auf **Ja** geändert.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Verkaufsgutschrift anzuzeigen, die die gebuchte Verkaufsrechnung storniert.

### <a name="partial-invoice-posting-also-supported"></a>Buchung von Teilrechnungen wird ebenfalls unterstützt

Wenn sich die Stornierung auf eine Rechnungsteilbuchung bezieht, wird die ursprüngliche Verkaufsauftragszeile aktualisiert, um die stornierte fakturierte Menge widerzuspiegeln. Die Felder **Zu fakturierende Menge** und **Fakturierte Menge** zur zugehörigen Verkaufsauftragszeile werden auf die Werte vor der Teilbuchung zurückgesetzt.

## <a name="to-correct-a-posted-sales-invoice"></a>Gebuchte Verkaufsrechnung korrigieren

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die gebuchte Verkaufsrechnung, die Sie korrigieren möchten.

    > [!NOTE]  
    >   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Auf der Seite **Gebuchte Verkaufsrechnung** wählen Sie **Korrekt** aus.  

    > [!NOTE]
    > Wenn die Verkaufsrechnung aus einem Kundenauftrag gebucht wurde, empfehlen wir Ihnen, dass Sie diese Verkaufsrechnung *stornieren* und dann die Korrektur aus dem ursprünglichen Kundenauftrag verarbeiten. Wenn der ursprüngliche Kundenauftrag gelöscht wurde, z. B. wenn er vollständig versendet wurde, können Sie einen neuen Kundenauftrag mithilfe er Aktion **Dokument kopieren** erstellen. Weitere Informationen finden Sie unter [So erstellen Sie eine Verkaufsgutschrift durch kopieren einer gebuchten Verkaufsrechnung](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können. Das Feld **Storniert** am Anfang gebuchten Verkaufsrechnung wird auf **Ja** geändert.

    Eine Verkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren.
5. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Verkaufsgutschrift anzuzeigen, die die gebuchte Verkaufsrechnung storniert.

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
