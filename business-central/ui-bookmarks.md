---
title: Erstellen eines Lesezeichens für einen Link zu einer Seite oder einem Bericht zum Rollencenter | Microsoft Docs
description: Erfahren Sie, wie Sie dem Rollencenter einen Link hinzugefügen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bb6c3762d9b6ec587cea6915cf292a6bb57e25fd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782493"
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter
Mit dem Lesezeichensymbol können Sie über das Navigationsmenü Ihres Rollencenters eine Aktion hinzufügen, die eine Seite oder einen Bericht öffnet. Auf diese Weise können Sie schnell Ihre bevorzugten Inhalte oder Geschäftsaufgaben aufrufen. Sie fügen das Lesezeichen von der Zielseite oder dem Zielbericht aus hinzu, d. h. von dem Bildschirm, der durch den Link im Rollenzentrum geöffnet werden soll.

Das Lesezeichensymbol wird in der oberen rechten Ecke einer Seite und auch im Fenster **Wie möchten Sie weiter verfahren** angezeigt, in dem Sie mehrere Seiten oder Berichte effizient mit einem Lesezeichen versehen können. Wenn für die Seite bereits ein Lesezeichen vorhanden ist, ist das Symbol dunkel und in der QuickInfo wird "Mit Lesezeichen versehen" angezeigt.

## <a name="to-bookmark-the-target-page"></a>So erstellen Sie ein Lesezeichen für die Zielseite
1. Öffnen Sie in Ihrem Rollencenter eine beliebige Seite, für die Sie einen Link im Rollencenter erstellen möchten.
2. Wählen Sie das ![Lesezeichen](media/ui_bookmark_icon.png "Lesezeichen")-Symbol.

Eine nach der Seite benannte Aktion wird jetzt dem Navigationsmenü in Ihrem Rollencenter hinzugefügt.

## <a name="to-bookmark-the-target-report"></a>So erstellen Sie ein Lesezeichen für den Zielbericht
1. Öffnen Sie eine beliebige Berichtsanforderungsseite, für die Sie in Ihrem Rollencenter einen Link erstellen möchten.
2. Wählen Sie das ![Lesezeichen](media/ui_bookmark_icon.png "Lesezeichen")-Symbol.

Eine nach dem Bericht benannte Aktion wird jetzt dem Navigationsmenü in Ihrem Rollencenter hinzugefügt.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>So erstellen Sie ein Lesezeichen für eine Seite oder einen Bericht über das Fenster „Wie möchten Sie weiter verfahren“
1. Öffne das **Wie möchten Sie weiter verfahren** Fenster und geben Sie zum Beispiel **Kundenaufträge** ein.
2. Zeigen Sie mit der Maus auf das Suchergebnis für die Seite **Verkaufsaufträge** oder den Bericht, und wählen Sie dann das Symbol für ![Lesezeichen](media/ui_bookmark_icon.png "Lesezeichen") aus.

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
Die Möglichkeit, ein Lesezeichen für eine Seite oder einen Bericht zu erstellen, ist eine von vielen Funktionen zur Benutzerpersonalisierung in Business Central. Wenn das Lesezeichensymbol nicht angezeigt wird, hat Ihr Administrator die Personalisierung möglicherweise deaktiviert.

- **Warum kann ich bestimmte Seiten oder Berichte nicht mit einem Lesezeichen versehen?**  
Nicht alle Seiten und Berichte können mit einem Lesezeichen versehen werden. Wenn eine Seite oder ein Bericht in einem speziellen Kontext ausgeführt wird, der von der Geschäftsanwendung gesteuert wird, wird das Lesezeichensymbol nicht angezeigt. Beispielsweise zeigen Seiten, die nicht im Fenster **Wie möchten Sie weiter verfahren** gefunden werden können, jedoch von einer anderen Stelle aus gestartet werden, kein Lesezeichensymbol an. Ebenso wird auf Berichtsanforderungsseiten, die nur zum Sammeln von Filtern verwendet werden, ohne den Bericht auszuführen, kein Lesezeichensymbol angezeigt.

Weitere Informationen finden Sie in den technischen Details zu [RunRequestPage](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) und [FilterPageBuilder](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Werden beim Löschen meiner Personalisierung auch meine Lesezeichen gelöscht?**  
Ja. Lesezeichen befinden sich im Navigationsmenü. Wenn Sie Änderungen am Navigationsmenü auf einer beliebigen Seite oder alle Personalisierungen im Rollencenter löschen, werden alle Ihre neuen Aktionen dauerhaft entfernt.

- **Warum zeigt das Lesezeichensymbol weiterhin an, dass es immer noch nicht mit einem Lesezeichen versehen ist?**  
Wenn Sie ein Lesezeichen hinzufügen, wird die neue Aktion dem Navigationsmenü im Rollencenter hinzugefügt, und bei nachfolgenden Besuchen der Seite oder des Berichts wird ein dunkles Lesezeichensymbol angezeigt. Wenn Sie Ihr Rollencenter personalisieren und Ihre Aktionen neu organisieren, indem Sie sie in Gruppen verschieben, wird das Lesezeichensymbol nicht mehr dunkel und Sie können derselben Seite oder demselben Bericht ein weiteres Lesezeichen hinzufügen. Auf diese Weise können Sie derselben Seite oder demselben Bericht mehrere Aktionen hinzufügen und diese in verschiedene Gruppen einteilen.

- **Warum zeigt mein Link zu einem Bericht einen anderen Bericht an?**  
Einige Berichte können durch andere Berichte ersetzt werden, nachdem eine Erweiterung auf Business Central angewendet wurde. Wenn eine Ersetzung erfolgt, wird der Text der neuen Aktion nicht aktualisiert und zeigt weiterhin den Namen des ursprünglichen Berichts an, navigiert jedoch zum neueren Bericht. Um den Text der neuen Aktion zu korrigieren, können Sie die neue Aktion entfernen und erneut hinzufügen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Sind Lesezeichen für XMLports verfügbar?**  
Nr. Derzeit ist das Hinzufügen von Aktionen zum Öffnen von XMLports über die Benutzeroberfläche nicht möglich.

- **Werden meine Lesezeichen übersetzt, wenn ich meine Sprache in Business Central ändere?**  
Wenn Sie ein neues Lesezeichen hinzufügen, wird jeder übersetzte Text, der zu diesem Zeitpunkt verfügbar war, mit einem Lesezeichen versehen. Wenn später neuer übersetzter Text hinzugefügt wird, sind die neueren Übersetzungen nicht in der neuen Aktion enthalten.


## <a name="see-also"></a>Siehe auch
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Merkmale angezeigt werden](ui-experiences.md)  
