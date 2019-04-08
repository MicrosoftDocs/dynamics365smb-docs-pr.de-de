---
title: Dynamics 365 Financials | Microsoft Docs
description: Informationen zu Accountant Hub für Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.openlocfilehash: 0c4dadb15c9756c49f94839236766432844088c8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798228"
---
# <a name="get-started-with-include-d365acclongincludesd365acclongmdmd"></a>Erste Schritte mit [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Jedes Unternehmens muss seine Bücher führen und die Buchhaltung genehmigen. Einige Unternehmen verwenden einen externen Buchhalter, und andere haben einen Buchhalter als Mitarbeiter. Wenn Sie ein Buchhalter mit mehreren Clients sind, können Sie das [!INCLUDE [d365acc](includes/d365acc_md.md)] als Ihr Dashboard für einen besseren Überblick über Ihre Clients verwenden.  

Sie erhalten Zugriff auf [!INCLUDE [d365acc](includes/d365acc_md.md)], indem Sie sich unter [Dynamics 365 – Accountant Hub auf Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants) anmelden  

> [!TIP]
>  Wenn Sich sich bei [!INCLUDE [d365acc](includes/d365acc_md.md)] anmelden, müssen Sie Ihre E-Mail-Adresse der Unternehmung angeben wie beispielsweise <em>me@accountant.com</em>. Es wird empfohlen, die gleiche E-Mail-Adresse zu verwenden, wenn Sie in Ihren Clients arbeiten [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)], sodass zwischen Clients einfach gewechselt werden kann. Die E-Mail-Adresse muss eine Arbeitsadresse sein, die auf Active Directory basiert.

## <a name="working-with-individual-clients"></a>Arbeiten mit einzelnen Clients
Das Dashboard zeigt die wichtigsten Informationen über jeden Clients an.  

> [!div class="mx-imgBorder"]
> ![Accountant Hub](./media/accountant-get-started/accountant-dashboard.png)

Die Spalte **Client-Name** zeigt die Namen Ihres Clients an, und die Spalten **Unternehmensname**zeigt alle Unternehmen an, wenn der Client mehr als einen Mandanten erstellt hat [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]. Es gibt auch Felder, die Ihnen Aufgaben zeigen, die Ihnen im Unternehmen Ihres Kunden zugeordnet werden, z. B. überfällige Aufgaben.  

Sie können das Dashboard anpassen, um die Datenpunkte zu zeigen, die Sie sehen möchten, indem Sie Spalten hinzufügen oder entfernen. Beispielsweise möchten Sie Steuern sehen, die fällig sind, wie viele offene Verkaufsbelege jeder Client hat oder die Anzahl der Einkaufsrechnungen, die nächste Woche fällig sind. Sie können die Ansicht konfigurieren, um Ihren Anforderungen zu entsprechen. Wenn Sie viele Clients haben, können Sie Filter setzen, um die Ansicht zu sortieren.  

Neben dem Clientnamen zeigene die drei Ellipsen ein Kurzmenü:

- Aktualisieren Sie das aktuelle Unternehmen und rufen Sie neue Daten für den Client ab  
- Navigieren Sie zum Client [!INCLUDE [d365fin](includes/d365fin_md.md)]  
- Weitere Clients auswählen  

In Analogie dazu können Sie das Dropdownmenü **Client-Zusammenfassung** verwenden, um alle Unternehmen zu aktualisieren.  

> [!TIP]
>  Um auf einem Client zuzugreifen [!INCLUDE [d365fin](includes/d365fin_md.md)], wählen Sie das Menüelement **Navigieren zum Client**. Sie werden automatisch angemeldet.

## <a name="company-details"></a>Unternehmensdetails
Sie können mehr Informationen über die Daten Ihrer Klienten anzeigen, indem Sie den Namen des Mandanten auswählen, zu dem Sie mehr erfahren möchten. Dadurch wird das **Unternehmensdetails** Fenster geöffnet, in dem Sie zusätzliche Informationen anzeigen können:  

* Kassenkontosalden  
* Cashflowplanung  
* Überfällige Einkaufsrechnungen  
* Überfällige Verkaufsrechnungen  

> [!div class="mx-imgBorder"]
> ![Kundenunternehmensdetails im Dashboard des Buchhalters](./media/accountant-get-started/accountant-company-details.png)

Technisch haben Sie sich jetzt bei Ihrem Client [!INCLUDE [d365fin](includes/d365fin_md.md)] angemeldet und Daten, die Sie sehen, sind Livedaten. Wenn Sie eine genauere Betrachtung der Daten vornehmen möchten, wie z.B. eine überfällige Einkaufsrechnung, wählen Sie den Link aus, und Sie gelangen zum Kundenunternehmen.  

> [!TIP]
> Sie können die vordefinierte Excel-Arbeitsmatte aus **Berichte** im Menüband anzeigen. Diese Excel-Arbeitsmappen sind dafür ausgelegt, bereit zu sein, Schlüsselfinanzauswertungen und Berichte zu drucken, können jedoch auch geändert werden, um sie Ihren Anforderungen anzupassen. Weitere Informationen finden Sie unter [Analysieren von Finanzauswertungen in Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) in der Hilfe für [!INCLUDE [d365fin](includes/d365fin_md.md)].  

Andernfalls schließen Sie den Detailbereich und gehen zum nächsten Client.  

## <a name="assigned-tasks"></a>Zugewiesene Aufgaben
Im [!INCLUDE [d365fin](includes/d365fin_md.md)] Ihres Kunden können Sie sich selbst sowie anderen Aufgaben zuordnen und andere Personen können Ihnen Aufgaben zuordnen. Ihr Dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] zeigt Ihnen eine Übersicht der zugewiesenen Aufgaben für jeden Kunden, und Sie können auf eine Liste aller zugewiesenen Aufgaben zugreifen, indem Sie in der linken Navigation **Meine Benutzeraufgaben** auf der Seite **Start**auswählen.  

Im Kundenunternehmen haben Sie auch Stapel, die Aufgaben ausrufen, die Ihnen bei diesem bestimmten Kunden zugeordnet werden.

> [!div class="mx-imgBorder"]
> ![Aufgaben, die dem Buchhalter im Kundenunternehmen zugeordnet sind](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Meine Benutzeraufgaben
Die Liste **Meine Benutzeraufgaben** in [!INCLUDE [d365acc](includes/d365acc_md.md)] hilft Ihnen dabei, Ihren Tag zu priorisieren, indem weitere Informationen über die Aufgaben angezeigt werden, die Ihnen von allen Ihren Kunden zugeordnet werden.  

> [!div class="mx-imgBorder"]
> ![Liste der Aufgaben, die mir al externem Buchhalter zugeordnet wurden](./media/accountant-get-started/accountant-tasklist.png)

Sie können z. B. nach Fälligkeitsdatum, oder einem beliebigen anderen Datentyp sortieren, der dabei hilft, den Tag zu priorisieren. Standardmäßig zeigt die Liste alle Aufgaben an, die Ihnen zugeordnet wurden, aber Sie können Filter setzen, um z.B. nur Aufgaben anzuzeigen, die mit hoher Priorität markiert wurden.

Um eine Aufgabe aufzunehmen, wählen Sie sie einfach aus der Liste der ausstehenden Benutzeraufgaben aus. Im Menüband öffnet der Link **Zu Aufgabenelement wechseln** die Seite, in dem Sie die Arbeit ausführen können.  

Wenn Sie eine Aufgabe abgeschlossen haben, kennzeichnen Sie sie einfach als abgeschlossen.  

## <a name="see-also"></a>Siehe auch

[Fügen Sie Ihren Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md) Kunden hinzu  
[Willkommen bei [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Finanzauswertungen analysieren in Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)  
[Buchhalter-Erfahrung in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 – Accountant Hub auf Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
