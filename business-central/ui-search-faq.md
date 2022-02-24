---
title: Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“ | Microsoft Docs
description: Dieser Artikel bietet Antworten zu den häufig von unseren Partner und Debitoren über „Wie möchten Sie weiter verfahren“ gestellten Fragen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 02/12/2020
ms.author: bholtorf
ms.openlocfilehash: 67dd65491710206245a2ff83dce3d3eb94484770
ms.sourcegitcommit: c78df3aefb3e2ed8c28e5ac8340d56ab787212e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071910"
---
# <a name="tell-me-faq"></a>Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“
In diesem Thema werden Fragen beantwortet, die unsere erfahrenen Benutzer häufig zu der Funktion "Wie möchten Sie weiter verfahren" stellen.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Werden alle Aktionen meiner aktuellen Seite von „Wie möchten Sie weiter verfahren“ abgedeckt?
Nein. Aktionen in Zeilen, z. B. der insgesamt, Verkaufszeilen-Teil der FactBoxes werden in „Wie möchten Sie weiter verfahren“ nicht angezeigt.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Werden die Ergebnisse in „Wie möchten Sie weiter verfahren“ nach Berechtigungen gefiltert?
Wenn der Benutzer nicht über AccessByPermissions verfügt, werden keine Aktionen angezeigt. Allerdings werden Seiten und Berichte in den Ergebnissen angezeigt. Der Benutzer benötigt jedoch die Berechtigungen, auf sie zuzugreifen. Es wird eine Meldung angezeigt, wenn der Benutzer, nicht über die Berechtigungen zum Anzeigen des Objekts verfügt.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Zeigt „Wie möchten Sie weiter verfahren“ Inhalt von meinen Anpassungen oder installierten Drittanbietererweiterungen an?
Aktionen, Seiten und Berichte, die aus Erweiterungen stammen, werden von „Wie möchten Sie weiter verfahren“ erkannt, angepasste Hilfedokumente allerdings nicht. Technische Informationen darüber, wie benutzerdefinierte Seiten und Berichte feststellbar gemacht werden, finden Sie unter [Hinzufügen von Seiten und Berichten zur Suche](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Worin unterschiedet sich dies von der vorherigen Funktion, die als Seitensuche bekannt war?
Die Seitensuche wurde zu „Wie möchten Sie weiter verfahren“ weiterentwickelt, damit Sie schneller arbeiten können. Die Seitensuche konnte Ihnen nur bei der Navigation in Seiten oder Berichten helfen. Auf technischer Ebene basiert „Wie möchten Sie weiter verfahren“ nicht mehr auf dem vorherigen MenuSuite-Konzept.

### <a name="i-use-on-premises-d365fin-does-that-include-tell-me"></a>Ich verwende [!INCLUDE[d365fin](includes/d365fin_md.md)] lokal. Schließt das „Wie möchten Sie weiter verfahren“ ein?
Sie können „Wie möchten Sie weiter verfahren“ mit dem lokalen Webclient verwenden, um nach Aktionen, Seiten und Berichten zu suchen, aber nicht nach Dokumentation oder Apps und Beratungsdiensten auf AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Ist „Wie möchten Sie weiter verfahren“ für alle Formularfaktoren verfügbar?
„Wie möchten Sie weiter verfahren“ ist nur im Webclient oder der Windows-Desktop-App verfügbar.

### <a name="are-the-documentation-results-available-in-any-language"></a>Sind die Dokumentationsergebnisse in jeder Sprache verfügbar?
Die Hilfeartikelanzeige werden in der Sprache angezeigt, die Sie in **Meine Einstellungen** angegeben haben, sofern die Hilfe in diese Sprache verfügbar ist.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Warum sehe ich kein Lesezeichensymbol für meine Suchergebnisse?
Das Lesezeichensymbol wird im Benachrichtigungsfenster nicht angezeigt, wenn die Personalisierung für eine Benutzerrolle deaktiviert ist.


## <a name="see-also"></a>Siehe auch  
[Speichern und personalisieren Sie Listenansichten](ui-views.md)  
[Suche nach Seiten und Informationen mit Tell Me](ui-search.md)  
[Suche nach Seiten mit dem Rollen-Explorer](ui-role-explorer.md)  
[Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter](ui-bookmarks.md)
