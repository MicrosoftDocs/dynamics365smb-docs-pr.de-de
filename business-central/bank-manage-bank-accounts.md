---
title: Verwalten von Bankkonten| Microsoft Docs
description: "Sie müssen regelmäßig Bankposten mit den zugehörigen Banktransaktionen in Ihren Bankkonten abstimmen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a>Verwalten von Bankkonten
In regelmäßigen Abständen müssen Sie Ihre Bankposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit den entsprechenden Banktransaktionen auf den Konten bei Ihrer Bank abstimmen, und dann den Saldo auf Ihrem Bankkonto buchen. Diese Aufgabe kann als Teil der Zahlungsverarbeitung auf einem Bankauszug im **Zahlungsabstimmungsbuch.-Blatt** dargestellt werden. Alternativ können Sie die Aufgabe separat ausführen vom Zahlungsprozess, indem das Fenster **Bankkonto Abstimmen**, in dem Sie die Bnkkontoauszugszeilen abstimmen (abgleichen) auf der linken Bereichsseite mit Ihrem internen Bankposten im rechten Fensterbereich. In beiden Fenstern können Sie die Bankkontoauszugsinformationen ausfüllen, indem Sie eine Datei oder einen Feed importieren oder automatische entsprechende Vorschläge verwenden.

> [!NOTE]  
> In den nordamerikanischen Versionen können Sie im Fenster **Bank Rec. Vorschlag** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet. Um dieses Fenster **Bankkonto Abstimmen** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bank Recon. mit Auto. Entsprechung** im Fenster **Finanzbuchhaltung Einrichtung**. Weitere Informationen finden Sie im Abschnitt "Bankkonten abstimmen" unter der der lokalen USA-Funktionalität.

Manchmal müssen Sie Beträge zwischen Bankkonten im [!INCLUDE[d365fin](includes/d365fin_md.md)] transferieren, um Überweisungen bei Ihrer Bank widerzuspiegeln. Diese Aufgabe wird im Fenster **Fibu Buch.-Blatt** auf unterschiedliche Arten, abhängig von der Währung der Geldmittel ausgeführt.

Bevor Sie Bankkonten verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten. Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-setup-banking.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| Aufgabe | Siehe |
| --- | --- |
| Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung im Fenster **Zahlungsabstimmungsbuch.-Blatt**. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Abstimmen von Bankkonten, inklusive Scheckposten, als separate Aufgabe im Fenster **Bankkontoabstimmung**. |[Bankkonten separat abstimmen](bank-how-reconcile-bank-accounts-separately.md) |
| Buchen von Überweisungen zwischen Bankkonten in der gleichen oder in unterschiedlichen Währungen. |[Bank-Geldmittel überweisen](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

