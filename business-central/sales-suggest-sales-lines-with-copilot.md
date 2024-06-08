---
title: Verkaufszeilen mit Copilot vorschlagen
description: 'Erfahren Sie, wie Sie Verkaufszeile in Verkaufsaufträgen mit Copilot vorschlagen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# <a name="suggest-lines-on-sales-documents-with-copilot-preview"></a>Zeilen in Verkaufsbelegen mit Copilot vorschlagen (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In diesem Artikel wird erläutert, wie Sie Verkaufsbelege schneller erstellen, indem Sie Copilot die Artikel vorschlagen lassen, die den Zeilen in den Verkaufsbelegen für Ihre Debitoren hinzugefügt werden sollen.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-sales-line-suggestions-with-copilot"></a>Infos zu Verkaufszeilenvorschlägen mit Copilot

Vorschläge für Verkaufszeilen mit Copilot können bei der Erstellung von Zeilen in Verkaufsdokumenten wie Verkaufsangeboten, Bestellungen und Rechnungen auf der Grundlage strukturierter Eingaben oder natürlicher Sprache hilfreich sein. Bei der Funktion handelt es sich nicht um einen Allzweck-Chat, sondern um ein hochspezifisches und integriertes Erlebnis, das Sie für Verkaufsdokumente nutzen können. Die Funktion bietet zwei unterschiedliche Fähigkeiten, mit denen Sie Daten zu einzelnen Produkten oder gesamten Dokumenten finden können.

* Produkte finden

  Informationen, die Produkte beschreiben, werden an mehreren Stellen in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert. Beispielsweise werden Artikelnummern und Beschreibungen in der Tabelle **Artikel**, mehrere Barcodes in der Tabelle **Artikelreferenz** und Produkteigenschaften in der Tabelle **Artikelattribute** gespeichert. Während Sie möglicherweise eine Eingabeaufforderung für *Rotes Fahrrad* eingeben, könnte das tatsächliche Produkt *Cube* sein, wobei *Fahrrad* eine Produktkategorie und *Rot* ein Attribut ist.

* Dokumente nach Referenz suchen

  Oft wird eine frühere Bestellung wiederholt oder zumindest als Ausgangspunkt verwendet. Allerdings kann es schwierig sein, in einem Stapel von Bestellungen die richtige Reihenfolge zu finden. Möglicherweise erinnern Sie sich an die Bestellnummer. Dabei kann es sich um eine vom Unternehmen zugewiesene Nummer oder eine von einem Debitoren erhaltene Referenznummer handeln. Die Möglichkeit, Eingabeaufforderungen wie *Benötige letzte Rechnung vom April* zu verwenden, soll Ihnen helfen, schneller eine Bestellung zu finden.

## <a name="prerequisites"></a>Voraussetzungen

* Verkaufszeilenvorschläge mit Copilot werden von einem Administrierenden eingeschaltet und aktiviert. Weitere Informationen zum Aktivieren von KI-Funktionen finden Sie unter [Copilot- und KI-Funktionen konfigurieren](enable-ai.md).
* Sie sind mit der Erstellung von Verkaufsaufträgen vertraut.

## <a name="geographic-availability"></a>Geografische Verfügbarkeit

Die folgende Tabelle zeigt die geografischen Microsoft Azure-Gebiete, in denen das Feature verfügbar ist.

|Azure-Region der Umgebung  |Geografische Region des Azure OpenAI Diensts   |Zum Entsperren von Copilot ist eine Administratoraktion erforderlich  |
|---------|---------|---------|
|Deutschland (Norden, Westen-Mitte)     | Schweden oder Schweiz        |  Ja       |
|Norwegen (Osten, Westen)     | Schweden oder Schweiz        | Ja     |
|Singapur     |         |         |
|Südafrika (Norden, Westen)     |   Vereinigte Staaten      |   Ja      |
|Schweiz (Norden, Westen)     |  Schweden oder Schweiz       |    Ja     |
|Vereinigte Arabische Emirate (Norden, Westen)     |    Vereinigte Staaten     |   Ja     |
|Vereinigte Staaten (Mitte, Osten, Norden-Mitte, Süden-Mitte, Westen)     |   Vereinigte Staaten      |   Nein      |
|Europa (Westen, Norden)     |   Schweden oder Schweiz      |   Ja      |
|Asien Pazifik     |         |         |
|Australien (Südosten)     |   Vereinigte Staaten      |    Ja     |
|Südamerika     |         |         |
|Indien (Mitte, Süden)     |    Vereinigte Staaten     |   Ja      |
|Japan (Osten, Westen)     |    Vereinigte Staaten     |    Ja     |
|Frankreich (Mitte, Süden)     |    Schweden oder Schweiz     |    Ja     |
|Korea (Mitte, Süden)     |    Vereinigte Staaten     |    Ja     |

## <a name="examples-of-prompts"></a>Beispiele für Eingabeaufforderungen

Mit Copilot können Sie Verkaufszeilen vorschlagen, die eine große Bandbreite an Eingaben verarbeiten. Dieser Abschnitt bietet einige Beispiele für Eingabeaufforderungen für verschiedene Szenarien, die wir getestet haben.

### <a name="sample-inquiry-to-repeat-the-past-document"></a>Beispielabfrage zum Wiederholen des früheren Beleges

Eingabeaufforderung: *Benötige alle Produkte aus Rechnung 103031*

### <a name="during-phone-call-user-quickly-types-list-of-required-products-and-quantities-not-always-accurate-enough-or-using-internal-product-names"></a>Während des Telefonats gibt der Benutzende schnell eine Liste der benötigten Produkte und Mengen ein, was nicht immer genau genug ist oder es werden interne Produktnamen verwendet

Eingabeaufforderung: *2 rote Kinderfahrrääder*

Beachten Sie, dass die Eingabeaufforderung auch bei mehreren Tippfehlern funktioniert.

### <a name="a-user-copies-an-inquiry-from-an-inbound-communication-and-pastes-it-to-the-sales-lines-suggestions-page"></a>Ein Benutzender kopiert eine Anfrage aus einer eingehenden Kommunikation und fügt sie auf der Seite „Vorschläge für Verkaufszeilen“ ein

Eingabeaufforderung: *Hallo, ich möchte Zubehör für meinen XXXX-Laptop kaufen, beispielsweise eine kabellose Maus, eine Tastaturabdeckung und eine Laptoptasche. Ich frage mich, ob Sie Empfehlungen oder Vorschläge für diese Artikel haben. Haben Sie Sonderangebote oder Rabatte für treue Kunden wie mich? Mit freundlichen Grüßen, M*

Beachten Sie, dass der XXXX-Laptop nicht in die Suche einbezogen wird.

## <a name="suggest-lines-on-a-sales-document"></a>Zeilen in einem Verkaufsbeleg vorschlagen

Dieser Prozess beschreibt, wie Zeilen in einem Verkaufsauftrag vorgeschlagen werden. Die Schritte sind für Verkaufsangebote und Rechnungen identisch.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Verkaufsauftrag** ein und wählen Sie dann den zugehörigen Link.
1. Öffnen Sie den Verkaufsauftrag.
1. Wählen Sie im Inforegister **Zeilen** die Option **Zeilenvorschläge abrufen** aus.
1. Geben Sie im Fenster **Zeilen mit Copilot vorschlagen** Ihre Eingabeaufforderung ein oder wählen Sie eine aus den Eingabeaufforderungsanleitungen aus.

## <a name="review-save-discard-or-regenerate-suggestions"></a>Vorschläge prüfen, speichern, verwerfen oder neu generieren

Nachdem Copilot die Elemente vorgeschlagen hat, die den Zeilen hinzugefügt werden sollen, überprüfen Sie die Vorschläge und entscheiden Sie, ob sie Ihren Wünschen entsprechen:

* Um eine einzelne vorgeschlagene Zeile zu verwerfen, wählen Sie sie in der Liste und dann die Aktion **Zeile löschen** aus.
* Um alle vorgeschlagenen Zeilen zu verwerfen und das Copilot-Fenster zu schließen, wählen Sie die Schaltfläche „Verwerfen“ (Papierkorb) neben der Schaltfläche **Behalten** aus.
* Um die im Copilot-Fenster angezeigten Zeilen zu übertragen, wählen Sie **Behalten** aus. 

Es gibt ein Feld **Zuverlässigkeit**, in dem die Werte **Hoch (80+)**, **Mittel (60-80)** und **Niedrig (60-)** angezeigt werden und das Sie auf Zeilen hinweist, die Ihrer Aufmerksamkeit bedürfen.

Dieser Schritt bestätigt, dass Sie die Zeilen in einen Verkaufsbeleg übertragen möchten. Sie können dort auch die übertragenen Zeilen löschen, bearbeiten oder den gesamten Beleg löschen.

## <a name="see-also"></a>Siehe auch

[AQ für Verkaufszeilenvorschläge mit Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Copilot- und KI-Funktionen konfigurieren](enable-ai.md)
