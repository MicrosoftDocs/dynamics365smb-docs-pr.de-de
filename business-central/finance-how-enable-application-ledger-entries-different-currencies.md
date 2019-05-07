---
title: Ausgleichen von Posten in unterschiedlichen Währungen| Microsoft Docs
description: Wenn Sie an einen Debitor in einer Währung verkaufen, die Zahlung jedoch in einer anderen Währung erfolgt, kann die Rechnung mit der Zahlung ausgeglichen werden.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1569ff45bbbf8c3bf63538abdab143f9851a23a6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "919168"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren
Falls Sie Einkäufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit dem Einkauf ausgleichen.

Wenn Sie entsprechend an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie die Zahlung mit der Verkaufsrechnung ausgleichen.

Im Folgenden wird beschrieben, wie dies für Kreditorenposten auf der Seite **Kreditoren & Einkauf Einrichtung** eingerichtet wird. Die Einrichtung für Debitorenposten auf der Seite **Debitoren & Verkauf Einrichtung** ist ähnlich.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>So aktivieren Sie den Ausgleich von Kreditorenposten in unterschiedlichen Währungen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Käufe und Verkäufe einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Feld **Währungsausgleich** eine der folgenden Optionen.

| Option | Beschreibung |
| --- | --- |
| Keine |Ausgleich zwischen Währungen ist nicht zugelassen. |
| EWU |Ausgleich zwischen EWU-Währungen ist zugelassen. |
| Alle |Ausgleich zwischen allen Währungen ist zugelassen. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>So richten Sie Sachkonten für Rundungsdifferenzen beim Währungsausgleich ein  
Wenn Sie Posten in unterschiedlichen Währungen ausgleichen, müssen Sie die Sachkonten einrichten, auf die Sie die Rundungsdifferenzen buchen möchten.  

> [!NOTE]  
>  Sie müssen die Sachkonten einrichten, bevor Sie die Aufgabe abschließen. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan verstehen](finance-general-ledger.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitorenbuchungsruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.  
3. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkäufer-Buchungsgruppen** ein, und wählen dann den zugehörigen Link aus.  
4. Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
