---
title: Häufig gestellte Fragen zur Zuordnung von E-Belegen zu Bestellungen
description: 'Die häufig gestellten Fragen zu verantwortungsvoller KI bieten Informationen über die in Business Central verwendete KI-Technologie sowie wichtige Überlegungen und Details dazu, wie die KI verwendet wird sowie wie sie getestet und bewertet wurde und welche spezifischen Einschränkungen gelten.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-mapping-e-documents-with-purchase-orders-using-copilot-preview"></a>Häufig gestellte Fragen zur Zuordnung von E-Belegen zu Bestellungen mit Copilot (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen des Features **Unterstützung beim Abgleich von E-Belegen** in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-e-documents-matching-assistance"></a>Was ist die Unterstützung beim Abgleich von E-Belegen?

Elektronische Belege (E-Belege) bilden die Grundlage moderner Geschäftstransaktionen. Sie umfassen wichtige Dokumente wie Rechnungen und Quittungen, die durch Lieferung und Wareneingang in beide Richtungen fließen. Sie können elektronische Rechnungen digital in einem strukturierten Format erstellen und übermitteln, das die automatisierte Rechnungsverarbeitung erleichtert. Allerdings kann die Bearbeitung eingehender digitaler Rechnungen für die Kreditorenbuchhaltung komplizierter sein.  

In kleinen und mittleren Unternehmen (KMU) spielt die Kreditorenbuchhaltung eine entscheidende Rolle bei der genauen Nachverfolgung der Kreditorenverpflichtungen. Ihre Hauptaufgabe besteht in der korrekten Erfassung eingehender Rechnungen. Es kann sehr aufwändig sein, hier die gewünschte Präzision zu erreichen, insbesondere wenn externe Rechnungen von Kreditoren mit vorhandenen Bestellungen abgeglichen werden. Diskrepanzen bei Codes, Beschreibungen und Maßeinheiten stellen häufig eine Herausforderung dar, da diese Elemente möglicherweise in verschiedenen Systemen und Unternehmen unterschiedlich sind. Außerdem können unerwartete Kosten, wie etwa Transportgebühren, als separate Posten auftauchen, die manuell abgeglichen werden müssen. Buchhaltungsfachkräfte müssen in den Belegen auch Rechnungsnummern und -daten angeben. Wichtig ist, dass die Beziehung zwischen Bestellungen und externen Rechnungen nicht immer eins zu eins ist. Möglicherweise erhalten Sie mehrere externe Rechnungen für dieselbe Bestellung.

Bisher konnte [!INCLUDE [prod_short](includes/prod_short.md)] neue Einkaufsrechnungen basierend auf eingegangenen elektronischen Rechnungen erstellen. Der manuelle Abgleich von Rechnungen mit bestehenden Bestellungen war jedoch ein zeitaufwändiger und fehleranfälliger Prozess.

Die **Unterstützung beim Abgleich von E-Belegen** nutzt generative KI, um diesen Prozess durch die Automatisierung der Analyse externer elektronischer Rechnungen zu rationalisieren. Mit diesem Feature kann die Buchhaltung Copilot auffordern, Positionen auf eingehenden elektronischen Rechnungen mit Positionen auf Bestellungen in [!INCLUDE [prod_short](includes/prod_short.md)] abzugleichen.

## <a name="what-are-capabilities-of-the-e-documents-matching-assistance"></a>Welche Funktionen bietet die Unterstützung beim Abgleich von E-Belegen?

Copilot bietet KI-gestützte Unterstützung beim Abgleich eingegangener digitaler Rechnungen mit bestehenden Bestellungen in [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot ordnet Positionen basierend auf Folgendem zu:

- Ähnlichkeit der Beschreibungen
- Maßeinheiten
- Zur Fakturierung verfügbare Mengen
- Beträge

Copilot identifiziert ähnliche Beschreibungen, wenn sie über die richtigen Maßeinheiten und Preise verfügen, kann aber auch in komplexeren Fällen Übereinstimmungen finden. Beispielsweise kann er erkennen, ob eine elektronische Rechnung zwei Positionen mit einer Variante desselben Artikels enthält, die Bestellung jedoch nur eine. [!INCLUDE [prod_short](includes/prod_short.md)] gleicht diese Positionen ab, solange die Beschreibungen ähnlich und die Preise identisch sind.

Copilot stellt keine Verbindung zu Ihrem E-Beleg-Endpunktdienst her, um digitale Gutscheine abzurufen oder zu senden. Diese Aufgabe unterliegt vollständig Ihrer Kontrolle und ist eine Voraussetzung für die Nutzung der Unterstützung durch Copilot. Dies gilt unabhängig davon, ob die digitalen Belege [!INCLUDE [prod_short](includes/prod_short.md)] über eine Verbindung mit einem Endpunktdienst hinzugefügt oder manuell eingegeben werden.  

## <a name="what-is-the-intended-use-of-the-e-documents-matching-assistance"></a>Wozu dient die Unterstützung beim Abgleich von E-Belegen?

Das Feature **Unterstützung beim Abgleich von E-Belegen** soll die Kreditorenbuchhaltung dabei zu unterstützen, bestehende Bestellungen mit eingehenden elektronischen Rechnungen abzugleichen. Bei einem Großteil dieser Aktivität geht es um das Abgleichen von Zeichenfolgen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet ein Feature, das einige dieser Aufgaben automatisiert, und große Sprachmodelle wurden als Möglichkeit identifiziert, dieses Feature zu ergänzen und den manuellen Aufwand weiter zu reduzieren.  

## <a name="how-was-e-documents-matching-assistance-evaluated-what-metrics-are-used-to-measure-performance"></a>Wie wurde die Unterstützung beim Abgleich von E-Belegen bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

Dieses Feature wurde mit Kombinationen der folgenden Informationen getestet:

- Externe Artikelbeschreibungen
- Maßeinheiten
- Mengen und Beträge
- Standardartikelbeschreibungen
- Verschiedene Sprachen
- Andere Parameter, welche die typischen Variationen und Datengrenzen für die einzelnen Feld abdecken 

Die Testdaten beziehen sich sowohl auf die typische Nutzung als auch die Nutzung durch böswillige Akteure. Die Leistung wurde im Vergleich zum manuellen Abgleich derselben Daten in elektronischen Rechnungen und Bestellungen gemessen.

## <a name="what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system"></a>Welche Einschränkungen gelten für die Unterstützung beim Abgleich von E-Belegen? Wie können Benutzende die Auswirkungen der Einschränkungen der Unterstützung beim Abgleich von E-Belegen bei der Nutzung des Systems minimieren?

Die **Unterstützung beim Abgleich von E-Belegen** funktioniert am besten, wenn externe (E-Rechnung) und interne ([!INCLUDE [prod_short](includes/prod_short.md)])Artikelbeschreibungen und Maßeinheiten in ein und derselben Sprache verfasst sind. Gemischte Sprachen oder eine gemischte Sprache der Artikelbeschreibungen führen häufig zu weniger Übereinstimmungen und Vorschlägen.  

Der vorgeschlagene Abgleich von Artikeln aus E-Rechnungen mit Artikeln in Bestellungen funktioniert in englischer Sprache am besten. Obwohl Sie dieses Feature in jeder Sprache verwenden können, die [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt, kann es sein, dass es in anderen Sprachen weniger Artikelübereinstimmungen findet.

## <a name="in-which-geographies-and-languages-is-e-documents-matching-assistance-available"></a>In welchen Regionen und Sprachen ist die Unterstützung beim Abgleich von E-Belegen verfügbar?

Diese Funktion ist für die Lokalisierung jedes Umgebungslandes bzw. jeder Umgebungsregion und in jeder Benutzersprache mit Ausnahme von Kanada verfügbar. Aufgrund der eingeschränkten Sprachenunterstützung steht das Feature kanadischen Debitoren zunächst nicht zur Verfügung, da es die gesetzlichen Vorgaben im Hinblick auf die Sprache nicht erfüllt. 

Für Kundenumgebungen in Ländern/Regionen, in denen der Azure OpenAI Dienst nicht bereitgestellt wird, steht diese Funktion nur zur Verfügung, wenn Administrierende zunächst der grenzüberschreitenden Übermittlung von Daten für [!INCLUDE [prod_short](includes/prod_short.md)] zustimmen, um eine Verbindung zum Azure OpenAI Dienst herzustellen.  

Weitere Informationen zur Sprache finden Sie unter [Welche Einschränkungen gelten für die Unterstützung beim Abgleich von E-Belegen? Wie können Benutzende die Auswirkungen der Einschränkungen der Unterstützung beim Abgleich von E-Belegen bei der Nutzung des Systems minimieren?](#what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system).   

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Welche betrieblichen Faktoren und Einstellungen lassen eine effektive und verantwortungsvolle Nutzung des Features zu?

Copilot ergänzt den Zuordnungsalgorithmus, den [!INCLUDE [prod_short](includes/prod_short.md)] bereits bereitstellt, und ordnet die Positionen zu, bei denen dies dem Algorithmus nicht gelungen ist.

### <a name="what-is-expected-of-end-users-while-using-e-documents-matching-assistance"></a>Was wird von Endbenutzenden erwartet, wenn sie die Unterstützung beim Abgleich von E-Belegen nutzen?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Nachdem Sie eingehende elektronische Rechnungen den Bestellungen zugeordnet haben, müssen Sie die Positionen in den Belegen zuordnen.

Auf der Seite **Bestellungszuordnung** werden alle Positionen aus beiden Belegen angezeigt. Hier können Sie die Zuordnung manuell vornehmen, was schwierig sein kann, wenn Sie es mit vielen Positionen zu tun haben.

Sie können die **Unterstützung beim Abgleich von E-Belegen** verwenden, um Positionen basierend auf den folgenden Kriterien zuzuordnen:

- Ähnlichkeit ihrer Beschreibungen
- Maßeinheiten
- Zur Fakturierung verfügbare Mengen
- Beträge

Die von Copilot vorgenommenen Abgleiche können falsch oder unvollständig sein. Sie sollten sie immer auf Richtigkeit überprüfen, bevor Sie sich entscheiden, sie zu behalten. Die von Copilot gelieferten Abgleiche und Vorschläge werden in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert, wenn Sie **Behalten** wählen und Copilot beenden. Sie können alle Zuordnungen oder Vorschläge bearbeiten und korrigieren, bevor Sie sich entscheiden, sie zu behalten. 

### <a name="what-is-expected-of-administrators-and-end-users-when-operating-e-documents-matching-assistance"></a>Was wird von Administrierenden und Endbenutzenden erwartet, wenn sie mit der Unterstützung beim Abgleich von E-Belegen arbeiten?

Endbenutzende, wie Mitarbeitende aus der Buchhaltung und andere, die E-Rechnungen erhalten, sollten immer die Richtigkeit der von Copilot bereitgestellten Abgleiche und Vorschläge überprüfen, bevor sie sich entscheiden, sie zu behalten. Wir empfehlen Ihnen, die Bestellpositionen zu überprüfen, um ihre Richtigkeit sicherzustellen und etwaige Unstimmigkeiten zu finden. Sie entscheiden, ob Sie die **Unterstützung beim Abgleich von E-Belegen** nutzen möchten. Auch wenn das Feature **Unterstützung beim Abgleich von E-Belegen** von den Administrierenden aktiviert wurde und verfügbar ist, können Sie sich trotzdem entscheiden, ob Sie es immer, manchmal oder nie verwenden möchten.  

Administrierende entscheiden, ob Copilot grundsätzlich in [!INCLUDE [prod_short](includes/prod_short.md)] verwendet werden soll. Wenn die Administrierenden Copilot aktivieren, sollten sie sicherstellen, dass die richtigen Zugriffsrechte gewähren.

> [HINWEIS!]
> - Wir unterstützen das Feature nicht in der lokalen Version von [!INCLUDE [prod_short](includes/prod_short.md)] oder in privaten Clouds.
> - Partner können dieses Feature nicht erweitern. Entwicklungsfachkräfte von Partnern können dieses Feature nicht ändern, ersetzen oder erweitern. 

## <a name="is-copilot-the-only-way-to-match-e-documents-to-purchase-orders"></a>Ist Copilot die einzige Möglichkeit, E-Belege mit Bestellungen abzugleichen?

Nein, ob Sie Copilot nutzen, bleibt Ihnen überlassen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet nicht auf KI basierende Möglichkeiten, Artikel aus erhaltenen elektronischen Rechnungen mit Artikeln in Bestellungen in [!INCLUDE [prod_short](includes/prod_short.md)] abzugleichen. Organisationen können auch beide Ansätze gleichzeitig verwenden.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Wie gebe ich Feedback zu KI-generierten Inhalten?

Jedes Mal, wenn Copilot Abgleiche oder Vorschläge bereitstellt, können Sie Microsoft mithilfe der Steuerelemente „Gefällt mir“ und „Gefällt mir nicht“ direkt im Copilot-Fenster Feedback geben. Ihr Feedback bleibt anonym und wir verwenden diese Daten, um die Qualität dieses Dienstes zu verbessern.  

## <a name="see-also"></a>Siehe auch

[Übersicht über E-Belege](finance-edocuments-overview.md)
[E-Belege mit Copilot Bestellzeilen zuordnen](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
