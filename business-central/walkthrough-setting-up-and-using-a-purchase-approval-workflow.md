---
title: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows | Microsoft Docs
description: Sie können den Genehmigungsprozesses für neuen oder geänderten Datensätze, z. B. Dokumente, Buch.-Blattzeilen und Debitorenkarten automatisieren, indem Sie Workflows mit Schritten für die entsprechenden Genehmigungen erstellen. Bevor Sie Genehmigungsworkflows erstellen, müssen Sie einen Genehmiger und einen Stellvertreter für jeden Genehmigungsbenutzer einrichten. Sie können außerdem Grenzbeträge für die Genehmiger festlegen, um zu definieren, für welche Verkaufs- und Einkaufsdatensätze sie für eine Genehmigung qualifiziert sind. Genehmigungsanforderungen und andere Benachrichtigungen können als E-Mail oder interne Notiz gesendet werden. Für jede Genehmigungsbenutzereinrichtung können Sie angeben wann dieser Benachrichtigungen erhält.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 74f8d9dcb309581681e6161a12e7e52fac066726
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193371"
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

## <a name="story"></a>Hintergrund  
Stephan ist ein Superuser bei CRONUS. Er erstellt zwei Genehmigungsbenutzer. Der eine ist Christine, die einen Einkäufer darstellt. Der andere ist er selbst. Er ist der Genehmiger für Christine. Stephan gibt sich selbst unbegrenzten Rechte zur Genehmigung und legt fest, dass er Benachrichtigungen über eine interne Notiz bei einem entsprechendes Ereignis erhält. Als letztes erstellt erstellt Stephan den erforderlichen Genehmigungsworkflow als Kopie der vorhandenen Workflow-Vorlage "Workflow Einkaufsbestellungsgenehmigung". Er übernimmt alle Ereignisbedingungen unverändert und aktiviert dann den Workflow.  

Um den Genehmigungsworkflow zu testen, meldet sich Sean zunächst bei [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia an und beantragt dann die Genehmigung einer Bestellung. Sean meldet sich dann selbst an, sieht die Notiz auf seinem Rollencenter, folgt dem Link zur Genehmigungsanforderung für die Bestellung und genehmigt die Anforderung.  

## <a name="setting-up-sample-data"></a>Einrichten der Beispieldaten
Bevor Sie Genehmigungsbenutzer und deren Benachrichtigungsmethode einrichten können, müssen Sie sicherstellen, dass zwei Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)]: vorhanden sind. Ein Benutzer stellt Christine dar. Die andere Benutzer, Sie, stellt Stephan dar. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Einrichten von Genehmigungsbenutzern  
Wenn Sie sich als Sie selbst angemeldet haben, richten Sie Alicia als Genehmigungsbenutzer ein, dessen Genehmigender Sie selbst sind. Richten Sie Ihre Genehmigungsrechte ein, und geben Sie an, wie und wann Sie über Genehmigungsanforderungen benachrichtigt werden.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>So richten Sie sich selbst und Christine als Genehmigungsbenutzer ein  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Genehmigungsbenutzereinrichtung** ein und wählen Sie dann den entsprechenden Link.  
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
7.  Wählen Sie auf der Seite **Benachrichtigungsplan** im Feld **Wiederholung** **Sofort**.  

## <a name="creating-the-approval-workflow"></a>Erstellen des Genehmigungsworkflows  
 Erstellen Sie den Einkaufsbestellungs-Genehmigungsworkflow, indem Sie die Schritte aus der Vorlage Einkaufsbestellungs-Genehmigungsworkflow kopieren. Lassen Sie die vorhandenen Workflowschritte unverändert, und aktivieren Sie dann den Workflow.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>So erstellen und aktivieren Sie einen Einkaufsbestellungs-Genehmigungsworkflow  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **Workflows** die Aktion **Neuer Workflow aus Vorlage**.  
3.  Wählen Sie auf der Seite **Workflow-Vorlage** die Worklow-Vorlage "Einkaufsbestellung-Genehmigungsworkflow" aus, und wählen Sie dann die Schaltfläche **OK** aus.  

    Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Einkaufsbestellungs-Freigabe-Workflow-Workflow-Vorlage erstellt wurde.  
5.  Aktivieren Sie im Kopfbereich der **Workflow**-Seite das **Aktiviert**-Kontrollkästchen.  

## <a name="using-the-approval-workflow"></a>Nutzung des Genehmigungsworkflows  
Verwenden Sie den neuen Workflow zur Genehmigung von Bestellungen, indem Sie sich zuerst bei [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia anmelden, um die Genehmigung einer Bestellung zu beantragen. Melden Sie sich dann als Sie selbst an, lesen Sie die Notiz im Rollencenter, folgen Sie dem Link zur Genehmigungsanfrage und genehmigen Sie die Anfrage.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>So genehmigen Sie eine Einkaufsbestellung als Christine  
1. Melden Sie sich als Alicia an.
2.  Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.  
3.  Wählen Sie die Zeile für offene Bestellung 106001 und die **Bearbeiten** Aktion aus.  
4.  Auf der Seite **Bestellung** wählen Sie die **Genehmigungsanforderung senden** Aktion aus.  

Beachten Sie, dass sich der Wert im Feld **Status** zu **Genehmigung ausstehend** ändert.  

### <a name="to-approve-the-purchase-order-as-sean"></a>So genehmigen Sie die Einkaufsbestellung als Stephan  
1. Melden Sie sich als Sean an.
2. Wählen Sie im Rollencenter im Bereich **Self Service** die Option **Anfragen zur Genehmigung**.
3. Markieren Sie auf der Seite **Anfragen zur Genehmigung** die Zeile über die Bestellung von Alicia und wählen Sie dann die Aktion **Genehmigen**.  

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
[Business Central in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md)
