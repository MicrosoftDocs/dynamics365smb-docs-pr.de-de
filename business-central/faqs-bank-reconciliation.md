---
title: Häufig gestellte Fragen zur Unterstützung bei Bankkontoabstimmung mit Copilot (Vorschauversion)
description: 'Diese häufig gestellten Fragen bietet Informationen über die KI-Technologie, die zur Abstimmung von Bankkonten und Kontoauszügen in Business Central verwendet wird. Dazu gehören auch wichtige Überlegungen und Details dazu, wie KI verwendet wird, wie sie getestet und bewertet wurde und welche spezifischen Einschränkungen bestehen.'
ms.date: 03/27/2024
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

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Häufig gestellte Fragen zur Unterstützung bei Bankkontoabstimmung mit Copilot (Vorschauversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen der Microsoft Copilot-Unterstützung bei Bankkontoabstimmung in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Was ist die Unterstützung bei Bankkontoabstimmung?

Die Bankkontoabstimmung ist eine häufige Buchhaltungsaufgabe, bei der Organisationen ihre Kontoauszüge überprüfen, um Transaktionen zu identifizieren, die in [!INCLUDE[prod_short](includes/prod_short.md)] registriert werden sollten. Diese Aufgabe wird beispielsweise verwendet, um regelmäßige Bankgebühren oder kleine Mitarbeiterausgaben zu ermitteln.

Die Bankabstimmung ist in der Regel ein mehrstufiger Prozess. Zunächst werden die Bankauszüge in [!INCLUDE[prod_short](includes/prod_short.md)] importiert. Als Nächstes werden Transaktionen mit Sachbucheinträgen abgeglichen. Abschließend werden neue Hauptbucheinträge gebucht, um etwaige Resttransaktionen widerzuspiegeln, die Ihren Hauptbüchern bisher nicht bekannt waren.

Copilot reduziert in [!INCLUDE[prod_short](includes/prod_short.md)] den manuellen Aufwand, indem mehr Transaktionen zugeordnet werden und Sachkonten vorgeschlagen werden, auf die Sie buchen können.

## <a name="what-are-the-capabilities-of-bank-reconciliation-assist"></a>Welche Funktionen bietet die Unterstützung bei Bankkontoabstimmung?

Copilot bietet KI-gestützte Unterstützung bei zwei unterschiedlichen Aufgaben:

- Verbesserte Zuordnung von Transaktionen mit Sachbucheinträgen

    [!INCLUDE[prod_short](includes/prod_short.md)] bietet automatisierte Regeln, die viele Banktransaktionen automatisch Sachbucheinträgen zuordnen. Diese Regeln sind jedoch unflexibel und führen häufig zu vielen nicht übereinstimmenden Transaktionen, die jeweils eine manuelle Prüfung und einen manuellen Vergleich erfordern. Copilot nutzt KI-Technologie, um diese nicht zugeordneten Transaktionen zu überprüfen und anhand der Daten, Beträge und Beschreibungen weitere Übereinstimmungen zu identifizieren. Wenn ein Debitor beispielsweise mehrere Rechnungen als Abschlag bezahlt hat, gleicht Copilot die einzelne Kontoauszugspositionen mit den Sachbucheinträgen für die Rechnung ab.

- Vorgeschlagene Sachkonten

    Für verbleibende Banktransaktionen, die keinem Sachbucheintrag zugeordnet werden können, verwendet Copilot KI-Technologie zum Vergleich der Transaktionsbeschreibung mit Sachkontonamen und schlägt dann das wahrscheinlichste Sachkonto vor, auf das gebucht werden soll. Wenn nicht zugeordnete Transaktionen beispielsweise die Meldung *Tanken 24* aufweisen, könnte Copilot vorschlagen, dass Sie sie auf das Konto *Beförderung* buchen.

Copilot stellt keine Verbindung zu Ihrer Bank her, um Transaktionen abzurufen oder zu senden. Diese Aufgabe liegt vollständig in Ihrer Kontrolle. Sie ist eine Voraussetzung, um die Unterstützung von Copilot in Anspruch nehmen zu können, unabhängig davon, ob die Transaktionen [!INCLUDE[prod_short](includes/prod_short.md)] über eine digitale Bankverbindung hinzugefügt, aus einer Kontoauszugsdatei importiert oder manuell eingegeben werden.

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Wozu dient die Unterstützung bei Bankkontoabstimmung?

Die Unterstützung bei der Bankkontoabstimmung soll die Genauigkeit von Sachkonten verbessern, indem Debitoren neue Transaktionen, die sie in [!INCLUDE[prod_short](includes/prod_short.md)] berücksichtigen sollten, leichter identifizieren können. Dies dient nicht der Betrugserkennung oder der Feststellung, ob Kunden pünktlich bezahlt haben.

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Wie wurde die Unterstützung bei Bankkontoabstimmung bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

Die Unterstützung bei der Bankkontoabstimmung wurde anhand von Kombinationen aus synthetischen Banktransaktionsdaten und ähnlichen Sachkonten und Sachkonteneinträgen getestet, die die typischen Variationen und Datengrenzwerte für jedes Feld und in verschiedenen Sprachen abdecken. Testdaten beziehen sich sowohl auf die typische Nutzung als auch die Nutzung durch böswillige Akteure. Die Leistung wurde im Vergleich zur manuellen Abstimmung derselben Daten gemessen.

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-these-limitations-when-they-use-the-system"></a>Welche Einschränkungen gelten für die Unterstützung bei Bankkontoabstimmung? Wie können Benutzer die Auswirkungen dieser Einschränkungen minimieren, wenn sie das System nutzen?

Die Unterstützung bei Bankkontenabstimmung funktioniert am besten, wenn die Namen der Sachkonten, die Beschreibungen der Sachkonten und die Beschreibungen der Banktransaktionen in derselben Sprache vorliegen. Gemischte Sprachen bzw. gemischte Sprachen für Transaktionsbeschreibungen führen häufig zu weniger Übereinstimmungen und Vorschlägen.

Die beste Leistung vorgeschlagener Sachkonten wird in einer der unterstützten Sprachen erzielt (eine Liste der Sprachen finden Sie im nächsten Abschnitt). In anderen Sprachen werden den Benutzern möglicherweise weniger Transaktionsübereinstimmungen und weniger Vorschläge für Sachkonten angezeigt.

## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>In welchen Regionen und Sprachen ist Unterstützung bei der Bankkontoabstimmung verfügbar?

- Verfügbare geografische Regionen

  Die Unterstützung bei der Bankkontoabstimmung ist in allen unterstützten [Ländern/Regionen von Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) verfügbar. Für Kundenumgebungen in Ländern/Regionen, in denen der Azure OpenAI-Dienst nicht bereitgestellt wird, müssen Administratoren zunächst der grenzüberschreitenden Übermittlung ihrer Daten zustimmen, damit [!INCLUDE [prod_short](includes/prod_short.md)] eine Verbindung zum Azure OpenAI-Dienst hergestellt werden kann. Erfahren Sie mehr unter [Copilot-Datenverschiebung über geografische Regionen hinweg](ai-copilot-data-movement.md).

- Verfügbare Sprachen

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Weitere Informationen zu Sprachen finden Sie in der vorherigen Frage zu Einschränkungen.

## <a name="what-is-expected-of-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Was wird von Systembenutzern erwartet, wenn sie die Unterstützung bei der Bankkontoabstimmung betreiben?

### <a name="during-bank-account-reconciliation"></a>Während der Bankkontoabstimmung

KI-gestützte Zuordnungen und Vorschläge können manchmal falsch oder unvollständig sein. Benutzer der Unterstützung bei der Bankkontoabstimmung müssen die Genauigkeit der von Copilot bereitgestellten Zuordnungen und Vorschläge überprüfen, bevor sie sich entscheiden, sie zu behalten. Die Zuordnungen und Vorschläge von Copilot werden erst dann in der [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank gespeichert, wenn Sie die Schaltfläche **Behalten** auswählen und das Copilot-Fenster schließen. Sie können alle Zuordnungen oder Vorschläge bearbeiten und korrigieren, bevor Sie sich entscheiden, sie zu behalten.

### <a name="after-bank-account-reconciliation-is-completed"></a>Nachdem die Bankkontoabstimmung abgeschlossen wurde

Wir empfehlen, dass Benutzer auch nach dem Schließen des Copilot-Fensters die Genauigkeit überprüfen und etwaige Unstimmigkeiten korrigieren. Dieser Prozess sollte die folgenden Aktivitäten umfassen:

- Sehen Sie sich den Abstimmungstestbericht an.
- Stellen Sie sicher, dass Ihre Organisation über die entsprechenden Überprüfungs- und Auditprozesse verfügt.
- Öffnen Sie alle veröffentlichten Abstimmungen erneut, indem Sie die Funktion **Rückgängig** verwenden.
- Korrigieren Sie fehlerhafte Buchungen, indem Sie eine Rückbuchung der Einträge durchführen.

## <a name="what-is-expected-of-administrators-and-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Was wird von Administratoren und Systembenutzern erwartet, wenn sie die Unterstützung bei der Bankkontoabstimmung verwenden?

Systembenutzer wie Buchhalter, Kassenverwalter oder andere Personen, die an der Unternehmensbuchhaltung mitwirken, sollten immer die Genauigkeit der von Copilot bereitgestellten Zuordnungen und Vorschläge überprüfen, bevor sie sich dazu entscheiden, diese zu behalten. Nach der Abstimmung mit Copilot empfehlen wir, dass diese Benutzer den Abstimmungstestbericht durchgehen, um die Genauigkeit zu überprüfen und etwaige Unstimmigkeiten zu identifizieren.

Administrierende sollten sicherstellen, dass die entsprechenden Benutzer aus der Buchhaltung Zugriff auf diese Funktion haben.

## <a name="is-copilot-the-only-means-of-completing-bank-account-reconciliation"></a>Ist Copilot die einzige Möglichkeit, die Bankkontoabstimmung abzuschließen?

Anz. Die Verwendung von Copilot ist optional. [!INCLUDE[prod_short](includes/prod_short.md)] bietet herkömmliche, nicht KI-gestützte Wege zum Importieren von Kontoauszügen, zum Ausführen voreingestellter Zuordnungsregeln und zum manuellen Anwenden von Zuordnungen und Verbuchen auf die entsprechenden Sachkonten. Sowohl der traditionelle Ansatz als auch Copilot können in einer Organisation gleichzeitig verwendet werden.

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Wie gebe ich Feedback zu KI-generierten Inhalten?

Jedes Mal, wenn Copilot Zuordnungen oder Vorschläge bereitstellt, können Sie Microsoft mithilfe der Steuerelemente „Gefällt mir“ (Daumen nach oben) und „Gefällt mir nicht“ (Daumen nach unten) direkt im Copilot-Fenster Feedback geben. Ihr Feedback bleibt anonym und wir verwenden diese Daten, um die Qualität dieses Dienstes zu verbessern.

## <a name="see-also"></a>Siehe auch

[Bankkontoabstimmung mit Copilot (Vorschauversion)](bank-reconciliation-with-copilot.md)
