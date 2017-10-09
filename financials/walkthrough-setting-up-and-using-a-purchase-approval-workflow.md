---
title: 'Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows | Microsoft Docs'
description: "Sie können den Genehmigungsprozesses für neuen oder geänderten Datensätze, z. B. Dokumente, Buch.-Blattzeilen und Debitorenkarten automatisieren, indem Sie Workflows mit Schritten für die entsprechenden Genehmigungen erstellen. Bevor Sie Genehmigungsworkflows erstellen, müssen Sie einen Genehmiger und einen Stellvertreter für jeden Genehmigungsbenutzer einrichten. Sie können außerdem Grenzbeträge für die Genehmiger festlegen, um zu definieren, für welche Verkaufs- und Einkaufsdatensätze sie für eine Genehmigung qualifiziert sind. Genehmigungsanforderungen und andere Benachrichtigungen können als E-Mail oder interne Notiz gesendet werden. Für jede Genehmigungsbenutzereinrichtung können Sie angeben wann dieser Benachrichtigungen erhält."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09d48e230291524e7771d4b4305c4290bd567eb9
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows
Sie können den Genehmigungsprozesses für neuen oder geänderten Datensätze, z. B. Dokumente, Buch.-Blattzeilen und Debitorenkarten automatisieren, indem Sie Workflows mit Schritten für die entsprechenden Genehmigungen erstellen. Bevor Sie Genehmigungsworkflows erstellen, müssen Sie einen Genehmiger und einen Stellvertreter für jeden Genehmigungsbenutzer einrichten. Sie können außerdem Grenzbeträge für die Genehmiger festlegen, um zu definieren, für welche Verkaufs- und Einkaufsdatensätze sie für eine Genehmigung qualifiziert sind. Genehmigungsanforderungen und andere Benachrichtigungen können als E-Mail oder interne Notiz gesendet werden. Für jede Genehmigungsbenutzereinrichtung können Sie angeben wann dieser Benachrichtigungen erhält.  

 Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Einrichtung der Genehmigungsbenutzer (einschließlich Einrichten eines Benutzers in Windows und in [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Benachrichtigungen für Genehmigungsbenutzer einrichten.  
-   Den Genehmigungsworkflow ändern und aktivierend.  
-   Die Aufgabenwarteschlange zur Verteilung von Benachrichtigungen starten.  
-   Die Genehmigung einer Einkaufsbestellung als Christine.  
-   Empfangen einer Benachrichtigung und Genehmigung als Stephan.  

## <a name="prerequisites"></a>Voraussetzungen  
Um diese Demonstration abzuschließen, benötigen Sie den CRONUS International Ltd.- Demomandanten.

## <a name="story"></a>Hintergrund  
Sean ist einem Superuser bei CRONUS auf seinem eigenen Computer.  

Er erstellt zwei Genehmigungsbenutzer. Der eine ist Christine, die einen Einkäufer darstellt. Der andere ist er selbst. Er ist der Genehmiger für Christine. Stephan gibt sich selbst unbegrenzten Rechte zur Genehmigung und legt fest, dass er Benachrichtigungen über eine interne Notiz bei einem entsprechendes Ereignis erhält. Als letztes erstellt erstellt Stephan den erforderlichen Genehmigungsworkflow als Kopie der vorhandenen Workflow-Vorlage "Workflow Einkaufsbestellungsgenehmigung". Er übernimmt alle Ereignisbedingungen unverändert und aktiviert dann den Workflow.  

Um den Genehmigungsworkflow zu testen, meldet sich Sean in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia an, und fordert dann die Genehmigung einer Einkaufsbestellung an. Dann meldet sich Stephan als er selbst an, sieht die Notiz in seinem Rollencenter, folgt der Verknüpfung zur Genehmigungsanforderung für die Einkaufsbestellung, und genehmigt die Anforderung.  

## <a name="setting-up-the-sample-data"></a>Einrichten der Beispieldaten  
Sie müssen einen neuen Benutzer auf dem lokalen Computer und in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, der Alicia darstellt. Diesen Benutzer verwenden Sie später als Genehmigungsbenutzer. Ihr eigenes Benutzerkonto stellt Stephan dar.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>So fügen Sie Christine als Benutzer auf dem lokalen Computer hinzu  

1.  Wählen Sie **Start**. Dann geben Sie im Feld **Programme/Dateien durchsuchen** den Text **Lokale Benutzer und Gruppen bearbeiten** ein, und wählen anschließend den zugehörigen Link aus.  
2.  Öffnen Sie den Ordner **Benutzer**.  
3.  Wählen Sie auf der Registerkarte **Aktionen** die Option **Neuer Benutzer** aus.  
4.  Geben Sie im Feld **Benutzername** den Text "Christine" ein.  
5.  Geben Sie in den Feldern **Kennwort** und **Kennwort bestätigen** ein gültiges Kennwort ein.  
6.  Deaktivieren Sie das Kontrollkästchen **Benutzer muss Kennwort bei der nächsten Anmeldung ändern**.  
7.  Schließen Sie das **Lokale Benutzer und Gruppen**-Fenster.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>So fügen Sie Alicia als Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzu  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.  
2.  Klicken Sie im Fenster **Windows Benutzher** auf der Registerkarte **Start** in der Gruppe **Neu** auf **Neu**.  
3.  Im Fenster **Benutzerkarte** im Feld **Benutzername**, geben Sie Alicia ein.  
4.  Wählen Sie im Feld **Windows Benutzername** die Schaltfläche AssistEdit, um das Fenster  zu öffnen.  
5.  Geben Sie im Fels **Auszuwählenden Objektnamen eingeben** im Fenster **Benutzer oder Gruppen auswählen** "Christine" ein und wählen Sie dann die Schaltfläche **Namen prüfen** aus.  
6.  Wenn [COMPUTERNAMW]\ALICIA im Feld erscheint, wählen Sie die Schaltfläche **OK**.  
7.  Geben Sie auf dem **Benutzerberechtigungssätze** Inforegister im Feld **Berechtigungssätze** die Option **SUPER** aus.  
8.  Wählen Sie im Feld **Mandant** die Option **CRONUS AG**.  
9. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="setting-up-approval-users"></a>Einrichten von Genehmigungsbenutzern  
Nutzen Sie den soeben erstellten Windows-Benutzer, um Christine als Genehmigungsbenutzer einzurichten, dessen Genehmiger Sie selbst sind. Richten Sie Ihre Genehmigungsrechte ein, und geben Sie an, wie und wann Sie über Genehmigungsanforderungen benachrichtigt werden.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>So richten Sie sich selbst und Christine als Genehmigungsbenutzer ein  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Genehmigungsbenutzereinrichtung** ein und wählen dann den zugehörigen Link aus.  
2.  Klicken Sie im Fenster **Genehmigungsbenutzereinrichtung** auf der Registerkarte **Start** in der Gruppe **Neu** auf **Neu**.  

    > [!NOTE]  
    >  Sie müssen einen Genehmiger einrichten, bevor Sie Benutzer einrichten können, die die Genehmigung dieses Genehmigers benötigen. Sie müssen sich selbst Einrichten, bevor Sie Christine einrichten.  

3.  Richten Sie zwei Genehmigungsbenutzer ein, indem Sie die Felder aus der folgenden Tabelle ausfüllen.  

    |Benutzer ID|Genehmiger-ID|Unbegrenzte Einkaufsgenehmigung|  
    |-------------|-----------------|---------------------------------|  
    |[COMPUTERNAME]\[SIE]||Ausgewählt|  
    |[COMPUTERNAME]\ALICIA|[COMPUTERNAME]\[SIE]||  

## <a name="setting-up-notifications"></a>Einrichten von Benachrichtigungen  
Geben Sie an, wie und wann Sie über Genehmigungsanforderungen benachrichtigt werden.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>So legen Sie fest, wie und wann Sie benachrichtigt werden  
1.  Im Fenster **Genehmigungsbenutzereinrichtung** wählen Sie die Zeile für sich aus, und wählen Sie anschließend auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Benachrichtigungseinrichtung** aus.  
2.  Im Fenster **Benachrichtigungseinrichtung** im Feld **Benachrichtigungstyp**, geben Sie **Genehmigung** ein.  
3.  Wählen Sie im **Benachrichtigungsvorlagen-Code**-Feld und wählen Sie dann **Erweitert** aus.  
4.  Wählen Sie im Fenster **Benachrichtigungsvorlage** auf der Registerkarte **Start**in der Gruppe **Verwalten** die Option **Liste bearbeiten** aus.  
5.  Geben Sie in der Zeile für die Genehmigungsvorlage im **Benachrichtigungsmethode-**Feld **Notiz** ein.  
6.  Wählen Sie die Schaltfläche **OK** aus.  
7.  Wählen Sie im Fenster **Benachrichtigung einrichten** auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Benachrichtungsplan** aus.  
8.  Wählen Sie im **Benachrichtigungsplan**-Fenster im Feld **Vorkommen** die Option **Sofort** aus.  
9. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="creating-the-approval-workflow"></a>Erstellen des Genehmigungsworkflows  
 Erstellen Sie den Einkaufsbestellungs-Genehmigungsworkflow, indem Sie die Schritte aus der Vorlage Einkaufsbestellungs-Genehmigungsworkflow kopieren. Lassen Sie die vorhandenen Workflowschritte unverändert, und aktivieren Sie dann den Workflow.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>So erstellen und aktivieren Sie einen Einkaufsbestellungs-Genehmigungsworkflow  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Workflow** auf der Registerkarte **Aktionen** in der Gruppe **Allgemein** die Option **Workflow aus Vorlage** erstellen aus.  
3.  Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Allgemein** die Option **Workflow aus Vorlage erstellen** aus. Das Fenster **Workflowvorlagen** wird geöffnet.  
4.  Wählen Sie die Zeile für die Workflow-Vorlage "Einkaufsbestellung-Genehmigungsworkflow" aus, und wählen Sie dann die Schaltfläche **OK**.  

    Das Fenster **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Einkaufsbestellungs-Freigabe-Workflow-Workflow-Vorlage erstellt wurde.  
5.  Aktivieren Sie im Kopfbereich des **Workflow**-Fensters das **Aktiviert**-Kontrollkästchen.  

## <a name="starting-a-notification-job-queue"></a>Starten einer Aufgabenwarteschlange für Benachrichtungen  
Stellen Sie sicher, dass die Aufgabenwarteschlange in Ihrer Installation so eingerichtet wurde, dass Workflowbenachrichtigungen verarbeitet werden.  

### <a name="to-start-the-notify-job-queue"></a>So starten Sie die Aufgabenwarteschlange für Benachrichtungen  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen]Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Projektwarteschlange** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Im Fenster **Projektwarteschlange** wählen Sie die Zeile für die Aufgabenwarteschlange BENACHR. aus, und wählen anschließend auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Aufgabenwarteschlange** starten aus.  

## <a name="using-the-approval-workflow"></a>Nutzung des Genehmigungsworkflows  
Verwenden Sie den Einkaufsbestellungs-Genehmigungsworkflos, indem Sie sich in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia anmelden (um die Genehmigung einer Einkaufsbestellung anzufordern). Dann melden Sie sich als sie selbst an, rufen die Notiz im Rollencenter auf, folgen der Verknüpfung zur Genehmigungsanforderung, und genehmigen die Genehmigungsanforderung.  

Um sich in [!INCLUDE[d365fin](includes/d365fin_md.md)] als anderer Benutzer anzumelden nutzen Sie die Funktion **Als anderer Benutzern ausführen**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>So melden Sie sich in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia an  

1.  Um den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Web-Client zu starten klicken Sie bei gedrückter Umschalttaste mit rechts auf das Symbol zum Starten des Browsers oder die Verknüpfung zur Webseite. Wählen Sie dann **Als anderer Benutzer ausführen** aus.  

    Um den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Windows-Client zu starten klicken Sie bei gedrückter Umschalttaste mit rechts auf das Symbol zum Starten des Browsers oder die Verknüpfung zum Programm. Wählen Sie dann **Als anderer Benutzer ausführen** aus.  

2.  In **Windows-Sicherheit**-Fenster geben Sie [COMPUTERNAME]\ALICIA und das erforderliche Kennwort ein.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>So genehmigen Sie eine Einkaufsbestellung als Christine  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Aufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Zeile zum öffnen der Einkaufsbestellung 104001 aus. Wählen Sie dann auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.  
3.  Wählen Sie im **Kaufauftrag**Fenster  auf der Registerkarte **Aktionen** in der Gruppe **Genehmigung** die **Genehmigungsanforderung senden-Option** aus.  

    Beachten Sie, dass sich der Wert im Feld **Status** zu **Genehmigung ausstehend** ändert.  

4.  Schließen[!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>So genehmigen Sie die Einkaufsbestellung als Stephan  

1.  Öffnen Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] ganz normal. Die Anwendung wird mit Ihnen als Benutzer geöffnet.  
2.  Suchen Sie im Rollencenter in Fenster **Meine Benachrichtigungen** nach einer neuen Notiz von Christine.  

    > [!NOTE]  
    >  Obwohl die Benachrichtigungswiederholung auf **Sofort** definiert ist, kommt die Notiz erst ungefähr eine Minute nachdem Christine sie gesendet hat an. Dieses liegt an der Standard-Wiederholungsfrequenz der Aufgabenwarteschlange.  

3.  Wenn die Notiz im Fenster **Meine Benachrichtigungen** erscheint, wählen Sie den Wert **Genehmigungseintrag: XX, XX** Wert im Feld **Seite** aus. Das -Fenster **Genehmigung anfordern**wird geöffnet und Alicias Anforderung für die Einkaufsbestellung wird hervorgehoben.  
4.  Wählen Sie im Fenster **Genehmigung anfordern** auf der Registerkarte **Start**in der Gruppe **Vorgang** die Option **Genehmigen** aus.  

    Der Wert im Feld **Status** auf von Christines Einkaufsbestellung ändert sich zu **Freigegeben**.  

Sie haben jetzt einen einfachen Genehmigungsworkflow auf Grundlage die ersten beiden Schritte der Workflow-Vorlage Einkaufsbestellungs-Genehmigungsworkflow eingerichtet und getestet. Sie können diesen Workflow sehr einfach erweitern, um Christines Einkaufsbestellung automatisch zu buchen, wenn Stephan sie genehmigt. Hierzu müssen Sie den Workflow "Workflow Einkaufsrechnung" aktivieren. In diesem wird eine genehmigte Einkaufsrechnung gebucht. Zuerst müssen Sie die Ereignisbedingung im ersten Workflowschritt aus (Einkauf ) **Rechnung** zu **Auftrag** ändern.  

Die Basisversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere Workflowvorlagen für Szenarien, die durch den Anwendungscode unterstützt werden. Die meisten dieser Worflowvorlagen sind Genehmigungsworkflows. Weitere Informationen finden Sie unter Workflow Vorlagen  

Sie definieren Workflowsvariationen, indem Sie die Felder in den Workflowzeilen über vordefinierte vom Anwendungscode unterstützten Listen mit Ereignissen und Reaktionen ausfüllen. Weitere Informationen finden Sie unter [Gewusst wie: Workflows erstellen](across-how-to-create-workflows.md).  

Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](https://msdn.microsoft.com/en-us/library/mt574349.aspx) in MSDN  

## <a name="see-also"></a>Siehe auch  
[Gewusst wie: Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)   
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
[So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md)   
[Gewusst wie. Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)

