---
title: Informationen zum Suchen und Filtern in Business Central
description: Antworten auf häufig gestellte Fragen zu Suche und Filter.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 11/16/2020
ms.author: mikebc
ms.openlocfilehash: b993fd047db09b1dc412d9927168aa0233c057a6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756717"
---
# <a name="searching-and-filtering-faq"></a>Suchen und Filtern – FAQs
In diesem Artikel finden Sie Antworten auf allgemeine Fragen, die Sie möglicherweise über das Suchen und Filtern haben.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Gibt es einen Unterschied zwischen Suchen und Filtern?
Ja.
- Die Suche ist einfach und breit gefächert: sie enthält Datensätze, die den Suchtext im sichtbaren Bereich der Seite enthalten. Dabei wird die Groß-/Kleinschreibung beachtet.
- Filterung ist sehr flexibel und kann auf bestimmte Bereiche angewendet werden, einschließlich derjenigen, die nicht auf der Seite sichtbar sind: sie zeigt Datensätze mit genauen Treffern an, bei denen die Groß-/Kleinschreibung beachtet wird. Sie kann mit leistungsfähigen Suchsymbolen, -token und -formeln angepasst werden. Weitere Informationen zur Nutzung dieser Funktionen finden Sie unter [Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md).

## <a name="exactly-which-fields-are-matched-when-searching"></a>Welche Felder stimmen bei der Suche genau überein?
[!INCLUDE[prod_short](includes/prod_short.md)] wendet die Suchkriterien auf alle Felder an, die auf der Seite sichtbar sind. Wenn ein Feld ausgeblendet wurde, z. B. durch Personalisierung, wird dieses Feld bei der Suche nicht berücksichtigt. Suchkriterien werden nur dann auf Felder angewendet, wenn ihr Datentyp mit dem der Suchkriterien übereinstimmt. Zum Beispiel nach dem Begriff *heute* suchen durchsucht alle Text- und Codefelder nach dem Literalwert heute sowie alle Datumsfelder, in denen *heute* als Ausdruck für das aktuelle Datum ausgewertet wird, sucht jedoch nicht in numerischen Feldern. Weitere Informationen zu Filterkriterien finden Sie unter [Sortieren, Suchen und Filtern von Listen](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Gibt es Tastaturfunktionen für Suche und Filter?
Suche und Filter wurden für Benutzer optimiert, die eine mausfreie Interaktion bevorzugen, um effizient mit ihren Daten zu arbeiten. Es gibt eine Reihe von Tastenkombinationen, die nacheinander verwendet werden können, um schnell zu arbeiten. Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Ist der Filterbereich in allen Listen verfügbar?
Der Filterbereich ist in Bildschirmen verfügbar, in denen die Liste der primäre Inhalt der Seite ist, wie Arbeitsblätter und Listenseiten, einschließlich Listen, die von der Navigationsleiste erreichbar sind. Der Filterbereich ist noch nicht für Listen verfügbar, die als Teile angezeigt werden, z. B. FactBoxen oder Rollencenterteilen oder für Listen, die als Dialogfelder angezeigt werden, z. B. in Suchvorgängen. Wenn eine Liste auf einer Seite, wie Verkaufszeilen in einem Verkaufsauftrag eingebettet ist, ist der Filterbereich verfügbar, wenn man sich auf diese Liste mithilfe der Schaltfläche Fokusmodus fokussiert. Weitere Informationen finden Sie unter [Fokussieren auf Positionsartikel](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Wie kann ich meine Filter speichern?
Ihre Filter und Änderungen an vordefinierten Filtern werden während der Sitzung beibehalten (solange Sie angemeldet bleiben), selbst wenn Sie die Seite verlassen. Sie können Filter als benannte Ansicht der Liste dauerhaft speichern, indem Sie das Symbol ![Ansicht speichern](media/save_view_icon.png "Ansicht speichern") im Filterbereich wählen. Weitere Informationen finden Sie unter [FAQ anzeigen](ui-views-faq.md). Beachten Sie, dass der Suchtext im Gegensatz zu Filtern nicht gespeichert wird, wenn Sie von einer Seite weg navigieren, und nicht gespeichert wird, wenn Sie eine Ansicht speichern.

Auf Berichtsanforderungsseiten können Sie auch Filter speichern oder vordefinierte Filter verwenden. Weitere Informationen finden Sie unter [Gespeicherte Einstellungen verwenden](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Gleicht diese Funktion der erweiterten Filter und "Summenberechnung einschränken" in Microsoft Dynamics NAV?
[!INCLUDE[prod_short](includes/prod_short.md)] baut auf diesen gängigen Funktionen auf und bietet eine moderne und als nutzbare Oberfläche für die Suche und das Analysieren Ihrer Daten. Dank weiterer Tastenkombinationen und der Einführung der Suche [!INCLUDE[prod_short](includes/prod_short.md)] übertrifft die Funktionalität, die in Dynamics NAV bereitgestellt wird.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Kann ich mithilfe der Begleiter-Apps und Add-Ins für Microsoft 365 suchen und filtern?
In verschiedenen Formularfaktoren, wie Mobilegeräten oder Outlook, können Sie in Listen suchen, aber in den meisten Fällen nicht in einzelnen Feldern filtern. In der [!INCLUDE[prod_short](includes/prod_short.md)] App für Microsoft Teams sind sowohl die Suche als auch der Filter in Listen verfügbar.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Wie kann ich anzeigen, wie meine Suchbegriffe auf Felder in der Liste angewendet wurden?
Nachdem Sie Suchbegriffe in das Suchfeld eingegeben haben, können Sie die genauen Suchkriterien und die Felder anzeigen, auf die sie angewendet wurden, indem Sie den Seitenprüfbereich öffnen (**Strg + ALT+F1**) und dann die Registerkarte **Seitenfilter** wählen.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kann ich etwas gegen die Meldung "Die Suche nach Zeilen nimmt zu viel Zeit in Anspruch." unternehmen?

Es gibt eine Zeitbegrenzung für die Dauer eines Suchvorgangs. Versuchen Sie zunächst, die Suchkriterien zu ändern, und versuchen Sie es erneut. Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden, wenden sich an den Systemadministrator, da ein Administrator die Zeitbegrenzung für Suchen erhöhen kann.

Als lokaler Administrator können Sie die Zeitbegrenzung für Suchen erhöhen, indem Sie die Einstellung **Zeitbegrenzung für Suche** des [!INCLUDE[prod_short](includes/prod_short.md)]-Servers ändern. Weitere Informationen finden Sie unter [Konfigurieren des Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) in der Hilfe für Business Central-Entwickler und IT-Experten.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Wird Microsoft den Filterbereich ausbauen?
Bei Microsoft achten wir stets auf das Feedback aus unserer breitgefächerten Benutzer-Community und reagieren auf die häufigsten Vorschläge. Wenn Sie möchten, dass der Filterbereich auf weitere Formfaktoren, mehr Listenarten und Berichtstypen erweitert wird, oder wenn Sie eine großartige Idee zur Verbesserung haben, fügen unter [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas) eine Idee hinzu, oder stimmen Sie sich für eine vorhandene Idee ab.

## <a name="see-also"></a>Siehe auch
[Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Suche nach Seiten mit dem Rollen-Explorer](ui-role-explorer.md)  
[Erste Schritte](product-get-started.md)  
