---
title: Aufgaben, Bankkonten auszugleichen und Zahlungen zu den jeweiligen Posten anzuwenden | Microsoft Docs
description: "Zeigt Aufgaben, um Ihre Bank, Verkaufs- und Kreditorensammelkonte, Beitragszahlungseingänge oder Kosten auszugleichen und gleicht Zahlungen automatisch aus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 02/28/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d1c0312ad76a0993a79981e71bf6650351d44ced
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Zahlungen automatisch vornehmen und Bankkonten abstimmen
Sie müssen Ihre Bank, Debitoren- und Kreditorensammelkonten routinemäßig abstimmen, indem Sie die Zahlungen, die in Ihrem Bankkonto aufgezeichnet sind, mit ihren entsprechenden unbezahlten Rechnungen und Gutschriften oder anderen offenen Posten im [!INCLUDE[d365fin](includes/d365fin_long_md.md)]ausgleichen.  

Diese Aufgabe können Sie dann im Fenster **Zahlungs-Abstimmungs-Buch.-Blatt** ausführen, indem Sie eine Bankkontoauszugsdatei oder einen Feed importieren, um die Zahlungen schnell zu erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können auch automatische Anwendungen überprüfen und ändern, bevor Sie das Blatt buchen. Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Sie können auch, Bankkonten abstimmen ohne Zahlungen gleichzeitig anzuwenden. Sie führen diese Arbeiten im Fenster **Bankkonto Abstimmen** aus. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).   

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Bank-Feed-Service Envestnet Yodlee anlegen und aktivieren und dann Ihr Bankkonto mit den entsprechenden Online Bankkonten verbinden. Für weitere Informationen, siehe [Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).  

Sie können auch die Funktion für den Bankdatenkonvertierungsdienst verwenden, um eine Bankkontoauszugsdatei, die Sie von Ihrer Bank erhalten, in einen Datenstream zu konvertieren, den Sie in das [!INCLUDE[d365fin](includes/d365fin_long_md.md)] importieren können. Für weitere Informationen, siehe [Einrichten des Bankdaten-Konvertierungsdienst](bank-how-setup-bank-data-conversion-service.md).  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

| Aufgabe | Siehe |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md) |
| Gleichen Sie manuell Zahlungen aus, indem Sie detaillierte Informationen über zugeordnete Daten und Vorschläge für offene Kandidatenposten anzeigen, mit denen Zahlungen ausgeglichen werden sollen. |[Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung](receivables-how-review-apply-payments-auto-application.md) |
| Lösen Sie Zahlungen auf, die nicht automatisch in die entsprechenden offenen Posten übernommen werden können. Beispielsweise weil die Beträge abweichen oder weil ein verwandter Posten vorhanden. |[Abstimmen von Zahlungen, die nicht automatisch übernommen werden können](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Verknüpfen Sie Text auf Zahlungen mit bestimmten Debitoren-, Kreditoren- oder Sachkonten, um solche wiederkehrenden Zahlungseingänge oder Ausgaben immer auf diesen Konten als Zahlungen ohne zugehörige Belege zu buchen, wenn keine entsprechenden Belege vorhanden sind. |[Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

