---
title: Zahlungen automatisch vornehmen und Bankkonten abstimmen| Microsoft Docs
description: Zeigt Aufgaben, um Ihre Bank, Verkaufs- und Kreditorensammelkonte, Beitragszahlungseingänge oder Kosten auszugleichen und gleicht Zahlungen automatisch aus.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2eb3b42c5b76487d579065b9a60ae614bbb71dda
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748618"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Zahlungen automatisch vornehmen und Bankkonten abstimmen
Sie müssen Ihre Bank, Debitoren- und Kreditorensammelkonten routinemäßig abstimmen, indem Sie die Zahlungen, die in Ihrem Bankkonto aufgezeichnet sind, mit ihren entsprechenden offenen (unbezahlten) Rechnungen und Gutschriften oder anderen offenen Posten im [!INCLUDE[prod_short](includes/prod_short.md)]ausgleichen.  

Diese Aufgabe können Sie dann auf der Seite **Zahlungs-Abstimmungs-Buch.-Blatt** ausführen, z. B., indem Sie eine Bankkontoauszugsdatei oder einen Feed importieren, um die Zahlungen schnell zu erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können auch automatische Anwendungen überprüfen und ändern, bevor Sie das Blatt buchen. Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Buch.-Blatt buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Die Logik, die regelt, wie der Zahlungstext automatisch mit den Eingabeinformationen abgeglichen wird, ist auf der Seite **Zahlungsausgleichsvorschriften** als eine Reihe priorisierter Regeln eingerichtet, die Sie bearbeiten können.

Sie können auch, Bankkonten abstimmen ohne Zahlungen gleichzeitig anzuwenden. Sie führen diese Arbeiten auf der Seite **Bankkonto Abstimmen** aus. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).   

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Envestnet Yodlee Bank Feeds Service anlegen und aktivieren und dann Ihr Bankkonto mit den entsprechenden Online Bankkonten verbinden. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).  

Alternativ können Sie mit der AMC Banking 365 Fundamentals-Erweiterung eine Kontoauszugsdatei von jedem Format in einen Datenstrom konvertieren, den Sie in [!INCLUDE[prod_short](includes/prod_short.md)] importieren können. Weitere Informationen finden Sie [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md).  

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.  

| Aufgabe | Siehe |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md) |
| Gleichen Sie manuell Zahlungen aus, indem Sie detaillierte Informationen über zugeordnete Daten und Vorschläge für offene Kandidatenposten anzeigen, mit denen Zahlungen ausgeglichen werden sollen. |[Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung](receivables-how-review-apply-payments-auto-application.md) |
| Lösen Sie Zahlungen auf, die nicht automatisch in die entsprechenden offenen Posten übernommen werden können. Beispielsweise weil die Beträge abweichen oder weil ein verwandter Posten vorhanden. |[Zahlungen abstimmen, die nicht automatisch ausgeglichen werden können](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Verknüpfen Sie Text auf Zahlungen mit bestimmten Debitoren-, Kreditoren- oder Sachkonten, um solche wiederkehrenden Zahlungseingänge oder Ausgaben immer auf diesen Konten als Zahlungen ohne zugehörige Belege zu buchen, wenn keine entsprechenden Belege vorhanden sind. |[Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Richten Sie die Regeln ein, um zu steuern, wie Zahlungen/Banktransaktionen automatisch mit ihren entsprechenden offenen Sachposten ausgeglichen werden, wenn Sie die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** verwenden.|[Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
