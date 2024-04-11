---
title: Häufig gestellte Fragen zum Chat mit Copilot
description: Dieser Artikel beantwortet einige häufige Fragen zum Chat mit Copilot in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
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

Selbst wenn Ihre Organisation mehrere Umgebungen oder Unternehmen zur Trennung von Daten verwendet, sucht Copilot nur nach Datensätzen in dem Unternehmen, bei dem Sie aktuell angemeldet sind.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Der Copilot-Chatbereich wird nicht angezeigt. Was kann ich tun?

Überprüfen Sie, ob Ihre Benutzersprache unter „Meine Einstellungen“ auf Englisch eingestellt ist und ob Ihre Umgebungsversion 24.0 oder höher ist. Stellen Sie auf der Seite „Copilot und KI-Funktionen“ sicher, dass Ihre Administrierenden die Zustimmung zur Datenverwendung über geografische Grenzen hinweg sowie den Chat aktiviert haben. Stellen Sie sicher, dass die Lokalisierung Ihrer Umgebung nicht Kanada ist.

Wenn das Feature „Chat mit Copilot“ immer noch nicht angezeigt wird, hat Microsoft es in Ihrer Region vielleicht noch nicht fertig eingeführt. Copilot wird zunächst im April 2024 für Kundschaft in den USA eingeführt und über mehrere Wochen hinweg in anderen Länderlokalisierungen eingeführt.

## <a name="next-steps"></a>Nächste Schritte

[Chat mit Copilot (Vorschauversion)](chat-with-copilot.md)
