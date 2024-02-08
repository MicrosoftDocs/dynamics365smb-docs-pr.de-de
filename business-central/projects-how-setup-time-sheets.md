---
title: Festlegen von Arbeitszeittabellen und deren Genehmigung
description: 'Sie richten Arbeitszeittabellen ein, um die für Aufgaben und Projekte aufgewendete Zeit zu verfolgen und Ihnen das Projektmanagement, die Stellenbesetzung und die Kapazitätsplanung zu erleichtern.'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Einrichten von Arbeitszeittabellen

Arbeitszeittabellen in [!INCLUDE[prod_short](includes/prod_short.md)] erfassen die Zeit in wöchentlichen Schritten von sieben Tagen. Sie können sie verwenden, um die für Projekte aufgewendete Zeit zu verfolgen und um die Ressourcenzeiterfassung aufzuzeichnen. Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie angeben, welche Benutzer Arbeitszeittabellen übermitteln und wie Sie Arbeitszeittabellen konfigurieren möchten.  

> [!TIP]
> Die Menschen, die Arbeitszeittabellen verwenden, sind *Ressourcen*. So können Sie zum Beispiel Arbeitszeittabellen verwenden, um die Arbeit von Nicht-Mitarbeitern zu erfassen. Um die Arbeit der Mitarbeiter zu verfolgen oder Arbeitszeittabellen zur Erfassung der Abwesenheit von Mitarbeitern zu verwenden, müssen Sie Mitarbeiter mit Ressourcen verknüpfen. Es gibt eine Anleitung zur unterstützten Einrichtung, die Ihnen dabei helfen kann. Um mehr über den Leitfaden zu erfahren, gehen Sie zu [Arbeitszeittabellen mit der Anleitung zur unterstützten Einrichtung festlegen](#set-up-time-sheets-with-the-assisted-setup-guide).  

Optional können Sie angeben, ob und wie Arbeitszeittabellen genehmigt werden. Abhängig von den Anforderungen Ihrer Organisation, können Sie festlegen:

* Einen oder mehrere Benutzer als Arbeitszeittabellenadministrator und Genehmiger für alle Arbeitszeittabellen.
* Ein Arbeitszeittabellengenehmiger für jede Ressource.

Wenn Sie Arbeitszeittabellen eingerichtet haben, können Sie Arbeitszeittabellen für Ressourcen erstellen und die Ressourcen können Arbeitszeittabellenzeilen buchen. Weisen Sie Arbeitszeittabellen optional Projektplanungzeilen zu. Weitere Informationen finden Sie unter [Arbeitszeittabellen verwenden](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Arbeitszeittabellen mit der Anleitung zur unterstützten Einrichtung festlegen

Eine Anleitung zum Einrichten von Arbeitszeittabellen kann Ihnen helfen, diese einzurichten.  

> [!TIP]
> Wenn Sie eine frühere Version als 2023 Veröffentlichungszyklus 1 (v22) haben, müssen Sie die Funktion **Funktionsaktualisierung: Neue Arbeitszeittabelle** auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren, um diese Funktion nutzen zu können.
>
> Mit dieser Einstellung können Sie Arbeitszeittabellen auch auf mobilen Geräten verwenden.

Öffnen Sie die Anleitung **Arbeitszeittabellen einrichten** für unterstützte Einrichtung über die Seite [Unterstützte Einrichtung](https://businesscentral.dynamics.com/?page=1801).

Die Anleitung zur unterstützten Einrichtung führt Sie durch die folgenden Schritte:

1. Legen Sie die Teilnehmer an den Arbeitszeittabellenprozessen fest.

    Die erste Seite in der Anleitung zeigt die Anzahl der Benutzer in [!INCLUDE [prod_short](includes/prod_short.md)] an. Dort werden außerdem andere erforderliche und optionale Informationen angezeigt.  
2. Legen Sie den ersten Tag einer Arbeitswoche in dieser Organisation fest.

    Der erste Tag einer Arbeitswoche ist standardmäßig der erste Tag für alle Arbeitszeittabellen.
3. Legen Sie die Person fest, die Arbeitszeittabellen verwaltet.

    Diese Person kann alle Arbeitszeittabellen bearbeiten und löschen. Optional können Sie auf der Seite **Benutzereinrichtung** anderen Personen die gleiche Rolle zuweisen.
4. Legen Sie die Ressourcen fest, die Arbeitszeittabellen verwenden werden, und die Personen, die Arbeitszeittabellen genehmigen werden.

Am Ende der Anleitung zur Einrichtung können Sie festlegen, dass [!INCLUDE [prod_short](includes/prod_short.md)] die Arbeitszeittabellen auf der Grundlage Ihrer Konfiguration erstellt. Zeigen Sie die neuen Arbeitszeittabellen auf der Seite **Arbeitszeittabellen** an, die Sie [hier](https://businesscentral.dynamics.com/?page=951) öffnen können. Alternativ können Sie die Anleitung zur unterstützten Einrichtung erneut ausführen oder die Einrichtung manuell vornehmen.

> [!IMPORTANT]
> Wenn Sie 2023 Veröffentlichungszyklus 1 (v22) oder später verwenden, müssen Sie, um sicherzustellen, dass Sie Arbeitszeittabellen auf mobilen Geräten verwalten können, die Option **Neue Erfahrung mit Arbeitszeittabellen verwenden** für die Einrichtung der Arbeitszeittabellen manuell aktivieren, wie im folgenden Verfahren beschrieben.

## <a name="set-up-time-sheets-manually"></a>Arbeitszeittabellen manuell festlegen

In den folgenden Abschnitten wird beschrieben, wie Sie Arbeitszeittabellen festlegen, wenn Sie nicht die Anleitung **Zeittabellen einrichten** für die unterstützte Einrichtung verwenden.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>So legen Sie die allgemeinen Informationen für Arbeitszeittabellen manuell fest

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") aus, geben Sie **Ressourcen Einr.** ein, und wählen Sie dann den zugehörigen Link aus.  
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Wenn Sie 2023 Veröffentlichungszyklus 1 (v22) oder später verwenden, um sicherzustellen, dass Sie Arbeitszeittabellen auf mobilen Geräten verwalten können, aktivieren Sie die Option **Neue Erfahrung mit Arbeitszeittabellen verwenden**.
1. Für das Feld **Arbeitszeittabelle nach Projekt-Genehmigung** wählen Sie eine der folgenden Optionen aus.

| Option | Beschreibung |
| --- | --- |
| **Nie** |Der Benutzer im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** der Ressourcenkarte genehmigt die Arbeitszeittabelle. |
| **Immer** |Der Benutzer im Feld **Verantwortliche Person** der Projektkarte genehmigt die Arbeitszeittabelle. |
| **Nur Arbeitsplätze** |Wenn die Arbeitsplatzzeittabelle mit einem Projekt verknüpft ist, dann genehmigt der Benutzer im Feld **Verantwortliche Person** auf der Projektkarte die Arbeitszeittabelle. Wenn die Arbeitsplatzzeittabelle mit einer Ressource verknüpft ist, dann genehmigt der Benutzer im Feld **Arbeitszeittabelle Genehmiger-Benutzer-ID** auf der Ressourcenkarte die Arbeitszeittabelle. |

### <a name="assign-a-time-sheet-administrator-manually"></a>So weisen Sie einen Arbeitszeittabellen-Administrator manuell zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie den Benutzer aus, der als Arbeitszeittabellen-Administrator fungieren soll, und aktivieren Sie dann das Kontrollkästchen **Zeittabellen-Administrator**.  

> [!TIP]  
> Wir empfehlen, nur einen Benutzer als Arbeitszeittabellenadministrator für ein Unternehmen festzulegen. Im folgenden Verfahren richten Sie einen Arbeitszeittabellenbesitzer und - genehmiger ein, wenn der Arbeitszeittabellengenehmiger für jede Ressource zugeordnet ist.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>So weisen Sie einen Besitzer und Genehmiger von Arbeitszeittabellen manuell zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Ressource, für die Sie die Möglichkeit einrichten möchten, Arbeitszeittabellen zu verwenden, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabelle verwenden**.  
3. Geben Sie im Feld **Arbeitszeittabellenbesitzer-Benutzer-ID** die ID des Besitzers der Arbeitszeittabelle ein. Der Eigentümer kann Bearbeitungszeit auf der Arbeitszeittabelle eingeben und ihn zur Genehmigung senden. Wenn es sich bei der Ressource um eine Person handelt, ist diese Person im Allgemeinen auch der Besitzer.  
4. Geben Sie im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** die ID des Genehmigers der Arbeitszeittabelle ein. Der Genehmiger kann eine Arbeitszeittabelle genehmigen, ablehnen oder erneut öffnen.  

> [!NOTE]  
> Sie können die ID des Arbeitszeittabellengenehmigers nicht ändern, wenn Arbeitszeittabellen vorhanden sind, die noch nicht verarbeitet wurden und die den Status **Übermittelt** oder **Offen**haben.

## <a name="see-also"></a>Siehe auch

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
