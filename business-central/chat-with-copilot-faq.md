---
title: Häufig gestellte Fragen zum Chat mit Copilot
description: 'Erfahren Sie, wie Sie mit Copilot, einem virtuellen Assistenten, der Sie bei der Verwendung von Business Central unterstützt, chatten. Finden Sie Antworten auf allgemeine Fragen zu Chatfunktionen, -einstellungen und -einschränkungen.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Häufig gestellte Fragen zum Chat mit Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Dieser Artikel beantwortet einige häufige Fragen zum Chaten mit Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Antworten auf Fragen zu KI und zum Chat finden Sie unter [Häufig gestellte Fragen zur verantwortungsvollen KI für den Chat mit Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Können Administrierende einzelnen Benutzenden den Zugriff auf den Chat erteilen oder verweigern?

Nein, es gibt für den Chat keine Berechtigung bzw. keinen Berechtigungssatz. Wenn der Chat auf der Seite [Copilot- und KI-Funktionen](enable-ai.md) aktiviert ist, haben alle Benutzenden in einer Umgebung Zugriff auf den Chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Ist der Chat auf Tablets, Smartphones oder anderen Formfaktoren verfügbar?

Nein, der Chatbereich ist nur auf dem [!INCLUDE[web_client](includes/web_client.md)]-Web-Client verfügbar.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Ich verwende Business Central nicht auf Englisch. Welche Möglichkeiten habe ich?

Derzeit ist der Chat nur auf Englisch verfügbar. Sie können Ihre Benutzersprache unter [Meine Einstellungen](ui-change-basic-settings.md#language) auf Englisch umstellen.

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>Welche Business Central-Version benötige ich zum Chatten?

Der Chat ist in der öffentlichen Vorschau ab Version 24.0 (2024, Veröffentlichungszyklus 1) verfügbar.

## <a name="does-chat-work-with-my-customizations"></a>Funktioniert der Chat mit meinen Anpassungen?

Das hängt von der Art der Frage ab, die Sie Copilot stellen. Beispiel:

- Wenn Sie Fragen stellen, um Datensätze zu finden, können Datensätze in Ihren benutzerdefinierten Tabellen Datensätze gefunden werden, die benutzerdefinierte Felder verwenden.
- Wenn Sie Copilot nach einer Erklärung oder Anleitung fragen, hat dieser keinen Zugriff auf Informationen zu Ihren Anpassungen oder die Dokumentation Ihrer Add-Ons.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Wie öffne ich einen Datensatz oder eine Seite mit Chat?

Wenn Sie Copilot auffordern, nach Datensätzen in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen, werden alle gefundenen Datensätze als auswählbare Kacheln oder Links im Chatbereich angezeigt. In der Vorschauversion navigiert Copilot nicht automatisch zu einer Seite.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Warum bekomme ich von Copilot unterschiedliche Antworten auf dieselbe Frage?

Copilot antwortet möglicherweise manchmal unterschiedlich. Antworten sind nicht immer identisch.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>Wie verwende ich die die Kopierfunktion für Chatnachrichten?

Mit der Schaltfläche „Kopieren“ können Sie eine frühere Nachricht aus Ihrer Unterhaltung mit Copilot kopieren, sie in das Eingabefeld einfügen, um die Nachricht an Copilot erneut oder in einer Abwandlung auszuprobieren.

## <a name="can-i-customize-or-extend-chat"></a>Kann ich den Chat anpassen oder erweitern?

In der Vorschauversion können der Chatbereich und die Antworten von Copilot überhaupt nicht durch Anpassung, Add-Ins oder Personalisierung geändert werden.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>Sucht Copilot nach Daten in anderen Unternehmen oder Umgebungen?

Copilot sucht nur nach Datensätzen in dem Unternehmen, bei dem Sie aktuell angemeldet sind. Es erfolgt keine Datensuche in mehreren Umgebungen oder Unternehmen.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>Was kann ich tun, wenn der Chatbereich nicht angezeigt wird?

Überprüfen Sie, ob Ihre Benutzersprache unter **Meine Einstellungen** auf Englisch eingestellt ist und ob Ihre Umgebungsversion 24.0 oder höher ist. Stellen Sie auf der Seite „Copilot und KI-Funktionen“ sicher, dass der Administror die Zustimmung zur Datenverwendung über geografische Regionen hinweg sowie den Chat aktiviert hat. Stellen Sie außerdem sicher, dass die Lokalisierung Ihrer Umgebung nicht Kanada ist.

Wenn das Feature „Chat mit Copilot“ immer noch nicht angezeigt wird, hat Microsoft die Funktion in Ihrer Region vielleicht noch nicht fertig eingeführt. Copilot wird zunächst im April 2024 für Kundschaft in den USA eingeführt und über mehrere Wochen hinweg in anderen Lokalisierungen von Ländern/Regionen eingeführt.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Warum zeigt Copilot nur drei Datensätze im Chatbereich an?

Wenn Sie Copilot bitten, nach Datensätzen zu suchen, bestimmt die Art und Weise, wie Sie die Frage formulieren, wie Copilot Seiten identifiziert und Filter anwendet, um das Gesuchte zu finden. Um die Antworten kurz zu halten, werden im Chatbereich maximal drei Datensatzkacheln angezeigt, selbst wenn Copilot relevantere Datensätze findet.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Warum gibt Copilot falsche Antworten auf Berechnungen?

In der Vorschau kann Ihnen der Chat mit Copilot dabei helfen, Datensätze zu finden, Konzepte zu erklären und Sie bei der Erledigung von Aufgaben in Business Central anzuleiten. Andere Anwendungsfälle werden nicht unterstützt, wie etwa das Addieren eines Felds über mehrere Datensätze hinweg oder das Berechnen des durchschnittlichen Monatsbetrags. Wir hoffen, Copilot in Zukunft um grundlegende Mathematikkenntnisse erweitern zu können.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kann ich meine Eingabeaufforderungen per Sprache statt per Eingabe eingeben?

Sie können mit Copilot chatten, indem Sie die Spracheingabe zum Sprechen verwenden, anstatt Ihre Worte im Chatbereich einzugeben. Die Spracherkennung nutzt die Online-Spracherkennung und ist unter Windows verfügbar. Um die Stimme zu verwenden, aktivieren Sie das Chatnachrichtenfeld und verwenden Sie dann das Tastaturkürzel <kbd>Windows</kbd>+<kbd>H</kbd>, und beginnen Sie zu sprechen. Weitere Informationen finden Sie unter [Spracheingabe zum Sprechen statt manuelle Eingabe auf Ihrem PC verwenden](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Nächste Schritte

- [Chat mit Copilot (Vorschauversion)](chat-with-copilot.md)
