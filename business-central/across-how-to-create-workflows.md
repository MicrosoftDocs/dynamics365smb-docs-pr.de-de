---
title: 'Genehmigungsworkflow erstellen, um Aufgaben zu verbinden'
description: 'Erfahren Sie, wie Sie Workflows erstellen, die Aufgaben verbinden, die von verschiedenen Benutzern in Geschäftsprozessen ausgeführt werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/29/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a>Workflows erstellen, um Aufgaben in Geschäftsprozessen zu verbinden

Sie können Workflows erstellen, die Aufgaben in Geschäftsprozessen verbinden, die von verschiedenen Benutzern ausgeführt werden. Sie können Systemaufgaben, wie automatische Buchung, als Schritte in Workflows aufnehmen, die vor oder nach Benutzeraufgaben erfolgen. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem Trigger und einer Antwort:

* Ein Ereignis, das die Bedingungen angibt, die den Workflow starten.
* Eine Workflowantwort, die definiert, was der Workflow tut.

[!INCLUDE[workflow](includes/workflow.md)]

Wenn Sie Workflows erstellen, können Sie die Schritte aus bestehenden Workflows oder aus Workflowvorlagen kopieren. Workflowvorlagen sind nicht bearbeitbare Workflows, die [!INCLUDE[prod_short](includes/prod_short.md)] bereitstellt. Die Kennung für Workflowvorlagen hat das Präfix „MS-“, z. B. in „MS-PIW“. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Alle Benachrichtigungen über Workflowschritte werden über eine Aufgabenwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange Ihre geschäftlichen Anforderungen widerspiegelt. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen zum Planen von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Abbildung eines Workflow-Beispiels.":::

Ein Workflow ist in drei Abschnitte unterteilt:

1. **Wenn Ereignis**  
   Hierbei wird der Trigger ausgewählt.  
   Beispiele für Auslöser:
   * Ein Stammdatensatz wird geändert
   * eine Buchungsblattzeile wird erstellt
   * Ein eingehender Beleg wird erstellt oder freigegeben
   * Die Genehmigung eines Belegs wird genehmigt
2. **Bei Bedingung**  
   **Bedingungen** bezieht sich auf das Ereignis und ermöglicht das Erstellen von Filtern, um zu entscheiden, wie der Workflow fortgesetzt wird.
3. **Dann Antwort**  
   **Antworten** legen die nächsten Schritte im Workflow fest.

Die Optionen für Ereignisse und Antworten sind systemdefiniert. Um neue Optionen hinzuzufügen, müssen Sie eine Erweiterung entwickeln.

## <a name="to-create-a-workflow"></a>So erstellen Sie einen Workflow

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow** wird geöffnet.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Um den Workflow von einer Workflowvorlage zu erstellen, wählen Sie auf der Seite **Workflows** die Aktion **Neuen Workflow aus Vorlage erstellen**. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).  
5. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
6. Im Feld **Kategorie** legen Sie fest, in welche Kategorie der Workflow gehört.  
7. Geben Sie im Feld **Wenn Ereignis** das Ereignis an, das auftreten muss, um den Workflowschritt zu starten.  

   Wenn Sie das Feld auswählen, führt die Seite **Workflowereignisse** alle verfügbaren Workflowereignisse auf.  
8. Geben Sie im Feld **Bei Bedingung** eine oder mehrere Bedingungen fest, die erfüllt sein müssen, bevor das Ereignis im Feld **Wenn-Ereigniss** auftreten kann.  

   Wenn Sie das Feld auswählen, werden auf der Seite **Ereignisbedingungen** Filterfelder aufgelistet, die Bedingungen für das Ereignis sein können. Sie können bei Bedarf neue Filterfelder hinzufügen.  

   Wenn es sich bei dem Workflowereignis um die Änderung eines bestimmten Felds in einem Datensatz handelt, verwenden Sie die Seite **Ereignisbedingungen** und wählen Sie das Feld und die Art der Änderung aus.  

   1. Um eine Feldänderung für das Ereignis festzulegen, wählen Sie auf der Seite **Ereignisbedingungen** im Feld **Feld** das Feld aus, das sich ändert.  
   2. Geben Sie im Feld **Operator** entweder **Verringert**, **Erhöht** oder **Geändert** aus.  
9. Geben Sie im Feld **Dann Antwort** die Antwort an, die beim Auftreten des Workflowereignisses folgt.  

   Wenn Sie das Feld auswählen, führt die Seite **Workflowantworten** alle verfügbaren Workflowantworten und Antwortoptionen auf.  
10. Geben Sie im Inforegister **Optionen für die ausgewählte Reaktion** die Optionen für die Workflowantwort an, indem Sie in die folgenden Felder Werte eingeben:  

    1. Um Optionen für eine Workflowantwort inkl. des Sendens einer Benachrichtigung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

    > [!NOTE]
    > Diese Felder variieren je nach ausgewählter Antwort.

       |Feld|Description|
       |-----|-----------|
       |**Absender benachrichtigen**|Geben Sie an, ob der Genehmigungsanfordernde anstatt des Genehmigungsanforderungsempfangenden benachrichtigt werden soll. Wenn Sie das Kontrollkästchen aktivieren, wird das Feld **Benutzer-ID des Empfangenden** deaktiviert, da stattdessen der Anfordernde der Genehmigung, der Absendenden, benachrichtigt wird. Der Name der Workflowreaktion ändert sich entsprechend zu **Benachrichtigung erstellen für &lt;Absender&gt;**. Wenn das Kontrollkästchen nicht aktiviert ist, lautet der Name der Workflowantwort **Benachrichtigung erstellen für &lt;Benutzende&gt;**.|
       |**Benutzer-ID des Empfängers**|Geben Sie den Benutzer an, an den Benachrichtigung gesendet werden muss. **Hinweis**: Diese Option ist nur für Workflow-Antworten mit einem Platzhalter für einen bestimmten Benutzer verfügbar. Für Workflowantworten ohne Platzhalter für Benutzer, wird der Benachrichtigungsempfänger in der Regel von der **Genehmigungsbenutzereinrichtung** definiert.|
       |**Benachrichtigungseintragstyp**|Geben Sie einen Trigger für die Workflowbenachrichtigung an. Der Trigger kann eine Datensatzänderung, eine Genehmigungsanfrage oder ein überschrittenes Fälligkeitsdatum sein.|
       |**Zielseite für Link**|Geben Sie die Seite an, die der Link in der Benachrichtigung öffnet. Die Seite muss dieselbe Quellentabelle wie der betreffende Datensatz aufweisen.|
       |**Benutzerdefinierter Link**|Geben Sie die URL eines Links an, der zusätzlich zum Link zur Seite in die Benachrichtigung aufgenommen wird.|

    2. Um Optionen für eine Workflowantwort inkl. des Erstellens von einer Genehmigungsanforderung festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

       |Feld|Description|  
       |-----|-----------|  
       |**Fälligkeitsdatumsformel**|Geben Sie die Anzahl der Tage an, die der Genehmigende hat, um die Anfrage zu lösen. Die Frist beginnt mit der Absendung der Anforderung.|
       |**Delegieren nach**|Geben Sie an, ob und wann eine Anforderung für fällige Genehmigung automatisch an den Stellvertretenden delegiert wird. Sie können eine automatische Delegierung ein, zwei oder fünf Tage nach der Anforderung der Genehmigung auswählen.|
       |**Genehmigertyp**|Geben Sie an, wer gemäß der Einrichtung von Genehmigungsbenutzern und von Workflowbenutzern der Genehmiger ist. Wenn das Feld auf **Verkäufer/Einkäufer** festgelegt ist, bestimmt der Benutzende, der im Feld **Verk.-/Einkäufercode** auf der Seite **Genehmigungsbenutzereinrichtung** den Genehmigenden. Es werden dann entsprechend des Werts im Feld **Einschränkungsart Genehmiger** Genehmigungsanforderungsposten erstellt. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-workflow-users.md).|
       |**Bestätigungsmeldung anzeigen**|Geben Sie an, ob nach Beantragung einer Genehmigung durch Benutzende eine Bestätigungsmeldung angezeigt werden soll.|
       |**Einschränkungsart Genehmiger**|Legen Sie die Auswirkung von Einschränkungen für Genehmigende fest. Eine Genehmigungseinschränkung eines Genehmigenden muss über dem Wert der Anforderung liegen. Folgende Optionen sind verfügbar: <ol><li>**Genehmigerkette** legt fest, dass Genehmigungsanforderungseinträge für alle Genehmigenden des Antragstellers bis einschließlich des ersten qualifizierten Genehmigers erstellt werden</li><li>**Direkter Genehmiger** legt fest, dass ein Genehmigungsanforderungseintrag nur für den unmittelbaren Genehmiger des Anforderers erstellt wird, unabhängig vom Genehmigungslimit des Genehmigers.</li><li>**Erster qualifizierter Genehmigender** gibt an, dass ein Eintrag für eine Genehmigungsanforderung nur für den ersten Genehmigenden des Anfordernden erstellt wird.</li><li>**Bestimmter Genehmiger** gibt an, dass Sie den im Feld **Genehmiger-ID** ausgewählten Benutzer benachrichtigen.</li></ol>|

    3. Um Optionen für eine Workflowantwort inklusive des Erstellens von Buchungsbeiblattzeilen festzulegen, füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.  

       |Feld|Description|  
       |-----|-----------|  
       |**Fibu Buch.-Blattvorlagenname**|Geben Sie den Namen der Buch.-Blattvorlage an, in der die angegebenen Buch.-Blattzeilen erstellt werden.|  
       |**Fibu Buch.-Blattname**|Geben Sie den Namen des Buch.-Blattname an, in den die angegebenen Buch.-Blattzeilen erstellt werden.|  

11. Wählen Sie die Schaltflächen **Einrückung vergrößern** und **Einrückung verkleinern**, um den Namen des Ereignisses im Feld **Wann** einzurücken, um die Position des Schritts im Workflow zu definieren.  

    1. Rücken Sie das Ereignis unter dem Namen des vorherigen Schritts ein, um anzuzeigen, dass es sich um den nächsten Schritt handelt.  
    2. Geben Sie an, dass der Schritt einer von mehreren alternativen Schritten ist, die abhängig von seiner Bedingung beginnen können, indem Sie den Ereignisnamen wie bei den anderen alternativen Schritte setzen. Sortieren Sie solche optionalen Schritte entsprechend der Priorität, indem Sie zuerst den wichtigsten Schritt setzen.  

    > [!NOTE]  
    >  Sie können den Einzug eines Schrittes nur ändern, wenn er keinen folgenden Schritt hat.  

12. Wiederholen Sie die Schritte 7 bis 11, um weitere Workflowschritte vor oder nach dem Schritt, den Sie erstellt haben, hinzuzufügen.  
13. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um anzugeben, dass der Workflow startet, wenn das Ereignis vom Typ **Einstiegspunkt** auftritt. Erfahren Sie mehr unter [Workflows verwenden](across-use-workflows.md).  

> [!NOTE]  
> Aktivieren Sie einen Workflow erst, wenn Sie sicher sind, dass er bereit ist.  

> [!TIP]  
> Um die Beziehungen zwischen Tabellen zu erkunden, die in Workflows verwendet werden, wählen Sie die ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, und geben Sie dann **Workflow – Tabellenbeziehungen** ein.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Beispiel für das Erstellen eines neuen Workflows unter Verwendung vorhandener Ereignisse

Das folgende Beispiel erstellt einen neuen Workflow, um den Namen eines Kreditors zu ändern:

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
    2. Im Feld **Bei Bedingung** wählen Sie das Wort **Immer**. Wählen Sie dann auf der Seite **Ereignisbedingungen** den Link **Bedingung hinzufügen, wenn sich ein Feldwert ändert**, und wählen Sie dann das Feld **Name**. Das Ergebnis dieses Schritts ist, dass die Bedingung als *Name ist geändert* lautet.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort wählen** die Antwort **Den Wert des Feldes \<Field\> im Datensatz zurücksetzen und die Änderung speichern**. Geben Sie dann im Abschnitt **Optionen für die ausgewählte Antwort** das Feld **Name** an.  
    4. Wählen Sie den Link **Weitere Antworten hinzufügen** und fügen Sie dann einen Eintrag für die Antwort **Erstellen Sie eine Genehmigungsanfrage für den Datensatz unter Verwendung der Genehmiger-Typen <%1> und <%2>**.  
    5. Ändern Sie im Abschnitt **Optionen für die ausgewählte Antwort** für die neue Antwort das Feld **Genehmigungstyp** in **Workflow-Benutzergruppe**. Geben Sie dann im Feld **Workflow-Benutzergruppe** die Benutzergruppe an. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md).  
    6. Fügen Sie eine dritte Antwort hinzu, **Senden Sie eine Genehmigungsanfrage für den Datensatz und erstellen Sie eine Benachrichtigung**.  
    7. Fügen Sie eine vierte Antwort **Nachricht „%1“ anzeigen** hinzu. Geben Sie dann im Abschnitt **Optionen für die ausgewählte Antwort** im Feld **Nachricht** **Eine Genehmigungsanforderung wurde gesendet** aus.  
    8. Wählen Sie die **OK** aus, um zum Workflow-Schritt zurückzukehren.  

5. Fügen Sie in der nächsten Zeile einen neuen Workflowschritt für das Ereignis **Eine Genehmigungsanforderung wird genehmigt** hinzu.

    1. Geben Sie im Feld **Wann Ereignis** an: **Ein Genehmigungsantrag wird genehmigt**.  
    2. Wählen Sie das Zeilenmenü und wählen Sie dann **Einzug vergrößern**.  
    3. Wählen Sie im Feld **Bei Bedingung** **Immer** aus. Geben Sie dann im Feld **Anstehende Genehmigungen** **0** an. Die Bedingung wird als **Anstehende Genehmigungen:0** gelesen, um anzuzeigen, dass für die Anforderung nicht mehr Genehmigende notwendig sind.  
    4. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort **Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen**.  
    5. Wählen Sie **OK** aus.  
6. Fügen Sie in der nächsten Zeile einen zweiten Workflow-Schritt für das Ereignis **Ein Genehmigungsantrag wird genehmigt** hinzu.  

    1. Geben Sie im Feld **Wann Ereignis** an: **Ein Genehmigungsantrag wird genehmigt**.
    2. Wählen Sie im Feld **Bei Bedingung** **Immer** aus. Geben Sie dann im Feld **Anstehende Genehmigungen** **>0** an. Die Bedingung wird als **Anstehende Genehmigungen:0** gelesen, um anzuzeigen, dass dies nicht der letzte Genehmigende ist.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort **Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen**.  
    4. Wählen Sie **OK** aus.  
7. Fügen Sie in der nächsten Zeile einen Workflow-Schritt für das Ereignis **Ein Genehmigungsantrag wird delegiert** hinzu.  

    1. Geben Sie im Feld **Wann-Ereignis** **Ein Genehmigungsantrag wird genehmigt** an.  
    2. Im Feld **Bei Bedingung** lassen Sie den Wert auf **Immer**.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der Seite **Workflow-Antworten** im Feld **Antwort auswählen** die Antwort **Genehmigungsanfrage für den Datensatz senden und eine Benachrichtigung erstellen**.  
    4. Wählen Sie **OK** aus.  
8. Fügen Sie in der nächsten Zeile einen zweiten Workflow-Schritt für das Ereignis **Ein Genehmigungsantrag wird abgelehnt** hinzu.  

    1. Geben Sie im Feld **Wann Ereignis** an: **Ein Genehmigungsantrag wird abgelehnt**.  
    2. Im Feld **Bei Bedingung** lassen Sie den Wert auf **Immer**.  
    3. Wählen Sie im Feld **Dann Antwort** den Link **Antwort auswählen** aus. Wählen Sie dann auf der **Workflow-Antworten** Seite im Feld **Antwort auswählen** die Antwort **Verwerfen Sie die neuen Werte**.  
    4. Wählen Sie den Link **Weitere Antworten hinzufügen** und fügen Sie dann einen Eintrag für die Antwort **Die Genehmigungsanfrage für den Datensatz ablehnen und eine Benachrichtigung erstellen** hinzu
    5. Wählen Sie **OK** aus.  
9. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um den Workflow zu aktivieren.  

Die folgende Abbildung gibt einen Überblick über das Ergebnis dieses Vorgangs.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Abbildung des Workflows zur Genehmigung des Namens des Kreditors.":::

Testen Sie als nächstes den Workflow, indem Sie eine vorhandene Kreditorkarte öffnen und ihren Namen ändern. Überprüfen Sie, ob nach der Änderung des Kreditorennamens ein Genehmigungsantrag gesendet wird.

## <a name="see-also"></a>Siehe auch

[Workflows aus Workflowvorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md)  
[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)  
[Einrichten von Genehmigungs-Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Artikelgenehmigungsworkflow löschen](across-how-to-delete-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
