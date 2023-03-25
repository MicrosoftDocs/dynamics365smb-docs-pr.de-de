---
title: Posten in unterschiedlichen Währungen ausgleichen
description: 'Wenn Sie an einen Debitor in einer Währung verkaufen, die Zahlung jedoch in einer anderen Währung erfolgt, kann die Rechnung mit der Zahlung ausgeglichen werden.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'multiple currencies, payment, reconcile'
ms.search.form: '148, 460, 25'
ms.date: 04/01/2021
ms.author: edupont
---
# Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren

Falls Sie Einkäufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit dem Einkauf ausgleichen.

Wenn Sie entsprechend an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie die Zahlung mit der Verkaufsrechnung ausgleichen.

Im Folgenden wird beschrieben, wie dies für Kreditorenposten auf der Seite **Kreditoren & Einkauf Einrichtung** eingerichtet wird. Die Einrichtung für Debitorenposten auf der Seite **Debitoren & Verkauf Einrichtung** ist ähnlich.

## So aktivieren Sie den Ausgleich von Kreditorenposten in unterschiedlichen Währungen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kredite und Einkauf Einr. ein** und wählen Sie dann den entsprechenden Link.
2. Wählen Sie im Feld **Währungsausgleich** eine der folgenden Optionen.

| Option | Beschreibung |
| --- | --- |
| Keine |Ausgleich zwischen Währungen ist nicht zugelassen. |
| EWU |Ausgleich zwischen EWU-Währungen ist zugelassen. |
| Alle |Ausgleich zwischen allen Währungen ist zugelassen. |

## So richten Sie Sachkonten für Rundungsdifferenzen beim Währungsausgleich ein

Wenn Sie Posten in unterschiedlichen Währungen ausgleichen, müssen Sie die Sachkonten einrichten, auf die Sie die Rundungsdifferenzen buchen möchten.  

> [!NOTE]  
> Sie müssen die Sachkonten einrichten, bevor Sie die Aufgabe abschließen. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan verstehen](finance-general-ledger.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Debitorenbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditorenbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
4. Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.  

## Siehe verwandte [Microsoft Schulungen](/training/modules/process-foreign-currency-payments-dynamics-365-business-central/)

## Siehe auch

[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
