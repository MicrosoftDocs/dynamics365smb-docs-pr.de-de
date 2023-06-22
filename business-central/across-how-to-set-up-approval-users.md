---
title: Genehmigungsbenutzer einrichten
description: 'Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-approval-users" />Genehmigungsbenutzer einrichten

Bevor Sie Workflows erstellen können, die Genehmigungsschritte beinhalten, müssen Sie die an den Genehmigungsprozessen beteiligten Benutzer auf der Seite **Genehmigungsbenutzereinrichtung** festlegen. Sie können außerdem Betragsgrenzen für verschiedene Arten von Anforderungen festlegen, Ersatzgenehmiger definieren und Benachrichtigungen einrichten.  

Nachdem Sie Genehmigungsbenutzer eingerichtet haben, können Sie über diese Konfiguration Workflowantworten für Genehmigungsworkflows erstellen. Erfahren Sie mehr unter [Genehmigungsworkflows erstellen](across-how-to-create-workflows.md).  

> [!TIP]
> Sie können verlangen, dass mehrere Genehmiger auf eine Genehmigungsanfrage reagieren, indem Sie auf der Seite **Workflow-Benutzergruppe** eine Gruppe von Genehmigern erstellen. Erfahren Sie mehr unter [Workflow-Benutzergruppen einrichten](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user" />So richten Sie einen Genehmigungsbenutzer ein

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Genehmigungsbenutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie auf der Seite **Genehmigungsbenutzereinrichtung** eine neue Zeile, und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

   |Feld|Description|
   |-----|-----------|
   |**Benutzer-ID**|Wählen Sie die ID der Person aus, die am Genehmigungsvorgang beteiligt ist.|
   |**Verk.-/Einkäufercode**|Geben Sie den Verkäufer- oder Einkäufercode für den Benutzer an.<br /><br /> In der Regel füllen Sie das Feld **Verk.-/Einkäufercode** aus, wenn der für den Debitor oder Kreditor zuständige Verkäufer oder Einkäufer derjenige ist, der eine Verkaufs- oder Einkaufsanforderung genehmigen muss.|
   |**Genehmiger-ID**|Wählen Sie die Benutzer-ID der Person aus, die den Anforderungen von dem von Ihnen angegebenen Benutzer im Feld **Benutzer-ID** genehmigen muss.|
   |**Grenzbetrag für Verkauf**|Geben Sie den maximalen Verkaufsbetrag in der lokalen Währung (LW) im Feld **Benutzer-ID** an, die der ausgewählte Benutzer genehmigen kann.|
   |**Unbegrenzte Verkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Vertriebsanforderungen unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Verkaufsbetrag-Genehmigungslimite** nicht ausfüllen.|
   |**Grenzbetrag für Einkauf**|Geben Sie den maximalen Einkaufsetrag in LCY an, die der Benutzer im Feld **Benutzer-ID** für Einkaufsanfragen genehmigen kann.|
   |**Unbegrenzte Einkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Kaufanforderungen unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Einkaufsbetrag-Genehmigungslimit** nicht ausfüllen.|
   |**Grenzbetrag für Anfrageanforderung**|Geben Sie den maximalen Betrag in LCY an, die der Benutzer im Feld **Benutzer-ID** für Einkaufsanfragen genehmigen kann.<br /><br /> Um dieses Feld verwenden zu können, müssen Sie die Option **Genehmigerkette** im Feld **Genehmigerlimitentpy** auf der Seite **Workflowreaktion** auswählen.|
   |**Unbegrenzte Anfragegenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Kaufangebote unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Anforderungsbetrag-Genehmigungslimite anfordern** nicht ausfüllen.|
   |**Stellvertreter**|Wählen Sie die ID des Benutzers aus, der Anforderungen vom Benutzer im Feld **Benutzer-ID** genehmigen muss, wenn der Benutzer unter **Genehmiger-ID** nicht verfügbar ist. <br /><br />**Hinweis:**  Der Ersatz kann entweder der Benutzer im Feld **Stellvertreter**, der direkten Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). Erfahren Sie mehr unter [Genehmigungsworkflows verwenden](across-how-use-approval-workflows.md).|
   |**E-Mail**|Geben Sie die E-Mail-Adresse der Person im Feld **Benutzer-ID** an.|
   |**Genehmigungsadministrator**|Geben Sie den Benutzer an, der berechtigt ist, gesperrte Genehmigungsworkflows freizugeben, beispielsweise durch das Delegieren von Genehmigungsanforderungen an neue Ersatzgenehmiger oder das Löschen von fälligen Genehmigungsanforderungen.<br /><br />**Hinweis** Nur eine Person kann der Genehmigungsadministrator sein.|

3. Wählen Sie zum Testen der Genehmigungsbenutzereinrichtung die Aktion **Genehmigungsbenutzereinrichtung - Test** aus.  
4. Wiederholen Sie die Schritte 2 und 3 für jede Person, die Sie als Genehmigungsbenutzer einrichten möchten.  

Im nächsten Schritt legen Sie fest, wie [!INCLUDE [prod_short](includes/prod_short.md)] die Benutzer darüber benachrichtigen soll, dass eine Anforderung auf ihre Bearbeitung wartet. Weitere Informationen erhalten Sie unter [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also" />Siehe auch

[Workflowbenutzer einrichten](across-how-to-set-up-workflow-users.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
