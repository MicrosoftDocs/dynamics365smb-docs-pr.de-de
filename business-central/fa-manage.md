---
title: Verwalten von Anlagen (enthält Video)
description: 'Informieren Sie sich über die Funktionalität der Anlagen und verschaffen Sie sich einen Überblick, wie Sie mit Ihren Anlagen arbeiten und diese verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Verwalten von Anlagen

Die Anlagenfunktion in [!INCLUDE[prod_short](includes/prod_short.md)] gibt Ihnen einen Überblick über Ihre Anlagen und hilft, sicherzustellen, dass sie korrekt abgeschrieben werden. Außerdem können Sie darüber Wartungskosten nachverfolgen, Versicherungen verwalten, Anlagentransaktionen buchen und verschiedene Berichte und Statistiken generieren.

## <a name="video-overview"></a>Videoübersicht

Das folgende Video behandelt die Grundlagen von Anlagen:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Anlagen erstmals einrichten

Bevor Sie Anlagen verwalten können, müssen Sie die folgenden Einstellungen vornehmen:

- Standardwerte
- Anlagenbuchhaltung
- Buchungsgruppen und -typen
- Verteilungsschlüssel
- Anlagen-Buch.-Blätter

Weitere Informationen finden Sie unter [Einrichten von Anlagen](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Anlagenanalysen

In diesem Abschnitt werden die Analysetools beschrieben, mit denen Sie sich Einblick in die Daten über Ihre Anlagen verschaffen können.

| Zweck ... | Siehe |
| --- | --- |
| Die Möglichkeiten zur Analyse von Daten über Anlagen kennenlernen. | [Anlagenanalysen – Übersicht](fa-analytics-overview.md) |
| Ad-hoc-Analysen von Anlagendaten direkt auf Listenseiten und in Abfragen durchführen. | [Ad-hoc-Analysen von Anlagendaten](ad-hoc-analysis-fa.md) |
| Sich mit den integrierten Berichten für Anlagen vertraut machen. | [Integrierte Anlagenberichte](fa-reports.md) |
| Wartungskosten überwachen. | [Wartungskosten überwachen](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Versicherungen überwachen. | [Versicherungsdeckung überwachen](fa-how-insure.md#to-monitor-insurance-coverage) |
| Anzeigen von Verkaufsposten | [Verkaufsposten anzeigen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Geschätzte Verkaufswerte anzeigen. | [Geschätzte Verkaufswerte anzeigen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Anlagen eintragen

Sie müssen für jede Anlage eine Karte mit entsprechenden Informationen darüber einrichten. Gebäude oder Produktionseinrichtungen können zum Beispiel als Hauptanlagen mit einer Komponentenliste eingerichtet werden. Sie können Anlagen auf verschiedene Arten gruppieren, beispielsweise nach Klasse, Kostenstelle oder Standort. Dann können Sie die Anlagen erwerben, verwalten und verkaufen. Sie können auch Plananlagen einrichten. Durch die Budgetierung haben Sie die Möglichkeit, geplante Anschaffungen und Verkäufe in Berichten zu berücksichtigen.

| Bis  | Siehe |
| --- | --- |
| Verwalten von Anlagenbudgets, Budgetieren von Anschaffungskosten, Budgetieren von Anlagenverkäufen und Budgetieren der AfA. |[Budgets für Anlagen verwalten](fa-how-manage-budgets.md) |
| Erstellen von Anlagen, Zuordnen von AfA-Methoden, Buchen von Anschaffungen und Restwerten sowie Drucken von Anlagenübersichten |[Anlagen erwerben](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Abschreibungen für Ihre Anlagen einrichten

Um Anlagenabscheibungen und andere finanzielle Transaktionen rund um Anlagen nachzuverfolgen, richten Sie mindestens ein AfA-Buch für jede Anlage ein. Es gibt mehrere Schritte, um Anlagen abzuschreiben:

1. Führen Sie einen Bericht aus, um die periodische Abschreibung zu berechnen.
1. Gehen Sie in ein Buch.-Blatt die entsprechenden Einträge ein.
1. Buchen Sie die Buch.-Blattzeile.

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene AfA-Methoden. Weitere Informationen finden Sie unter [Abschreibungsmethoden](fa-depreciation-methods.md). Sie können für jede Anlage mehrere AfA-Bücher für unterschiedliche Zwecke einrichten, beispielsweise eins für eine Steuerberichterstellung und ein weiteres zur internen Berichterstellung.

| Zweck  | Siehe |
| --- | --- |
| Informieren Sie sich über verschiedene Anlagen-AfA-Methoden. |[Abschreibungsmethoden](fa-depreciation-methods.md) |
| Berechnen und Buchen der AfA und Analysieren der AfA in Anlagenberichten. |[Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md) |
| Geänderte Abschreibungsbuchwerte anzeigen. | [Geänderte AfA-Buchwerte anzeigen](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Buch.-Blatt** oder auf der Seite **Anlagen Buch - Blatt** manuell erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. | [Abschr. Anlagevermögen einrichten](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Wartung und Versicherung von Anlagen

Sie können für jede Anlage die Wartungskosten und das nächste Wartungsdatum erfassen. Die Nachverfolgung der Wartungskosten ist unter Umständen für die Budgetierung und die Entscheidung über den Verkauf einer Anlage wichtig. Sie können jede Anlage einer oder mehreren Versicherungspolicen zuordnen und überprüfen, ob die Versicherungsprämien dem Wert der Anlagen entsprechen.

| Bis  | Siehe |
| --- | --- |
| Erfassen von Servicebesuchen, Buchen und Überwachen von Wartungskosten. |[Anlagen verwalten](fa-how-maintain.md) |
| Wartungskosten überwachen. | [Wartungskosten überwachen](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Aktualisieren von Versicherungsinformationen, Buchen von Anschaffungskosten auf Versicherungspolicen, Anpassen der Versicherungsdeckung, Anzeigen der Versicherungsstatistik und Auflisten von Versicherungspolicen |[Anlagen versichern](fa-how-insure.md) |
| Versicherungen überwachen. | [Versicherungsdeckung überwachen](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Umbuchen, Übertragung, Aufteilung/Zusammenlegung, Wertberichtigung, Abschreibung und Veräußerung von Anlagen

| Bis  | Siehe |
| --- | --- |
| Umbuchen von Anlagen, Transferieren von Anlagen an verschiedene Standorte sowie Aufteilen oder Zusammenfassen von Anlagen |[Übertragen, Teilen oder Kombinieren von Anlagen](fa-how-trans-split-combine.md) |
| Anpassen der Werte von Anlagen, Buchen von Zuschreibungen und Buchen von erhöhten AfA-Transaktionen |[Anlagen neu bewerten](fa-how-revalue.md) |
| Buchen von Verkaufstransaktionen, Anzeigen von Verkaufsposten und Buchen von Teilverkäufen |[Anlagen entsorgen oder außer Betrieb nehmen](fa-how-dispose-retire.md) |
| Anzeigen von Verkaufsposten | [Verkaufsposten anzeigen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Geschätzte Verkaufswerte anzeigen. | [Geschätzte Verkaufswerte anzeigen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="see-also"></a>Siehe auch

[Einrichten von Anlagen](fa-setup.md)  
[Überblick über die Anlagenanalyse](fa-analytics-overview.md)  
[Finanzen – Übersicht](finance.md)  
[Vorbereitung auf die Verwendung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Angezeigte Features ändern](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
