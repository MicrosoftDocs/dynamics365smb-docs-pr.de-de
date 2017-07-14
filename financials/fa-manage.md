---
title: Anlagen| Microsoft Docs
description: Beschreibt, wie Anlagen verwaltet werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d57603202d9e2e5304c899eaf764dde8cfa6369d
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Anlagen
<a id="fixed-assets" class="xliff"></a>
Die Anlagenfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt Ihnen einen Überblick über Ihre Anlagen und stellt die korrekten periodischen Abschreibungen sicher. Außerdem erhalten Sie dort einen Überblick über die Wartungskosten, können die Versicherungen verwalten, Anlagentransaktionen buchen und verschiedene Berichte und Statistiken generieren.

Sie müssen für jede Anlage eine Karte mit entsprechenden Informationen zur Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Dann können Sie beginnen, die Anlagen zu erwerben, zu verwalten und zu verkaufen. Sie können auch Plananlagen einrichten. Dadurch haben Sie die Möglichkeit, geplante Anschaffungen und Verkäufe in Berichten zu berücksichtigen.

Um Anlagenabscheibungen sowie andere finanzielle Transaktionen, die sich auf die Anlagen beziehen, nachzuverfolgen, richten Sie mindestens ein AfA-Buch für jede Anlage in Ihrem Unternehmen ein. Die Abschreibung wird getätigt, indem ein Bericht ausgeführt wird, der die periodische Abschreibung berechnet und ein Buch.-Blatt mit den daraus resultierenden Posten ausfüllt, die dann gebucht werden. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt verschiedene AfA-Methoden. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md). Sie können mehrere AfA-Bücher pro Anlage für unterschiedliche Zwecke einrichten, beispielsweise eins für eine Steuerberichterstellung und ein weiteres zur internen Berichterstellung.

Für jede Anlage können Sie die Wartungskosten und das nächste Servicedatum erfassen. Durch die Überwachung der Wartungskosten werden die Budgetierung und die Entscheidung über den Verkauf einer Anlage erleichtert.

Jede Anlage kann mit Versicherungspolicen verknüpft werden. Daher haben Sie die Möglichkeit zu überprüfen, ob die Deckungsbeiträge in den Versicherungspolicen mit dem Wert der Anlagen übereinstimmen. Damit ist auch die Möglichkeit gegeben, die jährlichen Versicherungsprämien zu prüfen.

**Hinweis**: Sie können Anlagentransaktionen im Fenster **Anlagen Fibu Buch.-Blatt** oder im Fenster **Anlagen Buch - Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird. Weitere Informationen finden Sie unter [So geht's: Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).

**Hinweis**: Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen].

Bevor Sie mit dem Verwalten von Anlagen beginnen können, müssen Sie Standardwerte, Anlagenbuchungen, Buchungsgruppen, Verteilungsschlüsseln, Buch.-Blätter und Buchungsarten einrichten. Weitere Informationen finden Sie unter [Einrichten von Anlagen](fa-setup.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| Aufgabe | Siehe |
| --- | --- |
| Erstellen von Anlagen, Zuordnen von AfA-Methoden, Buchen von Anschaffungen und Restwerten sowie Drucken von Anlagenübersichten |[So geht's: Beschaffen von Anlagen](fa-how-acquire.md) |
| Erfassen von Servicebesuchen, Buchen und Überwachen von Wartungskosten. |[So geht's: Anlagen aktualisieren](fa-how-maintain.md) |
| Aktualisieren von Versicherungsinformationen, Buchen von Anschaffungskosten auf Versicherungspolicen, Anpassen der Versicherungsdeckung, Anzeigen der Versicherungsstatistik und Auflisten von Versicherungspolicen |[So geht's: Versichern von Anlagen](fa-how-insure.md) |
| Umbuchen von Anlagen, Transferieren von Anlagen an verschiedene Standorte sowie Aufteilen oder Zusammenfassen von Anlagen |[So geht's: Übertragen, Teilen oder Kombinieren von Anlagen.](fa-how-trans-split-combine.md) |
| Anpassen der Werte von Anlagen, Buchen von Zuschreibungen und Buchen von erhöhten AfA-Transaktionen |[So geht's: Anlagen neu bewerten](fa-how-revalue.md) |
| Berechnen und Buchen der AfA und Analysieren der AfA in Anlagenberichten. |[So geht's: Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md) |
| Buchen von Verkaufstransaktionen, Anzeigen von Verkaufsposten und Buchen von Teilverkäufen |[So geht's: Anlagen entsorgen oder außer Dienst stellen](fa-how-dispose-retire.md) |
| Verwalten von Anlagenbudgets, Budgetieren von Anschaffungskosten, Budgetieren von Anlagenverkäufen und Budgetieren der AfA. |[So geht's: Budgets für Anlagen verwalten](fa-how-manage-budgets.md) |

## Siehe auch
<a id="see-also" class="xliff"></a>
[Anlagen einrichten](fa-setup.md)  
[Die Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] anpassen](ui-experiences.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
