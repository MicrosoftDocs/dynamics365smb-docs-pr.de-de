---
title: Genehmigungsbenutzer einrichten
description: Bevor Sie Workflows erstellen können, die Genehmigungsschritte beinhalten, müssen Sie die an den Genehmigungsprozessen beteiligten Workflow-Benutzer auf der Seite „Genehmigungsbenutzereinrichtung“ festlegen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 464212d90ba43648bcb5d2852f5d3fec0c23ca41
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530783"
---
# <a name="set-up-approval-users"></a>Genehmigungsbenutzer einrichten

Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind. Auf der Seite **Genehmigungsbenutzereinrichtung** müssen Sie zusätzlich Grenzbeträge für bestimmte Arten von Anforderungen festlegen und Ersatzgenehmiger definieren, an die Genehmigungsanforderungen delegiert werden, wenn der ursprüngliche Genehmiger abwesend ist.  

> [!NOTE]  
> Genehmigungsbenutzer (sowohl Genehmigungsanforderer als auch Genehmiger) müssen zunächst als **Workflowbenutzergruppe** auf der Seite eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten von Workflows-Benutzern](across-how-to-set-up-workflow-users.md).  

 Wenn Sie Genehmigungsbenutzer eingerichtet haben, können Sie über diese Konfiguration Workflowantworten für Genehmigungsworkflows erstellen. Weitere Informationen finden Sie unter Schritt 9 unter [Erstellen von Workflows](across-how-to-create-workflows.md).  

> [!NOTE]  
> Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Genehmiger in einer Genehmigungskette diese genehmigt haben, richten Sie Genehmiger in einer Hierarchie ein. Für Genehmigungstypen **Genehmiger** richten Sie auf der Seite **Genehmigungsbenutzereinrichtung** einen Genehmiger ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen**-Fenster fest, und definiert Sie die Hierarchie, indem Sie ansteigende Nummern zu jedem Genehmiger im Feld **Sequenznummer** zuweisen. Feld Weitere Informationen finden Sie unter [Workflowö-Benutzer einrichten](across-how-to-set-up-workflow-users.md) und in diesem Thema.  

## <a name="to-set-up-an-approval-user"></a>So richten Sie einen Genehmigungsbenutzer ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Genehmigungsbenutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie auf der Seite **Genehmigungsbenutzereinrichtung** eine neue Zeile, und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Benutzer-ID**|Wählen Sie die ID des Benutzers aus, der am Genehmigungsvorgang beteiligt ist.|  
    |**Verk.-/Einkäufercode**|Geben Sie den Verkäufer- oder Einkäufercode für den Benutzer im Feld **Verk.-/Einkäufercode** an.<br /><br /> In der Regel füllen Sie das Feld **Verk.-/Einkäufercode** aus, wenn der für den Debitor oder Kreditor zuständige Verkäufer oder Einkäufer derjenige ist, der die entsprechende Verkaufs- oder Einkaufsanforderung genehmigen muss.|  
    |**Genehmiger-ID**|Wählen Sie die ID des Benutzers aus, der Anforderungen vom Benutzer im Feld **Benutzer-ID** genehmigen muss.|  
    |**Grenzbetrag für Verkauf**|Geben Sie den maximalen Verkaufsbetrag in der Mandantenwährung (MW) im Feld **Benutzer-ID** an, die der Benutzer genehmigen kann.|  
    |**Unbegrenzte Verkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Vertriebsanforderungen unabhängig von ihrem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Verkaufsbetrag-Genehmigungslimite** nicht ausfüllen.|  
    |**Grenzbetrag für Einkauf**|Geben Sie den maximalen Einkaufsbetrag in der Mandantenwährung (MW) im Feld **Benutzer-ID** an, die der Benutzer genehmigen kann.|  
    |**Unbegrenzte Einkaufsgenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Einkaufsanforderungen unabhängig von ihrem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Verkaufsbetrag-Genehmigungslimite** nicht ausfüllen.|  
    |**Grenzbetrag für Anfrageanforderung**|Geben Sie den maximalen Betrag in der Mandantenwährung an, die der Benutzer im Feld **Benutzer-ID** für Einkaufsanfragen genehmigen kann.<br /><br /> Um dieses Feld verwenden zu können, müssen Sie die Option **Genehmigerkette** im Feld **Genehmigerlimitentpy** auf der Seite **Workflowreaktion** auswählen.|  
    |**Unbegrenzte Anfragegenehmigung**|Geben Sie an, dass der Benutzer im Feld **Benutzer-ID** alle Einkaufsangebote unabhängig von ihrem Betrag genehmigen kann.<br /><br /> Wenn Sie dieses Kontrollkästchen aktivieren, können Sie das Feld **Verkaufsbetrag-Genehmigungslimite anfordern** nicht ausfüllen.|  
    |**Stellvertreter**|Wählen Sie die ID des Benutzers aus, der Anforderungen vom Benutzer im Feld **Benutzer-ID** genehmigen muss, wenn der Benutzer unter **Genehmiger-ID** nicht verfügbar ist. <br /><br />**Hinweis:**  Der Ersatz kann entweder der Benutzer im Feld **Stellvertreter**, der direkten Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).|  
    |**E-Mail**|Geben Sie die E-Mail-Adresse des Benutzers im Feld **Benutzer-ID** an.|  
    |**Genehmigungsadministrator**|Geben Sie den Benutzer an, der über Rechte zum Entsperren des Genehmigungsworkflows verfügt. Beispielsweise durch das Delegieren von Genehmigungsanforderungen an neue Ersatzgenehmiger und das Löschen von fälligen Genehmigungsanforderungen.|

    > [!Note]
    > Nur eine Person kann der Genehmigungsadministrator sein.|

3. Wählen Sie zum Testen der Genehmigungsbenutzereinrichtung die Aktion **Genehmigungsbenutzereinrichtung - Test** aus.  
4. Wiederholen Sie die Schritte 2 und 3 für jeden Benutzer, den Sie als Genehmigungsbenutzer einrichten möchten.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Erstellen eines Workflows](across-how-to-create-workflows.md)  
[Einrichten von Workflows](across-set-up-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
