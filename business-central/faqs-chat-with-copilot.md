---
title: Häufig gestellte Fragen zur verantwortungsvollen KI für den Chat mit Copilot (Vorschauversion)
description: 'Diese häufig gestellten Fragen bietet Informationen zu der in Business Central für den Chat mit Copilot verwendeten KI-Technologie. Dazu gehören auch wichtige Überlegungen und Details dazu, wie KI verwendet wird, wie sie getestet und bewertet wurde und welche spezifischen Einschränkungen bestehen.'
ms.date: 03/18/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# <a name="responsible-ai-faq-for-chat-with-copilot-preview"></a>Häufig gestellte Fragen zur verantwortungsvollen KI für den Chat mit Copilot (Vorschauversion)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen des Chats mit Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie an allgemeinen Fragen zur Verwendung des Features interessiert sind, gehen Sie zu [Häufig gestellte Fragen zum Chat mit Copilot](chat-with-copilot-faq.md).

## <a name="what-is-chat-with-copilot"></a>Was ist der Chat mit Copilot?

Microsoft Copilot ist der KI-gestützte Assistent, der dabei hilft, Kreativität freizusetzen, die Produktivität zu steigern und mühsame Aufgaben zu eliminieren. Sie können mit Copilot in Business Central chatten, um Antworten auf Fragen zu erhalten und Geschäftsdaten zu finden, indem Sie das Gesuchte in natürlicher Sprache ausdrücken.

Chat mit Copilot, auch Chat genannt, ist ein interaktives Feature, das Fragen beantwortet und Geschäftsdaten findet, die sich auf [!INCLUDE[prod_short](includes/prod_short.md)] beziehen, ohne dass Benutzende durch die Benutzeroberfläche oder die Produktdokumentation navigieren müssen. Der Copilot-Bereich ist überall im [!INCLUDE[prod_short](includes/prod_short.md)]-Client verfügbar.

Benutzende stellen Fragen in natürlicher Sprache, wie zum Beispiel „Wie lasse ich Waren von meinen Kreditoren direkt an meine Debitoren liefern?“ oder „Haben wir Bürostühle für unter 600 $ auf Lager?“ Copilot gibt daraufhin Antworten in natürlicher Sprache. Je nach den Fragen können die Antworten nur Text, Links zu Datensätzen oder Seiten in [!INCLUDE[prod_short](includes/prod_short.md)] und Links zu [!INCLUDE[prod_short](includes/prod_short.md)]-Hilfeartikel auf Microsoft Learn enthalten.

## <a name="what-are-capabilities-of-chat-with-copilot"></a>Welche Funktionen bietet Chat mit Copilot?

Sie können mit Copilot chatten, um Antworten auf die folgenden Arten von Fragen zu erhalten:

### <a name="explain-and-guide"></a>Erklärungen und Anleitungen

Benutzende können Copilot bitten, ein bestimmtes Konzept zu erklären, das mit [!INCLUDE[prod_short](includes/prod_short.md)] zu tun hat, z. B. was Dimensionen sind, oder eine Anleitung zum Erledigen einer Aufgabe zu geben, z. B. zum Buchen eines Verkaufsauftrags. Copilot durchsucht die offizielle [!INCLUDE[prod_short](includes/prod_short.md)]-Dokumentation von Microsoft und bietet eine auf der Dokumentation basierende Antwort.

- Copilot nutzt das Wissen auf Microsoft Learn (keine umfassende Websuche), um nur die Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-Dokumentation auf Microsoft Learn semantisch zu durchsuchen.

- Copilot ergreift keine Maßnahmen, erstellt keine neuen Daten und ändert keine Konfiguration. Er fasst einfach alle Absätze zusammen, die er auf Microsoft Learn findet und die zur Frage oder zum Prompt im Chat passen.

### <a name="find-business-data-and-related-pages"></a>Geschäftsdaten und zugehörige Seiten finden

Benutzende können Copilot bitten, Seiten nach Namen zu suchen oder Datensätze basierend auf ihren Feldern und Einschränkungen abzurufen. Wenn Copilot eine Übereinstimmung findet, antwortet er mit einem Link zum entsprechenden Datensatz oder zur Seite, den der Benutzende dann auswählen und öffnen kann.

- Copilot wandelt die Eingabe in natürlicher Sprache in eine Abfrage um, die aus einer Tabellensuche, Sortierung und Filterkriterien besteht.

  Die Funktion nutzt die native Datensuche von [!INCLUDE[prod_short](includes/prod_short.md)], um passende Daten aus Tabellen innerhalb der Unternehmensdatenbank zu finden. Aus Sicherheitsgründen und zur Einhaltung von Vorschriften wird die Suche unter der Identität des Benutzenden ausgeführt. Die Suche erfolgt nicht außerhalb der [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank.

- Copilot ergreift keine Maßnahmen, erstellt keine neuen Daten und ändert keine Konfiguration. Er fasst nur die von der nativen Datensuche von [!INCLUDE[prod_short](includes/prod_short.md)] erhaltenen Aufzeichnungen zusammen. 

## <a name="what-is-the-intended-use-of-chat-with-copilot"></a>Für welche Nutzung ist der Chat mit Copilot vorgesehen?

Der Chat ist für den Einsatz in Unternehmen konzipiert und beantwortet Fragen, die mit [!INCLUDE[prod_short](includes/prod_short.md)] und den darin enthaltenen Geschäftsdaten zusammenhängen. Mithilfe des Features können Benutzende häufige Aufgaben erledigen, wie zum Beispiel nach Datensätzen suchen und Anweisungen erhalten, wobei die Benutzenden ihr Anliegen in ihren eigenen Worten ausdrücken, was die Arbeit mit [!INCLUDE[prod_short](includes/prod_short.md)] einfacher und benutzerfreundlicher macht.

## <a name="how-was-chat-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Wie wurde Chat mit Copilot bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

- Das Feature wurde umfangreichen Tests unterzogen, bei denen Copilot zahlreiche englischsprachige Texte zu einem breiten Themenspektrum und in verschiedenen Schreibstilen vorgelegt wurden. Die Ergebnisse wurden auf Genauigkeit, Relevanz und Sicherheit bewertet.
- Das Feature basiert auf dem Standard für verantwortungsbewusste KI von Microsoft. [Erfahren Sie mehr über verantwortungsbewusste KI von Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Wie überwacht Microsoft die Qualität der generierten Inhalte?

Microsoft verfügt über verschiedene Systeme, um sicherzustellen, dass die von Copilot generierten Inhalte von höchster Qualität sind, Missbrauch zu erkennen und die Sicherheit unserer Kundschaft und ihrer Daten zu gewährleisten.

Benutzende haben die Möglichkeit, zu jeder Copilot-Antwort Feedback zu geben und ungenaue oder unangemessene Inhalte zu melden, um Microsoft bei der Verbesserung dieses Features zu unterstützen. 

- Sie geben Feedback, indem Sie das Symbol „Gefällt mir“ (Daumen hoch) oder „Gefällt mir nicht“ (Daumen runter) auf dem **Copilot**-Bereich in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.
- Wir analysieren und nutzen das Feedback der Benutzenden zu dem Feature, um die Antworten zu verbessern.
- Wenn Sie auf unangemessen generierte Inhalte stoßen, melden Sie diese Microsoft mithilfe dieses Feedbackformulars: [Missbrauch melden](https://go.microsoft.com/fwlink/?linkid=2249810).
- Microsoft kann die Copilot-gesteuerten Features für ausgewählte Kundschaft deaktivieren, wenn ein Missbrauch der Funktionalität festgestellt wird.

## <a name="what-are-the-limitations-of-chat-with-copilot-how-can-users-minimize-the-impact-of-the-chat-with-copilot-limitations-when-using-the-system"></a>Welche Einschränkungen gelten für den Chat mit Copilot? Wie können Benutzende die Auswirkungen der Einschränkungen des Chats mit Copilot bei der Nutzung des Systems minimieren?

- Allgemeine Einschränkungen von KI

  KI-Systeme sind wertvolle Werkzeuge, aber sie sind nichtdeterministisch. Die Inhalte, die sie generieren, sind möglicherweise nicht ganz korrekt. Daher müssen Sie unbedingt Ihr eigenes Urteilsvermögen einsetzen, um die Antworten von Copilot zu überprüfen und zu bestätigen, bevor Sie Entscheidungen treffen, die sich auf Interessengruppen wie Debitoren und Partner auswirken könnten. Copilot fügt bei den meisten Antworten auch Zitate oder Links zu Referenzen hinzu, mit denen Sie schnell überprüfen können, ob Copilot die richtige Antwort gefunden hat. Wenn Sie beispielsweise gefragt werden, wie eine Aufgabe ausgeführt werden soll, fügt Copilot Links zum Quellartikel hinzu. Wenn Copilot aufgefordert wurde, einen Datensatz anhand bestimmter Kriterien zu finden, fügt er Links hinzu, die die Listenseite beschreiben, die es als Gesprächsthema identifiziert hat, sowie alle Filter oder Sortierungen, die er angewendet hat, um zu der Antwort zu gelangen.

- Sprachliche Einschränkungen

  - Der Chat wird nur in Englisch und nur für die folgenden Gebietsschemas unterstützt: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Wenn die Anzeigesprache in [!INCLUDE[prod_short](includes/prod_short.md)] nicht zu diesen Gebietsschemas gehört, ist der Chat nicht verfügbar.

  - Unter den folgenden Bedingungen kann die Qualität der Antworten schlechter sein:
    - Das Sprachgebietsschema ist nicht en-US.
    - Die Spracheinstellung des Benutzenden in [!INCLUDE[prod_short](includes/prod_short.md)] weicht von der primären Sprache der Daten in der [!INCLUDE[prod_short](includes/prod_short.md)] Datenbank ab.

- Spezifische Branchen-, Produkt- und Themeneinschränkungen

   Der Chat verfügt über integrierte Sicherheitsmechanismen, welche die unerwünschte Generierung schädlicher Inhalte wie sexuell expliziter Inhalte oder Aufstachelung zu Gewalt verhindern. Manchmal ist Kundschaft in Branchen tätig, verkauft Produkte und Dienstleistungen oder arbeitet mit Prozessen, bei denen es natürliche Überschneidungen mit Themen gibt, die in einem anderen Zusammenhang als unangemessen angesehen werden könnten, oder sie arbeiten mit Daten, die eventuell diese Sicherheitsmaßnahmen auslösen. In diesen Fällen funktioniert der Chat möglicherweise nicht so gut wie sonst.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## <a name="what-data-does-chat-with-copilot-collect-and-how-is-it-used"></a>Welche Daten sammelt Chat with Copilot und wie werden sie verwendet?

Microsoft verwendet Ihre Geschäftsdaten, einschließlich der Texte, die Sie an Copilot senden, nicht, um die zugrundeliegenden KI-Modelle für die Nutzung durch andere zu trainieren. Die Unternehmensadministrierenden haben die volle Kontrolle über die Verwaltung dieser Daten, die Teil ihres Azure-Abonnements sind. Da Administrierende und andere Personen in Ihrem Unternehmen je nach den Vorgaben Ihres Arbeitgebers Zugriff auf diese Daten haben, sollten Sie niemals sensible Daten wie Kennwörter oder andere Geheimnisse eingeben.

## <a name="what-does-chat-with-copilot-offer-for-security"></a>Wie sorgt Chat mit Copilot für Sicherheit?

Der Chat ist so konzipiert, dass er sicher ist und unter der Identität des Benutzenden ausgeführt wird, alle Sicherheitsberechtigungen und anderen Einschränkungen übernimmt und niemals außerhalb der Plattformsicherheit von [!INCLUDE[prod_short](includes/prod_short.md)] arbeitet. Das bedeutet, dass Copilot nur auf Daten zugreifen kann, auf die auch der Benutzende Zugriff hat.

Bei Benutzenden mit SUPER-Berechtigung kann der Chat ungesicherte Daten leichter finden, die für andere Benutzende normalerweise schwerer zugänglich sind. Organisationen, die das Sicherheitsmodell von [!INCLUDE[prod_short](includes/prod_short.md)] nicht nutzen, um einzuschränken, auf welche Tabellen und Objekte die einzelnen Benutzenden oder Benutzerrollen Zugriff haben, setzen sich bei der Verwendung des Chats eventuell einem höheren Risiko aus. Daher empfehlen wir Ihrer Organisation entweder das Sicherheitsmodell von [!INCLUDE[prod_short](includes/prod_short.md)] zu implementieren oder den Chat zu deaktivieren.

## <a name="see-also"></a>Siehe auch

[Chat mit Copilot (Vorschauversion)](chat-with-copilot.md)

