---
title: "Überblick der Aufgaben zum Verwalten von Debitoren | Microsoft Docs"
description: "Gliedert Aufgaben, um Debitoren zu verwalten, beispielsweise zahlende Gläubiger oder ausgehende Zahlungen an Buch-Posten, um Rechnungen oder Gutschriften zu schließen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d260cf22980d097637e26d97282ad5e4f344120a
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="managing-payables"></a>Verwalten von Verbindlichkeiten
Ein Teil der Verwaltung großer aus das Wareneinkaufskonto zahlt Ihre Kreditoren oder erstattet Mitarbeiter für Ausgaben zurück. Sie können Funktionalität verwenden, um das Fenster **Zahlung Buch.-Blatt** automatisch mit Zahlungszeilen für fällige Einkaufsrechnungen auszufüllen. Um die entsprechenden Banktransaktionen schnell auszuführen, können Sie mehrere Zahlungsausgangs Buch.-Blattzeilen in eine Datei exportieren, die Sie dann für Ihre Bank für die Verarbeitung hochladen. Sie können Zahlungen auch mit Scheck leisten inkl. der Möglichkeit, Schecks als elektronisches Zahlungsmittel zu senden.

Eine weitere typische Aufgabe ist es, ausgehenden Zahlungen dem zugehörigen Debitor bzw. einem Kreditorenposten zuzuordnen, um die entsprechenden Einkaufsrechnungen oder Einkaufsgutschriften zu schließen, wenn sie bezahlt sind. Diese Aufgabe können Sie dann im Fenster **Zahlungs-Abstimmungs-Buch.-Blatt** ausführen, indem Sie eine Bankkontoauszugsdatei importieren, um die Zahlungen schnell zu erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden. Es gibt verschiedene Arten, die Übereinstimmungen zu prüfen und zu ändern, bevor Sie das Buch.-Blatt buchen. Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Alternativ können Sie ausgehende Zahlungen im **Zahlungsausgangs Buch.-Blatt**-Fenster oder aus den zugehörigen Kreditorenposten manuell ausgleichen.

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den Kreditoren, in denen diese Aufgaben erläutert werden.

| An | Siehe |
| --- | --- |
| Generieren von Fälligkeitsdatum oder Kreditorenzahlungen oder Mitarbeitervergütungen, bereiten Sie Scheckzahlungen vor und exportieren sie Zahlungen beim Buchen an eine Bank. |[Zahlungen vornehmen](payables-make-payments.md) |
| Gleichen Sie Kreditorenzahlungen automatisch für unbezahlte Einkaufsrechnungen aus, indem Sie eine Bankkontoauszugsdatei importieren. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Gleichen Sie Kreditorenzahlungen für unbezahlten Einkaufsrechnungen manuell aus. |[Vorgehensweise: Manuelle Abstimmung von Debitorenzahlungen](payables-how-apply-purchase-transactions-manually.md) |
|Um eine korrekte Bewertung sicherzustellen, müssen Ihre Lagerartikel Kosten wie Fracht, Versicherung, Umlagerung und Transport enthalten, die beim Kauf oder Verkauf entstehen.|[Vorgehensweise: Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Vorgehensweise: Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

