---
title: Lesezeichen-Link zu Seite oder Bericht in Role Center
description: 'Mit dem Lesezeichensymbol können Sie über das Navigationsmenü Ihres Rollencenters eine Aktion hinzufügen, die eine Seite oder einen Bericht öffnet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter
Mit dem Symbol für ein Lesezeichen können Sie eine Aktion hinzufügen, die eine Seite oder einen Bericht aus dem Navigationsmenü Ihres Role Centers öffnet. Lesezeichen lassen zu, dass Sie schnell zu Ihren bevorzugten Inhalten oder Geschäftsaufgaben gelangen. Sie fügen das Lesezeichen von der Zielseite oder dem Zielbericht aus hinzu, d. h. von dem Bildschirm, der durch den Link im Rollenzentrum geöffnet werden soll.

Das Lesezeichen-Symbol wird in der oberen rechten Ecke einer Seite angezeigt und auch im **Tell Me**-Fenster, in dem Sie effizient mehrere Seiten oder Berichte mit Lesezeichen versehen können. Wenn für die Seite bereits ein Lesezeichen vorhanden ist, ist das Symbol dunkel und in der QuickInfo wird "Mit Lesezeichen versehen" angezeigt.

## <a name="to-bookmark-the-target-page"></a>So erstellen Sie ein Lesezeichen für die Zielseite
1. Öffnen Sie in Ihrem Rollencenter eine beliebige Seite, für die Sie einen Link im Rollencenter erstellen möchten.
2. Wählen Sie das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Eine nach der Seite benannte Aktion wird jetzt dem Navigationsmenü in Ihrem Rollencenter hinzugefügt.

## <a name="to-bookmark-the-target-report"></a>So erstellen Sie ein Lesezeichen für den Zielbericht
1. Öffnen Sie eine beliebige Berichtsanforderungsseite, für die Sie in Ihrem Rollencenter einen Link erstellen möchten.
2. Wählen Sie das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Eine nach dem Bericht benannte Aktion wird jetzt dem Navigationsmenü in Ihrem Rollencenter hinzugefügt.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>So erstellen Sie ein Lesezeichen für eine Seite oder einen Bericht über das Fenster „Wie möchten Sie weiter verfahren“
1. Öffne das **Wie möchten Sie weiter verfahren** Fenster und geben Sie zum Beispiel **Kundenaufträge** ein.
2. Bewegen Sie den Mauszeiger über das Suchergebnis für die Seite oder den Bericht **Verkaufsaufträge**, und wählen Sie dann das ![Lesezeichen.](media/ui_bookmark_icon.png "Lesezeichen") Symbol.

Eine nach der Seite oder dem Bericht benannte Aktion wird jetzt dem Navigationsmenü in Ihrem Rollencenter hinzugefügt.


## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

- **Kann ich meine Lesezeichen neu organisieren?**  
Ja. Sie können Ihr Rollencenter personalisieren und Aktionen in eine bessere Reihenfolge oder in vorhandene Gruppen oder Untergruppen verschieben.  
Erfahren Sie, wie Sie [Ihren Arbeitsbereich personalisieren](ui-personalization-user.md).

- **Wie entferne ich ein Lesezeichen?**  
Wählen Sie auf der Zielseite oder im Zielbericht erneut das Lesezeichensymbol aus, um die betreffende Aktion aus Ihrem Rollencenter zu entfernen. Sie können Ihr Rollencenter auch personalisieren und Aktionen vorübergehend ausblenden, ohne sie vollständig zu entfernen.

- **Wo finde ich meine Lesezeichen?**  
Wenn Sie einer Seite oder einem Bericht ein Lesezeichen hinzufügen, wird die neue Aktion dem oberen Navigationsmenü auf Ihrem aktuellen Startbildschirm (Rollencenter) hinzugefügt. Sollten Sie über viele Aktionen verfügen, müssen Sie möglicherweise die Schaltfläche **Mehr** aktivieren, um alle anzuzeigen, da die neue Aktion immer am Ende dieser Aktionen angehängt wird.
<!-- Should we add a screenshot here? -->

- **Ich habe kein Lesezeichensymbol. Ist ein Fehler aufgetreten?**  
Die Möglichkeit, ein Lesezeichen für eine Seite oder einen Bericht zu erstellen, ist eine von vielen Funktionen zur Benutzerpersonalisierung in Business Central. Wenn das Symbol für das Lesezeichen nicht angezeigt wird, hat Ihr Administrator wahrscheinlich die Personalisierung deaktiviert.

- **Warum kann ich bestimmte Seiten oder Berichte nicht mit einem Lesezeichen versehen?**  
Nicht alle Seiten und Berichte können mit einem Lesezeichen versehen werden. Wenn eine Seite oder ein Bericht innerhalb eines speziellen Kontexts ausgeführt wird, der von der Geschäftsanwendung gesteuert wird, wird das Lesezeichen-Symbol nicht angezeigt. Beispielsweise zeigen Seiten, die nicht im Fenster **Wie möchten Sie weiter verfahren** gefunden werden können, jedoch von einer anderen Stelle aus gestartet werden, kein Lesezeichensymbol an. Ebenso wird auf Berichtsanforderungsseiten, die nur zum Sammeln von Filtern verwendet werden, ohne den Bericht auszuführen, kein Lesezeichensymbol angezeigt.

  Weitere Informationen finden Sie in den technischen Details zu [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) und [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Werden beim Löschen meiner Personalisierung auch meine Lesezeichen gelöscht?**  
Ja. Lesezeichen befinden sich im Navigationsmenü. Wenn Sie Änderungen am Navigationsmenü auf einer beliebigen Seite oder alle Personalisierungen im Rollencenter löschen, werden alle Ihre neuen Aktionen dauerhaft entfernt.

- **Warum zeigt das Lesezeichen-Symbol weiterhin an, dass es noch nicht mit Lesezeichen versehen ist?**  
Wenn Sie ein Lesezeichen hinzufügen, wird die neue Aktion dem Navigationsmenü im Rollencenter hinzugefügt, und bei nachfolgenden Besuchen der Seite oder des Berichts wird ein dunkles Lesezeichensymbol angezeigt. Wenn Sie Ihr Rollencenter personalisieren und Ihre Aktionen neu organisieren, indem Sie sie in Gruppen verschieben, wird das Lesezeichensymbol nicht mehr dunkel und Sie können derselben Seite oder demselben Bericht ein weiteres Lesezeichen hinzufügen. Dies lässt zu, dass Sie mehrere Aktionen zu derselben Seite oder demselben Bericht hinzufügen und sie in verschiedene Gruppen einteilen können.

- **Warum zeigt mein Link zu einem Bericht einen anderen Bericht an?**  
Einige Berichte können durch andere Berichte ersetzt werden, nachdem eine Erweiterung auf Business Central angewendet wurde. Beim Ersetzen wird der Text der neuen Aktion nicht aktualisiert und zeigt weiterhin den Namen des ursprünglichen Berichts an, navigiert aber zu dem neueren Bericht. Um den Text der neuen Aktion zu korrigieren, können Sie die neue Aktion entfernen und erneut hinzufügen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Sind Lesezeichen für XMLports verfügbar?**  
Nein. Zur Zeit ist das Hinzufügen von Aktionen zum Öffnen von XMLports nicht über die Benutzeroberfläche möglich.

- **Werden meine Lesezeichen übersetzt, wenn ich meine Sprache in Business Central ändere?**  
Wenn Sie ein neues Lesezeichen hinzufügen, wird jeder übersetzte Text, der zu diesem Zeitpunkt verfügbar war, mit einem Lesezeichen versehen. Wenn später neuer übersetzter Text hinzugefügt wird, sind die neueren Übersetzungen nicht in der neuen Aktion enthalten.

- **Warum kann ich keinen Text in eine Seite einfügen, nachdem ich sie mit dem Lesezeichen geöffnet habe?**<br> Wenn eine Seite mit einem Lesezeichen versehen wird, wird die Seite immer im Ansichtsmodus vom Lesezeichen aus geöffnet &mdash; auch wenn sie sich beim Setzen des Lesezeichens im Bearbeitungsmodus befand. Die Auswahl des Symbols **Änderungen auf der Seite vornehmen**![Zeigt das Bleistift-Symbol zum Bearbeiten der Seite an.](media/edit-pencil.png) lässt Sie Text in die bearbeitbaren Felder einfügen.


## <a name="see-also"></a>Weitere Informationen
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
