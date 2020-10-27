---
title: Verwalten von Bankkonten| Microsoft Docs
description: Sie müssen regelmäßig Bankposten mit den zugehörigen Banktransaktionen in Ihren Bankkonten abstimmen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7d5610e86ea06b6edd2ef0ae4cb7c1473dd096e9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924353"
---
# <a name="reconciling-bank-accounts"></a>Abstimmen von Bankkonten

Eine Bankabstimmung sollte in regelmäßigen Abständen für alle Ihre Bankkonten durchgeführt werden, um sicherzustellen, dass die Kassenunterlagen des Unternehmens korrekt sind. Sie tun dies, indem Sie die Einträge in Ihren internen Bankkonten mit den Banktransaktionen in Ihrer Bank vergleichen und abgleichen und dann die Salden auf Ihre internen Bankkonten buchen, um den Finanzmanagern Gesamtsummen zur Verfügung zu stellen. Der Bankabgleich ist auch eine praktische Methode, um fehlende Zahlungen und Buchhaltungsfehler zu ermitteln und zu beheben.

Sie können die Aufgabe auf der Seite **Bankkonto Abstimmen** ausführen, auf der Sie die Bankkontoauszugszeilen auf der linken Bereichsseite mit Ihrem internen Bankposten im rechten Fensterbereich abstimmen (abgleichen). Alternativ können Sie diese Aufgabe auf der Seite **Zahlungsabstimmungsbuch.-Blatt** als Teil der Verarbeitung der Zahlungen durchgeführt werden, die auf einem Bankauszug dargestellt werden. Auf beiden Seiten können Sie die Bankkontoauszugsinformationen ausfüllen, indem Sie eine Datei oder einen Feed importieren oder automatische entsprechende Vorschläge verwenden.

> [!NOTE]  
> In den nordamerikanischen Versionen können Sie auf der Seite **Bank Rec. Vorschlag** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet. Um diese Seite **Bankkonto Abstimmen** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bank Recon. mit Auto. Entsprechung** auf der Seite **Finanzbuchhaltung Einrichtung** . Weitere Informationen finden Sie im Abschnitt [Bankkonten abstimmen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) unter der lokalen USA-Funktionalität.

Bevor Sie Ihre Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten. Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden. Weitere Informationen finden Sie unter [Einrichten von Banken](bank-setup-banking.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.

| Aktion | Siehe |
| --- | --- |
| Stimmen Sie Bankkonten als separate Aufgabe auf der Seite **Bankkontoabstimmung** ab. |[Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md) |
| Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung auf der Seite **Zahlungsabstimmungsbuch.-Blatt** . |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Verwenden Sie die Bankabstimmung, um zu überprüfen, ob Ihre Bücher auf dem neuesten Stand sind, und veröffentlichen Sie die Abstimmung erst, wenn Sie mit der Abstimmung zufrieden sind.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Banken](bank-setup-banking.md)  
[Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Bank-Geldmittel überweisen](bank-how-transfer-bank-funds.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)
