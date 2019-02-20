---
title: "Aktualisieren von Währungswechselkursen | Microsoft Docs"
description: "Um mehrere Währungen in Ihrem Unternehmen zu verwenden, können Sie einen Code für jede Währung einrichten und einen externen Wechselkursdienst, wie Yahoo verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: de-de
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Währungswechselkurse aktualisieren
Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können. Sie müssen für jede Währung, die Sie verwenden, einen Währungscode einrichten, wenn Sie in anderen Währungen als Ihrer Mandantenwährung verkaufen oder einkaufen, Forderungen oder Verbindlichkeiten haben oder in unterschiedlichen Währungen buchen.

In der Anwendung wird die Finanzbuchhaltung in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet. Wird eine zweite Währung als [!INCLUDE[d365fin](includes/d365fin_md.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, in der Mandantenwährung und der Berichtswährung erfasst. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Regulieren von Wechselkursen
Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in das Programm gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde. Die Stapelverarbeitung  Wechselkurse regulieren dient zur Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. Berichtswährungsbeträge in Sachposten können hiermit ebenfalls aktualisiert werden.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein
Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Währungskurs-Services** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie das Kontrollkästchen **Aktiviert**, um den Service zu aktivieren.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Währungen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird auf der Seite **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-also"></a>Siehe auch
[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)  
[Abschlussjahre und -perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

