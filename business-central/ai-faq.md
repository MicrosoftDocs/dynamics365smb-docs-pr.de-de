---
title: FAQ zu KI-gestützten Marketingtext für Artikel (Vorschauversion) mit Copilot
description: Erhalten Sie Antworten auf häufig gestellte Fragen zu den Funktionen zum Generieren von Text mit KI mit Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a>FAQ zu KI-gestützten Marketingtext für Artikel (Vorschauversion) mit Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

In diesem Artikel werden anhand von Fragen und Antworten wichtige Aspekte der KI-Technologie hinter Copilot und der von ihr generierten Texte erläutert.

## [Allgemein](#tab/general)

### <a name="what-is-copilot"></a>Was ist Copilot?

Copilot bietet KI-generierte Textvorschläge für Artikel in Business Central. Es ist für Benutzende gedacht, die Marketingtexte für Artikel schreiben, und soll sie bei der Erstellung ansprechender und überzeugender Inhalte unterstützen. Einige der wichtigsten Vorteile sind:

- Reduziert den Zeitaufwand für das Verfassen von Texten, was die Markteinführungszeit für Artikel, die in Onlineshops verkauft werden, verkürzen kann.
- Setzt Kreativität frei, sodass ansprechendere Produktbeschreibungen bereitgestellt werden können.
- Stärkt die Einheitlichkeit von Marketingmaterial für Produktlinien.

Benutzende sollten den von der KI generierten Text als Vorschlag betrachten, der sie auf Richtigkeit überprüfen und bearbeiten müssen, bevor er veröffentlicht wird.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a>Warum ist Copilot nicht für Marketingtext auf meinen Artikeln in Business Central verfügbar?

Die folgenden Voraussetzungen müssen erfüllt sein, damit Copilot zur Verfügung steht:

- Die Sprache, die Sie in Business Central verwenden, muss Englisch sein. Alle verfügbaren englischen Gebietsschemas funktionieren, wie z. B. Englisch (Vereinigte Staaten), Englisch (Vereinigtes Königreich) oder Englisch (Südafrika).

  Um die Sprache zu ändern, wählen Sie in der oberen rechten Ecke das **Einstellungen**-Symbol ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") > **Meine Einstellungen** > **Sprache** aus. Weitere Informationen finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md#language).
- Wenn Sie Business Central Online Version 22 oder eine spätere lokale Version (wenn Sie ein bestehender Kunde sind) oder eine Testversion verwenden.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->.

   Um die Version zu überprüfen, wählen Sie das Fragezeichen in der oberen rechten Ecke und dann **Hilfe und Support** aus. Suchen Sie unter **Problembehandlung** nach der Anwendungsversion. Informationen dazu, wie Sie die richtige Vorschauversion erhalten, finden Sie unter [Erste Schritte mit einer Business Central-Vorschauversion](ai-preview-getstarted.md).
- Das Feature **Erstellen Sie KI-unterstützte Produktbeschreibungen mit Copilot** muss aktiviert sein.

   Weitere Informationen finden Sie unter [Das Feature „Erstellen Sie KI-unterstützte Produktbeschreibungen mit Copilot“ aktivieren oder deaktivieren](enable-ai.md#enable-or-disable-the-create-ai-powered-product-descriptions-with-copilot-feature).
- Ein Administrator hat den Nutzungsbedingungen zugestimmt.

   Weitere Informationen finden Sie unter [Den Nutzungsbedingungen für die Vorschauversion und den Datenschutzbestimmungen für alle Benutzende zustimmen oder sie ablehnen](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises"></a>Steht Copilot in der lokalen Version von Business Central als Vorschauversion zur Verfügung?

Nein, es wird derzeit im lokalen Business Central nicht unterstützt.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a>Wie funktioniert Copilot, woher kommt der vorgeschlagene Text?

Copilot verwendet [den Azure OpenAI-Dienst von Microsoft](/azure/cognitive-services/openai/overview) , um auf leistungsstarke Sprachmodelle zuzugreifen, die natürliche Sprache analysieren und generieren. Diese Modelle wurden mit einer Vielzahl von Textdatensätzen trainiert. Infolgedessen kann Copilot basierend auf einer minimalen Menge an Eingabedaten, wie den Attributen, der Kategorie oder Beschreibung eines Artikels, vorgeschlagene, personalisierte Antworten auf Englisch generieren. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot"></a>Welche Qualität hat der von Copilot vorgeschlagene Text?

Da die zugrunde liegende Technologie von Copilot KI verwendet, die anhand einer Vielzahl von Quellen trainiert wurde, sind die generierten Inhalte nicht immer sachlich korrekt oder angemessen. Manche Vorschläge können sogar fragwürdige oder unangemessene Inhalte enthalten. Sie sind selbst dafür verantwortlich, generierte Vorschläge zu überprüfen und zu bearbeiten, um sicherzustellen, dass sie korrekt und angemessen sind.

Informationen zu unangemessenen Vorschlägen finden Sie unter [Was wird gegen missbräuchliche und schädliche Textvorschläge unternommen?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a>Wie kann ich die Vorschläge, die ich von Copilot erhalte, verbessern?

Sie können ein paar Dinge unternehmen, um die Vorschläge von Copilot optimal zu nutzen:

- Fügen Sie einem Artikel weitere Attribute hinzu, um die spezifischen Merkmale und Eigenschaften zu fördern, an denen Sie interessiert sind
- Passen Sie die Optionen für Tonfall und die Betonung der Qualität an Ihre persönlichen Präferenzen an.
- Die Beschreibung des Artikels verbessern
- Stellen Sie sicher, dass dem Artikel die am besten geeignete Kategorie zugewiesen ist.

Weitere Informationen finden Sie unter [Textvorschläge verbessern und anpassen](item-marketing-text.md#improve-and-tailor-text-suggestions).

### <a name="what-if-im-not-satisfied-with-the-generated-text"></a>Was ist, wenn ich mit dem generierten Text nicht zufrieden bin?

Um uns zu helfen, den Text zu verbessern, wählen Sie **Ist das ein guter Vorschlag?** auf der Seite **Mit Copilot erstellen** aus. Sie können darauf mit „Daumen hoch“ (gefällt mir) oder „Daumen runter“ (verbesserungswürdig) antworten.

![Zeigt eine Artikelkarte mit Bereich „Marketingtext“](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how"></a>Können Administratoren Copilot deaktivieren? Wenn ja, wie?

Business Central bietet Administratoren zwei Möglichkeiten, Copilot in der Vorschauversion zu deaktivieren:

- Lehnen Sie die Datenschutzhinweis von Azure OpenAI für alle Benutzende ab.

  oder

- Deaktivieren Sie das Feature **Erstellen Sie KI-unterstützte Produktbeschreibungen mit Copilot** auf der Seite **Funktionsverwaltung**.

Weitere Informationen finden Sie unter [KI-gestützte Marketingtext für Artikel (Vorschauversion) mit Copilot als Administrator konfigurieren](enable-ai.md).

## [Fairness](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english"></a>Funktioniert Copilot auch mit anderen Sprachen als Englisch?

Derzeit unterstützt Copilot nur Englisch. Wenn Benutzer mit dem System in anderen Sprachen als Englisch interagieren, werden eventuell falsche Antworten zurückgegeben.

## [Menschliche Aufsicht](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions"></a>Was wird gegen missbräuchliche und schädliche Textvorschläge unternommen?

Der Azure OpenAI-Dienst speichert Eingabeaufforderungen und Vervollständigungen des Dienstes, um sie auf die missbräuchliche Verwendung zu überwachen und die Qualität der Content-Management-Systeme von Azure OpenAI weiterzuentwickeln und zu verbessern. [Erfahren Sie mehr über unser Content Management und die Inhaltsfilterung](/azure/cognitive-services/openai/concepts/content-filter).

Befugte Microsoft-Mitarbeitende können auf Ihre Eingabeaufforderungs- und Erfassungsdaten zugreifen, die unsere automatisierten Systeme ausgelöst haben, um potenziellen Missbrauch zu untersuchen und zu überprüfen. Wenn Kunden den Azure OpenAI-Dienst in der Europäischen Union bereitgestellt haben, befinden sich die autorisierten Microsoft-Mitarbeitenden in der Europäischen Union. Diese Daten können zur Verbesserung unserer Content-Management-Systeme verwendet werden.Im Falle eines bestätigten Richtlinienverstoßes können wir Sie bitten, unverzüglich Maßnahmen zu ergreifen, um das Problem zu beheben und weiteren Missbrauch zu verhindern. Wenn das Problem nicht behoben wird, kann der Zugriff auf Azure OpenAI-Ressourcen ausgesetzt oder beendet werden.

Weitere Informationen finden Sie unter [Daten, Datenschutz und Sicherheit für den Azure OpenAI-Dienst](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process"></a>Kann ich die Protokollierung und die menschliche Überprüfung abwählen?

Im Rahmen der Bereitstellung der Azure OpenAI-Vorschauversionen verarbeitet und speichert Microsoft an den Dienst übermittelte Kundendaten sowie ausgegebene Inhalte zum Zwecke der (1) Überwachung und Verhinderung missbräuchlicher oder schädlicher Nutzungen oder Ausgaben des Diensts; und des (2) Entwickelns, Testens und Verbesserns von Fähigkeiten, die darauf ausgelegt sind, die missbräuchliche Nutzung und/oder schädliche Ausgaben des Dienstes zu verhindern.Befugtes Microsoft-Personal kann Daten überprüfen, die unsere automatisierten Systeme ausgelöst haben, um potenziellen Missbrauch zu untersuchen und zu überprüfen, und kann eine begrenzte Stichprobe von Begriffen entnehmen, die nicht von unseren automatisierten Systemen gekennzeichnet wurden, um sicherzustellen, dass die Systeme ordnungsgemäß funktionieren. Befugtes Microsoft-Personal kann auch auf diese Daten zugreifen und sie verwenden, um unsere Systeme zu verbessern, die missbräuchliche oder schädliche Nutzungen oder Ausgaben des Dienstes überwachen und verhindern.Mehr darüber erfahren Sie unter [Nutzungsbedingungen der Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)

## [Datenschutz](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Welche Daten erfasst die Funktion? Wie werden die Daten verwendet?

Die Funktion erfasst Ihre Antworten auf die Frage **Ist das ein guter Vorschlag?** auf der Seite **Mit Copilot erstellen** aus, die entweder mit „Daumen hoch“ (gefällt mir) oder „Daumen runter“ (verbesserungswürdig) beantwortet werden kann.

Wir verwenden diese Daten, um die Qualität der Funktion zu bewerten und zu verbessern. Weitere Informationen darüber, welche Daten erfasst werden, finden Sie in den [Nutzungsbedingungen der Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Zeigt eine Artikelkarte mit Bereich „Marketingtext“](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also"></a>Siehe auch

[Überblick über KI-gestützte Marketingtexte für Artikel mit Copilot](ai-overview.md)  
[KI-gestützten Marketingtext für Artikel mit Copilot als Administrator konfigurieren](enable-ai.md)  
[Mit Copilot Marketingtext für Artikel erstellen](item-marketing-text.md)  
[FAQ zu KI-gestützten Marketingtext für Artikel mit Copilot](ai-faq.md)  
