---
title: Häufig gestellte Fragen zur Unterstützung bei Bankkontoabstimmung (Vorschauversion) mit Copilot
description: 'Diese häufig gestellten Fragen bietet Informationen über die KI-Technologie, die zur Abstimmung von Bankkonten und Kontoauszügen in Business Central verwendet wird. Dazu gehören auch wichtige Überlegungen und Details dazu, wie KI verwendet wird, wie sie getestet und bewertet wurde und welche spezifischen Einschränkungen bestehen.'
ms.date: 11/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
---

# <a name="faq-for-bank-account-reconciliation-assist-preview-with-copilot"></a>Häufig gestellte Fragen zur Unterstützung bei Bankkontoabstimmung (Vorschauversion) mit Copilot

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen der Copilot-Unterstützung bei Bankkontoabstimmung in [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-bank-reconciliation-assist"></a>Was ist die Unterstützung bei Bankkontoabstimmung?

Die Bankkontoabstimmung ist eine häufige Buchhaltungsaufgabe, bei der Organisationen ihre Kontoauszüge überprüfen, um Transaktionen zu identifizieren, die in [!INCLUDE[prod_short](includes/prod_short.md)] registriert werden sollten. Diese Aufgabe wird beispielsweise verwendet, um regelmäßige Bankgebühren oder kleine Mitarbeiterausgaben zu ermitteln. Diese Aufgabe ist in der Regel ein mehrstufiger Prozess, der mit dem Importieren von Kontoauszügen in [!INCLUDE[prod_short](includes/prod_short.md)] beginnt. Anschließend werden Transaktionen mit Sachbucheinträgen abgeglichen und neue Sachbucheinträge gebucht, um alle verbleibenden Transaktionen widerzuspiegeln, die Ihren Sachbüchern zuvor nicht bekannt waren. Copilot reduziert in [!INCLUDE[prod_short](includes/prod_short.md)] den manuellen Aufwand, indem mehr Transaktionen zugeordnet werden und Sachbuchkonten vorgeschlagen werden, auf die Sie buchen können. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Welche Möglichkeiten bietet die Unterstützung bei Bankkontoabstimmung?

Copilot bietet KI-gestützte Unterstützung bei zwei unterschiedlichen Aufgaben: 

- Verbesserte Zuordnung von Transaktionen mit Sachbucheinträgen 

   [!INCLUDE[prod_short](includes/prod_short.md)] bietet automatisierte Regeln, die viele Banktransaktionen automatisch Sachbucheinträgen zuordnen. Diese Regeln sind jedoch unflexibel und führen häufig zu vielen nicht übereinstimmenden Transaktionen, die jeweils eine manuelle Prüfung und einen manuellen Vergleich erfordern. Copilot nutzt KI-Technologie, um verbleibende Transaktionen zu überprüfen und anhand der Daten, Beträge und Beschreibungen weitere Übereinstimmungen zu identifizieren. Wenn beispielsweise mehrere Rechnungen von einem Kunden als Abschlag bezahlt wurden, gleicht Copilot die einzelne Kontoauszugspositionen mit den Sachbucheinträgen für die Rechnung ab. 
 
- Vorgeschlagene Sachkonten 

   Für verbleibende Banktransaktionen, die keinem Sachbucheintrag zugeordnet werden können, verwendet Copilot KI-Technologie zum Vergleich der Transaktionsbeschreibung mit Sachkontonamen und schlägt das wahrscheinlichste Sachkonto vor, auf das gebucht werden soll. Beispielsweise könnte Copilot vorschlagen, Transaktion mit der Meldung „Tanken 24“ auf das Konto „Beförderung“ zu buchen. 

Copilot stellt keine Verbindung zu Ihrer Bank her, um Transaktionen abzurufen oder zu senden. Diese Aufgabe liegt vollständig in Ihrer Kontrolle und ist eine Voraussetzung, um die Unterstützung von Copilot in Anspruch nehmen zu können, unabhängig davon, ob diese Transaktionen [!INCLUDE[prod_short](includes/prod_short.md)] über eine digitale Bankverbindung hinzugefügt, aus einer Kontoauszugsdatei importiert oder manuell eingegeben wird. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Wozu dient die Unterstützung bei Bankkontoabstimmung?

Die Unterstützung bei Bankkontoabstimmung soll dabei helfen, neue Transaktionen zu identifizieren, die Kunden in [!INCLUDE[prod_short](includes/prod_short.md)] berücksichtigen sollten, um die Genauigkeit ihrer Bücher zu verbessern. Diese Aktivität dient nicht der Betrugserkennung oder der Feststellung, ob Kunden pünktlich bezahlt haben.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Wie wurde die Unterstützung bei Bankkontoabstimmung bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

Diese Funktionalität wurde anhand von Kombinationen aus synthetischen Banktransaktionsdaten und ähnlichen Sachkonten und Sachkonteneinträgen getestet, die die typischen Variationen und Datengrenzwerte für jedes Feld und in verschiedenen Sprachen abdecken. Testdaten beziehen sich sowohl auf die typische Nutzung als auch die Nutzung durch böswillige Akteure. Die Leistung wurde im Vergleich zur manuellen Abstimmung derselben Daten gemessen. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Welche Einschränkungen gelten für die Unterstützung bei Bankkontoabstimmung? Wie können Benutzende die Auswirkungen der Beschränkungen der Bankkontoabstimmung bei der Nutzung des Systems minimieren?

Die Unterstützung bei Bankkontenabstimmung funktioniert am besten, wenn die Namen der Sachkonten, die Beschreibungen der Sachkonten und die Beschreibungen der Banktransaktionen in derselben Sprache vorliegen. Gemischte Sprachen oder eine gemischte Sprache der Transaktionsbeschreibungen führen häufig zu weniger Übereinstimmungen und Vorschlägen. 

Vorgeschlagene Sachkonten erzielen die beste Leistung in englischer Sprache. Dieses Feature kann zwar in jeder der verfügbaren [!INCLUDE[prod_short](includes/prod_short.md)] Sprachen ausgeführt werden, Benutzenden werden jedoch möglicherweise weniger Transaktionsübereinstimmungen und weniger vorgeschlagene Sachkonten in anderen Sprachen angezeigt. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>In welchen Regionen und Sprachen ist Unterstützung bei der Bankkontoabstimmung verfügbar?

Diese Funktion ist für die Lokalisierung jedes Umgebungslandes bzw. jeder Umgebungsregion und in jeder Benutzersprache verfügbar. Für Kundenumgebungen in Ländern/Regionen, in denen der Azure OpenAI Dienst nicht bereitgestellt wird, müssen Administrierende zunächst der grenzüberschreitenden Übermittlung von Daten für [!INCLUDE[prod_short](includes/prod_short.md)] zustimmen, um eine Verbindung zum Azure OpenAI Dienst herzustellen und diese Funktion verfügbar zu machen. 

Weitere Informationen zur Sprache finden Sie in der vorherigen Frage zu Einschränkungen.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Was wird von Endbenutzenden erwartet, wenn sie die Unterstützung bei Bankkontoabstimmung betreiben?

### <a name="while-using-bank-account-reconciliation"></a>Während der Verwendung der Bankkontoabstimmung

KI-gestützte Zuordnungen und Vorschläge können manchmal falsch oder unvollständig sein. Benutzende der Unterstützung bei Bankkontoabstimmung müssen die Richtigkeit der von Copilot bereitgestellten Zuordnungen und Vorschläge überprüfen, bevor sie sich entscheiden, sie zu behalten. Die Zuordnungen und Vorschläge von Copilot werden erst dann in der [!INCLUDE[prod_short](includes/prod_short.md)] Datenbank gespeichert, wenn Sie auf die Schaltfläche „Behalten“ klicken und das Copilot-Fenster verlassen. Sie können alle Zuordnungen oder Vorschläge auch bearbeiten und korrigieren, bevor Sie sie behalten. 

### <a name="after-completing-bank-account-reconciliation"></a>Nach der Bankkontoabstimmung

Benutzende sollten auch nach dem Verlassen des Copilot-Fensters die Richtigkeit überprüfen und etwaige Unstimmigkeiten korrigieren, einschließlich der folgenden Aktivitäten: 

- Sehen Sie sich den Abstimmungstestbericht an. 
- Stellen Sie sicher, dass Ihre Organisation über die entsprechenden Überprüfungs- und Auditprozesse verfügt. 
- Öffnen Sie alle veröffentlichten Abstimmungen erneut, indem Sie die Funktion „Rückgängig“ verwenden. 
- Korrigieren Sie fehlerhafte Buchungen, indem Sie eine Rückbuchung der Einträge durchführen. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Was wird von Administrierenden und Endbenutzenden erwartet, wenn sie die Unterstützung bei Bankkontoabstimmung betreiben?

Endbenutzende wie Buchhalter, Kassenverwalter oder andere, die an der Unternehmensbuchhaltung mitwirken, sollten immer die Richtigkeit der von Copilot bereitgestellten Zuordnungen und Vorschläge überprüfen, bevor sie sich für die Beibehaltung entscheiden. Nach der Abstimmung mit Copilot empfehlen wir, den Abstimmungstestbericht durchzugehen, um die Richtigkeit zu überprüfen und etwaige Unstimmigkeiten zu identifizieren. 

Administrierende sollten sicherstellen, dass die entsprechenden Benutzenden aus der Buchhaltung Zugriff auf diese Funktion haben. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Ist Copilot die einzige Möglichkeit, die Bankkontoabstimmung abzuschließen?

Nein, die Nutzung von Copilot ist optional. [!INCLUDE[prod_short](includes/prod_short.md)] bietet herkömmliche, nicht KI-gestützte Wege zum Importieren von Kontoauszügen, zum Ausführen voreingestellter Zuordnungsregeln und zum manuellen Anwenden von Zuordnungen und Verbuchen auf die entsprechenden Sachkonten. Sowohl der traditionelle Ansatz als auch Copilot können innerhalb einer Organisation gleichzeitig verwendet werden. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Wie gebe ich Feedback zu KI-generierten Inhalten?

Jedes Mal, wenn Copilot Zuordnungen oder Vorschläge bereitstellt, können Sie Microsoft mithilfe der Steuerelemente „Gefällt mir“ und „Gefällt mir nicht“ direkt im Copilot-Fenster Feedback geben. Ihr Feedback bleibt anonym und wir verwenden diese Daten, um die Qualität dieses Dienstes zu verbessern.


## <a name="see-also"></a>Siehe auch

[Bankkontoabstimmung mit der Unterstützung bei Bankkontoabstimmung (Vorschauversion)](bank-reconciliation-with-copilot.md)
