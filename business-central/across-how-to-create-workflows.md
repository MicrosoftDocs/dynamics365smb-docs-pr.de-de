---
title: Erstellen von Workflows | Microsoft Docs
description: Sie können Workflows einrichten, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: 0589314914b2f7982c52b62475d41754845a48d5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881192"
---
# <a name="create-workflows"></a>Erstellen eines Workflows
Sie können Workflows einrichten, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer Workflowantwort mit Antwortoptionen. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

Wenn Sie Workflows erstellen, können Sie die Schritte aus bestehenden Workflows oder aus Workflowvorlagen kopieren. Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden. Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS“ vorangestellt, z. B. „MS-PIW“. Weitere Informationen finden Sie unter [Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).  

Wenn Ihr Szenario Workflowereignisse oder -antworten benötigt, die nicht unterstützt werden, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst.  

> [!NOTE]  
>  Alle Benachrichtigungen über Workflowschritte werden über eine Aufgabenwarteschlange gesendet. Stellen Sie sicher, dass die Aufgabenwarteschlange in Ihrer Installation so eingerichtet wurde, dass Workflowbenachrichtigungen empfangen werden. Das Kontrollkästchen **Automatisch von NAS starten** muss aktiviert sein. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)  

## <a name="to-create-a-workflow"></a>So erstellen Sie einen Workflow  
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Workflows** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow** wird geöffnet.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Um den Workflow von einer Workflowvorlage zu erstellen, wählen Sie auf der Seite **Workflows** die Aktion **Workflow von Vorlage erstellen**. Weitere Informationen finden Sie unter [Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).  
5. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
6. Im Feld **Kategorie** legen Sie fest, in welche Kategorie der Workflow gehört.  
7. Geben Sie im Feld **Wenn Ereignis** das Ereignis an, das auftreten muss, um den Workflowschritt zu starten.  

    Wenn Sie das Feld auswählen, wird die Seite **Workflow-Ereignisse** geöffnet, das alle vorhandenen Workflowereignisse zur Auswahl anbietet.  
8. Legen Sie im Feld **Bedingung** eine oder mehrere Bedingungen fest, die erfüllt sein müssen, bevor das Ereignis im Feld **Wenn Ereigniss** auftreten kann.  

    Wenn Sie das Feld auswählen, wird die **Ereignisbedigungen**-Seite geöffnet. In diesem wählen Sie aus einer Liste mit Filterfeldern die Bedingungen aus, die zum jeweiligen Ereignis relevant sind. Sie können neue Filterfelder hinzufügen, die Sie als Ereignisbedingungen verwenden möchten. Die Ereignisbedingungsfilter konfigurieren Sie so wie die Filter für Berichtsanforderungsseiten.  

    Wenn es sich bei dem Workflowereignis um die Änderung eines bestimmten Felds in einem Datensatz handelt, wird die Seite **Ereignisbedingungen** geöffnet. Dort können Sie Optionen für das Feld und die Art der Änderung auswählen.  

    1.  Um eine Feldänderung für das Ereignis festzulegen, wählen Sie auf der Seite **Ereignisbedingungen** im Feld **Feld** das Feld aus, das sich ändert.  
    2.  Geben Sie im Feld **Operator** entweder **Verringert**, **Erhöht** oder **Geändert** aus.  
9. Geben Sie im Feld **Dann Antwort** die Antwort an, die beim Auftreten des Workflowereignisses folgt.  

     Wenn Sie das Feld auswählen, wird die Seite **Workflow-Antworten** geöffnet, das alle vorhandenen Workflowantworten zur Auswahl anbietet und in dem Sie Antwortoptionen für die gewählte Antwort festlegen können.  
10. Geben Sie im Inforegister **Optionen für die ausgewählte Reaktion** die Optionen für die Workflowantwort an, indem Sie in die folgenden Felder Werte eingeben:  

    1.  Um Optionen für eine Workflowantwort inkl. des Sendens einer Benachrichtigung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld|Beschreibung|  
        |----------------------------------|---------------------------------------|  
        |**Absender benachrichtigen**|Geben Sie an, ob der Genehmigungsanforderer anstatt des Genehmigungsanforderungsempfängers benachrichtigt wird. Wenn Sie das Kontrollkästchen aktivieren, wird das Feld **Benutzer-ID des Empfängers** deaktiviert, da stattdessen der Anforderer der Genehmigung, der Absender, benachrichtigt wird. Der Name der Workflowreaktion ändert sich entsprechend zu **Benachrichtigung erstellen für &lt;Absender&gt;**. Wenn das Kontrollkästchen nicht aktiviert ist, lautet der Name der Workflowreaktion **Benachrichtigung erstellen für &lt;Benutzer&gt;**.
        |**Benutzer-ID des Empfängers**|Geben Sie den Benutzer an, an den Benachrichtigung gesendet werden muss. Hinweis: Diese Option ist nur für Workflowantworten mit einem Platzhalter für einen bestimmten Benutzer verfügbar. Für Workflowantworten ohne Platzhalter für Benutzer, wird der Benachrichtigungsempfänger in der Regel von der Genehmigungsbenutzereinrichtung definiert.|  
        |**Benachrichtigungseintragstyp**|Gibt an, ob die Workflowbenachrichtigung durch eine Datensatzänderung, eine Genehmigungsanforderung oder übergebene fällige Daten ausgelöst wird.|
        |**Zielseite für Link**|Geben Sie eine andere Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] an, die über den Link in der Benachrichtigung anstelle der Standardseite geöffnet werden soll.|  
        |**Benutzerdefinierter Link**|Geben Sie die URL eines Links an, den Sie zusätzlich zu dem Link, der auf die Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] verweist, der Benachrichtigung hinzufügen möchten.|  
    2.  Um Optionen für eine Workflowantwort inkl. des Erstellens von einer Genehmigungsanforderung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld|Description|  
        |----------------------------------|---------------------------------------|  
        |**Fälligkeitsdatumsformel**|Geben Sie an, in wievielen Tagen eine die Genehmigungsanforderung ab dem Datum, an dem sie gesendet wurde, abgeschlossen werden muss.|  
        |**Delegieren nach**|Geben Sie an, ob und wann eine Anforderung für fällige Genehmigung automatisch an den relevanten Stellvertreter delegiert wird. Sie können eine automatische Delegierung ein, zwei oder fünf Tage nach der Anforderung der Genehmigung auswählen.|  
        |**Genehmigertyp**|Geben Sie an, wer gemäß der Einrichtung von Genehmigungsbenutzern und von Workflowbenutzern der Genehmiger ist.<br /><br /> Folgende Optionen sind verfügbar:<br /><br /> -   **Verkäufer/Einkäufer** bedeutet, dass der Benutzer, der im Feld **Verkäufer-/Einkäufercode** auf der Seite **Genehmigungsbenutzereinrichtung** definiert wurde, den Genehmiger bestimmt. Es werden dann entsprechend des Werts im Feld **Einschränkungsart Genehmiger** Genehmigungsanforderungsposten erstellt.<br />     Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-workflow-users.md)|  
        |**Bestätigungsmeldung anzeigen**|Geben Sie an, ob Benutzern eine Bestätigungsmeldung angezeigt wird, nachdem sie eine Genehmigung angefordert haben.|  
        |**Einschränkungsart Genehmiger**|Gibt an, welchen Einfluss die Genehmigungsgrenzwerte des Genehmigers haben, wenn Genehmigungsanforderungsposten für sie erstellt werden. Ein qualifizierter Genehmiger ist ein Genehmiger, dessen Genehmigungsgrenzwert über dem Wert der Genehmigungsanforderung liegt.<br /><br /> Folgende Optionen sind verfügbar:<br /><br /> 1.  **Genehmigerkette** gibt an, dass Genehmigungsanforderungsposten für alle Genehmiger des Anforderers bis einschließlich dem ersten qualifizierten Genehmiger erstellt werden.<br />2.  **Direkter Genehmiger** gibt an, dass ein Genehmigungsanforderungsposten nur für den direkten Genehmiger des Anforderers erstellt wird, unabhängig vom Genehmigungsgrenzwert des Genehmigers.<br />3.  **Erster qualifizierter Genehmiger** gibt an, dass ein Genehmigungsanforderungsposten nur für den ersten qualifizierten Genehmiger des Anforderers erstellt wird.<br />|  
    3.  Um Optionen für eine Workflowantwort inkl. des Erstellens von Buch.-Blattzeilen festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld|Description|  
        |----------------------------------|---------------------------------------|  
        |**Fibu Buch.-Blattvorlagenname**|Geben Sie den Namen der Buch.-Blattvorlage an, in der die angegebenen Buch.-Blattzeilen erstellt werden.|  
        |**Fibu Buch.-Blattname**|Geben Sie den Namen des Buch.-Blattname an, in den die angegebenen Buch.-Blattzeilen erstellt werden.|  

11. Wählen Sie die Schaltflächen **Einzug vergrößern** und **Einzug verringern** aus, um den Ereignisnamen im Feld **Wenn** einzurücken und die Position des Schritts im Workflow zu definieren.  
    1.  Geben Sie an, dass der Schritt der nächste in der Workflowsequenz ist, indem Sie den Ereignisnamen unter dem Ereignisnamen des vorangegangenen Schrittes einrücken.  
    2.  Geben Sie an, dass der Schritt einer von mehreren alternativen Schritten ist, die abhängig von seiner Bedingung beginnen können, indem Sie den Ereignisnamen an derselben Einrückung wie die anderen alternativen Schritte setzen. Sortieren Sie solche optionalen Schritte entsprechend der Priorität, indem Sie zuerst den wichtigsten Schritt setzen.  

    > [!NOTE]  
    >  Sie können den Einzug eines Schrittes nur ändern, wenn er keinen folgenden Schritt hat.  

12. Wiederholen Sie die Schritte 7 bis 11, um weitere Workflowschritte hinzuzufügen (entweder vor oder nach dem Schritt, den Sie gerade angelegt haben).  
13. Wählen Sie das Kontrollkästchen **Aktiviert**, um anzugeben, dass der Workflow startet, sobald das Ereignis vom Typ **Einstiegspunkt** auftritt. Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).  

> [!NOTE]  
>  Aktivieren Sie keinen Workflow, bevor Sie sicher sind, dass der Workflow abgeschlossen wurde und dass die entsprechenden Workflowschritte beginnen können.  

> [!TIP]  
>  Um Beziehungen zwischen Tabellen anzuzeigen, die in Workflows verwendet werden, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "TTeilen Sie mir mit, was Sie tun möchten.“), und geben Sie dann **Workflow – Tabellenrelationen** ein.  

## <a name="see-also"></a>Siehe auch  
[Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)   
[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)   
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)   
[Löschen eines Workflows](across-how-to-delete-workflows.md)   
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Einrichten von Workflows](across-set-up-workflows.md)   
[Verwenden von Workflows](across-use-workflows.md)   
[Workflow](across-workflow.md)      
