---
title: Erstellen von Genehmigungs-Workflows zur Verbindung von Aufgaben
description: Erfahren Sie, wie Sie Workflows erstellen, die Aufgaben verbinden, die von verschiedenen Benutzern in Geschäftsprozessen ausgeführt werden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/11/2022
ms.author: bholtorf
ms.openlocfilehash: 0d84da534c754ba7b0f6d1de97b61634ff743ddc
ms.sourcegitcommit: 9bba11d474e21711cc8e2afefee8efb473170707
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9763256"
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a>Workflows erstellen, um Aufgaben in Geschäftsprozessen zu verbinden

Sie können Workflows erstellen, die Aufgaben in Geschäftsprozessen verbinden, die von verschiedenen Benutzern ausgeführt werden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer Workflowantwort mit Antwortoptionen. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

[!INCLUDE[workflow](includes/workflow.md)]

Wenn Sie Workflows erstellen, können Sie die Schritte aus bestehenden Workflows oder aus Workflowvorlagen kopieren. Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] finden. Dem Code für Workflow-Muster, die von Microsoft hinzugefügt werden, wird ein „MS-„ vorangestellt, z. B. in „MS-PIW“. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Alle Benachrichtigungen über Workflowschritte werden über eine Aufgabenwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange Ihre geschäftlichen Anforderungen widerspiegelt. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen zum Planen von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Abbildung eines Workflow-Beispiels.":::

Der Workflow ist in drei Abschnitte unterteilt:

1. **Wenn-Ereignis**  
   Hierbei wird der Trigger ausgewählt.  
   Beispiele für Auslöser:
   * Ein Stammdatensatz wird geändert
   * eine Buchungsblattzeile wird erstellt
   * Ein eingehender Beleg wird erstellt oder freigegeben
   * Die Genehmigung eines Belegs wird genehmigt
2. **Bei Bedingung**  
   **Bedingungen** bezieht sich auf das Ereignis und ermöglicht das Erstellen von Filtern, um zu entscheiden, wie der Workflow fortgesetzt wird.
3. **Dann-Antwort**  
   **Antworten** legen die nächsten Schritte im Workflow fest.

Für Ereignisse und Antworten gilt, dass die Optionen systemdefiniert sind. Neue Ereignisse müssen durch die Entwicklung einer Erweiterung hinzugefügt werden.

## <a name="to-create-a-workflow"></a>So erstellen Sie einen Workflow

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow** wird geöffnet.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Um den Workflow von einer Workflowvorlage zu erstellen, wählen Sie auf der Seite **Workflows** die Aktion **Neuen Workflow aus Vorlage erstellen**. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).  
5. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
6. Im Feld **Kategorie** legen Sie fest, in welche Kategorie der Workflow gehört.  
7. Geben Sie im Feld **Wenn Ereignis** das Ereignis an, das auftreten muss, um den Workflowschritt zu starten.  

   Wenn Sie das Feld auswählen, wird die Seite **Workflow-Ereignisse** geöffnet, und Sie können alle verfügbaren Workflowereignisse auswählen.  
8. Geben Sie im Feld **Bei Bedingung** eine oder mehrere Bedingungen fest, die erfüllt sein müssen, bevor das Ereignis im Feld **Wenn-Ereigniss** auftreten kann.  

   Wenn Sie das Feld auswählen, wird die **Ereignisbedigungen**-Seite geöffnet. In diesem wählen Sie aus einer Liste mit Filterfeldern die Bedingungen aus, die zum jeweiligen Ereignis relevant sind. Sie können neue Filterfelder hinzufügen, die Sie als Ereignisbedingungen verwenden möchten. Die Ereignisbedingungsfilter konfigurieren Sie so wie die Filter für Berichtsanforderungsseiten.  

   Wenn es sich bei dem Workflowereignis um die Änderung eines bestimmten Felds in einem Datensatz handelt, wird die Seite **Ereignisbedingungen** geöffnet. Dort können Sie Optionen für das Feld und die Art der Änderung auswählen.  

   1. Um eine Feldänderung für das Ereignis festzulegen, wählen Sie auf der Seite **Ereignisbedingungen** im Feld **Feld** das Feld aus, das sich ändert.  
   2. Geben Sie im Feld **Operator** entweder **Verringert**, **Erhöht** oder **Geändert** aus.  
9. Geben Sie im Feld **Dann Antwort** die Antwort an, die beim Auftreten des Workflowereignisses folgt.  

   Wenn Sie das Feld auswählen, wird die Seite **Workflow-Antworten** geöffnet, das alle verfügbaren Workflowantworten zur Auswahl anbietet und in dem Sie Antwortoptionen für die gewählte Antwort festlegen können.  
10. Geben Sie im Inforegister **Optionen für die ausgewählte Reaktion** die Optionen für die Workflowantwort an, indem Sie in die folgenden Felder Werte eingeben:  

    1. Um Optionen für eine Workflowantwort inkl. des Sendens einer Benachrichtigung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

    > [!NOTE]
    > Diese Felder variieren je nach ausgewählter Antwort.

       |Feld|Description|
       |-----|-----------|
       |**Absender benachrichtigen**|Geben Sie an, ob der Genehmigungsanforderer anstatt des Genehmigungsanforderungsempfängers benachrichtigt wird. Wenn Sie das Kontrollkästchen aktivieren, wird das Feld **Benutzer-ID des Empfängers** deaktiviert, da stattdessen der Anforderer der Genehmigung, der Absender, benachrichtigt wird. Der Name der Workflowreaktion ändert sich entsprechend zu **Benachrichtigung erstellen für &lt;Absender&gt;**. Wenn das Kontrollkästchen nicht aktiviert ist, lautet der Name der Workflowreaktion **Benachrichtigung erstellen für &lt;Benutzer&gt;**.|
       |**Benutzer-ID des Empfängers**|Geben Sie den Benutzer an, an den Benachrichtigung gesendet werden muss. **Hinweis**: Diese Option ist nur für Workflow-Antworten mit einem Platzhalter für einen bestimmten Benutzer verfügbar. Für Workflowantworten ohne Platzhalter für Benutzer, wird der Benachrichtigungsempfänger in der Regel von der **Genehmigungsbenutzereinrichtung** definiert.|
       |**Benachrichtigungseintragstyp**|Geben Sie an, ob die Workflowbenachrichtigung durch eine Datensatzänderung, eine Genehmigungsanforderung oder übergebene fällige Daten ausgelöst wird.|
       |**Zielseite für Link**|Geben Sie eine andere Seite an, die der Link in der Benachrichtigung anstelle der Standardseite öffnet. Die Seite muss dieselbe Quellentabelle wie der betreffende Datensatz aufweisen.|
       |**Benutzerdefinierter Link**|Geben Sie die URL eines Links an, der zusätzlich zum Link zur Seite in die Benachrichtigung aufgenommen wird.|

    2. Um Optionen für eine Workflowantwort inkl. des Erstellens von einer Genehmigungsanforderung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

       |Feld|Description|  
       |-----|-----------|  
       |**Fälligkeitsdatumsformel**|Geben Sie an, in wievielen Tagen eine die Genehmigungsanforderung ab dem Datum, an dem sie gesendet wurde, abgeschlossen werden muss.|
       |**Delegieren nach**|Geben Sie an, ob und wann eine Anforderung für fällige Genehmigung automatisch an den relevanten Stellvertreter delegiert wird. Sie können eine automatische Delegierung ein, zwei oder fünf Tage nach der Anforderung der Genehmigung auswählen.|
       |**Genehmigertyp**|Geben Sie an, wer gemäß der Einrichtung von Genehmigungsbenutzern und von Workflowbenutzern der Genehmiger ist. Wenn das Feld auf **Verkäufer/Einkäufer** festgelegt ist, bestimmt der Benutzer, der im Feld **Verk.-/Einkäufercode** auf der Seite **Genehmigungsbenutzereinrichtung** den Genehmiger. Es werden dann entsprechend des Werts im Feld **Einschränkungsart Genehmiger** Genehmigungsanforderungsposten erstellt. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-workflow-users.md).|
       |**Bestätigungsmeldung anzeigen**|Geben Sie an, ob Benutzern eine Bestätigungsmeldung angezeigt wird, nachdem sie eine Genehmigung angefordert haben.|
       |**Einschränkungsart Genehmiger**|Geben Sie an, wie sich die Genehmigungsgrenzen des Genehmigers darauf auswirken, wann Genehmigungsanforderungseinträge für sie erstellt werden. Ein qualifizierter Genehmiger ist ein Genehmiger, dessen Genehmigungsgrenzwert über dem Wert der Genehmigungsanforderung liegt. Folgende Optionen sind verfügbar: <ol><li>**Genehmigerkette** legt fest, dass Genehmigungsanforderungseinträge für alle Genehmigenden des Antragstellers bis einschließlich des ersten qualifizierten Genehmigers erstellt werden</li><li>**Direkter Genehmiger** legt fest, dass ein Genehmigungsanforderungseintrag nur für den unmittelbaren Genehmiger des Anforderers erstellt wird, unabhängig vom Genehmigungslimit des Genehmigers.</li><li>**Erster qualifizierter Genehmiger** gibt an, dass ein Eintrag für eine Genehmigungsanfrage nur für den ersten qualifizierten Genehmiger des Antragstellers erstellt wird.</li><li>**Bestimmter Genehmiger** gibt an, dass Sie den im Feld **Genehmiger-ID** ausgewählten Benutzer benachrichtigen.</li></ol>|
    3. Um Optionen für eine Workflowantwort inkl. des Erstellens von Buch.-Blattzeilen festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

       |Feld|Description|  
       |-----|-----------|  
       |**Fibu Buch.-Blattvorlagenname**|Geben Sie den Namen der Buch.-Blattvorlage an, in der die angegebenen Buch.-Blattzeilen erstellt werden.|  
       |**Fibu Buch.-Blattname**|Geben Sie den Namen des Buch.-Blattname an, in den die angegebenen Buch.-Blattzeilen erstellt werden.|  

11. Wählen Sie die Schaltflächen **Einrückung vergrößern** und **Einrückung verkleinern**, um den Namen des Ereignisses im Feld **Wann** einzurücken, um die Position des Schritts im Workflow zu definieren.  

    1. Geben Sie den nächsten Schritt in der Workflowsequenz an, indem Sie den Ereignisnamen unter dem Ereignisnamen des vorangegangenen Schrittes einrücken.  
    2. Geben Sie an, dass der Schritt einer von mehreren alternativen Schritten ist, die abhängig von seiner Bedingung beginnen können, indem Sie den Ereignisnamen wie bei den anderen alternativen Schritte setzen. Sortieren Sie solche optionalen Schritte entsprechend der Priorität, indem Sie zuerst den wichtigsten Schritt setzen.  

    > [!NOTE]  
    >  Sie können den Einzug eines Schrittes nur ändern, wenn er keinen folgenden Schritt hat.  

12. Wiederholen Sie die Schritte 7 bis 11, um weitere Workflowschritte vor oder nach dem Schritt, den Sie erstellt haben, hinzuzufügen.  
13. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um anzugeben, dass der Workflow startet, sobald das Ereignis vom Typ **Einstiegspunkt** auftritt. Erfahren Sie mehr unter [Workflows verwenden](across-use-workflows.md).  

> [!NOTE]  
> Aktivieren Sie keinen Workflow, bevor Sie sicher sind, dass der Workflow abgeschlossen wurde und dass die entsprechenden Workflowschritte beginnen können.  

> [!TIP]  
> Um Beziehungen zwischen Tabellen zu sehen, die in Workflows verwendet werden, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, und geben Sie dann **Workflow – Tabellenbeziehungen** ein.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Beispiel für das Erstellen eines neuen Workflows unter Verwendung vorhandener Ereignisse

Im folgenden Beispiel wird ein neuer Workflow erstellt, um Änderungen am Namen eines bestehenden Kreditors zu genehmigen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow** wird geöffnet.
3. Füllen Sie im Workflow-Abschnitt die Felder wie in der folgenden Tabelle beschrieben aus.

    |Feld  |Wert  |
    |---------|---------|
    |**Code**|**VENDAPN-01**|
    |**Beschreibung**|**Genehmigung der Änderung des Kreditorennamens** |
    |**Kategorie**|**PURCH**|

4. Um den ersten Workflow-Schritt zu erstellen, gehen Sie wie folgt vor.

    1. Geben Sie im Feld **Wann Ereignis** an: *Ein Datensatz des Kreditors wird geändert*.  
    2. Im Feld **Bei Bedingung** wählen Sie das Wort **Immer**. Wählen Sie dann auf der Seite **Ereignisbedingungen** den Link **Bedingung hinzufügen, wenn sich ein Feldwert ändert**, und wählen Sie dann das Feld *Name*. Das Ergebnis dieses Schritts ist, dass die Bedingung als *Name ist geändert* lautet.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort wählen** die Antwort *Den Wert des Feldes \<Field\> im Datensatz zurücksetzen und die Änderung speichern*. Geben Sie dann im Abschnitt **Optionen für die ausgewählte Antwort** das Feld *Name* an.  
    4. Wählen Sie den Link **Weitere Antworten hinzufügen** und fügen Sie dann einen Eintrag für die Antwort *Erstellen Sie eine Genehmigungsanfrage für den Datensatz unter Verwendung der Genehmiger-Typen <%1> und <%2>*.  
    5. Ändern Sie im Abschnitt **Optionen für die ausgewählte Antwort** für die neue Antwort das Feld **Genehmigungstyp** in *Workflow-Benutzergruppe* und geben Sie dann im Feld **Workflow-Benutzergruppe** die entsprechende Benutzergruppe an. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md).  
    6. Fügen Sie eine dritte Antwort hinzu, *Senden Sie eine Genehmigungsanfrage für den Datensatz und erstellen Sie eine Benachrichtigung.*  
    7. Fügen Sie eine vierte Antwort hinzu, *Nachricht "%1" anzeigen*, und geben Sie dann im Abschnitt **Optionen für die ausgewählte Antwort** im Feld **Nachricht** an: **Eine Genehmigungsanfrage wurde gesendet**.  
    8. Wählen Sie die **OK** aus, um zum Workflow-Schritt zurückzukehren.  

5. Fügen Sie in der nächsten Zeile einen neuen Workflow-Schritt für das *Ein Genehmigungsantrag wurde genehmigt.* Ereignis.

    1. Geben Sie im Feld **Wann Ereignis** an: *Ein Genehmigungsantrag wird genehmigt*.  
    2. Wählen Sie das Zeilenmenü und wählen Sie dann **Einzug vergrößern**.  
    3. Wählen Sie im Feld **Bei Bedingung** das Wort **Immer** und geben Sie dann im Feld **Anstehende Genehmigungen** *0* an. Das Ergebnis dieses Schritts ist, dass die Bedingung als *Ausstehende Genehmigungen:0* gelesen wird, um anzuzeigen, dass dies der letzte Genehmigende ist.  
    4. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort *Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen*.  
    5. Wählen Sie **OK** aus.  
6. Fügen Sie in der nächsten Zeile einen zweiten Workflow-Schritt für das Ereignis *Ein Genehmigungsantrag wird genehmigt* hinzu.  

    1. Geben Sie im Feld **Wann Ereignis** an: *Ein Genehmigungsantrag wird genehmigt*.
    2. Wählen Sie im Feld **Bei Bedingung** das Wort **Immer** und geben Sie dann im Feld **Anstehende Genehmigungen** *>0* an. Das Ergebnis dieses Schritts ist, dass die Bedingung als *Ausstehende Genehmigungen:>0* gelesen wird, um anzuzeigen, dass dies *nicht* der letzte Genehmiger ist.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort *Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen*.  
    4. Wählen Sie **OK** aus.  
7. Fügen Sie in der nächsten Zeile einen Workflow-Schritt für das Ereignis *Ein Genehmigungsantrag wird delegiert* hinzu.  

    1. Geben Sie im Feld **Wann-Ereignis** *Ein Genehmigungsantrag wird genehmigt* an.  
    2. Im Feld **Bei Bedingung** lassen Sie den Wert auf *Immer*.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort *Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen*.  
    4. Wählen Sie **OK** aus.  
8. Fügen Sie in der nächsten Zeile einen zweiten Workflow-Schritt für das Ereignis *Ein Genehmigungsantrag wird abgelehnt* hinzu.  

    1. Geben Sie im Feld **Wann Ereignis** an: *Ein Genehmigungsantrag wird abgelehnt*.  
    2. Im Feld **Bei Bedingung** lassen Sie den Wert auf *Immer*.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der **Workflow-Antworten** Seite im Feld **Antwort auswählen** die Antwort *Verwerfen Sie die neuen Werte*.  
    4. Wählen Sie den Link **Weitere Antworten hinzufügen** und fügen Sie dann einen Eintrag für die Antwort *Die Genehmigungsanfrage für den Datensatz ablehnen und eine Benachrichtigung erstellen* hinzu
    5. Wählen Sie **OK** aus.  
9. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um den Workflow zu aktivieren.  

Die folgende Abbildung gibt einen Überblick über das Ergebnis dieses Vorgangs.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Abbildung des Workflows zur Genehmigung des Namens des Kreditors.":::

Testen Sie als nächstes den Workflow, indem Sie eine vorhandene Kreditorkarte öffnen und ihren Namen ändern. Überprüfen Sie, ob nach der Änderung des Kreditorennamens ein Genehmigungsantrag gesendet wird.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)  
[Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)  
[Einrichten von Genehmigungs-Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Artikelgenehmigungsworkflow löschen](across-how-to-delete-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
