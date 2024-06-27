---
title: Häufig gestellte Fragen zum Vorschlagen von Verkaufszeilen mit Copilot
description: Diese häufig gestellten Fragen bietet Informationen zu der in Business Central verwendeten KI-Technologie.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# Häufig gestellte Fragen zu Verkaufszeilenvorschlägen mit Copilot (Vorschauversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Diese häufig gestellten Fragen (FAQ) beschreiben die KI-Auswirkungen des Features für Verkaufszeilenvorschläge in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Was sind Verkaufszeilenvorschlägen mit Copilot?

Vorschläge für Verkaufszeilen mit Copilot können bei der Erstellung von Zeilen in Verkaufsdokumenten wie Verkaufsangeboten, Bestellungen und Rechnungen auf der Grundlage strukturierter Eingaben oder natürlicher Sprache hilfreich sein. Bei der Funktion handelt es sich nicht um einen Allzweck-Chat, sondern um ein hochspezifisches und integriertes Erlebnis, das Sie für Verkaufsdokumente nutzen können. Die Funktion bietet zwei unterschiedliche Fähigkeiten, mit denen Sie Daten zu einzelnen Produkten oder gesamten Dokumenten finden können.

## Welche Möglichkeiten bieten Verkaufszeilenvorschläge mit Copilot?

* Produkte finden

  Informationen, die Produkte beschreiben, werden an mehreren Stellen in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert. Beispielsweise werden Artikelnummern und Beschreibungen in der Tabelle **Artikel**, mehrere Barcodes in der Tabelle **Artikelreferenz** und Produkteigenschaften in der Tabelle **Artikelattribute** gespeichert. Während Sie möglicherweise eine Eingabeaufforderung für *Rotes Fahrrad* eingeben, könnte das tatsächliche Produkt *Cube* sein, wobei *Fahrrad* eine Produktkategorie und *Rot* ein Attribut ist.

* Einen Beleg nach Referenz suchen

  Oft wird eine frühere Bestellung wiederholt oder zumindest als Ausgangspunkt verwendet. Allerdings kann es schwierig sein, in einem Stapel von Bestellungen die richtige Reihenfolge zu finden. Möglicherweise erinnern Sie sich an die Bestellnummer. Dabei kann es sich um eine vom Unternehmen zugewiesene Nummer oder eine von einem Debitoren erhaltene Referenznummer handeln. Die Möglichkeit, Eingabeaufforderungen wie *Benötige letzte Rechnung vom April* zu verwenden, soll Ihnen helfen, schneller eine Bestellung zu finden.

## Welchen Zweck haben Vorkaufszeilenvorschläge mit Copilot?

* Produkte finden

  Sollen auf Prompts von Benutzenden antworten, um Produkte basierend auf vagen, unvollständigen oder ungenauen Beschreibungen zu suchen.

  Da die durchschnittliche Anzahl der Artikel (Produkte/Services) für [!INCLUDE [prod_short](includes/prod_short.md)]-Debitoren bei 10.000 liegt, kann es ohne vorherige Erfahrung oder Wissen schwierig sein, die richtigen Artikel zu finden. Die Art und Weise, wie Daten in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert werden, macht die Sache nicht einfacher, da Sie auf den verschiedenen Seiten, auf denen Produktdaten gespeichert sind, mehrere Suchen oder Filterungen durchführen müssen.

  Copilot extrahiert die angeforderten Produkte und Mengen und identifiziert den Hauptsuchbegriff sowie die Attribute, sodass Sie Ihre Prompts schneller eingeben können. Anschließend führt Copilot eine erweiterte Suche in mehreren zusammengehörenden Tabellen durch, nutzt Synonyme, korrigiert Tippfehler und bewertet die Qualität der Suchausgabe.

* Einen Beleg nach Referenz suchen

  Dient zur Beantwortung von Anfragen von Benutzenden, um vorhandene Verkaufsbelege für einen bestimmten Debitor anhand teilweiser oder vager Informationen zu finden.

  In B2B-Umgebungen haben Mitarbeitende es oft mit wiederkehrenden Anfragen zu tun, und Auftragsverarbeitende werden vielleicht gebeten, einen alten Beleg erneut einzusetzen oder ihn zumindest als Ausgangspunkt zu verwenden. Es kann aus mehreren Gründen schwierig sein, solche Belege zu finden:

  - Im Laufe seines Lebenszyklus kann aus einem Verkaufsbeleg erst ein Angebot, dann ein Auftrag und schließlich eine gebuchte Rechnung oder Lieferung werden. Darüber hinaus können Belege archiviert werden.
  - Sie verfügen möglicherweise über eine genaue Kennung, können aber nicht sagen, wofür sie steht. Handelt es sich beispielsweise um die Auftragsnummer, die Rechnungsnummer oder eine externe Referenz?
  - Manchmal haben Sie ein Datum oder einen Zeitraum, aber keine Kennung für den Beleg.

  Um einen Quellbeleg manuell zu finden, müssen Sie mehrere Seiten öffnen und mehrmals suchen und filtern. Copilot kann dies jedoch in einer einzigen Abfrage in natürlicher Sprache vereinfachen, sodass Sie das Gesuchte in Ihrem eigenen Stil ausdrücken können. 

  * *Produkte aus Auftrag 103031 abrufen*
  * *Benötige Produkte der letzten Rechnung im August*

## Wie wurden die Verkaufszeilenvorschläge mit Copilot bewertet? Welche Metriken werden verwendet, um die Leistung zu messen?

Das Feature wurde umfangreichen Tests unterzogen, bei denen zahlreiche Prompts in amerikanischem Englisch eingesetzt wurden, die sowohl die übliche Verwendung als auch die Verwendung durch böswillige Akteure simulierten. Die Tests basierten auf den Demodaten von [!INCLUDE [prod_short](includes/prod_short.md)] und einem großen, gekennzeichneten Produktkatalog, der im Open-Source-Format verfügbar ist.

Dieses Feature basiert auf dem Standard für verantwortungsbewusste KI von Microsoft. [Erfahren Sie mehr über verantwortungsbewusste KI von Microsoft](https://aka.ms/RAI).

## Welche Einschränkungen gelten bei den Vorkaufszeilenvorschlägen mit Copilot? Wie können Benutzende die Auswirkungen der Einschränkungen der Vorkaufszeilenvorschläge mit Copilot bei der Nutzung des Systems eindämmen?

* Produkte finden
  
  Die Produktsuche funktioniert in englischer Sprache am besten. Obwohl Sie dieses Feature in allen Sprachen verwenden können, die [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt, ist die Artikelsuche in anderen Sprachen möglicherweise eventuell weniger genau.

Wenn sich Ihre Branche oder Domäne mit Themen überschneidet, die Microsoft als vertraulich betrachtet (z. B. Drogen, Gewalt, Erwachsenenunterhaltung usw.), kann es sein, dass Copilot seine Antworten auf neutrale, eingeschränkte Aussagen eingrenzt oder ungenaue Antworten gibt.

Verkaufszeilenvorschläge tragen nur in die Felder **Typ** wie beschrieben Angaben als **Artikel**, **Nr.** und **Menge** ein. Andere Felder, einschließlich **Maßeinheit**, **VK-Preis** und **Standort**, verwenden die aktuelle Logik und werden entweder basierend auf den Artikeleinstellungen oder übernommenen Werten aus dem Belegkopf ausgefüllt.

Der **Variantencode** wird derzeit nicht unterstützt. Wenn Sie beispielsweise ein Produkt in zwei verschiedenen Farben liefern können, findet Copilot das benötigte Produkt, lässt aber das Feld **Variantencode** leer. Sie müssen das Feld manuell ausfüllen.

Wie Sie Ihre Produkte benennen, kann sich auf die Ausgabe auswirken. Es kann zum Beispiel die Ausgabequalität beeinträchtigen, wenn Sie kryptische Abkürzungen anstelle benutzerfreundlicher Namen verwenden.

Die folgende Tabelle enthält die Tabellen und Felder auf, die Copilot für Produkte durchsucht.

|Tabelle  |Felder  |
|---------|---------|
|**Artikel**     |  * Nr.<br>* Beschreibung<br>* Beschreibung 2<br>* Suchbegriff<br>* GTIN<br>* Kreditorenartikelnummer       |
|**Artikelvariante**     | * Code<br>* Beschreibung<br>* Beschreibung 2          |
|**Artikelreferenz**     | * Referenznr.<br>* Beschreibung<br>* Beschreibung 2        |
|**Artikelattribute**     | * Name<br>* Wert        |
|**Artikelkategorie**     |  * Code<br>* Beschreibung<br>* Übergeordnete Kategorie – eine Ebene           |
|**Artikelübersetzung**     | * Sprache<br>* Beschreibung<br>* Beschreibung 2          |
|**Artikelbarcode**     |  * Code       |
|**Textbausteinzeile**     |  * Text      |

* Dokumente nach Referenz suchen

  Derzeit können Sie die Verkaufszeilenvorschläge von Verkaufsaufträgen, Rechnungen und Angeboten aus starten und die folgenden Belege durchsuchen:

  * Verkaufsaufträge
  * Angebote
  * Verkaufsrechnungen
  * Gebuchte Verkaufsrechnungen
  * Gebuchte Verkaufslieferungen

  Copilot durchsucht die folgenden Felder

  * Belegnummer
  * Externe Belegnr.
  * Ihre Referenz
  * Anfragenr.
  * Belegdatum
  * Verkauf an Deb.-Nr.

  Copilot gibt nicht alle Zeilen vom Typ „Artikel“ zurück. Es werden lediglich Artikelnummern, Variantencodes und Mengen übertragen. Mengen aus dem Quellbeleg werden in den **Verkaufseinheitencode** umgerechnet.

## In welchen Regionen und Sprachen sind die Verkaufszeilenvorschläge verfügbar?

- Verfügbare geografische Regionen

   Diese Copilot-Funktion ist in allen unterstützten [Ländern/Regionen von Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) verfügbar. Für Kundenumgebungen in Ländern/Regionen, in denen der Azure OpenAI-Dienst nicht bereitgestellt wird, müssen Administratoren jedoch zunächst der grenzüberschreitenden Übermittlung ihrer Daten zustimmen, damit [!INCLUDE [prod_short](includes/prod_short.md)] eine Verbindung zum Azure OpenAI-Dienst hergestellt werden kann. Erfahren Sie mehr unter [Copilot-Datenverschiebung über geografische Regionen hinweg](ai-copilot-data-movement.md).

- Verfügbare Sprachen

   [!INCLUDE[sales-lines-suggestions-language-support](includes/sales-lines-suggestions-language-support.md)]

## Welche betrieblichen Faktoren und Einstellungen lassen eine effektive und verantwortungsvolle Nutzung des Features zu?

KI-gestützte Vorschläge können manchmal falsch oder unvollständig sein. Sie sollten immer die Richtigkeit der Vorschläge von Copilot überprüfen, bevor Sie sich entscheiden, sie zu übernehmen. Die Vorschläge von Copilot werden erst dann in der [!INCLUDE [prod_short](includes/prod_short.md)] Datenbank gespeichert, wenn Sie auf die Schaltfläche **Behalten** gehen und das Copilot-Fenster schließen. Sie können alle Vorschläge bearbeiten und korrigieren, bevor Sie sie behalten oder nachdem Sie sie in einen Verkaufsbeleg eingefügt haben.

### Was wird von Administrierenden und Endbenutzenden erwartet, wenn sie die Verkaufszeilenvorschläge verwenden?

Jeder einzelne Benutzende entscheidet, ob er die **Verkaufszeilenvorschläge** verwendet oder nicht. Auch wenn das Feature von den Administrierenden aktiviert wurde und verfügbar ist, können Sie sich entscheiden, ob Sie es immer, manchmal oder nie verwenden möchten.  

Administrierende entscheiden, ob Copilot-Funktionen grundsätzlich in [!INCLUDE [prod_short](includes/prod_short.md)] verwendet werden sollen. Wenn die Administrierenden Copilot aktivieren, sollten sie sicherstellen, dass sie den entsprechenden Benutzenden Zugriff gewähren.

> [!NOTE]
> - Wir unterstützen dieses Feature nicht in der lokalen Version von [!INCLUDE [prod_short](includes/prod_short.md)] oder in der privaten Cloud.
> - Partner können dieses Feature nicht erweitern. Das bedeutet, dass Entwicklungsfachkräfte von Partnern es nicht ändern, ersetzen oder erweitern können.

## Ist Copilot das einzige Mittel zum Erstellen von Verkaufszeilen?  

Nein, die Nutzung von Copilot ist optional. [!INCLUDE [prod_short](includes/prod_short.md)] bietet auch Möglichkeiten zum Einfügen von Verkaufszeilen oder zum Kopieren von Belegen, die keine KI verwenden. Es können auch beide Ansätze gleichzeitig verwendet werden.  

## Wie gebe ich Feedback zu KI-generierten Inhalten?  

Jedes Mal, wenn Copilot Vorschläge bereitstellt, können Sie Microsoft mithilfe der Schaltflächen „Gefällt mir“ und „Gefällt mir nicht“ direkt im Copilot-Fenster Feedback geben. Ihr Feedback bleibt anonym und wir verwenden diese Daten, um die Qualität dieses Dienstes zu verbessern.  

## Siehe auch

[Zeilen in Verkaufsaufträgen mit Copilot vorschlagen](sales-suggest-sales-lines-with-copilot.md)  
[Copilot- und KI-Funktionen konfigurieren](enable-ai.md)  
[Häufig gestellte Fragen zur verantwortungsvollen KI für Dynamics 365 Business Central](responsible-ai-overview.md)  
