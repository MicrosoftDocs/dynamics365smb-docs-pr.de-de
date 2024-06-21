---
title: Chat mit Copilot (Vorschauversion)
description: 'Erfahren Sie, wie Sie den Chat mit Copilot verwenden, um in Business Central Daten zu finden und Hilfe zu erhalten.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/18/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Chat mit Copilot (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In diesem Artikel wird beschrieben, wie Sie mit Copilot chatten, um Antworten zu Ihren Unternehmensdaten und Unterstützung bei Aufgaben und Themen im Zusammenhang mit Business Central zu erhalten.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Über den Chat mit Copilot

Microsoft Copilot ist der KI-gestützte Assistent, der dabei hilft, Kreativität freizusetzen, die Produktivität zu steigern und mühsame Aufgaben zu eliminieren. Sie können mit Copilot in Business Central chatten, um Antworten auf Fragen zu erhalten und Geschäftsdaten zu finden, indem Sie das Gesuchte in natürlicher Sprache ausdrücken. Sie können den Chat verwenden, um:

- In Business Central nach Geschäftsdaten für das Unternehmen, für das Sie arbeiten, zu suchen. Verwenden Sie den Chat, um Daten zu Entitäten/Datensätzen im Zusammenhang mit Geschäftsprozessen wie Debitoren, Kreditoren, Verkaufsaufträgen, Artikeln und mehr zu suchen (und zu öffnen). Fordern Sie Copilot zum Beispiel auf: „Zeige mir den neuesten Verkaufsauftrag für Adatum.“
- Ein Konzept erklären oder Anleitungen zum Erledigen einer Aufgabe erhalten. Geben Sie zum Beispiel ein: „Hilf mir, die Dimension zu verstehen“ oder „Wie buche ich einen Verkaufsauftrag?“
- Den Zweck und die typische Verwendung einzelner Felder zu verstehen. Wenn Sie in einer QuickInfo für ein Feld die Option **Copilot fragen** auswählen, wird der Chat mit einer Erläuterungsaufforderung für den Feldnamen geöffnet und Copilot stellt Informationen dazu bereit. Copilot verlinkt auf die Artikel, auf die es verwiesen hat, sodass die Beschreibung leicht überprüft werden kann.

  Die von Copilot bereitgestellten Antworten basieren ausschließlich auf der offiziellen Dynamics 365 Business Central-Dokumentation, die auf Microsoft Learn unter [Dynamics 365 Business Central Dokumentation](/dynamics365/business-central/) verfügbar ist.

Durch den Chat mit Copilot entfällt die Notwendigkeit, durch die Benutzeroberfläche oder die Produkthilfe zu navigieren, wodurch Sie Zeit sparen und die Produktivität steigern können.
  
> [Video ansehen](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Voraussetzungen

- Die Funktion zum Chat mit Copilot ist aktiviert. Diese Aufgabe wird von Administrierenden ausgeführt. [Erfahren Sie mehr über das Konfigurieren von Copilot- und KI-Funktionen](enable-ai.md).
- Die Anzeigesprache in Business Central ist auf eines der folgenden englischen Gebietsschemas eingestellt: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Erfahren Sie mehr über das Ändern der Sprache](ui-change-basic-settings.md#language).
- Ihre Business Central-Umgebung befindet sich in einem beliebigen Land bzw. einer beliebigen Region außer Kanada (dieses Feature ist in Kanada noch nicht verfügbar).

## <a name="get-started-using-chat-with-copilot"></a>Erste Schritte mit dem Chat mit Copilot

1. Wählen Sie in der oberen rechten Ecke des Bildschirms das ![Zeigt das Symbol für den Chat mit Copilot](media/chat-copilot-icon.png) **Copilot**-Symbol ![Zeigt Legende Nummer 1](media/callout-number-1.svg).

   Der **Copilot**-Bereich wird, wie in der folgenden Abbildung dargestellt, auf der rechten Seite angezeigt:

    ![Zeigt das Symbol für den „Chat mit Copilot“-Bereich mit Legenden an](media/chat-with-copilot-pane.svg)

1. Geben Sie unten im Feld **Eine Frage stellen** ![Zeigt Legende Nummer 2](media/callout-number-2.svg) Ihre Frage ein und wählen Sie dann den Pfeil aus oder drücken Sie <kbd>Eingeben</kbd>, um eine Antwort zu erhalten.

   Bei dem von Ihnen eingegebenen Text, der im Hinblick auf Copilot häufig als *Prompt* bezeichnet wird, kann es sich um eine Frage, Aussage oder einen Befehl handeln.

   > [!TIP]
   > Copilot enthält einige Features, die Ihnen beim Verfassen von Fragen helfen können:
   > - Um mit der Formulierung einer Frage zu beginnen, wählen Sie eine der Anleitungen für Prompts – **Finden**, **Erklären** oder **Anleitung** – am oberen Rand des Fensters ![Zeigt Legende Nummer 3](media/callout-number-3.svg) oder das ![Zeigt das Symbol für Anleitung für Prompts](media/prompt-guide-icon.png) **Prompts anzeigen**-Symbol über dem Feld **Eine Frage stellen** aus ![Zeigt Legende Nummer 4](media/callout-number-4.svg). Anleitungen für Prompts sind vordefinierte kurze Sätze, die eine Frage oder einen Prompt einleiten. Sie sparen nicht nur Zeit, sondern dienen auch dazu, die Antworten von Copilot einer Antwortkategorie zuzuordnen. Sie helfen Ihnen auch dabei, die Fragen so zu formulieren, dass Sie so gute Antworten wie möglich erhalten.
   > - Wählen Sie die Prompt-Vorschläge über die Schaltfläche **Prompts anzeigen** ![Zeigt Legende Nummer 5](media/callout-number-5.svg), um automatisch eine vordefinierte Frage zu stellen und so einen Einblick in die Funktionsweise der Fragen und Antworten zu erhalten. Prompt-Vorschläge sind nur verfügbar, wenn Sie das CRONUS-Demounternehmen verwenden.

1. Die im Copilot-Bereich angezeigten Antworten überprüfen ![Zeigt die Legende Nummer 6](media/callout-number-6.svg).

   Je nach Ihrer Frage kann die Antwort Text, Links zu Datensätzen oder Seiten in Business Central sowie Links zu Business Central-Hilfeartikeln auf Microsoft Learn enthalten.

1. Stellen Sie eine weitere Frage, um die Antwort zu verfeinern.

   Der Chat merkt sich den Kontext, sodass Sie wichtige Punkte der ursprünglichen Frage nicht wiederholen müssen.

## <a name="clear-chat-to-start-over"></a>Chat löschen, um neu zu starten

Wenn Sie mit Copilot zu einem anderen Gesprächsthema wechseln möchten, wählen Sie das aus ![Zeigt das Symbol zum Löschen des Chats an](media/clear-chat-icon.png) Symbol **Eine neue Copilot-Chatsitzung starten** unten im Copilot-Bereich über dem Fragefeld aus. Diese Aktion löscht Ihre letzten Nachrichten aus dem Speicher von Copilot. Nach einer langen Unterhaltung mit vielen Nachrichten ist es oft hilfreich, von vorne zu beginnen. Dies kann Copilot dabei helfen, genauere Antworten zu geben.

Der Chat wird auch gelöscht, wenn Sie Business Central schließen oder sich abmelden.

## <a name="tips-for-better-questions"></a>Das Maximum aus Ihren Fragen herausholen

In diesem Abschnitt finden Sie Tipps, wie Sie die Antworten, die Sie von Copilot erhalten, verbessern können.

- Stellen Sie klare und konkrete Fragen.
- Seien Sie prägnant und vermeiden Sie lange oder mehrere Sätze.
- Stellen Sie immer nur eine Frage auf einmal. <!--Avoid asking about multiple questions in one message.-->
- Verwenden Sie eine natürliche Sprache und formulieren Sie Ihre Fragen freundlich und im Plauderton.
- Verwenden Sie Schlüsselwörter, Phrasen und Begriffe, von denen Sie wissen, dass sie in Business Central entweder in der App oder in der Dokumentation verwendet werden.
- Wenn die erste Antwort Ihre Fragen nicht vollständig beantwortet, stellen Sie Folgefragen oder formulieren Sie die letzte Frage um.
- Wenn Sie eine Frage zu einem anderen Thema als die bisherige Unterhaltung stellen möchten, löschen Sie die aktuelle Chatsitzung und beginnen Sie von vorn.

## <a name="example-prompts"></a>Beispiele für Prompts

Ihre Fragen an Copilot hängen natürlich von Ihrer Rolle, Ihren aktuellen Aufgabe, den Prozessen, die Ihre Organisation verwendet, und Ihrer Ausdrucksweise ab. Im Folgenden finden Sie Beispiele für verschiedene Möglichkeiten zum Stellen von Fragen im Chatbereich. Sie sollen Sie dazu inspirieren, eigene, an Ihre individuelle Situation angepasste Fragen zu verfassen.

Prompt: `Find the Item with Description 'ATHENS Desk'`

In diesem Beispiel geben Sie Copilot klare Anweisungen zum Auffinden eines einzelnen Datensatzes. Sie weisen beispielsweise darauf hin, dass der Datensatz in der Artikelliste zu finden ist. Sie geben an, dass das Feld „Beschreibung“ einen bestimmten Text enthalten muss, den Sie mit Anführungszeichen und korrekter Groß- und Kleinschreibung angegeben haben. Copilot antwortet normalerweise korrekt, wenn ihm ein paar präzise Hinweise gegeben werden. Sie können aber auch lockerere Formulierungen wie im nächsten Beispiel verwenden.

Prompt: `give me the latest invoice for adatum`

In diesem Beispiel bitten Sie Copilot, einen Datensatz zu suchen, die Frage ist jedoch weniger präzise und führt möglicherweise zu einer weniger genauen Antwort. Copilot versteht oder rät häufig richtig, dass es sich bei der gesuchten Rechnung nicht um eine Einkaufsrechnung, sondern um eine Verkaufsrechnung aus der Liste der gebuchten Verkaufsrechnungen handelt. Copilot müsste außerdem `adatum` der `Adatum Corporation` zuordnen, d. h. dem vollständigen und genauen Namen des mit der Rechnung verknüpften Debitores.

Prompt: `Show me customer ledger entries for Adatum from about three weeks ago`

In diesem Beispiel bitten Sie den Copiloten, ein häufiges Datumsproblem zu lösen, für das Sie normalerweise einen Kalender öffnen oder erweiterte Datumsbereichsfilter verwenden müssen. Copilot versteht in der Regel gängige Ausdrücke und wirtschaftliche Begriffe.

Prompt: `How does I save my filterrings to do them later?`

In diesem Beispiel bitten Sie Copilot um Anleitung zur Erledigung bestimmter Aufgaben in Business Central. Copilot versteht normalerweise, welche Absicht Sie mit der Frage verfolgen, selbst wenn sie einige Grammatikfehler, Rechtschreibfehler oder Abkürzungen enthält.

## <a name="provide-feedback-on-answers"></a>Feedback zu Antworten geben

Sie können die Antworten, die Sie von Copilot erhalten, bewerten, indem Sie für eine gute Bewertung die „Gefällt mir“-Schaltfläche (Daumen hoch) und für eine schlechte Bewertung die „Gefällt mir nicht“-Schaltfläche (Daumen runter) verwenden. Wenn Sie auf die Schaltfläche „Gefällt mir nicht“ klicken, können Sie einen Grund auswählen, z. B. „ungenau“, „unangemessen“ oder „Sonstiges“. Diese Informationen können helfen, Vorschläge zu verbessern.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
## <a name="see-also"></a>Siehe auch

[Probleme mit Copilot- und KI-Funktionen beheben](ai-copilot-troubleshooting.md)  
[Copilot- und KI-Funktionen konfigurieren](enable-ai.md)  
[Häufig gestellte Fragen zur verantwortungsvollen KI für den Chat mit Copilot](faqs-chat-with-copilot.md)  
[Hilferessourcen in Business Central](product-help-and-support.md)  
