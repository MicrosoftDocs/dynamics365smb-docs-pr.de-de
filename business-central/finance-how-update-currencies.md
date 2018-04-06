---
title: "Aktualisieren von Währungswechselkursen | Microsoft Docs"
description: "Um mehrere Währungen in Ihrem Unternehmen zu verwenden, können Sie einen Code für jede Währung einrichten und einen externen Wechselkursdienst, wie FloatRates verwenden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 35ecddf35dbe094ef05760ba4148f8ae79e7bf26
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="update-currency-exchange-rates"></a>Währungswechselkurse aktualisieren
Sie müssen für jede Währung, die Sie verwenden, einen Währungscode einrichten, wenn Sie in anderen Währungen als Ihrer Mandantenwährung verkaufen oder einkaufen, Forderungen oder Verbindlichkeiten haben oder in unterschiedlichen Währungen buchen.  

Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können. Die Anwendung unterstützt mehrere Währungen. In der Anwendung wird die Finanzbuchhaltung in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet.  

 Wird eine zweite Währung als zusätzliche Berichtswährung festgelegt, erfasst [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch Beträge für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, in der Mandantenwährung und der Berichtswährung. Wenn Sachpostenbeträge in einer zusätzlichen Berichtswährung berechnet werden, wird der relevante Wechselkurs anhand der Angaben im Fenster **Währungswechselkurse** ermittelt.  

> [!WARNING]  
>  Die Funktion "Berichtswährung" sollte NICHT als Grundlage für die Umrechnung von Finanzauswertungen verwendet werden. Es handelt sich dabei nicht um ein Tool, mit dem Finanzauswertungen von Niederlassungen im Rahmen einer Unternehmenskonsolidierung durchgeführt werden können. Die Berichtswährungsfunktion bietet lediglich die Möglichkeit, Berichte so in anderen Währungen vorzubereiten, als handelte es sich dabei um die Mandantenwährung des Unternehmens.

## <a name="adjusting-exchange-rates"></a>Regulieren von Wechselkursen  
Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in das Programm gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde. Die Stapelverarbeitung  Wechselkurse regulieren dient zur Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. Berichtswährungsbeträge in Sachposten können hiermit ebenfalls aktualisiert werden.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Anzeigen von Berichten und Beträgen in der Berichtswährung  
Eine Berichtswährung kann in folgenden Fällen für das Berichtswesen eines Unternehmens hilfreich sein:  

- Unternehmen in nicht-EU-Ländern/-Regionen mit einem hohen Anteil von Transaktionen mit Unternehmen in EU-Ländern/-Regionen. In diesem Fall möchte das nicht-EU-Unternehmen seine Berichte möglicherweise ebenfalls in Euro erstellen, damit diese für die Handelspartner in der EU besser nutzbar sind.  

- Unternehmen, die Berichte in einer international gehandelten Währung anzeigen möchte, wenn dies auf deren Landeswährung nicht zutrifft.  

Mehrere Berichte im Sachkonto-Anwendungsbereich basieren auf Sachposten. Um die Finanzdaten in dem Bericht in der zusätzlichen Berichtswährung anzuzeigen, wählen Sie einfach das Feld **In zusätzlicher Währung anzeigen** im Fenster für den entsprechenden Sachkontobericht.  

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein
Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten.

1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie das Kontrollkästchen **Aktiviert**, um den Service zu aktivieren.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird im Fenster **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-also"></a>Siehe auch
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

