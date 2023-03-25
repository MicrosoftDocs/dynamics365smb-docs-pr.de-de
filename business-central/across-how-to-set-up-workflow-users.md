---
title: So legen Sie Workflow-Benutzer fest
description: 'Bevor Sie Workflows erstellen können, müssen Sie die Benutzer, die daran teilnehmen, auf der Seite Workflow-Benutzergruppen festlegen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Einrichten von Workflowbenutzern

Bevor Sie Genehmigungsworkflows erstellen können, müssen Sie die Benutzer einrichten, die an Workflows teilnehmen. Dies ist notwendig, um beispielsweise festzulegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren.  

Auf der Seite  **Workflow Benutzergruppen** richten Sie Benutzer unter Workflowbenutzergruppen ein und legen die Nummer des Benutzers in einer Prozessfolge fest, zum Beispiel in einer Genehmigerkette. 

Workflowbenutzer, die als Genehmigungsbenutzer agieren (sowohl Genehmigungsanforderer als auch Genehmiger) müssen auch als Workflowbenutzer auf der Seite **Genehmigungsbenutzuer einrichten** eingerichtet werden. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Benutzer diese genehmigt haben, richten Sie Genehmiger in einer Hierarchie ein. Für Genehmigungstypen **Genehmiger** richten Sie auf der Seite **Genehmigungsbenutzereinrichtung** einen Genehmiger ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen**-Fenster fest, und definiert Sie die Hierarchie, indem Sie ansteigende Nummern zu jedem Genehmiger im Feld **Sequenznummer** zuweisen. Feld Erfahren Sie mehr unter [Genehmigungsworkflowbenutzer einrichten](across-how-to-set-up-approval-users.md). 

## So richten Sie Workflowbenutzer ein

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Workflow-Benutzergruppen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow-Genehmigungsgruppe** öffnet sich.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
5. Füllen Sie im Inforegister **Mitglieder der Workflowbenutzergruppe** die Felder in der ersten Zeile gemäß der Beschreibung in der folgenden Tabelle aus.  

   |Feld|Description|
   |-----|-----------|
   |**Benutzername**|Geben Sie den Benutzer an, der in Workflows einbezogen werden soll.<br /><br /> Der Benutzer muss auf der Seite **Benutzereinrichtung** enthalten sein. Weitere Informationen erhalten Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).|
   |**Reihenfolge**|Geben Sie die Reihenfolge an, in der Workflowbenutzer im Verhältnis zu anderen Benutzern in einen Workflow eingebunden werden. Mit diesem Feld können Sie beispielsweise angeben, wann ein Benutzer relativ zu anderen Genehmigern genehmigen kann, indem Sie die Option **Workflow-Benutzergruppe** im Feld **Genehmigungsart** der entsprechenden Workflowreaktion verwenden.| 

   > [!TIP]
   > Um zu definieren, dass eine Genehmigungsanforderung unabhängig von einer Hierarchie von mehreren gleichen Benutzern genehmigt werden muss, richten Sie eine flache Workflowbenutzergruppe ein, indem Sie allen betreffenden Genehmigern die gleiche laufende Nummer zuweisen.

6. Wiederholen Sie Schritt 5, um weitere Workflowbenutzer zur Workflowbenutzergruppe hinzuzufügen.  
7. Wiederholen Sie die Schritte 2 bis 6, um weitere Workflowbenutzergruppen hinzuzufügen.  

## Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## Siehe auch

[Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
