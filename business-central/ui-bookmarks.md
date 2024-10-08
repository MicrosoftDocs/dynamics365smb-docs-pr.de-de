---
title: Verknüpfen als Lesezeichen für die Seite oder den Bericht im Rollencenter speichern
description: 'Mithilfe des Lesezeichensymbols können Sie eine Aktion hinzufügen, die eine Seite oder einen Bericht aus dem Navigationsmenü Ihres Rollencenters öffnet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Eine Seite oder einen Bericht in Ihrem Rollencenter mit einem Lesezeichen versehen

Mithilfe des Lesezeichensymbols können Sie eine Aktion hinzufügen, die eine Seite oder einen Bericht aus dem Navigationsmenü Ihres Rollencenters öffnet. Lesezeichen lassen zu, dass Sie schnell zu Ihren bevorzugten Inhalten oder Geschäftsaufgaben gelangen. Sie fügen das Lesezeichen von der Zielseite oder dem Zielbericht hinzu, also dem Bildschirm, den verknüpfen im Rollencenter öffnen soll.

Das Lesezeichen-Symbol wird in der oberen rechten Ecke einer Seite angezeigt und auch im **Tell Me**-Fenster, in dem Sie effizient mehrere Seiten oder Berichte mit Lesezeichen versehen können. Wenn für die Seite bereits ein Lesezeichen vorhanden ist, ist das Symbol dunkel und in der QuickInfo wird "Mit Lesezeichen versehen" angezeigt.

## <a name="bookmark-the-target-page"></a>Lesezeichen für die Zielseite setzen

1. Öffnen Sie in Ihrem Rollencenter eine beliebige Seite, für die Sie ein verknüpfen benötigen.
2. Wählen Sie das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Dem Navigationsmenü in Ihrem Rollencenter wird nun eine nach der Seite benannte Aktion hinzugefügt.

## <a name="bookmark-the-target-report"></a>Den Zielbericht mit einem Lesezeichen versehen

1. Öffnen Sie in Ihrem Rollencenter eine beliebige Berichtsanforderungsseite, für die Sie ein verknüpfen benötigen.
2. Wählen Sie das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Dem Navigationsmenü in Ihrem Rollencenter wird jetzt eine nach dem Bericht benannte Aktion hinzugefügt.

## <a name="bookmark-a-page-or-report-from-the-tell-me-window"></a>Eine Seite oder einen Bericht aus dem Fenster „Wie möchten Sie weiter vorgehen“ mit einem Lesezeichen versehen

1. Öffne das **Wie möchten Sie weiter verfahren** Fenster und geben Sie zum Beispiel **Kundenaufträge** ein.
2. Bewegen Sie den Mauszeiger über das Suchergebnis für die Seite oder den Bericht **Verkaufsaufträge**, und wählen Sie dann das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Dem Navigationsmenü in Ihrem Rollencenter wird jetzt eine nach der Seite oder dem Bericht benannte Aktion hinzugefügt.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="can-i-reorganize-my-bookmarks"></a>Kann ich meine Lesezeichen neu organisieren?

Ja. Sie können Ihr Rollencenter personalisieren und Aktionen in eine optimalere Reihenfolge bringen oder sie in vorhandene Gruppen oder Untergruppen verschieben.  
Erfahren Sie, wie Sie [Ihren Arbeitsbereich personalisieren](ui-personalization-user.md).

### <a name="how-do-i-remove-a-bookmark"></a>Wie entferne ich ein Lesezeichen?

Wählen Sie auf der Zielseite oder im Zielbericht erneut das Lesezeichensymbol aus, um die entsprechende Aktion aus Ihrem Rollencenter zu entfernen. Sie können Ihr Rollencenter auch personalisieren und Aktionen vorübergehend ausblenden, ohne sie vollständig zu entfernen.

### <a name="where-do-i-find-my-bookmarks"></a>Wo finde ich meine Lesezeichen?

Wenn Sie einer Seite oder einem Bericht ein Lesezeichen hinzufügen, wird die neue Aktion dem oberen Navigationsmenü auf Ihrem aktuellen Startbildschirm (Rollencenter) hinzugefügt. Sollten Sie über viele Aktionen verfügen, müssen Sie möglicherweise die Schaltfläche **Mehr** aktivieren, um alle anzuzeigen, da die neue Aktion immer am Ende dieser Aktionen angehängt wird.
<!-- Should we add a screenshot here? -->

### <a name="i-dont-have-a-bookmark-icon-is-something-wrong"></a>Ich verfüge über kein Lesezeichensymbol. Ist ein Fehler aufgetreten?

Die Möglichkeit, ein Lesezeichen für eine Seite oder einen Bericht zu erstellen, ist eine von vielen Funktionen zur Benutzerpersonalisierung in Business Central. Wenn das Symbol für das Lesezeichen nicht angezeigt wird, hat Ihr Administrator wahrscheinlich die Personalisierung deaktiviert.

### <a name="why-cant-i-bookmark-certain-pages-or-reports"></a>Warum kann ich bestimmte Seiten oder Berichte nicht mit meinen Lesezeichen versehen?

Nicht alle Seiten und Berichte können mit einem Lesezeichen versehen werden. Wenn eine Seite oder ein Bericht innerhalb eines speziellen Kontexts ausgeführt wird, der von der Geschäftsanwendung gesteuert wird, wird das Lesezeichen-Symbol nicht angezeigt. Beispielsweise zeigen Seiten, die nicht im Fenster **Wie möchten Sie weiter verfahren** gefunden werden können, jedoch von einer anderen Stelle aus gestartet werden, kein Lesezeichensymbol an. Ebenso wird auf Berichtsanforderungsseiten, die nur zum Sammeln von Filtern verwendet werden, ohne den Bericht auszuführen, kein Lesezeichensymbol angezeigt.

  Weitere Informationen finden Sie in den technischen Details zu [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) und [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

### <a name="when-clearing-my-personalization-will-my-bookmarks-also-be-cleared"></a>Werden beim Löschen meiner Personalisierung auch meine Lesezeichen gelöscht?

Ja. Lesezeichen befinden sich im Navigationsmenü. Wenn Sie Änderungen am Navigationsmenü auf einer beliebigen Seite löschen oder alle Personalisierungen im Rollencenter löschen, werden alle Ihre neuen Aktionen dauerhaft entfernt.

### <a name="why-does-the-bookmark-icon-continue-to-indicate-its-still-not-bookmarked"></a>Warum zeigt das Lesezeichensymbol weiterhin an, dass noch immer kein Lesezeichen vorhanden ist?

Wenn Sie ein Lesezeichen hinzufügen, wird die neue Aktion dem Navigationsmenü im Rollencenter hinzugefügt und bei nachfolgenden Besuchen der Seite oder des Berichts wird ein dunkles Lesezeichensymbol angezeigt. Wenn Sie Ihr Rollencenter personalisieren und Ihre Aktionen neu organisieren, indem Sie sie in Gruppen verschieben, ist das Lesezeichensymbol nicht mehr dunkel und Sie können derselben Seite oder demselben Bericht ein weiteres Lesezeichen hinzufügen. Dies lässt zu, dass Sie mehrere Aktionen zu derselben Seite oder demselben Bericht hinzufügen und sie in verschiedene Gruppen einteilen können.

### <a name="why-does-my-link-to-a-report-display-a-different-report"></a>Warum wird bei meinem verknüpfen zu einem Bericht ein anderer Bericht angezeigt?

Einige Berichte können durch andere Berichte ersetzt werden, nachdem eine Erweiterung auf Business Central angewendet wurde. Beim Ersetzen wird der Text der neuen Aktion nicht aktualisiert und zeigt weiterhin den Namen des ursprünglichen Berichts an, navigiert aber zu dem neueren Bericht. Um den Text der neuen Aktion zu korrigieren, können Sie die neue Aktion entfernen und erneut hinzufügen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### <a name="is-bookmarking-available-for-xmlports"></a>Ist die Funktion zum Setzen von Lesezeichen für XMLports verfügbar?

Anzahl Zur Zeit ist das Hinzufügen von Aktionen zum Öffnen von XMLports nicht über die Benutzeroberfläche möglich.

### <a name="will-my-bookmarks-be-translated-when-i-change-my-language-in-business-central"></a>Werden meine Lesezeichen übersetzt, wenn ich meine Sprache in Business Central ändere?

Wenn Sie ein neues Lesezeichen hinzufügen, wird jeder übersetzte Text, der zu diesem Zeitpunkt verfügbar war, mit einem Lesezeichen versehen. Wenn später neuer übersetzter Text hinzugefügt wird, sind die neueren Übersetzungen nicht in der neuen Aktion enthalten.

### <a name="why-cant-i-add-text-in-a-page-right-after-opening-it-with-the-bookmark"></a>Warum kann ich einer Seite nicht direkt Text hinzufügen, nachdem ich sie mit einem Lesezeichen geöffnet habe?

Wenn eine Seite mit einem Lesezeichen versehen wird, wird die Seite immer im Ansichtsmodus vom Lesezeichen aus geöffnet &mdash; auch wenn sie sich beim Setzen des Lesezeichens im Bearbeitungsmodus befand. Die Auswahl des Symbols **Änderungen auf der Seite vornehmen**![Zeigt das Bleistift-Symbol zum Bearbeiten der Seite an.](media/edit-pencil.png) lässt Sie Text in die bearbeitbaren Felder einfügen.

## <a name="see-also"></a>Siehe auch

[Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Grundlegende Einstellungen ändern](ui-change-basic-settings.md)  
[Angezeigte Features ändern](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
