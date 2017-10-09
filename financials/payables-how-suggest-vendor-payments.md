---
title: Verwenden Sie die Zahlungsvorschlag-Stapelverarbeitung| Microsoft Docs
description: "Sie können Kreditorenzahlungseinstellungen festlegen, um Vorschläge zu erhalten oder damit für Zahlungen, die in Kürze fällig sind, oder denen ein Rabatt verfügbar ist."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 2085cc744c2ff3761937920cd893faab5a84dada
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-suggest-vendor-payments"></a>Vorgehensweise: Erstellen von Zahlungsvorschlägen für Kreditoren
Im Fenster **Zahlungsjournal** können Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungspositionen vorzuschlagen. Zeilen für Elemente wie Zahlungen, die in Kürze fällig sind oder Zahlungen, bei denen ein Rabatt verfügbar ist, werden entsprechend Ihren Einstellungen vorgeschlagen.

Um aus vorgeschlagenen Zeilen voll zu profitieren, müssen Sie zuerst die Kreditoren priorisieren. Weitere Informationen finden Sie unter [Vorgehensweise: Priorisieren von Kreditoren](purchasing-how-prioritize-vendors.md).  

Kreditorenposten, die nicht auf **Abwarten** sind, werden nicht berücksichtigt.  

> [!IMPORTANT]  
>   Wenn Sie Skonti nutzen möchten und einen verfügbaren Betrag eingegeben haben, wird der Rechnungsrabatt verwendet für:  

* Priorisierte überfällige Kreditorenposten nach der Priorität.  
* Überfällige Kreditorenposten, die nicht berücksichtigt werden.  
* Öffnen Sie die Kreditorenposten, die sich für Rabatte qualifizieren, angeordnet nach Kreditorennummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Die Zahlungsvorschlagfunktion verwenden
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungs-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Öffnen Sie das relevante Buch.-Blatt, und klicken Sie dann auf die Aktion **Zahlungsvorschlag**.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Einfügen des Fälligkeitsdatum als Buchungsdatum auf Zahlungsausgangs Buch.-Blattzeilen
Wenn Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungszeilen für Ihre Kreditoren zu erstellen, können Sie zwei Felder ausfüllen, um sicherzustellen, dass die erzeugten Zeilen das Fälligkeitsdatum verwenden, um das Buchungsdatum zu berechnen. Diese Felder sind **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** und **Offset für Fälligkeitsdatum für Ausgleich mit Beleg**.  

> [!IMPORTANT]  
>   Sie können das Feld **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** nicht zusammen mit den Feldern **Skonto finden** oder **Pro Kreditor summieren** verwenden. Der Grund besteht darin, dass, wenn das Buchungsdatum auf dem Fälligkeitsdatum liegt, einige Zahlungsrabatte nicht korrekt berechnet werden, da das Buchungsdatum nach dem Zahlungsrabattdatum liegen kann.  

Wenn das berechnete Buchungsdatum also in der Vergangenheit liegt, wird das Buchungsdatum auf das Arbeitsdatum verschoben, und eine Warnung wird angezeigt.  

Alternativ können Sie Zahlungspositionen mithilfe des Fälligkeitsdatums manuell generieren, um das Buchungsdatum zu berechnen Nachdem Sie Kreditorenposten ausgleichen, können Sie die Aktion **Buchungsdatum berechnen** verwenden, um das Buchungsdatum der Buch.-Blattzeile mit dem Fälligkeitsdatum der zugehörigen Einkaufsrechnung zu aktualisieren. Weitere Informationen finden Sie unter [So gehts: Einkaufstransaktionen manuell ausgleichen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Wenn die Einkaufsrechnung überfällig ist, wird das Buchungsdatum auf das Arbeitsdatum festgelegt, und die Schrift auf der Zeile wird in roter Farbe angezeigt.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Zahlungen vornehmen](payables-make-payments.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

