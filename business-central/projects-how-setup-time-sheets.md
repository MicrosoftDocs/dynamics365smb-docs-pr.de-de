---
title: Festlegen von Arbeitszeittabellen und deren Genehmigung
description: 'Sie richten Arbeitszeittabellen ein, um die für Aufgaben und Projekte aufgewendete Zeit zu verfolgen und Ihnen das Projektmanagement, die Stellenbesetzung und die Kapazitätsplanung zu erleichtern.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: bholtorf
---
# Einrichten von Arbeitszeittabellen

Arbeitszeittabellen in [!INCLUDE[prod_short](includes/prod_short.md)] erfassen die Zeit in wöchentlichen Schritten von sieben Tagen. Sie können sie verwenden, um die für Projekte aufgewendete Zeit zu verfolgen und um die Ressourcenzeiterfassung aufzuzeichnen. Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie angeben, welche Benutzer Arbeitszeittabellen übermitteln und wie Sie Arbeitszeittabellen konfigurieren möchten.  

> [!TIP]
> In [!INCLUDE [prod_short](includes/prod_short.md)] sind die Benutzer von Arbeitszeittabellen *Ressourcen*. Auf diese Weise können Sie beispielsweise Arbeitszeittabellen verwenden, um die Arbeit von Nichtmitarbeitern zu verfolgen. Um die Arbeit Ihrer eigenen Mitarbeiter zu verfolgen oder Arbeitszeittabellen zum Verfolgen von Mitarbeiterabwesenheiten zu verwenden, müssen Sie *Mitarbeiter* *Ressourcen* im Einrichtungsleitfaden zuordnen.  

Geben Sie optional an, ob und wie Arbeitszeittabellen genehmigt werden. Abhängig von den Anforderungen Ihrer Organisation, können Sie festlegen:

* Einen oder mehrere Benutzer als Arbeitszeittabellenadministrator und Genehmiger für alle Arbeitszeittabellen.
* Ein Arbeitszeittabellengenehmiger für jede Ressource.

Wenn Sie Arbeitszeittabellen eingerichtet haben, können Sie Arbeitszeittabellen für Ressourcen erstellen und die Ressourcen können Arbeitszeittabellenzeilen buchen. Weisen Sie Arbeitszeittabellen optional Projektplanungzeilen zu. Weitere Informationen finden Sie unter [Verwenden von Arbeitszeittabellen](projects-how-use-time-sheets.md).  

## Arbeitszeittabellen mit der Anleitung zur unterstützten Einrichtung festlegen

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Ab dem Veröffentlichungszyklus 2021 2 können Sie eine Anleitung zur unterstützten Einrichtung verwenden, um Arbeitszeittabellen festzulegen.  

> [!TIP]
> Um diese Funktionalität nutzen zu können, müssen Sie die Funktion **Funktion Update: Neue Erfahrung mit Arbeitszeittabellen** auf der Seite [Funktionalität Verwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren.
>
> Die gleiche Funktion erleichtert auch die Verwaltung von Arbeitszeittabellen auf einem mobilen Gerät.

Öffnen Sie die Anleitung **Arbeitszeittabellen einrichten** für unterstützte Einrichtung über die Seite [Unterstützte Einrichtung](https://businesscentral.dynamics.com/?page=1801).

Die Anleitung zur unterstützten Einrichtung führt Sie durch die folgenden Schritte:

1. Legen Sie die Teilnehmer an den Arbeitszeittabellenprozessen fest

    Die erste Seite in der Anleitung zeigt die Anzahl der Benutzer in [!INCLUDE [prod_short](includes/prod_short.md)] an. Dort werden außerdem andere erforderliche und optionale Informationen angezeigt.  
2. Legen Sie den ersten Tag einer Arbeitswoche in dieser Organisation fest

    Der erste Tag einer Arbeitswoche ist standardmäßig der erste Tag für alle Arbeitszeittabellen.
3. Legen Sie die Person fest, die Arbeitszeittabellen verwaltet

    Diese Person kann alle Arbeitszeittabellen bearbeiten und löschen. Optional können Sie auf der Seite **Benutzereinrichtung** anderen Personen die gleiche Rolle zuweisen.
4. Legen Sie die Ressourcen fest, die Arbeitszeittabellen verwenden werden, und die Personen, die Arbeitszeittabellen genehmigen werden

Am Ende der Anleitung zur Einrichtung können Sie festlegen, dass [!INCLUDE [prod_short](includes/prod_short.md)] die Arbeitszeittabellen auf der Grundlage Ihrer Konfiguration erstellt. Zeigen Sie die neuen Arbeitszeittabellen auf der Seite **Arbeitszeittabellen** an, die Sie [hier](https://businesscentral.dynamics.com/?page=951) öffnen können. Alternativ können Sie die Anleitung zur unterstützten Einrichtung erneut ausführen oder die Einrichtung manuell vornehmen.  

## Arbeitszeittabellen manuell festlegen

In den folgenden Abschnitten wird beschrieben, wie Sie Arbeitszeittabellen festlegen, wenn Sie nicht die Anleitung **Zeittabellen einrichten** für die unterstützte Einrichtung verwenden.  

### So legen Sie die allgemeinen Informationen für Arbeitszeittabellen manuell fest

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") aus, geben Sie **Ressourcen Einr.** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Für das Feld **Arbeitszeittabelle nach Projekt-Genehmigung** wählen Sie eine der folgenden Optionen aus.

| Option | Beschreibung |
| --- | --- |
| **Nie** |Der Benutzer im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** der Ressourcenkarte genehmigt die Arbeitszeittabelle. |
| **Immer** |Der Benutzer im Feld **Verantwortliche Person** der Projektkarte genehmigt die Arbeitszeittabelle. |
| **Nur Arbeitsplätze** |Wenn die Arbeitsplatzzeittabelle mit einem Projekt verknüpft ist, dann genehmigt der Benutzer im Feld **Verantwortliche Person** auf der Projektkarte die Arbeitszeittabelle. Wenn die Arbeitsplatzzeittabelle mit einer Ressource verknüpft ist, dann genehmigt der Benutzer im Feld **Arbeitszeittabelle Genehmiger-Benutzer-ID** auf der Ressourcenkarte die Arbeitszeittabelle. |

### So weisen Sie einen Arbeitszeittabellen-Administrator manuell zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Fügen Sie einen neuen Benutzer hinzu, wenn die Benutzerliste nicht die Person enthält, die Arbeitszeittabelleadministrator sein soll. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).
3. Wählen Sie einen Benutzer aus, der Arbeitszeittabellenadministrator sein soll, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabellen-Administrator** aus.  

> [!TIP]  
> Es wird empfohlen, nur einen Benutzer als Arbeitszeittabellenadministrator für ein Unternehmen festzulegen. Im folgenden Verfahren richten Sie einen Arbeitszeittabellenbesitzer und - genehmiger ein, wenn der Arbeitszeittabellengenehmiger für jede Ressource zugeordnet ist.  

### So weisen Sie einen Besitzer und Genehmiger von Arbeitszeittabellen manuell zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Ressource, für die Sie die Möglichkeit einrichten möchten, Arbeitszeittabellen zu verwenden, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabelle verwenden**.  
3. Geben Sie im Feld **Arbeitszeittabellenbesitzer-Benutzer-ID** die ID des Besitzers der Arbeitszeittabelle ein. Der Eigentümer kann Bearbeitungszeit auf der Arbeitszeittabelle eingeben und ihn zur Genehmigung senden. Wenn es sich bei der Ressource um eine Person handelt, ist diese Person im Allgemeinen auch der Besitzer.  
4. Geben Sie im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** die ID des Genehmigers der Arbeitszeittabelle ein. Der Genehmiger kann eine Arbeitszeittabelle genehmigen, ablehnen oder erneut öffnen.  

> [!NOTE]  
> Sie können die ID des Arbeitszeittabellengenehmigers nicht ändern, wenn Arbeitszeittabellen vorhanden sind, die noch nicht verarbeitet wurden und die den Status **Übermittelt** oder **Offen**haben.

## Siehe auch

[Arbeitszeittabellen für Projekte verwenden](projects-how-use-time-sheets.md)  
[Wie Sie Arbeitszeittabellen erstellen](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Verbrauch oder Nutzung für Projekt erfassen](projects-how-record-job-usage.md)  
[Einrichten des Projektmanagements](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
