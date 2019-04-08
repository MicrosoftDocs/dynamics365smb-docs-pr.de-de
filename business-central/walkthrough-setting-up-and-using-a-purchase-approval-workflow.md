---
title: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows | Microsoft Docs
description: Sie können den Genehmigungsprozesses für neuen oder geänderten Datensätze, z. B. Dokumente, Buch.-Blattzeilen und Debitorenkarten automatisieren, indem Sie Workflows mit Schritten für die entsprechenden Genehmigungen erstellen. Bevor Sie Genehmigungsworkflows erstellen, müssen Sie einen Genehmiger und einen Stellvertreter für jeden Genehmigungsbenutzer einrichten. Sie können außerdem Grenzbeträge für die Genehmiger festlegen, um zu definieren, für welche Verkaufs- und Einkaufsdatensätze sie für eine Genehmigung qualifiziert sind. Genehmigungsanforderungen und andere Benachrichtigungen können als E-Mail oder interne Notiz gesendet werden. Für jede Genehmigungsbenutzereinrichtung können Sie angeben wann dieser Benachrichtigungen erhält.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/08/2018
ms.author: sgroespe
ms.openlocfilehash: d7af9edc0620a61f6e3f114feff3a831e91add57
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798448"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows
Sie können den Genehmigungsprozesses für neuen oder geänderten Datensätze, z. B. Dokumente, Buch.-Blattzeilen und Debitorenkarten automatisieren, indem Sie Workflows mit Schritten für die entsprechenden Genehmigungen erstellen. Bevor Sie Genehmigungsworkflows erstellen, müssen Sie einen Genehmiger und einen Stellvertreter für jeden Genehmigungsbenutzer einrichten. Sie können außerdem Grenzbeträge für die Genehmiger festlegen, um zu definieren, für welche Verkaufs- und Einkaufsdatensätze sie für eine Genehmigung qualifiziert sind. Genehmigungsanforderungen und andere Benachrichtigungen können als E-Mail oder interne Notiz gesendet werden. Für jede Genehmigungsbenutzereinrichtung können Sie angeben wann dieser Benachrichtigungen erhält.

> [!NOTE]
> Zusätzlich zur Workflowfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] ist die Microsoft Flow-Integration möglich, um Workflows für Ereignisse in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu definieren. Beachten Sie, dass, obwohl es zwei verschiedene Workflowsysteme sind, eine mit Microsoft Flow erstellte Fluss-Vorlage der Liste von Workflow-Vorlagen in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt wird. Weitere Informationen finden Sie unter [Business Central in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md).   

 Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Einrichten von Genehmigungsbenutzern.  
-   Benachrichtigungen für Genehmigungsbenutzer einrichten.  
-   Den Genehmigungsworkflow ändern und aktivierend.  
-   Die Genehmigung einer Einkaufsbestellung als Christine.  
-   Empfangen einer Benachrichtigung und Genehmigung als Stephan.  

## <a name="prerequisites"></a>Voraussetzungen  
Um diese exemplarische Vorgehensweise abzuschließen, benötigen Sie das CRONUS AG-Demounternehmen.

## <a name="story"></a>Hintergrund  
Stephan ist ein Superuser bei CRONUS. Er erstellt zwei Genehmigungsbenutzer. Der eine ist Christine, die einen Einkäufer darstellt. Der andere ist er selbst. Er ist der Genehmiger für Christine. Stephan gibt sich selbst unbegrenzten Rechte zur Genehmigung und legt fest, dass er Benachrichtigungen über eine interne Notiz bei einem entsprechendes Ereignis erhält. Als letztes erstellt erstellt Stephan den erforderlichen Genehmigungsworkflow als Kopie der vorhandenen Workflow-Vorlage "Workflow Einkaufsbestellungsgenehmigung". Er übernimmt alle Ereignisbedingungen unverändert und aktiviert dann den Workflow.  

Um den Genehmigungsworkflow zu testen, meldet sich Sean in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia an, und fordert dann die Genehmigung einer Einkaufsbestellung an. Dann meldet sich Stephan als er selbst an, sieht die Notiz in seinem Rollencenter, folgt der Verknüpfung zur Genehmigungsanforderung für die Einkaufsbestellung, und genehmigt die Anforderung.  

## <a name="setting-up-sample-data"></a>Einrichten der Beispieldaten
Bevor Sie Genehmigungsbenutzer und deren Benachrichtigungsmethode einrichten können, müssen Sie sicherstellen, dass zwei Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)]: vorhanden sind. Ein Benutzer stellt Christine dar. Die andere Benutzer, Sie, stellt Stephan dar. Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Einrichten von Genehmigungsbenutzern  
Wenn Sie als Sieselbst angemeldet sind, richten Sie Christine als einen Genehmigungsbenutzer ein, dessen Genehmiger Sie sind. Richten Sie Ihre Genehmigungsrechte ein, und geben Sie an, wie und wann Sie über Genehmigungsanforderungen benachrichtigt werden.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>So richten Sie sich selbst und Christine als Genehmigungsbenutzer ein  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Genehmigungsbenutzer Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Genehmigungsbenutzereinrichtung** die Aktion **Neu** aus.  

    > [!NOTE]  
    >  Sie müssen einen Genehmiger einrichten, bevor Sie Benutzer einrichten können, die die Genehmigung dieses Genehmigers benötigen. Sie müssen sich selbst Einrichten, bevor Sie Christine einrichten.  

3.  Richten Sie zwei Genehmigungsbenutzer ein, indem Sie die Felder aus der folgenden Tabelle ausfüllen.  

    |Benutzer ID|Genehmiger-ID|Unbegrenzte Einkaufsgenehmigung|  
    |-------------|-----------------|---------------------------------|  
    |SIE||Ausgewählt|  
    |CHRISTINE|SIE||  

### <a name="setting-up-notifications"></a>Einrichten von Benachrichtigungen  
In dieser exemplarischen Vorgehensweise wird der Benutzer über eine interne Notiz über die Genehmigung benachrichtigt. Die Genehmigungsbenachrichtigung kann auch per E-Mail erfolgen. Weitere Informationen finden Sie unter [Definieren Sie, wann und wie Sie Benachrichtigungen möchten](across-how-to-specify-when-and-how-to-receive-notifications.md). 

#### <a name="to-set-up-how-and-when-you-are-notified"></a>So legen Sie fest, wie und wann Sie benachrichtigt werden  
1.  Auf der Seite **Genehmigungsbenutzereinrichtung** wählen Sie die Zeile für sich und dann die **Benachrichtigungseinrichtung** Aktion aus.  
2.  Auf der Seite **Benachrichtigungseinrichtung** im Feld **Benachrichtigungstyp**, wählen Sie **Genehmigung** aus.  
3.  Wählen Sie im Feld **Benachrichtigungsmethode** die Option **Hinweis** aus.  
6.  Wählen Sie auf der Seite **Benachrichtigungseinrichtung** die Aktion **Benachrichtigungsplan** aus.  
7.  Wählen Sie auf der Seite **Benachrichtigungsplan** im Feld **Vorkommen** die Option **Sofort** aus.  
8. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="creating-the-approval-workflow"></a>Erstellen des Genehmigungsworkflows  
 Erstellen Sie den Einkaufsbestellungs-Genehmigungsworkflow, indem Sie die Schritte aus der Vorlage Einkaufsbestellungs-Genehmigungsworkflow kopieren. Lassen Sie die vorhandenen Workflowschritte unverändert, und aktivieren Sie dann den Workflow.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>So erstellen und aktivieren Sie einen Einkaufsbestellungs-Genehmigungsworkflow  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion "Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Workflows** ein, und wählen dann den zugehörigen Link aus.  
2.  Auf der Seite **Workflows** wählen Sie die **Workflow aus Vorlage erstellen** Aktion aus.  
3.  Wählen Sie auf der Seite **Workflow-Vorlage** die Worklow-Vorlage "Einkaufsbestellung-Genehmigungsworkflow" aus, und wählen Sie dann die Schaltfläche **OK** aus.  

    Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Einkaufsbestellungs-Freigabe-Workflow-Workflow-Vorlage erstellt wurde.  
5.  Aktivieren Sie im Kopfbereich der **Workflow**-Seite das **Aktiviert**-Kontrollkästchen.  

## <a name="using-the-approval-workflow"></a>Nutzung des Genehmigungsworkflows  
Verwenden Sie den Einkaufsbestellungs-Genehmigungsworkflos, indem Sie sich in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia anmelden (um die Genehmigung einer Einkaufsbestellung anzufordern). Dann melden Sie sich als sie selbst an, rufen die Notiz im Rollencenter auf, folgen der Verknüpfung zur Genehmigungsanforderung, und genehmigen die Genehmigungsanforderung.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>So genehmigen Sie eine Einkaufsbestellung als Christine  
1. Melden Sie sich als Alicia an.
2.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.  
3.  Wählen Sie die Zeile für offene Bestellung 104001 und die **Bearbeiten** Aktion aus.  
4.  Auf der Seite **Bestellung** wählen Sie die **Genehmigungsanforderung senden** Aktion aus.  

Beachten Sie, dass sich der Wert im Feld **Status** zu **Genehmigung ausstehend** ändert.  

### <a name="to-approve-the-purchase-order-as-sean"></a>So genehmigen Sie die Einkaufsbestellung als Stephan  
1. Melden Sie sich als Sean an.
2.  Suchen Sie im Rollencenter auf der Seite **Meine Benachrichtigungen** nach einer neuen Notiz von Christine.  
3.  Wenn die Notiz auf der Seite **Meine Benachrichtigungen** erscheint, wählen Sie den Wert **Genehmigungseintrag: XX, XX** Wert im Feld **Seite** aus. Die Seite **Genehmigung anfordern** wird geöffnet und Alicias Anforderung für die Einkaufsbestellung wird hervorgehoben.  
4.  Auf der Seite **Zu genehmigende Anforderungen** wählen Sie die **Genehmigen** Aktion aus.  

    Der Wert im Feld **Status** auf von Christines Einkaufsbestellung ändert sich zu **Freigegeben**.  

Sie haben jetzt einen einfachen Genehmigungsworkflow auf Grundlage die ersten beiden Schritte der Workflow-Vorlage Einkaufsbestellungs-Genehmigungsworkflow eingerichtet und getestet. Sie können diesen Workflow sehr einfach erweitern, um Christines Einkaufsbestellung automatisch zu buchen, wenn Stephan sie genehmigt. Hierzu müssen Sie den Workflow "Workflow Einkaufsrechnung" aktivieren. In diesem wird eine genehmigte Einkaufsrechnung gebucht. Zuerst müssen Sie die Ereignisbedingung im ersten Workflowschritt aus (Einkauf ) **Rechnung** zu **Auftrag** ändern.  

Die Basisversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere Workflowvorlagen für Szenarien, die durch den Anwendungscode unterstützt werden. Die meisten dieser Worflowvorlagen sind Genehmigungsworkflows.  

Sie definieren Workflowsvariationen, indem Sie die Felder in den Workflowzeilen über vordefinierte vom Anwendungscode unterstützten Listen mit Ereignissen und Reaktionen ausfüllen. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in der Entwickler- und IT-Pro-Hilfe.  

## <a name="see-also"></a>Siehe auch  
[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)   
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
[Erstellen eines Workflows](across-how-to-create-workflows.md)   
[Artikelgenehmigungsworkflow verwenden](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)  
[Business Central  in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md)
