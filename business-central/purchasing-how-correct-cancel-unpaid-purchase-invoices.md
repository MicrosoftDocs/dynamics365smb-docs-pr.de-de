---
title: Ändern oder Löschen einer unbezahlten Einkaufsrechnung| Microsoft Docs
description: Erklärt, wie automatisch eine Einkaufsgutschrift korrigiert, abgebrochen oder rückgängig gemacht wird und eine gebuchte Einkaufsrechnung erstellt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6568828a50e274de0ac6364a1df72cc48abd4956
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748718"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Ändern oder Löschen einer unbezahlten Einkaufsrechnung

Sie können eine bezahlte Einkaufsrechnung korrigieren oder abbrechen. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten.

Wenn Sie bereits für Produkte auf der gebuchten Einkaufsrechnung bezahlt haben, können Sie diese aus der gebuchten Einkaufsrechnung selbst nicht korrigieren oder stornieren. Stattdessen müssen Sie eine Einkaufsgutschrift manuell erstellen, um den Einkauf zu stornieren, optional verwaltet mit einer Einkaufsreklamation. Dies gilt auch, wenn Sie eine gebuchte Einkaufrechnung ändern möchten, die auf kombinierten Einkaufslieferungen basiert. Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Auf der Seite **Geb. Einkaufsrechnung** können Sie die Schaltfläche **Korrigieren** oder **Stornieren** wählen. Wenn Sie eine gebuchte Einkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Einkaufsrechnung gebucht wurde. Dadurch wird die gebuchte Einkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrektureinkaufsgutschrift für Ihr Protokoll. Nachfolgend wird die Verwendung von **Korrigieren** und **Stornieren** beschrieben.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Gebuchte Einkaufsrechnung korrigieren
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie korrigieren möchten.  

    > [!NOTE]  
    >   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Auf der Seite **Gebuchte Einkaufsrechnung** wählen Sie **Korrekt** aus.

    Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md). Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung storniert.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Gebuchte Einkaufsrechnung stornieren
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie stornieren möchten.

    > [!NOTE]  
    >   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Auf der Seite **Gebuchte Einkaufsrechnung** wählen Sie **Abbrechen** aus.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung storniert.

### <a name="partial-invoice-posting-also-supported"></a>Rechnungsteilbuchung wird ebenfalls unterstützt
Wenn sich die Stornierung auf eine Rechnungsteilbuchung bezieht, wird die ursprüngliche Einkaufsbestellzeile aktualisiert, um die stornierte fakturierte Menge widerzuspiegeln. Die Felder **Zu fakturierende Menge** und **Fakturierte Menge** zur zugehörigen Einkaufsbestellzeile werden auf die Werte vor der Teilbuchung zurückgesetzt.

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
