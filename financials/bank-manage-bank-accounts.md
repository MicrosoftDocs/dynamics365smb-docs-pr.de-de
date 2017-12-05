---
title: Verwalten von Bankkonten| Microsoft Docs
description: "Sie müssen regelmäßig Bankposteneinträge in Financials mit den verknüpften Banktransaktionen in Ihren Bankkonten abstimmen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 2e8314c6da4da73712787a40204a964922f153f4
ms.contentlocale: de-de
ms.lasthandoff: 10/17/2017

---
# <a name="managing-bank-accounts"></a>Verwalten von Bankkonten
In regelmäßigen Abständen müssen Sie Ihre Bankposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit den entsprechenden Banktransaktionen auf den Konten bei Ihrer Bank abstimmen, und dann den Saldo auf Ihrem Bankkonto buchen. Diese Aufgabe kann als Teil der Zahlungsverarbeitung auf einem Bankauszug im **Zahlungsabstimmungsbuch.-Blatt** dargestellt werden. Alternativ können Sie die Aufgabe unabhängig von der Zahlungsverarbeitung im Fenster **Bankkontoabstimmung** ausführen, in dem Scheckposten unterstützt werden. In beiden Fällen füllen Sie das Fenster aus, indem Sie den Bankkontoauszug in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.

Manchmal müssen Sie Beträge zwischen Bankkonten im [!INCLUDE[d365fin](includes/d365fin_md.md)] transferieren, um Überweisungen bei Ihrer Bank widerzuspiegeln. Diese Aufgabe wird im Fenster **Fibu Buch.-Blatt** auf unterschiedliche Arten, abhängig von der Währung der Geldmittel ausgeführt.

Bevor Sie Bankkonten verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten. Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-setup-banking.md).

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

| Aufgabe | Siehe |
| --- | --- |
| Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung im Fenster **Zahlungsabstimmungsbuch.-Blatt**. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Abstimmen von Bankkonten, inklusive Scheckposten, als separate Aufgabe im Fenster **Bankkontoabstimmung**. |[Gewusst wie: Bankkonten separat abstimmen](bank-how-reconcile-bank-accounts-separately.md) |
| Buchen von Überweisungen zwischen Bankkonten in der gleichen oder in unterschiedlichen Währungen. |[Gewusst wie: Bank-Geldmittel überweisen](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

