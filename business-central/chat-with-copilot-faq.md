---
title: Häufig gestellte Fragen zum Chat mit Copilot
description: Dieser Artikel beantwortet einige häufige Fragen zum Chat mit Copilot in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Häufig gestellte Fragen zum Chat mit Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Dieser Artikel beantwortet einige häufige Fragen zum Chaten mit Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Antworten auf Fragen zu KI und zum Chat finden Sie unter [Häufig gestellte Fragen zur verantwortungsvollen KI für den Chat mit Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Können Administrierende einzelnen Benutzenden den Zugriff auf den Chat erteilen oder verweigern?

Nein, es gibt für den Chat keine Berechtigung bzw. keinen Berechtigungssatz. Wenn der Chat auf der Seite [Copilot- und KI-Funktionen](enable-ai.md) aktiviert ist, haben alle Benutzenden in einer Umgebung Zugriff auf den Chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Ist der Chat auf Tablets, Smartphones oder anderen Formfaktoren verfügbar?

Nein, der Chatbereich ist nur auf dem [!INCLUDE[web_client](includes/web_client.md)]-Web-Client verfügbar.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Ich verwende Business Central nicht auf Englisch. Welche Möglichkeiten habe ich?

Derzeit ist der Chat nur auf Englisch verfügbar. Sie können Ihre Benutzersprache unter [Meine Einstellungen](ui-change-basic-settings.md#language) auf Englisch umstellen.

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Welche Business Central-Version brauche ich, um den Chat nutzen zu können?

Der Chat ist in der öffentlichen Vorschau ab Version 24.0 (2024, Veröffentlichungszyklus 1) verfügbar.

## <a name="does-chat-work-with-my-customizations"></a>Funktioniert der Chat mit meinen Anpassungen?

Das hängt von der Art der Frage ab, die Sie Copilot stellen. Beispiel:

- Wenn Sie Fragen stellen, um Datensätze zu finden, kann Copilot Datensätze in Ihren benutzerdefinierten Tabellen finden, die anhand benutzerdefinierter Felder identifiziert werden.
- Wenn Sie nach einer Erklärung oder Anleitung fragen, hat Copilot keinen Zugriff auf Informationen zu Ihren Anpassungen oder die Dokumentation Ihrer Add-Ons.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Copilot scheint den Datensatz oder die Seite, nach der ich gefragt habe, nie zu öffnen. Was mache ich falsch?

Wenn Sie Copilot auffordern, nach Datensätzen in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen, werden alle gefundenen Datensätze als auswählbare Kacheln oder Links im Chatbereich angezeigt. In der Vorschauversion navigiert Copilot nicht automatisch zu einer Seite.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Ich bekomme von Copilot unterschiedliche Antworten auf die gleiche Frage. Ist das ein Fehler?

Copilot antwortet möglicherweise manchmal unterschiedlich. Die Antworten sind nicht unbedingt identisch.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Wann sollte ich für Chatnachrichten die Kopierfunktion verwenden?

Mit der Schaltfläche „Kopieren“ können Sie eine frühere Nachricht aus Ihrer Unterhaltung mit Copilot kopieren, sie in das Eingabefeld einfügen, um die Nachricht an Copilot erneut oder in einer Abwandlung auszuprobieren.

## <a name="how-do-i-customize-or-extend-chat"></a>Wie kann ich den Chat anpassen oder erweitern?

In der Vorschauversion können der Chatbereich und die Antworten von Copilot überhaupt nicht durch Anpassung, Add-Ins oder Personalisierung geändert werden.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Findet Copilot Daten in anderen Unternehmen oder Umgebungen?

Copilot sucht nur nach Datensätzen in dem Unternehmen, bei dem Sie aktuell angemeldet sind,&mdash; auch wenn Ihre Organisation mehrere Umgebungen oder Unternehmen verwendet, um Daten zu trennen.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Der Copilot-Chatbereich wird nicht angezeigt. Was kann ich tun?

Überprüfen Sie, ob Ihre Benutzersprache unter „Meine Einstellungen“ auf Englisch eingestellt ist und ob Ihre Umgebungsversion 24.0 oder höher ist. Stellen Sie auf der Seite „Copilot und KI-Funktionen“ sicher, dass Ihre Administrierenden die Zustimmung zur Datenverwendung über geografische Grenzen hinweg sowie den Chat aktiviert haben. Stellen Sie sicher, dass Ihre Umgebungslokalisierung nicht Kanada ist.

Wenn die Funktion „Chat mit Copilot“ immer noch nicht angezeigt wird, besteht die Möglichkeit, dass Microsoft diese Funktion in Ihrer Region noch einführt. Copilot wird im April 2024 zunächst für US-Kunden und dann im Laufe der Wochen auch in anderen Ländern/Regionen eingeführt.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Warum zeigt Copilot im Chat-Bereich nur drei Datensätze an?

Wenn Sie Copilot auffordern, Datensätze abzurufen, bestimmt die Art und Weise, wie Sie die Frage formulieren, wie Copilot Seiten identifiziert und Filter anwendet, um das Gesuchte zu finden. Um die Antworten kompakt und prägnant zu halten, werden im Chat-Bereich maximal drei Datensatzkacheln angezeigt, selbst wenn Copilot eine größere Anzahl relevanter Datensätze findet.

## <a name="copilot-returns-incorrect-answers-to-totals-and-other-calculations"></a>Copilot gibt falsche Antworten auf Summen und andere Berechnungen zurück

In der Vorschau kann Chat mit Copilot Datensätze suchen, Konzepte erklären und Sie durch die Erledigung von Aufgaben in Business Central führen. Andere Anwendungsfälle werden nicht unterstützt, wie etwa das Addieren eines Felds über mehrere Datensätze hinweg oder das Berechnen des durchschnittlichen Monatsbetrags. Wir hoffen, Copilot in Zukunft um grundlegende Mathematikkenntnisse erweitern zu können.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kann ich meine Eingabeaufforderungen per Sprache statt per Eingabe eingeben?

Sie können mit Copilot chatten, indem Sie zum Sprechen die Spracherkennung verwenden, anstatt Ihre Wörter in den Chat-Bereich einzugeben. Die Spracherkennung nutzt die Online-Spracherkennung und ist unter Windows verfügbar. Um die Sprache zu verwenden, aktivieren Sie das Chat-Nachrichtenfeld, verwenden Sie dann die Tastenkombination  <kbd>Windows</kbd>+<kbd>H</kbd>  und beginnen Sie zu sprechen. Weitere Informationen finden Sie unter [Verwenden der Spracherkennung, um auf Ihrem PC zu sprechen, anstatt zu tippen](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Nächste Schritte

[Chat mit Copilot (Vorschauversion)](chat-with-copilot.md)
