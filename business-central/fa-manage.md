---
title: Verwalten von Anlagen (enthält Video)
description: 'Informieren Sie sich über die Funktionalität der Anlagen und verschaffen Sie sich einen Überblick, wie Sie mit Ihren Anlagen arbeiten und diese verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Verwalten von Anlagen

Die Anlagenfunktion in [!INCLUDE[prod_short](includes/prod_short.md)] gibt Ihnen einen Überblick über Ihre Anlagen und stellt die korrekten periodischen Abschreibungen sicher. Außerdem erhalten Sie dort einen Überblick über die Wartungskosten, können die Versicherungen verwalten, Anlagentransaktionen buchen und verschiedene Berichte und Statistiken generieren.

## <a name="video-overview"></a>Videoübersicht

Das folgende Video behandelt die Grundlagen von Anlagen:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="fixed-assets-overview"></a>Anlagen – Übersicht

Sie müssen für jede Anlage eine Karte mit entsprechenden Informationen zur Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Dann können Sie beginnen, die Anlagen zu erwerben, zu verwalten und zu verkaufen. Sie können auch Plananlagen einrichten. Durch die Budgetierung haben Sie die Möglichkeit, geplante Anschaffungen und Verkäufe in Berichten zu berücksichtigen.

> [!IMPORTANT]
> Bevor Sie Anlagen verwalten können, müssen Sie die folgenden Einstellungen vornehmen:
>
> * Standardwerte
> * Anlagenbuchhaltung
> * Buchungsgruppen
> * Verteilungsschlüssel
> * Anlagen-Buch.-Blätter
>
> Weitere Informationen finden Sie unter [Einrichten von Anlagen](fa-setup.md).

Um Anlagenabscheibungen und andere finanzielle Transaktionen rund um Anlagen nachzuverfolgen, richten Sie mindestens ein AfA-Buch für jede Anlage ein. Die Abschreibung wird vorgenommen, indem ein Bericht ausgeführt wird, der die periodische Abschreibung berechnet und ein Buch.-Blatt mit den daraus resultierenden Posten ausfüllt und das Buch.-Blatt dann bucht. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene AfA-Methoden. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md). Sie können mehrere AfA-Bücher pro Anlage für unterschiedliche Zwecke einrichten, beispielsweise eins für eine Steuerberichterstellung und ein weiteres zur internen Berichterstellung.

Für jede Anlage können Sie die Wartungskosten und das nächste Servicedatum erfassen. Die Nachverfolgung der Wartungskosten ist unter Umständen für die Budgetierung und die Entscheidung über den Verkauf einer Anlage wichtig.

Sie können jede Anlage einer oder mehreren Versicherungspolicen zuordnen und überprüfen, ob die Versicherungsprämien dem Wert der Anlagen entsprechen.

> [!NOTE]  
> Hinweis: Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Buch.-Blatt** oder auf der Seite **Anlagen Buch - Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird. Weitere Informationen finden Sie unter [Abschreibungen für Anlagen festlegen](fa-how-setup-depreciation.md).

## <a name="how-to-use-fixed-assets"></a>Anlagen verwenden

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

| Bis  | Siehe |
| --- | --- |
| Richten Sie die Voraussetzungen für die Verwendung des Anlagenfeatures ein (legen Sie Standardwerte, Anlagenbuchungen, Buchungsgruppen, Verteilungsschlüssel, Buch.-Blätter und Buchungsarten fest). | [Einrichten von Anlagen](fa-setup.md)|
| Erstellen von Anlagen, Zuordnen von AfA-Methoden, Buchen von Anschaffungen und Restwerten sowie Drucken von Anlagenübersichten |[Erworbene Anlagen](fa-how-acquire.md) |
| Erfassen von Servicebesuchen, Buchen und Überwachen von Wartungskosten. |[Anlagen verwalten](fa-how-maintain.md) |
| Aktualisieren von Versicherungsinformationen, Buchen von Anschaffungskosten auf Versicherungspolicen, Anpassen der Versicherungsdeckung, Anzeigen der Versicherungsstatistik und Auflisten von Versicherungspolicen |[Versichern von Anlagen](fa-how-insure.md) |
| Umbuchen von Anlagen, Transferieren von Anlagen an verschiedene Standorte sowie Aufteilen oder Zusammenfassen von Anlagen |[Übertragen, Teilen oder Kombinieren von Anlagen](fa-how-trans-split-combine.md) |
| Anpassen der Werte von Anlagen, Buchen von Zuschreibungen und Buchen von erhöhten AfA-Transaktionen |[Anlagen neu bewerten](fa-how-revalue.md) |
| Berechnen und Buchen der AfA und Analysieren der AfA in Anlagenberichten. |[Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md) |
| Informieren Sie sich über verschiedene Anlagen-AfA-Methoden. |[Abschreibungsmethoden](fa-depreciation-methods.md) |
| Buchen von Verkaufstransaktionen, Anzeigen von Verkaufsposten und Buchen von Teilverkäufen |[Anlagen entsorgen oder außer Dienst stellen](fa-how-dispose-retire.md) |
| Verwalten von Anlagenbudgets, Budgetieren von Anschaffungskosten, Budgetieren von Anlagenverkäufen und Budgetieren der AfA. |[Budgets für Anlagen verwalten](fa-how-manage-budgets.md) |
| Erfahren Sie mehr über integrierte Berichts- und Analysefunktionen für Anlagen. | [Anlagenberichte und -analysen](fa-reports.md) |

## <a name="see-also"></a>Siehe auch

[Einrichten von Anlagen](fa-setup.md)  
[Finanzen – Übersicht](finance.md)  
[Vorbereitung auf die Verwendung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Angezeigte Features ändern](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
