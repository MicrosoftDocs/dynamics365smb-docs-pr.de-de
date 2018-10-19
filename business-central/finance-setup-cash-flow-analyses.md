---
title: Cashflow-Analyse einrichten | Microsoft Docs
description: "Einrichten der Diagramme im Feld Konto-Rollencenter, die Ihnen helfen, die Richtung des Geldes in Ihrem Unternehmen, einschließlich Ausgaben und Umsatz, Liquidität und Zahlungseingänge minus der Barzahlungen zu analysieren."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24ca91f224a198ec462081ced06ddfe0e9db6cf4
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-cash-flow-analysis"></a>Aufstellung Cashflow-Analyse
Wenn Sie etwas Unterstützung benötigen, was Sie mit Ihrem Barkonto zu tun sollen, schauen Sie sich das Diagramm im Buchhalter-Rollencenter an:  

* **Bargeldumlauf**  
* **Einnahmen und Ausgaben**  
* **Cashflow**  
* **Cashflowplanungen**  

Dieses Thema beschreibt, wo die Daten in den Diagrammen herkommen und was zu tun ist, um die Diagramme zu nutzen.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Diagramme Geldumlauf und Einnahmen und Ausgaben
Die Diagramme **Bargeldumlauf** und **Einnahmen und Ausgaben** stehen für die Nutzung bereit, basierend auf dem Kontenplan und dem Kontenschemata. Die Konten sind dort, wo die Daten herkommen und die Kontenschemata berechnen die Beziehung zwischen Verkauf und Debitoren. Einige Konten und Kontenschemata werden bereitgestellt. Sie können sie verwenden, um sie zu ändern und neue hinzufügen. Wenn Sie z. B. Sachkonten Ihrem Kontenplan hinzufügen indem Sie sie aus QuickBooks importieren, müssen Sie die Konten auf der Seite **Kontenschemata** folgenden Kontenschemanamen zuweisen:  

| Kontenschemaname | Wo sie verwendet werden |
| --- | --- |
| **I_CACYCLE** |Bargeldumlauf |
| **I_CASHFLOW** |Cashflow |
| **I_INCEXP** |Einnahmen und Ausgaben |
| **I_MINTRIAL** |Als GuV-Konten, wenn Sie nicht den Kontenplan verwenden |

**Hinweis** Es ist sinnvoll, die Berechnungen zu behalten, die für das Kontenschema bereitgestellt werden.  

Geben Sie im Feld **Zusammenzählung** das Feld **Umsätze, gesamt**, **Forderungen gesamt**, **Verbindlichkeiten gesamt** und **Lager gesamt** ein. Um eine Reihe von Konten oder mehr als ein bestimmtes Konto zu verteilen, geben Sie die Kontonummern ein, die mit ".." oder einem senkrechten Strich geteilt werden. Beispielsweise **1111..4444** or **2222|3333|5555**.  

**Tipp** Überprüfen Sie die Zuordnung, indem Sie die Aktion **Übersicht** auswählen.  

## <a name="set-up-the-cash-flow-chart"></a>Richtet den Cashflow-Kontenplan ein.
Das Cashflow-Diagramm basiert auf Folgendem:  

* Einem Diagramm von Cashflow-Konten.
* Einem oder mehrerer Cashflow-Einstellungen. Das gibt die Konten an, die für die Bereiche Finanzbuchhaltung, Einkauf, Verkauf, Services und Anlagen verwendet werden.  

Einige Konten und Cashfloweinrichtung sind bereits bereitgestellt. Sie können diese ändern, hinzufügen oder entfernen.  

Um diese einzurichten, suchen Sie für nach **Cashflowkonten**, wählen Sie den Link aus, und füllen Sie die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Wiederholen Sie diese Schritte für **Cashfloweinrichtung**.  

## <a name="set-up-cash-flow-forecasts"></a>Richtet Cashflowplanungen ein
Das Diagramm **Cashflowplanung** verwendet Cashflowkonten, Cashfloweinrichtung und Cashflowplanungen. Einige werden bereitgestellt, aber Sie können eigene einrichten, indem Sie die unterstützte Einrichtung verwenden. Die unterstützte Einrichtung definiert u.a., wie oft die Planung aktualisiert werden soll, die Konten, die darauf basieren sollen, Informationen darüber, wann Sie Steuern bezahlen und ob [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) verwendet werden soll.  

Cashflowplanungen können Cortana Intelligence verwenden, um Dokumente mit einem Fälligkeitsdatum in der Zukunft zu berücksichtigen. Das Ergebnis ist eine umfassendere Voraussage. Die Verknüpfung zu Cortana Intelligence ist bereits eingerichtet. Sie müssen sie nur aktivieren. Wenn Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden, wird eine Benachrichtigung in einer blauen Leiste angezeigt mit einem Link zur Standardcashfloweinrichtung. Die Mitteilung wird jeweils nur einmal angezeigt. Wenn Sie sie schließen, sich aber dazu entscheiden, Cortana Intelligence zu aktivieren, können Sie die unterstützte Einrichtung oder den manuellen Vorgang nutzen.  

> [!NOTE]  
>   Alternativ können Sie Ihren eigenen vorbestimmten Webdienst verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden von eigenen vorbestimmten Webdiensten für Cashflowplanungen](#AnchorText).  

Um die unterstützte Einrichtung zu verwenden:  

1. Im Buchhalterrollencenter unter **Cashflow-Planung** wählen Sie die Aktion **Unterstütze Einrichtung** aus.  
2. Füllen Sie die Felder soweit erforderlich für jeden Schritt aus.  
3. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Cash Flow Planung** ein, und wählen dann den zugehörigen Link aus.
4. Im Fenster **Cashflowplanung** wählen Sie die **Berechnen Sie Planung nach** Aktion aus.  

Um einen manuellen Vorgang zu verwenden:  

1. Im Feld Buchhalter-Rollencenter suchen Sie nach **Cashfloweinrichtung** und wählen Sie dann den zugehörigen Link aus.  
2. Erweitern Sie das Inforegister **Cortana Intelligence** und aktivieren Sie dann das Kontrollkästchen **Cortana Intelligence aktiviert**.  
3. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Cash Flow Planung** ein, und wählen dann den zugehörigen Link aus.
4. Im Fenster **Cashflowplanung** wählen Sie die **Berechnen Sie Planung nach** Aktion aus.  

> [!TIP]  
>   Beachten Sie die Länge der Perioden, die der Service in den Berechnungen verwendet. Je mehr Daten Sie liefern, umso genauer wird die Vorhersage sein. Halten Sie auch nach umfangreichen Abweichungen in Perioden Ausschau. Sie werden ebenfalls Auswirkungen auf die Vorhersagen haben. Wenn Cortana-Intelligenz nicht genügend Daten findet oder die Daten stark abweichen, wird der Service keine Vorhersage machen.  

## <a name="AnchorText"> </a>erstellt und verwendet Ihren eigenen vorhersagenden Webdienst für Cashflowplanungen.
Sie können Ihren eigenen vorhersagenden Webdienst auf einem öffentliches Modell erzeugen, dem **Prognosemodell für Microsoft Business Central**. Dieses vorhersagende Modell ist online im Cortana Intelligence Katalog verfügbar. Um das Modell zu verwenden, gehen folgendermaßen vor:  

1. Öffnen Sie einem Browser und gehen Sie zum [Cortana Intelligence Katalog](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Suchen Sie nach dem **Vorhersagemodell für Microsoft  Business Central** und öffnen Sie dann das Modell im Azure Machine Learning Studio.  
3. Verwenden Sie das Microsoft-Konto, um sich für einen Arbeitsbereich anzumelden und kopieren Sie dann das Muster.  
4. Führen Sie die Vorlage aus und veröffentlichen Sie dieses als Webdienst.  
5. Notieren Sie den API URL und den API Schlüssel. Sie verwenden diese Anmeldeinformationen für die Cashfloweinrichtung.  
6. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Cash Flow Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
7. Erweitern Sie das Inforegister **Cortana Intelligence** und füllen Sie die Felder wie notwendig aus.  

## <a name="see-also"></a>Siehe auch
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

