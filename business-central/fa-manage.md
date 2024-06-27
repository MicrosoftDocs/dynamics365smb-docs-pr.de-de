---
title: Verwalten von Anlagen
description: 'Informieren Sie sich über die Funktionalität der Anlagen und verschaffen Sie sich einen Überblick, wie Sie mit Ihren Anlagen arbeiten und diese verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Verwalten von Anlagen

Die Anlagenfunktion in [!INCLUDE[prod_short](includes/prod_short.md)] gibt Ihnen einen Überblick über Ihre Anlagen und hilft, sicherzustellen, dass sie korrekt abgeschrieben werden. Außerdem können Sie darüber Wartungskosten nachverfolgen, Versicherungen verwalten, Anlagentransaktionen buchen und verschiedene Berichte und Statistiken generieren.

## <a name="what-is-a-fixed-asset"></a>Was ist ein Anlage?

Anlagen unterscheidet sich von anderen Artikeln in Ihrem Lager. Ein Anlagevermögen, auch als Kapitalvermögen bezeichnet, ist eine Sachanlage, die Sie besitzen oder verwalten, in der Erwartung, dass sie weiterhin zur Erzielung von Einnahmen beiträgt. Bei einer Anlage handelt es sich um einen Gegenstand, das Ihr Unternehmen nicht innerhalb des nächsten Kalenderjahres verbrauchen, verkaufen oder in Geld umwandeln wird. Anlagen unterscheiden sich vom Umlaufvermögen, das in bar vorliegt oder innerhalb der nächsten 12 Monate in Bargeld umgewandelt werden soll. Anlagen unterscheiden sich auch von Ihrem Lagerbestand, da dieser in der Regel innerhalb kurzer Zeit verbraucht wird.

## <a name="types-of-fixed-assets"></a>Anlagentypen

Unternehmen investieren in der Regel in einige Anlagentypen. Einige Beispiele hierfür sind:

- Gebäude und Einrichtungen
- Computerausrüstung und Software
- Möbel und Maschinen
- Maschinen
- Fuhrpark

## <a name="understanding-fixed-asset-accounting"></a>Anlagenbuchhaltung verstehen

Bei der Anlagenbuchhaltung handelt es sich um präzise Finanzdatensätze zu Ihrem Kapitalvermögen. Diese Datensätze enthalten Details zu den fünf Phasen im Lebenszyklus einer Anlage. Nach dem Erstkauf umfasst der Lebenszyklus jeder Anlage mindestens drei der folgenden Phasen:

- Anschaffung: Sie fügen Ihren Büchern eine neue Anlage hinzu.
- Abschreibung: Sie erfassen den periodischen Wertverlust einer Anlage, den Sie mithilfe einer Abschreibungsmethode berechnen. Weitere Informationen finden Sie unter [Berechnung der Anlageanabschreibung](LocalFunctionality/India/FA_Depreciation.md).
- Neubewertung: Sie erfassen eine Einschätzung des aktuellen Marktwerts eines Vermögenswerts. Weitere Informationen finden Sie unter [Anlagen neu bewerten](fa-how-revalue.md).
- Dauerhafte Wertminderung: Sie erfassen eine Wertminderung aufgrund von Ereignissen oder Umständen.
- Entsorgung: Sie verkaufen, verschrotten oder entsorgen ein Anlagegut am Ende seiner Nutzungsdauer auf andere Weise.

Zu den Betriebsprüfungen zählt auch die eingehende Prüfung der Buchhaltungsunterlagen Ihres Unternehmens nach Abschluss des Geschäftsjahres. Bei internen oder externen Prüfungen stellen Sie unter Umständen Unstimmigkeiten oder Unterschiede zwischen Ihren Aufzeichnungen und dem tatsächlichen Zustand Ihrer Anlagen fest. Überwachungen fördern die Transparenz Ihres Vermögens und Ihrer Buchhaltung, wenn Sie mehr Geld verlieren als erwartet.

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
| Wartungskosten überwachen. | [Wartungskosten überwachen](fa-how-maintain.md#monitor-maintenance-costs)|
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

1. Führen Sie einen Bericht zur Berechnung der periodischen Abschreibung aus.
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
| Wartungskosten überwachen. | [Wartungskosten überwachen](fa-how-maintain.md#monitor-maintenance-costs)|
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

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Tipps zur Verbesserung Ihrer Anlagenbuchhaltung

Es gibt einige Dinge, die Sie in Ihrer Buchhaltungsstrategie für Anlagen umsetzen können, um sicherzustellen, dass Sie Ihre Gewinne maximieren.

- Legen Sie einen Aktivierungsschwellenwert fest. Legen Sie beim Kauf eines Artikels einen festen Betrag für die Aktivierung fest. Der Betrag trägt dazu bei, die Konsistenz Ihrer Kontoblätter sicherzustellen, und erleichtert Ihnen und Ihrem Team das Erkennen von Buchhaltungsfehlern.
- Bewerten Sie den Lebenszyklus der Ausrüstung neu. Es ist wichtig, die Zeitspanne richtig einzuschätzen, in der Sie Ihre Anlagen für ihren ursprünglichen Zweck nutzen können. Da die Buchhaltung und die Abschreibung auf genauen Lebenszyklusschätzungen basieren, sollten Sie bei Bedarf eine Neubewertung vornehmen, da sich diese im Laufe der Zeit ändern können.
- Kennzeichnen Sie Ihre Anlagen. Es ist wichtig, Ihre Anlagen während ihres gesamten Lebenszyklus zu verfolgen und zu kennzeichnen, da ihr Wert von vielen Faktoren beeinflusst werden kann. Durch die Kennzeichnung können Sie Ihre Gegenstände in allen Phasen ihres Lebenszyklus nachverfolgen und Diebstähle verhindern, Fehlplatzierungen vermeiden und Finanzstatistiken unterstützen.
- Automatisieren Sie Einblicke mit einer Software zur Anlagenbuchhaltung. Durch die Automatisierung manueller Aktivitäten zur Nachverfolgung Ihrer Daten mit einer Software zur Anlagenbuchhaltung können Prozesse einfacher abgeschlossen werden. Der Kennwortschutz kann dazu beitragen, dass nur die Personen Zugang erhalten, die ihn benötigen und dafür geschult sind.

## <a name="see-also"></a>Siehe auch

[Einrichten von Anlagen](fa-setup.md)  
[Anlagenanalysen – Übersicht](fa-analytics-overview.md)  
[Finanzen – Übersicht](finance.md)  
[Vorbereitung auf die Verwendung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Angezeigte Features ändern](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
