---
title: Häufig gestellte Fragen zur Analyseunterstützung (Vorschauversion)
description: 'Diese häufig gestellten Fragen bietet Informationen zu der für die Analyse von Daten auf Seiten in Business Central verwendeten KI-Technologie. Dazu gehören auch wichtige Überlegungen und Details dazu, wie KI verwendet wird, wie sie getestet und bewertet wurde und welche spezifischen Einschränkungen bestehen.'
ms.date: 02/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-analysis-assist-preview"></a>Häufig gestellte Fragen zur Analyseunterstützung (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen des Features zur Analyseunterstützung in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-analysis-assist"></a>Was ist die Analyseunterstützung?

Die Analyseunterstützung ist ein Copilot, der Sie bei der Arbeit mit dem [Datenanalysemodus](analysis-mode.md) in Business Central unterstützt. Mit dem Datenanalysemodus können Sie Daten auf Seiten und in Abfragen organisieren, aggregieren und zusammenfassen, sodass sie für die Analyse und Gewinnung aussagekräftiger Erkenntnisse besser geeignet sind. Mit der Analyseunterstützung können Sie automatisch die Ansicht der zu analysierenden Daten erstellen, indem Sie Ihre Anforderungen in einfacher, natürlicher Sprache ausdrücken, z. B. „Kreditoren nach Standort und sortiert nach Anzahl der Einkäufe anzeigen.“ Die Analyseunterstützung erleichtert die Arbeit mit Daten und erfordert keine komplexen technischen Kenntnisse.

## <a name="what-are-capabilities-of-analysis-assist"></a>Welche Möglichkeiten bietet die Analyseunterstützung?

Die Analyseunterstützung basiert auf den Entwicklertools für Copilot in Business Central. Sie verwendet Azure OpenAI um unstrukturierte Anweisungen in ein strukturiertes Design zur Anzeige von Daten im Analysemodus umzuwandeln, ohne die Geschäftsdaten der Kundschaft selbst zu erstellen, zu ändern oder zu aktualisieren.

## <a name="what-is-the-intended-use-of-analysis-assist"></a>Wozu dient die Analyseunterstützung?

Die Analyseunterstützung ist dazu gedacht, Analyseregisterkarten im Datenanalysemodus zu erstellen, um Daten so darzustellen, dass leichter Schlussfolgerungen daraus gezogen werden können. Es ist jedoch wichtig zu beachten, dass die Analyseunterstützung keine direkten Erkenntnisse oder Schlussfolgerungen zu den Daten bietet. Sie ist ein Tool, mit dem Benutzende ihre Daten organisieren und anzeigen können. Letztendlich müssen die Benutzenden aber selbst verwertbare Informationen extrahieren, Trends erkennen und fundierte Entscheidungen zur Steigerung des geschäftlichen Werts treffen.

## <a name="how-was-analysis-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Wie wurde die Analyseunterstützung bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

- Das Feature wurde basierend auf den [!INCLUDE[prod_short](includes/prod_short.md)] Demodaten und anderen fiktiven Produktkatalogen umfassend getestet. Copilot erhielt in den unterstützten englischen Sprachumgebungen zahlreiche Prompts. Die Prompts deckten ein breites Spektrum an Anweisungen zur Datenanalyse und Stilen zur Klarstellung der Absicht ab. Die Ergebnisse wurden auf Genauigkeit, Relevanz und Sicherheit bewertet.

- Das Feature basiert auf dem Standard für verantwortungsbewusste KI von Microsoft. [Erfahren Sie mehr über verantwortungsbewusste KI von Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Wie überwacht Microsoft die Qualität der generierten Inhalte?

Microsoft verfügt über verschiedene Systeme, um sicherzustellen, dass die von Copilot generierten Inhalte von höchster Qualität sind, Missbrauch zu erkennen und die Sicherheit unserer Kundschaft und ihrer Daten zu gewährleisten.

Benutzende haben die Möglichkeit, zu jeder Copilot-Antwort Feedback zu geben und ungenaue oder unangemessene Inhalte zu melden, um Microsoft bei der Verbesserung dieses Features zu unterstützen.

- Wenn Sie auf unangemessen generierte Inhalte stoßen, melden Sie diese Microsoft mithilfe dieses Feedbackformulars: [Missbrauch melden](https://go.microsoft.com/fwlink/?linkid=2249810).

- Wir analysieren und nutzen das Feedback der Benutzenden zu dem Feature, um die Antworten zu verbessern.

  Sie geben Feedback, indem Sie das Symbol „Gefällt mir“ (Daumen hoch) oder „Gefällt mir nicht“ (Daumen runter) auf dem **Copilot**-Bereich in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.

- Microsoft kann die Copilot-gesteuerten Features für ausgewählte Kundschaft deaktivieren, wenn ein Missbrauch der Funktionalität festgestellt wird.

## <a name="what-are-the-limitations-of-analysis-assist-how-can-users-minimize-the-impact-of-the-analysis-assist-limitations-when-using-the-system"></a>Welche Einschränkungen gelten für die Analyseunterstützung? Wie können Benutzende die Auswirkungen der Einschränkungen der Analyseunterstützung bei der Nutzung des Systems minimieren?

- Allgemeine Einschränkungen von KI

  KI-Systeme sind wertvolle Werkzeuge, aber sie sind nichtdeterministisch. Die Inhalte, die sie generieren, sind möglicherweise nicht korrekt. Daher müssen Sie unbedingt Ihr eigenes Urteilsvermögen einsetzen, um die Antworten von Copilot zu überprüfen und zu bestätigen, bevor Sie Entscheidungen treffen, die sich auf Interessengruppen wie Debitoren und Partner auswirken könnten.

- Sprachliche und geografische Einschränkungen:

  - Die Analyseunterstützung wird nur in Englisch und nur für die folgenden Gebietsschemas unterstützt: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Wenn die Anzeigesprache in Business Central nicht zu den aufgeführten Gebietsschemas gehört, ist das Feature nicht verfügbar.

  - Die Qualität der Antworten kann geringer ausfallen, wenn:
    - Das Sprachgebietsschema in Business Central nicht en-US ist.
    - Die Spracheinstellung des Benutzenden in Business Central von der primären Sprache der Geschäftsdaten in der [!INCLUDE[prod_short](includes/prod_short.md)] Datenbank abweicht.
  
  - Geografische Einschränkungen:
  
    Das Feature ist aufgrund gesetzlicher Vorschriften im Hinblick auf die Sprache in allen unterstützten [Business Central-Ländern/-Regionen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) außer Kanada verfügbar. Das Feature verwendet jedoch den Microsoft Azure OpenAI-Dienst, der derzeit nur in einigen Regionen für Business Central verfügbar ist. Wenn sich Ihre Umgebung in einem Land/einer Region befindet, in welcher der Azure OpenAI-Dienst nicht verfügbar ist, müssen Ihre Administrierenden zulassen, dass Daten über geografische Grenzen hinweg verschoben werden. [Weitere Informationen](/dynamics365/business-central/ai-copilot-data-movement).

- Einschränkungen im Hinblick auf bestimmte Branchen, Produkte und Themen:

  Bei Organisationen, die in bestimmten Geschäftsbereichen, zum Beispiel im Zusammenhang mit Medizin, Arzneimitteln, Recht oder Waffen, tätig sind, kann es zu einer Verschlechterung der Dienstqualität kommen.

## <a name="what-data-does-analysis-collect-and-how-is-it-used"></a>Welche Daten sammelt die Analyse und wie werden sie verwendet?

Die Analyseunterstützung erfasst die Mindestdaten, die Business Central zum Anbieten des Dienstes benötigt. Microsoft verwendet Ihre Geschäftsdaten, einschließlich der Texte, die Sie an Copilot senden, nicht, um die zugrundeliegenden Modelle für die Nutzung durch andere zu trainieren. Weitere Informationen finden Sie unter [Dynamics 365-Bedingungen für Azure OpenAI-basierte Features](https://go.microsoft.com/fwlink/?linkid=2236010).

Es sammelt darüber hinaus Daten aus dem Feedback, das Benutzende über die Symbole „Gefällt mir“ (Daumen hoch) oder „Gefällt mir nicht“ (Daumen runter) auf der **Copilot**-Seite der Analyseunterstützung geben können. Die Daten sind anonym und umfassen die Auswahl zwischen „Gefällt mir“ oder „Gefällt mir nicht“, gegebenenfalls den Grund für die Ablehnung und das Copilot-Feature, auf das sich das Feedback bezieht.

## <a name="see-also"></a>Siehe auch

[Daten mit Copilot analysieren (Vorschauversion)](analysis-assist.md)
