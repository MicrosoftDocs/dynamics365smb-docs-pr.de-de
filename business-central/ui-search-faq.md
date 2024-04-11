---
title: Häufig gestellte Fragen zu Tell Me
description: 'In diesem Artikel finden Sie Antworten auf Fragen, die unsere Partner und Kunden häufig zur „Wie möchten Sie weiter verfahren“-Funktion stellen.'
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 03/20/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“

Dieser Artikel beantwortet Fragen, die unsere fortgeschrittenen Benutzer häufig zu der Funktion „Wie möchten Sie weiter verfahren“ stellen.

## Werden alle Aktionen meiner aktuellen Seite von „Wie möchten Sie weiter verfahren“ abgedeckt?

Nein. Aktionen in Zeilen, z. B. der insgesamt, Verkaufszeilen-Teil der Infoboxen werden in „Wie möchten Sie weiter verfahren“ nicht angezeigt.

## Kann ich nach einem bestimmten Datensatz suchen?

Ja. Wenn Sie beispielsweise schnell einen Kundenauftrag finden möchten, geben Sie dessen Kennung ein und wählen Sie dann die Aktion **Unternehmensdaten durchsuchen** aus. Wenn Sie nur den Namen des Kunden kennen, geben Sie diesen ein. Tell Me ordnet die Ergebnisse nach Typ, sodass Sie die Bestellung in der Kategorie „Kundenaufträge“ finden können.

## Werden die Ergebnisse in „Wie möchten Sie weiter verfahren“ nach Berechtigungen gefiltert?

Wenn der Benutzer nicht über AccessByPermissions verfügt, werden keine Aktionen angezeigt. Allerdings werden Seiten und Berichte in den Ergebnissen angezeigt. Der Benutzer benötigt jedoch die Berechtigungen, auf sie zuzugreifen. Es wird eine Meldung angezeigt, wenn der Benutzer, nicht über die Berechtigungen zum Anzeigen des Objekts verfügt.

## Zeigt „Wie möchten Sie weiter verfahren“ Inhalt von meinen Anpassungen oder installierten Drittanbietererweiterungen an?

Aktionen, Seiten und Berichte, die aus Erweiterungen stammen, werden von „Wie möchten Sie weiter verfahren“ erkannt. Technische Informationen darüber, wie benutzerdefinierte Seiten und Berichte feststellbar gemacht werden, finden Sie unter [Hinzufügen von Seiten und Berichten zur Suche](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## Worin unterschiedet sich dies von der vorherigen Funktion, die als Seitensuche bekannt war?

Die Seitensuche wurde zu „Wie möchten Sie weiter verfahren“ weiterentwickelt, damit Sie schneller arbeiten können. Die Seitensuche konnte Ihnen nur bei der Navigation in Seiten oder Berichten helfen. Auf technischer Ebene basiert „Wie möchten Sie weiter verfahren“ nicht mehr auf dem vorherigen MenuSuite-Konzept.

## Ich verwende [!INCLUDE[prod_short](includes/prod_short.md)] lokal. Schließt das „Wie möchten Sie weiter verfahren“ ein?

Sie können „Wie möchten Sie weiter verfahren“ mit dem lokalen Webclient verwenden, um nach Aktionen, Seiten und Berichten zu suchen, aber nicht nach Apps und Beratungsdiensten auf AppSource.

## Ist „Wie möchten Sie weiter verfahren“ für alle Formularfaktoren verfügbar?

Ja. Es wurde im 2. Veröffentlichungszyklus von Business Central 2023 auf Smartphones und Tablets eingeführt. Im Veröffentlichungszyklus 2 2023 muss dies in der [Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management) mit dem Schalter **Feature: Nach Seiten und Daten in der mobilen App suchen** eingeschaltet werden. Im 1. Veröffentlichungszyklus 2024 und später ist es immer aktiviert.

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## Bietet „Wie möchten Sie weiter verfahren“ Hilfestellungen zum Verwendung von Seiten, Berichten und anderen Dingen?

Nein, Sie können diese Informationen jedoch ganz einfach über den Hilfebereich abrufen. Wählen Sie einfach die Aktion **Hilfe suchen** auf der Seite **Wie möchten Sie weiter verfahren** oder <kbd>STRG</kbd>+<kbd>F1</kbd> auf Ihrer Tastatur. Weitere Informationen zum Hilfebereich finden Sie unter [Hilfebereich](product-help-and-support.md#help-pane).

### Warum sehe ich kein Lesezeichensymbol für meine Suchergebnisse?

Das Lesezeichensymbol wird im Benachrichtigungsfenster nicht angezeigt, wenn die Personalisierung für eine Benutzerrolle deaktiviert ist.

## Siehe auch  

[Speichern und personalisieren Sie Listenansichten](ui-views.md)  
[Suche nach Seiten und Informationen mit Tell Me](ui-search.md)  
[Suche nach Seiten mit dem Rollen-Explorer](ui-role-explorer.md)  
[Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]