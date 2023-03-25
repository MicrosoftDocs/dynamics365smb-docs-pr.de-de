---
title: Genehmigungsbenutzer einrichten
description: 'Bevor Sie Workflows erstellen können, die Genehmigungsschritte beinhalten, müssen Sie die an den Genehmigungsprozessen beteiligten Workflow-Benutzer auf der Seite „Genehmigungsbenutzereinrichtung“ festlegen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
---
# Genehmigungsbenutzer einrichten

Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind. Auf der Seite **Genehmigungsbenutzereinrichtung** müssen Sie zusätzlich Grenzbeträge für bestimmte Arten von Anforderungen festlegen und Ersatzgenehmiger definieren, an die Genehmigungsanforderungen delegiert werden, wenn der ursprüngliche Genehmiger abwesend ist.  

> [!NOTE]  
> Sowohl Genehmigungsanforderer als auch Genehmiger müssen zunächst als **Workflowbenutzergruppe** auf der Seite eingerichtet werden. Erfahren Sie mehr unter [Workflowbenutzer einrichten](across-how-to-set-up-workflow-users.md).  

Wenn Sie Genehmigungsbenutzer eingerichtet haben, können Sie über diese Konfiguration Workflowantworten für Genehmigungsworkflows erstellen. Erfahren Sie mehr ab Schritt 9 unter [Erstellen Sie Genehmigungsworkflows](across-how-to-create-workflows.md).  

> [!NOTE]  
> Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Benutzer diese genehmigt haben, richten Sie Genehmiger in einer Hierarchie ein. Für Genehmigungstypen **Genehmiger** richten Sie auf der Seite **Genehmigungsbenutzereinrichtung** einen Genehmiger ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen**-Fenster fest, und definiert Sie die Hierarchie, indem Sie ansteigende Nummern zu jedem Genehmiger im Feld **Sequenznummer** zuweisen. Feld Erfahren Sie mehr unter [Workflowbenutzer einrichten](across-how-to-set-up-workflow-users.md).  

## So richten Sie einen Genehmigungsbenutzer ein

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Genehmigungsbenutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie auf der Seite **Genehmigungsbenutzereinrichtung** eine neue Zeile, und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

   |Feld|Description|
   |-----|-----------|
   |**Benutzer-ID**|Wählen Sie die ID der Person aus, die am Genehmigungsvorgang beteiligt ist.|
   |**Verk.-/Einkäufercode**|Geben Sie den Verkäufer- oder Einkäufercode für den Benutzer an.<br /><br /> In der Regel füllen Sie das Feld **Verk.-/Einkäufercode** aus, wenn der für den Debitor oder Kreditor zuständige Verkäufer oder Einkäufer derjenige ist, der die entsprechende Verkaufs- oder Einkaufsanforderung genehmigen muss.|
   |**Genehmiger-ID**|Wählen Sie die ID der Person aus, die den Anforderungen vom identifizierten Benutzer im Feld **Benutzer-ID** genehmigen muss.|
   |**Grenzbetrag für Verkauf**|Geben Sie den maximalen Verkaufsbetrag in der lokalen Währung (LCY) im Feld **Benutzer-ID** an, die der Benutzer genehmigen kann.|
   |**Unbegrenzte Verkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Vertriebsanforderungen unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Verkaufsbetrag-Genehmigungslimite** nicht ausfüllen.|
   |**Grenzbetrag für Einkauf**|Geben Sie den maximalen Einkaufsetrag in LCY an, die der Benutzer im Feld **Benutzer-ID** für Einkaufsanfragen genehmigen kann.|
   |**Unbegrenzte Einkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Kaufanforderungen unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Einkaufsbetrag-Genehmigungslimit** nicht ausfüllen.|
   |**Grenzbetrag für Anfrageanforderung**|Geben Sie den maximalen Betrag in LCY an, die der Benutzer im Feld **Benutzer-ID** für Einkaufsanfragen genehmigen kann.<br /><br /> Um dieses Feld verwenden zu können, müssen Sie die Option **Genehmigerkette** im Feld **Genehmigerlimitentpy** auf der Seite **Workflowreaktion** auswählen.|
   |**Unbegrenzte Anfragegenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Kaufangebote unabhängig von dem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Anforderungsbetrag-Genehmigungslimite anfordern** nicht ausfüllen.|
   |**Stellvertreter**|Wählen Sie die ID des Benutzers aus, der Anforderungen vom Benutzer im Feld **Benutzer-ID** genehmigen muss, wenn der Benutzer unter **Genehmiger-ID** nicht verfügbar ist. <br /><br />**Hinweis:**  Der Ersatz kann entweder der Benutzer im Feld **Stellvertreter**, der direkten Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). Erfahren Sie mehr unter [Genehmigungsworkflows verwenden](across-how-use-approval-workflows.md).|
   |**E-Mail**|Geben Sie die E-Mail-Adresse der Person im Feld **Benutzer-ID** an.|
   |**Genehmigungsadministrator**|Geben Sie den Benutzer an, der berechtigt ist, gesperrte Genehmigungsworkflows freizugeben, beispielsweise durch das Delegieren von Genehmigungsanforderungen an neue Ersatzgenehmiger oder das Löschen von fälligen Genehmigungsanforderungen.|

   > [!NOTE]
   > Nur eine Person kann der Genehmigungsadministrator sein.|

3. Wählen Sie zum Testen der Genehmigungsbenutzereinrichtung die Aktion **Genehmigungsbenutzereinrichtung - Test** aus.  
4. Wiederholen Sie die Schritte 2 und 3 für jede Person, die Sie als Genehmigungsbenutzer einrichten möchten.  

## Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## Siehe auch

[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
