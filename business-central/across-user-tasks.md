---
title: Zuweisen und Verwalten von Aufgaben | Microsoft Docs
description: Erfahren Sie, wie Benutzern, einschließlich Ihres Buchhalters, Aufgaben in Business Central zugewiesen werden
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c76751726f5cd680fafc0887fc57a1464d0ac3ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922617"
---
# <a name="define-user-tasks"></a>Benutzeraufgaben definieren

In [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Aufgaben erstellen, die Sie an Arbeit erinnern, die durchgeführt werden muss. Sie können Aufgaben für sich selbst erstellen, aber Sie können auch Aufgaben an Andere zuweisen oder Ihnen kann von jemand anderem in Ihrer Organisation eine Aufgabe zugewiesen werden.  

## <a name="managing-user-tasks"></a>Benutzeraufgaben verwalten

Die Seite **Benutzeraufgaben** zeigt alle Aufgaben an, und Sie können einfach neue Aufgaben erstellen und zuweisen. Wenn Sie eine Aufgabe erstellen, können Sie das Startdatum und das Fälligkeitsdatum angeben, und Sie können einen Link auf der Seite oder dem Bericht in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzufügen, wo der Benutzer die Arbeit machen muss.  

Beispielsweise können Sie eine Aufgabe für sich selbst oder einen Mitarbeiter erstellen, sodass alle gebuchten Verkaufsrechnungen angezeigt werden. In diesem Fall können Sie die Aufgabe mit Seite 143, **„Gebuchte Verkaufsrechnungen“** , verknüpfen. Im folgenden Screenshot erstellt jemand eine Aufgabe für MeganB, um die gebuchten Verkaufsrechnungen zu überprüfen.  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Beispiel für eine Benutzeraufgabe":::

> [!TIP]  
> Verwenden Sie die Suche im Feld **Seite** , und verwenden Sie dann das Feld **Suche** , um die Seite zu finden, die Sie anzeigen möchten.  
>
> Sie können auf jede Seite verlinken, aber nicht auf einzelne Einträge. Machen Sie die Beschreibung daher so explizit wie möglich, z. B. „Bitte werfen Sie einen Blick auf Kunden-Nr. 10000 und stellen Sie sicher, dass keine überfälligen Zahlungen vorliegen.“

### <a name="picking-up-user-tasks"></a>Benutzeraufgaben aufnehmen

In den Rollencentern Geschäftsführer, Bookkeeper und Buchhalter zeigt eine Kachel ausstehende Aufgaben an, die diesem Benutzer zugewiesen sind. Um eine Aufgabe aufzunehmen, wählen Sie sie einfach aus der Liste der ausstehenden Benutzeraufgaben aus. Im Menüband öffnet der Link **Zu Aufgabenelement wechseln** die Seite, in dem Sie die Arbeit ausführen können.  

Wenn Sie eine Aufgabe abgeschlossen haben, kennzeichnen Sie sie einfach als abgeschlossen.  

### <a name="deleting-user-tasks"></a>Benutzeraufgaben löschen

Wenn Sie eine Massenlöschung aller oder einiger Benutzeraufgaben vornehmen möchten, können Sie den Bericht **Benutzeraufgaben** löschen verwenden. Auf der Anforderungsseite können Sie Filter festlegen, um zu bestimmen, welche Aufgaben gelöscht werden müssen.  

## <a name="see-also"></a>Siehe auch

[Nach einer Seite oder einem Bericht suchen](ui-search.md)  
[Buchhalter-Erfahrung in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)  
